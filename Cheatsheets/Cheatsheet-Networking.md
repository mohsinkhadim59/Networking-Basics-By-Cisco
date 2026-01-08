


>[! Notes] 
>- This md file contains all the necessary commands that are learnt throughout this course.



```dataviewjs
// ---------- Helper functions for numeric file sorting ----------
function parseFileNumber(name) {
    // Extract leading numeric part: "12.3.4 Something" → [12,3,4]
    let match = name.match(/^(\d+(?:\.\d+)*)/);
    if (!match) return [];
    return match[1].split(".").map(n => parseInt(n, 10));
}

function compareFileNumbers(a, b) {
    let len = Math.max(a.length, b.length);
    for (let i = 0; i < len; i++) {
        let x = a[i] ?? 0;
        let y = b[i] ?? 0;
        if (x !== y) return x - y;
    }
    return 0;
}

// ---------- Collect pages ----------
let pages = dv.pages().where(p => /^\d+(\.\d+)*\s+.+$/i.test(p.file.name));
let merged = new Map();

// ---------- Scan files ----------
for (let p of pages) {
    if (!p.file.path) continue;

    let content = await dv.io.load(p.file.path);
    if (!content) continue;

    let lines = content.split(/\r?\n/);
    let inTable = false;

    for (let line of lines) {
        let trimmed = line.trim();

        // Detect table header
        if (trimmed.toLowerCase().startsWith("| command")) {
            inTable = true;
            continue;
        }

        if (!inTable) continue;

        // End of table
        if (trimmed === "" || !line.includes("|")) {
            inTable = false;
            continue;
        }

        if (line.includes("---")) continue;

        let parts = line.split("|").map(c => c.trim());

        // Expected columns:
        // | Command | Description | Category |
        if (parts.length >= 4) {
            let cmdPlain = parts[1];
            let desc = parts[2];
            let catField = parts[3];
            let from = `[[${p.file.name}]]`;

            let cats = catField
                .split(",")
                .map(c => c.trim())
                .filter(Boolean);

            for (let cat of cats) {
                let key = `${cat.toLowerCase()}|${cmdPlain.toLowerCase()}`;

                if (!merged.has(key)) {
                    merged.set(key, {
                        cmdRaw: cmdPlain,
                        desc: desc,
                        category: cat,
                        froms: new Set([from])
                    });
                } else {
                    merged.get(key).froms.add(from);
                }
            }
        }
    }
}

// ---------- Build sorted rows ----------
let rows = Array.from(merged.values())
    .map(r => {
        // Sort source files numerically
        let sortedFroms = Array.from(r.froms).sort((a, b) => {
            let fa = parseFileNumber(a.replace(/\[\[|\]\]/g, ""));
            let fb = parseFileNumber(b.replace(/\[\[|\]\]/g, ""));
            return compareFileNumbers(fa, fb);
        });

        return {
            cmd: r.cmdRaw,
            desc: r.desc,
            cat: r.category,
            froms: sortedFroms,
            firstFile: parseFileNumber(
                sortedFroms[0].replace(/\[\[|\]\]/g, "")
            )
        };
    })
    // Sort rows by earliest source file
    .sort((a, b) => compareFileNumbers(a.firstFile, b.firstFile))
    .map(r => [
        r.cmd,
        r.desc,
        r.cat,
        r.froms.join("<br>")
    ]);

// ---------- Render table ----------
dv.table(
    ["Command", "Description", "Category", "Source File"],
    rows
);

```
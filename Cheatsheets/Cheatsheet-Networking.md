


>[! Notes] 
>- This md file contains all the necessary commands that are learnt throughout this course.



```dataviewjs
let pages = dv.pages().where(p => /^\d+(\.\d+)*\s+.+$/i.test(p.file.name));
let merged = new Map();

for (let p of pages) {
    // Safety: ensure we are looking at a file path
    if (!p.file.path) continue;
    
    let content = await dv.io.load(p.file.path);
    if (!content) continue;
    
    let lines = content.split(/\r?\n/);
    let inTable = false;

    for (let line of lines) {
        let trimmed = line.trim();
        
        // Detect table header - matches "| Command" regardless of trailing content
        if (trimmed.toLowerCase().startsWith("| command")) {
            inTable = true;
            continue;
        }

        if (inTable) {
            // Stop if the table ends
            if (trimmed === "" || !line.includes("|")) {
                inTable = false;
                continue;
            }
            if (line.includes("---")) continue;

            let parts = line.split("|").map(c => c.trim());
            
            // Expected: | (parts[0]) | Command (1) | Description (2) | Category (3) |
            if (parts.length >= 4) {
                let cmdPlain = parts[1];
                let desc = parts[2];
                let catField = parts[3];
                let from = `[[${p.file.name}]]`;

                // Split categories by comma in case one command has multiple categories
                let cats = catField.split(",").map(c => c.trim()).filter(c => c);
                for (let c of cats) {
                    if (c.toLowerCase() === "network") {
                        // Key includes category and command to ensure uniqueness
                        let key = "network|" + cmdPlain.toLowerCase();
                        
                        if (!merged.has(key)) {
                            merged.set(key, { 
                                cmdRaw: cmdPlain, 
                                cmdPlain: cmdPlain, 
                                desc: desc, 
                                froms: new Set([from]) 
                            });
                        } else {
                            merged.get(key).froms.add(from);
                        }
                    }
                }
            }
        }
    }
}

let rows = Array.from(merged.values())
    .sort((a, b) => a.cmdPlain.localeCompare(b.cmdPlain))
    .map(r => [
        r.cmdRaw,
        r.desc,
        Array.from(r.froms).join("<br>")
    ]);

dv.table(["Command", "Description", "Source File"], rows);
```
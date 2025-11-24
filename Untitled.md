> [!step] **Step 1 — A frame arrives**
> A switch receives an Ethernet frame on one of its ports.

---

> [!step] **Step 2 — Switch checks the **source MAC**
> The switch looks at the *source MAC address* in the frame.
> Example: Frame arrives on port **Fa0/1** with source MAC **AAAA.AAAA.AAAA**

---

> [!step] **Step 3 — Switch LEARNS**
> The switch adds this entry to its MAC table:
> **AAAA.AAAA.AAAA → Fa0/1**
>  
> If the entry already exists, the switch simply **refreshes** its 5-minute timer.

---

> [!step] **Step 4 — Switch checks destination MAC**
> If the MAC exists in the table:
> → It forwards the frame **only** out that port.  
> If NOT:
> → It **floods** the frame out all ports except the incoming one.

---

> [!step] **Step 5 — Aging timer starts**
> Each MAC entry has a **300-second (5-minute)** aging timer.
> If no frames are received from that MAC within 5 minutes → entry is deleted.

---

> [!step] **Result**
> The MAC table constantly updates as hosts send traffic.
> This is how switches learn and maintain a dynamic forwarding database.

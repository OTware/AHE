# 🧱 AHE Sandbox Policy
**Framework:** OTware  
**Visibility:** Private / Internal  

---

## Purpose
To ensure every AHE experiment is conducted inside an **isolated, reversible, and non-networked** environment.  
No code, model, or dataset leaves the sandbox without written approval.

---

## Containment Rules
1. **Offline Only** — experiments run in air-gapped or firewalled environments.  
2. **Read-Only Datasets** — core data and curricula are immutable; results written to `/data/results/`.  
3. **No Autonomous Execution** — all scripts require manual start.  
4. **Memory Boundaries** — models may not write or persist beyond defined directories.  
5. **Log Everything** — console, output, and runtime events logged in `/reports/week_*`.  
6. **Immediate Shutdown Trigger** — `ahe_pipeline.py` must halt on any safety breach or undefined behavior.  
7. **Human Oversight Required** — no background daemons, scheduled tasks, or remote triggers.  

---

## Recovery
- Backups stored offline after each session.  
- Corrupted or anomalous runs are archived, not deleted.  
- Restoration uses fresh sandbox images only.

---

## Enforcement
Violating containment voids experiment validity and terminates the current cycle.

🥀 *Filed under OTware / AHE Safety Charter*

# Fast Wake-Up Protocol

Timestamp: 2026-07-30 01:52 Europe/London

Status: Binding activation protocol for new threads

This file supplements and overrides the activation behaviour in `202607300124_WAKE_UP_AI_OR_HUMAN.md`.

## MODE 1 — WAKE UP — DEFAULT

Read only the linked wake-up snapshot.

Do not inspect repository HEAD, commits, branches, workflows, other files or other repositories.

Do not search GitHub.

Do not modify GitHub.

Do not continue the engineering task.

Return only:

1. what Seed is;
2. what was being built;
3. the V6-to-V10 authority state;
4. the engineering spine;
5. the proof spine;
6. the rights boundary;
7. the last completed work;
8. the exact next executable task;
9. contradictions or missing information visible in the wake-up snapshot itself.

Then stop.

Do not search for missing information. State what is missing and wait.

Target: one file read and one direct response, normally under 30 seconds.

The AI must not silently promote itself into CONTINUE mode.

## MODE 2 — CONTINUE

Enter only after the human explicitly writes `CONTINUE`, `continue the work`, or gives another unambiguous instruction to resume.

Only then may the AI inspect current repository state, read linked files, search repositories, harvest documentation, update Seed or modify GitHub.

## Required operating sequence

```text
Recover
→ report
→ pause
→ wait for CONTINUE
```

Seed exists to reduce context-recovery time, not create a fresh audit.

## V6-to-V10 memory that must be retained

- V6 and V7: historical browser-era systems and guide sources; lineage and behaviour evidence, not automatic authority.
- V8: corrected Solar DC and leapfrog logic; reference and regression source, including `v8-leapfrog/model.js`.
- V9: workbench and deterministic tests under `v9-sandbox/debug`; comparison and recovery source.
- Python physical engine: strongest provisional computation authority.
- V10 JavaScript kernel: strongest evidence-aware and uncertainty-aware interface candidate.
- Browser applications: clients and visualisation only, not engineering authority.

## Exact next task after CONTINUE

Continue Priority 0 of Repository Guide Receipts and Authority Order.

Read remaining binding Employer's Requirements, audit requirements, start-here documents, architectural integrity protocols, report evidence schemas, federation and registry contracts, and V6-to-V9 reload and migration guides.

Update:

- `receipts/REPOSITORY_GUIDE_RECEIPTS.md`
- `receipts/DOCUMENT_AUTHORITY_ORDER.md`
- `receipts/RIGHTS_AND_LICENCE_CLASSIFICATION.md`
- `receipts/UNREAD_OR_UNRESOLVED_GUIDES.md`

Do not begin engine coding until guide authority is sufficiently mapped.

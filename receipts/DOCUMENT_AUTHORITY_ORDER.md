# Document Authority Order

## Purpose

This document defines how Seed resolves instruction order when several repositories, guides, reports and historical notes address the same work.

The existence of many documents is a strength only if their authority is explicit. Without an authority order, a historical roadmap can accidentally overrule a current Employer's Requirement, a browser note can be mistaken for engineering truth, or an audit report can be mistaken for policy.

## Core principle

The most specific current lawful instruction for the relevant scope governs, provided it does not conflict with a higher external authority.

Authority is not determined by file age, file size, eloquence, repository popularity or the identity of the tool that wrote it.

## Authority ladder

### Level 0 — Physical reality and established mathematics

Physical law, dimensional consistency, observed system behaviour and reproducible mathematics constrain every lower layer.

A document cannot make an impossible circuit possible or turn a dimensionally invalid equation into engineering truth.

Disagreement at this level requires evidence, experiment, measurement or stronger derivation.

### Level 1 — Applicable law, regulation and binding external obligations

Includes, where applicable:

- statute;
- regulation;
- licence condition;
- grid code;
- planning or environmental obligation;
- binding contract;
- binding Employer's Requirement;
- binding manufacturer limitation;
- court or regulator decision.

Seed records these authorities and their scope but does not provide legal status merely by labelling a document.

### Level 2 — Approved project or repository scope

Examples:

- approved Employer's Requirement;
- approved scope statement;
- signed-off architecture decision;
- repository-local binding requirement;
- explicit human owner decision recorded with date and scope.

A document at this level defines what is to be built, what is excluded and who approves it.

Example already observed:

`data-federation-map-for-globalgrid2050-all-repos/every-drop-is-the-ocean/FEDERATION_LEDGER_SCOPE_EMPLOYERS_REQUIREMENT.md`

It expressly states that it is binding scope and must not be exceeded.

### Level 3 — Canonical doctrine and architecture

Examples:

- canonical data doctrine;
- authoritative engine recovery plan;
- architecture contract;
- current data contract;
- current schema contract;
- current operating manual.

These govern implementation within their declared scope.

Examples already observed:

- `globalgrid2050/data_science_protocol/THE_DATA_SPINE.md`;
- `solar-electrical-topology-analysis-engine-text-based/v10-development/recovery/V10_ENGINE_RECOVERY_PLAN.md`;
- `globalgrid2050/AI_GRIDBOT_START_HERE.md` for GridBot-governed production changes.

### Level 4 — Current operational procedures

Examples:

- audit procedure;
- workflow trigger guide;
- release process;
- rollback process;
- human operator manual;
- current AI read-first guide;
- current reload instructions.

These control how approved work is carried out. They do not silently expand scope or redefine physics.

### Level 5 — Verified evidence receipts

Examples:

- audit report;
- apply report;
- independent verification report;
- test report;
- measurement record;
- clean-clone receipt;
- DuckDB data-law proof;
- comparison report.

Evidence receipts establish what happened or what passed. They do not automatically create policy.

A green workflow is evidence of a run, not proof that the underlying engineering claim is valid unless the declared invariant and key were actually tested.

### Level 6 — Current implementation documentation

Examples:

- codebase blueprint;
- module README;
- API documentation;
- schema commentary;
- function documentation;
- dependency map.

These explain the implementation and may expose divergence from doctrine. Where implementation and higher authority conflict, the conflict must be recorded rather than silently normalised.

### Level 7 — Roadmaps, proposals and work cards

Examples:

- roadmap;
- feature request;
- work card;
- migration proposal;
- design option;
- research backlog.

These direct future work only after approval appropriate to their scope.

### Level 8 — Historical documentation

Examples:

- old reload instructions;
- superseded architecture;
- prior-version README;
- historical changelog;
- obsolete workflow instructions;
- abandoned prototype notes.

Historical documents are valuable lineage evidence. They must not govern current work unless deliberately reactivated.

### Level 9 — Commentary, opinion and unverified recollection

Includes informal notes, conversation fragments, speculative interpretation and unverified memory.

These may identify a question or lead but cannot become authority without evidence and an explicit decision.

## Specificity rule

Where two documents occupy the same authority level, the more specific document governs within its narrower scope.

Example:

A root data doctrine may govern all data products, while an app-specific data contract governs field names and keys for one application. The app contract cannot violate the root doctrine, but it may add precise requirements.

## Currency rule

Where two documents occupy the same level and scope, the current approved revision normally governs.

However, newer does not automatically mean stronger. A recent draft does not overrule an older approved requirement.

Seed should record:

- approval status;
- effective date;
- supersedes relation;
- scope;
- owner;
- revision identifier;
- reopening condition.

## Conflict protocol

When documents conflict:

1. Stop the dependent decision if the conflict is material.
2. Identify each document's authority level, scope, revision and approval state.
3. Distinguish a real contradiction from different scopes or operating states.
4. Check physical, legal, contractual and rights constraints.
5. Preserve the conflict in Seed.
6. Apply the higher and more specific valid authority where determinable.
7. Escalate only the unresolved decision, not the whole programme.
8. Record the resulting authority decision and conditions for reopening.

## Human and AI roles

The human owner defines intent, approves scope and makes final decisions where judgement, risk or authority requires it.

AI may:

- inspect;
- compare;
- identify conflict;
- draft controlled implementation;
- execute authorised repository changes;
- produce evidence receipts;
- recommend an authority decision.

AI must not silently promote its own draft to binding authority.

The builder must not be the sole independent verifier of its own result.

## Repository-local read-order law

Before modifying a repository, read in this sequence where such documents exist:

1. binding local Employer's Requirement or scope;
2. root or local `START_HERE` instructions;
3. repository README;
4. canonical doctrine and architecture;
5. data contract, schema and dependency declarations;
6. operator and audit procedures;
7. latest evidence reports;
8. recent relevant commits;
9. implementation files;
10. historical roadmaps and older versions for lineage.

This order may be altered by an explicit local read-order document.

## V10 authority order

For the V10 solar electrical topology engine, the provisional authority order is:

1. physical reality, dimensional consistency and validated engineering mathematics;
2. applicable law, manufacturer limitations, project requirements and selected standards cartridges;
3. Seed ethics, engineering logic, context logic and rights doctrine;
4. approved V10 scope and recovery plan;
5. canonical object, topology, result and evidence schemas once approved;
6. authoritative Python steady-state implementation once selected by comparison;
7. independent topology and calculation verification;
8. V8, V9 and V10 JavaScript as lineage, comparison and interface sources until separately promoted;
9. reports and databases as derived consumers;
10. browser visualisation last.

## Closing rule

Authority should be visible enough that a future human or AI can answer:

- Which instruction governs?
- Why does it govern?
- What is its scope?
- What evidence supports it?
- What would supersede it?

A hidden authority order is not an authority system. It is merely habit.

---

Status: Living document

Classification: Seed governance and context doctrine

Copyrighted external material reproduced: No

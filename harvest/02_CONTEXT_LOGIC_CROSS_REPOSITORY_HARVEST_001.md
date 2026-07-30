# Context Logic — Cross-Repository Harvest 001

## Status

First cross-repository context-logic harvest for Seed 🌱.

This document strengthens `02_CONTEXT_LOGIC.md` by extracting the contextual disciplines already embedded across the Ventus repository federation.

Its purpose is to teach future work not merely what a file says, but how to determine whether that statement is current, authoritative, applicable, permitted, reproducible and safe to act upon.

## 1. Repository context is contractual context

The strongest repository guides do not treat README files as informal introductions. They treat local doctrine, employer's requirements, data contracts, audit guides and architecture notes as binding operating context.

Seed should therefore distinguish among repository documents:

- binding requirement;
- canonical doctrine;
- local operating manual;
- architecture description;
- data contract;
- workflow instruction;
- historical context;
- experiment;
- audit report;
- generated evidence;
- superseded note.

A future AI must not treat all Markdown files as equal authority merely because they share the same file extension.

## 2. Read order is part of context

The GlobalGrid2050 GridBot guide specifies a reading order before production changes. This reveals an important principle:

> Context is sequential. Later action depends on reading the right documents in the right order.

Seed should record, for each serious repository:

```text
start file
→ binding requirements
→ architecture
→ data or engineering contracts
→ recent audit evidence
→ recent commits
→ target implementation
```

A file registry that lists documents but omits read order remains incomplete.

## 3. Recent evidence can outrank old doctrine on current state

Stable doctrine may remain authoritative for principles, while recent audit and apply reports may be more authoritative for operational state.

Context records should therefore separate:

- enduring doctrine;
- current implementation state;
- most recent verified run;
- latest generated output;
- latest human approval;
- unresolved drift.

A recent commit is not automatically stronger than an older doctrine, and an old doctrine is not automatically proof that the current system complies with it.

## 4. Scope is an executable boundary

The federation employer's requirement repeatedly states: build to the approved scope and do not exceed it.

For Seed and V10, scope must be recorded as more than prose. A work item should state:

- included capabilities;
- excluded capabilities;
- target repositories and paths;
- allowed mutations;
- required evidence;
- approval owner;
- exit criteria;
- deferred work;
- rollback boundary.

Scope drift is a context failure before it becomes a coding failure.

## 5. Permanent and temporary are different context classes

The federation repository distinguishes a permanent ledger from temporary consumers such as a homepage.

Seed should record lifecycle class for repositories and artefacts:

- permanent authority;
- long-lived product;
- replaceable implementation;
- temporary migration tool;
- generated snapshot;
- disposable raw input;
- historical archive;
- experimental branch.

Dependency direction should respect that classification. A permanent authority should not depend intellectually or operationally on a temporary presentation layer.

Applied to V10:

- Seed doctrine is permanent knowledge context;
- the canonical kernel is long-lived authority;
- browser implementations are replaceable clients;
- generated reports are snapshots;
- raw temporary imports may be disposable once receipts and permitted evidence are retained;
- V8 and V9 may become historical reference layers rather than production dependencies.

## 6. Source of truth is plural by domain, singular by claim

The repositories reveal several valid sources of truth:

- Seed for federation-wide doctrine and lineage;
- leaf repositories for local implementation and operating instructions;
- the federation ledger for repository metadata and dependency state;
- canonical data products for verified facts;
- the solar kernel for engineering calculations;
- evidence objects for report claims;
- human approval records for governance decisions.

There is no useful single universal source of truth for everything.

However, every individual claim should resolve to one declared authority chain.

Seed should therefore ask:

- Truth about what?
- At what grain?
- For which time?
- Under which scope?
- Produced and verified by which mechanism?

## 7. Declared, inferred and derived relationships must remain distinct

The federation scanner distinguishes explicit repository declarations, canonical file probes and inferred dependency edges.

V10 context should similarly distinguish:

- declared connection;
- geometrically inferred relationship;
- electrically validated connection;
- manufacturer-declared internal commoning;
- user assumption;
- algorithmically derived topology;
- field-verified as-built condition.

An inference may be useful, but it must never be relabelled as a declaration merely because it appears plausible.

## 8. Context needs a confidence and status vocabulary

The repository federation makes unknown visible. The Data Spine distinguishes live, provisional, candidate and confirmed.

Seed should establish a common but extensible status vocabulary:

### Observation state

- not scanned;
- not found;
- found;
- inaccessible;
- ambiguous.

### Evidence state

- raw;
- provisional;
- candidate;
- reviewed;
- confirmed;
- rejected;
- superseded.

### Implementation state

- absent;
- prototype;
- experimental;
- active;
- deprecated;
- archived.

### Authority state

- unknown;
- reference only;
- provisional authority;
- approved authority;
- contested;
- withdrawn.

### Validity state

- valid;
- warning;
- invalid;
- not applicable;
- not evaluated.

One generic `status` field is too weak for serious engineering context.

## 9. Unknown must remain visible rather than guessed

The federation colour law provides an important contextual ethic: lack of evidence is grey, not hidden and not guessed green.

For V10:

- an unknown cable route is not zero metres;
- an unknown connector resistance is not automatically negligible;
- unknown internal MPPT commoning is not inferred from terminal count;
- missing standard applicability is not an automatic pass;
- absent licence information is not permission to copy;
- missing confidential status is not permission to publish.

Default values may support exploration, but they must be visibly classified as defaults or assumptions.

## 10. Status depends on evidence and precedence rules

A summary state should be reproducibly derived from lower-level evidence.

Seed should preserve:

- the status rule;
- the evidence fields used;
- precedence order;
- scope of propagation;
- date and version of the rule;
- result explanation.

A red, amber, green, grey or blue status without the query or rule that produced it is editorial decoration, not evidence.

## 11. Clean-clone reproducibility is contextual proof

The federation discipline insists that an independent auditor verify outputs from a clean clone.

This adds an important context field to every claimed capability:

- environment used;
- dependency versions;
- command executed;
- input snapshot;
- output hash;
- clean or pre-existing workspace;
- verifier identity or process;
- date verified.

A result that works only in an undocumented local environment is not fully contextualised.

## 12. Builder, auditor and approver are different roles

The repository guides distinguish executor, independent auditor and human approver.

Seed should record role context:

- author;
- source owner;
- builder;
- reviewer;
- independent verifier;
- approver;
- operator;
- publisher.

One person or system may hold more than one role in a small project, but the roles should still be conceptually separate.

This prevents the false conclusion that successful generation equals independent verification or approval.

## 13. Audit and apply are different events

Context should distinguish intended change from executed change.

For each material operation, Seed should be capable of recording:

- proposed action;
- audit result;
- declared target list;
- approval reference;
- apply event;
- apply receipt;
- post-apply verification;
- rollback availability;
- live verification.

A plan, a dry run, a commit and a verified deployment are not the same state.

## 14. Data context includes grain, completeness and method

The Data Spine teaches that a data point is incomplete without source dataset, grain, completeness, status and method.

Engineering context should generalise this:

Every result should identify:

- physical grain;
- temporal grain;
- source method;
- completeness;
- status;
- units;
- operating conditions;
- aggregation method;
- applicable exclusions.

Examples:

- `total conductor length` must state whether both polarities, factory leads, coils and home runs are included;
- `site loss` must state operating point, temperature basis and weighting period;
- `maximum voltage` must state cold-temperature method, module count and tolerance policy;
- `route distance` must state geodesic, plan, three-dimensional or installed path basis.

## 15. Rights context travels with knowledge

Cross-repository harvesting creates a major contextual obligation.

Every recovered item should carry:

- repository visibility;
- repository owner;
- upstream project where applicable;
- licence;
- copyright status where known;
- confidential or public classification;
- permitted use;
- required attribution;
- abstraction-only flag;
- redistribution restriction;
- source link and commit.

Publicly readable is not the same as public-domain.

Private access is not publication permission.

A factual engineering principle may often be independently expressed, while protected wording, diagrams, tables or code structure may not be copied without a compatible basis.

## 16. Fork context must preserve upstream identity

The `pandapower` repository is a fork or upstream-derived technical codebase rather than automatically original Ventus work.

Seed must distinguish:

- Ventus-authored repository;
- Ventus fork;
- vendored dependency;
- mirrored repository;
- adapted external code;
- original independent implementation.

Harvesting from a fork requires review of upstream licence, attribution and whether the capability should be referenced rather than migrated.

## 17. Public examples and confidential experience require different abstraction paths

The reports repository requires synthetic and generalised public examples and excludes confidential project material.

Seed should record abstraction pathway:

### Public-source pathway

- cite source;
- confirm licence or permissible summary;
- retain source identity;
- distinguish fact from interpretation.

### Confidential-experience pathway

- identify general lesson;
- remove project identifiers and commercially unique detail;
- avoid reproducing protected drawings or report text;
- independently express the engineering rule;
- state that the abstraction is not a project record;
- preserve only authorised minimal provenance.

## 18. Presentation context cannot upgrade technical authority

A polished dashboard, PDF or website does not make an underlying claim verified.

The reports and federation guides both reinforce:

- rendering success is not data proof;
- a report is not the atomic truth object;
- a colour is not a status unless derived;
- a browser view is not an engineering calculation unless reproducible independently;
- a public page is not the permanent ledger.

Seed should therefore preserve separate states for:

- generated;
- rendered;
- schema-valid;
- mathematically verified;
- independently reproduced;
- reviewed;
- approved;
- published.

## 19. Local self-sufficiency and federation memory must coexist

The federation requirement says the permanent ledger must carry its own doctrine and not depend on a temporary homepage for its operating brain.

Seed should not centralise context so aggressively that leaf repositories become unusable without it.

The preferred relationship is:

```text
Seed
  preserves cross-repository lineage, shared doctrine and authority map

Leaf repository
  preserves local purpose, contracts, test instructions, dependencies and operating manual
```

Seed references the leaf. The leaf references the relevant Seed doctrine. Neither should silently duplicate the other's entire content.

## 20. Context freshness requires explicit review

The repository guides warn about stale workflows and duplicate paths.

Seed should record:

- last observed commit;
- last guide review;
- current default branch;
- stale or duplicate workflow warning;
- superseding path;
- broken or unverified public route;
- next review trigger.

Repository metadata alone is not enough. A recently modified copy of an old guide may still be obsolete in substance.

## 21. Context for external pages

A repository may have multiple external expressions:

- GitHub source;
- GitHub Pages route;
- GlobalGrid2050 portal route;
- live app;
- documentation page;
- generated report;
- external upstream project.

The repository map should distinguish:

- backend source URL;
- canonical public URL;
- preview URL;
- legacy URL;
- redirect;
- current verification state;
- publisher;
- deployment mechanism.

A link existing is not proof that the page is current or generated from the referenced repository.

## 22. The context receipt

Every significant Seed harvest should produce a compact receipt:

```yaml
harvest_id:
source_repository:
source_commit:
source_path:
document_class:
authority_claim:
observed_statement:
original_synthesis:
rights_status:
confidence:
validation_state:
affects_capabilities:
affects_build_order:
reviewed_at:
```

Markdown explains the lesson. Structured receipts make the knowledge searchable and auditable.

## 23. Context logic amendments recommended

The parent `02_CONTEXT_LOGIC.md` should eventually incorporate these rules directly:

1. Document class and read order are part of authority.
2. Scope is an executable boundary.
3. Permanent and temporary artefacts have different dependency rights.
4. Source of truth is domain-specific, while each claim needs one authority chain.
5. Declared, inferred and derived relationships remain distinct.
6. Status requires multiple dimensions, not one generic field.
7. Unknown is visible and legal.
8. Build, audit, approval, apply and live verification are separate events.
9. Clean-environment reproduction is part of proof context.
10. Roles are recorded separately.
11. Fork and upstream context must survive harvesting.
12. External-page linkage needs deployment and freshness context.
13. Every harvest leaves a structured receipt.

## 24. Closing principle

Context is not the prose surrounding engineering truth.

Context identifies which truth is being claimed, by whom, for what scope, at what grain, with which evidence, under which rights, after what verification, and for how long that claim may safely be relied upon.

---

Status: Living harvest document  
Harvest ID: `CTX-HARVEST-001`  
Classification: Original cross-repository context synthesis  
Copyrighted source material reproduced: No

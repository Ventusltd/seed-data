# Unread or Unresolved Guides

## Purpose

This file makes incomplete knowledge visible.

Seed must not pretend that a repository has been understood merely because its README was found, a search returned no result, or one implementation file was inspected. Unknown is a lawful state. This queue records what remains unread, unresolved, conflicting or insufficiently receipted.

## Status terms

- `unread` — path is known but content has not yet been fully examined.
- `not_found_by_initial_search` — no guide was found in the first pass; absence is not proven.
- `minimal_repository` — repository currently appears empty or nearly empty.
- `authority_unresolved` — documents exist but precedence is not yet established.
- `rights_unresolved` — licence, upstream or confidentiality treatment remains open.
- `staleness_unresolved` — guide may be historical or superseded.
- `conflict_unresolved` — two guides appear to disagree materially.
- `receipt_partial` — key principles were extracted but a full structured receipt remains due.

## Priority 0 — binding or read-first documents

These should be read before further cross-repository code harvesting.

### `Ventusltd/globalgrid2050`

- `AI_START_HERE.md` — `unread`; referenced by the confirmed GridBot read order.
- `data_science_protocol/AUDIT_PROCESS_AND_REPORTING_REQUIREMENTS.md` — `unread`; required reading for production audit discipline.
- `scripts/README_GRIDBOT_AUDIT_REQUIREMENTS.md` — `unread`; script-level audit contract.
- `.github/workflows/README_GRIDBOT_AUDIT_WORKFLOWS.md` — `unread`; workflow-level audit contract.
- `OPERATOR_MANUAL_V1.md` — `receipt_partial`; human operating behaviour should be connected to AI instructions.
- `ARCHITECTURE.md` — `receipt_partial`; needs comparison against current app-split and data-spine doctrine.

### `Ventusltd/data-federation-map-for-globalgrid2050-all-repos`

- `every-drop-is-the-ocean/AUDIT_AND_COMMIT_EMPLOYERS_REQUIREMENT.md` — `unread`; declared binding.
- `every-drop-is-the-ocean/README.md` — `unread`; required local context.
- `jean-luc/README.md` — `receipt_partial`; dashboard consumer contract.

### `Ventusltd/solar-electrical-topology-analysis-engine-text-based`

- current root README or AI start guide — `not_found_by_initial_search`; inspect repository tree and recent commits.
- any local `DEPENDENCIES`, `DATA_CONTRACT`, schema or authority files outside the already receipted V10 recovery folder — `not_found_by_initial_search`.
- current test execution receipts — `unread`; repository inventory identified tests but this Seed pass has not rerun them.

### `Ventusltd/reports`

- `docs/WORKFLOW_TRIGGER_GUIDE.md` — `unread`.
- contracts under `contracts/` — `unread`; likely important to evidence-object and Save As interfaces.
- schemas under `schemas/` — `unread`; required before V10 report DNA is finalised.

## Priority 1 — engineering repositories

### `Ventusltd/pv-arc-protection-circuit`

Status: `authority_unresolved`, `rights_unresolved`.

Read next:

- README;
- architecture or design notes;
- circuit diagrams and source provenance;
- licence;
- test or simulation instructions;
- any assumptions concerning arc interruption, detection or protection.

Seed question:

Which capabilities are original Ventus engineering, which are external circuit references, and which belong in the V10 transient/protection layer rather than the steady-state kernel?

### `Ventusltd/cable_selection`

Status: private, `authority_unresolved`, `rights_unresolved`.

Read next without public disclosure:

- README and local guides;
- cable object and product models;
- selection rules;
- standards references;
- derating and installation assumptions;
- test fixtures;
- confidential or commercial content boundaries.

Seed question:

Which finished-product, conductor, installation and selection capabilities can be abstracted into public V10 without disclosing private material?

### `Ventusltd/pandapower`

Status: `rights_unresolved`, likely external fork.

Read next:

- upstream identity;
- licence;
- local modifications;
- repository purpose;
- whether Ventus changes contain reusable network logic;
- boundaries between AC network analysis and the Solar DC engine.

Seed question:

Should Seed migrate any local capability, or merely record interoperability and use pandapower as an external engine?

### `Ventusltd/Solar-PV-Hybrid-and-off-grid`

Status: `minimal_repository` in the initial inventory.

Read next:

- repository head and commit history;
- branches;
- README or pending scaffold.

Seed question:

Is this a future capability placeholder or does useful logic exist outside the default branch?

### `Ventusltd/solar-repowering-whitepaper`

Status: `authority_unresolved`, `rights_unresolved`.

Read next:

- README;
- original white-paper content;
- sources and citations;
- engineering claims;
- project abstractions;
- copyright notices.

Seed question:

Which repowering principles should become context, lifecycle and decision logic rather than code?

## Priority 2 — data repositories

### `Ventusltd/data-gb-electricity`

Status: `authority_unresolved`, `rights_unresolved` at source-dataset level.

Read next:

- README;
- `DATA_SOURCES`;
- `DATA_CONTRACT`;
- schema;
- workflow guides;
- audit reports;
- dependency declarations;
- source terms.

Seed question:

Which grain, additivity, completeness, status and non-destructive merge rules are reusable beyond GB electricity?

### `Ventusltd/data-interconnectors`

Status: `authority_unresolved`, `rights_unresolved` at source-dataset level.

Read next:

- README;
- direction and sign convention;
- interconnector identity model;
- country and BMRS-code mapping;
- source terms;
- audit evidence.

Seed question:

How should identity and direction be preserved across data, engineering and reports?

### `Ventusltd/data_uk_dno_and_tso`

Status: `authority_unresolved`, `rights_unresolved`.

Read next:

- README;
- source registry;
- network-owner identifiers;
- voltage-level and asset schemas;
- provenance and freshness logic;
- licensing.

### `Ventusltd/data-centres-gb`

Status: `authority_unresolved`, `rights_unresolved`.

Read next:

- README;
- source list;
- location confidence;
- public versus commercial data boundaries;
- relationship to Atlas and private-wire screening.

## Priority 3 — control-plane and presentation repositories

### `Ventusltd/spiders`

Status: `authority_unresolved`.

Read next:

- README;
- data inputs;
- dependency model;
- whether it consumes federation ledger outputs or retains historical hand-authored state;
- visualisation-only boundaries.

### `Ventusltd/registry_of_all_content_in_repos_and_dependencies`

Status: `minimal_repository`; observed README contains only a title.

Read next:

- commit history;
- branches;
- intended relationship to federation ledger and Seed;
- whether it is superseded, dormant or awaiting generation.

### `Ventusltd/globalgrid2050-hompage`

Status: `staleness_unresolved` and temporary-presentation classification.

Read next only as needed:

- README;
- current publication path;
- redirects;
- relationship to `globalgrid2050` root homepage and Spider.

Seed constraint:

Do not let temporary homepage logic define permanent federation or engineering truth.

### `Ventusltd/gb-electricity-ui`

Status: `authority_unresolved`.

Read next:

- README;
- data contract consumed;
- browser-state boundaries;
- chart and aggregation assumptions;
- fallback and staleness behaviour.

## Priority 4 — governance, education and organisational repositories

### `Ventusltd/Mahabharata`

Status: `rights_unresolved` at source-publication level; user-created distillation is a separate original layer.

Read next:

- README;
- provenance of the distilled aphorisms;
- copyright boundary statement;
- whether the repository distinguishes original distillation from source text.

Seed constraint:

Harvest ethical governance in original engineering language. Do not reproduce protected source editions.

### `Ventusltd/youengineer-code-review`

Status: `authority_unresolved`, `rights_unresolved`.

Read next:

- README;
- review method;
- code-quality and educational principles;
- external examples and licences.

Seed question:

Which review logic should become general verification doctrine?

### `Ventusltd/crm`

Status: private, `rights_unresolved`, high confidentiality risk.

Default Seed treatment:

Do not harvest personal, customer or commercial data into public Seed.

Read only governance or schema logic where necessary and authorised, using abstraction.

## Cross-cutting unresolved questions

### Which guide is current?

Several repositories contain repeated roadmaps, copied documentation and versioned reload files. Seed must distinguish:

- current canonical file;
- historical copy;
- generated copy;
- migration artefact;
- stale duplicate.

### Which repository is permanent?

The federation doctrine explicitly separates permanent metadata ledgers from temporary homepages. Similar permanence classifications are needed for:

- Seed;
- canonical engines;
- data products;
- app UIs;
- generated reports;
- historical sandboxes.

### Which implementation is authoritative?

The solar engine currently has Python, V8/V9 JavaScript and V10 JavaScript families. Authority remains provisional until baseline execution and comparative verification are complete.

### Which facts are additive?

The Data Spine's additivity law must be generalised carefully. Seed needs an engineering aggregation register identifying which quantities may be summed, averaged, maximised, composed or not aggregated.

### Which verifier is independent?

Tests within the builder are necessary but not always independent proof. V10 needs a separate verifier for topology invariants, schema laws and key engineering results.

### Which rights permit migration?

Public visibility is not enough. Forks, datasets, standards references, private repositories and confidential abstractions require explicit classification.

## Completion rule for this queue

An item leaves this file only when:

1. the guide has been read;
2. its source path and revision are recorded;
3. its authority and scope are classified;
4. its rights treatment is known sufficiently for the intended use;
5. its Seed and V10 effects are recorded;
6. conflicts and staleness are resolved or moved into a named decision record.

## Next executable batch

Read and receipt the Priority 0 documents first, then perform a repository-by-repository canonical-file probe over the engineering and data repositories.

The next generated artefacts should be:

- structured repository guide rows;
- repository permanence classes;
- engineering grain and aggregation register;
- baseline execution receipt plan;
- first authority decisions for V10 object, topology and result schemas.

---

Status: Living unresolved queue

Principle: Unknown remains visible; nothing is guessed complete

Copyrighted external material reproduced: No

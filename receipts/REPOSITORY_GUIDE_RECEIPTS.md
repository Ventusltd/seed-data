# Repository Guide Receipts

## Status

Seed Pass 2, initial live-repository guide harvest.

This file records guidance documents discovered across the Ventus and GlobalGrid2050 repositories. It is a receipt, not a claim that every repository has already been exhaustively read. Missing or unresolved guides are recorded separately rather than guessed.

## Governing rule

Read doctrine before implementation.

A repository may contain code, data, reports and interfaces whose purpose cannot be understood safely from filenames alone. Seed therefore records the local guides, their declared authority and the order in which they should be read before harvesting capability.

## Receipt fields

Each guide receipt should preserve:

- repository;
- repository role;
- guide path;
- document type;
- declared status;
- binding strength;
- scope;
- read-order position;
- head or source revision where observed;
- Seed impact;
- V10 impact;
- unresolved conflict or limitation.

## Confirmed high-authority guide family: GlobalGrid2050 root

Repository: `Ventusltd/globalgrid2050`

Observed source revision during this pass: `c0965dfdebf7a7fab5a919a4692e676e149073be`

### `README.md`

Type: repository entry point.

Authority: high for current repository purpose and navigation, subject to more specific binding requirements.

Seed impact: establishes the operating-system character of the repository and points to local doctrine.

### `AI_GRIDBOT_START_HERE.md`

Type: AI operating manual and required read order.

Authority: binding for GridBot-governed production changes.

Confirmed rules include:

- inspect existing workflow and audit patterns before editing;
- commit controlled scripts or workflows directly where authorised;
- run audit before apply;
- inspect committed audit evidence before approval;
- verify live output and rollback path after apply;
- never perform broad undeclared mutation;
- commit compact reviewed facts rather than raw bulk;
- separate provisional and settled data;
- preserve named interconnector identity and direction;
- prefer one repository per serious application.

Seed impact: provides the strongest current example of a controlled human-AI execution protocol.

V10 impact: V10 must distinguish proposal, audit, approval, application, verification and rollback as separate states.

### `PHILOSOPHY.md`

Type: architectural philosophy.

Authority: strategic and architectural; not mathematical authority.

Confirmed rules include:

- human domain expertise and intent precede generated syntax;
- physical reality, electrical physics and commercial consequence must remain connected;
- application state follows Input → State → Compute → Render → Export;
- geometry and geodesic reality must be respected;
- preserve working truth through controlled incremental change;
- use readable and deterministic structures that humans and AI can inspect;
- expose constraints early;
- AI is a structured reasoning layer, not an uncontrolled code generator.

Seed impact: establishes intent compilation, physical truth, strict boundaries and incremental preservation as cross-repository doctrine.

V10 impact: the kernel contract must be explicit, deterministic and independent of presentation; physical and evidence state must not be scattered through UI code.

### `ARCHITECTURE.md`

Type: root architecture guide.

Authority: high architectural context, to be reconciled with current app-specific guides and data-spine doctrine.

Seed action: full detailed receipt remains due.

### `AI_START_HERE.md`

Type: AI read-first guide.

Authority: potentially binding.

Status in this pass: referenced by the GridBot read order but not yet fully receipted.

Seed action: unresolved guide queue.

### `OPERATOR_MANUAL_V1.md`

Type: human operator manual.

Authority: operational.

Seed impact: likely source for human-side trigger, verification and rollback behaviour.

Seed action: full receipt remains due.

## Confirmed high-authority guide family: Data Science Protocol

Repository: `Ventusltd/globalgrid2050`

### `data_science_protocol/THE_DATA_SPINE.md`

Type: canonical data doctrine.

Declared status: canonical doctrine.

Authority: binding for systems that ingest, distil, store or serve grid data.

Confirmed rules include:

- store the right grain for the question;
- Python fetches, validates, distils and writes compact intelligence plus audit method;
- temporary raw data is deleted unless retention is explicitly approved;
- GitHub stores method, facts and trail;
- the browser loads the grain required for the question;
- additive quantities and non-additive extrema must be treated differently;
- every fact carries source, schema, completeness and status;
- weak, empty or partial incoming data must not overwrite stronger reviewed data;
- promotion proceeds from provisional acquisition to candidate, validation, review and confirmed fact;
- commit facts, not bulk.

Seed impact: establishes grain, additivity, promotion, completeness and non-destructive merge as general laws.

V10 impact: object, segment, circuit, string, MPPT, inverter, site and fleet grains must be declared before schema and aggregation code are finalised.

### `data_science_protocol/DATA_SCIENCE_LOGIC_VENTUS.md`

Type: data-science reasoning doctrine.

Authority: likely high within data systems.

Status: discovered, full receipt due.

### `data_science_protocol/DATA_STORAGE_DISCIPLINE_PROTOCOL.md`

Type: storage protocol.

Authority: likely binding for persistence decisions.

Status: discovered, full receipt due.

### `data_science_protocol/APP_REPO_SPLIT_AND_DATA_PIPELINE_ARCHITECTURE.md`

Type: repository-boundary and data-pipeline guide.

Authority: architectural.

Status: discovered, full receipt due.

### `data_science_protocol/AUDIT_PROCESS_AND_REPORTING_REQUIREMENTS.md`

Type: audit and reporting requirement.

Authority: referenced as required reading by `AI_GRIDBOT_START_HERE.md`.

Status: high-priority unread guide.

### Audit and inspection reports

Observed families include:

- `data_science_protocol/audit_reports/*_LATEST.md`;
- `data_science_protocol/inspection_reports/*_LATEST.md`;
- JSON equivalents.

Authority: evidence receipts, not doctrine by themselves.

Seed impact: current state must be established from committed evidence, not only from guide prose.

## Confirmed guide family: Solar and BESS historical versions

Repository: `Ventusltd/globalgrid2050`

### `solar-bess-topology-v6/README.md`
### `solar-bess-topology-v7/README.md`
### `solar-bess-topology-v6/docs/ARCHITECTURE.md`
### `solar-bess-topology-v7/docs/ARCHITECTURE.md`
### `solar-bess-topology-v5/V5_CHANGELOG_AND_ROADMAP.md`
### copied or migrated roadmap documents under later versions
### `solar-bess-topology-v8/CODEBASE_BLUEPRINT.md`

Type: version-specific architecture, roadmap, migration and codebase guides.

Authority: historical and version-local. They are important lineage evidence but must not automatically override the dedicated solar topology repository's current recovery plan.

Seed impact: preserve version lineage, explicit migration decisions and rejected assumptions.

V10 impact: use as historical evidence for capability evolution and regression recovery, not as automatic authority.

## Confirmed guide family: UK Energy Tracker

Repository: `Ventusltd/globalgrid2050`

### `uk_energy_tracking_v2/AI_RELOAD_INSTRUCTIONS.md`
### `uk_energy_tracking_v3/AI_RELOAD_INSTRUCTIONS.md`
### `uk_energy_tracking_v4/AI_RELOAD_INSTRUCTIONS.md`
### `uk_energy_tracking_v5/AI_RELOAD_INSTRUCTIONS.md`
### `uk_energy_tracking_v6/V6_ARCHITECTURAL_INTEGRITY_PROTOCOL.md`
### V5-to-V6 comparison and repair reports

Type: reload instructions, architectural integrity requirements and regression evidence.

Authority: version-local, with the latest integrity protocol stronger than earlier reload files for current V6 maintenance.

Seed impact: proves that reload documentation is operational infrastructure rather than narrative decoration.

V10 impact: every major build phase should produce a compact reload file, capability receipt and comparison report.

## Confirmed high-authority guide family: Solar electrical topology engine

Repository: `Ventusltd/solar-electrical-topology-analysis-engine-text-based`

### `v10-development/recovery/V10_ENGINE_RECOVERY_PLAN.md`

Type: authoritative recovery plan.

Authority: binding current build-order candidate for the solar topology programme, subject to Seed cross-repository assessment.

Confirmed order:

Physical objects → geometry → terminals and connectivity → ordered electrical topology → computation → evidence → reporting → browser visualisation.

Confirmed controls include:

- browser is not authority;
- complete circuit representation cannot rely on one assumed total length;
- topology failure stops dependent calculation;
- Python is the leading steady-state authority candidate;
- distributed and transient models remain separate from steady-state logic;
- standards cartridges do not own the physics kernel;
- no copied standards text, figures or tables;
- no number without units and provenance;
- browser rebuild last.

### `v10-development/recovery/V6_TO_V10_CAPABILITY_MIGRATION_LEDGER.md`

Type: capability lineage and migration guide.

Authority: evidence-bearing planning artefact.

### `v10-development/recovery/PASS_1_ENGINE_INVENTORY.md`

Type: repository inventory receipt.

Authority: current evidence of discovered engine families.

### `v10-development/recovery/WORK_CARD_001_ENGINE_INVENTORY_AND_AUTHORITY.md`

Type: scoped work instruction.

Authority: work-card level.

### `v10-development/research/ENGINEERING_EVIDENCE_REGISTER.md`

Type: evidence map.

Authority: supporting evidence register.

### `v10-development/research/IEC_TS_62738_CAPABILITY_MATRIX.md`

Type: standards-capability cross-reference.

Authority: interpretation and mapping, not a reproduction of the standard and not independent legal authority.

Seed impact: this repository provides the most mature current physical-object, topology, calculation and evidence-chain doctrine for V10.

## Confirmed high-authority guide family: Federation map

Repository: `Ventusltd/data-federation-map-for-globalgrid2050-all-repos`

### `README.md`

Type: repository entry and local binding pointer.

Authority: high.

It declares the repository to be the source-of-truth metadata product for federation nodes and dependency edges, not a homepage or UI repository.

### `every-drop-is-the-ocean/FEDERATION_LEDGER_SCOPE_EMPLOYERS_REQUIREMENT.md`

Type: approved Employer's Requirement.

Declared status: binding scope; build to it and do not exceed it.

Confirmed rules include:

- permanent ledger points to leaf repositories and does not copy their source trees;
- temporary consumers may depend on the permanent ledger, never the reverse;
- metadata before cloning and canonical probes before inference;
- keys and exact-equality invariants must be declared;
- unknown is a lawful visible state;
- status is query-derived, never hand-authored;
- prove before consolidate;
- independent verification before later layers;
- current-state views derive from append-only evidence;
- no assistant marks its own homework;
- green CI, rendering and file count are not proof.

Seed impact: strongest current guide for permanence boundaries, declared keys, proof, independent verification and non-absorption.

V10 impact: V10 requires an independent topology and result verifier, not only tests executed by the builder.

### `every-drop-is-the-ocean/AUDIT_AND_COMMIT_EMPLOYERS_REQUIREMENT.md`

Type: binding audit and commit requirement.

Status: referenced as required reading; full receipt due.

### `every-drop-is-the-ocean/README.md`

Type: local philosophical and scope context.

Status: required reading; full receipt due.

### `jean-luc/README.md`

Type: dashboard specification.

Authority: UI-consumer scope, downstream of verified Parquet-derived data.

## Confirmed guide family: Reports

Repository: `Ventusltd/reports`

### `README.md`

Type: report instrumentation doctrine and repository map.

Authority: high for the reports layer.

Confirmed rules include:

- the atomic unit is an evidence object, not a PDF;
- reports are projections over evidence;
- CSV, plain text and HTML remain available;
- PDF is an optional rendered form;
- outputs carry manifest, source badge, confidence state and disclaimer;
- examples remain synthetic and generalised;
- future report packs share one evidence model.

Seed impact: report DNA and evidence objects must be defined before document templates.

V10 impact: the first report milestone should be a machine-readable evidence pack plus reproducible text/HTML projection, not a polished PDF-first deliverable.

### `docs/WORKFLOW_TRIGGER_GUIDE.md`

Type: workflow order guide.

Authority: operational.

Status: discovered, full receipt due.

## Minimal or unresolved repository guides

The following repositories are known federation nodes but require a deeper local guide pass before Seed treats their implementation as harvested knowledge:

- `Ventusltd/pv-arc-protection-circuit`;
- `Ventusltd/solar-repowering-whitepaper`;
- `Ventusltd/Solar-PV-Hybrid-and-off-grid`;
- `Ventusltd/cable_selection`;
- `Ventusltd/pandapower`;
- `Ventusltd/crm`;
- `Ventusltd/youengineer-code-review`;
- `Ventusltd/globalgrid2050-hompage`;
- `Ventusltd/data-gb-electricity`;
- `Ventusltd/data-interconnectors`;
- `Ventusltd/gb-electricity-ui`;
- `Ventusltd/spiders`;
- `Ventusltd/data_uk_dno_and_tso`;
- `Ventusltd/registry_of_all_content_in_repos_and_dependencies`;
- `Ventusltd/Mahabharata`;
- `Ventusltd/data-centres-gb`.

The absence of a receipt is not evidence that no guide exists. It means Seed has not yet read and classified it.

## Immediate next receipt order

1. Binding Employer's Requirements and audit requirements.
2. AI or human `START_HERE` and reload documents.
3. Root README and architecture files.
4. Data contracts, schema and dependency documents.
5. Operator manuals and workflow trigger guides.
6. Changelogs, roadmaps and migration reports.
7. Code only after the relevant guides have been receipted.

## Closing receipt

The guide harvest confirms that the Ventus repositories were prepared for this Seed moment. The doctrine is already distributed across operating manuals, Employer's Requirements, data laws, reload files, architecture notes, audit reports and version migration records.

Seed's duty is not to replace them. It is to preserve their authority order, connect their logic, identify conflicts and turn their strongest recurring principles into a durable engineering and proof architecture.

---

Status: Living receipt

Pass: Seed Pass 2, initial guide harvest

Copyright treatment: original synthesis and path-level references only; no protected external work reproduced

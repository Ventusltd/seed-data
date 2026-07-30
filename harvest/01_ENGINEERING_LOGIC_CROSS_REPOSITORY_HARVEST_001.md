# Engineering Logic — Cross-Repository Harvest 001

## Status

First cross-repository engineering-logic harvest for Seed 🌱.

This document does not replace `01_ENGINEERING_LOGIC.md`. It strengthens it with evidence recovered from the live Ventus repository federation and identifies rules that should change the V10 build order.

The harvest is original synthesis. It records repository paths and engineering lessons without copying protected standards, proprietary reports or third-party expression.

## Repositories and guide families inspected

This pass inspected the currently connected Ventus repository set and concentrated on repositories already carrying explicit architectural or engineering doctrine:

- `Ventusltd/globalgrid2050`
- `Ventusltd/solar-electrical-topology-analysis-engine-text-based`
- `Ventusltd/reports`
- `Ventusltd/data-federation-map-for-globalgrid2050-all-repos`
- `Ventusltd/registry_of_all_content_in_repos_and_dependencies`
- `Ventusltd/spiders`
- `Ventusltd/data-gb-electricity`
- `Ventusltd/data-interconnectors`
- `Ventusltd/data_uk_dno_and_tso`
- `Ventusltd/data-centres-gb`
- `Ventusltd/pv-arc-protection-circuit`
- `Ventusltd/Solar-PV-Hybrid-and-off-grid`
- `Ventusltd/cable_selection`
- `Ventusltd/pandapower`
- `Ventusltd/globalgrid2050-hompage`
- `Ventusltd/gb-electricity-ui`
- `Ventusltd/reports`
- `Ventusltd/Mahabharata`
- `Ventusltd/youengineer-code-review`
- `Ventusltd/crm`
- `Ventusltd/solar-repowering-whitepaper`

Not every repository yet exposes a mature guide or indexed code surface. Absence of recovered doctrine in this pass means `not yet observed`, not `none exists`.

## 1. The strongest recovered engineering pattern

Across the repositories, the strongest recurring pattern is:

```text
Intent
→ declared scope
→ canonical objects and grain
→ deterministic builder
→ independent verifier
→ evidence receipt
→ human approval
→ derived presentation
```

This pattern appears in different forms in the GridBot operating discipline, the Data Spine, the federation ledger, the solar topology recovery plan and the reports repository.

It should become a first-class V10 architecture law.

## 2. Physical truth and data truth are parallel disciplines

The solar engine says:

```text
Physical objects
→ geometry
→ terminals and connectivity
→ ordered topology
→ computation
→ evidence
→ reporting
→ visualisation
```

The Data Spine says:

```text
Python fetches
→ validates
→ distils
→ writes compact facts and audit method
→ discards transient raw bulk
→ browser loads the grain appropriate to the question
```

These are not separate philosophies. They are the same architecture applied to two domains.

The unifying rule is:

> Preserve the smallest sufficient authoritative object, derive higher-level views reproducibly, and never allow presentation to become the source of truth.

For V10 this means:

- conductor segments, terminals, products, evidence objects and topology edges are canonical;
- string, MPPT, inverter, site and fleet totals are derived;
- report tables and browser cards are projections;
- no aggregated result may destroy the lower-level lineage from which it was produced.

## 3. Grain must be selected by the question

The Data Spine establishes that the error is not merely storing too much data; it is storing the wrong grain for the question.

The engineering equivalent is:

- a total cable length is the wrong grain for geometric and electromagnetic questions;
- a string total may be the right grain for a summary but the wrong grain for segment loss or protection analysis;
- an inverter total is not sufficient for MPPT topology;
- a site aggregate cannot validate conductor continuity;
- a screenshot is not sufficient evidence for a numerical result.

V10 therefore needs an explicit engineering grain ladder:

```text
measurement or declaration
component
terminal
connection
segment
route
circuit
string
MPPT
inverter
block
site
fleet
network interface
```

Every calculation and report field should declare its input grain and output grain.

## 4. Additivity must be declared, not assumed

The Data Spine makes a powerful distinction: energy sums, but peaks and extrema do not.

V10 should generalise this into an aggregation law register.

Examples:

- conductor length is additive only when the included segments and counting basis are explicit;
- resistance in series is additive, but parallel resistance is not a direct sum;
- segment losses are additive for a defined operating state, but percentage losses may not be averaged without weighting;
- copper mass is additive where segment material and quantity are defined;
- maximum voltage is an extremum, not an additive quantity;
- current may split, combine or remain equal depending on topology;
- uncertainty may require correlation treatment and must not be naively summed;
- status uses a declared precedence rule rather than arithmetic aggregation.

Each result type should carry an aggregation policy such as:

- `sum`
- `weighted_mean`
- `maximum`
- `minimum`
- `logical_all`
- `logical_any`
- `worst_state_wins`
- `topology_defined`
- `non_aggregable`

## 5. Current state is derived; events and evidence endure

The federation ledger establishes a key principle:

> Append-only events are the source of truth; current-state tables are derived views.

Applied to V10:

- changes to objects, assumptions, topology, product selection, exceptions and approvals should produce immutable evidence events;
- the current design model may be rebuilt from those events or at minimum accompanied by a durable change trail;
- authority decisions should never be silently overwritten;
- superseded calculations should remain traceable;
- report revisions should identify which evidence snapshot they represent.

This does not require a complex event-sourcing framework immediately. It does require the schema to avoid making future lineage impossible.

## 6. Prove on the declared key

The federation guide rejects file counts, green CI and successful rendering as proof. Proof is an explicit invariant tested on an explicit key.

V10 should adopt the same discipline.

Examples of declared engineering keys:

- object key: project + object identifier;
- terminal key: object identifier + terminal identifier;
- connection key: source terminal + destination terminal + connection type;
- segment key: topology version + segment identifier;
- result key: input snapshot hash + kernel version + calculation identifier;
- evidence key: source identity + revision + evidence item identifier;
- report key: result-set hash + report profile + report revision.

Examples of invariants:

- zero duplicate object keys;
- zero null terminal identifiers;
- every connection endpoint resolves to a terminal;
- every topology segment resolves to a physical conductor object;
- every calculated result resolves to its input objects and method;
- every report number resolves to a result key;
- every standards check identifies its edition and interpretation record;
- no dependent calculation survives a failed topology validation.

## 7. Unknown is a legal engineering state

The federation ledger treats grey or unknown as legitimate rather than forcing a false green status.

V10 should explicitly support:

- unknown;
- not observed;
- not provided;
- not applicable;
- unresolved;
- provisional;
- candidate;
- verified;
- rejected;
- superseded.

Missing evidence must not be silently replaced by a default and then displayed as certainty.

## 8. Worst-state-wins must be scoped

The federation status law uses a declared precedence where the worst material state governs the summary.

V10 should use the same principle for safety and validity summaries, but only where the rule is explicitly applicable.

Examples:

- one unresolved dangling terminal may make the topology invalid;
- one failed mandatory evidence requirement may make a compliance claim unavailable;
- one segment exceeding a hard product limit may make the selected route infeasible;
- one provisional input need not make every unrelated result provisional if result-level lineage isolates its influence.

Therefore summary status must be derived from dependency-aware rules, not a universal red flag sprayed across the project.

## 9. Browser and dashboards may render truth but must not invent it

The recovered guides repeatedly reject hand-authored status, hidden browser maths and UI inference.

V10 browser law should be:

```text
Input editor
→ canonical object mutation request
→ validation
→ kernel computation
→ evidence-aware result contract
→ browser rendering
```

The browser may:

- create and edit candidate objects;
- visualise routes and validated topology;
- request calculations;
- display warnings and provenance;
- export reports.

The browser may not:

- become the only implementation of an engineering formula;
- infer internal electrical commoning from visual placement;
- convert drawing order into electrical order without validation;
- hand-colour compliance status;
- write results that cannot be reproduced outside the browser.

## 10. Reports begin with evidence objects, not documents

The reports repository establishes that the atomic unit is not a PDF. It is an evidence object carrying provenance.

This materially changes V10 reporting architecture.

The build order should not jump from kernel to PDF generation. It should first define:

1. evidence-object schema;
2. calculation-result schema;
3. report DNA or projection manifest;
4. plain text and CSV baseline outputs;
5. HTML review output;
6. optional PDF and DOCX renderers.

Every output should carry:

- manifest;
- source badge or provenance statement;
- confidence or status;
- scope and disclaimer;
- result-set identity.

## 11. Static-first does not mean browser-authoritative

The wider ecosystem favours static, GitHub Pages-friendly delivery and browser-side save workflows.

This is compatible with an authoritative kernel provided the contract is clear:

- computation can run in a tested portable kernel, service, CLI or compiled browser-safe package;
- result generation is independent of page rendering;
- browser saving is an output transport, not an authority layer;
- large working data should use appropriate storage rather than localStorage;
- committed repositories should contain compact reviewed evidence, not uncontrolled raw bulk.

## 12. Audit before apply

The GridBot guidance establishes a controlled workflow:

```text
inspect
→ declare target
→ audit
→ inspect evidence
→ approve
→ apply
→ inspect apply receipt
→ verify live state
→ retain rollback path
```

V10 should use an equivalent discipline for:

- schema migrations;
- authority promotions;
- batch data imports;
- topology conversions;
- standards cartridge updates;
- cross-language replacement of calculations;
- report-template changes affecting claims.

A dry-run or audit mode should show intended object changes, affected results and failed invariants before mutation.

## 13. Surgical change is safer than uncontrolled rewrite

The guides strongly favour small, reviewable, traceable and reversible changes over mass refactoring.

For V10 this means:

- preserve working reference implementations until replacements pass equivalence tests;
- migrate capability by capability;
- retain baseline fixtures;
- avoid deleting V8 or V9 logic simply because Python becomes authoritative;
- separate code commits from generated evidence where practical;
- define rollback points;
- do not consolidate before the existing path is understood and proven.

## 14. One serious app per repository, one permanent doctrine locally

The ecosystem guide favours one repository per serious application while keeping doctrine, contracts and operating instructions local enough that the repository is self-sufficient.

Seed should therefore become the federation-wide memory and cross-reference layer, but must not make every leaf repository intellectually dependent on a remote document.

Each serious V10 repository should carry a concise local contract:

- purpose;
- authority boundary;
- canonical inputs and outputs;
- test command;
- audit and apply process;
- dependencies;
- Seed references;
- copyright and confidentiality boundary.

Seed points outward and records lineage. It should not absorb entire source trees.

## 15. Heavy machinery is threshold-triggered

The federation guide explicitly defers GitHub Apps, webhooks, CRDTs and peer-to-peer infrastructure until concrete thresholds are crossed.

V10 should adopt the same anti-premature-complexity law:

- do not introduce distributed orchestration merely because it is architecturally fashionable;
- do not add a backend where deterministic local or static execution suffices;
- do not add optimisation before feasibility;
- do not add transient models before the steady-state kernel and topology are stable;
- do not add AI autonomy before audit contracts and permissions are explicit;
- record the trigger conditions for deferred architecture.

## 16. Engineering capability promotion states

The cross-repository evidence supports a stronger promotion sequence:

```text
observed
→ inventoried
→ rights-checked
→ contextualised
→ reconstructed
→ unit-checked
→ invariant-tested
→ independently verified
→ candidate authority
→ human-approved authority
→ monitored
→ superseded or retained
```

The earlier `adopt`, `adapt`, `reference`, `reject`, `archive` decisions remain useful migration decisions, but they are not sufficient as validation states.

## 17. Independence of builder and verifier

A repeated lesson is that the builder should not be the sole verifier of its own output.

V10 should eventually provide:

- independent topology validation separate from topology generation;
- independent result-schema verification separate from calculation production;
- cross-language known-answer comparisons where useful;
- clean-environment reproduction;
- human approval for authority promotion;
- field or hand-calculation evidence where the claim warrants it.

This does not mean every unit test must be written by another person. It means the proof path must not merely repeat the implementation's assumptions.

## 18. Revised canonical engineering chain

The repository harvest strengthens the earlier chain into:

```text
Human intent and engineering question
→ declared scope and authority boundary
→ evidence acquisition and rights classification
→ canonical grain and object identity
→ physical objects and conditions
→ geometry and route
→ terminals and connectivity
→ ordered topology
→ topology-independent verification
→ product and conductor properties
→ calculation policy and aggregation laws
→ authoritative computation
→ uncertainty and validity
→ evidence receipts and immutable events
→ independent result verification
→ derived current-state tables
→ report DNA and projections
→ browser and federation consumers
→ human review and authority decision
```

## 19. Immediate amendments recommended for `01_ENGINEERING_LOGIC.md`

The parent doctrine should later incorporate these additions directly:

1. Grain is selected by the question.
2. Every result declares an aggregation law.
3. Unknown is a legal state.
4. Current state is derived from durable evidence and change history.
5. Proof is an invariant over a declared key.
6. Builder and verifier are logically separate.
7. Reports begin with evidence objects and projection manifests.
8. Audit precedes mutation.
9. Complexity is threshold-triggered.
10. Leaf repositories remain locally intelligible while Seed preserves federation-wide lineage.

## 20. Copyright and confidentiality boundary

This harvest records original synthesis of repository doctrines and publicly visible engineering architecture.

It does not reproduce:

- standards clauses or tables;
- copyrighted book text;
- proprietary customer drawings;
- confidential project reports;
- third-party code bodies;
- private repository content not authorised for public abstraction.

Links and source paths are retained for provenance. Future capability migration must inspect the applicable licence and confidentiality context before copying code or detailed expression.

---

Status: Living harvest document  
Harvest ID: `ENG-HARVEST-001`  
Classification: Original cross-repository engineering synthesis  
Copyrighted source material reproduced: No

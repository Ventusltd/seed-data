# Engineering Logic

## Purpose

This document defines the engineering reasoning order that Seed 🌱 should preserve and that V10 should implement.

It is not a catalogue of equations. It is the logic that determines where equations belong, what objects they act on, how evidence enters them and how outputs become trustworthy.

## 1. Physics before software

Software does not create physical truth.

The physical system exists independently of the user interface, programming language, database or report format.

Every computational capability should therefore begin with a physical question:

- What objects exist?
- What are their dimensions and materials?
- Where are they located?
- How are they connected?
- Which quantities are measured, declared, derived or assumed?
- Under what conditions is the model valid?

The implementation follows the answer. The answer must not be distorted to fit an existing interface.

## 2. Geometry before totals

A total cable length entered by a user is not a geometric model.

Where physical arrangement affects resistance, inductance, capacitance, electromagnetic coupling, installation feasibility, material quantity, routing or maintenance, length should be derived from ordered physical objects and routes.

Totals may be accepted as declared evidence, but they must not silently replace geometry.

## 3. Objects before equations

Equations should operate on explicit engineering objects.

Examples include:

- module;
- junction box;
- flying lead;
- connector;
- field-installed conductor;
- harness;
- segment;
- route;
- coil;
- mounting structure;
- string;
- MPPT input;
- inverter;
- protective device;
- test record.

An object should have identity, properties, provenance and relationships. A number without an object and context is weak evidence.

## 4. Terminals before connectivity

Electrical topology should be constructed through terminals and connections rather than inferred from drawing proximity or array position.

Each conductive object should expose defined terminals. Connections join compatible terminals. The resulting graph determines the circuit order.

This enables:

- continuity validation;
- polarity checking;
- branch detection;
- open-circuit detection;
- short-circuit detection;
- ordered segment traversal;
- MPPT allocation;
- topology comparison;
- reproducible export.

## 5. Topology before calculation

Resistance, voltage drop, stored energy and other results are meaningful only after the circuit being calculated is unambiguous.

The engine should first establish:

- the connected components;
- their order;
- the current path;
- the return path;
- branching and combining points;
- source and termination;
- topology feasibility.

Calculation over an invalid topology should fail clearly rather than return a plausible number.

## 6. Formation is separate from connectivity

Two circuits may have identical electrical connectivity but different physical conductor formation.

The model should distinguish:

- electrical graph;
- physical route;
- conductor separation;
- pairing;
- bundling;
- crossing;
- coiling;
- mounting relationship;
- proximity to conductive structures.

This separation is essential for electromagnetic and installation analysis.

## 7. Units are part of the type

Units must not be left to memory or comments.

Every quantity should carry or be validated against its unit and physical dimension.

The engine should reject incompatible operations and avoid ambiguous bare numbers at public interfaces.

Conversions should occur at explicit boundaries.

Canonical internal units may be used, but original declared units and conversion provenance should remain recoverable.

## 8. Conditions belong with values

A resistance value without temperature, material condition and basis is incomplete.

A voltage without operating state is incomplete.

A current without irradiance, temperature, spectrum or source definition may be incomplete.

Quantities should carry applicable conditions, including where relevant:

- reference temperature;
- operating temperature;
- frequency;
- irradiance;
- installation state;
- tolerance;
- confidence;
- measurement method;
- declared standard or datasheet basis.

## 9. Evidence classes remain distinct

Seed and V10 should preserve at least these evidence classes:

- `manufacturer_declared`;
- `field_measured`;
- `public_observation`;
- `user_created`;
- `derived`;
- `generic_example`;
- `assumed`;
- `external_reference`.

Derived outputs should identify the inputs and method from which they were produced.

Assumed values must not be rendered as measured or manufacturer-declared values.

## 10. Products and conductors are not interchangeable

A conductor cross-sectional area is not a finished cable product.

A product object may include:

- conductor material and construction;
- nominal area;
- conductor diameter;
- insulation and sheath systems;
- cable outer diameter;
- resistance at reference conditions;
- voltage rating;
- temperature rating;
- environmental properties;
- certification or declaration metadata;
- source and revision.

Calculations should use the strongest appropriate property. Geometry-based derivation should not overwrite a declared finished-product value without an explicit reason.

## 11. Derived length must remain auditable

Every derived route length should be decomposable into named segments.

A result should be traceable from total length to:

- module leads;
- connector offsets;
- row transitions;
- home runs;
- drops and rises;
- coils;
- slack allowances;
- inverter termination routes;
- any user-defined detours.

The engine must not hide geometric assumptions inside a single scalar.

## 12. Sequential and leapfrog are topology cartridges

Sequential and leapfrog arrangements should be represented as explicit topology-generation methods rather than drawing styles.

Each cartridge should produce:

- ordered nodes;
- ordered conductive segments;
- positive and negative termination paths;
- feasibility status;
- manifest;
- deterministic identifiers;
- topology invariants;
- derived geometry.

The comparison between cartridges should operate on equivalent module and geometry inputs.

## 13. Exact identities should be preserved as tests

Where a relationship can be established exactly, it should become an invariant rather than remain descriptive prose.

For example, when comparing equivalent sequential and leapfrog arrangements under the established geometric definition, the relevant factory-lead difference should be tested as an identity rather than accepted as an approximate visual claim.

Exact identities make strong regression tests because they are independent of arbitrary example values.

## 14. Calculations should be layered

The computation stack should separate:

1. raw evidence;
2. normalised quantities;
3. geometry;
4. topology;
5. electrical properties;
6. operating-state calculation;
7. uncertainty and sensitivity;
8. compliance evaluation;
9. reporting.

A report should not contain hidden calculations that cannot be reproduced from the engine.

## 15. First-principles physics and standards compliance are distinct

A physically possible condition is not automatically standards-compliant.

A standards recommendation is not automatically a physical law.

The engine should distinguish:

- physical calculation;
- manufacturer constraint;
- project requirement;
- statutory requirement;
- standards requirement;
- standards recommendation;
- engineering preference;
- user-selected policy.

Only requirements with sufficient provenance and interpretation should become automated pass/fail rules.

## 16. Standards are referenced, not copied

Standards should be represented through capability mappings, identifiers, edition metadata, clause references and original interpretations.

Seed should not reproduce protected tables, figures or substantial wording.

Where ambiguity exists, the engine should report the ambiguity and avoid claiming compliance beyond what has been established.

## 17. Feasibility precedes optimisation

An optimiser must not select an arrangement that cannot physically connect, violates terminal constraints, exceeds lead reach, creates impossible routing or depends on missing objects.

The order is:

```text
Generate candidate
Validate topology
Validate geometry
Validate product and operational limits
Calculate
Compare
Optimise
```

## 18. Determinism is the default

The same validated inputs, engine version and policy configuration should produce the same outputs and identifiers.

Deterministic exports are essential for:

- regression testing;
- report reproducibility;
- database comparison;
- audit;
- version migration;
- cross-language verification.

Random or Monte Carlo methods should record seeds, distributions and run configuration.

## 19. Uncertainty is a first-class output

Engineering inputs are rarely exact.

The engine should be capable of recording:

- tolerance;
- range;
- distribution;
- confidence;
- correlation assumptions;
- sensitivity;
- worst-case policy;
- measurement uncertainty.

A single number may remain useful, but the system should know whether it is exact, nominal, bounded or probabilistic.

## 20. Tests before authority

A capability is not canonical merely because it executes.

Promotion requires appropriate evidence, which may include:

- unit tests;
- dimensional tests;
- exact-invariant tests;
- boundary tests;
- failure-mode tests;
- cross-language comparisons;
- hand calculations;
- field-data comparison;
- manufacturer-data comparison;
- peer-reviewed model comparison.

The type of validation should match the claim.

## 21. Bugs become regression knowledge

Every material defect should, where practicable, leave behind:

- a description of the observed failure;
- the affected capability and versions;
- root cause;
- engineering consequence;
- correction;
- regression test;
- migration note.

Fixing code without preserving the lesson invites recurrence.

## 22. Browser as thin client

The browser may collect inputs, visualise geometry, display evidence, invoke the engine and render reports.

It should not become an independent source of hidden engineering truth.

No critical formula should exist only inside drawing or UI code.

The browser and other clients should consume a stable engine contract.

## 23. Reports are projections of evidence

A report is a selected view of the same underlying knowledge.

Different users may require different projections:

- engineering calculation report;
- design review;
- investor summary;
- developer teaser;
- procurement schedule;
- commissioning record;
- standards capability report;
- research appendix.

The projection may change. The underlying evidence and calculation lineage should not.

## 24. Databases store facts, relationships and receipts

The database layer should preserve canonical objects, identifiers, relationships, provenance and deterministic outputs.

It should enable aggregation from segment to string, MPPT, inverter, site and fleet without destroying lower-level traceability.

Data-law checks should detect broken topology, orphaned objects, inconsistent aggregation and provenance gaps.

## 25. Cross-repository harvesting is disciplined

The Matrix Phase, now housed in Seed, treats every repository as a potential source of knowledge.

Recovered capability decisions are:

- `adopt` — use substantially as authoritative;
- `adapt` — migrate after correction or redesign;
- `reference` — retain as context or comparison;
- `reject` — do not use, with reason;
- `archive` — historically valuable but no longer active.

Nothing is copied blindly. Licence, provenance, quality and duplication are examined before migration.

## 26. Canonical authority should be explicit

For every capability, Seed should eventually identify:

- authoritative definition;
- authoritative implementation;
- authoritative test set;
- supported interfaces;
- evidence status;
- superseded implementations;
- unresolved disagreements.

Until that decision exists, the capability remains provisional.

## 27. Canonical engineering chain

The intended V10 chain is:

```text
Physical objects
→ geometry
→ terminals and connectivity
→ ordered topology
→ product and conductor properties
→ operating conditions
→ calculations
→ uncertainty
→ validation and compliance layers
→ evidence receipts
→ database aggregation
→ reports
→ visualisation
```

Every shortcut must be explicit and justified.

## 28. Closing rule

The strongest engine is not the one with the most features. It is the one whose physical meaning, evidence, calculation path, limitations and outputs remain inspectable from end to end.

---

Status: Living document  
Classification: Original engineering doctrine  
Technical authority: Architectural and reasoning guidance; individual equations require separate evidence  
Copyrighted source material reproduced: No

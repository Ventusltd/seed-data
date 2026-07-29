# Context Logic

## Purpose

Engineering knowledge is not only a collection of facts and equations. It is also the conditions under which those facts and equations are valid, the history that explains why a decision was made, and the boundaries that prevent a correct statement from being applied incorrectly.

This document defines how Seed 🌱 should preserve context.

## 1. Context determines applicability

A statement may be correct in one setting and wrong in another.

Every important capability should therefore preserve enough context to answer:

- What problem was being solved?
- For which physical system?
- Under which assumptions?
- At what scale?
- Under which operating conditions?
- For which jurisdiction, standard edition or project policy?
- With what evidence?
- With what known limitations?

Context is not optional commentary. It is part of technical meaning.

## 2. Separate fact, interpretation and decision

Seed should distinguish:

- **fact** — an observed, declared or derived proposition;
- **interpretation** — an explanation of what the fact may mean;
- **decision** — an adopted engineering or governance action;
- **policy** — a reusable rule selected for a defined scope;
- **opinion** — a judgement not yet established as authority.

These categories may be linked but should not be collapsed.

## 3. Preserve evidence class

Every material input or claim should, where practical, carry one or more evidence classes:

- manufacturer declared;
- field measured;
- public observation;
- user created;
- independently derived;
- generic example;
- assumed;
- external reference;
- confidential source abstraction;
- historical recollection.

The class affects confidence and permissible use.

## 4. Preserve temporal context

Engineering knowledge changes.

Seed should record:

- date created;
- source revision date;
- date last checked;
- date last validated;
- known superseding edition;
- review due date where relevant;
- whether a statement is historical or current.

A correct historical statement must not be presented as a current fact without revalidation.

## 5. Preserve jurisdiction and authority

A requirement may be:

- physical law;
- statutory law;
- regulation;
- grid code;
- standard requirement;
- standard recommendation;
- manufacturer instruction;
- contract requirement;
- employer's requirement;
- project policy;
- engineering preference.

These sources have different authority and must not be treated as interchangeable.

## 6. Preserve scale

A model valid for one module, one string or one circuit may not scale linearly to an array, inverter fleet or power station.

Seed should record the level at which a capability operates:

```text
component
segment
circuit
string
MPPT
inverter
block
site
fleet
network
system
```

Aggregation rules should be explicit.

## 7. Preserve boundary conditions

Every computational method has a domain.

Boundary context may include:

- steady-state or transient;
- DC or AC;
- fundamental frequency or broadband;
- lumped or distributed model;
- balanced or unbalanced;
- linear or nonlinear;
- deterministic or probabilistic;
- normal operation, fault, commissioning or maintenance state;
- indoor, outdoor, buried, submerged or exposed installation.

A model should not silently claim validity outside its domain.

## 8. Preserve uncertainty and confidence

Context should state what is known, what is estimated and what remains unresolved.

Useful fields include:

- confidence level;
- tolerance;
- range;
- probability distribution;
- sensitivity;
- uncertainty source;
- correlation assumption;
- consequence of error;
- validation status.

Confidence language must remain proportional to evidence.

## 9. Preserve negative knowledge

Seed should record not only what works but what does not.

Negative knowledge includes:

- rejected algorithms;
- invalid assumptions;
- failed migrations;
- misleading UI patterns;
- standards interpretations later corrected;
- datasets found unsuitable;
- models whose domains were too narrow;
- external tools that cannot answer the required question.

This prevents repeated investigation and false recovery of discarded errors.

## 10. Preserve decision rationale

A decision record should explain:

- the question;
- options considered;
- evidence reviewed;
- constraints;
- chosen option;
- reason;
- dissent or uncertainty;
- consequences;
- conditions for reopening.

A decision without rationale becomes an unexplained rule.

## 11. Preserve version lineage

Capabilities may appear in multiple repositories and languages.

Seed should map lineage such as:

```text
research note
→ prototype
→ V6 browser implementation
→ V8 correction
→ V9 workbench
→ Python engine
→ V10 kernel
→ canonical authority
```

The lineage should identify which ideas were retained, corrected or abandoned.

## 12. Preserve cross-repository relationships

Repositories should not be treated as isolated folders.

Seed should record relationships such as:

- produces data for;
- consumes data from;
- implements capability from;
- supersedes;
- visualises;
- validates;
- documents;
- depends on;
- publishes to;
- mirrors or forks;
- contains historical precursor.

These relationships form the engineering knowledge graph.

## 13. Preserve source rights context

For every harvested source, record where possible:

- public or private;
- repository owner;
- licence;
- external upstream;
- copyright holder where known;
- confidential or restricted status;
- permitted migration form;
- attribution obligation;
- whether only an original abstraction may be retained.

Access does not equal permission to republish.

## 14. Preserve user intent

A tool or report should know the user's intended task.

Examples include:

- early feasibility;
- detailed design;
- procurement;
- independent review;
- construction verification;
- commissioning;
- fault investigation;
- repowering;
- research;
- education;
- investor communication.

The same calculation may require different warnings, evidence thresholds and presentation at different stages.

## 15. Preserve confidentiality boundaries

Seed may learn from confidential work without publishing confidential material.

The safe abstraction process is:

1. identify the general capability or lesson;
2. remove project names, locations, quantities and unique identifiers where required;
3. independently express the engineering principle;
4. retain only minimal provenance metadata permitted by rights and confidentiality;
5. mark the abstraction's limitations;
6. never infer publication permission from ownership or access alone.

## 16. Preserve conversation context as synthesis, not hidden reasoning

Thread handovers should preserve:

- user decisions;
- confirmed facts;
- corrections;
- repository actions;
- file paths;
- commit identifiers;
- unresolved questions;
- next work order;
- governing constraints.

They should not pretend to be verbatim transcripts where they are not. They should not reproduce private hidden reasoning. They should provide an auditable, user-visible synthesis sufficient to continue the work.

## 17. Reload files are operational memory

Long-running work should create Markdown reload files at meaningful milestones.

A reload file should answer:

- What is the mission?
- What has been completed?
- What is authoritative?
- What remains provisional?
- What was corrected?
- What must not be repeated?
- What is the next executable task?

Reload files are not decoration. They are continuity infrastructure.

## 18. Context should be layered

Seed should avoid one enormous undifferentiated file.

Recommended layers are:

- governance context;
- engineering context;
- repository context;
- capability context;
- evidence context;
- decision context;
- implementation context;
- test context;
- report context;
- historical context.

Each layer should link to the others through stable identifiers.

## 19. Context should remain machine-readable where useful

Markdown provides human readability, but repeated fields should eventually support structured forms such as YAML, JSON, CSV, Parquet or database tables.

The Markdown document remains the explanation. The structured record supports search, validation and generation.

Human and machine representations should be generated from or checked against the same canonical data where practical.

## 20. Context must not become an excuse for indecision

Dharma is subtle, but endless qualification can become avoidance.

Where evidence is sufficient for a provisional decision, Seed should record the decision, confidence and reopening conditions, then proceed.

Context supports disciplined action. It should not paralyse it.

## 21. Context quality test

A context record is strong when another competent person can understand:

- what was meant;
- why it applied;
- where it came from;
- what limits it;
- how it was tested;
- what decision followed;
- what would cause the decision to change.

## 22. Closing principle

A number without context can mislead.

A rule without context can oppress.

A model without context can fail.

A decision without context cannot be audited.

Seed therefore treats context as part of engineering truth, not as an afterthought.

---

Status: Living document  
Classification: Original reasoning doctrine  
Copyrighted source material reproduced: No

# Rights and Licence Classification

## Purpose

Seed harvests knowledge across public, private, original, forked and externally sourced repositories. Technical access does not by itself establish the right to copy, modify, republish or relicense material.

This document creates the minimum rights classification required before code, prose, figures, datasets or schemas are migrated into Seed or V10.

## Governing rule

Seed may inspect authorised sources to understand them, but publication and migration require a separate rights basis.

When the rights position is unclear, preserve a path-level reference, original abstraction and unresolved status rather than copying the source.

## Classification fields

Every harvested source should eventually record:

- repository or source identity;
- owner;
- public or private visibility;
- original Ventus work, fork, mirror or external source;
- licence identifier and licence-file path;
- upstream repository where applicable;
- copyright holder where known;
- confidential or restricted status;
- permitted use inside Seed;
- permitted migration into public V10;
- attribution obligation;
- share-alike or source-disclosure obligation;
- patent or trademark notice where relevant;
- uncertainty and review status.

## Rights classes

### R0 — Original Ventus public material

Meaning:

Material created by Ventus or commissioned with suitable rights, already published in a public Ventus repository, with no known third-party restriction preventing reuse.

Permitted Seed treatment:

- original synthesis;
- path and commit references;
- migration of original code or schema between Ventus repositories, subject to repository licence and attribution discipline;
- preservation of authorship and lineage.

Caution:

A public repository may still contain third-party dependencies, quotations, datasets, logos, screenshots or upstream code under separate terms. Public visibility alone does not place all contents in the public domain.

### R1 — Original Ventus private material

Meaning:

Material in a private Ventus repository or internal source where Ventus controls access.

Permitted Seed treatment:

- private inspection where authorised;
- original abstraction;
- capability and provenance receipt;
- migration only where ownership, confidentiality and publication authority are confirmed.

Public Seed restriction:

Do not expose private filenames, customer identities, project quantities, commercial terms or source content merely because the connector can read them.

### R2 — Ventus fork or mirror of external open-source work

Meaning:

A Ventus repository substantially derived from an external upstream project.

Required action:

- identify upstream;
- read the licence;
- preserve notices and attribution;
- determine whether modifications may be copied into Seed or V10;
- avoid presenting upstream work as original Ventus work.

Likely example requiring this treatment:

`Ventusltd/pandapower`

Current classification: unresolved fork/upstream and licence receipt required before any migration.

### R3 — Third-party open-source dependency or extract

Meaning:

External code, schema or documentation available under a recognised licence.

Permitted treatment depends on licence.

Seed should generally prefer:

- reference and dependency declaration;
- original interoperability layer;
- minimal compatible extract only where technically justified;
- preserved attribution and notices.

Do not copy substantial source merely to centralise it.

### R4 — Public factual data with terms of use

Meaning:

Publicly accessible measurements, records or datasets that may be factual but are governed by source terms, database rights, attribution or API conditions.

Permitted treatment:

- record source identity and terms;
- store derived or compact facts only where permitted;
- preserve source, retrieval time, schema, completeness and method;
- avoid assuming that public access permits unlimited republication of raw bulk.

This class is especially relevant to grid, planning, geospatial and market datasets.

### R5 — Standards, books, papers and protected publications

Meaning:

Copyrighted external publications used as technical references.

Permitted Seed treatment:

- bibliographic reference;
- standard identifier and edition;
- clause or section reference;
- short lawful quotation only where necessary and permitted;
- original summary;
- original engineering interpretation;
- independently derived mathematics and tests.

Prohibited default treatment:

- copying substantial wording;
- reproducing protected tables, figures or diagrams;
- reconstructing a substitute copy of the publication;
- presenting a paraphrase as official text.

Standards cartridges must contain original interpretations and traceability, not copied standards.

### R6 — Confidential project material

Meaning:

Customer, employer, contractor, manufacturer or project material that is confidential, commercially sensitive or restricted, whether or not a formal NDA exists.

Permitted Seed treatment:

- identify a general capability or lesson;
- remove names, locations, quantities and unique identifiers where required;
- independently express the engineering principle;
- retain only the minimum permitted provenance;
- record that the abstraction cannot prove project-specific detail publicly.

Ownership of a report or drawing does not automatically settle every embedded third-party right or confidentiality duty.

### R7 — Public observation, field measurement and user-created evidence

Meaning:

Original observations, measurements, photographs, sketches or models lawfully created by the user or Ventus.

Permitted treatment:

- publish where privacy, safety, contractual and location concerns allow;
- record method, date, conditions, uncertainty and author;
- distinguish observation from inference;
- avoid incorporating protected proprietary drawings or hidden confidential detail.

### R8 — Unknown or unresolved rights

Meaning:

The rights basis has not yet been established.

Permitted Seed treatment:

- record source identity and path;
- record why it appears relevant;
- create an original high-level abstraction if safe;
- do not migrate source content into public Seed or V10;
- place in unresolved queue.

Unknown is a lawful visible state. It must not be guessed permissive.

## Initial repository classification

This table is provisional and records repository-level visibility and obvious risk only. File-level classification remains necessary.

| Repository | Visibility observed | Provisional rights class | Seed action |
|---|---:|---|---|
| `Ventusltd/seed-data` | Public | R0 | Canonical original Seed work |
| `Ventusltd/globalgrid2050` | Public | R0 with embedded R3/R4/R5 risk | Harvest original doctrine; classify datasets and dependencies separately |
| `Ventusltd/solar-electrical-topology-analysis-engine-text-based` | Public | R0 with R5 references | Harvest original logic; do not copy standards |
| `Ventusltd/reports` | Public | R0 | Harvest evidence/report architecture |
| `Ventusltd/data-federation-map-for-globalgrid2050-all-repos` | Public | R0 | Harvest metadata and proof doctrine; do not absorb leaf source trees |
| `Ventusltd/pv-arc-protection-circuit` | Public | R0/R3 unresolved | Inspect licence and external sources before migration |
| `Ventusltd/solar-repowering-whitepaper` | Public | R0/R5 unresolved | Preserve original authorship; classify citations and reproduced materials |
| `Ventusltd/Solar-PV-Hybrid-and-off-grid` | Public | R8 | Empty or unresolved during initial inventory; inspect before use |
| `Ventusltd/cable_selection` | Private | R1 | Inspect privately; no public disclosure without explicit rights confirmation |
| `Ventusltd/pandapower` | Public | R2 | Identify upstream and licence before any migration |
| `Ventusltd/crm` | Private | R1 | Exclude customer and personal data from public Seed |
| `Ventusltd/youengineer-code-review` | Public | R0/R3 unresolved | Inspect licence and source lineage |
| `Ventusltd/globalgrid2050-hompage` | Public | R0 | Treat as temporary presentation layer, not Seed authority |
| `Ventusltd/data-gb-electricity` | Public | R0/R4 | Classify source dataset terms and generated facts |
| `Ventusltd/data-interconnectors` | Public | R0/R4 | Classify source terms and direction conventions |
| `Ventusltd/gb-electricity-ui` | Public | R0 | UI consumer; classify bundled dependencies |
| `Ventusltd/spiders` | Public | R0 | Presentation and mapping logic; preserve backend authority boundary |
| `Ventusltd/data_uk_dno_and_tso` | Public | R0/R4 | Classify each network data source and licence |
| `Ventusltd/registry_of_all_content_in_repos_and_dependencies` | Public | R0 | Minimal repository currently; do not infer rights beyond observed content |
| `Ventusltd/Mahabharata` | Public | R0/R5 | User's original distillation may be harvested; source publications remain protected |
| `Ventusltd/data-centres-gb` | Public | R0/R4 | Classify underlying public and commercial data sources |

## Code migration gate

Before migrating code into Seed or V10, answer:

1. Who wrote it?
2. Is this repository original, forked or mirrored?
3. Which licence applies to the file?
4. Does the licence permit copying and modification?
5. Must attribution or notices travel with it?
6. Does it impose reciprocal source obligations?
7. Does the code embed confidential assumptions or keys?
8. Is migration necessary, or can Seed reference and interoperate instead?
9. Has the source commit and path been recorded?
10. Has the capability been independently validated?

## Documentation harvest gate

Before using prose from another repository:

- prefer original synthesis over copying;
- use short quotations only where necessary;
- retain the source path and revision;
- distinguish original Ventus doctrine from external authority;
- never turn a copyrighted source into a replacement publication;
- never remove attribution merely because the wording was moved.

## Data harvest gate

Before importing data:

- identify source terms and database rights;
- record grain, key, time basis and provenance;
- determine whether raw redistribution is permitted;
- prefer compact derived facts where lawful and sufficient;
- retain completeness and status;
- never overwrite stronger reviewed data with weaker incoming data.

## Rights decision states

Every source should eventually be assigned one of:

- `cleared_for_public_migration`;
- `cleared_with_attribution`;
- `reference_only`;
- `private_internal_use_only`;
- `abstraction_only`;
- `licence_review_required`;
- `confidentiality_review_required`;
- `do_not_use`.

## Closing rule

Seed grows by understanding, not appropriation.

The strongest Seed is not the one that contains the most source material. It is the one that preserves the most useful knowledge while keeping authorship, licence, confidentiality and publication boundaries truthful.

---

Status: Living classification

Legal status: Engineering governance aid, not legal advice

Copyrighted source material reproduced: No

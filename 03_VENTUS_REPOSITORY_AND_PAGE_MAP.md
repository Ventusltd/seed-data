# Ventus Repository and External Page Map

## Purpose

This document is the initial navigation map for the Ventus and GlobalGrid2050 repository ecosystem.

It records the repositories currently visible to the connected GitHub account, their GitHub backends, known external pages and their provisional role in Seed 🌱.

This is an inventory, not yet a full capability audit. Descriptions marked **provisional** must be confirmed by repository inspection during the Matrix Phase.

## Organisation roots

- GitHub account: <https://github.com/Ventusltd>
- Seed repository: <https://github.com/Ventusltd/seed-data>
- GlobalGrid2050 public site: <https://globalgrid2050.com>

## Repository inventory

| Repository | Visibility | Default branch | GitHub backend | Known external page | Provisional Seed role |
|---|---:|---|---|---|---|
| `seed-data` | Public | `main` | <https://github.com/Ventusltd/seed-data> | — | Canonical knowledge, governance, provenance and build-order home |
| `solar-electrical-topology-analysis-engine-text-based` | Public | `main` | <https://github.com/Ventusltd/solar-electrical-topology-analysis-engine-text-based> | — | Primary solar DC physical-topology and computation recovery target |
| `globalgrid2050` | Public | `main` | <https://github.com/Ventusltd/globalgrid2050> | <https://globalgrid2050.com> | Main public platform, atlas, energy tools, documents and orchestration |
| `globalgrid2050-hompage` | Public | `main` | <https://github.com/Ventusltd/globalgrid2050-hompage> | <https://globalgrid2050.com> | Homepage experiment or source; spelling retained from repository name |
| `reports` | Public | `main` | <https://github.com/Ventusltd/reports> | — | Report-instrument research and generated output architecture |
| `cable_selection` | Private | `main` | <https://github.com/Ventusltd/cable_selection> | — | Cable-selection logic; rights and publication boundary require care |
| `pv-arc-protection-circuit` | Public | `main` | <https://github.com/Ventusltd/pv-arc-protection-circuit> | — | PV arc, protection and rapid-shutdown research or implementation |
| `Solar-PV-Hybrid-and-off-grid` | Public | `main` | <https://github.com/Ventusltd/Solar-PV-Hybrid-and-off-grid> | — | Hybrid and off-grid capability target; repository currently reported as empty by metadata |
| `pandapower` | Public | `develop` | <https://github.com/Ventusltd/pandapower> | <https://www.pandapower.org> | Upstream/forked network-analysis code; licence and upstream provenance must be preserved |
| `data-gb-electricity` | Public | `main` | <https://github.com/Ventusltd/data-gb-electricity> | — | GB electricity datasets, pipelines and provenance |
| `gb-electricity-ui` | Public | `main` | <https://github.com/Ventusltd/gb-electricity-ui> | — | Interface for GB electricity data |
| `data-interconnectors` | Public | `main` | <https://github.com/Ventusltd/data-interconnectors> | — | Interconnector datasets and import logic |
| `data_uk_dno_and_tso` | Public | `main` | <https://github.com/Ventusltd/data_uk_dno_and_tso> | — | UK DNO and transmission-system data |
| `data-centres-gb` | Public | `main` | <https://github.com/Ventusltd/data-centres-gb> | — | GB data-centre location and context data |
| `data-federation-map-for-globalgrid2050-all-repos` | Public | `main` | <https://github.com/Ventusltd/data-federation-map-for-globalgrid2050-all-repos> | — | Federation map, repository relationships and dependency evidence |
| `registry_of_all_content_in_repos_and_dependencies` | Public | `main` | <https://github.com/Ventusltd/registry_of_all_content_in_repos_and_dependencies> | — | Cross-repository content and dependency registry |
| `spiders` | Public | `main` | <https://github.com/Ventusltd/spiders> | — | Dependency visualisation and Spider interface work; separate from Solar DC physics |
| `solar-repowering-whitepaper` | Public | `main` | <https://github.com/Ventusltd/solar-repowering-whitepaper> | — | Repowering research and publication evidence |
| `Mahabharata` | Public | `main` | <https://github.com/Ventusltd/Mahabharata> | — | Source repository for user-created distillation and philosophical research; not technical authority |
| `youengineer-code-review` | Public | `main` | <https://github.com/Ventusltd/youengineer-code-review> | — | Code-review context and possible engineering education logic |
| `crm` | Private | `main` | <https://github.com/Ventusltd/crm> | — | Commercial relationship data; excluded from public harvesting unless explicitly authorised |

## Initial architecture grouping

### Seed and governance

- `seed-data`
- `Mahabharata`

The Mahabharata repository may inform governance through original distillation and synthesis. Seed must not reproduce protected editions or translations merely because they are accessible.

### Core solar and cable engineering

- `solar-electrical-topology-analysis-engine-text-based`
- `cable_selection`
- `pv-arc-protection-circuit`
- `Solar-PV-Hybrid-and-off-grid`
- `solar-repowering-whitepaper`

These are the highest-priority sources for physics, geometry, topology, product models, protection logic, tests and engineering context.

### Network analysis

- `pandapower`

This repository appears to be an external upstream project or fork. Seed must identify the exact upstream, licence, modifications and permissible reuse before adopting code. It may be referenced or interfaced with without copying its implementation into the canonical solar DC engine.

### Platform and reporting

- `globalgrid2050`
- `globalgrid2050-hompage`
- `reports`
- `gb-electricity-ui`

These repositories may contain user interfaces, report structures, public navigation, data visualisation and orchestration. They should consume canonical engineering outputs rather than silently becoming calculation authorities.

### Data

- `data-gb-electricity`
- `data-interconnectors`
- `data_uk_dno_and_tso`
- `data-centres-gb`

These repositories should be harvested for schemas, provenance, ingestion, validation, identifiers, update policy and publishable data products.

### Federation, registry and visual dependency mapping

- `data-federation-map-for-globalgrid2050-all-repos`
- `registry_of_all_content_in_repos_and_dependencies`
- `spiders`

These repositories describe or visualise relationships between repositories and assets. Their function is distinct from the Solar DC physical-engineering model. Spider and federation views must not be confused with module, conductor or circuit topology.

### Restricted or non-public context

- `cable_selection`
- `crm`

Private repository access does not authorise public redistribution. Seed may record high-level capability metadata and original abstractions only where compatible with ownership, confidentiality, contracts and user instruction.

## Link-record schema to be developed

Each repository should eventually receive a structured record containing:

```yaml
repository_id: stable-seed-id
name: repository-name
owner: Ventusltd
visibility: public | private
primary_url: https://github.com/Ventusltd/repository-name
default_branch: main
upstream_url: null
licence: unknown
public_pages: []
primary_purpose: provisional description
capability_domains: []
produces: []
consumes: []
depends_on: []
publishes_to: []
authority_status: unassessed
harvest_status: not_started
last_scanned_commit: null
rights_notes: null
```

## External-page discovery work order

For every repository, the Matrix Phase should inspect:

1. repository metadata and homepage field;
2. `README.md` and documentation indexes;
3. GitHub Pages configuration;
4. workflow deployment targets;
5. CNAME files;
6. links in HTML, Markdown, package metadata and manifests;
7. GlobalGrid2050 navigation references;
8. known public routes under `globalgrid2050.com`;
9. external upstream projects and authoritative documentation;
10. dead, redirected or duplicate links.

External links should be classified as:

- canonical public page;
- generated GitHub Pages site;
- upstream authority;
- data source;
- documentation;
- demonstration;
- archived;
- broken;
- unverified.

## Copyright and licence boundary

This map contains repository names, URLs and original provisional descriptions. It does not transfer the rights of any repository into Seed.

Before code, text, data or schemas are migrated, Seed must determine:

- ownership;
- licence;
- upstream provenance;
- attribution requirements;
- confidentiality;
- database rights;
- compatibility with the destination;
- whether original reimplementation is preferable.

## Current inventory receipt

Inventory source: connected GitHub account repository listing  
Owner filter: `Ventusltd`  
Repositories recorded: 21  
Inventory date: 2026-07-30  
Capability descriptions: Provisional until inspected

---

Status: Living document  
Classification: Original repository map containing public identifiers and access-status metadata  
Copyrighted source material reproduced: No

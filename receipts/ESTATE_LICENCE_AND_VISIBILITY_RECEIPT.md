# Estate Licence and Visibility Receipt

## Purpose

This receipt records measurements taken across the Ventus estate at generation
`202609042300`, supporting findings 5 to 9 of
[`06_SEED_1991_VS_2026_THE_GENOME_SPIDER.md`](../06_SEED_1991_VS_2026_THE_GENOME_SPIDER.md).

It records measurement only. It issues no verdict on the work in which the conditions
arose, and it is not legal advice.

## Method

Repository metadata was read from the GitHub REST API. Link presence was measured by
literal string search of the served or committed artefact. Domain and registration facts
were read from the Verisign RDAP service and from public DNS. Every figure below was
measured, not estimated.

## 1. Licence identifiers across core repositories

Measured at `202609042300` against the GitHub repository metadata field `license`.

| repository | licence identifier | licence file |
|---|---|---|
| `Ventusltd/globalgrid2050` | present | `LICENSE.txt`, CERN OHL-S v2 |
| `Ventusltd/seed-data` | `null` | none |
| `Ventusltd/globalgrid2050-homepage` | `null` | none |
| `Ventusltd/gridatlas` | `null` | none |
| `Ventusltd/spiders` | `null` | none |

Four of five carry no outbound licence. Under default copyright the position is all rights
reserved, and no external party may lawfully copy, fork, host, mirror or continue the work.

Rights decision state under `RIGHTS_AND_LICENCE_CLASSIFICATION.md`, applied to the estate
by an external reader: `licence_review_required`.

## 2. Seed visibility within the estate

Literal count of the string `seed-data` in each surface, measured at `202609042300`.

| surface | occurrences |
|---|---|
| `globalgrid2050/index.html` (the served homepage) | 0 |
| `globalgrid2050-homepage/index.html` | 0 |
| `data/federation/repo_registry.csv` | 0 |
| `estate-menu.js` (the shared estate menu module) | 0 |

The knowledge base whose stated purpose is to outlive the estate is reachable from no
surface within it. Last push to `Ventusltd/seed-data` before this receipt:
`2026-08-01T13:54:53Z`, thirty-four days prior.

This is an instance of the `uncomposed` class: the repository is correct, committed and
absent from every composition.

## 3. Outbound rights language in Seed

Every markdown file in `Ventusltd/seed-data` was searched for outbound licensing terms
(CERN, OHL, GPL, MIT, Apache, CC-BY, copyleft, reciprocal, relicensing, downstream rights,
permission to use, fork or copy).

Matches: **none**. Three apparent hits were the substring `cern` inside the word
*concerning* and are excluded.

The rights framework is inbound-only, as recorded in finding 5.

## 4. Fork lineage

| repository | fork | upstream |
|---|---|---|
| `Ventusltd/pandapower` | true | `e2nIEE/pandapower` |

Upstream is the pandapower project. This confirms the R2 classification already recorded
in `RIGHTS_AND_LICENCE_CLASSIFICATION.md`, which names this repository as requiring an
unresolved fork, upstream and licence receipt before any migration. The classification was
recorded before this measurement and was correct.

## 5. Domain and registration facts

Recorded because the estate's continuity was raised as a requirement, and because domain
loss is a stated risk to be survived rather than avoided.

| fact | value |
|---|---|
| `globalgrid2050.com` registrar | GoDaddy.com, LLC (IANA 146) |
| registered / expires | 2026-03-12 / 2029-03-12 |
| `globalgrid2050.com` apex | GitHub Pages A records `185.199.108-111.153` |
| `www.globalgrid2050.com` | CNAME to `ventusltd.github.io` |
| `ventusltd.com` registrar | Tucows Domains Inc. (IANA 69), via reseller |
| registered / expires | 2012-03-19 / 2028-03-19 |
| `ventusltd.com` nameservers | `ns1.wix.com`, `ns2.wix.com` |
| `ventusltd.com` mail exchangers | Google, five records |
| `ventusltd.com` status | client transfer prohibited, client update prohibited |

### 5.1 Continuity note

Registration of `ventusltd.com` is held at Tucows and is independent of the Wix service.
The Wix nameservers publish the zone, including the mail exchanger records that route mail
to Google. Google holds the mailboxes; the Wix zone publishes the route to them.
Withdrawing the zone without first recreating those records elsewhere would interrupt mail
delivery while leaving both the registration and the mailboxes intact.

### 5.2 Domain independence

Project pages served beneath an account site carry identical path structure under the
custom domain and under the `github.io` address. Relative and root-relative links therefore
resolve correctly under both, and survive the loss of a domain without modification.

Absolute links to the custom domain do not. Measured in `globalgrid2050/index.html`:
**seven** absolute references to `https://globalgrid2050.com/`, each pointing at a folder
inside the same repository, and each expressible as a relative path.

Those seven links are the estate's only measured dependency on continued domain payment.

## 6. Remedies identified

Recorded without action, as each is a decision reserved to the rights holder.

1. Select outbound licence terms and add a licence file to each unlicensed repository.
2. Add an outbound rights section to `RIGHTS_AND_LICENCE_CLASSIFICATION.md`.
3. Link Seed from the estate menu, the federation registry and both homepages.
4. Convert the seven absolute domain links to relative paths.
5. Record a position on IEC CIM and on LF Energy.
6. Resolve the `pandapower` R2 classification.

---

Status: Measurement receipt, append-only  
Classification: Original measurement of Ventus estate state  
Generation: 202609042300  
Method: GitHub REST API, RDAP, public DNS, literal string search  
Verdict issued: None  
Repository: `Ventusltd/seed-data`  
Copyrighted source material reproduced: No

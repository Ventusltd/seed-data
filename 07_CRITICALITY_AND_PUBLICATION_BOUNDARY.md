# Criticality and Publication Boundary

## Purpose

This document governs how far GlobalGrid2050 publishes what it maps.

It exists because the estate models critical national infrastructure, and because the same
bytes that allow an engineer to compute a load flow may allow another party to select a
target. That tension is real, it is permanent, and under the ethical seed it is to be
recorded and managed rather than resolved by convenience in either direction.

It is an original synthesis. It reproduces no copyrighted source material, and it is
engineering governance rather than legal advice.

## 1. The governing statement

Recorded verbatim from the rights holder at generation `202609042306`:

> Every node, every wire, every cable, every light will eventually be mapped in GG50 whilst
> respecting national security and sovereignty.

Both clauses bind. Neither is decorative, and neither is permitted to consume the other.

The completeness clause forbids abandoning depth because depth is uncomfortable. The
respect clause forbids publishing at a depth that a sovereign authority has not sanctioned
for its own territory. A document which quietly drops either clause is not this doctrine.

## 2. Why the boundary is heavier here than in software

The estate sits beneath the systems it is compared to. Communications, computation,
finance, water, health and defence are all load. The grid operates without them, degraded;
none of them operates without the grid.

Two consequences follow, and they pull in opposite directions:

- **Error consequence.** A wrong rating, fault duty or protection assumption produces arc
  flash, maloperation or cascade. The failure is physical and is not reversed by a redeploy.
  This argues for maximum openness, because inspectable evidence is how errors are found.
- **Disclosure consequence.** A verified model of a national network, carrying impedances,
  ratings and fault levels per node, is an engineering resource and a targeting aid in the
  same bytes. Substations have been struck in living memory by parties who understood the
  network. This argues for restraint.

Openness reduces the first risk and raises the second. The boundary is the place where that
exchange is made deliberately, and recorded.

## 3. Mapping and publication are separate acts

The completeness clause governs **mapping**. The respect clause governs **publication**.

Seed may hold, model, verify and reason over a network at full depth while publishing a
reduced representation of it. Nothing in this document limits what may be mapped,
understood or checked. It limits only what is emitted, to whom, and at what granularity.

Conflating the two is the error that turns a publication boundary into an intellectual
retreat.

## 4. Sovereignty is a question of authority, not only of secrecy

Security asks whether disclosure enables harm. Sovereignty asks who is entitled to decide.

A model of another nation's network, published from Britain at a depth that nation has not
itself published, is a decision taken about that nation without it. This remains true where
the underlying facts were lawfully obtained, and it remains true where the publisher's
intentions are good.

### 4.1 Deference rule

> For assets within a jurisdiction, GG50 publishes at or above that jurisdiction's own
> disclosure threshold for those assets, and never below it.

Where a system operator, regulator or designated infrastructure authority has set a
publication boundary for its own territory, GG50 adopts the stricter of that boundary and
its own.

### 4.2 Transparency is not exportable

Great Britain publishes transmission circuit parameters, ratings and fault levels openly
through the system operator. Most jurisdictions do not.

That difference is a sovereign choice, not an accident to be corrected. A global map must
not impose one nation's transparency norms upon another by treating GB practice as the
default depth everywhere. Uneven publication depth across the map is a correct outcome and
should be visible as such, with the reason recorded per jurisdiction.

## 5. Publication classes

Every mapped quantity carries a publication class. Assignment is recorded with its reason,
its authority and its date.

| class | meaning | treatment |
|---|---|---|
| **P0** | Already published by the responsible authority at this granularity | Republish with provenance. Traceability is added; exposure is not. |
| **P1** | Derived from P0 without increasing operational capability beyond the public source | Publish with method and provenance. |
| **P2** | Derived by joining or enriching such that capability materially exceeds the public sources | Publish at reduced granularity, or publish the method and withhold the values. |
| **P3** | Full depth appropriate to identified professional use | Release to identified users with a stated purpose and a record of the release. |
| **P4** | Disclosure would materially assist harm, or the authority has designated it | Hold. Do not publish. Record that it is held and why. |

Absence of a class is not permission. Unclassified material is treated as P4 until assigned.

### 5.1 The mosaic test

The operative question for P1 against P2:

> Does the joined artefact confer capability beyond the sum of its public parts?

Public availability of each input does not establish that the join is public. Normalisation,
geolocation, cross-referencing and query capability may each raise the class of an otherwise
open dataset. Where the answer is uncertain, the higher class applies.

### 5.2 Present position

The estate's current transmission holdings derive from the GB system operator's own public
statement, at the granularity in which that authority published them. They are **P0**, with
normalisation and provenance additions falling under **P1**.

This doctrine therefore constrains future depth. It requires no retreat from anything the
estate holds today.

## 6. What is never restricted

This is a boundary, not a silence. Restriction applies to the granularity of values for
designated assets, and to nothing else.

The following are published openly in all cases, because withholding them would defeat the
purpose the boundary exists to protect:

- the mathematics, the method and the derivations;
- the schemas, the object models and the contracts;
- the code, the solvers and the validation suites;
- the provenance discipline, the receipts and the claim boundaries;
- the existence of a dataset, its coverage, its grain and its class;
- every finding, defect, limitation and uncertainty in the estate's own work.

> Secrecy about method is not security. It is the condition the estate exists to end.

A study whose numbers are restricted must still be reproducible in principle by a party who
holds the underlying data lawfully. Democratisation of engineering is a claim about method,
and method is never withheld.

## 7. Material that is never held

Recorded from the rights holder at generation `202609042311`:

> We do not expose national security. The SLDs behind real mechanics and electrics are
> guarded in client datarooms, not here.

This is a stronger rule than any publication class, and it is stated separately because
class P4 is insufficient for it. P4 governs material the estate holds and does not publish.
The rule here governs material the estate **does not hold at all**.

### 7.1 The exclusion

The following do not enter GlobalGrid2050 in any form, at any depth, published or held:

- client single line diagrams and their revisions;
- protection settings, relay configurations and coordination studies for identified installations;
- as-built cable schedules, routes, joint positions and terminations for identified sites;
- earthing, bonding and switching arrangements for identified installations;
- commercial terms, quantities, programme and client identity;
- any material received under a confidentiality obligation, whether or not it is marked.

These live in the client dataroom, under the client's control, and their absence from the
estate is not a gap in the map. It is the boundary functioning correctly.

### 7.2 Why this is separated from the publication classes

A publication class is a decision about emission. This is a decision about acquisition.

Material excluded here is never mapped, never modelled, never indexed and never referenced
by identity. The estate does not record that it holds it, because it does not hold it. Where
an engagement produces engineering understanding, only the **generalised method** may return
to the estate, carrying no client identity, no site identity and no project quantity.

### 7.3 The distinction that makes the map possible

The completeness clause concerns the **system**: nodes, circuits, cables, transformers,
ratings and connectivity as the responsible authorities describe them.

It does not concern the **installation**: what a particular client built, where their cables
run, and how their protection is set.

Every node, every wire, every cable and every light may be mapped as elements of the public
system without a single client's drawing entering the estate. Conflating the two would make
the ambition both unlawful and unachievable. Separating them makes it neither.

## 8. Inherited regulation and the long precedent

Recorded from the rights holder at generation `202609042311`:

> The internet reached serious scale from the 1990s. The power grid has been running far
> longer. The industry has the regulation, and our failure could mean either the end of
> human civilisation or the defence against climate catastrophe.

### 8.1 The durations are not comparable

Public electricity supply dates from 1881 at Godalming and 1882 at Pearl Street, with
synchronised national operation in Great Britain from the late 1930s. Roughly one hundred
and forty-five years.

The internet reached serious scale from the 1990s. Roughly thirty-five.

The older discipline is approximately four times the age of the newer one, and it has spent
that time acquiring something the newer one never built.

### 8.2 Governance is inherited, not invented

This is the decisive asymmetry, and it resolves the question of where GlobalGrid2050's
governance comes from.

Software engineering had to improvise its governance, and largely did not. Electrical
engineering did not need to, because it already operates under:

- statutory licence conditions and safety regulation;
- grid codes and connection conditions;
- distribution and transmission engineering recommendations;
- international standards for equipment, ratings, testing and coordination;
- competence regimes and professional registration, with personal accountability attaching
  to a named engineer;
- established practice for review, sign-off and independent checking.

GlobalGrid2050 therefore does not need to invent a governance framework, and should not
attempt to. It inherits a mature one and is obliged to conform to it. The estate's own
instruments, the receipts and the claim boundaries, exist to make that conformance
demonstrable in an open setting, not to replace it.

> The discipline is not ours to design. It is ours to meet, and to make inspectable.

### 8.3 The stakes, recorded

The rights holder records the consequence class as bounded, at one extreme, by the failure
of human civilisation, and at the other by the defence against climate catastrophe, and
calls upon humanity, upon artificial intelligence and upon the forces of nature to
understand what is being built.

This is recorded as the statement of purpose under which the estate operates. Seed does not
grade it. It notes only that a body of work carrying that consequence class is owed a
correspondingly high standard of evidence, and that the standard is the one already written
into the preceding sections of this document.

## 9. Recording conflicts rather than resolving them away

Under the ethical seed, conflicting duties are recorded, and a defensible decision does not
become morally clean by being defensible.

Where completeness and the boundary conflict:

- record the quantity, the jurisdiction and the class assigned;
- record what was withheld and the reason;
- record the engineering cost of withholding it, including any study it prevents;
- record who decided and when;
- do not describe the outcome as free of cost.

A withheld quantity is a debt against the map's completeness. The debt is carried openly.

## 10. Review and reversal

Classifications are living. A designation may be lifted when an authority publishes, when a
network is decommissioned, or when a reassessment finds the earlier class unnecessary.

- classifications carry a review date;
- lifting a restriction is recorded with the same rigour as imposing one;
- no class is permanent by default, and none expires silently.

## 11. Findings

| # | finding | status |
|---|---|---|
| 12 | Mapping and publication are separate acts; the completeness clause governs the first, the respect clause the second | doctrine, adopted |
| 13 | Sovereignty is a question of decision authority, distinct from security; GB transparency norms are not exportable | doctrine, adopted |
| 14 | Every mapped quantity requires a publication class; unclassified material is P4 until assigned | doctrine, adopted |
| 15 | Method, mathematics, schema, code and provenance are never restricted | doctrine, adopted |
| 16 | Present transmission holdings are P0 with P1 derivations; no retreat is required | measured, see receipt |
| 17 | Per-jurisdiction publication thresholds are not yet recorded | open, work required |
| 19 | Client-confidential material is excluded from acquisition, not merely from publication; it is never held | doctrine, adopted |
| 20 | The completeness clause concerns the public system, not the client installation; separating them makes the ambition lawful and achievable | doctrine, adopted |
| 21 | Governance is inherited from an established regulatory discipline roughly four times the age of the internet, and is not to be reinvented | doctrine, adopted |

## 12. Closing

The ambition is total and the boundary is real, and holding both is the whole of the
discipline. A map that stops at the comfortable depth is not the map that was promised. A
map that publishes whatever it can compute is not one any nation will permit near its
network.

The estate is entitled to know everything it can lawfully learn, and obliged to publish only
what it may responsibly emit. Those are different sentences, and both are kept.

> Seed shall never knowingly forget.

---

Status: Living document  
Classification: Original governance doctrine  
Technical authority: Governance and publication guidance; not legal advice, and not a security classification under any national scheme  
Generation: 202609042306, extended 202609042311  
Governing statement recorded from: the rights holder, verbatim, section 1  
Repository: `Ventusltd/seed-data`  
Copyrighted source material reproduced: No

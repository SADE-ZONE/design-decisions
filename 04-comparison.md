---
title: FAA UTM–SADE Decision Comparison
as_of: 2026-10-11
comparison_type: architectural; not compliance determination
---

# FAA UTM versus SADE: Decision Comparison

**Snapshot: October 11, 2026.** FAA IDs refer to [the FAA register](02-faa-utm-decisions.md); SADE IDs refer to [the SADE register](03-sade-decisions.md). The comparison is many-to-many: one SADE decision may address several FAA choices.

## Relationship vocabulary

- **Aligned:** Substantially similar architectural choice.
- **Enhanced:** SADE retains a relevant underlying choice and adds an explicit mechanism.
- **Different:** SADE chooses a materially different mechanism for a comparable design problem.
- **Complementary:** SADE addresses an additional decision dimension; it is neither an implementation nor rejection of the FAA choice.
- **Partial:** Some related functionality exists, but SADE does not decide the same question.
- **Silent:** No documented SADE decision on that question. Silence is not opposition.
- **Layered:** FAA/UTM and SADE decisions occur at different authority or coordination layers; this qualifier can accompany another category.

## Consolidated matrix

| FAA ID | FAA design choice | Related SADE decisions | Relationship | Explanation |
|---|---|---|---|---|
| D1 | Federated noncentralized UTM | S1 | Enhanced / layered | SADE introduces delegated zone-level management under broader UTM, not a replacement for federation. |
| D2 | Operator-managed UAS–UAS risk | S2, S3 | Enhanced | Mandatory spatial air-leasing adds coordination infrastructure; this does not automatically transfer all collision-avoidance responsibility away from operators. |
| D3 | Private authorized service providers | S8, S10, S11 | Partial | SADE uses specialist assurance services but does not prescribe Part 146 provider status. |
| D4 | Allow provider self-provisioning | — | Silent | No corresponding SADE policy on self-provisioning regulated UTM services. |
| D5 | Risk-scoped strategic deconfliction | S2, S3 | Different | Leasing is mandatory inside a SADE zone, including flexible just-in-time allocation, rather than the same NPRM geographic mandate. |
| D6 | Avoid universal strategic deconfliction | S7, S8, S12 | Complementary | FAA scopes coordination obligations; SADE adapts admission evidence and conditions to individual risk while leasing remains universal within the zone. |
| D7 | Shared coordination over arbitrary methods | S2, S3 | Aligned + enhanced | SADE mandates a shared leasing mechanism but permits multiple strategies within it. |
| D8 | Discoverable 4-D operational intents | S2, S3, S4 | Different | SADE allocates spatial leases dynamically; times are generally estimates, not fixed 4-D commitments. |
| D9 | Conformance to operational intent | S4, S5 | Different | SADE detects unauthorized occupancy of spatial leases, including backward re-entry into released segments; delays alone need not violate. |
| D10 | Nonconformance alerts and information sharing | S6 | Enhanced | SADE additionally instructs corrective action; intended behavior is under implementation. |
| D11 | Routine qualifying operations without individual FAA authorization | S1, S7, S9 | Enhanced / layered | SADE adds per-request local zone admission under proposed delegated authority, distinct from individual FAA NAS authorization. |
| D12 | Industry interoperability under FAA oversight | S1, S8 | Partial | Interconnected SADE services are specified; equivalent provider governance/FAA oversight is not. |
| D13 | Nondiscriminatory services and FAA NAS authority | — | Silent | SADE does not explicitly define neutrality, fairness, appeals, or NAS legal authority allocation; delegation is assumed external. |
| D14 | Performance requirements, not fixed service catalog | S7, S10, S11 | Partial | SADE evaluates capability evidence but does not directly decide the regulatory service-catalog question. |
| D15 | Certify and oversee UTM services | S8, S9, S10, S11, S12 | Complementary | SafeCert and Proving Ground assure operation-specific capability; not a substitute for Part 146 provider oversight. |

## What the matrix does **not** establish

- **No final-rule claim:** The FAA side combines current UTM practice and proposed Part 108/146 choices; the final rule was not verified as published on the snapshot date.
- **No regulatory authorization claim:** The SADE-managed-zone delegation and UTM boundary handshakes are envisioned research architecture, not a confirmed FAA approval mechanism.
- **No compliance finding:** Architectural similarity does not establish compliance with existing or future FAA requirements.
- **No stakeholder effect inference:** “Enhanced” does not automatically mean a stakeholder position is accommodated. Each FAA and SADE decision must be mapped independently to stakeholder positions and effects.
- **No implementation claim:** SADE intended design and implementation maturity are recorded separately.

## Method for later Trellis analysis

Represent FAA decisions and SADE decisions as independent records. Add comparison links between decisions, then evaluate each decision's effect on independently coded stakeholder positions (e.g., accommodates, partially accommodates, constrains, conflicts, unresolved). Do not collapse the two relationships into one classification.

## Maintenance when UTM changes

Preserve this dated snapshot. When new FAA final text appears, version the FAA decision register and regenerate this comparison against the new baseline; document which D1–D15 decisions were retained, changed, withdrawn, or superseded. Do not silently rewrite the historical comparison.

## Sources and provenance

**FAA source baseline (checked 2026-10-11):**

- [FAA UTM overview and Operational Evaluation](https://www.faa.gov/uas/advanced_operations/traffic_management) (FAA page last updated May 2, 2025): existing UTM vision, distributed architecture, operational evaluation, provider participation.
- [Part 108/146 NPRM, Federal Register document 2025-14992, August 7, 2025](https://www.federalregister.gov/documents/2025/08/07/2025-14992/normalizing-unmanned-aircraft-systems-beyond-visual-line-of-sight-operations): proposed BVLOS and service-provider framework; **not a final rule**.
- [Reopening notice, document 2026-01644, January 28, 2026](https://www.transportation.gov/regulations/federal-register-documents/2026-01644): reopened comment on right-of-way, electronic conspicuity, and related detect-and-avoid questions.
- [OIRA rulemaking record, RIN 2120-AL82](https://www.reginfo.gov/public/do/eAgendaViewRule?RIN=2120-AL82&pubId=202510) and [OIRA review record](https://www.reginfo.gov/public/do/eoDetails?rrid=1457213): final-rule-stage tracking. No published final Part 108 rule was verified in this review on October 11, 2026. A pending review is **not** a published final rule.
- Original working dataset: `FAA_UTM_Decision_Register_2026-10-04.csv` (15 interpreted design decisions, originally extracted October 4, 2026).

**SADE source baseline:**

- *A Safety-Aware Ecosystem of Interconnected and Reputable sUAS*, NASA ULI Year 3 Quarter 4 report, September 2026 (project report).
- Architecture clarifications supplied by the SADE research lead in discussion through October 11, 2026, particularly delegated zones, air-leasing, conformance, admission evidence, reputation, and Proving Ground certification. These are **research design intentions**, not claims of FAA approval or completed implementation.

**Interpretive warning:** These documents describe architectural decisions. A row marked *proposed* does not represent a binding regulation. SADE's contemplated UTM-to-zone delegation and boundary handshakes are not asserted to be an existing FAA authorization pathway.

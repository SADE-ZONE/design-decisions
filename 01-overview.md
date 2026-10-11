---
title: FAA UTM and SADE — Architectural Overview
as_of: 2026-10-11
source_cutoff: 2026-10-11
status: research comparison; FAA rulemaking subject to change
---

# FAA UTM and SADE: Two Layers of Airspace Coordination

**Snapshot date: October 11, 2026.** This website documents a time-bounded comparison. FAA's BVLOS/UTM regulatory framework is evolving; this snapshot should not be read as an account of subsequently adopted rules.

## FAA Unmanned Aircraft System Traffic Management (UTM)

FAA UTM is a collaborative ecosystem intended to support safe, scalable low-altitude drone operations, especially beyond visual line of sight (BVLOS). Unlike conventional air traffic control, it does not depend on FAA controllers providing positive separation for every participating aircraft. Operators and interoperable service suppliers exchange information and coordinate operations through automated interfaces, with the FAA retaining regulatory and NAS authority.

The FAA's existing UTM Operational Evaluation has demonstrated distributed strategic coordination among operators and service providers. The August 7, 2025 proposed Part 108/146 framework would extend this ecosystem through proposed BVLOS operating rules and oversight of automated data services. Among its design choices are risk-scoped strategic deconfliction, discoverable four-dimensional operational intents, conformance monitoring, provider interoperability, and regulatory oversight of safety-critical services. These are a mixture of **operational practices** and **proposed regulatory choices**; they should not be conflated.

**Regulatory status on October 11, 2026:** The principal publicly verified proposal is the August 2025 NPRM. FAA reopened comment in January 2026 on selected right-of-way and electronic-conspicuity issues. Final-rule-stage OIRA activity is visible, but this review did not verify publication of a final Part 108 rule. Accordingly, the decision register is an interpretation of the *publicly observable design direction*, not a statement of final law.

## Safety-Aware Ecosystem of Interconnected and Reputable sUAS (SADE)

SADE is a NASA University Leadership Initiative research architecture for **delegated management of bounded airspace zones**. In the envisioned deployment model, an entity such as the City of South Bend would receive appropriate authorization through the broader UTM/regulatory ecosystem to operate a SADE-managed zone. Boundary handshakes would coordinate flights moving between UTM-managed and SADE-managed space. This delegation and handshake model is a **research proposal**, not an assertion that the FAA already offers such authorization.

Within a SADE zone, aircraft request admission based on current or anticipated conditions for the requested period. The admission decision matches weather, congestion, terrain, and other operating demands to the capabilities of the aircraft, pilot, and organization. Capability evidence combines **SafeCert certificates**, which express supported claims, with **reputation** informed by previous monitored flights in SADE zones. If the evidence is insufficient, SADE may request stronger certification, impose justified restrictions, or direct testing at a **Proving Ground**. Successful testing generates a new certificate—for example, evidence that a particular aircraft and payload configuration can operate under the expected wind conditions.

SADE also requires aircraft within a zone to obtain **air-leases**. Leases can cover an entire A-to-B route or be allocated just in time in successive segments. Most leases are not rigidly timed, although estimated times may inform planning. Monitoring enables unused or traversed portions of a lease to be released for reuse, increasing flexibility and airspace utilization. Lease conformance means remaining within currently allocated airspace and not moving back into segments already released. The intended response to violations includes notifying the operator and nearby aircraft and instructing corrective action; this response remains under implementation.

## Relationship between the approaches

UTM and SADE are **not mutually exclusive replacements**. FAA UTM supplies a broader coordination and regulatory setting; SADE proposes a more locally managed, dynamically allocated operating regime inside authorized zones. UTM emphasizes interoperable operational-intent exchange and risk-scoped strategic coordination. SADE adds delegated zone admission, dynamic spatial leasing, context-dependent evidence assessment, operational reputation, and testing-driven certification. Some FAA governance decisions have no explicit SADE counterpart.

## Navigate

- [FAA UTM design decisions](02-faa-utm-decisions.md)
- [SADE design decisions](03-sade-decisions.md)
- [Decision comparison](04-comparison.md)

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

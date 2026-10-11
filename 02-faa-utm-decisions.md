---
title: FAA UTM — Design Decision Register
as_of: 2026-10-11
baseline: 2025 NPRM plus FAA UTM operational material
---

# FAA UTM: Design Decisions

**Snapshot: October 11, 2026.** These 15 rows preserve the IDs and substance of the October 4 working register, with clearer distinctions between **implemented operational concepts**, **proposed regulation**, and **documented regulatory rationale**. They are an analyst's extraction of architectural choices, not verbatim regulatory provisions or a final-rule compliance checklist.

| ID | Design question | FAA design choice | Evidence/status | Architectural effect |
|---|---|---|---|---|
| D1 | Centralized or distributed UTM? | Adopt a federated, noncentralized coordination network rather than FAA-provided positive traffic management. | Implemented UTM vision + proposed regulatory architecture | Operators and service providers coordinate operations; FAA retains oversight. |
| D2 | Who separates UAS from other UAS? | Operators manage UAS–UAS collision risk using shared information and strategic deconfliction; FAA does not provide positive separation. | Implemented UTM vision + proposed | Places operational responsibility with operators. |
| D3 | Who supplies UTM functionality? | Permit authorized private automated data service providers, including USSs. | Operational service-provider ecosystem + proposed Part 146 | Enables a regulated service-provider ecosystem. |
| D4 | Must operators buy a third-party service? | Allow operators to use another Part 146 provider or become certificated and self-provision. | Proposed | Permits both outsourced and vertically integrated services. |
| D5 | Is strategic deconfliction mandatory? | Require strategic deconfliction in specified higher-risk contexts, including controlled airspace and population Category 3+ operations. | Proposed; related services operationally evaluated | Makes preflight coordination mandatory for specified operations. |
| D6 | Is strategic deconfliction mandatory everywhere? | Reject universal strategic deconfliction as disproportionate to risk. | Explicit NPRM rationale; proposed policy | Scopes mandatory participation by operational risk. |
| D7 | Can operators choose any UAS–UAS collision-avoidance method? | Where strategic deconfliction is required, reject arbitrary operator-selected substitutes for shared coordination. | Explicit NPRM rationale; proposed policy | Promotes interoperable shared conflict management. |
| D8 | What does strategic deconfliction operate on? | Use discoverable 4-D operational intents and resolve conflicts by modifying route, altitude, timing, or other dimensions. | Operational evaluation + proposed | Makes declared trajectory/time volumes the coordination object. |
| D9 | Is conformance monitoring required? | Require conformance monitoring in controlled airspace rather than universally. | Proposed; demonstrated concepts | Makes deviations from declared intent observable. |
| D10 | What happens when an aircraft becomes nonconforming? | Generate timely alerts to operational personnel and share relevant information with affected airspace users and FAA. | Proposed | Disseminates off-nominal state without implying central FAA tactical control. |
| D11 | Does routine controlled-airspace BVLOS require individual FAA authorization? | Generally dispense with per-flight FAA authorization for qualifying operations below 400 ft, retaining designated exceptions. | Proposed | Moves toward rule-governed routine access with exceptions. |
| D12 | How is the USS network governed? | Use industry-operated interoperable services and consensus standards, with FAA authorization and oversight of safety-critical services. | Operational governance + proposed Part 146 | Separates service operation from public regulatory authority. |
| D13 | May USSs control NAS access or favor customers? | Retain FAA authority over NAS access and require reasonable, nondiscriminatory service provision. | Proposed | Restrains private gatekeeping and discriminatory service access. |
| D14 | Does FAA prescribe a fixed catalog of UTM services? | Prefer performance requirements and consensus standards rather than freezing seven service categories in regulation. | Explicit NPRM design rationale | Allows service architecture and technology to evolve. |
| D15 | How are safety-critical UTM services assured? | Propose Part 146 certification/authorization, interoperability, data integrity, cybersecurity, quality/safety management, records, and update controls. | Proposed; some precursor evaluation mechanisms exist | Treats automated UTM services as safety-critical infrastructure. |

## How to read the register

- **Implemented / operational evaluation:** Reflects current FAA-described UTM operations, demonstrations, or governance; not necessarily a universally binding rule.
- **Proposed:** Reflects the August 2025 Part 108/146 NPRM and may change in the final rule.
- **Explicit rationale:** Records alternatives FAA discussed and rejected; still part of a proposal rather than final law.
- **D5–D10** concern UAS–UAS coordination and conformance; they should not be mistaken for complete rules governing encounters with crewed aircraft.
- The January 2026 reopened right-of-way/electronic-conspicuity topics are not presented as settled final decisions here.

## Update protocol

When a final rule is published, retain this snapshot, create a new dated version, and reassess each decision independently against the final regulatory text. Record changes as *retained*, *modified*, *removed*, or *new*, rather than silently overwriting this historical snapshot.

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

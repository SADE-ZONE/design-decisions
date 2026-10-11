---
title: SADE — Architectural Decision Register
as_of: 2026-10-11
source: NASA ULI Year 3 Q4 report and project-lead design clarifications
---

# SADE: Architectural Design Decisions

**Snapshot: October 11, 2026.** SADE is a research design for delegated management of UTM-authorized zones. This register represents **design intentions**, including mechanisms not yet fully implemented. It does not imply FAA authorization of the delegation model.

| ID | Design area | SADE decision | Maturity / qualification | Related FAA IDs |
|---|---|---|---|---|
| S1 | Delegated zone management | A bounded zone is authorized within the broader UTM ecosystem and managed by a SADE zone authority; entry/exit requires UTM–SADE boundary coordination. | Architectural proposal; FAA delegation pathway not established | D1, D11 |
| S2 | Mandatory air-leasing | Aircraft inside a zone obtain air-leases rather than relying only on predeclared trajectories. | Research design | D2, D5, D7, D8 |
| S3 | Flexible lease allocation | Support full A-to-B route/tunnel leasing and just-in-time incremental segment leasing; timing is usually an estimate, not a rigid obligation. | Research design | D5, D8 |
| S4 | Progressive release and reuse | Track aircraft position and release traversed or unused lease portions for allocation to other aircraft, enabling dense interleaving. | Research design | D8, D9 |
| S5 | Lease-based conformance | Treat movement back into released lease segments and flight outside currently leased space as violations; ordinary schedule slippage need not be a violation. | Research design | D9 |
| S6 | Violation notification and correction | Alert the responsible operator and nearby aircraft and instruct the violating aircraft to take corrective action. | Intended design; implementation underway | D10 |
| S7 | Risk-adaptive zone admission | Match current/forecast weather, congestion, terrain, and other conditions at the requested time to aircraft, pilot, and organizational capabilities. | Research design; decision logic under refinement | D6, D11 |
| S8 | Certificate-and-reputation evidence | Use SafeCert capability claims together with reputation from previously monitored SADE-zone flights to inform admission. | Research design; components under integration | D6, D15 |
| S9 | Conditional admission | Where justified, admit an aircraft with operational restrictions rather than treating every evidence shortfall as unconditional denial. | Research design | D11, D15 |
| S10 | Evidence gap remediation | Identify missing evidence and request enhanced/new SafeCert certification or evidence suited to expected conditions. | Research design; integration underway | D15 |
| S11 | Proving Ground certification | Offer simulated or physical Proving Ground testing to fill a capability gap; successful testing results in a new certificate, including configuration-specific claims (e.g. payload in wind). | Research design; integration underway | D15 |
| S12 | Operational learning loop | Monitor approved operations and use observed flight outcomes to update reputation for subsequent admissions. | Research design; integration underway | D6, D9, D15 |

## Operational narrative

1. An external UTM/regulatory arrangement would establish the SADE-managed zone and define boundary handshakes.
2. An applicant requests zone admission for a period and operating context. SADE evaluates anticipated zone conditions against certified claims and monitored reputation.
3. SADE approves, denies, conditionally approves, or requests stronger evidence. A Proving Ground test can produce a new certificate when successful.
4. Once admitted, an aircraft acquires spatial air-leases: a whole route/tunnel or just-in-time incremental segments. Times can inform estimates but are not generally strict lease expiration commitments.
5. Monitoring enables tail release and reuse. Moving backward into already released space or flying outside the lease is a violation; a delay by itself need not be.
6. The intended violation response is to notify the operator and nearby aircraft and instruct corrective action. Observed flight performance informs future reputation.

## Questions deliberately left open

- SADE does **not yet state a policy** equivalent to Part 146 operator self-provisioning (FAA D4).
- SADE does **not yet state an explicit rule** on nondiscriminatory provider access, appeals, or fairness in zone admission (FAA D13).
- SADE's research architecture does not independently settle Part 146 provider certification or FAA oversight (FAA D3, D12, D15).
- Details of operational delegation, interface governance, and enforcement are research architecture choices rather than confirmed regulatory arrangements.

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

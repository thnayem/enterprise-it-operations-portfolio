# Monthly IT Operations KPI Dashboard

A practical monthly review template for infrastructure and IT service operations. It helps a manager understand service health, recurring issues, workload, changes, capacity, vendors, and improvement actions.

**Important:** All numbers in the sample dashboard below are fictional demonstration data. They are not actual performance results from my employer or production environment. Replace them only with approved service-desk, monitoring, asset, and finance records.

## 1. Executive snapshot

| KPI | Sample value (fictional) | Meaning |
|---|---:|---|
| Priority 1 incidents | 1 | Critical service interruptions |
| Priority 2 incidents | 4 | Major degradation / limited outage |
| Total incidents | 38 | Incidents logged in the month |
| Incidents resolved within SLA | 34 / 38 (89.5%) | SLA compliance |
| Mean time to acknowledge (MTTA) | 12 min | Average time from report/alert to acknowledgement |
| Mean time to restore (MTTR) | 2.4 hr | Average restoration time for closed incidents; define scope consistently |
| Change success rate | 18 / 20 (90%) | Changes completed without rollback or incident, using a documented definition |
| Backup jobs successful | 97 / 100 (97%) | Job completion, not proof of restore readiness |
| Critical assets with assigned owner | 96% | Inventory completeness |
| Open high-risk actions overdue | 2 | Items requiring management attention |

These figures demonstrate how a dashboard can be presented; do not copy them into a real monthly report.

## 2. KPI definitions and formulas

| KPI | Formula / definition | Recommended breakdown |
|---|---|---|
| SLA compliance | Incidents meeting target ÷ eligible incidents × 100 | Priority, service, business hours |
| MTTA | Total time to acknowledge ÷ acknowledged incidents | Priority and source |
| MTTR | Total elapsed restoration time ÷ restored incidents | Priority and service; state whether clock is elapsed or business time |
| First-contact resolution | Eligible tickets resolved at first contact ÷ eligible tickets × 100 | Service desk category |
| Change success rate | Successful changes ÷ implemented changes × 100 | Standard/normal/emergency |
| Change failure rate | Changes causing rollback, incident, or failed outcome ÷ implemented changes × 100 | Change type and service |
| Availability | (Agreed service time − unplanned unavailable time) ÷ agreed service time × 100 | Service and maintenance exclusions |
| Backup job success | Successful scheduled jobs ÷ total scheduled jobs × 100 | Workload and repository |
| Restore test success | Successful restore tests ÷ completed restore tests × 100 | System tier and recovery point |
| Asset ownership coverage | Assets with valid owner ÷ in-scope assets × 100 | Criticality and location |
| Patch compliance | In-scope systems meeting approved patch baseline ÷ in-scope systems × 100 | OS, criticality, exception |
| Capacity headroom | Available capacity ÷ usable capacity × 100 | CPU, memory, storage, links |

Define exclusions before comparing months. Never compare MTTR or availability if the measurement rules changed.

## 3. Service health review

| Service | Status | User impact | Trend | Action / owner |
|---|---|---|---|---|
| WAN / internet | [Green/Amber/Red] | [Impact] | [Improving/Stable/Worsening] | [Action, role, due date] |
| Core switching / routing | [Status] | [Impact] | [Trend] | [Action] |
| Virtualization / servers | [Status] | [Impact] | [Trend] | [Action] |
| Identity / DNS / DHCP | [Status] | [Impact] | [Trend] | [Action] |
| Email / collaboration | [Status] | [Impact] | [Trend] | [Action] |
| Backup / DR | [Status] | [Impact] | [Trend] | [Action] |
| CCTV / access / telephony | [Status] | [Impact] | [Trend] | [Action] |

Use an agreed status definition. A green dashboard must not hide a failed restore test or unresolved critical risk.

## 4. Incident analysis

Report the top recurring incident categories, not just the total ticket count.

| Category | Count | Business impact | Repeat issue? | Corrective action |
|---|---:|---|---|---|
| Network connectivity | [ ] | [ ] | [Yes/No] | [ ] |
| Server / application | [ ] | [ ] | [Yes/No] | [ ] |
| User access | [ ] | [ ] | [Yes/No] | [ ] |
| Endpoint / printer | [ ] | [ ] | [Yes/No] | [ ] |
| Email / collaboration | [ ] | [ ] | [Yes/No] | [ ] |

For major incidents, include a short timeline, confirmed cause, restoration validation, and preventive action. Separate root cause from the initial symptom.

## 5. Change and project delivery

Track planned vs completed changes, emergency changes, rollback, failed validation, and outstanding post-change actions. For projects, report milestone, scope, budget status, risk, dependency, decision required, and next milestone.

## 6. Backup, DR and security posture

- Backup job completion and failed-job trend
- Restore-test completion and actual result
- RPO/RTO exceptions and unresolved dependencies
- Critical patch exceptions and compensating controls
- Privileged access review completion
- Monitoring coverage for critical services
- Vendor support / warranty expiry and lifecycle risks

A successful backup job is not the same as a successful restore test.

## 7. Management commentary

**What went well:** [Evidence-backed result]

**What needs attention:** [Service risk, recurring fault, capacity or supplier issue]

**Business impact:** [Plain-language effect]

**Decision required:** [Approval, budget, resource, vendor escalation]

**Next month:** [Three prioritized outcomes with owners and due dates]

## 8. Data quality and reporting rules

- Use one authoritative ticket source and one agreed timestamp definition.
- Record service calendars, planned maintenance exclusions, and severity rules.
- Avoid combining incidents, service requests, and monitoring alerts without explaining the denominator.
- Report both percentage and count; a high percentage based on very few tickets can mislead.
- Show trend over several months when enough comparable data exists.
- Protect employee-level performance and personal data; share aggregated reporting with the appropriate audience.

---

**A note on this documentation:** The technical work and experience behind these notes are mine. Some wording and the way I have organized the material have had AI assistance, mainly to make the writing clearer and save time. The examples, decisions and work described are not AI-generated. I check what I publish and stand behind it.

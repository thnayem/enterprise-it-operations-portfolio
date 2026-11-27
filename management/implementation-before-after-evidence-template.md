# Implementation Evidence: Before / After Review Template

Use this template to explain an infrastructure implementation in a way that a technical reviewer, service owner, or manager can verify. Complete it from approved project records. Do not invent baselines, outcomes, savings, or dates.

## 1. Project summary

| Field | Record |
|---|---|
| Project / change reference | [Internal reference; do not publish sensitive IDs] |
| Service / business function | [Service name or sanitized description] |
| Business problem | [What users or operations experienced] |
| Scope | [Sites, systems, devices, users; use approved figures only] |
| Role and responsibility | [What I personally planned, implemented, coordinated, reviewed] |
| Contributors | [Roles, not personal details] |
| Approval / change reference | [Internal reference] |
| Implementation window | [Date/time, if approved for disclosure] |

## 2. Before implementation

Describe the starting point using evidence, not adjectives.

| Area | Baseline | Evidence source | Confidence / limitation |
|---|---|---|---|
| Availability / service health | [Measured baseline] | [Monitoring/ticket] | [Period and caveat] |
| Performance / capacity | [Measured baseline] | [Graph/report] | [Peak/average and units] |
| Incident volume | [Count over defined period] | [Ticket export] | [Classification used] |
| User impact | [Affected users/services] | [Service desk/business owner] | [Scope] |
| Operational effort | [Time or steps, if measured] | [Work log] | [Method] |
| Risk / supportability | [Known issue] | [Audit/assessment] | [Evidence] |

If a baseline was not captured, write **"Not measured before implementation"**. Do not estimate it retrospectively as if it were a measurement.

## 3. Design and implementation

- Requirements and acceptance criteria:
- Options considered and why this approach was selected:
- Dependencies and stakeholders:
- Security and access considerations:
- Capacity and compatibility checks:
- Backup / snapshot / configuration capture:
- Maintenance window and user communication:
- Implementation steps:
- Rollback trigger and rollback procedure:
- Validation steps and responsible approver:

## 4. After implementation

| Area | Result | Evidence source | Validation owner |
|---|---|---|---|
| Service health | [Observed result] | [Monitoring/test] | [Role] |
| Performance / capacity | [Measured result] | [Graph/report] | [Role] |
| Incident volume | [Count over same period] | [Ticket export] | [Role] |
| User impact | [Confirmed status] | [Service owner] | [Role] |
| Operational effort | [Measured result] | [Work log] | [Role] |
| Remaining risks | [Open items] | [Risk/action log] | [Owner] |

Compare equivalent periods and conditions. State any differences in traffic, user count, seasonality, scope, or measurement method.

## 5. Outcome statement

Use a factual format:

> I was responsible for [specific responsibility] as part of [implementation]. The change addressed [documented problem]. Post-implementation validation showed [measured or directly observed result], confirmed through [evidence]. Remaining work includes [open risk/action].

If no quantified evidence exists, describe the verified operational result without adding percentages or financial claims.

## 6. Evidence checklist

- [ ] Approved change record or sanitized summary
- [ ] Before-state monitoring snapshot
- [ ] Design or topology diagram with documentation-only identifiers
- [ ] Implementation and rollback plan
- [ ] Sanitized change diff or command output
- [ ] After-state monitoring snapshot
- [ ] Service-owner validation
- [ ] Incident / problem record and follow-up actions
- [ ] Approval to publish all included evidence

## 7. Public disclosure review

Before publishing, remove credentials, tokens, private keys, internal hostnames, public management IPs, customer/provider names, circuit IDs, serial numbers, MAC addresses, personal information, commercial terms, and screenshots containing sensitive browser or ticket details.

If the organization has not approved the evidence for public release, publish only a generic workflow or fictional lab demo and label it clearly.

---

**A note on this documentation:** The technical work and experience behind these notes are mine. Some wording and the way I have organized the material have had AI assistance, mainly to make the writing clearer and save time. The examples, decisions and work described are not AI-generated. I check what I publish and stand behind it.

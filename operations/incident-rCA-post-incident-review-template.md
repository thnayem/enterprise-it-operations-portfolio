# Incident RCA & Post-Incident Review Template

Use this template for significant, recurring or business-impacting incidents. Adapt it to the organization's incident policy, severity model and approval process.

> This is a reusable template. It does not describe a specific incident or claim an actual root cause or service improvement.

## 1. Incident summary

| Field | Details |
|---|---|
| Incident reference | [Internal ticket/reference] |
| Service / business process | [Service name] |
| Affected site or scope | [Sanitized scope] |
| Severity / priority | [Per approved policy] |
| Start time | [Date/time/time zone] |
| Detection time | [Date/time/time zone] |
| Acknowledgement time | [Date/time/time zone] |
| Restoration time | [Date/time/time zone] |
| Incident owner | [Role/team] |
| Technical resolver(s) | [Role/team/vendor] |

## 2. Business impact

- What service or business process was affected?
- Which users, sites, systems or customers were impacted?
- Was the service unavailable, degraded or operating with a workaround?
- What was the confirmed impact window?
- Which impact statements are confirmed, and which remain estimates?

Do not include personal data, customer details or confidential business information in a public copy.

## 3. Timeline

| Time | Event / observation | Action / decision | Owner | Evidence reference |
|---|---|---|---|---|
| [Time] | [Detection / alert] | [Action] | [Role] | [Ticket/log] |
| [Time] | [Finding] | [Action] | [Role] | [Ticket/log] |
| [Time] | [Service restored] | [Validation] | [Role] | [Test/monitor] |

## 4. Technical investigation

Document the facts collected from relevant layers:

- Physical layer: power, cabling, optics, link state and hardware alarms.
- Network layer: interface counters, VLAN, addressing, routing, tunnel/VPN and path checks.
- Server/platform: resource utilization, service state, storage, logs and dependencies.
- Application: health checks, transactions, error messages and service-owner confirmation.
- External dependency: provider status, vendor findings and third-party service impact.

Record timestamps, source systems and sanitized evidence references. Distinguish observation from interpretation.

## 5. Root cause analysis

**Confirmed root cause:** [State only when supported by evidence]

**Contributing factors:**
- [Factor 1]
- [Factor 2]

**Why was the issue not prevented or detected earlier?**
- [Monitoring/control/process gap, if verified]

**Unresolved questions:**
- [Question, owner and due date]

If the root cause is not confirmed, state "Under investigation" rather than guessing.

## 6. Resolution and recovery

- Immediate containment / workaround: [Details]
- Corrective action taken: [Details]
- Recovery validation: [Checks performed]
- Service-owner or user confirmation: [Reference]
- Remaining risk or limitation: [Details]

## 7. Corrective and preventive action plan

| Action | Type | Owner | Due date | Priority | Status / evidence |
|---|---|---|---|---|---|
| [Action] | Corrective | [Role] | [Date] | [Priority] | [Status] |
| [Action] | Preventive | [Role] | [Date] | [Priority] | [Status] |

Actions should be specific, owned, time-bound and verifiable.

## 8. Service management review

Review relevant measures using the same definitions and time window:

- Time to detect / acknowledge / restore.
- SLA impact, where contractually and operationally applicable.
- Repeat incident frequency.
- Change-related contribution, if any.
- Monitoring coverage and alert quality.
- User communication and escalation effectiveness.

Do not publish or claim MTTR, SLA or availability improvements without a reliable baseline and verified records.

## 9. Lessons learned

- What worked well?
- What delayed diagnosis or recovery?
- Which runbook, monitoring rule or dependency map should change?
- Is additional training, capacity, vendor action or investment required?
- Who will verify that the improvement is effective?

## 10. Review and approval

| Role | Name / team | Review date | Status |
|---|---|---|---|
| Incident owner | [Role/team] | [Date] | [Pending/approved] |
| Service owner | [Role/team] | [Date] | [Pending/approved] |
| IT management | [Role/team] | [Date] | [Pending/approved] |

## Publication and confidentiality checklist

- [ ] Remove real IPs, hostnames, usernames, serial numbers and circuit IDs.
- [ ] Remove credentials, tokens, private keys and security-sensitive configuration.
- [ ] Remove customer, employee and personal information.
- [ ] Remove vendor ticket contents, contracts and internal screenshots unless approved.
- [ ] Obtain authorization before publishing any incident-derived material.
- [ ] Label hypothetical examples and templates clearly.

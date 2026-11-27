# Team Performance & Resource Allocation

A fair, practical framework for coordinating an IT infrastructure team. Use it to make workload visible, identify training needs, plan coverage, and remove blockers. It is not a substitute for HR policy or a claim about any particular team size.

## 1. Principles

- Evaluate agreed responsibilities and outcomes, not personality or visibility.
- Consider incident complexity, workload, shift coverage, dependencies, and available tools.
- Give feedback privately, respectfully, and with specific examples.
- Recognize collaboration, documentation, mentoring, and safe escalation, not only ticket count.
- Never use raw ticket volume alone as a measure of an engineer's value.
- Agree development actions with the employee and review progress fairly.

## 2. Weekly workload board

| Work item | Priority | Accountable owner | Support / reviewer | Effort estimate | Due date | Status / blocker |
|---|---|---|---|---:|---|---|
| WAN incident follow-up (example) | High | Network role | Team lead | 2 h | [Date] | Waiting for provider |
| Restore test (example) | Medium | Systems role | Application owner | 4 h | [Date] | Scheduled |
| Access review (example) | Medium | Systems role | Security role | 3 h | [Date] | In progress |
| Asset reconciliation (example) | Low | Support role | Procurement | 5 h | [Date] | Planned |

Example tasks are illustrative, not actual employee assignments. Keep named employee data and sensitive service references in approved internal systems.

## 3. Capacity and resource allocation

Estimate available capacity before assigning planned work.

```text
Net available hours =
  scheduled working hours
  - leave / training / meetings
  - on-call or shift handover allowance
  - planned operational support reserve
```

A simple allocation model for planning (not a universal target):

| Work category | Planning consideration |
|---|---|
| Incident and service support | Reserve capacity based on historical demand and criticality |
| Planned changes / projects | Schedule only against confirmed available capacity |
| Preventive maintenance | Protect time for patching, lifecycle, capacity and restore checks |
| Documentation / knowledge transfer | Include time in the task estimate |
| Training / mentoring | Plan as real work, not after-hours expectation |
| Contingency | Keep a buffer for unexpected priority incidents |

Review allocation weekly. If incidents consume the planned project capacity, reforecast and communicate the impact rather than quietly overloading the team.

## 4. Skills and coverage matrix

Use role-level skills, not public employee names.

| Capability | Primary coverage | Backup coverage | Risk / development action |
|---|---|---|---|
| Routing and switching | [Role] | [Role] | [Cross-training] |
| Firewall / VPN | [Role] | [Role] | [Vendor/lab training] |
| Windows / identity | [Role] | [Role] | [Runbook review] |
| Linux / virtualization | [Role] | [Role] | [Restore exercise] |
| Backup / DR | [Role] | [Role] | [Test recovery] |
| Monitoring / service desk | [Role] | [Role] | [Alert tuning] |

Avoid a single point of failure: critical services should have documented procedures and at least one trained backup where practical.

## 5. Balanced performance discussion

Use a consistent review period and agreed role expectations.

| Dimension | Evidence to discuss | Coaching question |
|---|---|---|
| Service ownership | Follow-through, user validation, handover | What helped or blocked closure? |
| Technical quality | Accuracy, safe changes, troubleshooting evidence | What could make diagnosis more repeatable? |
| Reliability | Commitments, escalation, documentation | Were priorities and dependencies clear? |
| Collaboration | Knowledge sharing, respectful communication | Where would pairing help? |
| Improvement | Runbook, automation, recurring-issue prevention | What should we improve next cycle? |
| Learning | Training, lab practice, new responsibility | What support or time is needed? |

### Suggested conversation structure

1. Ask the person how the period went.
2. Review agreed goals and evidence together.
3. Discuss strengths with specific examples.
4. Identify one or two improvement areas without blame.
5. Agree a realistic development action and required support.
6. Confirm next review date and record only necessary information.

## 6. Delegation and review

For a risky change, make the expected outcome and guardrails clear:
- Scope and business impact
- Required approval and maintenance window
- Pre-checks and backup
- Implementation owner and peer reviewer
- Rollback trigger and decision authority
- Validation and communication
- Documentation and handover

Delegation means giving ownership with appropriate support, not transferring risk without authority.

## 7. Escalation and workload conflict

Escalate when there is a service outage, security/data-loss risk, unsafe workload, missed dependency, supplier delay, or a decision outside the engineer's authority. Bring facts, business impact, options, and the decision needed.

## 8. Monthly team review summary

- Work completed and service outcomes:
- Major incidents and learning:
- Planned work deferred and why:
- Coverage gaps / single points of failure:
- Training and mentoring actions:
- Workload or wellbeing concerns requiring support:
- Decisions required from management:
- Owners and review dates:

Keep employee performance records confidential and follow local HR and data-protection policies.

---

**A note on this documentation:** The technical work and experience behind these notes are mine. Some wording and the way I have organized the material have had AI assistance, mainly to make the writing clearer and save time. The examples, decisions and work described are not AI-generated. I check what I publish and stand behind it.

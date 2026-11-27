# IT Budget & Cost Planning Framework

A practical planning template for an IT infrastructure budget. It helps connect technical needs to business continuity, risk, lifecycle, and total cost of ownership (TCO). It does not state an actual company budget or purchasing authority.

## 1. Start with business need

For every proposed cost, document:
- Business service or risk being addressed
- Current condition and evidence
- Options considered (repair, renew, upgrade, replace, managed service)
- Consequence of not funding the request
- Required timing and dependencies
- Technical owner and business sponsor
- Procurement and approval route

## 2. Budget categories

| Category | Typical items | Planning basis |
|---|---|---|
| Hardware lifecycle | Servers, switches, routers, storage, endpoints | Age, warranty, capacity, failure risk |
| Software and licensing | OS, virtualization, security, backup, business apps | User/device/core counts, renewal dates |
| Connectivity | Internet, NTTN, MPLS/leased lines, dark fiber, cross-connects | Bandwidth, redundancy, SLA, contract |
| Data centre / DR | Rack, colocation, power, cooling, backup site | Capacity, resilience, recovery objectives |
| Power continuity | UPS batteries, generator maintenance, fuel, PDU | Load, runtime, battery health, service |
| Security | Firewall support, endpoint security, audits, remediation | Risk assessment and control coverage |
| Support and maintenance | Warranty, AMC, vendor support, spare parts | Criticality and response requirements |
| Consumables | Toner, cables, SFPs, accessories | Usage, lead time, reorder point |
| Projects | Migration, upgrades, implementation services | Approved scope, milestones, contingency |
| Training | Technical training, knowledge transfer | Skills gap and operational coverage |

## 3. Annual budget worksheet

| Item | CAPEX / OPEX | Qty | Unit estimate | Frequency | Annual estimate | Priority | Justification |
|---|---|---:|---:|---|---:|---|---|
| Example: access switch replacement | CAPEX | 2 |  [currency] | One-time | [calculation] | High | End-of-support / capacity |
| Example: WAN service | OPEX | 1 | [currency] | Monthly | [monthly × 12] | Critical | Site connectivity |
| Example: backup support renewal | OPEX | 1 | [currency] | Annual | [annual fee] | High | Recoverability |
| Example: UPS battery set | CAPEX/OPEX per policy | 1 | [currency] | Lifecycle | [estimate] | High | Runtime / battery condition |

Use supplier quotations and finance-approved assumptions for real figures. Do not publish quotations, negotiated rates, account details, or contract terms in a public repository.

## 4. Total cost of ownership

Consider more than purchase price:

```text
TCO over review period =
  acquisition
  + licensing/subscription
  + implementation/migration
  + support and maintenance
  + connectivity / power / cooling
  + training and operations
  + expected replacement / disposal cost
```

Compare options over the same review period and scope. Include currency, tax treatment, inflation or exchange-rate assumptions, and residual value where relevant.

## 5. Procurement comparison

| Evaluation factor | Weight | Vendor A | Vendor B | Vendor C |
|---|---:|---:|---:|---:|
| Technical compliance | [ ] | [ ] | [ ] | [ ] |
| Security / supportability | [ ] | [ ] | [ ] | [ ] |
| Warranty and SLA | [ ] | [ ] | [ ] | [ ] |
| Delivery and implementation | [ ] | [ ] | [ ] | [ ] |
| TCO | [ ] | [ ] | [ ] | [ ] |
| References / service quality | [ ] | [ ] | [ ] | [ ] |

Define scoring rules before evaluating suppliers. Technical compliance and mandatory security requirements should be pass/fail gates where appropriate, not traded away for a lower price.

## 6. Forecasting and cost control

- Maintain a renewal calendar for licenses, domains, certificates, support and connectivity.
- Track committed spend, actual spend, forecast-to-complete, and variance.
- Reconcile invoices against contract, purchase order, delivery, and service acceptance.
- Review unused licenses, idle capacity, duplicate services, and recurring incidents.
- Track warranty expiry and end-of-support before emergency replacement is required.
- Maintain a controlled spare-parts strategy for critical equipment.
- Review power, cooling, and bandwidth trends to avoid capacity surprises.

## 7. Business case template

**Request:** [Item / project]

**Problem and evidence:** [Current condition, monitoring, incident, lifecycle or audit finding]

**Options:** [Do nothing, repair, upgrade, replace, outsource]

**Recommended option:** [Choice and reason]

**Estimated cost:** [CAPEX, OPEX, one-time and recurring; source/date of estimate]

**Benefits:** [Risk reduction, service continuity, supportability, capacity, productivity; quantify only when evidence supports it]

**Risks and dependencies:** [Migration, compatibility, vendor, staffing, downtime]

**Implementation plan:** [Owner, milestones, change window, rollback, validation]

**Decision required:** [Approver and deadline]

## 8. Governance

Follow the organization's delegated financial authority, procurement policy, competitive quotation rules, asset capitalization policy, tax treatment, security review, and segregation-of-duties requirements. Technical recommendation, commercial evaluation, approval, receipt, and payment should have appropriate independent checks.

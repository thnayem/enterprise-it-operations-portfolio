# Data Centre & Disaster Recovery Planning

Data centre and disaster recovery planning is about keeping critical services recoverable when equipment, connectivity, power, facilities or a wider site becomes unavailable. A recovery plan must be based on business impact and tested dependencies, not only on the existence of backups.

## 1. Data centre operations

Maintain an approved record of:

- Rack layout, equipment ownership and support contacts.
- Power feeds, UPS capacity, battery condition and generator arrangements.
- Cooling, temperature and environmental alerts.
- Network paths, carrier circuits, firewalls and out-of-band access.
- Compute, hypervisor, storage and backup dependencies.
- Physical access control, visitor records and maintenance windows.
- Firmware, warranty, support contracts and end-of-life dates.

Keep detailed rack diagrams, real addresses, access procedures and security-sensitive facility information in controlled internal documentation.

## 2. Business impact and recovery objectives

Agree recovery priorities with business and service owners.

| Term | Meaning |
|---|---|
| Business impact analysis (BIA) | Identifies business processes, dependencies and impact of service disruption |
| RTO | Target time to restore a service after disruption |
| RPO | Maximum acceptable period of data loss measured in time |
| MTD | Maximum tolerable time a business process can remain disrupted |

RTO and RPO are service-specific targets. They should be approved by the business and validated against technical capability, cost and recovery-test results.

## 3. Recovery strategy

Choose protection based on service criticality and dependencies:

- **Backup and restore:** recover systems and data from protected backups.
- **Warm standby:** maintain a prepared environment that requires activation and synchronization.
- **Hot standby / replication:** maintain a near-ready secondary environment where justified by recovery targets.
- **Configuration recovery:** preserve approved network, firewall, hypervisor and system configurations.
- **Manual continuity:** document temporary business processes when technology recovery takes time.

Replication is not a replacement for backup. Corruption, accidental deletion or malicious changes can also replicate.

## 4. Recovery dependency map

For each critical service, identify the order and dependencies required to restore it. Common dependencies include power, WAN, DNS, identity services, virtualization, storage, firewall rules, certificates, databases and application services.

A recovery sequence should be agreed and tested. Do not assume that restoring a virtual machine alone makes the business service available.

## 5. Backup and recovery controls

- Define backup scope, frequency, retention and ownership.
- Protect backup administration with separate access controls and MFA where supported.
- Keep an appropriately isolated or immutable recovery copy where feasible.
- Monitor backup failures and capacity.
- Record encryption and key-recovery responsibilities.
- Test file-level, application-level and full-service restoration.
- Record restore duration, data consistency and issues found.

## 6. Exercise and evidence

Run tabletop reviews and technical recovery tests at an agreed frequency. Record:

| Field | Record |
|---|---|
| Exercise date and scope | |
| Scenario | |
| Services and owners | |
| Approved RTO / RPO | |
| Actual recovery time | |
| Actual data recovery point | |
| Dependencies or blockers | |
| Test evidence location | |
| Corrective actions and owner | |
| Retest date | |

A plan is not proven until recovery has been exercised and the result reviewed. Do not publish internal recovery credentials, live topology, backup locations or sensitive facility details.

---

**A note on this documentation:** The technical work and experience behind these notes are mine. Some wording and the way I have organized the material have had AI assistance, mainly to make the writing clearer and save time. The examples, decisions and work described are not AI-generated. I check what I publish and stand behind it.

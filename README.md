# Enterprise IT Operations Portfolio

**Enterprise IT Infrastructure | Operations | Service Coordination**

This repository collects practical references for the systems and services that keep an organization's IT environment running: communication systems, physical security, monitoring, business applications, databases, endpoint support and operational planning.

The focus is not only on the technology. It is also on service ownership, clear handovers, incident coordination, documentation, vendor follow-up and keeping work understandable for the next person.

## Important context: practical experience vs. published material

The real-world, hands-on production experience behind this portfolio is broader than what is documented here. This repository is only a selected glimpse of the systems, support activities, operational challenges and lessons I have encountered. It is not a complete record of my work, and there is more experience I have not yet added.

I do not publish original employer/customer production configurations, internal records, credentials, personal data, raw backups or confidential documents. The material here is made up of study and learning notes, independently prepared examples, lab/demo exercises, troubleshooting scenarios, implementation practice, reusable templates and selected lessons from practical operations. Where I describe production involvement, I keep it at a safe, high level. Templates and illustrative workflows are not claims that a particular organization used them or achieved a specific result.

I can make mistakes. I believe the right response is not to hide them or shift blame, but to acknowledge the issue, take responsibility, communicate with the people affected, work toward a safe correction and learn from what happened. In IT operations, accountability, teamwork and clear communication matter just as much as technical knowledge.


## Five-minute overview

- **Technical operations:** IP telephony, CCTV/NVR, fiber connectivity, monitoring, mail services, ERP support, database references and endpoint support.
- **Infrastructure planning:** Data centre and DR, power continuity, UPS, cooling, rack planning and asset lifecycle.
- **Service management:** Incident handling, prioritization, escalation, vendor/SLA follow-up, procurement evaluation and operational reporting.
- **People and teamwork:** Task ownership, knowledge sharing, practical handovers, workload coordination and respectful communication.

## Technical coverage

| Area | Scope |
|---|---|
| IP Telephony | Fanvil GRP2601, Grandstream UCM6301, extensions, SIP trunks, provisioning and call routing |
| CCTV & NVR | IP camera operations, NVR/VMS architecture, recording, storage and retention planning |
| Fiber Connectivity | Optical links, SFPs, media converters and fiber troubleshooting |
| Monitoring | LibreNMS and Cacti concepts, SNMP, device onboarding, graphs and alerts |
| Email Services | Mail administration, mailbox setup, mail flow, DNS records and Outlook |
| End-user & Hardware | Printer/scanner/NAS, PC/laptop upgrades, Windows installation and diagnostics |
| ERP Support | User support, application triage, developer coordination and change handling |
| DBMS & SQL | Relational database fundamentals, read-only examples, backup/restore and performance basics |
| Attendance Systems | Face/fingerprint terminals, data flow, synchronization and troubleshooting |
| Data Centre & DR | Facility operations, backup strategy, RPO/RTO planning and recovery dependencies |
| Power & Cooling | UPS, generator, load, energy monitoring, cooling, airflow and rack planning |
| Vendor & Asset Operations | Supplier evaluation, SLA, warranty, inventory, procurement and lifecycle tracking |

## Repository map

- [IP Telephony](telephony/README.md)
- [CCTV, NVR & Storage](cctv-nvr/README.md)
- [Fiber Connectivity](fiber-connectivity/README.md)
- [LibreNMS & Cacti Monitoring](monitoring/README.md)
- [Mail Services](mail-services/README.md)
- [Endpoint, Printer, NAS & Hardware Support](endpoint-support/README.md)
- [ERP Application Support](erp-support/README.md)
- [DBMS & SQL References](database-sql/README.md)
- [Face & Fingerprint Attendance](attendance-systems/README.md)
- [Operations Runbooks](operations/README.md)
- [IT Management & Team Operations](management/README.md)
- [Leadership & Operations Playbook](management/leadership-and-operations-playbook.md)

## How I approach operations

When a service is reported as unavailable, I first establish who and what is affected. I record the timeline, identify an owner, check available evidence and coordinate the right technical or vendor support. I try to keep updates clear: what is confirmed, what is still being checked, what happens next and when people will hear from us again.

For planned work, I look at dependencies, impact, approvals, maintenance timing, rollback and acceptance checks. After implementation, the service should be verified with monitoring and, where appropriate, the people who use it.

Good documentation should help someone else take over without having to guess. A runbook needs scope, prerequisites, checks, expected results, recovery steps, escalation and a review date.

## Management and team coordination

The management references cover capacity planning, service reviews, incident ownership, workload prioritization, vendor/SLA follow-up, asset lifecycle, procurement and team coordination.

The playbook uses sample workflows and fictional task entries to explain a practical approach. It does not claim a particular team size, budget authority, reporting line, KPI result or project outcome. Those details should only be added when they can be supported by real evidence and are appropriate to disclose.

## Documentation and evidence labels

- **Production experience:** A description of work I have been involved in, with confidential details removed.
- **Sanitized reference:** A reduced or anonymized procedure/configuration reference.
- **Lab/demo:** An independently authored example for learning or demonstrating a workflow, not proof of production deployment.
- **Template:** A reusable form or checklist that must be adapted to the organization's process.

New and updated pages follow [DOCUMENTATION-GUIDE.md](./DOCUMENTATION-GUIDE.md), including purpose, scope, architecture or workflow, configuration/procedure, troubleshooting, verification, rollback and lessons learned.

## Related portfolios

- [Network Engineering Portfolio](https://github.com/thnayem/network-engineering-portfolio)
- [System & Server Virtualization Portfolio](https://github.com/thnayem/system-server-virtualization-portfolio)
- [GitHub Profile](https://github.com/thnayem)

## Security and practical limits

Use sanitized examples and documentation-only address ranges. Treat firmware, interface labels, licensing and feature availability as model/version dependent. Never publish credentials, public IPs, internal hostnames, camera addresses, serial numbers, personal attendance data, customer records or employer-confidential documents.

Maintained by [Md. Tanvir Hossain](https://github.com/thnayem) · [LinkedIn](https://www.linkedin.com/in/thnayem/)

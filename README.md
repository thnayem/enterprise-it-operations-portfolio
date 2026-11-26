# Enterprise IT Operations Portfolio

Practical technical documentation and implementation references for enterprise IT operations, communication systems, physical security infrastructure, monitoring, business applications, databases, and workforce attendance systems.

This repository is part of my broader IT infrastructure portfolio. It presents technology coverage, operational workflows, configuration considerations, and reusable planning references. It does not publish customer-specific configurations, credentials, private network details, or confidential deployment records.

## Technical Coverage

| Area | Scope |
|---|---|
| IP Telephony | Fanvil GRP2601 SIP phone, Grandstream UCM6301 IP PBX, extensions, SIP trunks, provisioning, call routing |
| CCTV & NVR | Large-scale IP camera operations, NVR/VMS architecture, recording, storage and retention planning |
| Fiber Connectivity | Optical links for CCTV and remote sites, SFPs, media converters, fiber troubleshooting |
| Monitoring | LibreNMS and Cacti deployment concepts, SNMP, device onboarding, graphs, alerts |
| Email Services | Mail server administration, mailbox/email ID creation, mail flow, DNS records and Outlook setup |
| End-User & Hardware Support | Printer/scanner/NAS setup, PC/laptop RAM and storage upgrades, Windows installation, diagnostics, troubleshooting and repair |
| ERP Support | User support, application issue triage, developer coordination, change and incident handling |
| DBMS & SQL | Relational database fundamentals, read-only query examples, backup/restore and performance basics |
| Attendance Systems | Face recognition and fingerprint terminals, attendance data flow, synchronization and troubleshooting |
| IT Management & Team Operations | Capacity planning, service reviews, work prioritization, escalation, stakeholder communication and operational reporting |
| Data Centre & Disaster Recovery | Facility operations, backup strategy, RPO/RTO planning, recovery dependencies and DR exercises |
| Vendor & SLA Management | Supplier evaluation, contract and warranty tracking, service reviews and escalation |
| Asset & Inventory Management | Asset lifecycle, stock control, audits, software entitlements and lifecycle planning |
| IT Procurement | Requirements, technical specifications, quotation evaluation, TCO and goods acceptance |
| Toner & Consumables | Printer supply compatibility, usage tracking, reorder levels and stock reconciliation |

## Repository Structure

- [IP Telephony](telephony/README.md)
- [CCTV, NVR & Storage](cctv-nvr/README.md)
- [Fiber Connectivity for CCTV](fiber-connectivity/README.md)
- [LibreNMS & Cacti Monitoring](monitoring/README.md)
- [Mail Server, Mailbox Creation & Outlook Setup](mail-services/README.md)
- [Endpoint, Printer, NAS & Hardware Support](endpoint-support/README.md)
- [ERP Application Support](erp-support/README.md)
- [DBMS & SQL References](database-sql/README.md)
- [Face & Fingerprint Attendance](attendance-systems/README.md)
- [Operations Runbooks](operations/README.md)
- [IT Management & Team Operations](management/README.md) - capacity planning, data centre and DR, vendor/SLA, asset inventory, procurement, toner/consumables and team leadership

## Management & Operational Practices

The management references cover the planning and coordination work behind day-to-day infrastructure operations: forecasting capacity, maintaining service continuity, tracking assets and suppliers, evaluating purchases, controlling consumables and keeping team work visible. They are practical templates that should be adapted to the organization's policies and actual authority structure.

## Related Technical Portfolios

- [Network Engineering Portfolio](https://github.com/thnayem/network-engineering-portfolio) — multi-vendor routing, switching, WAN and network configuration references.
- [System & Server Virtualization Portfolio](https://github.com/thnayem/system-server-virtualization) — Windows Server, Ubuntu, VMware, storage, backup and server operations.
- [GitHub Profile](https://github.com/thnayem)

## Documentation Principles

- Use sanitized examples and documentation-only address ranges where examples require IPs.
- Treat vendor firmware, interface labels and feature availability as model/version dependent.
- Separate general reference designs from verified implementation evidence.
- Do not assume a single NVR can handle hundreds of cameras; large deployments require validated multi-server/VMS architecture.
- Calculate storage from actual camera bitrate, codec, recording schedule, retention and redundancy requirements.
- Never publish production credentials, public IPs, internal hostnames, camera addresses, serial numbers or personal attendance data.

## About

This portfolio is intended to demonstrate practical understanding of enterprise IT operations and technical coordination across infrastructure and business systems. Specific production environments are not identified. Example procedures are references and must be validated against the actual hardware, firmware, licensing and organizational change process before use.

# Enterprise IT Operations Runbooks

## Purpose

Reusable operational checklists for service continuity, incident response, change management and asset documentation across telephony, CCTV, monitoring, ERP, databases and attendance systems.

## Incident Record

Capture:
- Incident ID and start/end time.
- Service and site/location reference (use non-sensitive identifiers in shared documents).
- Impact, scope and affected users/devices.
- Symptoms and evidence.
- Actions taken and responsible owner.
- Escalation, workaround and resolution.
- User confirmation and follow-up actions.

For significant or recurring incidents, use the [Incident RCA & Post-Incident Review Template](incident-rca-post-incident-review-template.md) to document the timeline, evidence, confirmed root cause, corrective actions and lessons learned. Do not guess a root cause when evidence is incomplete.

## Change Record

Before a change:
- Define objective, scope and affected services.
- Identify dependencies and stakeholders.
- Assess risk and user impact.
- Obtain required approval.
- Schedule maintenance and communication.
- Prepare backup, rollback and validation steps.

After a change:
- Validate service functionality and monitoring.
- Confirm with service owner or users.
- Record actual outcome and deviations.
- Close or raise follow-up actions.

## Asset Register Fields

| Field | Purpose |
|---|---|
| Asset ID | Unique inventory reference |
| Category/model | Device or service type |
| Location | Approved site/room reference |
| Owner | Responsible team |
| Management address | Store only in controlled internal inventory |
| Firmware/version | Lifecycle and compatibility |
| Warranty/support | Renewal and escalation |
| Status | Active, spare, repair or retired |

Do not publish actual management addresses, serial numbers, credentials, phone numbers, camera inventory or sensitive site details in this public portfolio.

## Related Portfolios

- [Network Engineering](https://github.com/thnayem/network-engineering-portfolio)
- [System & Server Virtualization](https://github.com/thnayem/system-server-virtualization-portfolio)

# Network Monitoring: LibreNMS & Cacti

## Scope

This section covers monitoring platform setup concepts, SNMP onboarding, polling, graphing, alerting and routine operations using LibreNMS and Cacti.

## Platform Roles

- **LibreNMS:** network device discovery, health and interface monitoring, alerting and inventory visibility.
- **Cacti:** SNMP-based graphing and historical performance trends using data collection templates.

The two platforms can coexist where there is a clear operational reason, but duplicate monitoring should be avoided unless it serves a defined reporting or resilience need.

## Deployment Preparation

- Select a supported operating system and database/runtime versions from current project documentation.
- Allocate CPU, RAM, storage and backup capacity based on device count and polling frequency.
- Configure DNS, NTP, firewall rules and restricted administrator access.
- Use a dedicated monitoring account and least-privilege SNMPv3 where supported.
- Document polling intervals, retention, alert ownership and escalation path.
- Back up application configuration, database and required device definitions.

## SNMP Device Onboarding

1. Enable SNMP on the target device.
2. Prefer SNMPv3 with authentication and privacy where supported.
3. Restrict SNMP access to monitoring server addresses.
4. Confirm reachability and UDP/161 filtering.
5. Add the device to the monitoring platform.
6. Validate system identity, interfaces, sensors and polling status.
7. Configure meaningful alert thresholds and test notification delivery.

## Useful Monitoring Areas

- Interface utilization, errors, discards and operational status.
- CPU, memory, temperature, power and fan sensors where exposed.
- Device uptime, availability and polling health.
- WAN utilization and packet loss/latency using suitable probes.
- Storage capacity and service availability for monitoring servers.
- Alert trends and recurring incidents.

## Operational Practices

- Keep device naming and location labels consistent but avoid exposing private production details in public examples.
- Tune alerts to reduce noise and identify actionable thresholds.
- Review devices that repeatedly become unavailable or stop polling.
- Monitor the monitoring platform itself, including database and disk growth.
- Test database/configuration restore procedures.
- Upgrade only after reviewing supported versions, dependencies and rollback options.

## Example Alert Policy

| Condition | Suggested response |
|---|---|
| Critical uplink down | Notify on-call team immediately |
| Interface errors rising | Investigate optics, cabling, congestion and hardware |
| High CPU sustained | Correlate with traffic, control-plane and scheduled tasks |
| Storage threshold reached | Review retention, growth and capacity plan |
| Poller/database backlog | Check poller capacity, database health and job schedule |

## References

- [LibreNMS Documentation](https://docs.librenms.org/)
- [Cacti Documentation](https://docs.cacti.net/)

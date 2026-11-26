# IP Telephony: Fanvil GRP2601 & Grandstream UCM6301

## Scope

This section documents SIP endpoint and IP-PBX administration concepts using:

- **Fanvil GRP2601** — SIP desk phone endpoint.
- **Grandstream UCM6301** — IP-PBX platform for extensions and call handling.

The examples are generic references. Menu names, firmware options and supported features can vary by device firmware and deployment configuration.

## Typical Implementation Workflow

1. Confirm LAN/VLAN, DHCP, DNS, gateway, NTP and PoE requirements.
2. Prepare an extension plan and define user/device mapping.
3. Configure the PBX network settings and administrator access securely.
4. Create extensions with unique authentication credentials.
5. Configure SIP trunk parameters with the service provider.
6. Configure inbound and outbound routes, caller ID and emergency calling policy.
7. Configure ring groups, IVR, voicemail and business-hour schedules as required.
8. Provision the Fanvil phone with the assigned SIP account.
9. Test registration, internal calls, inbound/outbound calls, audio in both directions and failover behavior.
10. Document the change, test results and rollback steps.

## Example Extension Plan

| Function | Example extension |
|---|---:|
| Reception | 100 |
| Accounts | 110 |
| IT Helpdesk | 120 |
| Meeting room | 130 |

These are illustrative values only, not production extension numbers.

## Fanvil GRP2601 Endpoint Checklist

- Confirm model variant and firmware compatibility.
- Assign the intended voice VLAN or verify DHCP-based provisioning.
- Set time zone, NTP and regional settings.
- Configure SIP server/PBX address and extension authentication.
- Apply a strong, unique SIP secret; do not reuse administrator credentials.
- Validate registration status and codec negotiation.
- Test handset, speakerphone, headset, DTMF and hold/transfer behavior.
- Disable unused services and restrict management access to trusted networks.

## Grandstream UCM6301 Checklist

- Update firmware using the approved maintenance process.
- Change default credentials and restrict management access.
- Configure network settings, time and DNS.
- Create extensions and appropriate user permissions.
- Configure SIP trunk registration or peer details as supplied by the carrier.
- Apply inbound/outbound routes and call permissions.
- Configure IVR, ring groups, voicemail and office-hour schedules.
- Review call logs and system status; protect exported backups.

## Troubleshooting Matrix

| Symptom | Checks |
|---|---|
| Phone not registered | VLAN/DHCP, reachability, SIP server, extension credentials, firewall/NAT |
| One-way or no audio | RTP range, NAT, SIP ALG behavior, routing and codec compatibility |
| Outbound calls fail | Trunk registration, outbound route, dial pattern, caller ID and provider restrictions |
| Inbound calls fail | DID mapping, inbound route, provider routing and destination extension |
| Intermittent call quality | WAN loss/latency/jitter, QoS, congestion, duplex and packet drops |

## Security & Change Notes

- Use unique extension secrets and restrict PBX administration.
- Avoid exposing SIP and management interfaces directly to the public internet.
- Apply vendor-supported updates after compatibility and rollback review.
- Keep configuration backups protected and access-controlled.
- Redact phone numbers, SIP credentials, provider account data and public addresses from shared examples.

## Related References

- [Network Engineering Portfolio](https://github.com/thnayem/network-engineering-portfolio)
- [System & Server Virtualization Portfolio](https://github.com/thnayem/system-server-virtualization)

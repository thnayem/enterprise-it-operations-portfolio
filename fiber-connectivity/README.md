# Fiber Connectivity for CCTV & Remote Infrastructure

## Scope

Optical fiber is commonly used to connect CCTV access/distribution points across buildings, floors, compounds and remote locations where distance, electrical isolation or bandwidth requirements make copper unsuitable.

## Typical Link Components

- Single-mode or multimode optical fiber, selected for distance and optics compatibility.
- SFP/SFP+ transceivers with matching wavelength, speed and optical budget.
- Fiber patch panels, ODFs, pigtails and patch cords.
- Managed switches with compatible optical interfaces.
- Media converters only where a switch fiber port is not available or operationally justified.
- UPS-backed network equipment at remote cabinets.

## Design Checklist

1. Identify endpoints, route, distance and fiber type.
2. Confirm available strands, connector type and patch-panel mapping.
3. Match both-end transceiver speed, wavelength, fiber type and reach.
4. Verify optical transmit/receive levels against transceiver specifications.
5. Define CCTV VLANs, management access and uplink redundancy.
6. Calculate PoE requirements at camera access switches; fiber does not deliver PoE.
7. Label both ends and maintain an as-built fiber schedule.
8. Test link, throughput, packet loss and failover where applicable.

## Troubleshooting

| Symptom | Checks |
|---|---|
| No link | SFP seating, compatibility, fiber polarity, patching and port status |
| Link flaps | Dirty connectors, damaged patch cord, marginal optical levels, temperature |
| CRC/input errors | Optics, fiber condition, speed/duplex and interface counters |
| Cameras unreachable | VLAN tagging, routing, ACLs, switch power and camera status |
| Intermittent video | Uplink congestion, packet loss, multicast/unicast behavior and recorder load |

## Safety

Never look into a fiber connector or optical transceiver. Inspect and clean connectors using approved tools and procedures. Follow site safety rules when working in cabinets, risers and outdoor routes.

## Related References

- [Network Engineering Portfolio](https://github.com/thnayem/network-engineering-portfolio)
- [System & Server Virtualization Portfolio](https://github.com/thnayem/system-server-virtualization)

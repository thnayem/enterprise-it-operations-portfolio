# IT Infrastructure Capacity Planning

Capacity planning helps IT teams identify resource constraints before they affect users or business services. It should use measured demand and growth trends rather than assumptions or a single utilization snapshot.

## Scope

Review capacity across:

- **Network:** internet bandwidth, WAN links, uplinks, switching capacity, Wi-Fi density, VPN and firewall throughput.
- **Compute:** physical hosts, CPU, memory, virtualization clusters and application workloads.
- **Storage:** usable capacity, IOPS, latency, growth, retention and backup windows.
- **Power and cooling:** UPS load, runtime, circuit capacity, rack power and cooling headroom.
- **CCTV:** camera count, bitrate, codec, recording schedule, retention, VMS/NVR limits and storage redundancy.
- **End-user services:** endpoint lifecycle, printer demand, licenses, telephony ports and support workload.

## Planning cycle

1. Establish a baseline from monitoring, system reports, invoices and inventory.
2. Record peak and average utilization over a representative period.
3. Identify business growth, new sites, new applications and retention changes.
4. Forecast demand for an agreed planning horizon.
5. Define required headroom and service limits with the service owner.
6. Compare options: optimize, reconfigure, upgrade, expand or replace.
7. Estimate total cost, implementation effort, risks and dependencies.
8. Submit a recommendation for review and approval.
9. Track the approved action and verify the result after implementation.

## Useful measures

| Area | Measures to review |
|---|---|
| WAN / Internet | 95th percentile and peak throughput, utilization, packet loss, latency, jitter, monthly transfer |
| Switching | Port utilization, uplink saturation, errors, PoE budget, available ports |
| Compute | CPU ready/usage, memory pressure, host capacity, VM density |
| Storage | Used and usable capacity, growth rate, IOPS, latency, rebuild and backup windows |
| CCTV | Aggregate bitrate, concurrent streams, retention days, usable storage, recording health |
| UPS | Current load, runtime at measured load, battery age, redundancy and maintenance status |
| Printing | Pages per month, cost per page, toner yield, device utilization and service incidents |

## Forecasting worksheet

| Field | Example / entry |
|---|---|
| Service or platform | |
| Current measured demand | |
| Measurement period | |
| Average and peak utilization | |
| Monthly or annual growth assumption | |
| Forecast horizon | |
| Required headroom | |
| Estimated future demand | |
| Current supported capacity | |
| Gap and target capacity | |
| Options and estimated cost | |
| Risk if deferred | |
| Recommendation / approval | |

A simple forecast can be expressed as:

`Forecast demand = Current demand × (1 + growth rate) ^ number of periods`

Use a growth rate supported by historical measurements or an agreed business forecast. Do not treat this simple formula as a substitute for workload testing or vendor sizing.

## Decision principles

- Plan against usable capacity, not raw advertised capacity.
- Include redundancy, maintenance and failure scenarios in the calculation.
- Check licensing, support lifecycle, compatibility and lead times before recommending hardware.
- Consider optimization and workload cleanup before purchasing additional capacity.
- Document assumptions and revisit them when demand changes.
- Define an alert threshold and an action owner for each critical resource.

## Review output

A useful capacity review ends with a short decision paper: current state, trend, forecast, service risk, options, estimated cost, recommendation, approval owner and target date. Record what was approved and compare actual utilization after delivery.

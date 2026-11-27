# IT Infrastructure Capacity Planning

Capacity planning helps IT teams identify resource constraints before they affect users or business services. It should use measured demand and growth trends rather than assumptions or a single utilization snapshot.

## Scope

Review capacity across:

- **Network:** internet bandwidth, WAN links, uplinks, switching capacity, Wi-Fi density, VPN and firewall throughput.
- **Compute:** physical hosts, CPU, memory, virtualization clusters and application workloads.
- **Storage:** usable capacity, IOPS, latency, growth, retention and backup windows.
- **Power and energy:** measured kW/kWh consumption, UPS loading and autonomy, generator capacity, solar PV contribution, circuit loading and power quality.
- **Cooling and physical infrastructure:** IT heat load, cooling capacity, airflow, temperature/humidity, rack U-space, PDU loading and physical growth headroom.
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
| UPS / backup power | Load in W/VA, runtime at measured load, battery age, generator transfer, redundancy and maintenance status |
| Energy / solar | kW demand, kWh consumption, load profile, PV yield, battery usable energy and system losses |
| Cooling | IT heat load, supply/return temperature, humidity, airflow, cooling capacity and redundancy |
| Rack / facility | Rack U-space, depth, weight rating, PDU capacity, power feeds and airflow clearance |
| Printing | Pages per month, cost per page, toner yield, device utilization and service incidents |

## Power, cooling and facility planning

Include measured electrical demand, UPS and battery runtime, generator capacity, solar energy contribution, cooling headroom and rack growth in the same capacity review. Evaluate critical and non-critical loads separately, and validate the power path and environmental design with qualified specialists.

For detailed assessment steps, use the [Power, UPS, Solar, Cooling & Rack Planning guide](power-cooling-rack-planning.md).

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

---

**A note on this documentation:** The technical work and experience behind these notes are mine. Some wording and the way I have organized the material have had AI assistance, mainly to make the writing clearer and save time. The examples, decisions and work described are not AI-generated. I check what I publish and stand behind it.

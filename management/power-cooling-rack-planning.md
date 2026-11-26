# Power, UPS, Solar, Cooling & Rack Infrastructure Planning

Reliable IT infrastructure depends on more than servers and network devices. Electrical protection, backup runtime, energy consumption, cooling, rack layout and physical safety must be planned together.

This guide provides a planning checklist and calculation framework. Final electrical, structural, fire-safety and HVAC designs must be reviewed by qualified professionals and comply with local codes, equipment requirements and site conditions.

## 1. Electrical load and power consumption

Build a load inventory for each rack, room or IT area.

| Equipment | Quantity | Rated input (W) | Measured typical load (W) | Peak load (W) | Criticality |
|---|---:|---:|---:|---:|---|
| Servers / storage | | | | | |
| Network switches / routers | | | | | |
| Firewall / security appliances | | | | | |
| CCTV / NVR / VMS | | | | | |
| IP PBX / telecom | | | | | |
| Monitoring / auxiliary systems | | | | | |
| Cooling and supporting equipment | | | | | |

Prefer measured input power from a suitable meter or PDU over nameplate maximums when building an operational baseline. Keep both normal and peak demand in the design.

### Energy tracking

- Record kW demand and kWh consumption by room, rack or circuit where metering is available.
- Compare daily, monthly and seasonal consumption.
- Identify idle equipment, inefficient cooling and unnecessary always-on loads.
- Track power factor, circuit loading and phase balance where applicable.
- Include UPS conversion losses and cooling energy when assessing total facility consumption.
- Establish alert thresholds and investigate unexpected changes.

Basic energy calculation:

`Energy (kWh) = Average power (kW) × Operating hours`

For example, a continuous average load of 1 kW over 24 hours uses 24 kWh before accounting for measurement boundaries and upstream losses.

## 2. Online UPS and power backup

An online double-conversion UPS continuously converts incoming AC to DC and back to regulated AC for the protected load. It is commonly considered for critical IT equipment where stable output and transfer-free battery operation are required. Confirm topology, efficiency, overload capability, bypass arrangements and compatibility for the specific model.

### UPS assessment checklist

- Identify critical and non-critical loads separately.
- Measure real load in watts and apparent load in VA.
- Confirm power factor, input/output voltage, phase and frequency.
- Check required redundancy, such as N+1, only where justified by the service design.
- Confirm UPS capacity at the expected operating temperature and power factor.
- Review battery chemistry, autonomy curve, battery age and replacement schedule.
- Check static and maintenance bypass, upstream/downstream protection and earthing.
- Verify monitoring cards, SNMP alerts, event logs and remote notification.
- Plan safe maintenance and battery replacement with qualified personnel.
- Confirm generator compatibility and acceptable input frequency/voltage range.

### UPS sizing considerations

Do not size a UPS using VA alone. Check both the UPS watt rating and VA rating against the measured load, while allowing for approved growth and redundancy.

`Required UPS output (W) ≥ Critical measured load (W) + planned headroom`

Runtime must be selected from the manufacturer's runtime curve for the actual load and battery configuration. Runtime is not reliably calculated by multiplying the battery's nominal voltage and amp-hour rating without accounting for inverter efficiency, discharge rate, aging, temperature and cutoff voltage.

### Backup runtime worksheet

| Field | Record |
|---|---|
| Protected load / rack | |
| Measured load (W / VA) | |
| UPS make and model | |
| UPS rated output (W / VA) | |
| Battery type and configuration | |
| Target autonomy | |
| Manufacturer runtime at actual load | |
| Generator / alternate supply | |
| Bypass and maintenance plan | |
| Last battery test / replacement | |
| Monitoring and alert owner | |

## 3. Generator and power continuity

Where a generator is part of the site's continuity design:

- Validate generator capacity against starting loads, UPS input behavior, cooling and other essential services.
- Confirm automatic transfer switch (ATS) operation and maintenance responsibility.
- Define fuel availability, refueling arrangements and safe operating procedures.
- Test generator start, transfer, stable operation and return-to-mains sequence.
- Coordinate tests with UPS, cooling and critical service owners.
- Document what happens if generator start or transfer fails.

A generator, UPS and ATS must be designed as one coordinated power path. Do not assume that generator nameplate kVA alone proves suitability.

## 4. Solar PV and hybrid power planning

Solar can reduce grid energy use or contribute to backup resilience, but grid-tied PV, hybrid inverter and battery-backed systems have different operating and safety characteristics.

Assess:

- Historical daily and seasonal kWh consumption.
- Daytime load profile and critical-load profile.
- Available roof/ground area, shading, orientation and structural suitability.
- Grid interconnection rules, utility approval and anti-islanding protection.
- Inverter type, output rating, surge capacity and compatibility with UPS/generator.
- Battery chemistry, usable energy, depth of discharge, cycle life and replacement cost.
- Essential-load subpanel and load-priority strategy.
- Earthing, surge protection, DC/AC isolators and fire-safety requirements.
- Monitoring, maintenance, warranties and end-of-life disposal.

### Solar and battery estimation

Use actual consumption data and an approved site assessment. A preliminary energy estimate may be expressed as:

`PV array estimate (kWp) ≈ Daily energy target (kWh) ÷ (Peak-sun-hours × overall system derating factor)`

This is only an initial estimate. Final sizing must account for local solar resource, shading, temperature, orientation, inverter efficiency, seasonal variation, utility constraints and system losses.

For battery backup, distinguish nominal battery energy from usable energy. Account for permitted depth of discharge, conversion losses, aging, temperature and required autonomy. Do not promise full-site backup unless the critical-load list and engineered design support it.

## 5. Cooling and environmental management

Cooling must handle the heat released by IT equipment and supporting electrical systems. Use measured load and equipment environmental specifications rather than selecting an air-conditioner based only on room floor area.

Review:

- IT heat load and future rack growth.
- Sensible cooling capacity at actual operating conditions.
- Airflow direction, hot aisle/cold aisle arrangement and blanking panels.
- Supply/return air paths and cable obstruction.
- Temperature and humidity sensors at representative rack locations.
- Redundancy and failure response for critical cooling.
- Condensate drainage, filters, maintenance access and leak detection.
- High-temperature alarms, escalation and emergency response.
- Cooling performance during UPS or generator operation.

### Cooling review record

| Field | Record |
|---|---|
| Room / rack area | |
| Measured IT load (kW) | |
| Estimated heat load and design basis | |
| Cooling unit capacity and operating mode | |
| Supply / return temperature | |
| Humidity range | |
| Airflow arrangement | |
| Redundancy / failover | |
| Sensor and alarm locations | |
| Maintenance / filter schedule | |
| High-temperature response owner | |

Avoid directing cold air without controlling the return path. Poor airflow separation can create hot spots even when the room thermostat reports an acceptable temperature.

## 6. Rack, cabinet and physical layout

Plan rack capacity before installing equipment.

- Confirm rack width, height (U), depth, static/dynamic load rating and floor loading.
- Check equipment rail compatibility, depth clearance and rear cable space.
- Reserve space for growth, maintenance access and airflow.
- Place heavy equipment according to rack and floor loading guidance.
- Separate A/B power feeds where the equipment and facility support them.
- Use appropriately rated PDUs and avoid overloaded strips or daisy-chaining.
- Label both ends of power and data cables.
- Maintain cable management without blocking ventilation.
- Provide earthing/bonding, access control and appropriate fire detection/suppression.
- Keep clear front/rear service access and safe egress.
- Maintain an approved rack elevation and port/power mapping.

### Rack elevation template

| Rack U position | Equipment / blanking panel | Weight | Power feed / PDU | Network / cable reference |
|---|---|---:|---|---|
| U42–U40 | | | | |
| U39–U36 | | | | |
| U35–U32 | | | | |
| U31–U28 | | | | |
| U27–U24 | | | | |

Update the rack elevation after every approved move, add or change. Keep live rack diagrams, exact room locations, circuit identifiers and security details in controlled internal documentation.

## 7. Maintenance and operational checks

| Frequency | Checks |
|---|---|
| Daily / monitored | UPS alarms, load, battery status, room temperature, humidity and power events |
| Weekly | Abnormal load trends, cooling alarms, PDU readings and environmental sensor status |
| Monthly | UPS event review, generator readiness, energy consumption and cooling performance |
| Quarterly / planned | Approved UPS and generator tests, battery health review, thermal inspection and rack audit |
| Annual / lifecycle | Battery replacement assessment, load forecast, cooling service, electrical inspection and capacity review |

Follow manufacturer procedures and site safety rules. Do not perform live electrical work or battery maintenance without qualified authorization.

## 8. Procurement and lifecycle considerations

Compare total cost of ownership, not only initial purchase price:

- UPS topology, rated W/VA, efficiency and runtime at actual load.
- Battery replacement interval and availability.
- Generator fuel, service and testing costs.
- Solar PV yield, inverter warranty, battery lifecycle and utility requirements.
- Cooling efficiency, redundancy, maintenance and refrigerant compliance.
- Rack capacity, PDU type, accessories, earthing and installation.
- Monitoring, spares, vendor response time and end-of-support dates.

Document the design assumptions, measured baseline, options, risks, estimated cost, approval and post-installation acceptance results.

## 9. Safety and publication boundaries

Electrical distribution, generator, PV, battery, cooling and structural rack work can create serious safety risks. Use qualified electrical/HVAC/structural professionals and follow applicable regulations and manufacturer instructions.

Do not publish real circuit identifiers, facility diagrams, access arrangements, exact rack elevations, serial numbers, energy bills, security controls or vendor commercial terms in a public portfolio.

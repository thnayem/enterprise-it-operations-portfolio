# End-User Computing, Desktop Support & Hardware Services

## Scope

This section covers routine enterprise IT support for desktop PCs, laptops, printers, scanners, network storage, Windows installation, hardware upgrades, diagnostics, troubleshooting and repair coordination.

The procedures are general references. Actual steps depend on device model, operating system edition, warranty terms, organizational security policy and vendor documentation.

## Printer Setup & Support

### Setup checklist

1. Identify printer model, connection type and required user/group access.
2. Confirm power, paper, toner/ink and device status.
3. For network printers, verify the approved VLAN, IP reservation, gateway and DNS settings.
4. Install the correct vendor driver or approved universal driver.
5. Add the printer using the organization's standard deployment method.
6. Configure duplex, paper size, tray and default print preferences.
7. Test printing from a standard application and confirm all intended users can print.
8. Document device location, queue name and support contact.

### Troubleshooting

| Symptom | Checks |
|---|---|
| Printer offline | Power, network link, IP reachability, queue and print service |
| Print job stuck | Clear queue using approved procedure; inspect spooler and driver |
| Poor print quality | Toner/ink, drum, printhead, paper type and maintenance cycle |
| Users cannot connect | Permissions, print server, driver compatibility and network path |
| Slow printing | Large documents, queue load, network errors and device memory |

## NAS Setup & Shared Storage

### Planning and setup

- Confirm business requirement, capacity, performance and availability expectations.
- Select a supported NAS model and compatible drives using the manufacturer's compatibility list.
- Plan RAID/storage pool layout based on capacity, fault tolerance and rebuild considerations.
- Configure management access on a restricted network.
- Set hostname, time synchronization, DNS and approved network settings.
- Create shared folders and groups based on business ownership.
- Apply least-privilege permissions and test access with representative user accounts.
- Configure snapshots, backup replication or cloud/off-site backup where supported.
- Enable monitoring for disk health, pool capacity, temperature and device status.
- Document recovery steps and periodically test file restoration.

### Important distinctions

- RAID is not a backup. It does not protect against accidental deletion, ransomware, theft or site-level failure.
- NAS snapshots are useful recovery points but should not be treated as the only backup.
- Capacity planning must account for RAID overhead, filesystem reserve, snapshot growth and future expansion.
- Avoid exposing NAS management interfaces directly to the public internet.

## Scanner Setup

- Identify flatbed, sheet-fed or network multifunction scanner model.
- Install vendor-supported drivers and scanning software.
- Configure USB or network connectivity.
- Set approved scan profiles: resolution, color mode, duplex, file format and destination.
- Configure scan-to-folder or scan-to-email only with authorized service credentials and permissions.
- Test multi-page documents, OCR if required, file naming and destination access.
- Confirm access control and handling requirements for scanned confidential documents.

## PC & Laptop Hardware Upgrades

### RAM upgrade

1. Confirm exact device model and service manual.
2. Check supported memory generation, form factor, capacity, speed and slot availability.
3. Verify whether memory is soldered or replaceable.
4. Check maximum supported capacity and module compatibility.
5. Shut down, disconnect power and follow ESD precautions.
6. Install compatible memory using manufacturer procedure.
7. Verify capacity in BIOS/UEFI and the operating system.
8. Run appropriate memory diagnostics and stability checks.

### SSD / storage upgrade

- Confirm supported interface and form factor: SATA 2.5-inch, M.2 SATA or M.2 NVMe.
- Check physical length, keying and platform compatibility.
- Review firmware/BIOS support and available storage slots.
- Back up user data and verify recovery media before migration.
- Clone or clean-install according to the approved deployment plan.
- Confirm boot mode, partition layout, encryption and device drivers.
- Verify SMART/health status and run post-upgrade checks.

### Upgrade record

Record device asset ID, model, previous and new RAM/storage specifications, installation date, test results and replaced-part disposition. Do not publish serial numbers or user data.

## Windows Installation & Configuration

### Pre-installation

- Confirm device ownership and approved Windows edition/licensing.
- Back up user data and verify that the backup can be accessed.
- Confirm hardware compatibility, storage health and firmware settings.
- Prepare installation media from an authorized Microsoft source.
- Record required drivers, applications, encryption and domain/join requirements.

### Installation and baseline

1. Install the approved Windows version using the organization's deployment process.
2. Apply supported firmware and hardware drivers.
3. Install current security and quality updates.
4. Configure hostname, time zone, network and approved identity/domain enrollment.
5. Enable endpoint protection, firewall and disk encryption according to policy.
6. Install approved business applications and printer/scanner utilities.
7. Configure user profile, permissions and standard settings.
8. Verify Windows activation and update status.
9. Test network, audio, camera, USB, printing, scanning and required business applications.
10. Return the device with a completion record and user confirmation.

## Diagnostics, Troubleshooting & Repair

### Standard diagnostic workflow

1. **Understand:** collect the reported symptoms, recent changes and business impact.
2. **Inspect:** check physical condition, power, cables, indicators, temperature and visible damage.
3. **Reproduce:** confirm the fault and identify whether it is consistent or intermittent.
4. **Isolate:** test the device, user profile, application, network path or peripheral separately.
5. **Diagnose:** use approved OS logs, built-in diagnostics, vendor tools and hardware tests.
6. **Plan:** determine repair, replacement, reconfiguration or escalation; check warranty first.
7. **Resolve:** perform only authorized changes and protect user data.
8. **Validate:** repeat the original test and check related functions.
9. **Document:** record cause, action, parts, outcome and any follow-up.

### Common fault categories

| Category | Examples of checks |
|---|---|
| Power/startup | Adapter, battery, power supply, POST indicators and boot device |
| Performance | CPU/RAM/disk utilization, startup apps, thermal throttling and storage health |
| Windows/software | Event logs, updates, drivers, services, profile and application errors |
| Storage | SMART status, filesystem errors, free space, backup and disk diagnostics |
| Memory | Supported configuration, seating, firmware detection and memory test |
| Network | Link, Wi-Fi, IP configuration, DNS, gateway and endpoint policy |
| Peripherals | Driver, cable, port, firmware, queue and device compatibility |

## Service Desk & User Support

- Record incidents and service requests with clear symptoms and impact.
- Prioritize based on business impact and agreed service levels.
- Provide clear user communication and realistic status updates.
- Use remote support tools only with authorization.
- Protect confidential files and credentials during troubleshooting.
- Escalate hardware faults, suspected data loss and security incidents through approved channels.
- Close tickets only after validation and user confirmation where appropriate.

## Safety, Security & Data Protection

- Follow ESD precautions and manufacturer repair instructions.
- Do not open power supplies or attempt unsafe electrical repairs.
- Check warranty terms before hardware disassembly.
- Obtain authorization before accessing user files or resetting devices.
- Back up data before storage replacement, OS reinstallation or repair operations.
- Use licensed software and approved installation media.
- Securely handle or erase retired storage according to organizational policy.
- Do not publish employee data, device serial numbers, recovery keys, passwords, private IP plans or internal asset inventories.

## Related References

- [System & Server Virtualization Portfolio](https://github.com/thnayem/system-server-virtualization-portfolio)
- [Network Engineering Portfolio](https://github.com/thnayem/network-engineering-portfolio)
- [Enterprise IT Operations Portfolio Home](../README.md)

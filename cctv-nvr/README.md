# IP CCTV, NVR/VMS & Storage Planning

## Scope

Reference material for operating large IP CCTV environments, including camera onboarding, NVR/VMS architecture, recording policy, storage sizing, health monitoring and operational support.

A camera estate described as **800+ cameras** should be treated as a scale-planning requirement, not evidence that one recorder can support that number. Capacity depends on the exact recorder/VMS platform, licensed channel count, ingest throughput, disk design, network design and retention policy.

## High-Level Architecture

1. IP cameras connect to managed PoE access switches.
2. Access switches aggregate to distribution/core switches over copper or optical uplinks.
3. CCTV traffic is segmented from user and server networks using dedicated VLANs and access controls.
4. NVR/VMS recording services are deployed according to validated channel and throughput limits.
5. Storage is designed for required retention, disk failure tolerance and rebuild behavior.
6. Monitoring covers camera reachability, recording status, storage health and server availability.
7. Authorized operators access live and recorded video through controlled client access.

## Camera Onboarding Checklist

- Record camera make/model, firmware, location reference and ownership.
- Assign a reserved address from the CCTV address plan.
- Set unique credentials and disable unused accounts/services.
- Configure time synchronization and correct time zone.
- Configure resolution, frame rate, codec, bitrate and stream profile.
- Confirm camera stream compatibility with the selected NVR/VMS.
- Verify live view, recording, playback, export and time search.
- Record switch port, PoE budget and uplink path in the asset register.

## Storage Sizing Method

For a first-order estimate using average bitrate:

**Daily storage (decimal TB) ≈ total bitrate (Mbps) × 0.0108**

**Retention storage (TB) ≈ daily storage × retention days**

Then add capacity for RAID/parity overhead, filesystem/formatting, operational free space, metadata, bitrate variation and growth. Usable capacity must be calculated from the selected RAID layout and actual drive sizes; raw disk capacity is not usable recording capacity.

### Illustrative calculation only

Assume 800 cameras averaging 4 Mbps each and continuous recording:

- Aggregate bitrate: 800 × 4 Mbps = 3,200 Mbps
- Approximate daily video data: 3,200 × 0.0108 = 34.56 TB/day
- Approximate 30-day video data: 34.56 × 30 = 1,036.8 TB

This is a simplified decimal estimate before RAID, filesystem, free-space, metadata, overhead and growth allowances. Actual sizing must use measured stream bitrates and the recording schedule. Motion-based recording changes the estimate and must be based on measured activity, not an assumed percentage.

## Design Inputs Required Before Sizing

| Input | Why it matters |
|---|---|
| Camera count and model | Codec, stream limits and compatibility |
| Resolution and frame rate | Drives image quality and bitrate |
| Average/maximum bitrate | Determines ingest and storage demand |
| H.264/H.265 profile | Affects compression and client compatibility |
| Continuous/motion/scheduled recording | Determines recording hours per day |
| Retention requirement | Multiplies daily data volume |
| RAID level and hot spare policy | Changes usable capacity and resilience |
| NVR/VMS throughput and channel licenses | Determines recorder/server count |
| Playback/export concurrency | Adds compute and network demand |

## Large-Scale NVR/VMS Design Considerations

- Divide camera channels across recording servers based on vendor-tested limits.
- Validate aggregate ingest bandwidth and concurrent playback/export requirements.
- Consider separate management, recording and storage roles where the platform supports them.
- Plan redundant power, storage fault tolerance, backup of configuration and recovery procedures.
- Use a dedicated CCTV VLAN and controlled inter-VLAN access.
- Verify retention and evidence-export requirements with the organization's policy.
- Test failure scenarios: disk degradation, recorder outage, uplink loss and camera reconnect.

## Operations Checklist

- Daily: review camera offline events, recording gaps, storage alarms and time drift.
- Weekly: review capacity trend, failed disks, PoE issues and recurring disconnects.
- During changes: record affected cameras, maintenance window, rollback and post-change tests.
- Periodically: test playback/export, permissions, time synchronization and restore procedures.

## Privacy & Security

Video footage and camera metadata can be sensitive. Restrict live view, playback, export and administration by role. Use strong credentials, secure management access, retention policy and audit logging. Do not upload real camera lists, footage, credentials, site maps or private IP allocations to a public repository.

---

**A note on this documentation:** The technical work and experience behind these notes are mine. Some wording and the way I have organized the material have had AI assistance, mainly to make the writing clearer and save time. The examples, decisions and work described are not AI-generated. I check what I publish and stand behind it.

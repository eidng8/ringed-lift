# Appendix II: Stratospheric Platform

## Volume VIII: Deployment and Maintenance Plan

**Version**: 1.2<br/>
**Date of Preparation**: June 2026<br/>
**Currency Unit**: Renminbi (RMB), symbol: ¥<br/>
**Related Main Volumes**: Main Volume VIII, Main Volume III<br/>
**Prerequisite Reading**: Volumes I through VII of this Appendix


### Glossary of Abbreviations

| Abbreviation | Full Name | Notes |
|------|----------|------|
| ECLSS | Environmental Control and Life Support System | Environmental Control and Life Support System |
| EVA | Extravehicular Activity | Operations performed outside the aerostat or gondola by crew members |
| HAPS | High Altitude Pseudo-Satellite | The internationally accepted designation for stratospheric platforms |
| LLS | Lightning Location System | Lightning Location System |
| MLI | Multi-Layer Insulation | Used for passive thermal control of equipment bays |
| MTBF | Mean Time Between Failures | Mean Time Between Failures |
| MTTR | Mean Time To Repair | Mean Time To Repair |
| RHU | Radioisotope Heating Unit | Used to maintain equipment operating temperature in low-temperature environments |
| UPS | Uninterruptible Power Supply | Uninterruptible Power Supply |


### 8.1 Volume Preamble

This volume is positioned as the **deployment and full life-cycle maintenance plan** for the stratospheric platform system, focused on answering the following core questions:

> How does a stratospheric platform travel from the ground to the anchoring point and complete deployment? How is it periodically returned to the ground for inspection and component replacement? How is redundancy configuration and task scheduling achieved during multi-platform coordinated operations? What is the full life-cycle maintenance plan for the platform from commissioning to decommissioning? How are the service lives and replacement cycles of critical equipment determined? How are spare parts managed and replenished?

This volume builds on:
- **Volume I of this Appendix (Platform Overall Design)**: Aerostat mass, tether cable parameters, gondola design, and ground anchoring interfaces have been established.
- **Volume II of this Appendix (Energy and Positioning Systems)**: Service lives and replacement cycles for the photovoltaic array, energy storage system, and navigation equipment have been established.
- **Volume III of this Appendix (Maintenance, Repair, and Rescue)**: Operating procedures and cycles for ring elevator cable maintenance including track sleeves, rack rails, and sealed segments have been established.
- **Volume IV of this Appendix (Experimental R&D Platform)**: Maintenance requirements for subscale experiment equipment have been established.
- **Volume V of this Appendix (Lightning Initiation and Protection)**: Maintenance cycles for lightning conductors, pulse power supplies, and grounding systems have been established.
- **Volume VI of this Appendix (Communications Relay)**: Service lives and replacement cycles for communications equipment have been established.
- **Volume VII of this Appendix (Emergency, Protection, and Rescue)**: Storage cycles for emergency supplies and drill frequency have been established.
- **Main Volume III (Node Siting and Anchoring Engineering)**: Ring elevator anchor stations have been designed; stratospheric platforms can share their ground facilities.

The core tasks of this volume are:

1. Design the ground anchoring and deployment/retrieval system, specifying interface requirements when stratospheric platforms share an anchoring station with the ring elevator.
2. Formulate the periodic ground return and inspection procedure, specifying inspection cycles and checklist items.
3. Plan multi-platform coordinated formations and redundancy configuration, ensuring that tasks are not interrupted in the event of a single-platform failure.
4. Establish a full life-cycle maintenance plan for the platform, providing service lives, replacement cycles, and spare parts strategies for critical equipment.
5. Output key parameters for use by Volume IX (Economic Model) and Volume X (Technical Interfaces).


### 8.2 Ground Anchoring and Deployment/Retrieval System

#### 8.2.1 Selection of Anchoring Method

The ground anchoring of stratospheric platforms can adopt either of the following two methods:

| Anchoring Method | Applicable Scenario | Advantages | Disadvantages |
|:---|:---|:---|:---|
| **Shared ring elevator anchor station** | Platform deployed at ring elevator nodes (Brazil, Gabon, Indonesia, etc.) | No need to independently construct grounding network, communications ground station, or maintenance facilities; investment is shared | Subject to impact of ring elevator construction progress |
| **Independent anchoring point** | Platform deployed at non-ring elevator nodes (e.g., polar scientific observation stations) | Flexible deployment, not dependent on the ring elevator | Requires independent construction of all ground facilities |

**Recommendation of this volume**: Priority shall be given to the shared ring elevator anchor station scheme. Independent anchoring points shall only be considered when ring elevator nodes are not yet available for deployment. The ground facilities design for independent anchoring points may reference Section 3.3 of Main Volume III; this volume does not repeat that content.

#### 8.2.2 Shared Anchoring Interface Requirements

When stratospheric platforms share an anchor station with the ring elevator, the following interface requirements must be satisfied:

| Interface Type | Requirement | Source / Basis |
|:---|:---|:---|
| Mechanical interface | The tether cable is connected to the ground winch via a redirecting pulley at the top of the anchoring tower. The winch is independent of the ring elevator anchoring system and shares the anchoring tower structure | Main Volume III Section 3.5.2 |
| Electrical interface | The grounding terminal of the platform's lightning initiation system is connected to the ring elevator grounding network, with connection impedance ≤0.5 Ω and a detachable isolation disconnect switch | Volume V of this Appendix, Section 5.4.1 |
| Communications interface | The platform's Ka/Ku ground antenna shares the RF front-end with the ring elevator ground station, isolated via an optical switch | Volume VI of this Appendix, Section 6.3 |
| Maintenance facilities | Shared maintenance workshop, spare parts warehouse, and crew living quarters of the ring elevator anchor station | — |
| Safety isolation | Physical separation (firewall, safety distance ≥10 m) between the platform and the ring elevator anchoring system | — |

> **Note**: The tether cable tension of stratospheric platforms (≤50 kN) is far smaller than that of ring elevator cables (≥1.57×10⁹ N); therefore, the winch must be independently designed and must not be shared with the ring elevator.

#### 8.2.3 Ground Winch and Deployment/Retrieval System

The ground winch is used for tether cable deployment/retrieval and tension control, and is the core equipment for platform deployment and recovery.

| Parameter | Design Value | Notes |
|:---|:---|:---|
| Winch type | Dual-drum (main/standby), electric + hydraulic drive | Redundant design |
| Rated pull force | ≥50 kN | Covers maximum net lift of the platform |
| Deployment/retrieval speed | 0–5 m/s (stepless speed control) | Matched to platform ascent/descent speed |
| Cable capacity | ≥55 km (including 50 km operating altitude + 10% margin) | — |
| Tension control accuracy | ±5% of set value | Constant-tension mode |
| Emergency brake | Spring-energy-storage brake, auto-engages on power loss | Normally closed type |
| Winch mass | ≤15,000 kg | Including drum, motor, reducer, and control system |
| Winch power consumption | ≤30 kW (peak during cable retrieval) | — |

> **Note**: The winch is installed on an independent foundation; foundation load capacity ≥20 tonnes; concrete foundation dimensions are designed according to geological conditions.

**Winch layout**: Installed in the ground equipment room of the anchor station, arranged in parallel with the ring elevator anchoring system, sharing the foundation.


### 8.3 Periodic Ground Return and Inspection Procedures

#### 8.3.1 Inspection Cycles

| Inspection Level | Cycle | Downtime | Main Work Content |
|:---|:---:|:---:|:---|
| **Level A (Routine Check)** | Once per month | 2–4 h | Visual inspection, data download, software upgrade, consumables replenishment |
| **Level B (Quarterly Maintenance)** | Once per quarter | 1–2 days | Electrical system testing, communications link testing, emergency drills |
| **Level C (Annual Overhaul)** | Once per year | 7–14 days | Equipment disassembly and inspection, worn component replacement, calibration, gas-bag leak detection |
| **Level D (Midterm Overhaul)** | Once every 5 years | 30–45 days | Core equipment factory repair, envelope replacement, cable replacement (aligned with envelope replacement cycle; mandatory major overhaul) |

#### 8.3.2 Ground Return Operating Procedure

1. **Issue command**: Ground control center confirms weather conditions (surface wind speed <10 m/s, no thunderstorms) and issues altitude-descent command.
2. **Ballonnet venting**: The aerostat's ballonnet vent valves open, reducing buoyancy; the platform begins to descend.
3. **Winch cable retrieval**: The ground winch reels in the tether cable at ≤5 m/s, maintaining cable tension.
4. **Approach to ground**: When platform altitude ≤50 m, reduce speed to ≤1 m/s.
5. **Landing and locking**: After the platform contacts the docking platform on the anchoring tower, the mechanical locking device engages automatically.
6. **Tether release**: Operators disconnect the tether cable from the aerostat end (or retain it, depending on maintenance requirements).
7. **Platform storage**: The aerostat is towed to the maintenance hangar (if available).

#### 8.3.3 Inspection Items and Cycle Reference Table

| System | Inspection Item | Level A | Level B | Level C | Level D | Basis / Source |
|:---|:---|:---:|:---:|:---:|:---:|:---|
| Aerostat | Envelope visual inspection (cracks, wear) | ✓ | ✓ | ✓ | Replace | Volume I |
| | Helium pressure and leak rate | ✓ | ✓ | ✓ | — | Volume I |
| | Ballonnet valve function | — | ✓ | ✓ | Overhaul | Volume I |
| Tether cable | Visual wear inspection | ✓ | ✓ | ✓ | Replace | Volume I |
| | Tension calibration | — | ✓ | ✓ | — | Volume I |
| | Embedded fiber optic attenuation test | — | ✓ | ✓ | — | Volume VI |
| Energy system | Photovoltaic array I-V test | — | ✓ | ✓ | Replace | Volume II |
| | Battery bank capacity test | — | ✓ | ✓ | Replace | Volume II |
| | Nuclear power source (if fitted) | — | — | — | Per nuclear safety regulations | — |
| Lightning initiation system | Lightning conductor visual inspection | ✓ | ✓ | ✓ | Replace | Volume V |
| | Pulse power supply functional test | — | ✓ | ✓ | Overhaul | Volume V |
| | Grounding resistance measurement | — | ✓ | ✓ | — | Volume V |
| Communications system | Antenna pointing accuracy | — | ✓ | ✓ | — | Volume VI |
| | Transmit power / receive sensitivity | — | ✓ | ✓ | — | Volume VI |
| Gondola | Drive gear wear | ✓ | ✓ | ✓ | Replace | Volume III |
| | Track-sleeve outer layer wear | ✓ | ✓ | Replace | — | Volume III |
| | Sealed-segment inert gas pressure | ✓ | ✓ | — | — | Volume III |
| Emergency equipment | Oxygen mask / cylinder pressure | ✓ | ✓ | ✓ | Replace | Volume VII |
| | Fire extinguisher pressure | ✓ | ✓ | ✓ | Replace | Volume VII |
| | Escape capsule parachute | — | — | ✓ | Recertify | Volume VII |
| Overall | Full-system functional test | — | — | ✓ | ✓ | — |


### 8.4 Multi-Platform Coordinated Formation and Redundancy Configuration

#### 8.4.1 Formation Scheme

When task requirements exceed single-platform capability (e.g., continuous equatorial belt coverage, synchronous multi-altitude polar observation), multiple stratospheric platforms can be deployed to form a coordinated formation.

| Formation Mode | Number of Platforms | Spacing | Coverage Area | Typical Tasks |
|:---|:---:|:---:|:---|:---|
| **Single platform** | 1 | — | Radius ≤600 km | Ring elevator maintenance, local communications relay |
| **Equatorial chain** | 6 | Approx. 60° longitude spacing | Continuous equatorial belt coverage | Global communications relay, navigation augmentation |
| **Polar network** | 3–4 | 120° longitude spacing | Polar regions (>80°N/S) continuous coverage | Polar meteorological observation, ice sheet monitoring |
| **Altitude-stratified** | 2–3 | Same lat/lon, different altitudes | 20 km, 30 km, 40 km | Atmospheric profile research |

#### 8.4.2 Redundancy Configuration Strategy

| Redundancy Level | Configuration | Switchover Mechanism | Recovery Time |
|:---|:---|:---|:---|
| **Equipment level** | Critical equipment (power, communications, control) n+1 redundancy | Automatic switchover | <1 s |
| **Platform level** | Adjacent platforms serve as mutual backups | Ground control center dispatches | Minutes |
| **Ground level** | Multiple ground stations back each other up | Automatic routing switchover | <10 s |

**Equipment-level redundancy list**:

| Equipment | Redundancy Method | Notes |
|:---|:---|:---|
| Main control computer | Dual hot-standby (1+1) | Automatic switchover on failure |
| Communications transceiver | Dual channel (Ka/Ku) | Mutual backup |
| Power distribution unit | Dual bus | Switches on failure of either bus |
| Energy storage battery bank | Capacity redundancy (120% of design capacity) | Single-string failure does not interrupt power supply |
| Winch motor | Main/standby motor | Manual switchover on failure |

#### 8.4.3 Task Scheduling and Handover

When a platform must return to the ground due to failure or maintenance, its tasks are taken over by an adjacent platform:

| Task Type | Handover Method | Handover Condition |
|:---|:---|:---|
| Communications relay | Adjacent platform adjusts antenna pointing to cover the original platform's area | <5 min after platform failure confirmed |
| Navigation augmentation | Adjacent platform increases differential signal transmit power | <10 min after platform failure confirmed |
| Ring elevator maintenance | Standby gondola dispatched or adjacent platform gondola performs task | Requires advance coordination |
| Meteorological observation | Data supplemented by adjacent platform, or degraded collection | Sparse data acceptable |

> **Note**: Failure confirmation is based on three consecutive missed heartbeats (10 s interval) or critical telemetry exceedance (e.g., main power voltage, ECLSS pressure).


### 8.5 Platform Full Life-Cycle Maintenance Plan

#### 8.5.1 Design Service Life and Decommissioning Strategy

| Platform Component | Design Service Life | Decommissioning Method | Replaceability |
|:---|:---:|:---|:---:|
| Aerostat envelope | 5 years | Replacement | Yes (replaced during major overhaul) |
| Tether cable | 10 years | Replacement | Yes |
| Photovoltaic array | 10 years | Replacement | Yes |
| Energy storage battery bank | 5 years | Replacement (cascade reuse) | Yes |
| Lightning conductor | 10 years | Replacement | Yes |
| Pulse power supply | 10 years | Factory repair | Yes |
| Communications antenna | 15 years | Replacement | Yes |
| Electronic equipment (control, communications) | 10 years | Replacement | Yes |
| Gondola drive gear | 3 years | Replacement (consumable) | Yes |
| Track-sleeve outer layer | 1–3 years | Replacement (consumable) | Yes |
| **Platform overall** | **15 years** | **Disassembly and recycling** | — |

> Note: The overall design service life of the platform is 15 years; service life is extended through periodic replacement of short-life components. After 15 years, an assessment is made on whether to conduct a second major overhaul or decommission the platform.

#### 8.5.2 Spare Parts Strategy

| Spare Parts Category | Storage Location | Minimum Stock | Replenishment Cycle | Notes |
|:---|:---|:---:|:---:|:---|
| Consumables (track-sleeve outer layer, sealing strips) | Anchor station warehouse | 1-year supply | Annual replenishment | Light weight; air-transportable |
| Wear parts (gears, bearings, sealing rings) | Anchor station warehouse | 2 sets | Semi-annual inspection | — |
| Electronic modules (power, communications, control) | Anchor station warehouse | 1 set | As needed | High-value spares shared |
| Large components (cable, photovoltaic panels) | Dedicated warehouse near anchor station (or ring elevator regional maintenance center) | 1 set | As needed | Requires special transport |
| Emergency supplies (oxygen, medicines) | Anchor station warehouse | 3-month supply | Monthly inspection | — |

#### 8.5.3 Maintenance Cost Estimates

| Maintenance Item | Annual Frequency | Estimated Unit Cost | Estimated Annual Cost | Notes |
|:---|:---:|:---:|:---:|:---|
| Level-A routine check | 12 times | ¥50,000 | ¥600,000 | Labor + consumables |
| Level-B quarterly maintenance | 4 times | ¥200,000 | ¥800,000 | Including test equipment |
| Level-C annual overhaul | 1 time | ¥1,500,000 | ¥1,500,000 | Including consumable replacements |
| Level-D midterm overhaul | Once every 5 years | ¥5,000,000 | ¥1,000,000/yr (average) | Including envelope replacement |
| Spare parts procurement | — | — | ¥2,000,000/yr | — |
| Ground facilities maintenance | — | — | ¥500,000/yr | Including winch, grounding network, communications ground station |
| **Total annual maintenance cost** | — | — | **≈¥6,400,000** | — |

> Note: The above is an estimated annual maintenance cost for a single platform. For multiple platforms, per-platform costs can be reduced by sharing spare parts and ground facilities.


### 8.6 Deployment Procedure (First Deployment)

#### 8.6.1 Pre-Deployment Preparation

| Phase | Work Content | Responsible Party | Duration |
|:---|:---|:---|:---:|
| Ground facilities construction | Anchoring tower, winch, grounding network, communications ground station | Ground construction team | 6 months |
| Platform ground assembly | Aerostat inflation, gondola installation, systems integration testing | Platform manufacturer | 2 months |
| Tether cable laying | Cable drawn from ground winch to aerostat | Platform manufacturer | 1 week |
| Low-altitude tethered test | Platform raised to 50 m; all systems tested | Platform control center | 3 days |
| First ascent | Platform raised to operating altitude (25–35 km) | Platform control center | 1 day |

#### 8.6.2 Deployment Transport

Aerostat components (envelope, gas bag, gondola, equipment) are transported to the anchoring point by land or sea. The tether cable is transported to the site by a dedicated cable transport vehicle. Large components (e.g., antennas) require containers.

#### 8.6.3 Deployment Cost (Single Platform, First Deployment)

| Item | Cost Estimate | Notes |
|:---|:---:|:---|
| Platform manufacturing | ¥30,000,000–50,000,000 | Including aerostat, gondola, and equipment |
| Tether cable | ¥5,000,000–8,000,000 | 50 km CNT cable |
| Ground facilities construction | ¥10,000,000–20,000,000 | Including winch, anchoring tower, grounding network, and communications ground station |
| Transport and installation | ¥2,000,000–3,000,000 | — |
| Testing and commissioning | ¥1,000,000–2,000,000 | — |
| **Total first-deployment cost** | **¥48,000,000–83,000,000** | — |


### 8.7 Parameter Outputs

| Parameter | Value | Status | Receiving Volume |
|:---|:---|:---|:---|
| Ground winch rated pull force | ≥50 kN | Design baseline | — |
| Winch deployment/retrieval speed | 0–5 m/s | Design baseline | Volume I |
| Level-A inspection cycle | Once per month | Procedural requirement | — |
| Level-B inspection cycle | Once per quarter | Procedural requirement | — |
| Level-C inspection cycle | Once per year | Procedural requirement | — |
| Level-D inspection cycle | Once every 5 years | Procedural requirement | — |
| Platform overall design service life | 15 years | Design baseline | Volume IX |
| Envelope replacement cycle | 5 years | Design baseline | — |
| Tether cable replacement cycle | 10 years | Design baseline | — |
| Energy storage battery replacement cycle | 5 years | Design baseline | Volume II |
| Gondola drive gear replacement cycle | 3 years | Design baseline | Volume III |
| Track-sleeve outer layer replacement cycle | 1–3 years | Design baseline | Volume III |
| Annual maintenance cost (single platform) | ≈¥6,400,000 | Order-of-magnitude estimate | Volume IX |
| Total first-deployment cost | ¥48,000,000–83,000,000 | Order-of-magnitude estimate | Volume IX |
| Multi-platform redundancy switchover time | ≤5 min (platform level) / <1 s (equipment level) | Design target | — |


### 8.8 Volume VIII Conclusion

This volume has completed the full design of the stratospheric platform deployment and full life-cycle maintenance plan. The core contributions are as follows:

1. **Interface requirements for shared ring elevator anchoring have been specified.** When stratospheric platforms are deployed at ring elevator nodes, they can share the grounding network, communications ground station, and maintenance facilities, significantly reducing investment. Interface parameters (mechanical, electrical, communications, and safety isolation) have been fully defined, and the reason for the winch being independent of the ring elevator has been explained.

2. **A four-level inspection system has been established.** Level-A routine check (monthly), Level-B quarterly maintenance, Level-C annual overhaul, and Level-D midterm overhaul (every 5 years, aligned with the envelope replacement cycle; mandatory major overhaul) cover the entire process from routine inspection to major overhaul. The inspection items and cycle reference table is clear and aligned with equipment service lives across all volumes.

3. **Multi-platform coordinated formations and redundancy configuration have been planned.** Three formation modes are supported: equatorial chain (6 platforms), polar network (3–4 platforms), and altitude-stratified (2–3 platforms). A three-tier redundancy strategy consisting of equipment-level redundancy (n+1), platform-level takeover, and ground-level mutual backup has been defined, with clear failure confirmation criteria (missed heartbeats or telemetry exceedance), ensuring tasks are not interrupted in the event of a single-platform failure.

4. **A full life-cycle maintenance plan has been formulated.** Design service lives of all components have been specified (envelope 5 years, cable 10 years, battery 5 years, gear 3 years, etc.); overall platform design service life is 15 years. The spare parts strategy distinguishes between consumables, wear parts, electronic modules, large components, and emergency supplies; the storage location for large components is specified as "dedicated warehouse near the anchor station (or ring elevator regional maintenance center)."

5. **Maintenance and deployment costs have been estimated.** Annual maintenance cost per platform is approximately ¥6,400,000; total first-deployment cost is approximately ¥48,000,000–83,000,000; ground facilities construction costs have been itemized (including winch, anchoring tower, grounding network, and communications ground station), providing inputs for the Volume IX economic model.

The parameter outputs of this volume are sufficient to support Volume IX (Economic Model) and Volume X (Technical Interfaces). The deployment procedure and inspection system can directly guide engineering implementation.


### References

[8.1] ISO 4309:2017, *Cranes — Wire ropes — Care and maintenance, inspection and discard*.

[8.2] Main Volume III: Node Siting and Anchoring Engineering, 2026.

[8.3] Volume V of this Appendix: Lightning Initiation and Protection Subsystem, 2026.

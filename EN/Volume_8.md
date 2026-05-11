# Volume 8: Transportation and Logistics Systems

**Version**: 2.5<br/>
**Compilation Date**: May 2026<br/>
**Currency Unit**: Renminbi (Yuan), symbol: ¥<br/>


## Terminology Table

| Abbreviation | English Full Name |
|------|----------|
| C/SiC | Carbon Fiber-Reinforced Silicon Carbide (Composite) |
| CNT | Carbon Nanotube |
| DM | Drive Module |
| GEO | Geostationary Earth Orbit |
| HAPS | High-Altitude Platform Station |
| ISRU | In-Situ Resource Utilization |
| LEO | Low Earth Orbit |
| PM | Payload Module (Cabin) |


## 8.1 Preface

This volume is positioned as the **transportation, logistics system, and global construction sequence planning** for the Space Ringed-Elevation Project, focusing on answering the following core questions:

> For the ring cable with a total mass of nearly 80 million tons, hundreds of millions of tons of counterweights, hundreds of space spiders, and the infrastructure of 6 elevator nodes, in what order should they be constructed? How should they be transported from the ground, the Moon, or asteroids to the GEO construction orbit? What types of carriers, launch cadence, and logistics networks are required?

Core tasks of this volume:

1. Propose a complete **global construction sequence**, establishing the construction logic of "starting with the elevator." The construction schedule is strictly based on the physical constraints of the first five volumes, using conservative engineering judgment as the baseline.
2. Summarize all transportation requirements and establish a complete logistics list from raw materials to finished products in orbit.
3. Design the three main transportation corridors: Earth to GEO, Moon to GEO, and Asteroid to GEO.
4. Provide an order-of-magnitude estimate of the total cost of the transportation system for use in Volume 10 (Economic Model).

This volume only provides functional descriptions of **lunar industry** and **High Altitude Platform Systems (HAPS)** as directly related to transportation and construction. Detailed technical solutions are compiled separately as independent appendices (Appendix 1: Lunar Industry; Appendix 2: HAPS).


## 8.2 Design Baselines and Constraints

### 8.2.1 Physical Constraints

The following constraints are derived from the locked parameters of the first five volumes. The construction sequence must strictly adhere to these:

| Constraint | Value | Source |
|------|------|------|
| One-way travel time (200 km/h low-altitude scheme) | ≈50 h | Volume 5, Section 5.8.3 |
| Round-trip pure travel time | ≈100 h (≈4.17 d) | Volume 5, Section 5.8.3 |
| Complete round-trip cycle including docking | ≥5 d | Includes loading/unloading, inspection, resupply |
| Maximum round-trips per elevator per year | ≈70/year | 365 d ÷ 5 d − maintenance downtime |
| Fully loaded cabin total mass | 200 t (C2 configuration) | Volume 5, Section 5.2.1 |
| DM mass | ≈49.3 t | Volume 5, Section 5.10.4 |
| PM mass | ≈69.4 t | Volume 5, Section 5.10.4 |
| Effective payload limit | **≈81.3 t/trip** | 200 − 49.3 − 69.4 |
| Annual effective capacity per elevator | **≈5,700 t/year** | 70 round-trips × 81.3 t |
| Single ring cable segment length/mass | 500 m / ≈150 t | Volume 6, Section 6.4.2 |
| Total number of ring cable segments | ≈530,916 segments | Volume 6, Section 6.4.2 |
| Total ring cable mass | ≈7.96×10⁷ t | Volume 6, Section 6.4.2 |

### 8.2.2 Conservative Estimate of Elevator Capacity

After the first elevator is completed, it does not immediately have full operational capacity. The trial operation phase must gradually verify the stability of the cable suspension, the reliability of the cabin drive system throughout the journey, and the repeated docking precision of the ground and GEO terminal mechanisms.

| Trial Phase | Duration | Load | Speed | Round-trip Frequency |
|------------|------|------|------|----------|
| Phase 1 (unloaded/light load) | 6 months | ≤50 t | ≤100 km/h | Once per month |
| Phase 2 (half load) | 6 months | 50–100 t | ≤200 km/h | Once per week |
| Phase 3 (full load verification) | 1 year | 200 t | 200 km/h | Once every 3 days |
| Commercial operation | Thereafter | ≤200 t | 200 km/h | Once every 5 days (including maintenance) |

From the "completion" of the first elevator (cable in place + counterweight stabilized) to having commercial operational capability (70 full-load round-trips per year, annual effective capacity about 5,700 t), at least **2 years of trial operation** are required.


## 8.3 Global Construction Sequence

### 8.3.1 Physical Logic of Construction

The physical composition of the ring elevator system includes three levels: **elevator cables** (6), **ring main body** (closed loop with a radius of 42,264 km), and **supporting facilities** (cabins, DM, racks, track sleeves, counterweights, etc.).

The core logic of construction is **elevators first, then the ring**. Reasons are as follows:

- The total weight of the ring cable is nearly 80 million tons and must be launched to GEO in large quantities by heavy-lift rockets from the ground.
- The first completed elevator can provide **auxiliary capacity for precision component transport** and **personnel rotation** for subsequent elevators and ring construction. Although the elevator's effective capacity (≈5,700 t/year/unit) is far from enough to replace rocket launches of ring cable segments (capacity gap of three orders of magnitude), it can undertake irreplaceable tasks—precision components such as DM, PM, and C/SiC connectors cannot be roughly launched into orbit by rockets and self-assembled; they must be transported smoothly by elevator. Personnel transfer is also an exclusive task for the elevator.
- The first elevator is the most difficult—geological surveys start from scratch, anchoring schemes are implemented for the first time, cable deployment processes are first verified, and counterweight asteroid capture is executed for the first time. Subsequent elevators can refer to the experience of the first, but due to the unique geological conditions of each node, simple replication is not possible.

### 8.3.2 Conservative Baseline for Elevator Construction Rate

| Elevator | Node Type | Geological Complexity | Estimated Main Construction Period | Notes |
|------|------|:--:|:--:|------|
| 1st (Brazil) | Land-based granite | Low | 8 years | First, process innovation |
| 2nd (Gabon) | Land-based gneiss | Low | 6 years | Refer to first's experience |
| 3rd (Belitung, Indonesia) | Land-based granite | Low | 6 years | Similar |
| 4th (Manta, Ecuador) | Land-based sedimentary rock | Medium | 7 years | Anchoring must adapt to sedimentary rock |
| 5th (Christmas Island) | Coral reef island | **High** | 8 years | Suction anchor inclined penetration, unique process |
| 6th (Indian Ocean Platform) | Deep-sea floating platform | **High** | 9 years | Platform construction + mooring, unique process |

The above construction periods are "from anchoring commencement to completion of full cable pre-tensioning," not including trial operation.

### 8.3.3 Four-Stage Global Construction Sequence

#### Stage 1: Technology Verification and First Elevator Construction (Years 1–10)

**Goal**: Complete asteroid capture technology verification (E-P0-5), build the first elevator (Brazil node), complete 2 years of trial operation, and achieve commercial operational capability.

| Year | Work Content | Key Constraint |
|------|------|------|
| Years 1–3 | Asteroid capture technology verification (E-P0-5); capture and tow the first counterweight asteroid to GEO+200 km; detailed geological drilling and anchoring construction at Node 1 (Macapá, Brazil) | Counterweight capture is a prerequisite for elevator construction |
| Years 4–8 | First elevator cable deployed downward from GEO (pulled by the positioned counterweight); cable material supplied by ground CNT pilot line | First, process innovation, construction period cannot be compressed |
| Years 9–10 | First elevator 2-year trial operation; cabin DM/PM deployment and commissioning | — |

**Total construction period for the first elevator: about 10 years** (including 2 years of trial operation).

#### Stage 2: Comprehensive Construction of Six Elevators (Years 5–16)

**Goal**: While constructing the first elevator, simultaneously advance surveys and anchoring construction at the remaining nodes. Complete construction and trial operation of all 6 elevators.

| Node | Anchoring Start | Cable Deployment Complete | Trial Operation Complete | Total Construction Period |
|------|:--:|:--:|:--:|:--:|
| Brazil (1st) | Year 3 | Year 8 | Year 10 | 8 years |
| Gabon (2nd) | Year 5 | Year 10 | Year 12 | 7 years |
| Belitung, Indonesia (3rd) | Year 5 | Year 10 | Year 12 | 7 years |
| Manta, Ecuador (4th) | Year 5 | Year 11 | Year 13 | 8 years |
| Christmas Island (5th) | Year 6 | Year 13 | Year 15 | 9 years |
| Indian Ocean Platform (6th) | Year 4 | Year 13 | Year 15 | 11 years |

(The Indian Ocean Platform, due to the longest construction period for the deep-sea floating platform, must start anchoring work earliest. For detailed construction plan of the deep-sea platform, see Volume 3, Section 3.3.4; the semi-submersible platform main body must be prefabricated and towed to the target sea area before Year 4.)

All 6 elevators will have commercial operational capability by **the end of Year 15**. Total annual effective capacity of 6 elevators = 6 × 5,700 ≈ 34,200 t/year.

#### Stage 3: Ring Construction and Closure (Years 13–24)

**Goal**: The main ring cable segments are mainly launched to GEO by heavy-lift rockets from the ground, while completed elevators are responsible for precision component transport and personnel rotation. The start time for ring construction is: at least 2 elevators have completed trial operation (Brazil + Gabon).

**Relation to Volume 6 "Four Stages of Ring Main Body"**: Section 6.7 of Volume 6 divides the construction process from the perspective of the ring main body's construction process into initial closure, cable addition, closure tuning, and full cable operation, focusing on the growth of the ring's linear density and tension evolution. The "Stage 3" in this volume covers all four stages of Volume 6 on the timeline, but the division in this volume is by **global construction sequence**—that is, the sequential dependencies between elevator construction, ring construction, and full cable operation. The two are complementary descriptions of the same physical process from different perspectives and are not contradictory.

The pure construction period for the ring is about 10–12 years (depending on rocket launch frequency), plus 2 years of tuning, totaling about 12–14 years.

| Stage | Year | Work Content | Corresponding to Volume 6 |
|------|------|------|:--:|
| Ring Construction Years 1–4 | Years 13–16 | Laying Brazil–Gabon arc segment (about 88,160 segments); laying Gabon–Indian Ocean arc segment | Initial closure + early cable addition |
| Ring Construction Years 5–8 | Years 17–20 | Laying Indian Ocean–Belitung arc segment; laying Brazil–Manta arc segment | Mid cable addition |
| Ring Construction Years 9–10 | Years 21–22 | Laying Manta–Christmas Island–Belitung arc segment; ring geometric closure | Late cable addition |
| Ring Tuning | Years 23–24 | Precision tuning of full ring tension uniformity; mechanical connection of elevator cables and ring | Closure tuning |

Lead-time reminder for funding availability: the heavy-launch-vehicle mass-production facilities required to support peak ring-construction launch demand in Years 13-22 (about 1,000-1,500 launches per year) must complete financing and construction in Years 8-10 (i.e., 3-5 years before ring construction begins). This schedule constraint must be incorporated into the phased investment plan in Volume 10 (economic model).

#### Stage 4: Full Cable Operation and Gradual Upgrades (From Year 25)

| Year | Work Content | Corresponding to Volume 6 |
|------|------|:--:|
| Years 25–28 | Complete remaining sub-cables and stranding (N→1,000 strands, λ=300 kg/m); install all track sleeves and racks | Full cable operation |
| From Year 29 | Full commercial operation of 6 elevators; deployment of solar power stations on the ring; gradual expansion | Expansion possibilities |


## 8.4 Overall Construction Timeline and Key Milestones

### 8.4.1 Overall Timeline

| Stage | Time | Core Events |
|------|------|------|
| **Stage 1** | Years 1–10 | First elevator (Brazil), including 2 years of trial operation |
| **Stage 2** | Years 5–16 | 5 elevators constructed in parallel, all in place by end of Year 15 |
| **Stage 3** | Years 13–24 | Ring construction and closure, including 2 years of tuning |
| **Stage 4** | From Year 25 | Full cable operation and gradual expansion |

### 8.4.2 Key Milestones

| Milestone | Time | Marker |
|--------|:--:|------|
| First elevator achieves commercial operational capability | Year 10 | Brazil node completes 2 years of trial operation |
| 2 elevators in place, ring construction starts | Year 13 | Brazil + Gabon can assist first ring arc construction |
| All 6 elevators in place | Year 15 | All 6 nodes have commercial operational capability |
| Ring geometric closure | Year 22 | Last arc segment of the full ring closed |
| Ring achieves full cable operation | Year 28 | λ=300 kg/m, N≥1000 strands |


## 8.5 Summary of Transportation Requirements

### 8.5.1 Ring Main Cable

| Item | Value | Source |
|------|------|------|
| Total ring cable mass | ≈7.96×10⁷ t | Volume 6, Section 6.4.2 |
| Single segment length/mass | 500 m / ≈150 t | Volume 6, Section 6.4.1 |
| Total number of segments | ≈530,916 segments | Ring circumference/500 m |
| Transportation method | Heavy-lift rocket launch from ground to GEO | — |
| Ring construction period (pure construction) | ≈10–12 years | This volume, Section 8.3.3 |

### 8.5.2 Elevator Cable and Counterweight

| Item | Value | Source |
|------|------|------|
| Total cable mass per elevator | ≈8.22×10⁴ t | Volume 4, Sections 4.2–4.3 |
| 6 elevators total | ≈4.93×10⁵ t | — |
| Counterweight mass per elevator | 8.0×10¹² kg | Volume 4, Section 4.5 / Volume 6, Section 6.2.3 |
| 6 elevators total | ≈4.8×10¹³ kg | — |
| Counterweight transportation method | Asteroid capture and towing | Volume 2, Section 2.5.6 |

### 8.5.3 Precision Components and Personnel

| Item | Unit Mass | Quantity | Total Mass | Transportation Method | Notes |
|------|:--:|:--:|:--:|------|------|
| DM | ≈49.3 t | ≥40 units | ≥1,972 t | **Elevator** | Precision component, cannot be roughly launched |
| PM | ≈69.4 t | ≥40 units | ≥2,776 t | **Elevator** | Same as above |
| Space Spider | ≈2.5 t | Peak 200 units | ≈500 t | Rocket + Elevator | — |
| Personnel rotation | — | ≈50 person-trips/year | — | **Elevator** | Exclusive task |
| C/SiC connectors | — | — | ≈5,000 t | Rocket + Elevator | — |

### 8.5.4 Total Transportation Requirements Table

| Category | Total Mass (t) | Transportation Method | Notes |
|------|:--:|------|------|
| Ring cable segments | ≈7.96×10⁷ | Heavy-lift rocket→GEO | About 530,000 segments |
| Elevator cable | ≈4.93×10⁵ | Heavy-lift rocket→GEO | 6 elevators |
| Counterweight | ≈4.8×10¹³ | Asteroid capture and towing | 12–18 capture missions |
| DM+PM | ≈4,750 | **Elevator** | Precision components |
| Space Spider | ≈500 | Rocket + Elevator | Peak 200 units |
| Anchoring facilities | ≈1.5×10⁶ | Sea transport + ground construction | 6 nodes |


## 8.6 Three Major Transportation Corridors

### 8.6.1 Corridor 1: Earth to GEO (Main Logistics Channel—Ring Cable Segments)

The total mass of ring cable segments is nearly 80 million tons, accounting for more than 99% of all transportation needs, and must be launched in large quantities by heavy-lift rockets from the ground.

| Parameter | Value |
|------|------|
| Peak annual launch demand | ≈8,000,000 t/year (distributed over 10 years of ring construction) |
| Single rocket LEO capacity | 150–200 t |
| Peak annual launch frequency | ≈1,000–1,500 launches/year |
| Required active rockets | ≈70–100 (15–20 reuses per year) |

This launch intensity far exceeds the current global total of space launches (about 200/year) and is the single largest logistics bottleneck of this project. **The achievability of this launch intensity—including large-scale mass production of heavy-lift rockets, reliability of 15–20 reuses per year, and coordination of the global launch site network—is further analyzed in Volume 10's industrial mobilization capability assessment.**

### 8.6.2 Corridor 2: Moon to GEO (Supplementary Logistics Channel)

According to the lunar in-situ manufacturing plan in Volume 2, Section 2.5. If lunar manufacturing undertakes 30% of the ring cable, the pressure on Earth launches can be correspondingly alleviated.

The prerequisite for lunar manufacturing is the completion of Phase 1 of the lunar base (Stage 1, about Years 5–8). The lunar corridor is listed in this volume as an "acceleration option" rather than a "baseline plan." For detailed capacity planning, see **Appendix 1: Lunar Industry**.

### 8.6.3 Corridor 3: Asteroid to GEO (Counterweight Transportation Channel)

Counterweights (8.0×10¹² kg/elevator) cannot be launched from Earth or the Moon and must be captured from C-type asteroids and towed to 200 km above GEO.

| Parameter | Value |
|------|------|
| Target asteroid | C-type, ø1.5 km, ≈3.5×10¹² kg |
| Towing vehicle | Nuclear thermal/electric propulsion space tug |
| Number of capture missions | 2–3 per elevator, total 12–18 |

The capture of the first counterweight asteroid must start in Stage 1 (Years 1–3) to ensure a counterweight is available when the first elevator cable is deployed.


## 8.7 Logistics Scheduling During Construction

### 8.7.1 LEO Distribution Orbit

Establish a **distribution hub station** in low Earth orbit (about 400 km) for temporary storage of cable segment spool rolls launched from the ground, refueling of space tugs, and transfer of personnel and spare parts. The total mass of the hub station is about 5,000–10,000 t, assembled in orbit through multiple launches.

### 8.7.2 GEO Construction Outpost

Establish a **construction outpost** at GEO (42,264 km) for deployment and maintenance of space spiders, temporary storage of cable segments, and as a communications relay during construction.

### 8.7.3 Resource Allocation During Overlap of Ring Construction and Elevator Construction

Years 13–16 are the start-up phase of ring construction and also the peak construction/trial operation period for the two most complex elevators: Christmas Island (5th) and Indian Ocean Platform (6th). The following resource conflicts exist during this overlap period:

| Resource | Conflict Point | Priority Arrangement |
|------|------|------|
| Heavy-lift rocket launch windows | Competition for launch slots between ring cable segment launches and elevator cable deployment material launches | Elevator cable has priority (must be completed within cable deployment window), ring cable segments use remaining windows |
| Space tugs | Competition for tugs between transporting ring cable segments from LEO to GEO and transporting precision components to elevator GEO terminals | Precision components have priority (higher orbital maneuver complexity, lower mass), ring cable segments use remaining tug capacity |
| GEO construction outpost berths | Competition for berths between space spider maintenance and temporary storage of ring cable segments | Space spider maintenance has priority (ensures construction continuity), cable segment storage can be flexibly adjusted |
| Personnel | Allocation between elevator trial operation teams and ring construction teams | Independent teams configured per node, avoid cross-node personnel overlap |

### 8.7.4 Fuel and Supply Logistics

| Item | Annual Demand (Peak) | Source |
|------|:--:|------|
| Liquid hydrogen/liquid oxygen (tug fuel) | ≈50,000 t | Earth launch or lunar ice electrolysis |
| Xenon (electric propulsion propellant) | ≈500 t | Earth launch |
| Astronaut rotation | About 50 person-trips/year | Elevator transport |
| Spare parts and consumables | ≈500 t/year | Earth launch + elevator transport |


## 8.8 Order-of-Magnitude Estimate of Transportation Costs

The following are conservative estimates based on current technology, accurate to 0.5 trillion yuan, for reference in Volume 10 (Economic Model).

| Item | Unit Price | Quantity | Subtotal |
|------|:--:|:--:|:--:|
| Heavy-lift rocket launch (LEO) | ¥100 million/launch | ≈15,000–18,000 launches (about 30 years) | **≈15–18 trillion yuan** |
| Space tug (including R&D) | ¥50 billion/unit | 50 units | **≈2.5 trillion yuan** |
| Fuel (liquid hydrogen/liquid oxygen) | ¥1,000/t | ≈750,000 t | **<0.1 trillion yuan** |
| Asteroid capture mission | ¥500 billion/mission | 15 missions | **≈7.5 trillion yuan** |
| Distribution hub station | ¥200 billion | 1 station | **≈0.2 trillion yuan** |
| Ground launch site expansion | ¥50 billion/site | 4 sites | **≈0.2 trillion yuan** |
| **Total transportation system** | — | — | **≈25–29 trillion yuan** |

> The above is a conservative estimate based on Earth launches. If lunar manufacturing (Appendix 1) undertakes 30% of the ring cable, the total transportation cost can be reduced to about **18–20 trillion yuan**.


## 8.9 Major Risks and Countermeasures

| Risk | Description | Level | Countermeasures |
|------|------|:--:|------|
| Launch frequency bottleneck | Peak demand for over 1,000 heavy-lift rocket launches per year, far exceeding current capacity | High | Prioritize lunar manufacturing; large-scale rocket mass production and reuse |
| First elevator construction delay | Geological or counterweight capture issues cause Brazil node to miss schedule | High | Advance multiple node surveys and construction in parallel; start counterweight capture early |
| Asteroid capture failure | Single mission fails to deliver asteroid to designated orbit | High | Configure 2–3 asteroids with redundancy per counterweight |
| **Lunar factory delay** | **Lunar CNT manufacturing not commissioned on schedule** | **Strategic risk** | **Adhere to Earth launch as the baseline plan; lunar manufacturing is only an acceleration option, and its progress is not a hard prerequisite for ring construction start.** |
| Christmas Island/Indian Ocean Platform construction period exceeds expectations | Unique geological conditions prevent simple replication of land-based schemes | High | Start detailed geological surveys early; independent construction teams work in parallel |


## 8.10 Parameter Output

| Parameter | Value | Status | Receiving Volume |
|------|------|------|:--:|
| Total construction period for first elevator | ≈10 years (including 2 years of trial operation) | Locked | — |
| All 6 elevators in place | Year 15 | Locked | — |
| Ring construction pure construction time | ≈10–12 years | Estimate | — |
| Full cable operation time for ring | Year 28 | Estimate | — |
| Total construction period | ≈28 years (to full cable operation) | Baseline | Volume 10 |
| Annual effective capacity per elevator | ≈5,700 t/year | Locked | — |
| Total annual effective capacity of 6 elevators | ≈34,200 t/year | Locked | — |
| Peak annual launch frequency | ≈1,000–1,500 launches/year | Estimate | — |
| Number of asteroid capture missions | 12–18 | Estimate | — |
| Total transportation system cost | **≈25–29 trillion yuan** | Order-of-magnitude estimate | Volume 10 |


## 8.11 Conclusion of Volume 8

Based on the physical constraints of the first five volumes, this volume corrects previous optimistic assumptions about construction cycles and elevator capacity, and proposes a global construction sequence that can withstand engineering scrutiny. Core conclusions:

1. **Elevator effective capacity is much lower than previously estimated**: Of the 200 t fully loaded cabin, only about 81.3 t is effective payload (DM+PM already account for about 118.7 t). The annual effective capacity per elevator is about 5,700 t, which can only handle precision component transport and personnel rotation, far from enough to replace rocket launches of ring cable segments.
2. **The first elevator is the biggest bottleneck**: From anchoring commencement to commercial operational capability takes about 10 years (including 2 years of trial operation). The construction period for subsequent land-based geological nodes can be shortened to 6–7 years, but coral reef (Christmas Island) and deep-sea platform (Indian Ocean) require at least 8–9 years due to their unique anchoring methods.
3. **All 6 elevators will be in place around Year 15**, with a total annual effective capacity of about 34,000 t.
4. **The pace of ring construction depends on heavy-lift rocket launch capability**: Peak annual launches exceed 1,000, making it the single largest logistics bottleneck of the project, with achievability further evaluated in Volume 10.
5. **Total global construction period is about 28 years** (to full cable operation), with total transportation cost about **25–29 trillion yuan** (spread over about 30 years).

The output parameters of this volume are sufficient to support further analysis in Volume 10 (Economic Model) and Volume 11 (Governance Framework).


## References (Index Table)

[8.1] Heavy-lift rocket capacity and cost data, refer to SpaceX Starship, China Long March 9 public technical parameters (2025).
[8.2] Asteroid capture technology verification, TransAstra Mini Bee ISS Technology Demonstration, 2025.
[8.3] Space tug nuclear thermal propulsion scheme, NASA NERVA project technical heritage and contemporary nuclear thermal propulsion research (2024).


## Appendices

- **Appendix 1: Lunar Industry** (detailed technical solution to be compiled separately)
- **Appendix 2: High Altitude Platform System** (detailed technical solution to be compiled separately)

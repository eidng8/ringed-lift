# Volume 7: Engineering Verification

**Version**: 1.4 (Final Review Edition)
**Compilation Date**: May 2026
**Currency Unit**: Renminbi (Yuan), symbol: ¥


## 7.1 Preface

This volume is positioned as the **comprehensive physical validation and experimental verification plan** for the Space Ringed-Elevation project, focusing on answering the following core questions:

> To what extent can the design schemes, physical models, and engineering parameters proposed in the previous six volumes withstand the scrutiny of full-system coupled simulation and key experiments? What fatal uncertainties remain that must be resolved through experiments, simulations, or in-orbit trial and error?

Core tasks of this volume:

1. Summarize and categorize all "items pending verification" marked in the previous six volumes, and establish a unified verification priority system.
2. Design a multi-physics full-system coupled simulation framework and key test scenarios.
3. Conduct global sensitivity analysis on core physical uncertainties to identify parameters with the greatest impact on system safety.
4. Perform failure mode and reliability assessment for the ring elevator system.
5. Develop a roadmap for ground experiments and in-orbit verification, clarifying the success criteria for each experiment.
6. Based on forward-looking predictions from simulations and experiments, provide design revision recommendations to each volume.

This volume does not cover transportation logistics planning, economic cost accounting, or international legal frameworks. For any verification items that cannot be closed at the current stage, a clear verification path and judgment criteria are provided.


## 7.2 Summary and Priority Classification of Items Pending Verification

### 7.2.1 Four-Level Priority System

The previous six volumes marked their respective "items pending verification" in various professional fields, with a dispersed numbering system. This volume unifies and summarizes them, classifying according to the following four-level criteria:

- **P0 (Highest Priority—Scheme Feasibility Criterion)**: If the result of this verification item is negative, it will directly lead to the rejection of the current recommended scheme (including the ring body, elevator cable, carriage drive, and anchoring design), or at least one of these must undergo fundamental physical scheme modification.
- **P1 (High Priority—Major Engineering Risk)**: If the result of this verification item is negative, it will cause key performance indicators to deviate significantly from design expectations (such as cable lifespan, transport speed, node reliability), requiring major technological breakthroughs to resolve, but not necessarily negating the scheme itself.
- **P2 (Medium Priority—Significant Performance Impact)**: The result of this verification item will significantly affect certain performance parameters, safety factors, or maintenance cycles, but does not alter the physical feasibility of the scheme.
- **P3 (Normal Priority—Local Design Optimization)**: The result of this verification item affects local design details, material selection, or construction processes, with limited impact on the overall scheme.

### 7.2.2 Summary of All Items Pending Verification from the Previous Six Volumes

#### Volume 1 Items Pending Verification

| Original No. | Content | Priority in This Volume |
|--------------|---------|:----------------------:|
| V1-F1 | Strict proof of n=0 mode stability | P2 |
| V1-F2 | Stability domain and critical wavelength for n≥2 modes | P2 |
| V1-F3 | Lunar perturbation inclination drift rate (N-body integration simulation) | P2 |
| V1-F4 | Closed-loop structure resonance spectrum (finite element modal analysis) | P2 |
| V1-F5 | Critical conditions for multi-strand fracture due to debris impact (Weibull reliability model) | P1 |

#### Volume 2 Items Pending Verification

| Original No. | Content | Priority in This Volume |
|--------------|---------|:----------------------:|
| **V2-M1** | **Precise measurement of f₁ (single filament → yarn strength transfer efficiency)** | **P0** |
| V2-M2 | f₂, f₃ dependence on braiding angle | P2 |
| V2-M3 | Long-term creep of cable in vacuum | P1 |
| V2-M4 | Low gravity/microgravity FCCVD process verification | P1 |
| V2-M5 | Catalyst extraction efficiency from lunar regolith | P2 |
| V2-M6 | Carbon extraction efficiency from C-type asteroids | P2 |
| **V2-M7** | **Asteroid capture and towing engineering verification** | **P0** |
| V2-M8 | Survey of CO₂ reserves in lunar polar regions | P2 |
| V2-M9 | In-situ CVD growth of CNT in lunar regolith simulant | P3 |
| V2-M10 | Verification of natural CNT formation mechanism in Chang'e-6 lunar regolith | P3 |

#### Volume 3 Items Pending Verification

| Original No. | Content | Priority in This Volume |
|--------------|---------|:----------------------:|
| V3-N1 | Detailed engineering geological drilling at each node (≥100 m) | P2 |
| **V3-N2** | **Suction anchor inclined penetration and bearing capacity in Christmas Island coral limestone** | **P0** |
| V3-N3 | Suction anchor penetration and bearing capacity in the Indian Ocean deep sea | P2 |
| V3-N4 | Inclined penetration and load transfer efficiency of composite anchors at nodes 2 and 3 | P2 |
| **V3-N5** | **Mechanical bearing and fatigue of ring-node connectors** | **P0** |
| V3-N6 | Standardized design of 6-node connectors | P3 |
| V3-N7 | Positioning accuracy and reliability of GEO-end active capture arm | P2 |
| V3-N8 | Equivalent bending fatigue life of steering pulley set under rated tension | P2 |
| V3-N9 | Reliability and reset accuracy of split-type drive wheel clamping frame opening/closing | P2 |
| V3-N10 | Positioning accuracy and lock pin reliability of carriage mechanical locking mechanism | P2 |
| V3-N11 | Synchronous docking accuracy of multi-layer gangway and multi-door carriage | P3 |

#### Volume 4 Items Pending Verification

| Original No. | Content | Priority in This Volume |
|--------------|---------|:----------------------:|
| V4-N1 | Scaled wind tunnel test of cable vortex-induced vibration | P2 |

#### Volume 5 Items Pending Verification

| Original No. | Content | Priority in This Volume |
|--------------|---------|:----------------------:|
| **V5-P0** | **Ultra-long-life aluminum alloy micro-arc oxidation coating friction and wear life** | **P0** |
| **V5-P1** | **High-power space radiation cooling technology verification for hollow section** | **P0** |
| **V5-N1** | **Aluminum alloy rack micro-arc oxide layer 10⁷ cycle contact fatigue limit** | **P0** |
| **V5-N2** | **Annual wear depth of aluminum alloy gear-rack in dry inert gas** | **P0** |
| V5-N3 | Load balancing and fault isolation for 40 pairs of gears in synchronous drive | P1 |
| V5-N4 | Vacuum deployment and cooling performance of DM deployable radiator panel | P1 |
| V5-N5 | Effectiveness of low-altitude segment sealed dry inert gas protection | P1 |
| **V5-N6** | **C/SiC conical transition section fatigue (5.23×10¹⁰ N)** | **P0** |
| V5-N7 | Spindle-shaped carriage vertical wind tunnel test | P2 |
| **V5-N8** | **Active liquid cooling verification for high-power cooling scheme (~20.8 MW) in hollow section** | **P0** |
| V5-N9 | High-altitude segment 6.3 MW radiator panel design and verification | P2 |
| V5-N24 | Joint cooling efficiency of GEO-end heat pipe network and radiator | P2 |
| V5-N25 | Vortex-induced vibration and anti-tangling of index cable in low-altitude segment | P3 |
| V5-N26 | Long-term reliability of multi-index cable synchronous tension control system | P3 |
| V5-N27 | Bending-tension coupled fatigue life of CNT braided cable | P2 |

#### Volume 6 Items Pending Verification

| Original No. | Content | Priority in This Volume |
|--------------|---------|:----------------------:|
| V6-M1 | Long-term strength attenuation of CNT braided cable stored at small radius | P2 |
| V6-M2 | Space spider microgravity precision operation accuracy | P2 |
| **V6-M3** | **Fatigue life of inter-segment C/SiC flange under repeated tension fluctuations** | **P0** |
| V6-M4 | Dynamic stability boundary of incomplete ring during construction | P2 |
| V6-M5 | Long-term bundling retention of aramid fiber tape under vacuum UV/atomic oxygen | P3 |
| V6-M6 | Collision avoidance and scheduling for multi-space-spider cooperative operation | P2 |


## 7.3 Full-System Coupled Simulation Framework

### 7.3.1 Simulation Objectives

This project involves a giant multi-flexible-body mechanical system from the Earth's surface to the GEO periphery, requiring multi-physics coupled simulation to capture interactions between subsystems. The simulation must cover the following coupled effects:

1. Coupling of orbital mechanics and structural mechanics (Volume 1 ring perturbation + Volume 6 incomplete ring during construction)
2. Aero-thermal-structural coupling (Volume 4 cable wind vibration + Volume 5 carriage low-altitude segment)
3. Contact mechanics and wear (Volume 4 rack + Volume 5 gear DM)
4. Coupling of cable longitudinal displacement and counterweight winch control (Volume 4 counterweight + thermal expansion/contraction)
5. Multi-axial fatigue at elevator cable-ring connection nodes (Volume 3 interface + Volume 4 connectors)

### 7.3.2 Key Simulation Scenarios

| Scenario No. | Description | Involved Volumes | Verification Objective | Priority |
|:---|:---|:---|:---|:---|
| **S-1** | **Full-cycle time-domain coupled simulation of ring construction (λ: 1.2→300 kg/m)** | **Volumes 1, 5, 6** | **Verify whether the active damping control law can maintain ring stability throughout the construction cycle under multi-modal coupling including in-plane (n≥2) and out-of-plane bending.** | **P0** |
| S-2 | Six elevators running at full load in full cable state | Volumes 1, 4, 5 | Ring tension fluctuation, node load | P2 |
| S-3 | Low-altitude segment 200 km/h full load headwind (85.6 m/s) | Volume 5 | Aerodynamic drag and DM tangential force margin | P2 |
| S-4 | Full journey thermal equilibrium (low altitude 200 km/h to high altitude 1,500 km/h) | Volume 5 | DM cooling feasibility | P2 |
| S-5 | Long-period lunar perturbation (10 years) ring inclination drift | Volume 1 | Thruster Δv budget | P2 |
| S-6 | Sudden breakage of single elevator cable | Volumes 1, 3, 6 | Transient response of ring tension redistribution | P1 |

### 7.3.3 Simulation Toolchain

| Physical Domain | Recommended Tools |
|-----------------|------------------|
| Multi-body dynamics and structure | Simpack / Adams / MBDyn |
| Orbital mechanics | GMAT / OreKit |
| Computational fluid dynamics | OpenFOAM / SU2 |
| Thermal analysis | Thermal Desktop / Sinda |
| Contact/wear analysis | Abaqus / Ansys |
| Debris impact probability | ESA DRAMA / NASA BUMPER |


## 7.4 Global Sensitivity Analysis

### 7.4.1 Key Uncertainty Parameters

| Parameter | Current Value | Uncertainty Range | Source |
|-----------|--------------|:----------------:|--------|
| CNT engineering strength $σ_{allow}$ | 20 GPa | 15–25 GPa | Volume 2 |
| Single filament to yarn loss factor f₁ | 0.5 (optimistic) | 0.11–0.5 | Volume 2 |
| Cable bending stiffness EI | ~1.18×10¹⁰ N·m² | ±50% | Volume 4 |
| Rack wear rate | Unknown | Orders of magnitude | Volumes 4, 5 |
| Hollow section cooling area | ≥3,000 m² | Deployment failure probability | Volume 5 (Note: 20.8 MW heat generation at 400 K panel temperature requires about 16,800 m² radiating area, ε=0.85; if panel temperature is raised to 600 K, about 4,200 m² is needed. Here ≥3,000 m² is a provisional reference value from Section 5.10.5 of Volume 5; final required area to be determined by E-P0-2 experiment combined with actual achievable panel temperature) |
| Maximum gust wind speed in low-altitude segment | 30 m/s | Up to 50 m/s | Volume 5 |
| Initial ring construction error | 0 | ±10 m/node | Volume 6 |
| Node C/SiC flange fatigue life | ≥10⁵ cycles | 10⁴–10⁶ cycles | Volume 6 |

### 7.4.2 Analysis Method

Use **Monte Carlo simulation** combined with **response surface models** for global sensitivity analysis. For output quantities such as maximum radial displacement of the ring, peak node stress, and GEO-end cable tension fluctuation, calculate the SOBOL indices for each input parameter. Based on sensitivity ranking, adjust the priority of each item pending verification (P0/P1/P2/P3), and identify parameters contributing most to system failure probability.


## 7.5 Failure Modes and Reliability Analysis

### 7.5.1 Top-Level Failure Modes

| No. | Failure Mode | Possible Consequence | Involved Volumes | Key Analysis Requirements |
|-----|--------------|---------------------|------------------|--------------------------|
| **F-1** | **Massive ring cable breakage leading to disintegration** | **Ring disintegration, mission failure** | **Volumes 1, 2, 6** | — |
| **F-1a** | **Space debris cascade impact (Kessler syndrome scenario)** | **Massive ring cable breakage, triggering full ring disintegration** | **Volumes 1, 2, 6** | **Must use worst-case debris flux model for Weibull reliability analysis and Monte Carlo simulation to assess full ring survival probability.** |
| F-2 | Elevator cable breakage | Single node failure, major economic loss | Volumes 3, 4 | — |
| F-3 | Massive rack wear/breakage | Transport interruption, long-term shutdown for repair | Volumes 4, 5 | — |
| F-4 | Hollow section cooling failure | Carriage overheating and shutdown | Volume 5 | — |
| F-5 | Counterweight drift out of control | Large cable displacement, elevator shutdown | Volumes 4, 6 | — |
| F-6 | Node anchoring failure (geological/tethering) | Single elevator collapse | Volume 3 | — |

### 7.5.2 Key Reliability Targets

| Failure Mode | Acceptable Probability (500-year design life) | Remarks |
|--------------|:--------------------------------------------:|---------|
| Ring disintegration | <10⁻⁶ | [Note 1] |
| Single elevator cable breakage | <10⁻⁴ | Single-point failure acceptable, cascading failure not acceptable [Note 2] |
| Single node C/SiC flange failure | <10⁻⁵ | [Note 3] |

> **Note 1**: Refer to NASA "General Requirements for Reliability of Critical Spacecraft Structures" (NASA-STD-5001) for failure probability requirements for permanent space infrastructure that is unrepairable and irreplaceable.
> **Note 2**: Based on the overview principle that "failure of a single elevator does not affect the integrity of the closed ring," single car failure is acceptable, but cascading reaction probability must be below 10⁻⁶.
> **Note 3**: Based on the number of about 530,000 nodes in the full ring and decomposition of the overall reliability target, to be finalized after detailed risk assessment in Volume 9.


## 7.6 Experimental Verification Plan

### 7.6.1 P0-Level Experiments (Scheme Feasibility Criteria)

**E-P0-1: Long-life wear test of aluminum alloy rack micro-arc oxidation coating**

- **Covered items pending verification**: V5-P0, V5-N1, V5-N2
- **Method**: In a vacuum chamber, conduct rolling contact fatigue tests with 1:1 rack segment + gear. Environment is dry nitrogen, simulating low-altitude inert protection conditions. Test parameters: contact stress 200 MPa, sliding speed 16.7 m/s, cycles ≥10⁷.
- **Success criteria**: Wear depth < allowable value (TBD), no large-area coating spalling, rack surface contact fatigue life ≥10⁷ cycles.

**E-P0-2: High-power active liquid cooling verification for hollow section**

- **Covered items pending verification**: V5-P1, V5-N8
- **Method**: Build a 1:1 local DM thermal model (including motor and gear simulated heat sources, total heat generation 20.8 MW) in a ground vacuum chamber, pump-driven liquid metal (e.g., NaK) loop, connected to deployable radiator panels (≥500 m², panel area can be reduced to about 4,200 m² if panel temperature is raised to 600 K; 500 m² here is the initial experimental scale, actual area to be extrapolated from results). Verify whether the liquid cooling loop can keep equipment temperature within safe working range (<150°C) under simulated heat load.
- **Success criteria**: Continuous operation ≥1 hour, all component temperatures <150°C, no leakage in the loop, radiator panel deployment and retraction function normally.

**E-P0-3: Precise measurement of CNT braided cable strength transfer efficiency (f₁ factor)**

- **Covered items pending verification**: V2-M1
- **Method**: Prepare MWCNT yarn samples (length ≥1 m), conduct comparative tensile tests of single filament and whole yarn under scanning electron microscope. Measure strength transfer efficiency under different braiding processes (twist, packing density).
- **Success criteria**: f₁ ≥ 0.3 (minimum acceptable value), target f₁ ≥ 0.5. If f₁ < 0.3, the cable strength baseline for Scheme C in Volume 5 must be re-evaluated.

**E-P0-4: Fatigue test of C/SiC conical transition section under 5.23×10¹⁰ N**

- **Covered items pending verification**: V5-N6, V3-N5
- **Method**: Manufacture 1:5 scale C/SiC conical transition section model, apply proportionally reduced cyclic load (simulating elevator cable tension fluctuation and thermal cycling), perform ≥10⁴ cycles.
- **Success criteria**: No crack initiation, bolt preload loss < 20% of initial value.

**E-P0-5: Asteroid capture and towing engineering verification**

- **Covered items pending verification**: V2-M7
- **Method**: Execute an actual near-Earth asteroid capture mission (target diameter 10–50 m), using inflatable capture bag or surface anchoring device, electric propulsion tug to tow it to a designated Earth-Moon space orbit.
- **Success criteria**: Successful capture, towing, and orbit insertion, verifying the scalability of TransAstra capture bag (1-meter class already successfully tested on ISS [2.19]) on real asteroid surfaces.

**E-P0-6: Suction anchor inclined penetration and bearing capacity in Christmas Island coral limestone**

- **Covered items pending verification**: V3-N2
- **Method**: Conduct 1:1 suction anchor sea trial in waters near Christmas Island, measure penetration resistance in coral limestone, bearing capacity under inclined penetration (~3.5°), and displacement accumulation under long-term cyclic load.
- **Success criteria**: After 3.5° inclined penetration, suction anchor bearing capacity meets design requirements (safety factor ≥2.0), displacement stable under long-term cyclic load.

**E-P0-7: Fatigue life of inter-segment C/SiC flange under repeated tension fluctuations**

- **Covered items pending verification**: V6-M3
- **Method**: Manufacture 1:1 or scaled C/SiC flange connection node model, apply periodic tension cycles in vacuum chamber (simulating tension fluctuations from thermal expansion/contraction and elevator operation), cycles ≥10⁵.
- **Success criteria**: No cracks in flange, bolt preload loss < 20% of initial value, node angle deviation < 0.05°.

**E-P0-8: 50–100 kV conductive rail system surface insulation and partial discharge test**

- **Covered items pending verification**: V5-P0, V5-N5 (supplementary)
- **Method**: In a chamber simulating 0–100 km altitude pressure variation (1 atm to near vacuum), apply 50–100 kV AC voltage to aluminum alloy conductive rail sample with UHMWPE insulation, monitor partial discharge inception voltage, surface flashover voltage, and long-term aging characteristics.
- **Success criteria**: No partial discharge at maximum working voltage (50 kV) across full pressure range; at 100 kV, only acceptable partial discharge at extremely low pressure, no flashover.

### 7.6.2 P1-Level Experiments (Major Engineering Risk Mitigation)

| Experiment No. | Covered Items Pending Verification | Brief Description |
|----------------|-----------------------------------|------------------|
| E-P1-1 | V2-M3, V1-F5 | Creep rate measurement of CNT braided cable under continuous load in vacuum for 1,000 h; scaled debris impact simulation |
| E-P1-2 | V5-N3 | 40 PMSM synchronous drive control simulation and full-power ground bench test |
| E-P1-3 | V5-N4 | DM deployable radiator panel (500 m² class) deployment/retraction reliability in vacuum chamber |
| E-P1-4 | V5-N5 | Inert gas injection and maintenance in locally sealed segment under simulated low-altitude atmosphere (with water vapor, oxygen) |
| E-P1-5 | V2-M4 | Low gravity/microgravity FCCVD process verification (lunar or space station experiment) |

### 7.6.3 In-Orbit Verification Mission

Before constructing the full-size ring, it is recommended to launch a "mini-ring" verification satellite to conduct in-orbit verification of the following technologies in low Earth orbit.

| Parameter | Value | Description |
|-----------|-------|-------------|
| Mini-ring radius | 100 m | Ring circumference about 628 m |
| Cable linear density | ≈1.2 kg/m (guide cable level) | Same as initial closed loop linear density of main ring first stage |
| Total cable mass | ≈754 kg | 628 m × 1.2 kg/m |
| Deployment orbit | LEO (400–600 km) | Easy to monitor and correct |
| Number of space spiders | 1–2 units | Scaled verification of fully autonomous braiding process |
| Launch method | Rideshare or dedicated small rocket | — |

| Verification Content | Covered Items Pending Verification |
|---------------------|-------------------------------|
| Fully autonomous braiding, movement, and connection process of space spider | V6-M2, V6-M6 |
| Distributed strain sensing and thruster station-keeping system | V1-F3 |
| Long-term vacuum/radiation/debris exposure of small-size CNT cable | V2-M3 |
| Long-term in-orbit performance of small-scale C/SiC node connections | V6-M3 |

**Supplement to Core Verification Objective—Material Long-Term Effect Experimental Module**:

A dedicated module should be set up on the mini-ring verification satellite to apply constant pre-tension to various specifications of CNT braided cable samples (with different braiding densities and protective coatings), and monitor their strain, temperature, and any signs of degradation (such as broken filaments, mass loss) in real time. This experiment aims to bridge the "cognitive gap" between short-term laboratory data and long-term engineering reality at large scale; the experimental period must cover at least one complete solar activity cycle (about 11 years).


## 7.7 Design Feedback and Revision Recommendations

Based on the above simulation framework and experimental plan predictions, this volume provides the following forward-looking revision recommendations to the previous six volumes:

### 7.7.1 Feedback to Volume 2 (Materials)

- If **E-P0-3** measures f₁ < 0.3, then the engineering target of "$σ_{cable}$ ≥ 20 GPa" in Volume 2 cannot be achieved with the current braiding process. At this point, two paths need to be evaluated: ① increase single filament strength to compensate for the loss; ② switch to Scheme E (multi-index cable, whose core issue is also CNT strength). If f₁ < 0.2, the entire cable design of the ring elevator scheme must be fundamentally re-evaluated.
- If the creep rate measured in V2-M3 exceeds expectations, the counterweight winch stroke must be increased from the current 1,000 m, or add in-orbit re-tensioning devices.

### 7.7.2 Feedback to Volume 5 (Carriage)

- If **E-P0-2** (hollow section cooling) fails verification, the 1,500 km/h high-speed operation scheme will be permanently locked out, and only the 200 km/h low-speed scheme will be retained. The one-way transport time of 50 hours will become a rigid constraint and cannot be reduced by increasing speed.
- If **E-P0-1** (rack wear) shows wear rate across orders of magnitude, it may be necessary to replace the rack material (e.g., steel rack) or permanently abandon full-speed operation, retaining only the 200 km/h low-speed scheme. This will trigger major revisions to Scheme C in Volume 5 (number of gears, DM size, cooling requirements, etc. must all be recalculated).

### 7.7.3 Feedback to Volume 6 (Construction)

- If **E-P0-7** (C/SiC flange fatigue) shows bolt preload loss exceeding expectations, the node connection scheme in Volume 6 must add extra in-orbit re-tensioning mechanisms or increase the number of bolts per node.
- If global sensitivity analysis shows that "initial ring construction error" significantly affects final ring tension uniformity, the positioning accuracy requirement for space spiders in Volume 6 must be further improved from ±0.5 mm.


## 7.8 Parameter Output

| Parameter | Value | Description |
|-----------|-------|-------------|
| **Number of P0 experiments** | **8 items** | **Rack wear, hollow section cooling, f₁ factor, C/SiC conical transition fatigue, asteroid capture, suction anchor bearing capacity, flange fatigue, high-voltage insulation** |
| Number of P1 experiments | 5 items | CNT creep/debris impact, motor synchronization, panel deployment, inert gas maintenance, microgravity CVD |
| Number of P2 experiments | About 22 items | Orbital mechanics simulation, geological drilling, anchoring efficiency, wind tunnel tests, etc. |
| Number of P3 experiments | 6 items | Standardized design, docking accuracy, sealing durability, anti-tangling, etc. |
| **P0 simulation scenario** | **1 item (S-1)** | **Full-cycle time-domain coupled simulation of ring construction** |
| **Critical failure probability for ring disintegration** | **<10⁻⁶** | **500-year design life** [Note 1] |
| Acceptable probability for single elevator cable breakage | <10⁻⁴ | 500-year design life [Note 2] |
| **Minimum acceptable f₁ value** | **≥0.3** | **Below this value, cable scheme must be re-evaluated** |
| **Hollow section cooling verification success criteria** | **Continuous 1 h, temperature <150°C** | **If failed, lock in 200 km/h low-speed scheme** |


## 7.9 Epilogue to Volume 7

This volume summarizes all items pending verification from the previous six volumes, establishes a unified **P0/P1/P2/P3** four-level priority system, and designs a full-system coupled simulation framework and experimental verification roadmap covering all key physical domains.

Core conclusions:

1. **There are about 11 P0-level items pending verification** (including 8 P0-level experiments, 1 P0-level simulation scenario, and 2 comprehensive verification items covered by both simulation and experiment), among which rack wear life (V5-P0/N1/N2), hollow section cooling (V5-P1/N8), and CNT strength transfer efficiency f₁ (V2-M1) are the three major technical bottlenecks determining whether Scheme C is viable.
2. There are about 5 P1-level items pending verification, covering major engineering risk areas such as cable creep, motor synchronization, panel deployment, inert gas maintenance, and microgravity CVD.
3. There are about 22 P2-level items pending verification, covering orbital mechanics, geological engineering, anchoring efficiency, wind tunnel tests, and space spider operation.
4. There are about 6 P3-level items pending verification, involving standardized design, docking accuracy, sealing durability, and anti-tangling local optimizations.
5. It is recommended to prioritize completion of **P0-level experiments** and the in-orbit mini-ring verification mission before starting full-size construction, to obtain reliable data on key physical parameters and support the finalization of designs in subsequent volumes.
6. **The mini-ring verification satellite must be equipped with a "material long-term effect experimental module"** to conduct in-situ exposure experiments on cable samples for at least one solar activity cycle, which is the key step to bridge the "cognitive gap" and ultimately confirm the feasibility of the full-size ring project.

# Appendix II: Stratospheric Platform

## Volume II: Energy and Positioning Systems

**Version**: 1.5<br/>
**Date of Preparation**: June 2026<br/>
**Currency Unit**: Renminbi (RMB), symbol: ¥<br/>
**Related Main Volumes**: Main Volume V, Volume IX<br/>
**Prerequisite Reading**: Volume I of this Appendix


### Glossary of Abbreviations

| Abbreviation | Full Name | Notes |
|------|----------|------|
| AM0 | Air Mass Zero | Air Mass Zero; extraterrestrial solar spectral standard |
| CFD | Computational Fluid Dynamics | Used for aerodynamic-thermal coupled simulation of propellers and heat dissipation panels |
| FOG | Fiber-Optic Gyroscope | Core angular rate sensor for inertial navigation systems |
| GPS | Global Positioning System | Used for horizontal positioning of the platform (available below 40 km only) |
| HAPS | High Altitude Pseudo-Satellite | The internationally accepted designation for stratospheric platforms |
| MLI | Multi-Layer Insulation | Used for passive thermal control of battery compartments and electronics bays |
| MoS₂ | Molybdenum Disulfide | Solid lubricant for moving parts in high-altitude low-pressure environments |
| MPPT | Maximum Power Point Tracking | Power optimization control for photovoltaic arrays |
| RFC | Regenerative Fuel Cell | Used for nighttime power supply and buoyant gas replenishment for the platform |
| UHMWPE | Ultra-High Molecular Weight Polyethylene | Protective and insulating outer layer of tether cables |


### 2.1 Volume Preamble

This volume is positioned as the **energy supply and navigation positioning infrastructure** for the stratospheric platform system, focused on answering the following core questions:

> For a high-altitude platform that must continuously reside at altitudes of 20–50 km for more than 6 months, equipped with a photovoltaic array of approximately 5,200 kW peak power, how can uninterrupted power supply be maintained through day-night cycles? What energy storage means can fill the approximately 14-hour energy gap at night? How does the operational gondola obtain power when moving along the tether cable? Can laser power transmission serve as a supplementary ground-to-platform power supply? At altitudes above 40 km where GPS is unavailable, how do the platform and gondola know their location and attitude? Can the combination of fiber-optic gyroscopes and cable markers achieve centimeter-level positioning accuracy?

This volume builds upon:
- **Volume I (Platform Overall Design)**: The aerostat design total mass of 5,000 kg (including 15% design margin), photovoltaic array area of 8,500 m², gondola empty mass of 500 kg, winch power of 25 kW (peak), propulsion system peak electrical power of 7,290 kW (30 m/s wind conditions), electric propeller auxiliary lift power of 4–6.3 MW (at 50 km altitude), and RFC-assisted pressure maintenance scheme, among other key parameters, have been established. This volume provides detailed energy balance calculations and system design for all of the above equipment.

Core tasks of this volume:

1. Design the photovoltaic array layout for the aerostat. Based on AM0 standard solar spectrum (1,361 W/m²) and multi-junction gallium arsenide cell efficiency (target 45%), provide full-weather output curves and day-night energy balance schemes for the photovoltaic array in the 20–50 km altitude range.
2. Design the energy storage system — excess daytime photovoltaic power is stored via lithium-ion battery banks (short-term peak shaving) and regenerative fuel cells (long-duration overnight storage), with nighttime power supplied by RFC. Provide order-of-magnitude estimates of storage capacity, mass, and charge/discharge efficiency.
3. Evaluate the feasibility of laser power transmission as a supplementary ground-to-platform power supply — transmitting energy from a ground laser station to the platform's receiving panels to provide emergency power during adverse weather or insufficient photovoltaic output.
4. Design the gondola power supply scheme — drawing power from the aerostat's main battery via **embedded copper conductors in the tether cable** when moving along the tether cable, and relying on its own battery when operating independently after detaching from the tether cable.
5. Plan the platform's energy management and distribution system — MPPT photovoltaic controllers, bus voltage regulation, load priority sequencing, and fault isolation strategies.
6. Design the platform's navigation and positioning system — a multi-sensor fusion scheme combining fiber-optic gyroscope inertial navigation, cable laser-reflective markers, barometric altimeters, and GPS/BeiDou (below 40 km), with positioning accuracy estimates for the full altitude range. Evaluate the independent operating accuracy of the positioning system under high-altitude no-GPS conditions.
7. Output key parameters for use by Volume III (Maintenance and Repair), Volume IV (Experimental R&D), and Volume X (Technical Interfaces).


### 2.2 Flexible Thin-Film Solar Cell Array

**(a) Array Configuration Principles**

The aerostat's photovoltaic array is deployed on the upper surface of the hull, with a total area of 8,500 m². At the regular operating altitude range of 25–35 km, the AM0 solar irradiance is 1,361 W/m² [1], with no atmospheric attenuation, no cloud cover, and no day-night alternation (the platform can maintain long-duration sunlight by adjusting its residence longitude within the equatorial stratospheric quasi-zero-wind layer; however, in actual operation the platform will still experience Earth shadow periods and must be equipped with an energy storage system). The array uses flexible thin-film multi-junction gallium arsenide (GaInP/GaAs/Ge) cells with a long-term target efficiency of 45% [2][3] and a fill factor of 0.85.

The unit-area electrical power of the photovoltaic array is determined jointly by the photovoltaic cell efficiency and the fill factor:

$$
P_A = S_0 \times \text{FF} \times \eta_{\text{PV}} = 1,361 \times 0.85 \times 0.45 \approx 520.6  \text{W/m}^2
$$

The total peak power of the array (nominal undegraded value) is given by the unit-area power and the array area:

$$
P_{\text{PV,peak}} = P_A \times A_{\text{PV}} = 520.6 \times 8,500 \approx 4.425 \times 10^6  \text{W} \approx 4,430  \text{kW}
$$

The above expression gives the peak power of the photovoltaic array under factory nominal conditions. During actual operation, photovoltaic panels undergo efficiency degradation after prolonged exposure to stratospheric UV radiation, temperature cycling, and trace high-energy particles. This scheme applies the following two degradation margins:

- **Encapsulation efficiency** (packaging loss from cell to actual output): taken as 0.95, i.e., nominal efficiency multiplied by 0.95.
- **Degradation margin** (efficiency decay after long-term operation): taken as 10%, i.e., the final output power multiplied by 1.10 to ensure design requirements are still met over the full service life.

Applying encapsulation efficiency and degradation margin corrections to the undegraded nominal value:

$$
P_{\text{PV,design}} = P_{\text{PV,peak}} \times \eta_{\text{encap}} \times (1 + \delta_{\text{deg}}) = 4,430 \times 0.95 \times 1.10 \approx 4,630 \times 1.10 \approx 5,200  \text{kW}
$$

where $\eta_{\text{encap}} = 0.95$ is the encapsulation efficiency and $\delta_{\text{deg}} = 0.10$ is the degradation margin. 5,200 kW is the design value after margin corrections, consistent with the parameter output table in Section 1.7 of Volume I. This design value already covers the efficiency decay expected from UV aging, temperature cycling, and trace high-energy particle irradiation over the 10-year operational life of the photovoltaic panels — based on existing aging research data for stratospheric airship skin materials [20], performance degradation of laminate materials after 700 hours of accelerated artificial aging is minimal, and efficiency decay after 10 years of natural aging is expected to be within 10%.

**(b) Key Technical Requirements**

- **Cell type**: Multi-junction gallium arsenide (GaInP/GaAs/Ge) flexible thin-film cells; long-term AM0 efficiency ≥45% [2].
- **Areal density**: Areal density including flexible substrate and wiring ≤0.14 kg/m².
- **Dust removal**: Electric curtain dust removal system (sharing dust removal technology with Appendix I, Volume III heliostats), using traveling-wave electric fields to "sweep away" deposited lunar dust or high-altitude ice crystals from the surface, without reliance on mechanical action or liquid cleaning [4].
- **Deployment method**: Roll-up launch → ground deployment testing → automatic deployment after ascending with the airship (completed by internal deployment mechanism of the airship).


### 2.3 Laser/Microwave Power Transmission Receiving System

**(a) Positioning of the Power Transmission Scheme**

Laser power transmission serves as an **emergency supplementary power supply** for the stratospheric platform, not as the primary daily power source. It is activated in the following scenarios:

- Consecutive days of adverse weather (high-altitude ice crystal clouds) causing a significant drop in photovoltaic output
- Energy storage system failure or capacity decay beyond expectations
- The platform needs to perform high-power tasks (such as electric propeller auxiliary lift hovering at 50 km altitude) while photovoltaic and storage are insufficient to simultaneously support them

**(b) Laser Power Transmission Link**

Infrared laser light (wavelength approximately 1.06 μm, ytterbium-doped fiber laser) is transmitted from a ground laser station (sited in a suitable flat area with favorable natural conditions) to receiving panels on the underside of the platform [5][6]. The link efficiency consists of the following stages:

| Stage | Symbol | Efficiency | Notes |
|:---|:---:|:---:|:---|
| Ground laser electrical-to-optical conversion | $\eta_{\text{laser}}$ | 40% | Ytterbium-doped fiber laser; current commercial level approximately 35%–40% [5] |
| Atmospheric transmittance (20–50 km slant path) | $\eta_{\text{atm}}$ | 85% | 1.06 μm band, stratospheric aerosol and trace water vapor absorption [6] |
| Receiving panel photovoltaic conversion | $\eta_{\text{PV,recv}}$ | 50% | Multi-junction gallium arsenide cells, optimized for 1.06 μm monochromatic light [2] |
| End-to-end efficiency | $\eta_{\text{total}}$ | **≈17%** | $0.40 \times 0.85 \times 0.50$ |

Using 1 MW ground laser electrical power as the baseline, the platform receives approximately 170 kW of electrical power. If the platform propulsion system needs to be supported (approximately 7,290 kW under 30 m/s wind conditions), a single laser station at this power level is completely unrealistic — approximately 43 MW of ground laser electrical power would be required, which is neither technically nor economically feasible. Therefore, laser power transmission is only used for emergency supplementary power and low-power task scenarios.

**(c) Microwave Power Transmission as an Alternative**

The end-to-end efficiency of microwave power transmission (5.8 GHz ISM band) is approximately 48% (sharing technology with the ring-to-ground power transmission link of the Main Volume IX, Section 9.3.1 space solar power station [7]); however, its transmit and receive antennas are far larger than the laser scheme, and there are risks of electromagnetic interference with stratospheric aircraft and communication equipment. Microwave power transmission is only activated when the platform requires continuous high-power supply (such as sustained multi-day operation of propeller-assisted hovering at 50 km altitude) and ground laser station power is insufficient, serving as a supplement to laser power transmission.


### 2.4 Energy Storage System

**(a) Energy Storage Requirements Analysis**

The stratospheric platform does not remain in sunlight at all times at its regular operating altitude range of 25–35 km — as the platform orbits Earth, it experiences approximately 12 hours of sunlight and 12 hours of Earth shadow per 24 hours (the exact ratio depends on the platform's residence longitude and season). The energy storage system must cover all of the following loads during the Earth shadow period:

| Load Type | Power (kW) | Operating Duration in Earth Shadow (h) | Energy Consumption (kWh) |
|:---|:---:|:---:|:---:|
| Communication system (Ka/Ku antenna + fiber interface) | 2 | 12 | 24 |
| Payload equipment bay (including maintenance supplies warehouse temperature control) | 5 | 12 | 60 |
| Thermal control system (radiant cooling panel circulation pump + heat pipe network) | 10 | 12 | 120 |
| Helium management system (valves + air compressor intermittent operation) | 3 | 12 | 36 |
| Winch (work gondola routine inspection, intermittent operation) | 5 (average) | 12 | 60 |
| Control system and sensors | 2 | 12 | 24 |
| Propulsion system (position-keeping, Accuracy Level C intermittent correction) | 11.3 (average) | 12 | 135 |
| **Total** | **≈38.3** | — | **≈459** |

Note: The propulsion system operates at Accuracy Level C at night — most of the time wind speed is <20 m/s and the propulsion system is dormant, only activating corrections when offset exceeds the limit. Nighttime average wind speed is taken as 10 m/s; each correction takes approximately 10 minutes; corrections occur once every 4 hours; actual nighttime propulsion time is only approximately 30 minutes (3 corrections total). At 10 m/s wind speed, propulsion electrical power is approximately 270 kW; nighttime average power = 270 kW × 0.5 h / 12 h ≈ 11.3 kW; energy consumption approximately 135 kWh. This is consistent with the definition of Accuracy Level C in Section 1.6(b) of Volume I. Electric propeller auxiliary lift is not activated at night.

**(b) Lithium-Ion Battery Bank (Short-Term Peak Shaving)**

- **Capacity**: 100 kWh
- **Mass**: approximately 400 kg (at energy density 250 Wh/kg) [8]
- **Purpose**: Covers short-term fluctuations in daytime photovoltaic output, supplements propulsion system peak power, and supplies nighttime base loads
- **Cycle life**: ≥10,000 cycles (solid-state lithium batteries, 80% depth of discharge)
- **Thermal control**: Battery compartment thermally insulated with MLI, supplemented by electric heaters maintaining cell temperature >0°C (at high-altitude −80°C environments, battery capacity will drop sharply; active thermal management is mandatory)
- **RFC interface**: RFC system interface is reserved but not yet deployed (mass is prohibitive). Nighttime power supply is carried entirely by the lithium-ion battery bank.

**(c) Regenerative Fuel Cell (Long-Duration Overnight Storage)**

> This subsection is provided as a long-term scheme reference and is separate from the current scheme choices in Sections 2.4(b) and 2.4(f) (100 kWh lithium-ion battery bank operating independently, with RFC interface reserved but not deployed).

RFC serves as a backup and supplementary means for nighttime power supply, activated when battery capacity degrades or nighttime loads exceed expectations. Excess daytime photovoltaic power is used to produce hydrogen by water electrolysis (efficiency approximately 70% [9]); at night, the hydrogen fuel cell generates electricity (efficiency approximately 55%) to supplement power supply. RFC round-trip efficiency is approximately 38.5%.

- **Storage capacity (electrical equivalent)**: 1,500 kWh
- **Hydrogen storage method**: Liquid hydrogen (density approximately 71 kg/m³, with MLI-insulated tank) [10]
- **Liquid hydrogen mass**: approximately 40 kg (corresponding to 1,500 kWh electrical equivalent; hydrogen lower heating value approximately 33.3 kWh/kg; fuel cell efficiency 55%)
- **Total hydrogen storage system mass (including tank and MLI insulation)**: approximately 800 kg (tank mass is approximately 20 times the stored hydrogen mass; taken as 20×40 = 800 kg)
- **Electrolyzer + fuel cell module mass**: approximately 400 kg [11]
- **Total RFC system mass**: approximately 1,200 kg
- **Purpose**: Long-duration backup for nighttime power; supplement after battery capacity degradation

Daytime photovoltaic peak power is approximately 5,200 kW. After deducting platform operating loads (propulsion system, communications, gondola, etc.; daytime average power depends on wind speed — approximately 2,160 kW at wind speed 20 m/s under Accuracy Level B conditions, and only approximately 270 kW at wind speed 10 m/s), all remaining power is used for hydrogen production by electrolysis. Sufficient hydrogen fuel to cover nighttime requirements can be produced within the approximately 8–10 hour daylight window.

**(d) Total Energy Storage Mass and Lift Feasibility**

Total energy storage system mass = lithium-ion battery 6,000 kg + RFC system 1,200 kg = 7,200 kg. This mass far exceeds the energy storage budget of only 400 kg within the aerostat's 5,000 kg design total mass (as noted in the fixed load table in Section 1.3 of Volume I), meaning the photovoltaic + lithium-ion battery + RFC scheme is completely infeasible under the 5,000 kg total mass constraint — the energy storage system alone already exceeds the entire lifting capacity of the airship.

**(e) The Nature of the Mass Contradiction and Resolution Pathways**

This contradiction is a well-known core engineering challenge in stratospheric airship design. The only technology pathway currently demonstrated internationally for 24/7 continuous flight is lightweight lithium-ion batteries + photovoltaics (such as the 24-hour stratospheric continuous flight completed by Sceye HAPS in 2024 [12]); its airship total mass is approximately 2,000–3,000 kg, battery capacity approximately 100–200 kWh, sufficient only to cover nighttime baseline communication and thermal control loads, and unable to support nighttime operation of a high-power propulsion system. Although the RFC scheme has been modeled and validated in the Stratobus design (theoretically extending endurance to 118.2 days), it was only used at a 25.5% auxiliary ratio to supplement buoyancy losses from helium leakage — it was not intended as an independent overnight primary power source. Engineering data on lightweight high-altitude RFC systems remains limited [11].

The structural contradiction faced by this platform is: the propulsion system requires 7,290 kW under 30 m/s wind conditions, while the mass budget available for energy storage under the 5,000 kg total mass constraint is approximately 400 kg (see the fixed load mass table in Section 1.3 of Volume I), equating to only about 100 kWh of capacity — this is one to two orders of magnitude short of the 1,500 kWh overnight storage requirement and the 7,200 kg total mass requirement.

There are three feasible resolution pathways:

**Pathway 1 (Recommended)**: Before the anchoring problem is solved, accept Accuracy Level B or C. At night, only maintain minimum communication and thermal control loads (approximately 20–30 kW average power); 12-hour total energy consumption approximately 240–360 kWh. A pure lithium-ion battery bank of 400 kg/100 kWh within the mass constraint can satisfy approximately 1/3 of the minimum nighttime load. The remaining shortfall is addressed by:
- Optimizing nighttime task scheduling: propulsion system only activates when absolutely necessary (large offset exceeded), otherwise dormant
- Platform reduces residence altitude to 20–25 km at night (wind speeds typically lower, offsets smaller)
- Accepting larger nighttime position offset (Accuracy Level C, 10 km)

**Pathway 2**: After a CNT engineering strength breakthrough, the airship total mass is increased to 11,000 kg (near-to-mid-term feasible upper limit; see Section 1.3(f) of Volume I), and the energy storage system mass budget can be expanded to approximately 2,000 kg (500 kWh of batteries), covering all minimum nighttime load requirements. However, this pathway is premised on concurrent breakthroughs in CNT tether cable and skin materials.

**Pathway 3**: After the ground anchoring problem is solved, power is supplied directly from the ground grid through large cross-section copper conductors embedded in the tether cable, and the photovoltaic + storage system switches to backup. At this point the platform is no longer constrained by self-mass for energy storage and can operate the propulsion system 24/7, achieving precision hovering at Accuracy Level A. Taking a 30 km residence altitude, 25 km cable length, platform peak demand of 7,290 kW, and ±100 kV DC transmission voltage (direct current, bipolar symmetric, each pole carrying half the power): single-pole transmission power approximately 3,645 kW, current approximately 36.5 A. Copper conductor cross-section approximately 500 mm², linear density approximately 4.45 kg/km, total bipolar mass approximately 223 kg (25 km length). This mass is fully acceptable under the airship's 5,000 kg total mass constraint. This is the ultimate energy solution for the stratospheric platform system under anchored conditions, but it cannot be relied upon during the independent deployment phase before the anchoring problem is solved.

**(f) Energy Storage Scheme Selection for This Volume**

Based on the above analysis, this volume designs the energy storage system following Pathway 1: lithium-ion battery bank 400 kg/100 kWh (already included in the fixed load mass allocation table in Section 1.3 of Volume I), serving as short-term supplement for minimum nighttime loads and daytime propulsion system peak power. RFC system interface is reserved but not deployed (mass is prohibitive). Nighttime position-keeping accuracy is Accuracy Level C (10 km offset); daytime is Accuracy Level B (5 km offset). Platform nighttime operating strategy is minimum load mode — communication system maintains minimum bandwidth, propulsion system dormant, gondola docked inside the aerostat, only thermal control and control system operating continuously.

All subsequent power and energy consumption calculations use the 100 kWh/400 kg lithium-ion battery bank as the baseline. The parameter output table in Section 1.7 of Volume I and all cross-volume references are unified accordingly.


### 2.5 Gondola Power Supply Scheme

When the work gondola moves along the tether cable, it draws power from the aerostat's main battery via **copper conductors embedded in the tether cable**. The winch transmits power simultaneously while releasing or retracting the cable — the conductors are woven along the cable between the load-bearing layer and the UHMWPE sheath, with a cross-section of ≥10 mm² (copper conductor); the resistance over a 50 km length is approximately 85 Ω. The gondola's average power requirement is approximately 5 kW; transmission voltage is 1 kV DC; current approximately 5 A; transmission loss approximately 2.1 kW; efficiency approximately 70%.

The winch transmits power simultaneously while releasing or retracting the cable — the wound sections of the cable on the drum are connected to the aerostat's internal grid via slip rings [13]. When the gondola detaches from the aerostat's tether cable to independently perform short-duration tasks, it relies on its own lithium-ion battery (capacity approximately 50 kWh, mass approximately 200 kg, already included in the gondola's 500 kg empty mass), with an endurance of approximately 6–10 hours.

> Note: The tether cable linear density estimate in Section 1.5(e) of Volume I only accounts for the CNT load-bearing layer and UHMWPE sheath. If the copper conductor (cross-section 10 mm², linear density approximately 0.089 kg/m) and optical fiber (linear density approximately 0.005 kg/m) are included, the single-cable linear density will increase from approximately 0.06 kg/m to approximately 0.154 kg/m (an increase of approximately 157%). The 25 km single-cable mass will increase from approximately 1,500 kg to approximately 3,850 kg, and the total mass of four cables will increase from approximately 6,000 kg to approximately 15,400 kg. After accounting for copper conductors and optical fibers, the mass feasibility boundary of the tether cable scheme will tighten from CNT ≥20 GPa to an even higher strength requirement.


### 2.6 Navigation and Positioning System

**(a) Multi-Sensor Fusion Positioning Architecture**

The stratospheric platform and work gondola need to obtain their own three-dimensional position, velocity, and attitude information across the 0–50 km altitude range. The positioning system adopts the following multi-sensor fusion architecture:

| Sensor | Accuracy | Applicable Altitude | Notes |
|:---|:---|:---|:---|
| GPS/BeiDou receiver | ±5 m (horizontal), ±10 m (vertical) | 0–40 km | Only available below the GPS/BeiDou satellite constellation (satellite orbit approximately 20,200 km); signal attenuates sharply above 40 km [14] |
| Barometric altimeter | ±50 m | Full altitude range | Altitude derived from atmospheric pressure measurement. Accuracy decreases to approximately ±100 m above 30 km where pressure is extremely low |
| Fiber-optic gyroscope (FOG) inertial navigation system | 0.01°/h (angular rate random walk), ±1 km/h (position drift) [15] | Full altitude range | Provides continuous three-axis angular rate and acceleration data; however, position error in pure inertial navigation accumulates over time |
| Tether cable laser-reflective markers | ±1 mm (altitude) | 20–50 km (cable deployed segment) | Full-reflection markers placed every 100 m along the cable; laser rangefinder on gondola reads distance with millimeter-level accuracy |
| Star tracker | ±1″ (attitude) [16] | Full altitude range | Determines platform attitude by identifying star positions; serves as attitude calibration source for inertial navigation at high altitudes without GPS |

**(b) Full-Altitude Positioning Accuracy Estimates**

**Below 40 km (GPS/BeiDou available)**: GPS/BeiDou provides absolute position reference; FOG inertial navigation provides continuous position and attitude data between GPS updates (typically 1 Hz). Combined navigation accuracy ±5 m, meeting Accuracy Level A requirements.

**40 km to 50 km (GPS unavailable, cable markers available)**: When the gondola moves along the tether cable, laser-reflective markers provide millimeter-level altitude accuracy. FOG inertial navigation provides continuous horizontal position and attitude data, but horizontal position error accumulates over time (approximately 1 km/h) [15]. The platform operates at Accuracy Level B (5 km offset) above 40 km; inertial navigation accumulates only 1 km error per hour, well within the 5 km offset tolerance.

**Above 50 km (GPS unavailable, cable markers unavailable)**: FOG inertial navigation operates independently; position error continues to accumulate. Star tracker provides attitude calibration; barometric altimeter provides rough altitude estimate. This altitude range is only used by the heavy climbing gondola for short-duration tasks, typically not exceeding several hours; inertial navigation accumulated error is within acceptable range.


### 2.7 Energy Management and Distribution

**(a) Bus Voltage and Topology**

The aerostat's internal grid adopts a **±10 kV DC ring bus** topology, consistent with the underground main grid voltage level in Section 3.4.1 of Appendix I, Volume III. MPPT controllers for each photovoltaic array sector step up the low-voltage DC to ±10 kV DC before connecting to the bus. The lithium-ion battery bank is connected to the bus via a bidirectional DC/DC converter. Each electrical load (propulsion system, communication system, thermal control system, winch, etc.) draws power from the bus through solid-state transformers, converting to the required voltage level for each.

The topology and operating principles of the solid-state transformer are detailed in Section 3.4.2 of Appendix I, Volume III, using SiC power devices and epoxy resin encapsulation to accommodate lunar surface vacuum/stratospheric low-pressure environments [17].

**(b) Load Priority Sequencing**

When photovoltaic output is insufficient or energy storage system capacity is critical, the energy management system automatically sheds loads in the following priority order:

| Priority | Load | Notes |
|:---:|:---|:---|
| 1 | Thermal control system (airship gas cell temperature maintenance) | Prevents helium over-expansion/contraction causing loss of airship control |
| 2 | Control system and communications (minimum bandwidth) | Maintains basic airship control and telemetry link |
| 3 | Propulsion system (Accuracy Level C minimum power) | Prevents complete loss of airship control under extreme wind conditions |
| 4 | Payload equipment bay (temperature maintenance only; experimental equipment powered off) | Protects equipment from cryogenic damage |
| 5 | Work gondola (docked inside aerostat; battery thermal management only) | Gondola hibernates when not on task |
| 6 | Helium management system (gas replenishment off; monitoring only) | Short-term operation without replenishment is acceptable |

**(c) Fault Isolation and Protection**

When a short circuit or ground fault occurs on any feeder section of the ±10 kV DC ring bus, relays isolate the fault section in <10 ms and complete network reconfiguration in <100 ms. The energy storage system (lithium-ion battery) is equipped with triple protection: anti-reverse diode + remotely controlled DC circuit breaker + manual isolation switch [18]. High-power variable-frequency drive equipment such as the propulsion system and winch are equipped with EMI filters to prevent harmonic interference with communication and navigation systems.


### 2.8 Parameter Outputs

| Parameter | Value | Status | Receiving Volume |
|:---|:---|:---|:---|
| Photovoltaic array area | 8,500 m² | Design baseline | Volume I |
| Photovoltaic cell type | Multi-junction gallium arsenide (GaInP/GaAs/Ge) flexible thin-film | Design baseline | — |
| Photovoltaic peak power (undegraded nominal value) | ≈4,430 kW | Design baseline | — |
| Photovoltaic peak power (design value including degradation margin) | ≈5,200 kW | Design baseline | Volume I |
| Photovoltaic degradation margin | Encapsulation efficiency 0.95 + degradation margin 10% | Design baseline | — |
| Photovoltaic areal density (including substrate and wiring) | ≤0.14 kg/m² | Design target | — |
| Photovoltaic dust removal method | Electric curtain dust removal (sharing technology with Appendix I, Volume III) [4] | Design baseline | — |
| Laser power transmission end-to-end efficiency | ≈17% | Order-of-magnitude estimate | — |
| Laser power transmission received power (1 MW ground emission) | ≈170 kW | Order-of-magnitude estimate | — |
| Laser power transmission applicable scenarios | Emergency supplementary power, low-power tasks (not primary power source) | Design principle | — |
| Lithium-ion battery capacity | 100 kWh | Design baseline | Volume I |
| Lithium-ion battery mass | 400 kg | Design baseline | Volume I |
| RFC system status | Interface reserved; not deployed (mass prohibitive) | Design principle | — |
| Nighttime minimum load energy consumption | ≈459 kWh (12 h) | Design baseline | — |
| Nighttime position-keeping accuracy | Accuracy Level C (10 km offset) | Design baseline | — |
| Daytime position-keeping accuracy | Accuracy Level B (5 km offset) | Design baseline | Volume I |
| Ground anchored power supply voltage | ±100 kV DC | Long-term alternative | — |
| Ground anchored power supply single-pole current | approximately 36.5 A | Long-term alternative | — |
| Ground anchored power supply copper conductor cross-section | approximately 500 mm² | Long-term alternative | — |
| Gondola tethered power supply method | Copper conductors embedded in tether cable (1 kV DC) | Design baseline | — |
| Gondola tethered power supply efficiency | ≈70% (50 km cable length) | Design baseline | — |
| Gondola independent battery capacity | 50 kWh | Design baseline | Volume I |
| Gondola independent endurance | 6–10 h | Design baseline | Volume I |
| Aerostat internal bus voltage | ±10 kV DC | Design baseline | Volume X |
| Positioning accuracy below 40 km | ±5 m (GPS/BeiDou + FOG combined) | Design baseline | — |
| Positioning accuracy above 40 km | ±1 mm (altitude) / ±1 km/h (horizontal drift) | Design baseline | — |
| Positioning accuracy above 50 km | ±1 km/h (pure FOG) + star tracker attitude calibration | Design baseline | — |


### 2.9 Volume II Conclusion

This volume has completed the preliminary design of the stratospheric platform's energy and positioning systems. Core conclusions:

1. **Photovoltaics + energy storage is the only feasible primary power source scheme during the platform's independent deployment phase**. The 8,500 m² photovoltaic array (peak approximately 5,200 kW including degradation margin) can cover all power demands of the propulsion system, communications, and gondola during daylight. The 100 kWh lithium-ion battery bank (400 kg) under the 5,000 kg total mass constraint can only cover nighttime minimum loads (communication + thermal control + control + propulsion system intermittent corrections, totaling approximately 38.3 kW/459 kWh), with the propulsion system operating intermittently at Accuracy Level C. Therefore, the platform's nighttime position-keeping accuracy must be reduced to Accuracy Level C (10 km offset), with the propulsion system only activating when absolutely necessary.

2. **The contradiction between energy storage system mass and airship lift capacity is the core engineering bottleneck of this platform**. With a total mass of 5,000 kg, the mass budget available for energy storage is only approximately 400 kg (100 kWh). The thousands-of-kilograms-scale lithium-ion batteries or RFC systems required for long-duration overnight storage are completely infeasible under current and near-to-mid-term mass constraints. Resolution pathways are: (a) accept nighttime accuracy degradation before the anchoring problem is solved; (b) after CNT material breakthrough, airship total mass increases to 11,000 kg with correspondingly expanded energy storage budget; (c) after the anchoring problem is solved, direct power supply from the ground grid through tether cable embedded conductors (±100 kV DC), completely removing energy storage capacity constraints.

3. **Laser power transmission is an emergency supplement, not a primary power source**. An end-to-end efficiency of approximately 17% means supporting the platform's propulsion system would require tens-of-megawatts-scale ground lasers — completely unrealistic. Laser power transmission is only suitable for brief supplementary power during severely insufficient photovoltaic output and low-power task scenarios.

4. **The platform positioning system adopts different accuracy strategies below and above 40 km**. GPS/BeiDou + FOG combination achieves ±5 m accuracy below 40 km. Above 40 km, GPS signals are unavailable; FOG inertial navigation accumulated horizontal drift (approximately 1 km/h) is acceptable given the 5 km offset tolerance of Accuracy Level B. Laser-reflective markers on the tether cable provide millimeter-level altitude accuracy, meeting the precise operation requirements of the gondola.


### References

[1] ASTM International. *ASTM E490-00a(2019) – Standard Solar Constant and Zero Air Mass Solar Spectral Irradiance Tables*. 2019.

[2] NREL. Best Research-Cell Efficiency Chart. 2025. https://www.nrel.gov/pv/cell-efficiency.html

[3] Yamaguchi, M., et al. Super-high-efficiency III-V tandem and multijunction cells. *Progress in Photovoltaics*, 2014.

[4] Kawamoto, H., & Shibata, T. Electrostatic cleaning system for removing dust adhering to solar panels on a planetary base. *Journal of Electrostatics*, Vol. 73, 2015, pp. 54–60.

[5] Richardson, D. J., Nilsson, J., & Clarkson, W. A. High power fiber lasers: current status and future perspectives. *Journal of the Optical Society of America B*, 2010, 27(11): B63-B92.

[6] Sprangle, P., Hafizi, B., Ting, A., & Fischer, R. High-power lasers for directed-energy applications. *Applied Optics*, 2015, 54(31): F201-F209.

[7] Sasaki, S., Tanaka, K., & Maki, K. Microwave power transmission technologies for solar power satellites. *Proceedings of the IEEE*, 2013, 101(6): 1438-1447.

[8] NREL. Cost and Performance of Lithium-Ion Batteries for Stationary Storage Applications. 2024.

[9] Ursúa, A., Gandía, L. M., & Sanchis, P. Hydrogen production from water electrolysis: current status and future trends. *Proceedings of the IEEE*, 2012, 100(2): 410-426.

[10] Klell, M. Storage of hydrogen in the pure form. In: *Handbook of Hydrogen Energy*, 2014.

[11] Extending the flight endurance of stratospheric airships using regenerative fuel cells-assisted pressure maintenance. *Renewable Energy*, 2024, 227: 120470.

[12] Sceye. Sceye completes 24-hour stratospheric flight using solar+storage. *EEPOWER*, 2024-09-06.

[13] Application of slip power transmission technology on steel cables. *Journal World* [Chinese academic database].

[14] Yang, J., Wang, X., Shen, L., & Chen, D. Availability analysis of GNSS signals above GNSSs constellation. *The Journal of Navigation*, 2020.

[15] Lefèvre, H. C. The fiber-optic gyroscope: Challenges to become the standard for inertial navigation. *Optical Fiber Technology*, 2014, 20(6): 578-594.

[16] Liebe, C. C. Accuracy performance of star trackers – a tutorial. *IEEE Transactions on Aerospace and Electronic Systems*, 2002, 38(2): 587-599.

[17] She, X., Huang, A. Q., & Burgos, R. Review of solid-state transformer technologies and their application in power distribution systems. *IEEE Journal of Emerging and Selected Topics in Power Electronics*, 2013, 1(3): 186-198.

[18] IEEE. *IEEE Std 242-2001 – IEEE Recommended Practice for Protection and Coordination of Industrial and Commercial Power Systems*. 2001.

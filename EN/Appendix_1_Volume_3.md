# Appendix I: Lunar Industry

## Volume III: Energy System

**Version**: 1.9<br/>
**Date of Preparation**: June 2026<br/>
**Currency Unit**: Renminbi (RMB), symbol: ¥<br/>
**Related Main Volumes**: Main Volume IX (Energy and Communication Infrastructure), Main Volume VII (Engineering Validation)<br/>
**Prerequisite Reading**: Appendix I Volume I (Pioneer Missions), Volume II (Site Selection and Infrastructure)


### Glossary

| Abbreviation | Chinese Term | Description |
|------|----------|------|
| C/SiC | Silicon-carbide-fiber-reinforced composite | Zero-expansion mirror-substrate material |
| CO₂ | Carbon dioxide | Working fluid for supercritical CO₂ Brayton cycle |
| COP | Coefficient of performance | Ratio of heat-pump heating output to input electric power |
| CSP | Concentrated solar thermal power | Technology that uses heliostats to focus sunlight and heat a working fluid for power generation |
| EMI | Electromagnetic interference | Interference from power-electronics equipment to communication and scientific instruments |
| EVA | Extravehicular activity | Astronaut operations outside the vehicle on the lunar surface or in space |
| FRC | Field-reversed configuration | A magnetic-confinement fusion configuration |
| GCR | Galactic cosmic rays | High-energy particle radiation from outside the Solar System |
| HEU | Highly enriched uranium | Fuel for space nuclear reactors, with U-235 enrichment >= 93% |
| HVDC | High-voltage direct current transmission | High Voltage Direct Current |
| HV | High voltage | Power-transmission voltage class |
| IEC | International Electrotechnical Commission | International Electrotechnical Commission |
| ITO | Indium tin oxide | Transparent conductive thin-film material used for electrostatic dust-curtain electrodes |
| kWe | Kilowatt electric | Unit of electric power output from generation systems |
| LED | Light-emitting diode | Light Emitting Diode |
| LiF | Lithium fluoride | Component of high-temperature phase-change thermal-storage media |
| MgF2 | Magnesium fluoride | Component of high-temperature phase-change thermal-storage media |
| MHD | Magnetohydrodynamic generation | Magnetohydrodynamic Generation |
| MLI | Multi-layer insulation | Reflective insulation used for passive thermal control in vacuum |
| MWe | Megawatt electric | Unit of electric power output from generation systems |
| MWt | Megawatt thermal | Unit of thermal power in collection or storage systems |
| NaK | Sodium-potassium alloy | Liquid-metal working fluid used for high-temperature heat-transfer loops |
| PE | Polyethylene | High-density polyethylene radiation-moderation layer material |
| PV | Photovoltaic | Solar photovoltaic power generation |
| s-CO₂ | Supercritical carbon dioxide | High-efficiency working fluid for Brayton cycle |
| SiC | Silicon carbide | Wide-bandgap power-device material used for solid-state transformers |
| SPE | Solar particle event | High-energy particle burst released by solar eruptions |
| ULE | Ultra-low-expansion glass | Candidate mirror-substrate material with near-zero thermal expansion |
| UPS | Uninterruptible power supply | Uninterruptible Power Supply |
| YBCO | Yttrium barium copper oxide | High-temperature superconducting tape, critical temperature around 92 K |
| Brayton cycle | Supercritical CO₂ Brayton cycle | Closed thermodynamic cycle using supercritical CO₂ as working fluid, with thermal-to-electric efficiency above 50% |
| Heliostat | Heliostat array | Large reflective-mirror array deployed on the lunar surface that tracks the Sun and reflects light to a central receiver |
| Electrostatic dust curtain | Electrostatic dust-curtain system | Contactless dust-removal device that uses a traveling-wave electric field to "throw off" deposited lunar dust |
| Spectral splitter | High-temperature spectral splitter | Optical device that separates ultraviolet/infrared bands from visible bands in concentrated sunlight |
| Adaptive optics | Adaptive-optics collimation system | System using wavefront sensors and deformable mirrors to reshape diverging concentrated beams into highly collimated beams |
| Molten salt | High-temperature molten salt | Mixed-salt working media for heat storage and heat transfer |
| Capillary network | Capillary radiant terminal network | Dense small-diameter pipe network embedded in sealed habitat walls for fanless radiant heating/cooling |
| Stirling engine | Stirling generator | External-combustion machine that generates electricity from heat, suitable for compact nuclear or solar-thermal power sources |


### 3.1 Opening Statement

This volume is positioned as the **energy-supply and thermal-management infrastructure plan** for the lunar industrial system. It focuses on answering the following core questions:

> After a permanent base is established, how much electrical supply is required for hundreds of residents, CNT factory production, water-ice extraction, and traction for orbital transport combined? Where does that energy come from? How do we maintain uninterrupted power through a 14-day lunar night? Can reactor and power-plant waste heat be connected into the base thermal loop, enabling a transition from "electricity-based heating" to "waste-heat utilization"? Are heliostat-field and solar-tower siting options constrained by skylight locations? After receiving concentrated beams of tens of megawatts, is the splitter itself "moderately warm" or "extremely hot"? What are the transmission efficiencies of high-temperature heat, electric power, and natural light under different operating conditions? How do these efficiencies shape the final underground-city layout? Can diverging beams be re-collimated optically for near-lossless ultra-long-distance light transmission? Can the lunar low-temperature environment support long-term deployment of superconducting power transmission? When base power demand eventually rises to the gigawatt scale, can helium-3 fusion move from "long-range concept" into engineering reality?

This volume builds on:

- **Volume I (Pioneer Missions)**: feasibility of lunar nuclear power sources (P0-M3) and small solar arrays has already been validated.
- **Volume II (Site Selection and Infrastructure)**: energy constraints for recommended sites (polar quasi-continuous daylight or mid/low-latitude lunar-night regime) have already been defined, and interface planning for near-term heat-pump thermal control and long-term thermal-electric-light co-generation hub has already been completed.
- **Overview volume**: strategic direction for the ultimate long-term energy solution (helium-3 fusion).

Core tasks of this volume:

1. Based on the population and industrial scale defined in Volume II, establish an energy-demand curve from early-stage hundreds of kilowatts to long-term megawatt and tens-of-megawatt levels, and ultimately gigawatt class.
2. Design the near-term (Stage II) distributed-energy solution: PV arrays + space nuclear reactors + storage-system configuration and redundancy. For the first time, incorporate reactor and industrial waste heat into a unified base thermal-loop design.
3. Fully detail the long-term (post-Stage III) engineering design for the thermal-electric-light co-generation hub: heliostat array (including siting-flexibility principles), supercritical CO₂ Brayton cycle, high-temperature molten-salt thermal storage, spectral splitter, and natural-light conduits (including temperature and thermal-management corrections).
4. Evaluate transmission efficiencies of high/low-temperature heat, electric power, and natural light under different operating conditions, and analyze their constraints and impacts on base layout, scale, and service radius. Introduce adaptive-optics collimation as a long-term option for major gains in light-transmission efficiency.
5. Analyze heat-rejection synergy between polar solar-thermal power plants and crater mining operations.
6. Plan the full base power transmission/distribution architecture from generation side to load side, including internationally grounded voltage-class selection, lunar-vacuum-specific adaptation design, and reserved upgrade path for long-term superconducting transmission.
7. Propose a conceptual lunar helium-3 fusion power-station scheme as the ultimate closed-loop energy path after Stage IV to break the physical upper limit of heliostat-array scaling.
8. Establish phased validation criteria for the energy system and align them with the P0 system in Appendix I Volume I and the validation framework in Main Volume VII.


### 3.2 Energy-Demand Analysis

#### 3.2.1 Phased Load Forecast

Lunar-base energy demand will rise in steps with population growth and industrial commissioning. The forecast below is based on the Phase I/II population and industrial scale in Volume II, plus expected full-load operation after Stage III.

| Stage | Time | Population | Major Electrical Loads | Peak Power Demand (estimate) |
|:-----|:-----|:-----|:-----|:-----|
| **Infrastructure Phase I** | Stage II, Years 2-5 | 12-20 | Life-support systems, construction-equipment charging, regolith 3D printers, communications and lighting | 100-200 kWe |
| **Infrastructure Phase II** | Stage II, Years 5-10 | 50-80 | All Phase I loads + regolith-sintering line, initial metal-smelting furnace, CNT pre-weaving pilot line, initial water-ice extraction, initial orbital transport | 500 kWe-1 MWe |
| **Early Industrialization** | Stage III, Years 1-5 | 100-200 | All Phase II loads + CNT mass-production line, large metal-smelting furnaces, scaled water-ice extraction, operational orbital transport, heliostat-array self-consumption | 5-10 MWe |
| **Mature Industrialization** | Stage III, Year 5 onward | 200-500 | All early-industrialization loads + helium-3 extraction (long-term technical validation), deep-space propellant depot, lunar-city public facilities | 20-50 MWe |
| **Lunar-City Stage** | Late Stage IV | 1,000-10,000 | All mature-industrialization loads + scaled helium-3 extraction, heavy industry (spacecraft final assembly, vacuum smelting), particle-physics facilities, etc. | 100-500 MWe (long-term gigawatt scale) |

#### 3.2.2 Near- and Long-Term Energy Strategy Split

- **Near term (Stage II, peak below 1 MWe)**: PV arrays serve as baseload during lunar daytime, suitable for polar quasi-continuous daylight sites. During lunar night, compact space reactors provide baseload, supported by lithium-ion batteries for short-term regulation and hydrogen storage for long-duration cross-night storage. The heat-pump system runs independently (see Volume II Section 2.4.3), with no direct thermal coupling to generation yet, but interface space must be reserved for future waste-heat recovery pipelines.
- **Long term (post-Stage III, peak above 5 MWe)**: Start construction of the thermal-electric-light co-generation hub, centered on heliostat array + supercritical CO₂ Brayton cycle + high-temperature molten-salt storage, delivering four-way co-production: power generation, heat storage, industrial heat supply, and natural lighting. PV and reactors remain as backup/emergency sources. Low-temperature waste heat from both reactors and plant systems is fully connected to the base thermal loop, with heat pumps retained only for peak shaving and backup.
- **Ultimate stage (late Stage IV, peak above 100 MWe)**: When heliostat-array area approaches the physical land limit of available polar continuous-light peaks, initiate deployment of lunar helium-3 fusion power stations (D-3He reaction, Section 3.5.9), enabling a fundamental transition from solar dependence to autonomous fusion energy, while supporting large-scale deep-space power export.


### 3.3 Near-Term Energy Solution: PV + Nuclear Source + Storage

#### 3.3.1 Solar Photovoltaic Array

**(a) Array configuration principles**

- Polar quasi-continuous daylight sites (Shackleton rim or Philolaus skylight): maximize near-continuous insolation, with PV as primary daytime supply. Arrays are deployed on surface areas around skylights or on continuous-light ridge platforms. For Phase II peak demand of 1 MWe, required array area is about 8,000-10,000 m², based on long-term multijunction GaAs cells with AM0 efficiency 45%, fill factor 0.85, and about 520 W/m² areal output.
- Mid/low-latitude sites (Marius Hills): daytime 14 days powered mainly by PV; nighttime 14 days switched to nuclear + storage. Array area must increase to about 12,000-15,000 m² to meet both load and storage-charging demand during daytime.

**(b) Key technical requirements**

- Cell type: flexible multijunction gallium-arsenide cells (GaInP/GaAs/Ge), long-term AM0 efficiency >= 45%.
- Dust removal: electrostatic dust-curtain system, shared with long-term heliostat dust-removal technology (see Section 3.5.2(c)), requiring neither mechanical cleaning nor liquids.
- Deployment method: spool launch -> autonomous surface deployment by mechanisms delivered with cargo landers.

#### 3.3.2 Space Nuclear Reactor

**(a) Configuration principles**

- Serves as nighttime baseload backup for polar sites, or primary nighttime source at mid/low latitudes.
- Total installed capacity must cover all nighttime life support, communications, and minimum industrial thermal-preservation demand.
- Per-reactor power class: 3-10 kWe (Phase I, Kilopower class [1]) -> 50-100 kWe (Phase II and beyond, Chinese space reactor [9] or Russian ABV-6E class [10]). Russian ABV-6E thermal power is 38 MWt with electric output 6-9 MWe and 10-year refueling cycle [10]. Deploy 2-3 units in both Phase I and Phase II with n+1 redundancy.
- Deployment mode: transported by dedicated cargo landers to radiation-safe zones at >= 1 km from base, using natural terrain shielding (crater rims or ridges) or artificial regolith berms.

**(b) Key technical requirements**

- Reactor type: Stirling space reactor (primary) or thermionic space reactor (backup).
- Fuel: highly enriched uranium, U-235 enrichment >= 93%.
- Design life: >= 10 years (Kilopower class [1]) or >= 15 years (Chinese space reactor [9]).
- Waste-heat rejection: under normal operation, Stirling cold-end waste heat (about 30°C-50°C) is conducted via heat-pipe network to large-area radiative panels facing deep space. **From Infrastructure Phase II onward, this low-grade waste heat should be preferentially integrated into the base thermal loop** through heat exchangers, transferring heat to the capillary-network heating loop in Volume II Section 2.4.3 and offsetting part of heat-pump electricity consumption; only when no heating demand exists should rejection switch to deep-space radiation.

#### 3.3.3 Energy Storage System

| Storage Type | Capacity (Phase II) | Purpose | Technical Parameters |
|:-----|:-----|:-----|:-----|
| **Lithium-ion battery packs** | 0.5-1 MWh | Short-term peak regulation (seconds to minutes), smoothing PV fluctuations, emergency transition power | Solid-state lithium batteries, energy density >= 500 Wh/kg, cycle life >= 10,000 |
| **Regenerative hydrogen fuel cells** | 10-20 MWh | Long-duration cross-lunar-night storage (14 days x about 500 kWe average Phase II load), daytime electrolysis and nighttime fuel-cell generation | Electrolysis efficiency >= 70%, fuel-cell efficiency >= 55%, hydrogen stored as liquid hydrogen or metal hydride |
| **High-temperature phase-change thermal storage** (industrial) | 5-10 MWh thermal | Preheating/thermal hold for metal-smelting and sintering lines, reducing nighttime electric heating demand | LiF/MgF2 eutectic salt, phase-change temperature about 740°C, energy density about 1 MJ/kg |

> Note: water for hydrogen storage systems comes from local water-ice extraction (see Volume IV), not Earth resupply. In the initial period (Infrastructure Phase I), before local extraction reaches scale, first-batch hydrogen tanks may be pre-deployed from Earth. First-batch liquid-hydrogen tanks with insulation require total launch mass about 5-10 tons for 10-20 MWh electric-equivalent hydrogen capacity and can be deployed in one heavy cargo-lander mission. After entering Stage III, hydrogen storage is gradually supplanted by high-temperature molten-salt storage (core component of the thermal-electric-light co-generation hub), with hydrogen storage retained as emergency backup.


### 3.4 Power Transmission and Distribution Architecture

The base T&D network must serve both elongated underground lava-tube spaces and dispersed surface facilities. The design follows three core principles:

1. **Underground-surface dual-network coordination**: the underground backbone runs along the full sealed-cave section and serves habitation, industrial, and life-support zones; surface grids connect through skylights to the underground backbone and serve PV fields, heliostat fields, mining zones, launch sites, and other remote facilities.
2. **DC backbone, AC conversion at endpoints**: exploiting lunar-vacuum advantages for DC transmission, no EMI coupling, no skin effect, no capacitive loss in the same way as AC line operation, the backbone uses HVDC. AC conversion is performed locally at loads for AC motors and conventional equipment.
3. **Fault isolation and network reconfiguration**: if any bus feeder section experiences short-circuit or ground fault, the system must isolate the faulted section within 10 ms and reconfigure within 100 ms to restore non-faulted sections. Critical loads such as life support require local UPS or a second independent power path for dual-fault scenarios.

#### 3.4.1 Voltage-Class System

| Voltage Class | Use | Selection Basis |
|:-----|:-----|:-----|
| **±100 kV DC** | Long-distance transmission trunk (near term) | Based on Main Volume V Section 5.11.2 conductive-track experience, ±100 kV DC can limit transmission loss to below 5% over hundred-kilometer distances |
| **±10 kV DC** | Underground ring-bus backbone | Medium-voltage class suitable for elongated lava-tube spans of hundreds of meters to several kilometers; 10 kV cable insulation requirements are lower than higher-voltage alternatives and better fit limited sealed-tunnel cross-sections |
| **690 V AC** | Industrial distribution | IEC 60038 standard: 690 V is the preferred industrial voltage for large equipment. At equal power, operating current is about 58% of a 400 V system, reducing line loss and cable cross-section. Widely used globally and directly compatible with lunar smelters, CNT lines, and sintering equipment |
| **400 V AC** | Habitation distribution | IEC 60038 standard: 400/230 V is the globally common low-voltage standard. Enables direct compatibility with civil, scientific, and medical equipment imported from Earth without extra transformers, maximizing reliability in habitation zones |
| **Superconducting DC transmission** | Long-distance, ultra-high-power trunk (long-term upgrade) | When single-circuit power reaches hundred-megawatt class or distance exceeds 100 km, losses and thermal management of conventional conductors become prohibitive. HTS tapes such as YBCO (Tc about 92 K) can significantly reduce cryogenic power under lunar low-temperature conditions. **Reserved for long-term evaluation** after validated long-length HTS manufacturing |
| **Long-term HV expansion interface** | Future high-power generation modules (reserved) | For post-Stage IV modules such as helium-3 fusion units at hundred-megawatt scale and above, interconnection voltage must be upgraded to ±200 kV DC or higher. Reserve step-up station interface between ±10 kV bus and high-voltage bus |

#### 3.4.2 Underground Main Grid (Ring Bus)

- **Topology**: **dual-redundant ring bus**. Two independent ±10 kV DC trunk cables run in parallel along the full sealed-cave section, one near cave crown and one near cave wall as backup. Tie-switch cabinets are installed every 100-200 m. Under normal operation, tie switches are open; when any segment fails, ties close automatically and reroute via the healthy cable.
- **Connection method**: load units, including habitation zones, industry, and life-support centers, are fed by **radial feeders** from ring-bus nodes. Each feeder has a remotely operated breaker at the ring-bus connection for feeder-level isolation.
- **Distribution transformers**: 10 kV/400 V AC for habitation and 10 kV/690 V AC for industrial areas. Solid-state transformer efficiency >= 98%.

#### 3.4.3 Surface Extension Grid (Trunk Type)

- **Topology**: ±10 kV or ±100 kV DC trunk lines are led from underground ring bus via skylights to remote surface loads. Trunk lines follow primary surface corridors with sectional switches every 1-2 km.
- **Long-distance transmission**: supply to mining sites, launch sites, and traction substations uses ±100 kV DC, controlling hundred-kilometer losses within acceptable range, e.g., <5%.
- **PV integration**: low-voltage DC from each PV subfield is boosted by DC/DC converters to ±10 kV DC and tied through combiner cabinets into distribution nodes near skylights, then into underground ring bus. Combiner cabinets include triple protection:
  - **Layer 1 (passive)**: anti-reverse diodes for millisecond-level automatic backflow blocking.
  - **Layer 2 (active dispatch)**: remotely controlled DC breakers automatically connected/disconnected by control system per load and generation forecast.
  - **Layer 3 (safety assurance)**: manual isolation switch with physical disconnect gap for locked-out maintenance/emergency isolation.

#### 3.4.4 Generation-System Interfaces

| Generation System | Grid-Tie Method | Protection Configuration |
|:-----|:-----|:-----|
| PV array | DC/DC boost -> ±10 kV DC bus | Anti-reverse diode + remote DC breaker + manual isolator (triple protection) |
| Nuclear reactor | AC/DC rectification -> ±10 kV DC bus | Remote DC breaker + manual isolator |
| Supercritical CO₂ turbine | AC/DC rectification -> ±10 kV DC bus | Remote DC breaker + manual isolator |
| High-temperature molten-salt storage | Not directly grid-connected (via turbine drive) | - |
| Lithium-ion battery pack | Bidirectional DC/DC -> ±10 kV DC bus | Bidirectional DC breaker + manual isolator |
| Hydrogen fuel cell | DC/DC boost -> ±10 kV DC bus | Remote DC breaker + manual isolator |
| Helium-3 fusion plant (long term) | MHD DC output -> ±100 kV DC trunk (via DC/DC step-up) | Remote DC breaker + manual isolator |

> Note: all generation and storage nodes connected to the main grid must include manual isolators with physical air-gap disconnects to ensure absolute electrical safety during maintenance and emergencies. This applies to all grid-tied equipment including PV arrays, reactors, turbine generators, battery packs, hydrogen fuel cells, and future helium-3 fusion stations.

#### 3.4.5 Lunar Environmental Impacts on Grid Design

- **Insulation design**: in lunar vacuum, conventional air-insulation clearances are not applicable. All medium/high-voltage connectors and switching equipment must use solid encapsulation (epoxy or silicone-rubber potting) or SF6 gas insulation. Creepage distances must be recalculated for vacuum operation. With no air convection cooling, cable ampacity must be derated by about 15%-20%.
- **Thermal management**: underground cables in sealed caves reject heat via cave-wall conduction and cabin-air convection. Long-distance high-load cables require distributed fiber-optic temperature sensing embedded in shield layers for automatic derating under abnormal temperature rise.
- **Electromagnetic compatibility**: DC transmission itself does not create the same EMI concerns in lunar vacuum, but harmonics from solid-state transformers and inverters may interfere with communications and scientific instruments. EMI filters are required at transformer/inverter I/O, and sensitive loads, such as radio telescopes and gravitational-wave detectors, must be segmented from industrial loops on separate ring-bus sections.

#### 3.4.6 Grid Intelligence Requirements

- **Load forecasting and automatic dispatch**: the control system must autonomously generate 24-72 hour generation/storage schedules based on historical load, PV forecasts from solar position and mirror-field state, storage-tank capacities, and reactor operating conditions.
- **Fault isolation and reconfiguration**: for short-circuit or ground fault on any feeder section, relays must isolate in <10 ms and complete reconfiguration in <100 ms to restore non-faulted sections. Critical loads require additional local UPS or second independent feed path.
- **Black-start plan**: after full-base blackout, reactors with independent startup supplies and thermal-storage turbines with hot-start capability can restore generation and progressively re-energize the grid. Detailed black-start sequence is defined in Volume VIII emergency planning.


### 3.5 Long-Term Energy Hub: Detailed Design of Thermal-Electric-Light Co-Generation

This section extends the high-level introduction in Volume II Section 2.5 and provides detailed engineering for the thermal-electric-light co-generation hub. Construction starts after Stage III industrialization and uses modular phased deployment to match load growth while reducing early capital risk.

#### 3.5.1 Overall Architecture and Modular Phased Deployment

The hub consists of three functionally coupled but independently phaseable subsystems:

- **Heliostat array (solar-thermal capture front end)**: deployed on surface zones around skylights or flat areas within several hundred meters, focusing sunlight to a central receiver.
- **Supercritical CO₂ Brayton cycle + high-temperature molten-salt storage (conversion and storage core)**: concentrated sunlight drives generation; molten-salt tanks provide energy buffering.
- **Spectral splitter + natural-light conduits (lighting subsystem)**: separates visible light from concentrated beam for underground illumination.

**Phase I (startup, about Years 12-15)**: deploy first heliostat block, about half planned area, and one 10 MWe-class s-CO₂ turbine-generator. Molten-salt storage sized for 12 hours full-power generation, about 120 MWhe equivalent. Splitter and light conduits are not installed yet; focus is generation and industrial heat.

**Phase II (expansion, about Years 16-20)**: expand heliostat area to full plan, add second turbine-generator, reaching 20-30 MWe total output. Expand storage to 24 hours. Install splitter and first habitation-zone light conduits.

**Phase III (mature, Year 21 onward)**: complete conduit coverage for ecological and public zones. Optional third turbine-generator can raise output to 50 MWe, matching mature-industrial peak demand. If geology permits, deploy adaptive-optics collimation with straight light conduits to deliver natural light to kilometer-scale remote zones.

#### 3.5.2 Heliostat Array

**(a) Optical design and siting flexibility**

Use a tower-concentrating configuration: heliostats reflect sunlight to a central secondary reflector, then the secondary redirects the beam toward the light-conduit and molten-salt receiver entrance below or near a skylight.

Note: all solar-spectrum data in this plan use ASTM E490-00a AM0 spectrum [3].

- **Siting-flexibility principle**: heliostat field and central tower do not have to be directly above skylight openings. Core constraints are only: (i) heat-transfer distance from central receiver to molten-salt storage to s-CO₂ heat exchanger should be as short as possible, <=500 m, to limit high-temperature pipeline losses; (ii) optical path from secondary reflector to light-conduit entrance must remain geometrically connected with proper pointing. When skylight area is constrained or terrain is unfavorable, heliostats can be concentrated on flat surface areas hundreds of meters away, with independent tower siting and short-distance thermal/optical links to underground equipment rooms. The skylight itself only needs to carry lift and logistics channels.
- Single-mirror area: 10-20 m², lightweight parabolic mirrors with C/SiC or ULE substrates, silver or aluminum reflective coatings, reflectivity >=95%.
- Mirror count: for 10 MWe generation baseline, about 2,500-5,000 mirrors are required, total collection area about 50,000 m², consistent with Volume II Section 2.5.2 order-of-magnitude estimate.
- Field footprint: about 0.1-0.2 km² including mirror spacing and maintenance lanes.

**(b) Tracking and control system**

- Dual-axis drive per mirror, azimuth + elevation, tracking precision <=0.5 mrad, about 0.03°.
- Control: ephemeris-based open-loop tracking + closed-loop correction. Feedback from beam-position sensors on central tower.
- **Automation requirement**: mirror-field control must be fully autonomous, dynamically adjusting focus/defocus of each mirror using solar position, space-weather forecast from circumlunar monitoring satellites, storage state, and grid-demand data to regulate total receiver thermal power. Under anomaly conditions such as SPE warning, full-field defocus must be completed within 1 minute to safe irradiance levels.

**(c) Lunar-dust protection**

- Each mirror includes transparent electrostatic dust-curtain electrodes using patterned ITO films in interdigitated layouts.
- Driven by dedicated high-voltage pulsed supply, about 1-3 kV amplitude and 1-10 Hz frequency, generating traveling-wave electric fields on mirror surfaces to move charged dust particles directionally off edges.
- Dust-removal power consumption: about 1-5 W/m² mirror area, around one-thousandth of incident solar power, about 1,361 W/m².

#### 3.5.3 Supercritical CO₂ Brayton-Cycle Power System

**(a) Thermodynamic cycle design**

Adopt the **recompression supercritical CO₂ Brayton cycle**, widely recognized as one of the highest-efficiency cycle topologies for next-generation thermal power [2][4].

- Working fluid: supercritical CO₂, critical temperature 31°C and critical pressure 7.38 MPa.
- Turbine inlet temperature: 700-750°C, heated by heliostat-concentrated input through molten-salt heat exchangers.
- Turbine inlet pressure: 20-25 MPa.
- Net cycle efficiency: >=50%, reaching about 52%-54% at 750°C turbine inlet, well above steam Rankine at about 35%-40% [2][4].
- Cooling mode: radiative heat rejection to deep-space-facing panels. In lunar vacuum, with deep-space background near 4 K, panel performance outperforms Earth water/air cooling. Required panel area is about 500-1,000 m² per MWe, estimated from panel surface temperature 400 K, emissivity 0.85, and Stefan-Boltzmann law [8].

**(b) Key equipment**

| Equipment | Technical Parameters | Notes |
|:-----|:-----|:-----|
| Turbine-compressor-generator unit | Unit power 10-25 MWe; speed >=30,000 rpm; dry gas bearings | s-CO₂ turbine is about one-tenth the volume of same-power steam turbine |
| Printed-circuit heat exchanger | Operating temperature <=800°C, pressure <=30 MPa | High-temperature side molten salt or s-CO₂, low-temperature side s-CO₂ recuperation |
| High-temperature molten-salt to s-CO₂ heat exchanger | Operating temperature <=800°C, pressure <=30 MPa | High-temperature side molten salt, low-temperature side s-CO₂ |
| Radiative panel | Rejection capacity 500-2,000 W/m²; area 500-1,000 m²/MWe | Lightweight carbon-carbon composite panel with embedded heat-pipe network |

**(c) Coupling with molten-salt storage**

- Molten salt is heated by concentrated sunlight to about 565°C and stored in **hot tanks**.
- During generation, hot salt is pumped through salt-s-CO₂ exchangers to heat s-CO₂ to 700-750°C and drive turbine work.
- Cooled salt from exchangers, about 350°C, enters **cold tanks** awaiting reheating.
- Storage capacity: Phase I provides 12 hours full-power generation, about 120 MWhe equivalent; Phase II expands to 24 hours. Total thermal medium mass is about 500-1,000 tons, based on usable 565°C to 350°C temperature differential and molten-salt heat capacity about 1.5 kJ/kg-K. Tank shells should preferably use locally manufactured regolith concrete, preferably with high-quality construction material that meets Volume I Section 1.3 criterion b. Only sealed liners and exchanger piping are launched from Earth to minimize transport cost.

**(d) Synergy between heat rejection and polar mining**

Radiative panels reject low-grade waste heat around 30°C-50°C to deep space under normal operation. For polar sites near Shackleton, if plant-to-permanently-shadowed crater distance is 5-15 km, part of this low-grade heat can be delivered via mobile insulated pipelines into crater water-ice mining zones to preheat ice-bearing regolith, significantly improving extraction efficiency while reducing electric heating demand. Detailed hot-water/steam pipeline schemes, insulation standards, and operation modes are provided in Appendix I Volume IV.


#### 3.5.4 High-Temperature Heat Transmission and Base Layout

Transmission efficiency of high-temperature heat from surface heliostat capture points to underground generation/storage equipment directly sets allowable distance between plant and core base zones, shaping overall layout.

**(a) High-temperature heat transmission mode**
Core thermal path, concentrated sunlight -> molten-salt receiver -> hot molten-salt tank -> s-CO₂ exchanger, uses liquid metal such as NaK or molten salt itself as transfer fluid in pipelines. Pipe surfaces can be wrapped with **multi-layer insulation** where needed to minimize losses.

**(b) Comparison of bare versus MLI-insulated pipe transmission efficiency**
For quantitative comparison, assume 50 MWt transfer over 500 m with 565°C molten salt.

| Parameter | Unit | Bare Pipe | MLI-Insulated Pipe |
|:-----|:-----|:-----|:-----|
| **Pipe outer diameter** | m | 0.3 | 0.4, including insulation |
| **Surface emissivity (epsilon)** | - | 0.6, oxidized stainless steel | 0.005, MLI outer layer |
| **Surface temperature (Ts)** | °C | about 560 | about 30, MLI outer surface |
| **Ambient temperature (Tamb)** | °C | 120, lunar daytime surface | 120, lunar daytime surface |
| **Radiative heat loss** | kW/m | about 3.8 | about 0.002 |
| **Total 500 m heat loss** | MWt | about 1.9 | about 0.001 |
| **Transmission efficiency** | % | about 96.2% | about 99.998% |

Calculated with Stefan-Boltzmann law [8]. The result is clear: **in lunar vacuum, radiative loss is the dominant loss mode for bare hot pipes, while MLI nearly eliminates this loss and enables near-lossless span transmission.**

**(c) Medium/low-temperature heat network**
Given near-lossless transfer behavior, a unified multi-temperature thermal network can be established:

- **High-temperature network, 500-750°C**: from central plant using NaK and MLI-insulated lines to high-energy industrial zones such as smelting and regolith sintering.
- **Medium-temperature network, 200-500°C**: using s-CO₂ extraction or dedicated molten-salt loops to water-ice and catalyst-extraction plants.
- **Low-temperature network, 30-50°C**: using plant waste heat via insulated hot-water lines to habitation/ecological zones, interfacing with Volume II Section 2.4.3 capillary radiant terminals.

**(d) Impacts of transmission efficiency on layout and scale**
High-efficiency insulation pipelines remove the requirement that generation equipment be adjacent to thermal sources:

1. **Layout decoupling and improved safety**: heliostat fields and molten-salt receivers can be built hundreds of meters to kilometers from underground base access skylights, avoiding excessive concentration of large infrastructure around single access points and physically separating high-temperature/high-pressure generation equipment from habitation.
2. **Scale expansion less constrained by terrain**: when terrain near skylights is limited, **siting-flexibility principles in Section 3.5.2** combined with **high-efficiency heat transfer** allow practical large-scale heliostat expansion.
3. **Zonal thermal control and on-demand supply**: near-lossless transmission makes a **base-wide unified thermal network** economically viable, enabling flexible placement of industrial subsystems by process and safety needs at different distances from the energy hub.


#### 3.5.5 Electric-Power Transmission Efficiency and Base Layout

Power-transmission efficiency behaves differently from heat: losses scale roughly linearly with distance rather than exponentially. Section 3.4 provides full grid architecture; this section focuses on layout constraints from transmission efficiency.

**(a) Near-term layout, Stage II**
At this stage demand is modest, hundred-kilowatt class. Transmission from **surface PV arrays -> underground load centers** spans short distances, typically <1 km from skylight to first underground equipment rooms. Resistive line loss is minimal and not a bottleneck. Deploying PV near skylights is practical and economical.

**(b) Long-term layout, post-Stage III**
In the thermal-electric-light hub, s-CO₂ turbine generators must be colocated with thermal sources, molten-salt storage. Therefore, **long-term generation equipment moves from surface to underground**.

- **Transmission efficiency**: distance from underground turbine generators to underground distribution buses is very short, usually <100 m. Even at 50 MWe transfer, conventional medium-voltage AC at around 10 kV yields negligible loss, <0.1%.
- **Layout impact**: high efficiency allows large high-temperature generation equipment to be safely deployed deep underground while supplying the full underground city through short cable runs. Transmission constraints mainly apply to **remote facilities** such as mining sites, launch areas, and traction substations, where HVDC from Section 3.4.1 is required to keep hundred-kilometer losses acceptable, e.g., <5%. If single-circuit power later reaches hundred-megawatt class, superconducting DC upgrades can be activated to exploit lunar low-temperature conditions.


#### 3.5.6 Light-Source Transmission Efficiency and Base Layout

Natural-light conduits are the most distinctive component of co-generation. Light-transmission efficiency determines how far underground areas can be illuminated and whether dedicated infrastructure is justified. Unlike electric power with roughly linear attenuation, light in traditional conduits shows **exponential attenuation with distance**. This behavior can be fundamentally changed with adaptive-optics collimation.

**(a) Near term, Stage II**
No light conduits are deployed in this stage, see Section 3.5.1. Underground illumination relies entirely on LEDs.

- **Efficiency assessment**: if LED lighting, electro-optical efficiency about 35%, is powered by PV, efficiency 45%, total sunlight to light efficiency is 45% x 35% ≈ **16%**. This means 100 W sunlight produces only 16 W lighting output.

**(b) Long term, post-Stage III: reflective conduit baseline**
Splitters route concentrated "cold light", visible band without infrared thermal load, into underground conduit networks.

- **Efficiency assessment**:
  - Splitter efficiency: >95%.
  - Conduit transmission: with high-reflectance inner coatings, R>98%, single-bounce loss about 2%. After $n$ reflections, transmission is $R^n$.
    - **Short distance, <200 m**: few reflections, e.g., 10, efficiency $0.98^{10} \approx 81.7\%$. End-to-end about $95\% \times 82\% \approx 78\%$.
    - **Medium distance, 200-500 m**: moderate reflections, e.g., 30, efficiency drops to $0.98^{30} \approx 54.5\%$. End-to-end about $95\% \times 54\% \approx 51\%$.
    - **Long distance, >1000 m**: many reflections, e.g., 60, efficiency drops sharply to $0.98^{60} \approx 29.8\%$. End-to-end only $95\% \times 30\% \approx 28\%$.
- **Operating analysis**:
  - **Short-range high efficiency**: within 200 m, conduit efficiency, 78%, greatly exceeds PV + LED, 16%.
  - **Mid-range parity**: around 500-800 m, conduit efficiency approaches PV + LED, about 30%-50%.
  - **Long-range low efficiency**: beyond 1000 m, conduit loses advantage and is often less economical than LED lighting.

**(c) Long term, post-Stage III: adaptive-optics collimation + straight conduit high-efficiency scheme**
The baseline bottleneck is beam divergence. If visible beams after splitting are re-collimated by **adaptive optics** into highly parallel beams, dominant physics shifts from reflection-loss control to near-lossless straight-line propagation.

- **Adaptive-optics collimation module**:
  1. **Wavefront sensor**: real-time measurement of wavefront distortion in transmitted visible beam.
  2. **Deformable mirror**: thin mirror driven by hundreds of micro-actuators with micron-scale shape control.
  3. **Closed-loop controller**: updates mirror shape thousands of times per second to reshape diverging aberrated beams into highly collimated beams.
- **Quantitative assessment**:
  - **Without adaptive optics**: for beam half-angle divergence 1°, beam in a 1.5 m diameter conduit first hits the wall at about **43 m**.
  - **With adaptive optics, medium performance**: compress divergence to 10 arcseconds, about 0.0028°. In same conduit, beam propagates about **15.4 km** before first wall contact.
  - **With adaptive optics, high performance**: at 1 arcsecond divergence, straight propagation exceeds **150 km**.
- **Efficiency and layout impact**: with collimated beams in straight conduits, inner reflective coatings are no longer the primary determinant of transmission efficiency. Losses are dominated by residual gas absorption in conduits, negligible under high vacuum, and very small wall diffraction effects. The network can shift from exponential attenuation to **near-lossless straight-line transmission**.
  - **Breaks the 500 m service-radius constraint**: remote zones previously outside natural-light range, such as industrial sectors or second base zones kilometers away, can receive illumination quality comparable to areas below skylights via straight conduits.
  - **"Optical-axis" layout mode**: habitation and ecological zones no longer need to cluster tightly around skylights. Light axes can follow naturally straight lava-tube segments or purpose-drilled straight microtunnels to support remote habitation/science zones. Skylights shift from "life core" to pure "light intake and logistics channel" roles.
  - **Geological dependency**: viability depends strongly on availability of sufficiently long straight segments without curvature. If natural tubes have hundred-meter to kilometer straight runs, they can be used directly; otherwise specialized excavation/boring is required, significantly increasing engineering scope. Therefore, this option should be decided only after mission-group II/III GPR data evaluate straight-segment availability in site-selection phase.

**(d) Engineering envelope of light-conduit solutions**
Regardless of reflective or collimated straight mode, the main conduit body is a rigid vacuum pipe, aluminum alloy or CFRP, with 1-2 m inner diameter. Reflective conduits can follow natural lava-tube curvature. Straight conduits require straight tunnel sections and tighter geological/construction tolerances. Flexible "optical cables", if interpreted as large-core liquid-core guides or hollow-core photonic-crystal fibers, can be used only for terminal last-mile distribution. Their loss, about 1%-5% per meter, is far higher than rigid vacuum conduits, limiting practical length to generally <=20 m for short-distance links.


#### 3.5.7 Industrial Heat Supply and Reactor Waste-Heat Recovery Interfaces

While generating power, the s-CO₂ Brayton system and nuclear reactors can form a unified **base thermal network**, delivering three process-heat grades by temperature level:

| Heat Grade | Temperature Range | Source | Use |
|:-----|:-----|:-----|:-----|
| **High temperature** | 500-750°C | Mainstream extraction before turbine inlet, or direct heliostat heating | Metal smelting, electric-furnace preheating, regolith sintering support heating |
| **Medium temperature** | 200-500°C | Mid-stage turbine extraction | Water-ice extraction, heating ice-bearing regolith to about 150-500°C, catalyst extraction |
| **Low temperature** | 30-50°C | Waste-heat recovery from s-CO₂ radiative panels **plus waste-heat recovery from reactor Stirling cold end** | Space heating through capillary-network interface in Volume II Section 2.4.3, greenhouse thermal maintenance |

This cascaded thermal-utilization system raises overall energy-utilization efficiency from about 50% for power-only operation to **above 85%**. After reactor waste heat is connected to low-temperature heating loops, most routine base-heating demand can be covered, with heat pumps retained only for peak regulation and backup. Detailed thermal-demand profiles, insulation standards, and interface designs for industrial subsystems are developed in Volume IV and Volume V.

#### 3.5.8 Implementation Notes for Thermal, Electrical, and Optical Transmission

The transmission schemes in Sections 3.5.4-3.5.7 are ideal-condition evaluations based on physical principles. Real engineering deployment faces additional constraints and must be adapted to site geology, equipment availability, and construction capability. Key variation factors and engineering impacts are listed below for downstream detailed design:

- **Long-distance high-temperature fluid transmission**: when molten-salt or NaK pipelines extend beyond kilometer scale, beyond heat loss considerations, **pumping power consumption** and **thermal-expansion compensation** become critical. Pressure-drop pumping demand scales with line length and roughly velocity squared; thermal expansion from ambient to 565°C can reach about 0.6%-0.8% in line length, requiring expansion joints or flexible segments at bends. These requirements may limit practical optimum transfer distance to a few kilometers rather than theoretically unlimited spans.

- **Excavation and breakthrough for straight light conduits**: the adaptive-optics + straight-conduit scheme in Section 3.5.6(c) depends strongly on natural straight segments. If tube geometry is curved, **microtunnel mechanical excavation, blasting, or laser boring** is required, along with **precision alignment at conduit joints**, requiring beam-center offset under a few centimeters over hundreds of meters. This can substantially increase schedule and cost and should be pre-allocated in Volume II infrastructure with dedicated construction corridors and equipment space.

- **Vacuum maintenance in light conduits**: for both reflective and straight designs, high transmission efficiency requires high vacuum in conduits to minimize absorption/scattering. Initial evacuation benefits from ambient lunar vacuum, but long-term operation is degraded by micro-outgassing from basalt walls and seal materials. **Distributed small vacuum-pump sets** or getter pumps must be installed along conduit sections for periodic or continuous pressure maintenance. Pump count and spacing depend on outgassing rates and must be quantified in detailed design.

- **Power-transmission redundancy and switching**: reconfiguration of ±10 kV DC ring bus after fault isolation, Section 3.5.5(b), requires reliable **fast switchgear**, action <10 ms, and coordinated **intelligent protection relays**. Dual faults on the ring can still cause partial blackout. Critical loads must therefore include local UPS or second independent feeder for dual-redundant supply.

- **Sectional isolation in thermal network**: high/medium/low-temperature pipeline networks in Section 3.5.4(c) require **sectional isolation valves**. If one section leaks due to micrometeoroid impact or aging, valves must auto-close to isolate that segment without disrupting other zones. Valve spacing and response time are determined in detailed designs of Volumes IV and V.


### 3.5.9 Ultimate Closed-Loop Energy: Lunar Helium-3 Fusion Plant, Long-Term Vision

**(a) Strategic role**

The thermal-electric-light co-generation hub can meet mid- to long-term lunar demand at 5-50 MWe. However, once lunar cities reach ten-thousand-person scale in Stage IV, deep-space ships are batch-built at lunar dockyards, and high-power heavy industry and particle-physics facilities run at full operation, peak demand may rise to hundreds of megawatts or even gigawatts. At that point, concentrated solar based on heliostat arrays reaches physical limits in area and storage. Each additional 100 MWe may require roughly 1 km² of mirror area, while usable polar continuous-light land remains finite.

Helium-3 fusion, D-3He, is the ultimate path to break this ceiling. Unlike deuterium-tritium fusion, D-T, D-3He theoretically produces minimal neutron output, releasing most energy as charged particles that can be converted directly by MHD generation without large steam turbines and heat exchangers. System efficiency can reach 60%-70%, and reactor-wall activation from neutron damage is greatly reduced [11]. D-3He is considered a primary advanced-fuel candidate for reducing tritium inventory, neutron flux, structural damage, and activation, though compared with traditional tokamak design it faces higher synchrotron-radiation losses and is currently more suitable for high-beta and/or non-Maxwellian plasma configurations [11]. Recent studies indicate D-3He reactors may output 16-20 GW fusion power near 40-45 keV, 10 T magnetic field, and 3x10^20 m^-3 electron density [12].

Total solar-wind-implanted He-3 in lunar regolith is estimated at 1 to 5 million tons, while known terrestrial reserves are about 0.5 tons. Conservative estimates place He-3 content at about 3.7 ppb in highlands and 7.8 ppb in maria. At 1998 global energy consumption and 50% recovery, upper 3 m of mare regolith alone could supply Earth for more than 1,000 years [13]. Detailed survey data are in Main Volume II Section 2.5.2 and Appendix I Volume IV Section 4.3.4.

**(b) Technical route overview**

The following conceptual D-3He plant is a long-term technology vision and primarily defines interfaces with existing base energy systems:

1. **Fuel supply**: helium-3 extraction facilities in Volume IV Section 4.3.4 heat regolith to about 700°C to release solar-wind-implanted volatiles. HEAT prototype systems have validated release of He-3 and other volatiles, hydrogen, He-4, CO₂, methane, nitrogen, water, from heated <100 um regolith simulants at 700°C, see references in Volume IV Section 4.3.4. Isotopic separation then yields concentrated He-3 for fusion fuel storage.
2. **Fusion reactor**: inertial or magnetic confinement, with field-reversed configuration, FRC, as a promising D-3He route due to high beta and open-field topology that can mitigate synchrotron losses. D-3He FRC plants are considered attractive in environmental acceptability and power cost [11]. Mixed D/3He fuel is heated to fusion temperatures around 10 keV, about 1.16x10^8 K. Main products are protons and alpha particles, both charged.
3. **Direct MHD power generation**: charged fusion products pass through MHD channels and convert kinetic energy directly to electrical power without steam-turbine intermediate stages. Theoretical conversion can reach 60%-70%, above about 50% for s-CO₂ Brayton cycles.
4. **Waste-heat utilization**: high-temperature helium from MHD channels, about 800°C, enters high-temperature network in Section 3.5.7 for smelting and regolith sintering. Low-grade waste heat, about 50°C, enters habitation capillary heating loops and is fully compatible with the existing co-generation waste-heat architecture.

**(c) Relationship with existing energy systems**

Helium-3 fusion plants do not replace the thermal-electric-light hub but represent its ultimate upgrade. Shared interfaces include:

- **High-temperature thermal network**: fusion MHD waste heat and hub molten-salt storage share 500-750°C high-temperature pipelines.
- **Low-temperature heating loops**: both supply 30-50°C waste heat into habitation capillary networks.
- **Transmission and distribution grid**: fusion MHD output is DC and can tie directly to ±100 kV DC trunks, compatible with AC/DC-rectified outputs from existing s-CO₂ turbines.

**(d) Timeline outlook**

Commercialization timing for D-3He depends on two key factors: first, scaled He-3 supply capability, with extraction in Volume IV Section 4.3.4 expected to exceed kilogram-per-month scale in Stage IV; second, breakthrough of key reactor technologies such as confinement time and high-temperature-resistant MHD-channel materials. Internationally, probability of commercial D-3He before mid-century is generally viewed as low, so this plan positions it as a late Stage IV option around Year 30-35.

Before fusion deployment, base power demand is fully met by the thermal-electric-light hub, heliostat arrays + s-CO₂ Brayton + molten-salt storage. Commercial fusion deployment marks the final transition from solar dependence to autonomous fusion energy and creates a physical basis for large-scale deep-space power export.


### 3.6 Validation Items and Success Criteria

The validation items below are specific to this volume, Volume III. They inherit P0 results from Volume I and provide boundary conditions for subsequent volumes. All are integrated into Main Volume VII P0/P1/P2/P3 framework.

| ID | Item | Validation Method | Success Standard |
|:-----|:-----|:-----|:-----|
| **P1-E1** | Heliostat tracking precision and dust-related attenuation | Continuous heliostat-array operation for >=12 months under lunar-vacuum and lunar-dust conditions, including at least 6 daytime months | Tracking precision maintained <=0.5 mrad and mirror reflectivity attenuation from dust <=5% |
| **P1-E2** | Lunar startup of supercritical CO₂ turbine | Ground vacuum-chamber test of full-power operation >=10 MWe for >=100 h continuous run | Validate startup, acceleration, grid tie, and load regulation in simulated lunar thermal-vacuum conditions, with focus on dry gas bearing load capacity and stability under 1/6 g |
| **P1-E3** | Cross-lunar-night thermal retention of molten-salt tanks | Simulated 14-day lunar-night heat-loss test in ground vacuum chamber using 1:10 scaled storage tank with MLI insulation and vacuum annulus | Heat loss from 565°C to about 350°C <=2% per day. Full-scale tanks have larger thermal inertia, so actual loss is expected lower than scaled extrapolation |
| **P2-E1** | Long-term performance of radiative panels | Accelerated aging test of carbon-carbon composite panels under simulated lunar vacuum, UV, and thermal cycling | Determine ten-year-scale degradation rate of heat-rejection performance |
| **P2-E2** | Durability of splitter coatings | Accelerated aging of dichroic dielectric coatings under simulated lunar vacuum, UV, and SPE proton irradiation with active cooling, about 100°C-150°C | Determine five-year-scale optical-performance degradation rate |
| **P2-E3** | Lunar suitability of adaptive optics | Long-term reliability tests, >=10^6 cycles, of adaptive-optics collimation under simulated lunar thermal vacuum and dust | Validate wavefront-correction precision and long-term actuator reliability of deformable mirrors |
| **P2-E4** | Lunar-vacuum thermal management of solid-state transformers | 1:1 transformer prototype tested in ground vacuum chamber at full power for >=100 h continuous run | Validate heat rejection and insulation reliability under simulated lunar vacuum and low gravity. Confirm SiC junction temperature <=175°C and aging rate of epoxy encapsulation under prolonged partial discharge |


### 3.7 Parameter Outputs

| Parameter | Value | Status | Receiving Volume |
|:-----|:-----|:-----|:-----|
| Near-term peak power demand | 100 kWe-1 MWe | Design baseline | Volume II, infrastructure construction; Volume V, manufacturing system |
| Long-term peak power demand | 5-50 MWe | Order-of-magnitude estimate | Volume II, co-generation hub sizing; Volume V, full-load production |
| Lunar-city-stage peak power demand | 100-500 MWe, long-term gigawatt class | Visionary estimate | Volume X, new civilization node |
| Heliostat total collection area, Phase I | about 50,000 m² | Design baseline | Volume II, skylight platform area reservation |
| Heliostat total collection area, Phase II | about 100,000 m² | Design target | Volume II, skylight platform area reservation |
| Heliostat siting constraints | Heat-transfer distance <=500 m and optical-path connectivity | Design principle | Volume II, skylight infrastructure planning |
| Solar-spectrum data baseline | ASTM E490-00a AM0 solar spectrum [3] | Design baseline | Volume VII, equivalent-efficiency calculations for light conduits |
| High-temperature heat transmission efficiency with MLI | Heat-loss rate <0.01% over kilometer class distances | Design target | Volume II, functional zoning; Volume V, industrial thermal network |
| Long-term short-distance electric transmission efficiency | Loss <0.1%, under 100 m | Design baseline | Volume II, underground equipment layout |
| Natural-light conduit service radius, reflective mode | High-efficiency zone, >50% efficiency, radius <=500 m | Design baseline | Volume II, underground functional zoning; Volume VII, lighting design |
| Natural-light conduit service radius, collimated + straight mode | High-efficiency near-lossless zone extendable to kilometer class | Long-term flexibility target | Volume II, straight-segment lava-tube evaluation; Volume III siting via GPR data |
| Practical length of flexible optical cable | <=20 m | Design baseline | Volume VII, terminal lighting design |
| Single-unit power of s-CO₂ turbine | 10-25 MWe | Design baseline | Volume V, industrial electric load |
| Molten-salt storage capacity, Phase I | 12 h, about 120 MWhe equivalent | Design baseline | Volume II, underground tank space reservation |
| Molten-salt storage capacity, Phase II | 24 h, about 240 MWhe equivalent | Design target | Volume II, underground tank space reservation |
| High-temperature molten-salt temperature | about 565°C storage and 700-750°C turbine inlet | Design baseline | Volume IV, water-ice extraction; Volume V, smelting and sintering |
| Low-grade waste-heat temperature from reactors and plant | about 30°C-50°C | Design baseline | Volume II, capillary heating interface |
| Main T&D voltage classes | ±10 kV DC internal and ±100 kV DC long distance | Design baseline | Volume VI, traction supply for orbital transport |
| Superconducting transmission applicability | Long-term single circuit >100 MWe or distance >100 km | Long-term upgrade option | Volume VI, traction supply for orbital transport |
| Helium-3 fusion deployment stage | Late Stage IV, about Years 30-35 | Vision positioning | Volume IV, helium-3 extraction; Volume IX, helium-3 export revenue |


### 3.8 Conclusion of Volume III

This volume completes the full energy-system roadmap for lunar industry, from the distributed near-term combination of PV + nuclear + storage at hundreds-of-kilowatts scale in early infrastructure phases, to centralized thermal-electric-light co-generation at tens-of-megawatts scale in mature industrialization, and ultimately to gigawatt-class helium-3 fusion in late Stage IV. It covers the complete demand curve from "habitable" to "self-sustaining" to "large-scale external power export."

Core conclusions:

1. **Base energy demand will rise from hundred-kilowatt class to tens-of-megawatts class within 30 years, and to gigawatt class in the long term.** This growth is an inevitable result of simultaneous expansion in population, from 20 to 10,000, and industry, from 3D printing to full heavy-industry chains, and requires reserving power corridors and thermal-storage spaces from the earliest infrastructure stage.

2. **Near term should adopt PV + nuclear + storage as the reliable combination.** This scheme has high technology readiness, both PV and Kilopower-class reactors [1] already having ground and in-orbit validation, and suits medium power and high reliability requirements in infrastructure phases. Low-grade reactor waste heat should be connected to base heating loops from Infrastructure Phase II onward to replace part of heat-pump electricity use.

3. **Long term should use the thermal-electric-light co-generation hub as the ultimate architecture.** A lunar heliostat array serves as unified solar-thermal front end, supercritical CO₂ Brayton cycle as high-efficiency generation core [2][4], high-temperature molten-salt storage as cross-lunar-night energy buffer, spectral splitters extracting "cold light" for underground natural illumination, and turbine extraction plus reactor waste heat supplying process and heating loads across 30°C to 750°C. This architecture increases generation efficiency from roughly 20%-30% in traditional PV-only pathways to above 50%, increases total energy-utilization efficiency to above 85%, and turns natural illumination into a near-zero-marginal-cost byproduct of generation.

4. **The transmission/distribution architecture balances near-term practicality and long-term foresight.** Voltage classes are selected based on IEC 60038 to ensure global industrial and habitation compatibility. All grid-tied nodes use triple protection, anti-reverse diode, remote breaker, manual isolator, to ensure absolute electrical safety. Long-term provisions include superconducting DC upgrades for remote ultra-high-power transfer and MHD DC interconnection interfaces for helium-3 fusion, explicitly leveraging lunar low-temperature environmental advantage.

5. **Heliostat fields and concentrator towers have engineering siting flexibility.** Core constraints are heat-transfer distance and optical connectivity, not strict colocating over skylights. When skylight space is limited or terrain is unfavorable, mirror fields and towers can be deployed on flat areas hundreds of meters away and linked to underground rooms through short thermal/optical paths.

6. **Evaluated transmission efficiencies of heat, power, and light determine underground-city spatial layout.** **Heat** can be delivered near-losslessly via MLI-insulated pipelines, allowing flexible industrial siting; **power** has very low loss over short underground distances, supporting safe underground placement of generation equipment; **natural light** has strong short-term advantages within 500 m in reflective conduits, constraining near-term habitation layouts, but this can be broken in suitable geological zones through **adaptive-optics collimation + straight conduits** to enable kilometer-class near-lossless transmission.

7. **Splitter operating temperatures must be treated realistically.** In lunar vacuum, even small optical absorption in dichroic splitters, about 0.1%-0.5%, can yield equilibrium temperatures around 150°C-250°C. Active cooling is necessary to keep temperatures in safe ranges, around 100°C-150°C, and to ensure coating lifetimes above ten years.

8. **Natural thermal-rejection synergy exists between polar solar-thermal plants and crater mining.** Large quantities of low-grade plant waste heat can be piped into nearby permanently shadowed extraction zones as effectively "free" process heat for water-ice extraction, reducing electric heating dependence. Detailed pipeline schemes are developed in Volume IV.

9. **Helium-3 fusion is the ultimate closed-loop path beyond heliostat physical limits.** When demand enters gigawatt class, D-3He plants [11][12] fueled by locally extracted helium-3 [13] can integrate direct MHD generation and cascaded waste-heat utilization, creating seamless continuity with thermal-electric-light systems. This marks transition from solar dependence to autonomous fusion energy and enables large-scale deep-space power export.

10. **All implementation schemes in this volume explicitly list additional real-world engineering constraints at the end of related sections**, including long-distance pumping of high-temperature fluids, excavation/alignment for straight light conduits, vacuum maintenance, power-redundancy switching, and sectional isolation of thermal networks. These factors do not invalidate physical feasibility but require explicit space allocation and construction planning in detailed designs of Volumes II, IV, V, and VII.


### References

[1] NASA. Kilopower/KRUSTY Project: Fission Power for Space Exploration. 2018. https://www.nasa.gov

[2] Dostal, V., et al. A Supercritical Carbon Dioxide Cycle for Next Generation Nuclear Reactors. MIT-ANP-TR-100, 2004.

[3] ASTM International. ASTM E490-00a(2019) - Standard Solar Constant and Zero Air Mass Solar Spectral Irradiance Tables. 2019.

[4] Turchi, C. S., et al. Supercritical CO₂ Brayton Cycles for CSP and Nuclear Applications. NREL/PR-5500-61234, 2013.

[5] Ho, C. K., and Iverson, B. D. Review of high-temperature central receiver designs for concentrating solar power. Renewable and Sustainable Energy Reviews, Vol. 29, 2014, pp. 835-846.

[6] Calvet, N., et al. Compatibility of containment materials with molten salt for CSP plants. Energy Procedia, Vol. 49, 2014, pp. 752-761.

[7] Kawamoto, H., and Shibata, T. Electrostatic cleaning system for removing dust adhering to solar panels on a planetary base. Journal of Electrostatics, Vol. 73, 2015, pp. 54-60.

[8] Boltzmann, L. Ableitung des Stefan'schen Gesetzes, betreffend die Abhängigkeit der Wärmestrahlung von der Temperatur aus der electromagnetischen Lichttheorie. Annalen der Physik, Vol. 258, 1884, pp. 291-294.

[9] Zhao, S., Sun, W., Zhuang, K., et al. Study on long-life lunar-base nuclear power reactor core physics based on annular fuel. Atomic Energy Science and Technology, 2025, 59(1): 1-13.

[10] Ingersoll, D. T., and Carelli, M. D., Eds. Handbook of Small Modular Nuclear Reactors, Second Edition. Woodhead Publishing, 2021.

[11] Motevalli, S. M., and Fadaei, F. A comparison between the burn condition of deuterium-tritium and deuterium-helium-3 reaction and stability limits. Fundamental Plasma Physics, 2025, 14: 100070.

[12] Bahmani, J. The effect of fundamental quantities of the deuterium-helium-3 fusion reaction in tokamak. Visnyk of V.N. Karazin Kharkiv National University, 2025, 42: 48-59.

[13] Wittenberg, L. J., et al. A review of 3He resources and acquisition for use as fusion fuel. Fusion Technology, 1992, 21(4): 2230-2253.

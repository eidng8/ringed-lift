# Appendix III: Engineering Project Discussion

## Volume III: Lunar Assembly Base and Long-Term Industrial Outlook

**Version**: 1.2<br/>
**Date of Preparation**: June 2026<br/>
**Currency Unit**: Renminbi (RMB), symbol: ¥<br/>
**Related Main Volumes**: Appendix I Volume V; Appendix I Volume X<br/>
**Prerequisite Reading**: Appendix III Volume II (Lunar Surface Railway Transportation Network)


### Glossary of Abbreviations

| Abbreviation | Full Name | Notes |
|------|----------|------|
| CNT | Carbon Nanotube | Core material for ring elevators and lunar industry |
| EDS | Electric Dust Shield | Electrostatic dust removal |
| ISRU | In-Situ Resource Utilization | Utilizing local resources on the lunar surface |
| LCC | Life Cycle Cost | Life Cycle Cost |
| MLI | Multi-Layer Insulation | Passive thermal control material |
| NEA | Near-Earth Asteroid | Near-Earth Asteroid |
| PGM | Platinum Group Metals | Platinum, palladium, rhodium, iridium, osmium, ruthenium |
| PSR | Permanently Shadowed Region | Water ice accumulation zone at the poles |
| SPA | South Pole–Aitken Basin | The largest impact basin on the Moon |


### 1.1 Volume Preamble

This volume focuses on a feasibility analysis of the Moon as an assembly base and the long-term industrial outlook. Building upon the logistics infrastructure of Appendix III Volume II (Lunar Surface Railway Transportation Network), this volume works from three application scenarios—**base self-use**, **deep space launch**, and **research facilities**—decomposing down to the component level, to determine which items must be transported from Earth and which can be manufactured in situ on the Moon. At the same time, this volume provides an outlook on the priority of high-value production lines that may eventually settle on the Moon in the long term, and introduces asteroid belt resources as a supplementary raw material source.

All analyses in this volume are based on the **steady-state operating period after the Lunar Industrial System is fundamentally established** (Years 15–25), assuming that the lunar surface already has basic smelting, 3D printing, and limited chemical engineering capabilities.


### 1.2 Assessment Premises

- The lunar surface has established: aluminum alloy smelting, crude iron and steel smelting, sintered regolith bricks/concrete, water ice electrolysis to produce hydrogen and oxygen, Sabatier process to produce methane, and sulfur extraction.
- The lunar surface **does not have**: polymer materials (rubber, plastics, resins), semiconductor manufacturing, precision bearings, high-purity rare-earth permanent magnets, optical glass, carbon fiber, or superconducting tape.
- The lunar surface **has limited capability for**: large-scale extrusion/rolling (equipment transported from Earth), metal 3D printing (powder must be supplemented from Earth), and simple chemical engineering (methane, nitrogen, sulfur).


### 1.3 List of Components That Must Be Transported from Earth (Core Gaps)

Regardless of what product is being manufactured, the following **component-level** materials must be shipped from Earth in finished or semi-finished form:

| Category | Specific Items | Reason They Cannot Be Manufactured In Situ |
|:---|:---|:---|
| **Microelectronics** | Chips (FPGA, CPU, MCU, ADC, RF IC), memory | Semiconductor manufacturing cannot be replicated |
| **Precision electromechanical** | Bearings (Grade P4 and above), gears, turbopumps, valves | Precision, materials, and heat treatment cannot be met |
| **Optical components** | Lenses, mirrors, optical fiber, lasers, star trackers | Optical glass manufacturing requires extreme precision |
| **Polymer materials** | Rubber seals, plastic parts, adhesives, cable insulation, MLI film | No organic chemical engineering |
| **High-performance metals** | Superalloys (Inconel), high-strength steel (wheel steel), permanent magnets (NdFeB) | Trace elements cannot be sourced locally |
| **Composite materials** | Carbon fiber prepregs, aramid fiber, glass fiber | Cannot manufacture fibers |
| **Superconducting materials** | YBCO tape | Cannot be manufactured |
| **Chemical reagents** | Catalysts (Pt, Ni), electrolytes, refrigerants | Cannot be refined |
| **Copper/copper alloys** | Wires, cables, motor windings | Copper content in lunar regolith is extremely low (<50 ppm) |


### 1.4 Volume and Weight Constraints of Earth Launches

Typical dimensions of heavy-lift rocket payload fairings: diameter 5–9 m, length 18–25 m (Starship: 9 m × 18 m; Long March 9: 7–8 m × 20–25 m). Conclusions:

- Structural components with length ≤20 m and diameter ≤8 m can be launched in one piece
- Structural components with length >20 m (such as a single EMU car body at 25 m) or diameter >9 m must be broken down into modules for welding and assembly on the lunar surface


### 1.5 List of Items That Can Be Manufactured In Situ (on the Lunar Surface)

| Category | Specific Items | Conditions |
|:---|:---|:---|
| **Structural metals** | Aluminum profiles, steel rails, structural steel, large castings | Requires rolling mills, forging presses, and tooling transported from Earth |
| **Simple mechanical parts** | Brackets, housings, flanges, bolts (rough machined) | Requires cutting tools transported from Earth |
| **Welded structures** | Trusses, tank cylinder sections, pipelines | Requires welding equipment transported from Earth |
| **Regolith construction materials** | Sintered bricks, sulfur concrete, roads | Mature |
| **Water/oxygen/hydrogen/methane** | Propellant, life support | Requires water ice and carbon source |
| **Simple metal powder (3D printing)** | Aluminum, iron, titanium powder | Requires ball milling equipment; powder can be produced locally |
| **Nitrogen gas** | Pipeline fill, welding shielding gas | Extracted from regolith volatiles |
| **Ordinary glass (soda-lime)** | Window glass, containers | Regolith contains SiO₂, CaO, Na₂O; requires glass melting furnace and molds from Earth |
| **Solar-grade polysilicon (6N)** | Local photovoltaic cells | Requires Siemens-process reduction furnace and wire saw from Earth; efficiency 15–18% |
| **Crude copper** | Wires, motor windings | If M-type asteroid copper supplementation is available, can be cast and drawn; but refined and high-purity copper wire still requires Earth |


### 1.6 Feasibility of Deploying Large Equipment (Such as Presses) on the Lunar Surface

#### 1.6.1 Typical Dimensions and Mass of Large Industrial Machine Tools

Using an **80 MN aluminum profile extrusion press** required to produce EMU car body profiles as an example:

| Component | Approximate Dimensions | Mass (tons) | Decomposable Modules |
|:---|:---|:---|:---|
| Main frame (prestressed wire winding) | 8×4×3 m | 200–300 | Can be divided into 2–4 blocks |
| Main cylinder | 2×2×8 m | 50–80 | Whole or segmented |
| Extrusion container | 1.5×1.5×3 m | 30–50 | Whole |
| Shearing device | 3×2×2 m | 20–30 | Whole |
| Hydraulic station | 5×3×3 m | 40–60 | Can be modular |
| Control system | 2×2×2 m | 5–10 | Whole |
| **Total** | — | **approximately 400–600 tons** | — |

#### 1.6.2 Rocket Carrying Capacity Feasibility

- Heavy-lift rockets (Starship/Long March 9) have an LEO carrying capacity of approximately 100–150 tons, and a Trans-Lunar Injection (TLI) carrying capacity of approximately 50–80 tons.
- Transportation to the lunar surface requires multiple launches. Using **maximum module ≤50 tons** (TLI capability) as the benchmark after modular decomposition, a complete extrusion press requires **10–15** heavy-lift rocket launches.
- Module dimensions can be controlled to ≤8×4×4 m, compatible with the payload fairing (diameter 9 m, length 18 m).

#### 1.6.3 Lunar Surface Assembly Feasibility

- Under the 1/6 g gravity on the lunar surface, hoisting, alignment, and positioning of large modules are significantly easier.
- Using a combination of **large-diameter bolted connections + welding** (friction stir welding), structural strength can meet requirements.
- The foundation requires pre-cast regolith concrete footings (thickness ≥1 m) with pre-embedded anchor bolts.

#### 1.6.4 Conclusions

**Engineering feasible, physically feasible**. But requires:
- Modular design: decomposed into transportable modules from the design stage
- Multiple launches: 10–15 heavy-lift rockets
- Large lunar surface crane: must be transported from Earth, also modular
- Overall economics: reasonable when amortized for mass production (e.g., all aluminum profiles needed to build hundreds of kilometers of railway); uneconomical for a single unit used only for experiments


### 1.7 Feasibility of Manufacturing Glass, Optical Fiber, and Monocrystalline Silicon on the Lunar Surface

| Product | Raw Material Source | Technical Threshold | Feasibility | Export Competitiveness |
|:---|:---|:---|:---|:---|
| **Ordinary glass (window glass, containers)** | Lunar regolith SiO₂, CaO, Na₂O sufficient | Low. Requires melting furnace (1,500°C), molds, annealing furnace | ✅ Feasible, for lunar surface local construction | Low export value (high mass, low value) |
| **Optical glass (lenses, prisms)** | Requires extremely high purity, special doping (La, Ta, Nb, etc.) | Extremely high. Requires precise control of bubbles, striae, and refractive index | ❌ Not feasible, dependent on Earth | — |
| **Fused silica (optical fiber preform)** | High-purity SiO₂ (>99.999%), doped Ge, F, etc. | High. Requires chemical vapor deposition (MCVD), precision draw tower | ❌ Not feasible, no relevant equipment on lunar surface | — |
| **Optical fiber** | Preform + draw tower + coating | High. Drawing diameter 125 μm±1 μm; coating requires UV-curable resin | ❌ Not feasible, core equipment cannot be manufactured on lunar surface | — |
| **Polysilicon (solar-grade, 6N)** | Lunar regolith SiO₂ → metallurgical silicon → Siemens reduction | Medium. Requires reduction furnace, ingot casting furnace, wire saw | ⚠️ Feasible but equipment transported from Earth; high energy consumption | Earth polysilicon production is oversupplied; no competitive advantage |
| **Monocrystalline silicon (semiconductor-grade, 11N)** | Polysilicon + Czochralski/float-zone method | Extremely high. Requires high-purity quartz crucibles, ultra-high vacuum, precision temperature control | ❌ Not feasible. Vibration, radiation, and cleanliness on the lunar surface do not meet requirements | Permanently dependent on Earth |

**Conclusions**:
- Ordinary glass can be manufactured on the lunar surface for use in base construction.
- Optical fiber, optical glass, and semiconductor-grade monocrystalline silicon **should not be manufactured on the Moon** and are permanently dependent on Earth.
- Solar-grade polysilicon can supplement local photovoltaics on the lunar surface, but is not suitable for export.


### 1.8 Additional Feasible Production Lines After Asteroid Supplementation

Based on asteroid belt resources (C-type, M-type, S-type) that can provide **carbon, nitrogen, water, platinum group metals, nickel, cobalt, copper, and some rare earth elements** and other key raw materials. Some production lines that were previously infeasible due to raw material shortages can be upgraded to feasible.

#### Assessment of New/Upgraded Production Lines

| Production Line Type | Original Feasibility (Without Asteroids) | After Asteroid Supplementation | Key Dependencies | Recommended Timeline |
|:---|:---:|:---:|:---|:---:|
| **CNT-reinforced composite materials** | ❌ Not feasible (lack of carbon) | ✅ **Feasible** | C-type asteroid carbon source + iron/nickel catalyst (asteroid) | Years 15–25 |
| **Carbon fiber structural parts** | ❌ Not feasible (lack of carbon, lack of polymer) | ⚠️ **Partially feasible** | Carbon fiber requires polyacrylonitrile (PAN) precursor, still dependent on Earth; but pitch-based carbon fiber can be attempted | Long-term (2050+) |
| **Copper wire/motor windings** | ❌ Not feasible (lack of copper) | ✅ **Feasible** | M-type asteroid copper ore (copper content can reach 5–10%), lunar surface casting and drawing | Years 15–25 |
| **Nickel-cobalt superalloys** | ❌ Not feasible (lack of Ni, Co) | ✅ **Feasible** | M-type asteroids rich in Ni, Co; can manufacture rocket engine components | Years 20–30 |
| **Platinum group metal refining** | ❌ Not feasible (lack of PGM) | ✅ **Feasible** | M-type asteroid PGM content (platinum, palladium, rhodium, etc.), for catalysts and electronic contacts | Years 20–30 |
| **Rare-earth permanent magnets (NdFeB)** | ❌ Not feasible (lack of rare earths) | ⚠️ **Limitedly feasible** | Asteroid rare earth abundance uncertain, requires survey; if abundance is sufficient, a permanent magnet production line can be established | Long-term (2050+) |
| **C/SiC ceramics** | ⚠️ Limitedly feasible | ✅ **Feasible** | C-type asteroid carbon source + lunar silicon; can be manufactured at scale | Years 20–30 |
| **Stainless steel (containing Cr, Ni)** | ⚠️ Limitedly feasible (lack of Cr, Ni) | ✅ **Feasible** | M-type asteroids provide Cr, Ni; can produce 304/316 stainless steel | Years 15–25 |
| **CIGS thin-film solar cells** | ❌ Not feasible (lack of In, Ga, Se) | ⚠️ **Partially feasible** | Asteroids may provide, but abundance is low and economics are poor | Not recommended |
| **Polymer materials (polyethylene, rubber)** | ❌ Not feasible (lack of carbon) | ❌ **Still not feasible** | Requires petrochemical routes; carbon source insufficient for conversion to olefin monomers | Permanently dependent on Earth |

**Updated Long-Term Production Line Settlement Priority Matrix** (including asteroid supplementation):

| Priority | Production Line Type | Engineering Feasibility | Economics | Strategic Value | Asteroid Dependency | Recommended Timeline |
|:---:|:---|:---:|:---:|:---:|:---:|:---|
| **1** | Large space structure manufacturing | ★★★★★ | ★★★★★ | ★★★★★ | Low | Years 10–15 |
| **2** | Propellant and bulk chemicals | ★★★★★ | ★★★★★ | ★★★★★ | Medium (carbon source) | Years 10–15 |
| **3** | Lunar surface specialty construction materials | ★★★★☆ | ★★★☆☆ | ★★★☆☆ | Low | Years 5–10 |
| **4** | Basic metal smelting (aluminum, iron, titanium) | ★★★☆☆ | ★★★☆☆ | ★★★☆☆ | Low | Years 10–20 |
| **5** | Copper wire/motor windings (asteroid supplementation) | ★★★☆☆ | ★★★★☆ | ★★★★☆ | High | Years 15–25 |
| **6** | Nickel-cobalt superalloys (asteroid supplementation) | ★★★☆☆ | ★★★★☆ | ★★★★☆ | High | Years 20–30 |
| **7** | CNT-reinforced composites (asteroid supplementation) | ★★★★☆ | ★★★★☆ | ★★★★☆ | High | Years 15–25 |
| **8** | Platinum group metal refining (asteroid supplementation) | ★★★☆☆ | ★★★★★ | ★★★★★ | High | Years 20–30 |
| **9** | Stainless steel (Cr, Ni) (asteroid supplementation) | ★★★☆☆ | ★★★☆☆ | ★★★☆☆ | High | Years 15–25 |
| **10** | Ordinary glass/polysilicon (local photovoltaics) | ★★★☆☆ | ★★☆☆☆ | ★★★☆☆ | Low | Years 15–25 |
| **11** | C/SiC ceramics (asteroid supplementation) | ★★★☆☆ | ★★★☆☆ | ★★★☆☆ | Medium | Years 20–30 |
| **12** | Rare-earth permanent magnets (asteroid supplementation) | ★★☆☆☆ | ★★☆☆☆ | ★★★☆☆ | High | Long-term |
| — | Precision manufacturing (chips, bearings, optics) | ★☆☆☆☆ | ★☆☆☆☆ | ☆☆☆☆☆ | High | **Not recommended** |
| — | Polymer materials (polyethylene, rubber) | ★☆☆☆☆ | ☆☆☆☆☆ | ★☆☆☆☆ | High | **Not recommended** |


### 1.9 Feasibility Classification for Industrial Machine Tools Settling on the Moon

#### 1.9.1 Industrial Machine Tools That Can Settle on the Moon (Engineering Feasible, Economically Acceptable)

Common features of these machine tools: **high structural strength, maximum module size and weight after modular decomposition is compatible with launch vehicles, and lunar surface assembly technology is mature**.

| Category | Typical Equipment | Decomposability | Transportation Feasibility | Lunar Surface Assembly Feasibility |
|:---|:---|:---:|:---:|:---:|
| **Metal forming** | Large extrusion press (80 MN) | ✅ Main frame divided into 2–4 blocks | ✅ Maximum module ≤50 t | ✅ Large bolts + welding |
| **Metal forming** | Large stamping press (500 t) | ✅ Frame divided into sections | ✅ Same as above | ✅ Same as above |
| **Metal forming** | Die forging hammer | ✅ Frame divided into sections | ✅ Same as above | ✅ Same as above |
| **Metal forming** | Steel rolling mill (rail rolling mill) | ✅ Rolls and housings separate | ✅ Same as above | ✅ Same as above |
| **Casting** | Large electric arc furnace (10–50 t) | ✅ Furnace body in sections | ✅ Shell welded on-site | ✅ Welding + refractory material casting |
| **Casting** | Medium-frequency induction melting furnace | ✅ Furnace body, coil, power supply separate | ✅ Power supply cabinet as whole unit | ✅ Coil wound on lunar surface |
| **Machining** | Large gantry boring and milling machine (worktable >10 m) | ✅ Cross beam divided into 2–3 sections | ✅ Maximum module ≤20 t | ✅ Guideway connection precision 0.01 mm |
| **Machining** | Large vertical lathe (machining diameter >5 m) | ✅ Column, cross beam, worktable separate | ✅ Same as above | ✅ Same as above |
| **Machining** | CNC horizontal lathe (medium-small) | ✅ Bed, headstock, tailstock separate | ✅ Transport as whole unit (≤10 t) | ✅ Only alignment required |
| **Welding** | Friction stir welding equipment (large) | ✅ Frame in sections | ✅ Maximum module ≤15 t | ✅ Lunar vacuum is advantageous |
| **Additive manufacturing** | Metal 3D printer (SLM) | ✅ Complete machine (≤5 t) | ✅ Transport as whole unit | ✅ Direct commissioning upon unpacking |

**Additional problems to be resolved**:
- **Foundation and vibration**: Large stamping presses and forging hammers require heavy concrete foundations. Regolith concrete can be cast on the lunar surface (compressive strength ≥20 MPa), thickness ≥1 m, with pre-embedded anchor bolts.
- **Lubrication and sealing**: Moving components require MoS₂ solid lubrication or self-lubricating materials (bronze-graphite). Hydraulic systems require vacuum-compatible seals (PTFE + spring-energized).
- **Thermal dissipation**: High-power equipment requires water cooling, which can connect to the lunar surface water-cooling pipe network.
- **Lunar dust protection**: Precision guideways and lead screws require elastic dust covers; the entire machine tool can be placed inside a fully enclosed workshop.

#### 1.9.2 Machine Tools Extremely Difficult to Settle on the Moon (or Never Possible)

| Category | Typical Equipment | Reason Cannot Settle |
|:---|:---|:---|
| **Semiconductor manufacturing** | Photolithography machines (DUV/EUV) | Requires ultra-clean environment (ISO Class 1), nanometer-level vibration isolation, ultrapure water, large quantities of specialty chemicals |
| **Semiconductor manufacturing** | CVD/PVD | Requires ultra-high vacuum (10⁻⁹ Torr), specialty gases; lunar surface cannot self-supply spare parts |
| **Semiconductor manufacturing** | Ion implanter | Requires ultra-high vacuum, high-voltage stability, specialty source materials |
| **Ultra-precision machining** | Single-point diamond lathe | Requires nanometer-level vibration isolation, constant temperature and humidity (±0.1°C) |
| **Optical manufacturing** | Large optical polishing machine | Requires dust-free environment, constant temperature, long-term stability |
| **Carbon fiber production** | Carbonization furnace, graphitization furnace | Requires polyacrylonitrile (PAN) precursor; cannot be produced on the lunar surface |
| **Polymer materials** | Polymerization reactor | Requires petrochemical feedstocks (ethylene, propylene); lunar surface cannot supply them |
| **Precision bearings** | Bearing grinding super-finishing machine | Equipment can be transported, but bearing steel cannot be smelted on the lunar surface, rendering the machine useless |

**Conclusion**: **Semiconductor manufacturing, ultra-precision optics, carbon fiber precursor, and polymer synthesis** — these four categories of production line machine tools can never (or are not worth) settling on the Moon.


### 1.10 Production Workshop Environment Requirements and Layout Plan

The design of lunar production workshops must simultaneously satisfy **equipment operating environment requirements**, **product quality control requirements**, and **personnel safety requirements**. Since the lunar surface environment (vacuum, extreme low temperatures, intense radiation, lunar dust, micrometeorites) differs greatly from Earth, workshop layouts must be tiered by production type.

#### 1.10.1 Workshop Classification and Environment Requirements

| Workshop Type | Typical Production Lines | Environment Requirements | Recommended Location | Rationale |
|:---|:---|:---|:---|:---|
| **Precision manufacturing workshop** | Chip packaging, sensor calibration, optical component assembly, electronic equipment final assembly | Constant temperature (20±1°C), constant humidity (40–50% RH), constant pressure (70±1 kPa), ISO Class 5 cleanroom (Class 100) | Underground lava tube (depth ≥50 m) | Natural radiation shielding, minimal temperature differential, no micrometeorite risk, excellent vibration isolation |
| **Machining workshop** | CNC machine tools, large gantry milling machines, 3D printing | Constant temperature (20±5°C), dust-controlled (ISO Class 7, Class 10,000), dry | Underground lava tube (shallow) or semi-recessed surface | Requires lunar dust protection, but cleanliness requirements lower than precision workshop |
| **Metal forming workshop** | Extrusion, stamping, forging, rolling | Temperature controlled (10–30°C), dust-controlled (ISO Class 8, Class 100,000), ventilated | **Surface** (semi-recessed or earthen dome) | Equipment is heavy with high vibration and requires large space; difficult to accommodate underground |
| **Casting/smelting workshop** | Electric arc furnace, medium-frequency furnace, casting | High-temperature work area, ventilation, heat insulation, dust-controlled (ISO Class 8) | **Surface** (independent workshop, far from other facilities) | High temperatures, exhaust gases, vibration; must be isolated from precision workshops |
| **Welding/assembly workshop** | Friction stir welding, TIG welding, large structure final assembly | Temperature controlled (10–30°C), ventilated (welding fumes), dust-controlled (ISO Class 8) | **Surface** (large factory building) | Requires large-span space (>20 m); lava tube height may be insufficient |
| **Materials storage** | Metal ingots, powders, chemical reagents | Dry, dust-controlled, segregated storage by zone | Underground (constant temperature and humidity) | Naturally constant temperature; reduces energy consumption |
| **Finished goods storage** | Products awaiting launch or transport | Dry, dust-controlled | Underground or semi-recessed surface | Can be selected based on product requirements |

#### 1.10.2 Division of Labor Between Underground and Surface Workshops

| Characteristic | Underground Lava Tube Workshop | Surface Semi-Recessed Workshop (Earthen Dome) |
|:---|:---|:---|
| **Applicable workshop types** | Precision manufacturing, machining, materials storage, finished goods storage | Metal forming, casting/smelting, welding/assembly, large final assembly |
| **Environmental stability** | Excellent (constant temperature −20°C to −30°C; achieves 20±1°C after temperature control) | Average (requires active temperature control; affected by lunar day/night cycle) |
| **Radiation protection** | Natural (≥30 m of rock above) | Artificial (≥2 m of regolith overburden) |
| **Space dimensions** | Limited by natural lava tube dimensions (width ≤20 m, height ≤10 m) | Expandable (dome span can reach 50 m) |
| **Equipment hoisting** | Difficult (must transport vertically through skylights) | Convenient (can be hoisted directly from the surface) |
| **Vibration isolation** | Excellent (rock layer absorbs vibration) | Average (requires independent foundation) |
| **Lunar dust protection** | Natural isolation (decontamination transition section at entrance) | Active decontamination required (airlock + electrostatics) |
| **Typical span** | ≤20 m | 10–50 m |
| **Typical height** | ≤15 m | 10–30 m |

**Site Selection Principles**:
- **Precision manufacturing, machining, electronics final assembly** → Prioritize underground (lava tube), utilizing natural constant temperature, humidity, and radiation shielding
- **Casting, smelting, large stamping, heavy forging** → Must be on surface (semi-recessed), utilizing large space and convenient equipment transport
- **Welding, large final assembly** → Large surface factory buildings; if underground lava tube has sufficient height (≥15 m) and width (≥20 m), can also be considered

#### 1.10.3 Underground Workshop Environmental Control Requirements

The natural temperature of underground lava tubes is approximately −20°C to −30°C; active temperature control is required to meet production requirements.

| Parameter | Precision Manufacturing Workshop | Machining Workshop | Control Method |
|:---|:---|:---|:---|
| Temperature | 20±1°C | 20±5°C | Heat pump (rock layer as constant-temperature cold source) + electric supplemental heating |
| Relative humidity | 40–50% RH | ≤60% RH | Dehumidifier (condensing type) + desiccant |
| Pressure | 70±1 kPa (slightly above exterior) | 70±2 kPa | Airlock chamber + automatic gas makeup system |
| Cleanliness (ISO 14644) | ISO Class 5 (Class 100) | ISO Class 7 (Class 10,000) | HEPA filtration + positive pressure maintenance + personnel changing rooms/air shower |
| Illuminance | 500–1,000 lx | 300–500 lx | Industrial LED lighting |
| Vibration | <0.1 µm/s (precision equipment) | <1 µm/s | Independent vibration-isolating foundations + natural rock layer isolation |

**Underground Workshop Structure Schematic** (using precision manufacturing workshop as an example, from exterior to interior):

- Basalt layer at top of lava tube
- MLI insulation layer (50 mm)
- SPUA sealing layer (5 mm)
- CFRP structural layer (3 mm)
- Constant temperature/humidity cleanroom
   - Temperature: 20±1°C
   - Humidity: 45±5% RH
   - Pressure: 70±1 kPa
   - Cleanliness: ISO Class 5
   - Equipment: precision machine tools / assembly tables
- Rock layer at bottom of lava tube

#### 1.10.4 Surface Workshop Environmental Control Requirements

Surface semi-recessed workshops (earthen dome) are used for large equipment; environmental control requirements are slightly lower than underground workshops, but still require active maintenance.

| Parameter | Metal Forming Workshop | Casting/Smelting Workshop | Welding/Assembly Workshop | Control Method |
|:---|:---|:---|:---|:---|
| Temperature | 10–30°C | Locally high temperature; overall 10–30°C | 10–30°C | Subsurface water-cooling pipe network + ventilation |
| Humidity | Dry (<60% RH) | Dry (<50% RH) | Dry (<60% RH) | Dehumidifier |
| Pressure | 70±2 kPa | 70±2 kPa (local negative pressure) | 70±2 kPa | Airlock chamber |
| Cleanliness | ISO Class 8 | ISO Class 8 (smelting area can be relaxed) | ISO Class 8 | Positive pressure + filtration |
| Illuminance | 300 lx | 200 lx (explosion-proof required in high-temperature areas) | 500 lx | Industrial LED lighting |
| Ventilation | General | **Forced exhaust** (smoke, hot gases) | Local exhaust (welding fumes) | Fan + filtration |

**Surface Workshop Structure Schematic** (semi-recessed earthen dome, from exterior to interior):

- Lunar surface (grade ±0)
- Overburden layer (≥2 m of regolith or sintered bricks)
- Dome (CFRP or steel reticulated shell)
- SPUA sealing layer
- Workshop space
   - Temperature: 10–30°C
   - Pressure: 70±2 kPa
   - Equipment: large extrusion press, gantry crane (20 t)
- Regolith concrete foundation (thickness 1–2 m)

#### 1.10.5 Operating Modes: Fully Automated, Semi-Automated (Remote Control), and Manual

Personnel arrangements in lunar production workshops are divided into three tiers, determined by task complexity and hazard level.

| Operating Mode | Definition | Applicable Scenarios | Personnel Location |
|:---|:---|:---|:---|
| **Fully automated** | Equipment operates autonomously without manual intervention | Repetitive, clearly defined tasks (e.g., sintered brick production line, 3D printing, continuous casting) | No personnel present; monitoring only |
| **Semi-automated (remote control)** | Operators remotely control in real time via remote control console | Tasks requiring human judgment but in dangerous or uninhabitable environments (e.g., operations in front of smelting furnace, large forging hoisting and alignment) | Operator at **remote control center** (underground or surface safe zone) |
| **Manual assistance** | Operator enters the workshop for on-site work | Tasks requiring fine tactile judgment, complex assembly, equipment maintenance, quality sampling | Operator wears lunar suit or pressure suit to enter workshop |

**Remote Control Center Requirements**:
- Located in underground safe zone (natural radiation shielding)
- Equipped with multi-screen display systems (equipment status, multi-angle video, sensor data)
- Control latency must be <100 ms (lunar surface local network)
- Each operator can simultaneously monitor 3–5 pieces of equipment (semi-automated) or 1:1 remote control (high-precision operations)

**Personnel Entry Workshop Requirements**:
- Precision manufacturing workshop: Operators wear **lightweight pressure suits** (similar to astronaut intravehicular activity suits) and enter through airlocks
- Casting/smelting workshop: Operators wear **heat-resistant lunar suits** (with active cooling) and enter through airlocks
- All workshop entrances are equipped with **air shower rooms** (to remove lunar dust) + **electrostatic dust removal**

#### 1.10.6 Workshop Connection with the Lunar Surface Railway Network

All surface and underground workshops should be connected to the lunar surface railway network via **airlock passages**.

| Connection Type | Requirements | Notes |
|:---|:---|:---|
| **Raw material/finished goods transport** | Airlock chamber + automatic docking | Train cars drive directly into workshop unloading area; unloaded after airlock isolation |
| **Personnel passage** | Independent airlock passage | Separated from material passage to ensure safety |
| **Emergency evacuation** | Independent escape passage | Direct access to underground shelter or surface emergency assembly point |

#### 1.10.7 Implementation Recommendations

| Priority | Workshop Type | Recommended Location | Construction Timeline |
|:---|:---|:---|:---|
| **1** | Metal forming workshop (extrusion, stamping) | Surface semi-recessed | Years 10–15 |
| **2** | Welding/large final assembly workshop | Surface semi-recessed | Years 10–15 |
| **3** | Machining workshop (CNC) | Underground lava tube | Years 15–20 |
| **4** | Precision manufacturing workshop | Underground lava tube (depth ≥50 m) | Years 20–25 |
| **5** | Remote control center | Underground safe zone | Years 10–15 |


### 1.11 List of Products That Can Transition to Lunar Manufacturing After Deploying Key Industrial Equipment

Based on the preceding analysis, assuming the Moon has deployed the industrial machine tools listed in Section 1.9.1 and asteroids supplement key raw materials such as carbon, copper, nickel, cobalt, and platinum group metals. The following assesses the substitution rate by product category.

#### 1.11.1 Fully Transferable to Lunar Manufacturing (Raw Materials and Processes Both Feasible)

| Product Category | Original Earth Dependency | Lunar Manufacturing Pathway | Raw Material Source | Required Machine Tools |
|:---|:---|:---|:---|:---|
| **Construction aluminum profiles** | Large extrusion press | Lunar aluminum ingots → extrusion | Lunar regolith | Large extrusion press |
| **Steel rails (U75V)** | Rolling mill, steel billets | Lunar iron → carbon addition + alloying → rolling | Lunar regolith iron + asteroid Mn/Cr | Rolling mill, electric arc furnace |
| **Sintered regolith bricks/concrete** | Already manufacturable | No machine tools needed | Lunar regolith | Sintering furnace, mixer |
| **Large pipelines** | Plate rolling and welding | Aluminum/steel plate rolling and welding | Lunar aluminum/steel | Plate rolling machine, welding equipment |
| **Storage tanks (water, fuel, liquid oxygen)** | Plate rolling and welding | Aluminum/steel tank body welding | Lunar aluminum/steel | Plate rolling machine, welding equipment |
| **Power transmission tower structures (lattice)** | Angle steel rolling + welding | Angle steel rolling → welding | Lunar steel | Rolling mill, welding robots |
| **Rail transit catenary supports** | Aluminum alloy extrusion | Aluminum profile extrusion | Lunar regolith aluminum | Large extrusion press |
| **Track fasteners, bolts (rough)** | Forging + machining | Steel billet die forging → turning | Lunar steel | Die forging hammer, CNC lathe |
| **Equipment brackets, bases, frames** | Casting/welding | Casting or welding | Lunar steel/aluminum | Electric arc furnace, welding equipment |
| **Rocket tank cylinder sections (aluminum alloy)** | Aluminum plate rolling + welding | Aluminum ingots → rolled plate → roll forming and welding | Lunar regolith aluminum | Rolling mill, plate rolling machine, friction stir welding |
| **Space truss units** | Aluminum extrusion + welding | Extruded profiles → welding | Lunar regolith aluminum | Large extrusion press, welding equipment |

#### 1.11.2 Partially Transferable to Lunar Manufacturing (Core Components Still Transported from Earth)

| Product Category | Lunar Manufacturing Portion | Still Transported from Earth | Reason |
|:---|:---|:---|:---|
| **EMU car bodies** | Car body structure (aluminum extrusion + welding) | Wheels, axles, bearings, permanent-magnet motors, IGBTs, air conditioning, interior | Wheel steel requires extremely high purity; permanent magnets require rare earths; interior requires plastics |
| **Lunar rovers/cargo vehicles** | Chassis, body shell | Motors, batteries, control board, tires, bearings | Same as above |
| **Rocket stages** | Tank cylinder sections (aluminum welding) | Engines, turbopumps, valves, electronic controls | Engines require superalloys and precision machining |
| **Liquid oxygen/liquid methane storage tanks (fixed ground)** | Tank body | Valves, seals, liquid level sensors | Valves require precision machining; seals require rubber |
| **Solar power plant trusses** | All metal structures | Solar cell panels, cables, inverters | Cell panels require semiconductor processes |
| **Large radio telescope structures** | Support trusses, reflector surface skeleton | High-precision reflector panels, feeds, receivers | Panel precision requirement is at the micron level |
| **Lunar base habitation modules** | Metal shell | Hatch doors, observation windows, airlocks, internal equipment | Sealing, optics, electronics |
| **Water cycle/life support equipment housings** | Stainless steel/aluminum shells | Pumps, membrane assemblies, sensors, controllers | Precision electromechanical, polymer membranes |
| **Heat exchangers (finned tube type)** | Finned tubes (aluminum/copper drawn) | Copper tubes (feasible after asteroid supplementation), brazing equipment | Copper requires asteroids; brazing equipment requires Earth |
| **Cable trays, wiring ducts** | Aluminum/steel rolled and stamped | The cables themselves (copper core + insulation) | Copper requires asteroids; insulation requires polymer |

#### 1.11.3 Still Cannot Be Transferred to Lunar Manufacturing (Must Be Transported from Earth)

| Product Category | Reason Cannot Be Manufactured |
|:---|:---|
| **Chips, integrated circuits** | Semiconductor manufacturing chain is absent |
| **High-precision bearings (Grade P4 and above)** | Bearing steel cannot be smelted on the lunar surface; ultra-precision machining cannot be achieved |
| **Permanent magnets (NdFeB)** | Rare earth elements are scarce on the Moon; uncertainty regarding asteroids is large |
| **Carbon fiber composite parts** | PAN precursor cannot be produced on the lunar surface |
| **Rubber seals, plastic parts** | No polymer chemical engineering |
| **Optical lenses and mirrors (high precision)** | Optical glass manufacturing chain is absent |
| **Optical fiber, optical cable** | Preform manufacturing chain is absent |
| **Flexible circuit boards, connectors** | Precision electronics + polymer |
| **Specialty valves** | Precision machining + sealing + specialty alloys |
| **Sensors (pressure, temperature, flow)** | Precision electromechanical + electronics |
| **LED chips, lasers** | Semiconductor + optics |
| **Pharmaceuticals, biological products** | Organic synthesis + biotechnology |


### 1.12 Summary of Lunar Manufacturing Substitution Rate

| Product Category | Typical Products | Lunar Manufacturing Ratio | Key Constraints | Changes After Asteroid Supplementation |
|:---|:---|:---:|:---|:---|
| **Building structures** | Aluminum profiles, steel rails, pipelines, trusses | 80–100% | None | — |
| **Pressure vessels** | Storage tanks, tank cylinder sections (shell) | 70–90% | Valves, seals | Valves still transported from Earth |
| **Transport vehicles (shell)** | EMU car bodies, cargo vehicle bodies | 60–70% | Wheels, bearings, motors, electronics | Copper available from M-type asteroids, but permanent magnets still lacking |
| **Rockets (structure)** | Tank cylinder sections, interstage sections | 70–80% | Engines, valves, electronics | Superalloys (Ni, Co) can be manufactured after asteroid supplementation |
| **Electromechanical equipment housings** | Pump housings, motor housings, frames | 80% | Internal precision components | — |
| **Heat exchangers** | Finned tubes, heat sinks | 50–70% | Copper tubes (available after asteroid supplementation), brazing equipment | Copper can be used |
| **Cables** | Electrical wires, bus bars | 30% | Copper core (possible with asteroids), insulation (polymer) | Copper available; insulation still lacking |
| **Electronic equipment** | Controllers, sensors | 0% | Chips, PCB | Permanently dependent on Earth |
| **Optical components** | Lenses, optical fiber | 0% | Optical glass, precision polishing | Permanently dependent on Earth |
| **Polymer products** | Seals, plastic parts | 0% | Petrochemical feedstocks | Permanently dependent on Earth |


### 1.13 Overall Conclusions

1. **The core value of lunar assembly lies in "size breakthrough," not "local weight reduction."** Giant structures (radio arrays, space power stations, rocket tanks) are suitable for lunar surface assembly; highly integrated, high-precision, small-sized products (chips, bearings, optics) should be manufactured on Earth.

2. **The list of components that must be transported from Earth has been established** (see Section 1.3).

3. **Large extrusion/rolling equipment can be transported modularly and assembled on the lunar surface**, requiring 10–15 heavy-lift rocket launches; engineering is feasible.

4. **Ordinary glass can be manufactured on the lunar surface**, but optical glass, optical fiber, and semiconductor-grade monocrystalline silicon are permanently dependent on Earth. Solar-grade polysilicon can be produced locally for photovoltaics, but is not suitable for export.

5. **After asteroid supplementation, production lines for copper, nickel, cobalt, platinum group metals, and carbon-related products are upgraded from infeasible to feasible**, with new lines for CNT composites, superalloys, platinum group refining, and stainless steel added (see updated table in Section 1.8).

6. **Industrial machine tool settlement feasibility**: Most heavy industrial machine tools (extrusion presses, stamping presses, rolling mills, electric arc furnaces, large machine tools, welding equipment) can settle on the Moon; semiconductor manufacturing, ultra-precision optics, carbon fiber precursor, and polymer synthesis can never settle on the Moon.

7. **Products that can transition to lunar manufacturing after deploying key industrial equipment**: Predominantly metal structural parts (accounting for 70–80% by mass of materials needed for the lunar base and deep space launches); high-precision, high-purity, and polymer products are still dependent on Earth.

8. **Division of labor between Earth and the Moon**:
   - **Earth**: Precision manufacturing center (chips, optics, pharmaceuticals, polymer materials, rare-earth permanent magnets)
   - **Moon**: Heavy industry center (large structures, propellant, construction materials, asteroid mining, CNT, superalloys, platinum group refining)

9. **Implementation roadmap** (updated version):
   - Years 5–10: Construction materials, basic smelting, water ice extraction
   - Years 10–15: Large structure manufacturing, propellant factory, near-Earth C-type asteroid capture (carbon source)
   - Years 15–20: Copper/nickel/cobalt production lines, CNT composites, stainless steel
   - Years 20–25: Platinum group metal refining, superalloys, C/SiC ceramics
   - After Year 25: Main-belt asteroid mining outpost, full industrial chain closed loop


### References

[1] Appendix I Volume V. *Manufacturing Systems*. 2026.

[2] Appendix III Volume II. *Lunar Surface Railway Transportation Network*. 2026.

[3] NASA. "In-Space Manufacturing and Assembly." 2025.

[4] ESA. "Lunar ISRU and Manufacturing." 2025.

[5] DARPA. "LunA-10: Commercial Lunar Economy." 2025.

[6] TransAstra. "Asteroid Capture and Mining." 2025.

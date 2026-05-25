# Appendix III: Engineering Project Discussion

## Volume II: Lunar Surface Railway Transportation Network

**Version**: 1.6<br/>
**Date of Preparation**: June 2026<br/>
**Currency Unit**: Renminbi (RMB), symbol: ¥<br/>
**Related Main Volumes**: Appendix I Volumes II and VI


### Glossary of Abbreviations

| Abbreviation | Full Name | Notes |
|------|----------|------|
| CNT | Carbon Nanotube | Core material for ring elevators and lunar industry |
| EVA | Extravehicular Activity | Astronaut operations on the lunar surface |
| GCR | Galactic Cosmic Ray | High-energy particle radiation |
| ISRU | In-Situ Resource Utilization | Utilizing local resources on the lunar surface |
| LCC | Life Cycle Cost | Life Cycle Cost |
| MLI | Multi-Layer Insulation | Passive thermal control material |
| PSR | Permanently Shadowed Region | Water ice accumulation zone at the poles |
| RHU | Radioisotope Heater Unit | Thermal insulation device |
| SPA | South Pole–Aitken Basin | The largest impact basin on the Moon |


### 1.1 Volume Preamble

This volume focuses on the planning and cost-effectiveness analysis of a bulk cargo transportation network on the lunar surface, aiming to provide decision-making support for the logistics infrastructure of the Lunar Industrial System (Appendix I). This volume compares three transportation schemes:

1. **Earth heavy-haul railway** (as a baseline reference)
2. **Lunar surface wheel-rail railway** (fully enclosed pipeline, upper-and-lower dual-rail clamping)
3. **Lunar surface maglev railway** (superconducting magnetic levitation, fully enclosed pipeline)

This volume specifically addresses the derailment risk of wheel-rail schemes in the low-gravity environment of the Moon (1/6 g), proposes the **upper-and-lower dual-rail clamping inside the pipeline** as the solution, and, based on the resource survey findings of Appendix I Volume II, designs a preliminary railway network covering high-value resource areas.


### 1.2 Assessment Premises

All cost and performance assessments in this volume are based on the **steady-state operating period after the Lunar Industrial System is fundamentally established**. The following conditions are met at that time:

- Lunar surface construction materials (sintered regolith bricks, regolith concrete, sulfur binder) are already being mass-produced locally
- Lunar surface metal smelting (steel rails, aluminum alloys, structural steel) already has stable production capacity
- Lunar surface energy system (photovoltaics + nuclear power source + molten salt thermal storage) has been established, with marginal electricity costs as low as approximately ¥0.05/kWh
- Automated equipment such as construction robots and Space Spiders has been deployed and commissioned
- The costs of equipment initially launched from Earth (smelting furnaces, rolling mills, construction robots, etc.) have been amortized over a 100-year depreciation period

**Therefore, the calculation results in this volume reflect the cost-effectiveness of a mature lunar surface railway, not the initial investment for the first line.**


### 1.3 List of Materials, Equipment, and Facilities That Must Be Provided by Earth

Prior to and after the fundamental establishment of the Lunar Industrial System, the following materials cannot be obtained locally through ISRU or are not economical to manufacture locally, and must be launched from Earth. This list is used for the "initial equipment amortization" item in cost estimates.

| Category | Item | Specification/Notes | Unit | Unit Consumption per 1,000 km | Optimistic (¥100M) | Conservative (¥100M) |
|:---|:---|:---|:---:|---:|---:|---:|
| **Vehicles** | Distributed-power freight trains | 8-car consist, including traction motors and control systems | Train | 10 | 100 | 150 |
| **Vehicles** | Passenger trains | 8-car consist, including life support systems | Train | 2 | 30 | 50 |
| **Vehicles** | Maglev trains (freight) | 8-car consist, superconducting components | Train | 10 | 150 | 200 |
| **Track** | Steel rails (U75V) | First set of rolling mill and tooling | Set | 1 | 50 | 80 |
| **Track** | High-strength bolts and fasteners | Stainless steel M30 | ton | 100 | 5 | 10 |
| **Track** | Welding equipment (thermite/flash-butt welding) | Lunar surface-specific | Set | 1 | 10 | 20 |
| **Pipeline** | SPUA elastomer raw material | Sealing coating | ton | 200 | 10 | 20 |
| **Pipeline** | MLI multi-layer insulation blanket | Pipeline thermal insulation | 10,000 m² | 10 | 20 | 30 |
| **Pipeline** | Metal bellows (316L) | Expansion joint sealing | ton | 200 | 10 | 15 |
| **Thermal** | Water-cooling circulation pumps | Cryogenic-rated, vacuum-compatible | Unit | 1,000 | 20 | 30 |
| **Thermal** | Graphene thermal coating | High absorptivity | ton | 10 | 50 | 100 |
| **Thermal** | Copper mesh on pipeline interior | Thermal conduction layer | ton | 500 | 20 | 30 |
| **Signal/Control** | Track circuit equipment | Block sections | Set | 1,000 | 30 | 50 |
| **Signal/Control** | Fiber optic sensing system | Distributed temperature and strain measurement | Set | 1 | 10 | 20 |
| **Signal/Control** | Communications base stations (Wi-Fi/leaky coax) | Full-line coverage | Set | 1,000 | 15 | 25 |
| **Power supply** | Contact wire (copper) | ±10 kV DC | ton | 8,000 | 40 | 60 |
| **Power supply** | Substation equipment (rectifier, inverter) | One per 50 km | Set | 20 | 20 | 30 |
| **Construction equipment** | Track-laying machine | Lunar surface-specific | Unit | 2 | 30 | 50 |
| **Construction equipment** | Tunnel boring machine (if excavation needed) | Standby | Unit | 1 | 100 | 150 |
| **Construction equipment** | Welding robots | Automated thermite welding | Unit | 10 | 10 | 15 |
| **Spare parts/consumables** | Wheels, brake pads, pantograph slides | 10-year spare parts | Batch | 1 | 20 | 30 |
| **Spare parts/consumables** | Solid lubricant (MoS₂) | 10-year supply | ton | 50 | 5 | 10 |
| **Spare parts/consumables** | RHU thermal insulation units | Anti-freeze for equipment | Unit | 10,000 | 10 | 20 |
| **Total (per 1,000 km)** | — | — | — | **≈ 700–1,200** | — | — |

> Note: The optimistic scenario uses the low value, and the conservative scenario uses the high value. Only items that must be launched from Earth are listed in this table; materials that can be manufactured locally on the lunar surface (such as sintered bricks, regolith concrete, ordinary steel, and aluminum alloy structural members) are not included. The number of train consists is estimated as 10 freight trains + 2 passenger trains per 1,000 km.


### 1.4 Basic Scenario Settings

| Parameter | Earth Heavy-Haul Railway | Lunar Wheel-Rail (Fully Enclosed) | Lunar Wheel-Rail (Open) | Lunar Maglev |
|:---|:---|:---|:---|:---|
| Line length | 1,000 km | 1,000 km | 1,000 km | 1,000 km |
| Annual throughput (one-way) | 100 million tons | 100 million tons | 100 million tons | 100 million tons |
| Design service life | 100 years | 100 years | 100 years | 100 years |
| Maximum operating speed | 80 km/h | 400 km/h | 80 km/h (speed-limited) | 800 km/h |
| Normal acceleration/deceleration (freight) | 0.2 m/s² | 1.96 m/s² | 1.96 m/s² | 1.96 m/s² |
| Emergency braking deceleration | 1.0 m/s² | 1.0 m/s² | 1.0 m/s² | 1.0 m/s² |
| Traction method | 25 kV AC catenary | ±10 kV DC catenary | ±10 kV DC catenary | Superconducting electromagnetic levitation |
| Lunar gravity environment | N/A | 1/6 g | 1/6 g | 1/6 g |
| Atmospheric environment | Standard atmosphere | 0.2 bar nitrogen inside pipeline | Lunar vacuum | <10⁻³ bar inside pipeline |
| Derailment protection | Wheel flanges | Upper-and-lower dual-rail clamping | Wheel flanges + guard rails only | No contact |
| Train type | Electric locomotive + freight cars | Distributed-power multiple-unit trains | Distributed-power multiple-unit trains | Distributed-power maglev trains |

> Note: Lunar surface railways adopt a **distributed-power multiple-unit train** design, with each car equipped with traction motors. This references the design philosophy of China's standard multiple-unit trains (CR series) but is optimized for freight.


### 1.5 Train Vehicle Parameters

#### 1.5.1 Earth Heavy-Haul Railway (Baseline)

| Parameter | Value | Notes |
|:---|:---|:---|
| Locomotive type | HXD series electric locomotive | Reference national standard |
| Single locomotive power | 9,600 kW | — |
| Freight car type | Type C80 open car | Load capacity 80 tons |
| Consist | 2 locomotives + 100 freight cars | Total load 8,000 tons |
| Axle load | 25 tons | Defined under Earth gravity |

> **On axle load**: Axle load is the vertical static load that a wheel set applies to the rail under Earth gravity (unit: tons). Under the 1/6 g lunar gravity, the same mass generates only 1/6 of the normal force on Earth; therefore, the concept of "25-ton axle load" on Earth has no direct physical meaning on the lunar surface. The lunar surface should use **mass per axle** (unit: tons/axle). In this volume, the mass per axle for lunar vehicles is referenced from equivalent Earth vehicle designs, and the actual wheel-rail contact force is calculated separately based on lunar gravity.

#### 1.5.2 Lunar Surface Wheel-Rail Trains (Fully Enclosed / Open)

**(a) Freight Train Parameters**

| Parameter | Design Value | Notes |
|:---|:---|:---|
| Train consist | 8 powered cars | Expandable to 16 cars |
| Single car length | 25 m | — |
| Single car mass (unloaded) | 40 tons | Including car body, bogies, traction motors |
| Maximum single-car payload | 60 tons (under lunar gravity) | Total payload 480 tons / 8 cars |
| Single-car traction power | 1,200 kW | Permanent-magnet synchronous motor |
| Total traction power | 9,600 kW | — |
| Axle arrangement | Bo-Bo | 4 axles per car |
| Mass per axle (unloaded) | 10 tons/axle | — |
| Running wheel diameter | 0.92 m | Reference CRH |
| Anti-derailment wheel diameter | 0.3 m | WC-Co material |
| Maximum speed | 400 km/h (fully enclosed) / 80 km/h (open) | — |
| Emergency braking distance (400 km/h) | 6.2 km | a = 1.0 m/s² |
| Pantograph type | Single-arm, carbon slide | Suitable for ±10 kV DC |
| Solid lubrication | MoS₂ coating | Wheel flanges, bearings |

**(b) Passenger Train Parameters**

| Parameter | Design Value | Notes |
|:---|:---|:---|
| Train consist | 8 powered cars | — |
| Single car length | 25 m | — |
| Passenger capacity | 80 per car (2+2 layout) | Total capacity 640 |
| Single car mass (unloaded) | 45 tons | Including life support system |
| Maximum operating speed | 400 km/h (fully enclosed) | Not permitted on open lines |
| Normal acceleration/deceleration | 0.5 m/s² | Human comfort priority |
| Mass per axle | 11.25 tons/axle | — |
| Life support system | Fully enclosed pressurized cars | 70 kPa oxygen-nitrogen atmosphere |
| Radiation shielding | Car body + 5 mm PE moderator layer | Annual dose ≤5 mSv |

#### 1.5.3 Lunar Surface Maglev Trains

**(a) Freight Maglev Trains**

| Parameter | Design Value | Notes |
|:---|:---|:---|
| Train consist | 8 cars | — |
| Single car length | 25 m | — |
| Single car mass | 35 tons | No running wheels |
| Single car payload | 60 tons | — |
| Levitation method | Superconducting electrodynamic suspension (EDS) | Reference JR Maglev |
| Levitation gap | 10 mm | — |
| Traction method | Linear synchronous motor (LSM) | Track coil drive |
| Maximum speed | 800 km/h | — |

**(b) Passenger Maglev Trains**

| Parameter | Design Value | Notes |
|:---|:---|:---|
| Consist | 8 cars | — |
| Passenger capacity | 80 per car | Total capacity 640 |
| Single car mass | 40 tons (including life support) | — |
| Maximum speed | 800 km/h | — |


### 1.6 Low-Gravity Derailment Problem and the "Upper-and-Lower Dual-Rail Clamping" Solution

#### 1.6.1 Problem Description

Under the 1/6 g gravity of the Moon, the normal force that a train exerts on the track is only 1/6 of that on Earth. When the terrain undulates or there are slight track irregularities, the vertical acceleration of the train may cause the wheels to leave the rail surface, leading to derailment. Conventional Earth railways rely on the geometric constraint between wheel flanges and rail heads, but under low gravity the flange pressing force is insufficient, and lateral vibrations more easily induce wheel climbing.

#### 1.6.2 Solution: Upper-and-Lower Dual-Rail Clamping Inside the Pipeline

**(a) Configuration Description**

A rail is laid on both the upper and lower interior walls of a semi-circular or fully enclosed pipeline. Trains are simultaneously equipped with running wheels (contacting the lower rail) and anti-derailment wheels (contacting the underside of the upper rail), which mechanically prevent vertical separation.

**(b) Pipeline Structural Parameters**

| Parameter | Design Value | Notes |
|:---|:---|:---|
| Pipeline cross-section | Circular | Fully enclosed |
| Pipeline inner diameter | 5.0 m | Accommodates upper and lower rails + train + maintenance passageway |
| Pipe wall material | Sintered regolith bricks + regolith concrete | Locally manufactured |
| Pipe wall thickness | 0.4 m | Balances strength and insulation |
| Pipeline internal temperature control range | 0–30°C | Active temperature control |
| Pipeline internal pressure | 0.2 bar nitrogen | — |
| Lower rail height (from pipe bottom) | 0.6 m | Facilitates installation of water-cooling pipes |
| Upper rail height (from pipe top) | 1.0 m | — |

**(c) Mechanical Analysis and Constraint Force**

Let the lunar surface gravitational acceleration be $g_m = 1.635 \text{ m/s}^2$ and the single car mass $m = 50$ tons (fully loaded). When a track hump produces an upward acceleration $a_v = 2.0 \text{ m/s}^2$, the maximum constraint force required from the anti-derailment wheels is:

$$
F_{\text{upper,max}} = m (a_v + g_m) = 50 \times 10^3 \times (2.0 + 1.635) = 181.75 \text{ kN}
$$

Distributed across 4 anti-derailment wheels, the constraint force per wheel is approximately 45.5 kN, within the safe range for WC-Co cemented carbide.

#### 1.6.3 Continuous Welded Rail Design (Inside Fully Enclosed Pipeline)

Active temperature control in the pipeline keeps temperature fluctuations within 0–30°C (ΔT = ±15°C). Taking a rail locking temperature of 15°C, the thermal stress is:

$$
\sigma_{\text{thermal}} = E \cdot \alpha \cdot \Delta T = 210 \times 10^9 \times 1.2 \times 10^{-5} \times 15 = 37.8 \text{ MPa}
$$

The yield strength of U75V steel rails is approximately 500 MPa, leaving an extremely large safety margin, enabling full-line continuous welded rail without the need for expansion regulators.

#### 1.6.4 Safety Measures for Open Wheel-Rail Track

Since there is no upper-and-lower dual-rail clamping, speed limiting (≤80 km/h), installation of guard rails, raising wheel flanges (40 mm), reducing sleeper spacing (0.4 m), and weekly ultrasonic inspection must be adopted as safety measures.


### 1.7 Thermal Dissipation Design

#### 1.7.1 Effective Radiating Surface Area Correction

| Surface | Single-Car Area (m²) | 8-Car Total (m²) |
|:---|:---:|:---:|
| Two side faces | 160 | 1,280 |
| Car roof | 80 | 640 |
| Car floor | 80 | 640 |
| **Total** | **320** | **2,560** |

Using corrugated plates (corrugation depth 20 mm, pitch 100 mm) increases the effective area by approximately 1.4 times, giving an equivalent radiating area of $2,560 \times 1.4 = 3,584 \text{ m}^2$.

#### 1.7.2 Lunar Night Thermal Dissipation (Exterior Wall Low Temperature, approximately −180°C)

Thermal dissipation path: train → car exterior surface radiation → pipeline interior wall absorption → pipe wall heat conduction → exterior wall radiation to deep space. Radiative power:

$$
P_{\text{rad}} = \varepsilon \sigma A (T_s^4 - T_i^4) \approx 0.9 \times 5.67\times10^{-8} \times 3,584 \times (1.23\times10^{10} - 7.5\times10^7) \approx 2.23 \text{ MW}
$$

This can meet 15%–25% of the total train heat generation (10–15 MW); the remainder is supplemented by the subsurface water-cooling pipe network and cooling during station stops.

#### 1.7.3 Lunar Day Thermal Dissipation (Exterior Wall High Temperature, approximately +120°C)

During lunar day, the pipeline exterior wall temperature is higher than the interior; the pipeline must act as a **thermal insulation layer** (MLI multi-layer insulation blanket thickness ≥50 mm), and heat must not be dissipated through the exterior wall. The primary method of thermal dissipation is the **subsurface water-cooling pipe network**:

- Aluminum alloy water-cooling flat tubes (10×20 mm) are pre-embedded in the pipeline interior walls, with a working fluid of pure water + ethylene glycol
- During train operation, radiated heat from the car body is absorbed by the graphene coating on the interior wall → equalized by copper mesh → water-cooling flat tubes → carried away by working fluid
- The undercarriage heat exchanger of the train performs non-contact convective heat exchange with the water-cooling pipes at the bottom of the pipeline
- The water-cooling working fluid circulates to deep-buried underground pipes (depth 5–10 m), discharging heat into the regolith
- During lunar night, the underground pipes recover low temperature through natural cooling

#### 1.7.4 Summary of Combined Thermal Dissipation Strategy

| Operating Condition | Primary Dissipation Method | Supplementary Method | Role of Pipeline |
|:---|:---|:---|:---|
| **Lunar night** | Car body → pipeline interior wall radiation → pipe wall heat conduction → exterior wall radiation | Subsurface water-cooling pipe network at low speed | Heat radiator |
| **Lunar day** | Subsurface water-cooling pipe network (active cooling) + roof heat exchanger at station stops | Car body → interior wall radiation (heat removed by water-cooling pipes) | Thermal insulation layer |


### 1.8 Overview of the Lunar Maglev Scheme

Lunar surface maglev uses superconducting electrodynamic suspension (EDS), with a levitation gap of 10–20 mm, no mechanical contact, and speeds of up to 800 km/h or more. The pipeline interior maintains near-vacuum conditions (<10⁻³ bar).

Key technology references: Japan's JR Maglev (603 km/h ground test) and NASA's MagLifter lunar maglev launcher concept study [3][4]. This volume does not present detailed derivations, and uses this scheme for cost estimation purposes only.


### 1.9 Maximum Gradient and Line Adaptability

Maximum gradient under wheel-rail adhesion (normal acceleration 1.96 m/s²):

$$
\tan \theta_{\text{max}} = \frac{\mu}{1 + a/g_m} = \frac{0.3}{1 + 1.96/1.635} \approx 0.136, \quad \theta_{\text{max}} \approx 7.8^\circ
$$

The design maximum gradient should not exceed **10°**. For steep terrain that must be crossed:
- **Bypassing**: Routing along contour lines, applicable for gradients of 10°–20°
- **Crossing**: Adding a rack-and-pinion system (module 12 mm), without unloading the running wheels, at a speed ≤30 km/h, maximum climbing gradient 30°


### 1.10 Construction Cost Estimates (Per Kilometer)

#### 1.10.1 Materials List (Per Kilometer, Locally Manufactured Portion)

| Material | Use | Unit Consumption | Maturity |
|:---|:---|:---|:---|
| Sintered regolith bricks (50 MPa) | Segment structure | 2,500 m³ | Mature |
| Regolith concrete (C30) | Segment fill, sleepers | 800 m³ | Mature |
| Sulfur binder | Concrete cementite | 50 tons | Mature |
| Steel rails (U75V) | Upper and lower rails | 158 tons | Mature |
| Graded crushed rock (sintered regolith) | Base layer | 1,000 m³ | Mature |
| Coarse regolith | Bedding layer | 2,000 m³ | Mature |

#### 1.10.2 Cost Estimates (Per Kilometer, Two Scenarios)

| Cost Item | Earth | Lunar Wheel-Rail Fully Enclosed | Lunar Wheel-Rail Open | Lunar Maglev |
|:---|---:|---:|---:|---:|
| Roadbed/earthworks | 0.3 | 0 | 0 | 0 |
| Bridges/tunnels | 0.5 | 0 | 0 | 0 |
| Rails/guideways | 0.2 | 0.12 (0.08) | 0.06 (0.04) | 0.25 (0.18) |
| Sleepers/fixing mechanisms | 0.05 | 0.08 (0.05) | 0.02 (0.01) | 0.05 (0.03) |
| Pipeline structure | — | 0.40 (0.28) | 0 | 0.40 (0.28) |
| Segment joints/expansion joints | — | 0.05 (0.03) | 0 | 0.05 (0.03) |
| Catenary/coils | 0.2 | 0.15 (0.10) | 0.15 (0.10) | 0.45 (0.30) |
| Signal/control | 0.2 | 0.15 (0.10) | 0.15 (0.10) | 0.15 (0.10) |
| Stations/maintenance facilities | 0.1 | 0.08 (0.05) | 0.04 (0.02) | 0.08 (0.05) |
| Communications, temperature control, accessories, consumables | 0.05 | 0.15 (0.10) | 0.05 (0.03) | 0.18 (0.12) |
| **Total (¥100M/km)** | **1.60** | **1.18 (0.79)** | **0.47 (0.30)** | **1.61 (1.09)** |

> Note: Values in parentheses are optimistic scenarios; values outside parentheses are conservative scenarios. Open wheel-rail assumes no pipeline, but requires additional safety facilities such as guard rails, so costs are slightly higher than bare track.


### 1.11 Life Cycle Cost (100 Years, 1,000 Kilometers)

Total initial investment = construction cost + amortization of equipment provided by Earth (see Section 1.3).  
Total throughput = 100 million tons/year × 1,000 km × 100 years = 1,000 billion ton-km.  
Cost per ton-km = total cost ÷ 1,000 billion.

| Scheme | Total Initial Investment (¥100M) | 100-Year Operating Expenditure (¥100M) | Total Cost (¥100M) | Cost per Ton-km (¥) |
|:---|---:|---:|---:|---:|
| Earth heavy-haul railway | 1,600 | 5,370 | **6,970** | **0.0697** |
| Lunar wheel-rail fully enclosed (conservative) | 1,180 + 1,200 ≈ 2,380 | 1,410 | **3,790** | **0.0379** |
| Lunar wheel-rail fully enclosed (optimistic) | 790 + 700 ≈ 1,490 | 945 | **2,435** | **0.0244** |
| Lunar wheel-rail open (conservative) | 470 + 1,200 ≈ 1,670 | 2,730 | **4,400** | **0.0440** |
| Lunar wheel-rail open (optimistic) | 300 + 700 ≈ 1,000 | 2,150 | **3,150** | **0.0315** |
| Lunar maglev (conservative) | 1,610 + 1,500 ≈ 3,110 | 720 | **3,830** | **0.0383** |
| Lunar maglev (optimistic) | 1,090 + 1,000 ≈ 2,090 | 480 | **2,570** | **0.0257** |

> Note: Amortization of equipment provided by Earth uses 1,200 ¥100M/1,000 km for the conservative scenario and 700 ¥100M/1,000 km for the optimistic scenario (see Section 1.3). Operating expenditure calculation parameters are shown in the table below.

#### Operating Expenditure Parameters

| Scheme | Annual Maintenance as % of Construction Cost | Annual Labor Cost (¥100M/1,000 km) | Annual Energy Consumption (¥100M kWh/1,000 km) |
|:---|---:|---:|---:|
| Earth heavy-haul | 2.2% | 6.0 | 25 |
| Lunar wheel-rail fully enclosed (conservative) | 1.05% | 1.5 | 3.3 |
| Lunar wheel-rail fully enclosed (optimistic) | 0.75% | 1.0 | 3.0 |
| Lunar wheel-rail open (conservative) | 10.0% | 2.0 | 3.3 |
| Lunar wheel-rail open (optimistic) | 8.0% | 1.5 | 3.0 |
| Lunar maglev (conservative) | 0.35% | 1.5 | 1.0 |
| Lunar maglev (optimistic) | 0.25% | 1.0 | 0.8 |

Annual electricity cost = annual energy consumption × ¥0.05/kWh (lunar surface) or ¥0.5/kWh (Earth).  
Annual operating expenditure = annual maintenance cost + annual labor cost + annual electricity cost.  
100-year operating expenditure = annual operating expenditure × 100.


### 1.12 Lunar Surface Railway Network Planning

Based on the candidate sites and high-value resource zone distribution from Appendix I Volume II, the following lines are planned:

| Line | Start | End | Length (km) | Gradient Characteristics | Recommended Scheme |
|:---|:---|:---|:---:|:---|:---|
| L1 | Shackleton Peak of Eternal Light | PSR water ice zone | 15 | Crater inner wall locally >10° | Rack-and-pinion crossing (fully enclosed) |
| L2 | Peak of Eternal Light | SPA titanium-iron ore zone | 120 | Gentle slope <5° | Fully enclosed wheel-rail |
| L3 | Peak of Eternal Light | Polar launch site | 30 | Gentle slope <5° | Fully enclosed wheel-rail |
| L4 | Peak of Eternal Light | Marius Hills | 3,200 | Across south polar highlands | Maglev trunk line |
| L5 | Marius Hills | Mare Tranquillitatis skylight | 2,500 | Equatorial plain | Fully enclosed wheel-rail |
| L6 | Philolaus | North Pole | 1,900 | Polar gentle slope | Fully enclosed wheel-rail |
| L7 | Marius Hills | Equatorial launch site | 300 | Plains | Fully enclosed wheel-rail (precision cargo) |


### 1.13 Comprehensive Comparison and Selection Recommendations

| Dimension | Earth Heavy-Haul Railway | Lunar Wheel-Rail (Fully Enclosed, Optimistic) | Lunar Maglev (Optimistic) |
|:---|:---:|:---:|:---:|
| Cost per ton-km (¥) | 0.0697 | **0.0244** | 0.0257 |
| Maximum speed (km/h) | 80 | 400 | 800 |
| Maintenance difficulty | High | Low | Very low |
| Lunar dust impact | N/A | None | None |
| Technological maturity | Very high | High | Medium |
| Applicable scenario | Baseline | Main line bulk logistics | High-speed trunk line |

**Three-Tier Lunar Logistics Network Architecture**:
- Within mining sites / building materials plants: open wheel-rail (short-haul, ≤80 km/h)
- Between regional distribution centers: fully enclosed wheel-rail (medium-distance bulk cargo, 400 km/h)
- Cross-latitude trunk lines: maglev (long-distance high-speed, 800 km/h)
- Launch site / skylight platform connections: fully enclosed wheel-rail (precision cargo)


### 1.14 Volume Conclusion

1. **The cost per ton-km for lunar fully enclosed wheel-rail (optimistic) is approximately 35% of Earth heavy-haul railway**, and maglev (optimistic) is approximately 37%. Under the optimistic scenario, fully enclosed wheel-rail has the highest cost-effectiveness ratio.

2. **Open wheel-rail has a higher life cycle cost than fully enclosed wheel-rail** (conservative scenario: 0.0440 vs 0.0379 ¥/ton-km), with speed limitations and frequent maintenance, making it suitable only for very short branch lines.

3. **The list of materials that must be provided by Earth has been established**, with total amortized costs of approximately 700–1,200 ¥100M/1,000 km, representing 20%–30% of total life cycle cost.

4. **The upper-and-lower dual-rail clamping scheme** effectively resolves the low-gravity derailment risk, and the continuous welded rail design is reliable.

5. **Thermal dissipation uses lunar night radiation + lunar day subsurface water-cooling pipe network**, a combined strategy that accommodates the extreme temperature differentials on the lunar surface.

6. **Trains use a distributed-power multiple-unit design**, with each car equipped with traction motors to accommodate steep gradients and low gravity.

7. **Recommended network construction sequence**: L1–L3 (polar fully enclosed wheel-rail) → L4 (maglev trunk line) → L5–L7 (remaining fully enclosed wheel-rail).


### References

[1] China State Railway Group Co., Ltd. *Railway Engineering Investment Estimate Preparation Methods*. 2020.

[2] Railway Science Research Institute. *Research on Energy Saving Technology for Heavy-Haul Railways*. 2018.

[3] JR Central. "Superconducting maglev test run at 603 km/h". 2015.

[4] NASA Marshall Space Flight Center. "MagLifter: A Mass Driver for Lunar Launch". 2005.

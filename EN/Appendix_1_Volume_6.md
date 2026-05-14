# Appendix I: Lunar Industry

## Volume VI: Transportation Network

**Version**: 1.2<br/>
**Date of Preparation**: May 2026<br/>
**Currency Unit**: RMB (Y)<br/>
**Related Main Volume**: Main Volume VIII (Transport and Logistics System)<br/>
**Prerequisite Reading**: Appendix I Volume I (Pioneer Missions), Volume II (Siting and Infrastructure), Volume III (Energy System), Volume IV (Resource Prospecting and Mining Engineering), Volume V (Manufacturing System)


### Terminology Table

| Abbreviation | Chinese Term | Description |
|------|----------|------|
| CFRP | Carbon-fiber-reinforced polymer | Lightweight high-strength structural material |
| CNT | Carbon nanotube | Core cable material for the ring and lunar industry |
| EVA | Extravehicular activity | Astronaut operations outside habitats on the lunar surface or in space |
| GCR | Galactic cosmic rays | High-energy particle radiation from outside the Solar System |
| HVDC | High-voltage DC transmission | Traction power mode for rail transport |
| ISRU | In-situ resource utilization | Manufacturing and survival with local lunar resources |
| kWe | Kilowatt electric power | Electric motor output unit |
| kWh | Kilowatt-hour | Battery capacity and energy consumption unit |
| MLI | Multi-layer insulation blanket | Reflective passive thermal-control insulation in vacuum |
| MoS2 | Molybdenum disulfide | Solid lubricant for vacuum and extreme temperatures |
| MPa | Megapascal | Pressure/stress unit |
| PSR | Permanently shadowed region | Permanently Shadowed Region |
| PTFE | Polytetrafluoroethylene | Sealing material with low friction and broad-temperature vacuum compatibility |
| RHU | Radioisotope heating unit | Device that uses radioactive decay heat for thermal maintenance |
| SPE | Solar particle event | High-energy particle flux released by solar eruptions |
| UHMWPE | Ultra-high-molecular-weight polyethylene | Wear-resistant low-friction material for pipe outer insulation jackets |
| WC-Co | Tungsten-carbide-cobalt hard alloy | High wear-resistance material for gears, racks, and cutting teeth |


### 6.1 Opening Statement

This volume is positioned as the **logistics and transportation infrastructure plan** of the lunar industrial system, focusing on the following core questions:

> How can mined construction aggregate, metal-mineral concentrate, and water ice be transported to the base efficiently? How can base-produced construction materials, metal ingots, and CNT cables be delivered to launch sites, skylight platforms, and GEO orbital-ring construction yards? How should personnel and cargo flow between surface and underground bases? From rovers to rail transport, from pipeline delivery to skylight lift systems, how should energy consumption, range, and payload of each mode match stage-specific throughput demand? What is the total mass of all transportation equipment? Can these systems operate reliably under extreme lunar temperature conditions (-180 C to +120 C)?

This volume follows:

- **Volume II (Siting and Infrastructure)**: overall framework of the lunar transport network has been planned.
- **Volume III (Energy System)**: traction power voltage class and grid interfaces for rail transport have been defined.
- **Volume IV (Resource Prospecting and Mining Engineering)**: mining-site locations, monthly extraction, and transport distances are defined.
- **Volume V (Manufacturing System)**: feedstock demand and product output for construction lines, metallurgy shops, and CNT plants are defined.

Core tasks:

1. Design the complete surface logistics network connecting mines, base, skylight platforms, and launch sites.
2. Provide detailed technical parameters, energy use, range, and key component sizes for all transport tools.
3. Define operating temperature ranges and solid-lubrication requirements for all surface-exposed transport equipment.
4. Plan phased expansion of the transportation network.
5. Provide order-of-magnitude estimates of mass, energy consumption, and range for all transportation equipment.


### 6.2 Transportation Demand Analysis

#### 6.2.1 Cargo Transport Demand (Infrastructure Phase II - Stage 2)

| Cargo Type | Origin | Destination | One-Way Distance | Monthly Throughput | Transport Frequency (Lunar Day) | Transport Method |
|:-----|:-----|:-----|:-----|:-----|:-----|:-----|
| Liquid water | Polar PSR ice mining site | Base water storage tank | 5-15 km | 200-500 L/lunar day (Stage 1) / 2,000-5,000 L/lunar day (Stage 2) | 3-4 trips/day (Stage 1) / continuous (Stage 2 pipeline) | Unpressurized cargo rover (Stage 1) / insulated pipeline (Stage 2) |
| Construction aggregate (coarse) | Aggregate pit | Base construction-material line | <=10 km | >=500 m3/month (about 750-1,000 t) | 1-2 trips/day (rover) / multi-trip daily (rail) | Unpressurized cargo rover (Stage 1) / open light rail (Stage 2) |
| Metal-mineral concentrate | Metal-mineral pit | Base metallurgy workshop | <=10 km | >=100 m3/month (about 200-300 t ROM ore, ~20-30 t concentrate after magnetic separation) | 2-3 trips/week | Unpressurized cargo rover (sealed container) |
| Construction products | Base construction-material line | Construction front / launch site | 0.5-5 km | About 47 t/month (42 t bricks + 5 t concrete) | 1-2 trips/day | Unpressurized cargo rover |
| Metal ingots (Al/Fe) | Base metallurgy workshop | Machine shop / catalyst-preparation shop / launch site (export) | 0.5-2 km | 200-1,000 kg/month | 1-2 trips/week | Small unpressurized rover or underground conveyor |
| CNT yarn (export grade) | Base CNT plant | Skylight platform (to lunar orbit then GEO ring construction yard) | 0.2-2 km (vertical + horizontal underground) | 10-50 kg/month (Stage 1) / >=1,000 kg/month (Stage 2) | 1 trip/week (Stage 1) / 1 trip/day (Stage 2) | Skylight lift system + pressurized crew rover |

#### 6.2.2 Personnel Commuting Demand (Infrastructure Phase II - Stage 2)

| Commute Route | Crew per Trip | Frequency | One-Way Distance | Transport Method |
|:-----|:-----|:-----|:-----|:-----|
| Base habitation zone <-> manufacturing shops | 2-10 | Multiple daily | 0.2-2 km (underground) | Underground electric walkway / small pressurized rover |
| Base <-> water-ice mining site | 2-4 | 2-3 times/week (maintenance) | 5-15 km | Pressurized crew rover |
| Base <-> aggregate pit | 2-4 | 1-2 times/week (maintenance) | <=10 km | Pressurized crew rover |
| Base <-> metal-mineral pit | 2-4 | Once/week (maintenance) | <=10 km | Pressurized crew rover |
| Base <-> skylight platform (surface) | 2-6 | Multiple daily (logistics transfer, EVA) | 0.2-0.5 km (vertical) | Skylight lift system (crewed capsule) |
| Base <-> launch site | 2-8 | 1-2 times/month (launch operations) | 10-20 km | Pressurized crew rover |


### 6.3 Full-System Operating Temperature and Solid-Lubrication Requirements

Surface temperatures are approximately -180 C to +120 C (down to about -250 C in polar PSRs). All surface-exposed moving parts and electrical systems must have explicit operating ranges and lubrication schemes. Equipment in sealed underground sections benefits from cave thermal stability, about -20 C to +30 C, with less severe requirements.

#### 6.3.1 Surface-Exposed Equipment Temperature Requirements

| Equipment/Component | Operating Temperature Range | Solid-Lubrication Scheme | Notes |
|:-----|:-----|:-----|:-----|
| Rover mobility system (hub motors, bearings, suspension) | -180 C to +120 C | MoS2 dry lubrication, sealed bearings | During lunar night, RHU keeps critical electronics >0 C |
| Rover battery pack | -50 C to +80 C (operation) / -180 C to +120 C (storage) | Not applicable (inside sealed thermal enclosure) | RHU keeps battery >-30 C during lunar night |
| Rail (aluminum alloy/steel) | -180 C to +120 C | No lubrication (dry wheel-rail contact) | Sleepers are regolith-concrete precast units, compressive strength >=20 MPa, thermal-cycle degradation <=20% |
| Rack-and-pinion section (gear/rack) | -180 C to +120 C | MoS2 dry lubrication on tooth surfaces | 7075-T6 aluminum alloy rack in modular 5-10 m segments |
| Rack-drive motor | -150 C to +150 C (winding temperature) | MoS2 dry lubrication (bearings) | RHU keeps motor >-50 C during lunar night |
| Enclosed-tube rail transport (low-pressure N2 section) | -180 C to +120 C (outer tube wall) / -50 C to +80 C (inside tube) | MoS2 on wheel-rail and motor bearings | N2 in tube improves heat transfer, moderating temperature |
| Insulated pipeline (liquid water) | -180 C to +120 C (outer wall) / +5 C to +30 C (water inside inner pipe) | Not applicable (no moving parts) | Inner-wall heating cable + MLI layer keeps water >=5 C at night |
| Skylight bridge crane (surface-exposed parts) | -180 C to +120 C | MoS2 dry lubrication (rack, winch bearings) | Motor windings protected by RHU at night |
| Cable car system (pit bottom to rim) | -250 C to +120 C (PSR segment) / -180 C to +120 C (non-PSR segment) | MoS2 dry lubrication (pulley bearings, hoist bearings, rail clamp brakes) | PSR-segment equipment requires extra RHU to keep electronics >-50 C |
| Cable rope / CNT cable | -250 C to +120 C | No lubrication required | CNT cables avoid low-temperature embrittlement (carbon materials outperform steel at cryogenic toughness) |

#### 6.3.2 Underground Equipment Temperature Requirements

| Equipment/Component | Operating Temperature Range | Lubrication Scheme | Notes |
|:-----|:-----|:-----|:-----|
| Underground electric rail (traction head, catenary) | -20 C to +50 C | MoS2 dry lubrication (wheel-rail, motor bearings) | Cave thermal stability, no RHU needed |
| Continuous conveyor (drive motor, belt) | -20 C to +50 C | MoS2 dry lubrication (drive drum bearings) | Enclosed hood operation, lunar dust excluded |
| Skylight crew elevator (underground section) | -20 C to +30 C | MoS2 dry lubrication (rack, guide rails) | Stable temperature in pressurized section |


### 6.4 Surface Transport Vehicle Design

#### 6.4.1 Unpressurized Cargo Rover

**(a) Basic parameters**

| Parameter | Design Value | Notes |
|:-----|:-----|:-----|
| Payload capacity | >=5 t (lunar-gravity equivalent) | Matches single-trip aggregate transport (~3-5 m3 loose material) |
| Curb mass | <=1,500 kg | Excludes payload mass |
| Envelope size | About 5.0 m L x 3.0 m W x 2.5 m H | Fits lunar roads and layered-platform corridors (6-8 m wide) |
| Cargo bed size | About 3.5 m L x 2.5 m W x 1.5 m H (open) | About 13 m3 volume |
| Mobility architecture | Six-wheel independent drive + independent suspension, track drive as backup | Six-wheel for flatter roads; track option for rough terrain with lower ground pressure |
| Tire/track | Aluminum hub + UHMWPE solid tire (non-pneumatic) | Tire OD ~1.2 m, width ~0.3 m; UHMWPE is wear-resistant, low-friction, wide-temperature (-250 C to +120 C) |
| Ground clearance | About 0.4 m | Crosses rocks <=20 cm diameter |
| Max speed | 20 km/h (loaded) / 40 km/h (empty) | Low gravity increases rollover risk at high speed |
| Range | >=100 km per charge | Battery capacity >=80 kWh |
| Battery type | Solid-state lithium battery, energy density >=500 Wh/kg | Battery mass ~160 kg |
| Drive motor | 6 hub motors, about 2 kW each | Total peak power ~12 kW, average ~8 kW |
| Brake system | Regenerative + mechanical braking | Mechanical brake uses dry friction with MoS2 lubricated moving interfaces |
| Comms and navigation | Lunar wireless backbone + autonomous navigation | Supports three modes: local crew real-time teleoperation (<10 ms), autonomous operation, and Earth macro-command dispatch (~2.6 s latency) |

**(b) Dust protection and temperature requirements**

- All moving components in wheel/suspension assemblies use elastic dust boots (spring-energized PTFE seals) and >=3-stage labyrinth sealing.
- Seal material PTFE, rated for -250 C to +260 C.
- Cargo bed is open (with dust cover). For concentrate and liquid water, use sealed aluminum containers (wall thickness >=2 mm).
- On return to base, rovers pass through dedicated dust-cleaning stations for high-pressure blow-off and electrostatic dust removal.

**(c) Thermal design for liquid-water transport**

For liquid-water transport, equip removable insulated tank (capacity >=2,000 L, inner diameter ~1.2 m, length ~2.0 m) with MLI (>=20 mm). During lunar night, RHU or thermal storage maintains water >=5 C.

#### 6.4.2 Pressurized Crew Rover

**(a) Basic parameters**

| Parameter | Design Value | Notes |
|:-----|:-----|:-----|
| Crew capacity | 4-6 | - |
| Curb mass | <=3,000 kg | Includes pressurized cabin, life support, radiation shielding |
| Envelope size | About 6.0 m L x 3.5 m W x 3.0 m H | - |
| Pressurized cabin inner diameter | >=2.5 m | - |
| Cabin length | About 4.0 m (crew activity zone) | - |
| Cabin pressure | 70 kPa (O2-N2 mixed atmosphere) | Leak rate <=0.05% per day |
| Mobility architecture | Six-wheel independent drive + independent suspension | Same tire spec as cargo rover (UHMWPE solid tires, OD ~1.2 m) |
| Max speed | 30 km/h (flat road) / 15 km/h (rough terrain) | - |
| Range | >=200 km per charge | Battery capacity >=140 kWh |
| Independent life support | >=72 h autonomous operation (4-person baseline) | - |
| Radiation shielding | Top of cabin with >=2 cm Al-equivalent shielding | UHMWPE fabric + aluminum-alloy composite layer |
| Temperature requirement | Cabin 20 C +/-5 C (active thermal control); external mobility system -180 C to +120 C (MoS2 lubrication) | - |

**(b) Emergency equipment**

PLSS interfaces x6, emergency oxygen masks x6, and lunar-dust cleaning kit.


### 6.5 Surface Rail Transport

#### 6.5.1 Basic Track Structure

| Parameter | Design Value | Notes |
|:-----|:-----|:-----|
| Gauge | 1.5 m | Standard gauge for freight and passenger consists |
| Rail profile | I-section, height ~120 mm, base width ~100 mm | Locally smelted aluminum alloy or steel (from Volume V metallurgy). Unit mass ~30 kg/m |
| Sleeper | Regolith-concrete precast, about 2.0 m L x 0.3 m W x 0.15 m T | Compressive strength >=20 MPa from Volume V construction line. Sleeper spacing ~0.6 m |
| Fastening | Aluminum spring clips + UHMWPE pads | MoS2-lubricated bolts, temperature range -180 C to +120 C |
| Track foundation | Regolith-concrete slab (width 6-8 m, thickness 0.2-0.3 m) | Laid on compacted regolith roadbeds or layered platforms (Volume II Section 2.3.2(d)) |
| Max gradient (adhesion section) | <=5% (~2.9 deg) | Limited by wheel-rail adhesion under low gravity (about 0.3-0.5) |
| Minimum curve radius | >=500 m (freight) / >=1,000 m (passenger high-speed section) | - |
| Operating temperature | -180 C to +120 C (rails/sleepers/fasteners exposed outdoors) | MoS2 dry lubrication for fastening bolts; sleeper strength degradation <=20% after thermal cycling |

#### 6.5.2 Train Consists

| Consist Type | Configuration | Payload/Passengers | Max Speed | Notes |
|:-----|:-----|:-----|:-----|:-----|
| Freight consist | Electric locomotive + 3-5 freight cars | >=50 t (lunar-gravity equivalent) | 300 km/h on mainline, <=60 km/h on rack sections | Open-top or sealed-container cars |
| Passenger consist | Electric locomotive + 2-3 pressurized passenger cars | 20-40 persons | 300 km/h on mainline, <=60 km/h on rack sections | Each car has independent life support (>=72 h) and radiation shielding |
| Mixed consist | Electric locomotive + freight cars + passenger cars | - | 200 km/h | Low-frequency combined transport |

**Locomotive size**: about 8.0 m L x 3.0 m W x 3.5 m H. **Freight-car size**: about 12.0 m L x 3.0 m W x 2.5 m H (open) / 3.0 m H (sealed), payload >=10 t per car. **Passenger-car size**: about 15.0 m L x 3.5 m W x 3.5 m H (pressurized inner diameter >=3.0 m), 10-20 passengers per car.

#### 6.5.3 Traction Power Supply

- **Power method**: overhead catenary (+/-10 kV DC), pantograph carbon contact strip (dry interface, MoS2 on associated mechanical sliding interfaces).
- **Traction power**: about 2 MW (full load 52 t, mainline 300 km/h, rolling resistance coefficient ~0.005 under low gravity).
- **Regenerative braking**: braking energy fed back to catenary or wayside storage, recovery efficiency >=60%.

#### 6.5.4 Signaling and Control

Use track-circuit block control with lunar navigation enhancement for fully automated driverless operation. Train positioning accuracy <=1 m.


### 6.6 Rack-and-Pinion System (Steep-Grade Sections)

For surface rail grades >5%, rack-and-pinion sections are required to overcome adhesion limits. This section provides lunar-specific rack parameters under low gravity, vacuum, and extreme temperature conditions.

#### 6.6.1 Basic Rack System Parameters

| Parameter | Design Value | Notes |
|:-----|:-----|:-----|
| Tooth profile | Trapezoidal, module 12 mm | Sized for medium lunar traction demand |
| Rack material | Aluminum alloy 7075-T6 | Locally supplied by Volume V metallurgy |
| Rack dimensions | Segment length 5-10 m, section about 120 mm W x 80 mm H | Modular design, replace only damaged segments |
| Tooth width | 100 mm | - |
| Gear material | Aluminum alloy 7075-T6 | Same material to avoid galvanic corrosion |
| Gear size | Pitch diameter 0.5 m, about 42 teeth | - |
| Number of gear pairs | >=12 pairs (3 layers, 4 pairs per layer) | - |
| Pressure angle | 20 deg | Standard value |
| Contact ratio | About 2.0 | Typical for trapezoidal profiles |
| Applicable grade | >5% to <=30 deg (~58% gradient) | Max design grade 30 deg covers most steep polar/crater terrain |
| Rack-section speed limit | 20-30 km/h at 30 deg; 40-60 km/h at 5%-20 deg steep grades | Same speed-limiting principle as rack sections on mainline |
| Operating temperature | -180 C to +120 C | MoS2 dry lubrication on tooth surfaces; RHU motor thermal hold at night |
| Lubrication | MoS2 dry lubrication (tooth faces, bearings) | Replaces conventional oil-gas lubrication |
| Estimated total rack length | About 150-300 km (assuming one 3,000 km line, steep section share 5%-10%) | Only initial installation tools and lock hardware are Earth-launched; rack bodies are locally made in Volume V |

#### 6.6.2 Mechanical Verification Under Three Load Cases

**(a) Basic parameters**

| Symbol | Value | Unit | Notes |
|:---|:---|:---|:---|
| $g_{moon}$ | 1.635 | m/s2 | Lunar gravity acceleration (= $g_0/6$) |
| $alpha$ | 30 deg | deg | Maximum design slope |
| $mu_{roll}$ | 0.005 | - | Rolling resistance coefficient (low gravity + vacuum) |
| $m_{empty}$ | $10 x 10^3$ | kg | Empty consist mass (locomotive only) |
| $m_{mid}$ | $30 x 10^3$ | kg | Medium-load consist mass (locomotive + 2 half-load cars) |
| $m_{full}$ | $52 x 10^3$ | kg | Full-load consist mass (locomotive + 5 full-load cars) |
| $N_{pairs}$ | 12 | pairs | Number of meshing gear pairs |
| $epsilon$ | 2.0 | - | Contact ratio |
| $theta$ | 20 deg | deg | Pressure angle |
| $m_n$ | 12 | mm | Module |
| $b$ | 100 | mm | Tooth width |
| $D_p$ | 0.5 | m | Gear pitch diameter |

**(b) Traction-force demand by load case**

Total lunar weight:

$$
W_{moon} = m \cdot g_{moon}
$$

Slope resistance at 30 deg:

$$
F_{slope} = W_{moon} \cdot \sin\alpha
$$

Rolling resistance:

$$
F_{roll} = W_{moon} \cdot \mu_{roll}
$$

Total traction demand (ignoring acceleration term):

$$
F_{traction} = F_{slope} + F_{roll} = W_{moon} \cdot (\sin\alpha + \mu_{roll})
$$

Design traction force (with safety factor $S$):

$$
F_{design} = F_{traction} \cdot S
$$

Safety factors are: empty case $S=1.5$, medium case $S=1.8$, full case $S=2.0$. These are conservative envelopes for rack-mesh stress verification, not motor sizing factors. Motor sizing uses actual traction demand.

**Computed results**:

**Empty** ($m_{empty}=10$ t):

$$
W_{moon} = 10 \times 10^3 \times 1.635 = 1.635 \times 10^4 \; N
$$

$$
F_{traction,empty} = 1.635 \times 10^4 \times (0.5 + 0.005) \approx 8.26 \times 10^3 \; N
$$

$$
F_{design,empty} = 8.26 \times 10^3 \times 1.5 \approx 1.24 \times 10^4 \; N
$$

**Medium** ($m_{mid}=30$ t):

$$
W_{moon} = 30 \times 10^3 \times 1.635 = 4.905 \times 10^4 \; N
$$

$$
F_{traction,mid} = 4.905 \times 10^4 \times (0.5 + 0.005) \approx 2.48 \times 10^4 \; N
$$

$$
F_{design,mid} = 2.48 \times 10^4 \times 1.8 \approx 4.46 \times 10^4 \; N
$$

**Full** ($m_{full}=52$ t):

$$
W_{moon} = 52 \times 10^3 \times 1.635 = 8.502 \times 10^4 \; N
$$

$$
F_{traction,full} = 8.502 \times 10^4 \times (0.5 + 0.005) \approx 4.29 \times 10^4 \; N
$$

$$
F_{design,full} = 4.29 \times 10^4 \times 2.0 \approx 8.59 \times 10^4 \; N
$$

| Load Case | Consist Mass | Lunar Weight $W_{moon}$ | Actual Traction $F_{traction}$ | Design Safety Factor $S$ | Design Traction $F_{design}$ |
|:---|:---|:---|:---|:---|:---|
| Empty | 10 t | 16.35 kN | 8.26 kN | 1.5 | 12.39 kN |
| Medium | 30 t | 49.05 kN | 24.78 kN | 1.8 | 44.60 kN |
| Full | 52 t | 85.02 kN | 42.95 kN | 2.0 | 85.90 kN |

**(c) Single-tooth normal force**

Total normal force (20 deg pressure angle):

$$
F_{n,total} = \frac{F_{design}}{\cos 20^\circ} = \frac{F_{design}}{0.9397}
$$

Single-tooth normal force (12 gear pairs, contact ratio $epsilon = 2.0$):

$$
F_n = \frac{F_{n,total}}{N_{pairs} \times epsilon} = \frac{F_{n,total}}{12 \times 2}
$$

| Load Case | $F_{design}$ | $F_{n,total}$ | $F_n$ |
|:---|:---|:---|:---|
| Empty | 12.39 kN | 13.19 kN | 549 N |
| Medium | 44.60 kN | 47.46 kN | 1,978 N |
| Full | 85.90 kN | 91.41 kN | 3,809 N |

**(d) Tooth-surface contact stress verification**

Tooth-profile curvature radius at pitch circle ($D_p = 0.5$ m):

$$
rho_1 = \frac{D_p}{2} \sin\alpha = 0.25 \times \sin 20^\circ = 0.25 \times 0.3420 \approx 0.0855 \; m
$$

Rack curvature radius is infinity, so equivalent curvature radius is $rho_{eq}=0.0855$ m.

Equivalent modulus (two 7075-T6 aluminum surfaces, $E=70$ GPa, $nu=0.33$):

$$
E_{eq} = \frac{E}{2(1-nu^2)} = \frac{70 \times 10^9}{2 \times (1-0.1089)} \approx 3.93 \times 10^{10} \; Pa
$$

Contact half-width (tooth width $b=100$ mm = 0.10 m):

$$
a_h = \sqrt{\frac{4 F_n rho_{eq}}{\pi b E_{eq}}}
$$

Maximum contact stress:

$$
sigma_{H,max} = \frac{2 F_n}{\pi a_h b}
$$

Conservative contact-fatigue limit for 7075-T6 is 300 MPa, with contact safety factor $S_H=1.5$:

$$
sigma_{H,allow} = \frac{300}{1.5} = 200 \; MPa
$$

| Load Case | $F_n$ | $a_h$ | $sigma_{H,max}$ | Allowable | Margin | Result |
|:---|:---|:---|:---|:---|:---|:---|
| Empty | 549 N | 0.124 mm | 28.2 MPa | 200 MPa | **7.1:1** | **Pass with large margin** |
| Medium | 1,978 N | 0.235 mm | 53.6 MPa | 200 MPa | **3.7:1** | **Pass with large margin** |
| Full | 3,809 N | 0.326 mm | 74.4 MPa | 200 MPa | **2.7:1** | **Pass with large margin** |

**(e) Tooth-root bending stress verification**

Full tooth height:

$$
h_{tooth} = 2.25 \cdot m_n = 2.25 \times 12 = 27 \; mm = 0.027 \; m
$$

Tooth-root thickness (critical section):

$$
t_{root} = 1.5 \cdot m_n = 1.5 \times 12 = 18 \; mm = 0.018 \; m
$$

Section modulus (rectangular section, tooth width $b=100$ mm = 0.10 m):

$$
W = \frac{b \cdot t_{root}^2}{6} = \frac{0.10 \times (0.018)^2}{6} = 5.40 \times 10^{-6} \; m^3
$$

Tooth-root bending moment (worst case, load at tooth tip):

$$
M_{root} = F_n \cdot h_{tooth}
$$

Tooth-root bending stress:

$$
sigma_F = \frac{M_{root}}{W}
$$

7075-T6 bending fatigue limit is about 115 MPa (10^7 cycles). With safety factor $S_F=2.0$:

$$
sigma_{F,allow} = \frac{115}{2.0} = 57.5 \; MPa
$$

| Load Case | $F_n$ | $M_{root}$ | $sigma_F$ | Allowable | Margin | Result |
|:---|:---|:---|:---|:---|:---|:---|
| Empty | 549 N | 14.82 N.m | 2.74 MPa | 57.5 MPa | **21.0:1** | **Very large margin** |
| Medium | 1,978 N | 53.41 N.m | 9.89 MPa | 57.5 MPa | **5.8:1** | **Pass with margin** |
| Full | 3,809 N | 102.84 N.m | 19.0 MPa | 57.5 MPa | **3.0:1** | **Pass with margin** |

**(f) Rack-section speed and power demand by load case**

At 30 deg extreme slope ($v=20$ km/h = 5.56 m/s, rack-mesh efficiency $eta_{rack} \approx 0.93$):

Rack-section traction power:

$$
P_{rack} = F_{traction} \cdot v / eta_{rack}
$$

| Load Case | Traction Force | Speed | Power Demand | Share of Total Train Installed Power (~2 MW) |
|:---|:---|:---|:---|:---|
| Empty | 8.26 kN | 5.56 m/s | About 49 kW | <3% |
| Medium | 24.78 kN | 5.56 m/s | About 148 kW | <8% |
| Full | 42.95 kN | 5.56 m/s | About 257 kW | <13% |

For all three load cases, rack meshing force and power demand remain within equipment capability.

#### 6.6.3 Real-Time Mesh Monitoring and Maintenance

- **Onboard meshing-force sensing**: torque sensors on output shafts of each rack-drive motor. If meshing force exceeds normal value by >20% at current speed, system auto-reduces speed and alarms.
- **Rack wear inspection**: every 3 months, rover-mounted laser profile scanner measures full-line tooth wear. Replace rack segment when wear depth exceeds 10% of tooth-top thickness (about 2.7 mm).


### 6.7 Pit-Bottom to Pit-Rim Transport System

#### 6.7.1 Early/Experimental Option: Mobile Lightweight Winch Lift System

In Infrastructure Phase I and early Infrastructure Phase II, permanent cableway and rack rail are not yet available. If water-ice mining is at crater bottoms (e.g., Shackleton PSR floor), a lightweight rapidly deployable temporary solution is required to lift initial ice output to crater rim for rover transfer to base.

**(a) Operating principle**

Deploy lightweight electric winch at crater rim, connect to simple bottom cargo bucket through one CNT braided cable or high-strength steel rope. System only needs rim-side winch anchoring and bottom turning pulley, enabling vertical or steep-slope lifting without pre-laid track or rack.

**(b) Main technical parameters**

| Parameter | Design Value | Notes |
|:---|:---|:---|
| System type | Mobile single-rope winch lifting system | Non-permanent, removable and relocatable |
| Max slope | Unlimited (vertical lifting supported) | Freely suspended cable, not limited by terrain grade |
| Max single-lift payload | <=2 t (lunar-gravity equivalent) | Matches early low-volume water-ice extraction (200-500 L/month) |
| Lift speed | 0.5-2 m/s (variable-frequency adjustable) | Loaded low speed, empty high speed |
| Max lift height | <=500 m | Covers typical pit bottom to rim elevation |
| Winch power | About 15-30 kW | Based on 2 t load at 2 m/s |
| Cable type | CNT braided cable (preferred) or high-strength steel rope | CNT cable offers cryogenic toughness and high strength-to-weight, no solid lubrication needed |
| Cable diameter | >=10 mm | Safety factor >=3.0 |
| Turning-pulley diameter | >=0.5 m | Pulley-to-cable ratio >=50:1 to reduce bending fatigue |
| Cargo bucket | Open or sealed aluminum container (wall thickness >=2 mm) | Capacity >=1 m3 (ice-bearing regolith or ice blocks) |
| Bucket mass | <=300 kg (empty) | Aluminum alloy or CFRP |
| Power source | Rim-side mobile nuclear source (Kilopower-type, >=10 kWe) or rover battery pack | Main grid not yet extended to rim in early phase |
| Deployment mode | One unpressurized cargo rover transports winch/pulley to rim | Second rover (or prepositioned lander) places bucket at pit bottom |
| Operating temperature | -250 C to +120 C (full exposure in PSR segment) | CNT cable has no low-temp embrittlement; winch motor kept warm by RHU; pulley bearings use MoS2 dry lubrication |
| Total system mass | <=1,500 kg (winch, cable, pulley, bucket) | Deployable in single rover transport mission |

**(c) Energy estimate**

For single 2 t lift, 300 m lift height, 2 m/s speed:

- Lift time: 300 m / 2 m/s = 150 s (~2.5 min)
- Lift energy (without regen): about 2 t x 1.635 m/s2 x 300 m = 0.98 MJ = 0.27 kWh
- Including drivetrain losses (efficiency ~85%), actual energy per lift is about 0.32 kWh

At early 200-500 L/month water output, one 2 t lift trip can cover monthly ice movement; energy demand is very low.

**(d) Transition to permanent system**

This system is temporary for Phase I through early Phase II, design life ~3-5 years. Once mid-to-late Phase II reaches >=2,000 L/month water output, permanent cableway (Section 6.7.2) enters operation and this system is retired. Winch may be repurposed for rim lifting tasks or disassembled/recycled; cable retained as spare; bucket reused as internal transport container.

#### 6.7.2 Permanent Option: Bi-Directional Circulating Freight Cableway

At grades >30 deg, wheel-rail adhesion is insufficient and rack traction is required. At even steeper slopes (e.g., 30-45 deg or more on crater walls), rack systems can still provide traction but train mass/stability become challenging. For permanent high-throughput fixed-line cargo from pit-bottom water-ice sites, add a **bi-directional circulating freight cableway** based on elevator-like counterbalancing. Under extreme slopes, it is not constrained by wheel-rail adhesion, and steeper gradients increase gravity-balance advantage.

**(a) System principle and suitability**

Use dual-car balanced circulation: two freight cars fixed to opposite ends of one high-strength cable routed over rim-side drive pulleys. As one car ascends from pit bottom, the other descends from rim. Potential energy of descending car offsets most lifting demand of ascending car; drive motor mainly covers friction losses and net load imbalance. This is especially suitable in 1/6 g. System supports freight-only one-way/two-way switched operation with open or sealed containers.

**(b) Main technical parameters**

| Parameter | Design Value | Notes |
|:-----|:-----|:-----|
| System type | Dual-car balanced freight cableway | - |
| Guideway type | Hybrid rack + wheel-rail guideway | - |
| Max slope | 45 deg (~100% grade) | Covers most steep polar crater-wall segments |
| Max payload | 20 t per car (lunar-gravity equivalent) | For bulk ice blocks or ice-bearing regolith containers |
| Operating speed | 1-8 m/s (variable frequency) | <=20 deg: 5-8 m/s; 20-30 deg: 3-5 m/s; 30-45 deg: 1-3 m/s |
| Route length | <=3 km (one way) | Typical pit-bottom to rim distance |
| Winch power | About 200-500 kW | Primarily friction and load-difference compensation, not full gravity lift |
| Drive-station location | Pit rim | Convenient for power and maintenance |
| Operating mode | Switchable two-way/one-way | - |
| Braking system | Regenerative + emergency rail-clamp braking | Normally-closed spring-energy storage design, lock within 50 ms |
| Operating temperature | -250 C to +120 C (PSR section) / -180 C to +120 C (non-PSR section) | MoS2 on pulley bearings, winch bearings, rail-clamp brakes |

**(c) Speed and braking tier strategy**

| Grade Range | Speed | Braking Strategy | Typical Use |
|:---|:---|:---|:---|
| <=20 deg | 5-8 m/s | Regenerative primary + mechanical assist | Gentle wall sections, rim transfer platforms |
| 20-30 deg | 3-5 m/s | Regenerative + mechanical coordinated | Medium-steep wall sections |
| 30-45 deg | 1-3 m/s | Regenerative + emergency rail clamp (independent of drive system) | Extreme-steep sections and pit-bottom station |

**(d) Car and cable dimensions**

| Parameter | Design Value | Notes |
|:-----|:-----|:-----|
| Car envelope | About 4.0 m L x 2.5 m W x 2.0 m H | Open-top or sealed-container type |
| Car mass | <=2,000 kg (empty) | Aluminum alloy or CFRP |
| Cable type | CNT braided cable or high-strength steel rope | CNT preferred for cryogenic toughness and strength-to-weight |
| Cable diameter | >=30 mm | Safety factor >=3.0 based on worst-case full load at 45 deg |
| Pulley diameter | >=2.0 m | Pulley-to-cable ratio >=60:1 to reduce bending fatigue |

**(e) Rim transfer facilities**

- **Rim station**: at crater edge, <=5 km from skylight platform. Includes small crane (>=5 t lift) and buffer storage. Cableway cargo is unloaded then transferred via sealed conveyor or small rover to rail freight station or base storage.
- **Bottom station**: at edge of water-ice mining site, with container loading platform.
- **Intermediate station**: when wall depth >500 m, provide one intermediate station with small crane and buffer storage to avoid excessive single-span lift length causing cable sag/swing issues.

**(f) Complementarity with rack rail**

Cableway and rack rail are complementary: rack rail handles medium/long-distance trunk transport (rim-base-mines), max slope 30 deg, high speed (mainline 300 km/h, rack sections 40-60 km/h). Cableway handles short-distance steep vertical transfer (pit bottom to rim), max slope 45 deg, low speed (1-8 m/s), dual-car balanced circulation. Seamless interface at rim transfer platform through sealed conveyor connection.


### 6.8 Insulated Liquid-Water Pipeline

When water-ice extraction reaches Stage 2 (>=2,000 L/month) and mining site is <=5 km from base, fixed insulated pipeline replacing rover hauling is the most economical and energy-efficient option.

| Parameter | Design Value | Notes |
|:-----|:-----|:-----|
| Pipe diameter | >=50 mm (inner diameter) | Meets >=2,000 L/month flow demand |
| Outer diameter | >=100 mm (including insulation) | MLI >=20 mm, UHMWPE outer jacket 5 mm |
| Pipe materials | Aluminum alloy or CFRP (inner pipe) + MLI (middle layer) + UHMWPE outer jacket | Shares MLI technology with Volume III Section 3.5.4 high-temperature molten-salt insulated piping |
| Insulation performance | Heat loss <=5% over full 5 km pipeline | Water temperature 5 C; ambient -180 C to +120 C |
| Freeze-prevention design | Inner-wall heating cable (1-2 kW/km) | During lunar night powered by base or thermal storage to keep water >=5 C |
| Operating temperature | -180 C to +120 C (outer wall) / +5 C to +30 C (water inside) | UHMWPE outer jacket rated -250 C to +120 C, no extra temperature protection required |
| Pumping power | About 2-5 kW continuous | Pump station with sealed small diaphragm pump, MoS2-lubricated, mass <=300 kg, operating range -180 C to +50 C |


### 6.9 Underground Transportation System

#### 6.9.1 Skylight Lift System

Skylights are the only physical connection between underground base and surface.

**(a) Bridge crane/gantry crane (primary cargo channel)**

| Parameter | Design Value | Notes |
|:-----|:-----|:-----|
| Rated lifting capacity | >=20 t (lunar-gravity equivalent) | - |
| Lifting speed | 0.5-2 m/s (variable) | Loaded low speed, empty high speed |
| Lift height | 50-300 m | Depends on vertical offset between skylight and underground functional zones |
| Drive mode | Electric hoist (rack and pinion), MoS2 solid lubrication | Module 20 mm rack shared with Main Volume IV rack technology, used for vertical lift only |
| Power | About 30-50 kWe (peak during lifting) | Regenerative recovery during descent |
| Mass | <=8,000 kg (tower, hoist, rack/pinion, controls) | - |
| Operating temperature | -180 C to +120 C (surface-exposed) / -20 C to +30 C (underground section) | - |
| Lift-channel dimensions | Width >=5 m x depth >=5 m | Physically separated from personnel channel |

**(b) Crew elevator (personnel channel)**

| Parameter | Design Value | Notes |
|:-----|:-----|:-----|
| Capacity | 6-10 persons/trip | Includes EVA equipment stowage |
| Lift speed | 2-4 m/s | Higher than cargo lift speed |
| Cabin size | Inner diameter >=2.5 m x height about 3.0 m | Pressurized cabin, 70 kPa |
| Independent life support | >=2 h autonomous operation | - |
| Power | About 10-15 kWe (peak during lifting) | - |
| Mass | <=3,000 kg (cabin, hoist, controls) | - |

#### 6.9.2 Underground Horizontal Transport System

Primary underground transport modes are **electric rail** and **conveyors**.

**(a) Underground electric rail (primary option)**

| Parameter | Design Value | Notes |
|:-----|:-----|:-----|
| Gauge | 1.0 m (narrow gauge) | Fits constrained cross-sections in sealed pressurized segments |
| Rail profile | I-section, height ~80 mm | Local aluminum alloy or steel, ~20 kg/m |
| Freight consist | Electric traction unit + 2-3 small freight cars | Payload >=10 t, speed <=30 km/h |
| Power method | Overhead catenary (+/-10 kV DC, cable-fed underground) | - |
| Operating temperature | -20 C to +50 C | Cave thermal stability, MoS2 dry lubrication |

**(b) Continuous conveyor (auxiliary option)**

| Parameter | Design Value | Notes |
|:-----|:-----|:-----|
| Belt width | 0.5-1.0 m | - |
| Throughput | >=5 t/h | - |
| Power | About 5-10 kW (200 m transport distance, 10 m lift height) | - |
| Sealing design | Fully enclosed hood (aluminum alloy or CFRP) | Prevents dust contamination of material stream |
| Mass | <=2,000 kg (drive motor, belt, enclosure) | - |
| Operating temperature | -20 C to +50 C | Cave thermal stability, MoS2 on drive-drum bearings |


### 6.10 Phased Expansion Plan for Transportation Network

| Stage | Period | Core Transport Modes | Expansion Scope |
|:-----|:-----|:-----|:-----|
| **Stage 1** | Infrastructure Phase I | Unpressurized cargo rovers (one each for liquid water, aggregate, concentrate) + pressurized crew rover (1) + skylight bridge crane + crew elevator + mobile lightweight winch lift system (if water-ice site is at pit bottom) | - |
| **Stage 2** | Infrastructure Phase II to early industrialization | Double rover fleet + first insulated liquid-water pipeline + underground electric rail (initial 2-3 km) + first open light rail + rack sections + permanent cableway (replacing early winch system) | Start rail foundation, rack installation, and pipeline laying |
| **Stage 3** | Mature industrialization | Enclosed-tube rail on trunk lines + full underground rail coverage + layered skylight platforms + pipeline extension to mining sites and launch sites | Rovers retire from trunk transport and remain as short-haul feeders between mines and rail stations |


### 6.11 Transportation System Equipment Mass and Energy Summary

#### 6.11.1 Equipment Mass Summary (Stage 2 - Infrastructure Phase II)

| Equipment | Quantity | Unit Mass | Subtotal | Notes |
|:-----|:-----:|:-----|:-----|:-----|
| Unpressurized cargo rover | 2 | <=1,500 kg each | <=3,000 kg | Includes removable insulated water tank |
| Pressurized crew rover | 2 | <=3,000 kg each | <=6,000 kg | - |
| Small underground rover | 2 | <=600 kg each | <=1,200 kg | - |
| Skylight bridge crane | 1 | <=8,000 kg | <=8,000 kg | Includes tower, hoist, rack/pinion |
| Skylight crew elevator | 1 | <=3,000 kg | <=3,000 kg | Includes cabin and hoist |
| Underground electric rail (initial 2-3 km) | 1 set | <=5,000 kg | <=5,000 kg | Includes traction unit, track, catenary |
| Insulated liquid-water pipeline (5 km) | 1 set | <=3,000 kg | <=3,000 kg | Includes piping, MLI, heating cable, pump station |
| Continuous conveyor (2 sets) | 2 sets | <=2,000 kg/set | <=4,000 kg | - |
| Rack system (initial install tools/locks) | 1 set | <=2,000 kg | <=2,000 kg | Rack bodies locally manufactured in Volume V; excluded from launch mass |
| Cableway system (initial hoist/pulleys/cars) | 1 set | <=12,000 kg | <=12,000 kg | Cars <=4,000 kg (2 units) + hoist <=5,000 kg + pulleys/cable <=3,000 kg |
| Early winch lift system (Stage-1 only) | 1 set | <=1,500 kg | <=1,500 kg | Decommissioned in Stage 2 |
| **Total launch mass of transport system equipment** | - | - | **<=48,700 kg (~48.7 t)** | Includes early winch lift system |

#### 6.11.2 Daily Energy Overview (Stage 2 - Typical Lunar-Day Operation)

| Equipment | Quantity | Operating Hours per Day | Daily Energy | Energy Type |
|:-----|:-----:|:-----:|:-----:|:-----|
| Unpressurized cargo rovers | 2 | 8 h each | ~128 kWh | Battery charging |
| Pressurized crew rovers | 2 | 4 h each (not daily) | ~72 kWh | Battery charging |
| Skylight bridge crane | 1 | 4 h | ~120 kWh | Cable-fed power |
| Skylight crew elevator | 1 | 2 h | ~20 kWh | Cable-fed power |
| Underground electric rail | 1 set | 6 h | ~90 kWh | Catenary power |
| Insulated water pipeline (pump station) | 1 set | 24 h continuous | ~72 kWh | Cable-fed power |
| Continuous conveyor | 2 sets | 8 h each | ~80 kWh | Cable-fed power |
| Cableway system | 1 set | 4 h | ~800 kWh | Cable-fed power |
| Lighting, signaling, auxiliary systems | - | 12 h | ~30 kWh | Cable-fed power |
| **Total** | - | - | **~1,412 kWh/day** | - |


### 6.12 Pending Validation Items and Acceptance Criteria

| ID | Item | Validation Method | Success Criterion | Related Volume |
|:-----|:-----|:-----|:-----|:-----|
| **P1-T1** | Lunar range verification of unpressurized cargo rover | 1:1 rover prototype executes >=10 continuous full-load transport loops on real lunar terrain | Full-load range >=100 km; bearing/seal wear in lunar-dust environment <=1.5x design baseline | Volume IV |
| **P1-T2** | Full-function validation of skylight bridge crane | >=20 rated-load lift/descent cycles under real lunar gravity and vacuum | No rack/pinion jamming or cold welding; regenerative recovery >=60%; positioning accuracy <=10 cm | Volume II |
| **P1-T3** | Full-load 30 deg rack-mesh validation | >=100 tests on 1:1 rack section + train gear under simulated lunar 1/6 g and vacuum at full load on 30 deg slope | No abnormal tooth-surface wear; mesh noise <= design limit; mesh-force fluctuation <=20% over nominal | This volume |
| **P2-T1** | Low-pressure thermal management validation for enclosed-tube rail | Run 1:1 train model for >=6 h in low-pressure N2 (0.2 bar) test tube | Train cooling system remains nominal; tube-gas temperature <=50 C | Volume III |
| **P2-T2** | Long-term stability of insulated liquid-water pipeline | Continuous >=3-month run in simulated lunar thermal-vacuum environment including lunar-night low-temperature segment | Heat loss <=5%; heating cable fault-free; no pipeline leakage | Volume IV |
| **P2-T3** | Extreme-slope cableway operation validation | >=50 full-load braking and operation tests on 1:1 car on simulated 45 deg track | Emergency rail-clamp brake locks within 50 ms; braking distance <=1/2 car spacing; regenerative recovery >=60% | This volume |


### 6.13 Parameter Outputs

| Parameter | Value | Status | Receiving Volume |
|:---|:---|:---|:---|
| Unpressurized cargo rover full-load range | >=100 km | P1 pending validation | Volume IV |
| Pressurized crew rover range | >=200 km | Design baseline | Volume II |
| Rack-system max design slope | 30 deg (~58% grade) | Design baseline | This volume |
| Rack-system full-load contact-stress margin | 2.7:1 | Design passed | This volume |
| Cableway max slope | 45 deg (~100% grade) | Design baseline | This volume |
| Cableway max payload | 20 t/car (lunar-gravity equivalent) | Design baseline | Volume IV |
| Early winch system max single-lift payload | <=2 t | Design baseline | Volume IV |
| Skylight bridge crane lifting capacity | >=20 t | Design baseline | Volume V |
| Insulated water pipeline heat-loss rate | <=5% (5 km full length) | Design target | Volume IV |
| Total launch mass of transport system equipment (Stage 2) | <=48.7 t (net mass) | Order-of-magnitude estimate | Volume X |
| Total daily electricity use of transport system (Stage 2) | ~1,412 kWh/day | Order-of-magnitude estimate | Volume III |


### 6.14 Conclusion of Volume VI

This volume completes the integrated planning of the lunar industrial transportation network. Core contributions are:

1. **First full coverage of operating temperatures and lubrication requirements across the whole system.** Section 6.3 defines operating ranges for all surface-exposed moving parts (-180 C to +120 C, down to -250 C in PSR segments) and the MoS2 solid-lubrication strategy.

2. **First complete multi-load-case mechanical verification for rack systems.** Section 6.6.2 provides full traction-force, contact-stress, and bending-stress calculations for empty, medium, and full load cases. Under worst-case full load at 30 deg, contact-stress margin is 2.7:1 and bending-stress margin is 3.0:1; all cases are within safe range.

3. **First systematic consolidation of key component dimensions.** All key dimensions are explicitly provided in the relevant sections, including cargo rover envelope, rail profile height, gear pitch diameter, rack module, cableway car size, and pulley diameter.

4. **Initial/experimental pit-bottom-to-rim solution fills the temporary transport gap.** Section 6.7.1 introduces a mobile lightweight winch system to cover ice transport needs before permanent cableway completion in early infrastructure phases, and explicitly defines transition in parameter outputs and phased expansion plan.

5. **Permanent pit-bottom-to-rim cableway fills the extreme-slope transport gap.** Section 6.7.2 defines a dual-car balanced freight cableway for 30-45 deg extreme slopes where rack operation becomes impractical, with max 20 t/car and 1-8 m/s operation, seamlessly interfaced with rack trains at rim transfer platforms.

6. **Transport-system mass and energy are consolidated in Section 6.11.** Net total equipment mass is about 48.7 t, and total daily energy use is about 1,412 kWh.

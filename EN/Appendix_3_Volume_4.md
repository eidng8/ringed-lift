# Appendix III: Engineering Project Studies

## Volume 4: Lunar Electromagnetic Launch Scheme

**Version**: 1.7<br/>
**Compilation Date**: June 2026<br/>
**Currency Unit**: Chinese Yuan (CNY), symbol: ¥<br/>
**Related Main Volumes**: Appendix I Volume 5, Appendix III Volume 2

### Terminology Table

| Abbrev. | Full Name | Description |
|------|----------|------|
| HTS | High-Temperature Superconductor | High-temperature superconducting technology |
| LMO | Low Moon Orbit | Low lunar orbit |
| SMES | Superconducting Magnetic Energy Storage | Superconducting magnetic energy storage |
| YBCO | Yttrium Barium Copper Oxide | High-temperature superconducting tape |

### 1.1 Opening Notes

This volume focuses on a lunar electromagnetic launch system as an extension of Appendix III Volume 2 (lunar railway transport network). The system uses the Moon's low gravity (1/6 g) and vacuum environment to enable low-cost, high-frequency payload launch from the lunar surface to lunar orbit or Earth-Moon transfer trajectories.

This volume follows:
- **Appendix III Volume 2**: lunar railway network, providing logistics connections to launch sites.
- **Appendix I Volume 5**: lunar manufacturing system, providing locally manufactured launch payloads.

Core tasks of this volume:

1. Systematically organize principles and parameters of lunar electromagnetic launch concepts (linear-track type and rotating-arm type).
2. For 50-ton and 200-ton payloads, calculate launch parameters under both **cargo** and **crewed** operating conditions.
3. Consider the impact of lunar curvature on long linear tracks, as well as end-of-track direction and kinetic-energy loss.
4. Derive key equipment parameters in detail: track materials, energy storage, superconducting magnets, cooling systems, and more.

### 1.2 Physical Basis of Lunar Electromagnetic Launch

The lunar surface is a hard vacuum (~10^-12 bar), with almost no atmospheric drag, and gravity is only about 1.625 m/s^2 (one-sixth of Earth). This makes electromagnetic launch engineering significantly more feasible on the Moon than on Earth.

#### 1.2.1 Target Velocity

Lunar escape velocity (from lunar surface to escape the Earth-Moon system):

$$
v_{\text{esc}} = \sqrt{\frac{2GM_{\text{Moon}}}{R_{\text{Moon}}}} = \sqrt{\frac{2 \times 4.902\times10^{12}}{1.737\times10^{6}}} \approx 2.38\,\text{km/s}
$$

Required velocity to reach low lunar orbit (LMO) is about 1.68 km/s. To also support deep-space missions, this volume uses **2.4 km/s** (escape-class velocity) as the design baseline.

#### 1.2.2 Kinetic-Energy Requirement

For payload mass $m$, required kinetic energy is:

$$
E_k = \frac{1}{2} m v^2
$$

#### 1.2.3 Acceleration and Track Length

For a linear track with constant acceleration $a$, track length $L$ satisfies:

$$
v^2 = 2 a L \quad\Rightarrow\quad L = \frac{v^2}{2a}
$$

Launch (acceleration) time:

$$
t = \frac{v}{a}
$$

Peak power (at end of acceleration, assuming constant force):

$$
P = F v = (m a) v = m a v
$$

Maximum power appears near launch end and must be supplied by short-duration high-power storage.

### 1.3 Human Acceleration Tolerance Reference

During launch, astronauts use a reclined posture (back toward acceleration direction), with acceleration directed from chest to back, i.e., **positive Gx**. In this orientation, inertia presses the head into the headrest; the neck mainly experiences compression rather than a bending moment, reducing whiplash-type injury risk.

| Acceleration (g) | Tolerance Duration | Physiological Response | Applicable Scenario |
|:---:|:---:|:---|:---|
| 2.0 | Several minutes | Slightly heavy breathing, no major discomfort | Acceptable for ordinary passengers |
| 3.0 | 1-2 minutes | Restricted limb movement, breathing difficulty, training needed | Acceptable for professional astronauts |
| 4.0 | 20-30 seconds | Grey-out appears, consciousness remains clear but discomfort is strong | Short emergency use |
| 5.0 | 10-15 seconds | Tunnel vision, peripheral vision loss | Extreme condition |

**Crewed launch criteria**: use **a <= 2g** for ordinary passengers; **a <= 3g** for professional astronauts.

### 1.4 Linear-Track Electromagnetic Launch (Mass Driver)

A linear mass-driver system lays electromagnetic coils along a straight track to accelerate payloads stage by stage.

#### 1.4.1 Representative Existing Concepts (Lunar Use Only)

| Configuration | Representative Concept | Key Technical Parameters | Current Status | Source |
|------|----------|--------------|----------|----------|
| Linear-track type | O'Neill Mass Driver (1977) | 0.5 kg payload, 33 g, 36 m/s | Principle verification | [5] |
| Linear-track type | SpaceX/xAI TERAFAB (2026) | Tens-of-km track, escape velocity target | Concept design | [6] |
| Linear-track type | NASA JPL FLOAT (flexible mag-track) | Lunar freight, about 1 km/s | TRL 4-5 | [7] |

#### 1.4.2 End-of-Track Direction and Kinetic-Loss Analysis

The terminal direction of the electromagnetic track directly affects whether payload can accurately enter target trajectory. Optimal launch angle is about **20-30 degrees**. The track end should use an upward curved transition segment; curvature radius is determined by centripetal acceleration:

$$
a_{\text{rad}} = \frac{v^2}{R} \quad\Rightarrow\quad R = \frac{v^2}{a_{\text{rad}}}
$$

For a central angle of 25 degrees, arc length is $s = R \times \theta$ ($\theta$ in radians).

#### 1.4.3 Curved-Segment Parameters Under Different Conditions

Using target velocity $v = 2400\,\text{m/s}$:

| Condition | Acceleration Limit (g) | Curvature Radius $R$ (km) | Arc Length (25-degree central angle, km) |
|:---:|:---:|:---:|:---:|
| Cargo | 50 | $2400^2 / (50 \times 9.81) \approx 11.74$ | $11.74 \times 25 \times \pi/180 \approx 5.12$ |
| Crewed (professional, 3g) | 3 | $2400^2 / (3 \times 9.81) \approx 195.7$ | $195.7 \times 25 \times \pi/180 \approx 85.4$ |
| Crewed (comfort, 2g) | 2 | $2400^2 / (2 \times 9.81) \approx 293.6$ | $293.6 \times 25 \times \pi/180 \approx 128.1$ |

**Engineering feasibility of curved segment**:
- Cargo (50g): feasible; segment can directly follow lunar curvature.
- Crewed (3g/2g): requires dedicated elevated structures; feasible but higher cost.

#### 1.4.4 Cargo-Mode Derivation (50-ton payload, 50g)

- **Kinetic energy**:

$$
E_k = \frac{1}{2} \times 50\times10^3 \times (2400)^2 = 1.44\times10^{11}\,\text{J} = 40\,\text{MWh}
$$

- **Track length**:

$$
L = \frac{v^2}{2a} = \frac{2400^2}{2 \times 490.5} \approx \frac{5.76\times10^6}{981} \approx 5.87\,\text{km}
$$

- **Acceleration time**:

$$
t = \frac{v}{a} = \frac{2400}{490.5} \approx 4.89\,\text{s}
$$

- **Peak power**:

$$
P_{\text{peak}} = m a v = 50\times10^3 \times 490.5 \times 2400 \approx 5.89\times10^{10}\,\text{W} \approx 58.9\,\text{GW}
$$

- **Storage requirement**: with 90% flywheel-storage efficiency, required storage capacity is about **45 MWh**.

#### 1.4.5 Cargo-Mode Derivation (200-ton payload, 50g)

- **Kinetic energy**:

$$
E_k = \frac{1}{2} \times 200\times10^3 \times 2400^2 = 5.76\times10^{11}\,\text{J} = 160\,\text{MWh}
$$

- **Track length**: still **5.87 km**.
- **Acceleration time**: still **4.89 s**.
- **Peak power**:

$$
P_{\text{peak}} = 200\times10^3 \times 490.5 \times 2400 \approx 2.35\times10^{11}\,\text{W} \approx 235\,\text{GW}
$$

- **Storage requirement**: about **180 MWh**.

#### 1.4.6 Crewed-Mode Parameter Derivation

| Parameter | Professional Astronaut (3g) | Ordinary Passenger (2g) |
|:---|:---:|:---:|
| Acceleration (m/s^2) | $3 \times 9.81 = 29.43$ | $2 \times 9.81 = 19.62$ |
| Track length $L = v^2/(2a)$ (km) | $5.76\times10^6 / (2 \times 29.43) \approx 97.9$ | $5.76\times10^6 / (2 \times 19.62) \approx 146.9$ |
| Acceleration time $t = v/a$ (s) | $2400 / 29.43 \approx 81.6$ | $2400 / 19.62 \approx 122.4$ |
| Peak power $P = m a v$ (50 tons) | $50\times10^3 \times 29.43 \times 2400 \approx 3.53\,\text{GW}$ | $50\times10^3 \times 19.62 \times 2400 \approx 2.35\,\text{GW}$ |
| Peak power (200 tons) | $14.1\,\text{GW}$ | $9.41\,\text{GW}$ |
| Required energy (50/200 tons) | **40/160 MWh** | **40/160 MWh** |

#### 1.4.7 Linear-Track Parameter Summary

| Condition | Payload (tons) | Acceleration (g) | Track Length (km) | Accel Time (s) | Peak Power (GW) | Storage Need (MWh) |
|:---:|:---:|:---:|:---:|:---:|:---:|:---:|
| Cargo | 50 | 50 | **5.87** | 4.89 | 58.9 | 45 |
| Cargo | 200 | 50 | **5.87** | 4.89 | 235 | 180 |
| Crewed (professional) | 50 | 3 | **97.9** | 81.6 | 3.53 | 40 |
| Crewed (professional) | 200 | 3 | **97.9** | 81.6 | 14.1 | 160 |
| Crewed (comfort) | 50 | 2 | **146.9** | 122.4 | 2.35 | 40 |
| Crewed (comfort) | 200 | 2 | **146.9** | 122.4 | 9.41 | 160 |

#### 1.4.8 Improved Comfort-Launch Scheme: Two-Stage Electromagnetic Launch

For ordinary passengers (2g), the 146.9 km single-track scheme is difficult due to excessive length and elevation difference (~8.6 km). A **two-stage electromagnetic launch** is recommended:

| Stage | Acceleration (g) | Velocity Increment (km/s) | Track Length (km) | Description |
|:---:|:---:|:---:|:---:|:---|
| Stage 1 | 2 | 0 -> 1.2 | $(1200)^2 / (2 \times 19.62) \approx 36.7$ | Short straight track, directly follows lunar surface |
| Coast Segment | Unpowered | 1.2 | 0.5-1 km | Attitude adjustment, terminal sensor calibration |
| Stage 2 | 2 | 1.2 -> 2.4 | $(2400^2 - 1200^2) / (2 \times 19.62) \approx 110.2$ | Curved rise segment |
| **Total** | - | - | **about 147 km** | - |

Two-stage launch halves the curved-segment burden and significantly reduces overall engineering difficulty.

### 1.5 Rotating-Arm Electromagnetic Launch (Rotational Projector)

A rotating arm provides centrifugal acceleration, with centripetal acceleration related to arm length $R$ and angular velocity $\omega$:

$$
a = \omega^2 R,\qquad v = \omega R
$$

Given target velocity $v = 2400\,\text{m/s}$, required arm length is $R = v^2 / a$.

| Condition | Acceleration (g) | Required Arm Length (km) | Rotating Arm Diameter (km) | Angular Velocity (rad/s) |
|:---:|:---:|:---:|:---:|:---:|
| Cargo | 50 | $2400^2 / (50 \times 9.81) \approx 11.74$ | 23.5 | 0.204 |
| Crewed (professional) | 3 | $2400^2 / (3 \times 9.81) \approx 195.7$ | 391 | 0.0123 |
| Crewed (comfort) | 2 | $2400^2 / (2 \times 9.81) \approx 293.6$ | 587 | 0.00817 |

**Rotating-arm structural parameters (50g cargo case as theoretical reference)**

| Parameter | Value | Notes |
|------|------|------|
| Arm length | 11.74 km | - |
| Arm material | Carbon-fiber composite | Specific strength >= 2,000 kN.m/kg |
| Arm cross section | Box beam, 2x2 m | Hollow structure for mass reduction |
| Arm mass estimate | about 5,000-10,000 tons | Cables/arm body only |
| Central shaft | Superconducting maglev bearing | Diameter >= 10 m |
| Drive motor | Superconducting synchronous motor | GW-class power |
| Counterweight | Equal to payload mass | On opposite side |
| Launch frequency | Very low (re-acceleration required each cycle) | - |
| Energy recovery | >70% recoverable during braking | - |

**Conclusion**: For 50-200 ton launch missions, rotating-arm concepts are not engineering-feasible.

### 1.6 Effect of Lunar Curvature on Linear Tracks

With lunar radius $R_{\text{Moon}} = 1{,}737\,\text{km}$, lunar curvature causes an apparent elevation drop of about $\Delta h = L^2/(2R_{\text{Moon}})$ over distance.

| Track Length (km) | Elevation Difference Between Ends (m) | Average Grade (per mille) |
|:---:|:---:|:---:|
| 5.87 | $5.87^2/(2\times1737)\times1000 \approx 9.9$ | 1.69 |
| 97.9 | $97.9^2/(2\times1737)\times1000 \approx 2{,}758$ | 28.2 |
| 146.9 | $146.9^2/(2\times1737)\times1000 \approx 6{,}210$ | 42.3 |

**Recommended schemes**:
- Cargo (5.87 km): directly follow lunar surface curvature; no special treatment.
- Crewed (97.9 km): use an **elevated straight track**, with support height gradually increasing from 0 to about 2.8 km.
- Crewed (146.9 km): use two-stage electromagnetic launch (see Section 1.4.8).

### 1.7 Derivation of Key System Parameters

#### 1.7.1 Track Structural Parameters (50-ton Cargo Baseline)

| Parameter | Value | Basis |
|------|------|----------|
| Track length | 5.87 km | See Section 1.4.4 |
| Track width | 3 m | Fits 2.5 m payload cabin + safety margin |
| Track type | Dual-rail magnetic levitation | Similar to maglev rail |
| Rail material | Aluminum alloy (lunar-made) or steel | Lunar aluminum can be extrusion-formed |
| Maglev gap | 10-15 mm | Referencing terrestrial maglev systems |
| End curved-segment radius | Cargo: 12 km; Crewed 3g: 196 km; Crewed 2g: 294 km | See Section 1.4.3 |
| Track foundation | Lunar-regolith concrete (C30) | Thickness >= 0.5 m, compressive strength >= 20 MPa |
| Sleeper spacing | 0.6 m | Heavy-load standard |
| Rail mass per km (dual rail) | about 158 tons | U75V, 75 kg/m x 2 |

#### 1.7.2 Superconducting Magnet Parameters

| Parameter | Value | Notes |
|------|------|------|
| Magnet type | High-temperature superconducting (YBCO) | Critical temperature about 92 K |
| Operating temperature | 77 K (liquid nitrogen) | Lunar local production possible |
| Levitation force per magnet set | 50 kN | Design value |
| Magnet count | 1 set per meter | - |
| Total levitation force (50 tons) | about 500 kN | Safety factor 2 |
| Total magnet mass | about 10-20 tons | Includes cryogenic vessels |
| Field strength | 1-2 T | Meets levitation and guidance needs |
| Coil material | YBCO tape (12 mm width, 0.1 mm thickness) | Critical current >= 500 A |
| Cryogenic vessel | Aluminum-alloy vacuum-insulated chamber | Vacuum < 10^-4 Pa |

#### 1.7.3 Energy Storage Parameters (Flywheel Array)

| Parameter | 50-ton cargo | 200-ton cargo | Notes |
|------|:---:|:---:|------|
| Total storage (MWh) | 45 | 180 | - |
| Single-unit capacity (MWh) | 5 | 5 | - |
| Number of flywheels | 9 | 36 | Redundant design |
| Single-unit power (MW) | 200 | 200 | Discharge power |
| Flywheel material | Carbon-fiber composite | - | Limit peripheral speed >= 1,000 m/s |
| Flywheel diameter | 2 m | - | Speed about 10,000 rpm |
| Vacuum chamber | Lunar vacuum environment | - | No extra pumping required |
| Superconducting bearing | Magnetic-levitation bearing | - | Near-zero friction |
| Total system mass | about 300 tons | about 1,200 tons | Includes structure and cooling |
| Discharge efficiency | >=95% | - | - |

#### 1.7.4 Cooling System Parameters

| Parameter | Value | Notes |
|------|------|------|
| Refrigeration method | Stirling cryocooler | Mature lunar-applicable technology |
| Operating temperature | 77 K | Liquid-nitrogen range |
| Cooling power | about 100 kW (steady state) | Maintains superconducting magnets |
| Liquid nitrogen replenishment rate | about 0.5 ton/day | Lunar production possible |
| Lunar-night power supply | Nuclear power source | about 10 kWe |
| Heat rejection method | Radiator panels | Area >= 500 m^2 |

#### 1.7.5 Payload Cabin Design Parameters

| Parameter | Cargo Cabin | Crewed Cabin | Notes |
|------|:---:|:---:|------|
| Empty mass | 10 tons | 20 tons (incl. life support) | - |
| Dimensions | 3x3x5 m | 4x4x8 m | - |
| Acceleration load rating | 50g (longitudinal), 10g (lateral) | 3g (longitudinal), 2g (lateral) | - |
| Structural material | Aluminum alloy + steel | Aluminum alloy + composites | - |
| Cabin sealing | Unpressurized (cargo) | Fully pressurized (70 kPa, O2-N2 mix) | - |
| Vibration isolation | None (cargo rigidly fixed) | Multi-stage damping seats | - |
| Escape system | None | Small solid rocket (thrust >= 500 kN) | Emergency separation |
| Docking interface | Standard mechanical interface | Standard docking + airtight passage | - |

#### 1.7.6 Ground Infrastructure Requirements

| Facility | Requirement | Notes |
|------|------|------|
| Launch-site grading zone | Length >= 6 km (cargo) or >=100 km (crewed), width >=50 m | Requires lunar surface earthmoving |
| Elevated bridge (crewed) | Column height 0-2.8 km (3g) or 0-6.2 km (2g) | Prefabricated concrete columns |
| Storage power station | Flywheel-array footprint about 10,000 m^2 (50-ton case) | Includes cooling systems |
| Substation | Power >=60 GW (cargo) or >=4 GW (crewed) | Requires superconducting switchgear |
| Control center | Underground secure zone | At least 5 km from launch site |
| Rail interface | Standard gauge (1.5 m) | Connected to construction-material lines and mines |

### 1.8 Conclusions and Recommendations

1. **Linear-track mass-driver launch is the only feasible electromagnetic launch scheme for large-scale lunar logistics.**

2. **Cargo launch**: for 50-ton and 200-ton payloads, required track length is only about 6 km; curved segment radius is about 12 km; direct adaptation to lunar curvature is possible; storage demand is 45-180 MWh.

3. **Crewed launch**: use 3g for professional astronauts (about 98 km track), 2g for ordinary passengers (about 147 km track), both requiring elevated tracks or staged launch. The two-stage scheme splits the 2g crewed launch into Stage-1 straight track (36.7 km) and Stage-2 curved track (110.2 km), significantly reducing engineering difficulty.

4. **Rotating-arm schemes** are suitable only for small payloads (<1 ton) and cannot scale to tens of tons or crewed missions.

5. **Energy storage** should use flywheel arrays, charged by lunar nuclear plants or large solar-plus-storage systems.

6. **Track materials** should prioritize locally manufactured lunar aluminum profiles and regolith concrete; superconducting magnets and carbon-fiber flywheels should be transported from Earth.

7. **Lunar landing** is not suitable for electromagnetic braking; chemical retropropulsive landing remains the only economical, mature solution and is outside the scope of this volume.

### References

[5] O'Neill, G. "The High Frontier: Human Colonies in Space." 1977.

[6] SpaceX/xAI. "TERAFAB Project." 2026.

[7] NASA JPL. "FLOAT: Flexible Levitation on a Track." 2025.

[8] Shanghai Institute of Satellite Engineering. "Lunar Maglev Rotational Launch System." 2024.

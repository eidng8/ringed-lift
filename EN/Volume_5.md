# Volume 5: Elevator Climber (Cabin) Design

**Version**: 8.1 (Final Review)
**Compilation Date**: May 2026
**Currency Unit**: Renminbi (Yuan), symbol: ¥


## 5.1 Preface

This volume focuses on the configuration design of the elevator cabin, drive scheme demonstration, power supply system, and full-range kinematic analysis. Building on the cable/track sheath design parameters from Volume 4, it outputs key parameters such as cabin dimensions, cruising speed, one-way time, drive mechanism design, and power supply requirements, for integrated simulation verification in Volume 7.

Core tasks of this volume:

1. Starting from ergonomics, determine the spatial and volumetric baselines of the cabin, provide complete dimensional derivations for spindle and disc-shaped configurations, and present stage-wise insights.
2. Propose the **drive separation concept**—separating the drive mechanism from the cabin as an independent Drive Module (DM), with the cabin as a Payload Module (PM) mounted on it. The DM's geometric dimensions have no preset restrictions and are entirely determined by physical requirements. This concept is adaptable to Schemes A–C.
3. Complete full ascent and descent kinematic, mechanical, and thermal derivations and comparisons for all drive schemes (rocket drive, A–E).
4. Present power supply schemes (proof of infeasibility for onboard batteries, derivation of hybrid power supply schemes).
5. Output key data such as cruising speed, one-way time, DM/PM mass, rack and pinion mechanical parameters, etc.

### Overview of Schemes Discussed in This Volume

| Scheme | Description | Adaptable to Drive Separation Concept | Status |
|--------|-------------|:--:|:--:|
| Rocket Drive | Cabin equipped with rocket engines (chemical/electric propulsion), not relying on cable for traction | Not applicable | **Rejected** (Δv requirement ~19 km/s, chemical rocket mass ratio >74x) |
| A | Drive wheels directly clamp main cable (friction drive, no track sheath) | Adaptable | **Rejected** (Contact stress ~600 MPa > CNT transverse strength 200–300 MPa) |
| B | Multiple rows of friction wheels + track sheath with UHMWPE outer layer | Adaptable | **Rejected** (UHMWPE contact stress ~78 MPa > yield 20–25 MPa; heat dissipation exceeds by ~38x) |
| C | Rack and pinion (gear-rack engagement, full-length aluminum alloy 7075-T6) | Adaptable (main focus of this volume) | **Feasible in principle** (Tooth surface contact stress ~116 MPa, margin 1.72; tooth root bending stress ~55 MPa, margin 5%) |
| D | Hybrid scheme (low altitude B + mid/high altitude C) | — | Not recommended (B already rejected, scheme invalid) |
| E | Multi-index cable pulley traction (drive moved to ground/GEO end) | Not applicable (drive already on ground) | Long-term alternative (CNT strength must reach 20 GPa) |
| Electromagnetic Drive | Linear synchronous motor (LSM) non-contact drive | Not applicable (drive integrated in cable) | Long-term concept (requires superconducting wire technology breakthrough) |


## 5.2 Basic Design Parameters and Constraints

### 5.2.1 Total Cabin Mass and Design Configuration

| Configuration | Fully Loaded Mass | Payload | Applicable Stage |
|---------------|------------------|---------|-----------------|
| C2 (Design Baseline) | 200 t | ≤160 t | Stage 3–4 normal operation |
| Light Load | 50 t | ~10 t | Stage 1–2 trial operation |

### 5.2.2 Operation Segmentation

| Segment | Altitude Range | Length (km) | Local Gravity Range (m/s²) |
|---------|---------------|:--:|-----------------------------|
| Low Altitude | 0–5,000 km | 5,000 | 9.81 → 3.08 |
| Mid Altitude | 5,000–14,000 km | 9,000 | 3.08 → 0.96 |
| High Altitude | 14,000 km–GEO | 28,164 | 0.96 → 0.224 |

### 5.2.3 Variation of Gravity with Altitude

At any altitude z, gravitational acceleration:

$$
g(z) = \frac{GM_e}{(R_e + z)^2}
$$

Where GMₑ = 3.986004418×10¹⁴ m³/s², Rₑ = 6.371×10⁶ m.

Substituting representative altitudes:

z = 0 km (ground):

$$
g(0) = \frac{3.986\times10^{14}}{(6.371\times10^6)^2} \approx 9.81 \, \text{m/s}^2
$$

z = 5,000 km:

$$
r = 6.371\times10^6 + 5.0\times10^6 = 1.1371\times10^7 \, \text{m}
$$
$$
g(5,000) = \frac{3.986\times10^{14}}{(1.1371\times10^7)^2} = \frac{3.986\times10^{14}}{1.2930\times10^{14}} \approx 3.08 \, \text{m/s}^2
$$

z = 14,000 km:

$$
r = 6.371\times10^6 + 1.4\times10^7 = 2.0371\times10^7 \, \text{m}
$$
$$
g(14,000) = \frac{3.986\times10^{14}}{(2.0371\times10^7)^2} = \frac{3.986\times10^{14}}{4.1498\times10^{14}} \approx 0.96 \, \text{m/s}^2
$$

z = 42,164 km (GEO):

$$
r = 4.2164\times10^7 \, \text{m}
$$
$$
g(42,164) = \frac{3.986\times10^{14}}{(4.2164\times10^7)^2} = \frac{3.986\times10^{14}}{1.7778\times10^{15}} \approx 0.224 \, \text{m/s}^2
$$

### 5.2.4 Shared Physical Parameters

| Parameter | Symbol | Value | Unit |
|-----------|--------|-------|------|
| Earth's Gravitational Constant | GMₑ | 3.986×10¹⁴ | m³/s² |
| Earth's Equatorial Radius | Rₑ | 6.371×10⁶ | m |
| Surface Gravity | g₀ | 9.81 | m/s² |
| GEO Radius | $R_{GEO}$ | 4.2164×10⁷ | m |
| Comfort Acceleration Limit | $a_{comfort}$ | 0.4905 | m/s² |
| Full Load Weight (ground) | W | 1.962×10⁶ | N |
| Design Safety Factor | S | 2.0 | — |
| Cable Elastic Modulus | E | 1,000 | GPa |
| Main Cable Ground End Diameter | d₀ | 0.5 | m |
| Track Sheath Outer Diameter (incl. UHMWPE) | $D_{sheath}$ | ≈0.552 | m |
| Rack Speed Limit | $v_{limit}$ | 1,500 km/h = 416.67 m/s | — |


## 5.3 Cabin Shape Design—Ergonomics-Based

### 5.3.1 Spatial and Volumetric Baselines

**Spatial Baseline**: The inner diameter of the mid-section living module should not be less than 4.2 m ( $R_{in}$ = 2.1 m), as a non-negotiable minimum design constraint [5.1]. Reasons:

- **Physiological Constraint**: In microgravity, the human spine elongates by 3–5 cm, arm span is about 2.0 m. An inner diameter of 4.2 m ensures no collision with the cabin wall during floating movement.
- **Psychological Constraint**: In a 50-hour enclosed space, horizontal openness is key to preventing claustrophobia. 4.2 m is the minimum comfortable inner diameter validated by long-term on-orbit use of the ISS Harmony Node.
- **Functional Constraint**: After deducting the floor sandwich (0.3–0.4 m) and equipment cabinets on both sides (0.3 m each), there is still sufficient free activity cross-section.

**Volumetric Baseline**: 50 passengers + cargo, benchmarked to luxury long-distance cruise ship standards (8–10 m³ per person).

Volume allocation:
- 50 crew (8 m³ per person) = 400 m³
- Public activity area and corridors ≈ 100 m³
- Life support equipment ≈ 50 m³
- Cockpit/command module ≈ 50 m³
- Cargo hold ≈ 100 m³
- **Unified target volume $V_{target}$ = 700 m³** (net internal volume, excluding structural layers)

### 5.3.2 Spindle Shape (Streamlined, Long Axis Aligned with Cable Axis)

**Physical Orientation**: The cabin's long axis is aligned with the main cable axis (vertical spindle), so the long axis is the direction of travel during ascent/descent. $C_d ≈ 0.05$ [5.2], windward area is the frontal cross-section. This is the optimal aerodynamic configuration for the low-altitude segment.

**Structural Form**: Three modules in series—front (command/cockpit) + mid (living module) + rear (equipment/cargo module).

**Dimensional Derivation**:

Mid-section cylinder (inner diameter 4.2 m, R = 2.1 m, length $H_{mid} = 37 m$ ):

$$
V_{\text{mid}} = \pi R^2 H_{\text{mid}} = \pi \times (2.1)^2 \times 37
$$
$$
= 3.14159 \times 4.41 \times 37 \approx 512.6 \, \text{m}^3
$$

Front half-ellipsoid (major semi-axis a = 10 m along cable, minor semi-axis b = 2.8 m, decoupled from mid-section radius to improve cockpit space):

$$
V_{\text{front}} = \frac{2}{3} \pi a b^2 = \frac{2}{3} \times 3.14159 \times 10 \times (2.8)^2
$$
$$
= \frac{2}{3} \times 3.14159 \times 10 \times 7.84 \approx 164.2 \, \text{m}^3
$$

Rear half-ellipsoid is symmetric to the front, also ≈ 164.2 m³.

Total internal volume:

$$
V_{\text{total}} = 512.6 + 164.2 + 164.2 = 841.0 \, \text{m}^3
$$

Slightly exceeds the 700 m³ target, retained as equipment reserve space.

Shell structural layer 0.3 m (includes pressure shell + multilayer insulation + debris protection):

- Outer diameter: D = 4.2 + 2×0.3 = 4.8 m → round up to **ø5.0 m**
- Total length: L = 37 + 2×10 = 57 m → round up to **60 m** (includes 3 m equipment margin)

**Final spindle dimensions: ø5.0 m × 60 m**.

**Internal Space Features**: After deducting the central cable and track sheath (outer diameter ø0.552 m), usable space is an annular area, usable inner diameter about 4.4 m (shell inner diameter), radial width about (4.4 − 0.552)/2 ≈ 1.92 m. Usable cross-sectional area about π×(2.2²−0.276²) ≈ 14.97 m². On the same cross-section, up to about 14–20 people can stand side by side (tightly). At this stage, more suitable for cargo or small crew transport.

### 5.3.3 Disc Shape

**Structural Form**: Double-deck—upper deck for cockpit/work/living (height 6 m), lower deck for equipment/cargo (height 3 m), total internal height 9 m. Set inner diameter $R_{in}$ unified.

Additional volume (observation dome, docking passage, etc.) ≈ 100 m³.

Volume equation:

$$
\pi R_{\text{in}}^2 \times 9 + 100 = 700
$$
$$
\pi R_{\text{in}}^2 \times 9 = 600
$$
$$
R_{\text{in}}^2 = \frac{600}{9\pi} = \frac{600}{28.274} \approx 21.22
$$
$$
R_{\text{in}} = \sqrt{21.22} \approx 4.61 \, \text{m}
$$

Take inner diameter $D_{in} = 9.2 m$ ( $R_{in} = 4.6 m$ ). Internal volume check:

$$
V_{\text{main}} = \pi \times (4.6)^2 \times 9 = 3.14159 \times 21.16 \times 9 \approx 598.5 \, \text{m}^3
$$
$$
V_{\text{total}} = 598.5 + 100 = 698.5 \, \text{m}^3
$$

Consistent with the 700 m³ target.

Shell structural layer 0.3 m:

- Outer diameter = 9.2 + 2×0.3 = 9.8 m → round up to **ø10 m**
- Total height = 9.0 + 2×0.3 = 9.6 m → round up to **10 m**

**Final disc dimensions: ø10 m × 10 m**.

**Internal Space Features**: No cable passes through the center of the disc (cable passes through edge clamping mechanism or DM bridge), interior is a complete circular hall. Usable area per deck about π×(4.6)² ≈ 66.5 m², total for two decks about 133 m², about 2.66 m² per person. High horizontal openness, excellent space quality. At this stage, more suitable for large-scale passenger transport.

### 5.3.4 Comparison and Stage-wise Insights

| Parameter | Spindle | Disc |
|-----------|:------:|:----:|
| **Target Volume** | **700 m³** | **700 m³** |
| Actual Net Volume | ≈841 m³ (incl. equipment margin) | ≈699 m³ |
| Outer Diameter | 5.0 m | 10 m |
| Total Length/Height | 60 m | 10 m |
| Frontal Area | 19.6 m² | 78.5 m² |
| Headwind Drag (v=85.6 m/s) | ≈4.3 kN | ≈276 kN |
| Internal Space Form | Annular corridor (radial width ≈1.92 m) | Complete circular hall |
| Internal Space Quality | Suitable for short-term/cargo | Suitable for long-term/passenger |
| Drive Wheel Arrangement | Multiple axial rows | Single circumferential row |
| Drag Coefficient $C_d$ | 0.05 | 0.8 |

**Note: Stage-wise insights on cabin configuration and mission matching**

Under current technical constraints (cable passes through cabin center of mass, track sheath occupies central space), the spindle shape's annular internal space is more suitable for cargo or small crew missions, while the disc shape's open circular hall is better for large-scale passenger transport. In the long term, with breakthroughs in non-contact drive coupling (e.g., Scheme E multi-index cable or electromagnetic drive) and higher-strength CNT materials allowing further reduction in track sheath and cable diameter, new generations of cabins balancing streamlining and passenger needs can be designed. The spindle and disc comparison at this stage is only a scheme selection based on current engineering constraints and should not be regarded as the final answer for cabin configuration.


## 5.4 Rocket Drive Scheme

This section uses the Tsiolkovsky rocket equation to independently analyze the feasibility of a cabin carrying its own propulsion for the entire journey, based solely on rocket propulsion physics, without referencing constraints from other schemes (such as speed, acceleration/deceleration models, etc.).

### 5.4.1 Physical Constraints

The rocket-driven cabin takes off from the ground, ascends vertically to GEO (altitude 42,164 km), and does not rely on the cable for traction. The cabin carries all propellant.

Core constraints:
- Thrust must overcome gravity
- Propellant consumption determined by the Tsiolkovsky equation
- Propellant tank mass proportional to propellant mass

### 5.4.2 Total Δv Requirement

Δv from ground to GEO consists of:

**(1) Gravitational Potential Energy Component**

Potential energy difference per unit mass from ground ( $r=R_e$ ) to GEO ( $r=R_{GEO}$ ):

$$
\Delta E_{\text{unit}} = GM_e \left( \frac{1}{R_e} - \frac{1}{R_{GEO}} \right)
$$
$$
= 3.986\times10^{14} \times \left( \frac{1}{6.371\times10^6} - \frac{1}{4.2164\times10^7} \right)
$$
$$
= 3.986\times10^{14} \times (1.5696\times10^{-7} - 2.3717\times10^{-8})
$$
$$
= 3.986\times10^{14} \times 1.3324\times10^{-7} \approx 5.311\times10^7 \, \text{J/kg}
$$

For Hohmann transfer orbit, the potential energy corresponds to:

$$
\Delta v_{\text{pot}} \approx 10,300 \, \text{m/s}
$$

**(2) GEO Orbital Velocity Component**

GEO orbital velocity (Earth's synchronous circular velocity):

$$
v_{\text{GEO}} = \omega_e R_{GEO} = 7.2921\times10^{-5} \times 4.2164\times10^7 \approx 3,075 \, \text{m/s}
$$

Ground equatorial initial rotational velocity:

$$
v_{\text{ground}} = \omega_e R_e = 7.2921\times10^{-5} \times 6.371\times10^6 \approx 465 \, \text{m/s}
$$

Velocity increment:

$$
\Delta v_{\text{orbit}} = 3,075 - 465 = 2,610 \, \text{m/s}
$$

**(3) Gravity Loss**

Thrust must overcome gravity, loss is proportional to ascent time. For chemical rockets, ascent time is 10 minutes (600 s):

$$
\Delta v_{\text{gravity}} = g_0 \times t_{\text{ascent}} = 9.81 \times 600 \approx 5,886 \, \text{m/s}
$$

**(4) Atmospheric Drag Loss**

Empirical value:

$$
\Delta v_{\text{atm}} \approx 150 \, \text{m/s}
$$

**(5) Total Δv Summary**

$$
\Delta v_{\text{total}} = \Delta v_{\text{pot}} + \Delta v_{\text{orbit}} + \Delta v_{\text{gravity}} + \Delta v_{\text{atm}}
$$
$$
= 10,300 + 2,610 + 5,886 + 150 \approx 18,946 \, \text{m/s}
$$

Rounded to **19,000 m/s**.

### 5.4.3 Tsiolkovsky Equation

$$
\frac{m_0}{m_f} = \exp\left(\frac{\Delta v}{I_{sp} g_0}\right)
$$

Where $m_0$ is initial total mass (incl. propellant), $m_f$ is burnout mass (structure + payload), $I_{sp}$ is engine specific impulse.

### 5.4.4 Chemical Rocket Scheme

For LH₂/LOX rocket ( $I_{sp}$ ≈ 450 s), currently the most optimized chemical propulsion:

$$
\frac{m_0}{m_f} = \exp\left(\frac{19,000}{450 \times 9.81}\right)
$$
$$
= \exp\left(\frac{19,000}{4,414.5}\right) = \exp(4.305) \approx 74.1
$$

If burnout mass $m_f = 200 t$ (C2 full load), then initial total mass:

$$
m_0 = 200 \times 74.1 \approx 14,820 \, \text{t}
$$

Propellant mass = 14,820 − 200 = **14,620 t**.

Propellant tank mass (about 8%–12% of propellant mass, take 10%) ≈ 1,462 t. Adding engine, structure, etc. (about 5% of propellant mass, ≈731 t), actual burnout mass far exceeds 200 t. After iteration, $m_f$ ≈ 2,393 t, $m_0$ ≈ 177,000 t.

Clearly, a single run would require over 100,000 tons of chemical propellant, which is completely infeasible in terms of launch, refueling, cost, and safety.

For LOX/methane ( $I_{sp}$ ≈ 380 s):

$$
\frac{m_0}{m_f} = \exp\left(\frac{19,000}{380 \times 9.81}\right) = \exp(5.10) \approx 164
$$

Mass ratio is even more extreme.

### 5.4.5 Nuclear Thermal Rocket Scheme

Nuclear thermal rocket ( $I_{sp} ≈ 900 s$ , e.g., NERVA):

$$
\frac{m_0}{m_f} = \exp\left(\frac{19,000}{900 \times 9.81}\right)
$$
$$
= \exp\left(\frac{19,000}{8,829}\right) = \exp(2.152) \approx 8.60
$$

$m_f = 200 t → m_0 ≈ 1,720 t$ , propellant about 1,520 t. Although much lower than chemical rockets, still requires kiloton-level propellant. Nuclear thermal rockets also face political and safety restrictions for ground launch, currently not feasible.

### 5.4.6 Electric Propulsion Scheme

Xenon Hall thruster ( $I_{sp} ≈ 3,000 s$ ):

$$
\frac{m_0}{m_f} = \exp\left(\frac{19,000}{3,000 \times 9.81}\right)
$$
$$
= \exp\left(\frac{19,000}{29,430}\right) = \exp(0.646) \approx 1.91
$$

$m_f = 200 t → m_0 ≈ 382 t$ , propellant only 182 t. Propellant requirement is reasonable.

But the fatal weakness of electric propulsion is **thrust density**. The most powerful current electric propulsion systems have thrusts of only hundreds of mN to a few N. For example, NASA's AEPS (Advanced Electric Propulsion System, thrust about 0.6 N, power about 13 kW), to generate enough thrust to overcome cabin gravity (ground 1.96×10⁶ N):

$$
\text{Required AEPS units} = \frac{1.96\times10^6}{0.6} \approx 3.27\times10^6
$$
$$
\text{Total power} = 3.27\times10^6 \times 13\times10^3 \approx 4.25\times10^{10} \, \text{W} \approx 42.5 \, \text{GW}
$$

Even with future fusion power, such a scale of thruster array is not feasible. Moreover, low thrust leads to extremely long ascent times (months or even years), greatly increasing gravity loss and further increasing Δv requirement.

### 5.4.7 Conclusion

Chemical rockets, due to extremely high Δv requirements, result in mass ratios over 74x (requiring over ten thousand tons of propellant per run); nuclear thermal rockets reduce this to 8.6x but still require kiloton-level propellant and face political and safety restrictions; electric propulsion lacks sufficient thrust density to overcome gravity. **A cabin relying on its own rocket engine to reach GEO from the ground is physically and economically infeasible.** The drive scheme for this project must rely on the cable system.


## 5.5 Speed Limit Derivation and Basic Kinematics

### 5.5.1 Segment Lengths and Acceleration

Perceived acceleration strictly ≤ $a_{comfort} = 0.05g_0 = 0.4905 m/s²$ .

Gravity variation with altitude as per Section 5.2.3.

### 5.5.2 Ideal Pure Acceleration/Deceleration Model (Kinematic Upper Bound Reference)

Ignoring all engineering constraints (track sheath heat dissipation, rack speed limit, etc.), only considering kinematics and basic dynamics. Segment lengths: $L_{low}=5,000 km, L_{mid}=9,000 km, L_{high}=28,164 km$ . Acceleration strictly maintained at $a = 0.4905 m/s²$ .

**(1) Ascent (Ground→GEO)**

During ascent, gravity does not affect acceleration value (only affects drive system output power). Acceleration in all segments is $a = 0.4905 m/s²$ .

**Low Altitude Segment** (initial speed=0→final speed v₁):

$$
v_1^2 = 2a L_{\text{low}}
$$
$$
v_1^2 = 2 \times 0.4905 \times 5.0\times10^6 = 4.905\times10^6
$$
$$
v_1 = \sqrt{4.905\times10^6} \approx 2,214.7 \, \text{m/s} \approx 7,973 \, \text{km/h}
$$
$$
t_1 = \frac{v_1}{a} = \frac{2,214.7}{0.4905} \approx 4,514 \, \text{s} \approx 1.254 \, \text{h}
$$

**Mid Altitude Segment** (initial speed v₁→final speed v₂):

$$
v_2^2 = v_1^2 + 2a L_{\text{mid}}
$$
$$
= 4.905\times10^6 + 2\times0.4905\times9.0\times10^6
$$
$$
= 4.905\times10^6 + 8.829\times10^6 = 1.3734\times10^7
$$
$$
v_2 = \sqrt{1.3734\times10^7} \approx 3,706.1 \, \text{m/s} \approx 13,342 \, \text{km/h}
$$
$$
t_2 = \frac{v_2 - v_1}{a} = \frac{3,706.1 - 2,214.7}{0.4905} = \frac{1,491.4}{0.4905} \approx 3,041 \, \text{s} \approx 0.845 \, \text{h}
$$

**High Altitude Segment** (14,000 km→GEO, initial speed v₂≠0, final speed=0, asymmetric acceleration/deceleration):

Let acceleration segment length $s_1$ , deceleration segment length $s_2$ , maximum speed $v_{max}$ .

Acceleration segment:
$$
v_{\text{max}}^2 = v_2^2 + 2a s_1
$$

Deceleration segment:
$$
0 = v_{\text{max}}^2 - 2a s_2 \Rightarrow v_{\text{max}}^2 = 2a s_2
$$

Combine:
$$
v_2^2 + 2a s_1 = 2a s_2 \Rightarrow s_2 = s_1 + v_2^2/(2a)
$$

Also $s_1 + s_2 = L_{high} = 2.8164×10^7 m$ .

$$
s_1 + s_1 + \frac{v_2^2}{2a} = L_{\text{high}}
$$
$$
2s_1 = L_{\text{high}} - \frac{v_2^2}{2a}
$$

$$
\frac{v_2^2}{2a} = \frac{1.3734\times10^7}{0.981} \approx 1.400\times10^7 \, \text{m}
$$
$$
2s_1 = 2.8164\times10^7 - 1.400\times10^7 = 1.4164\times10^7
$$
$$
s_1 = 7.082\times10^6 \, \text{m} \approx 7,082 \, \text{km}
$$
$$
s_2 = L_{\text{high}} - s_1 = 28,164 - 7,082 = 21,082 \, \text{km}
$$

$$
v_{\text{max}}^2 = v_2^2 + 2a s_1 = 1.3734\times10^7 + 2\times0.4905\times7.082\times10^6
$$
$$
= 1.3734\times10^7 + 6.947\times10^6 = 2.0681\times10^7
$$
$$
v_{\text{max}} = \sqrt{2.0681\times10^7} \approx 4,548 \, \text{m/s} \approx 16,373 \, \text{km/h}
$$

$$
t_{3a} = \frac{v_{\text{max}} - v_2}{a} = \frac{4,548 - 3,706}{0.4905} \approx 1,717 \, \text{s} \approx 0.477 \, \text{h}
$$
$$
t_{3b} = \frac{v_{\text{max}}}{a} = \frac{4,548}{0.4905} \approx 9,272 \, \text{s} \approx 2.576 \, \text{h}
$$
$$
t_3 = 0.477 + 2.576 = 3.053 \, \text{h}
$$

**Total Ascent Time** = 1.254 + 0.845 + 3.053 = **5.152 h ≈ 0.215 d**.

**(2) Descent (GEO→Ground)**

Under strict g₀±0.05g₀ comfort constraint, kinematics is fully symmetric to ascent. Descent time also = **5.152 h**.

> **Note on Gravity Direction**: The above "symmetry" refers to the mirror symmetry of the perceived acceleration profile for ascent and descent, corresponding to the same kinematic time. Actual drive system output during descent is affected by gravity direction: acceleration segment gravity assists (drive requirement reduced), braking segment gravity opposes braking (brake must provide $g_{local} + a_{brake}$ total deceleration). In subsequent derivations for each scheme, local gravity effects are included for each segment.

> The ideal model is only a kinematic upper bound reference. Actual cruising speed is limited by rack speed (1,500 km/h) and low-altitude heat/strength constraints, much lower than the above ideal values.

### 5.5.3 Rack Speed Limit Derivation

Maximum rack speed is determined by interface resonance constraints. The local natural frequency of the cabin/DM frame is about 30–100 Hz. To avoid periodic excitation from rack segment interfaces causing resonance, take a 1/3 safety margin, i.e., interface passing frequency ≤ 30/3 = 10 Hz. Conservatively, $f_{interface} ≤ 15 Hz$ .

Rack segment length $L_{segment}$ , gear passing interface frequency:

$$
f_{\text{interface}} = \frac{v}{L_{\text{segment}}}
$$

Engineering constraint:

$$
v \leq f_{\text{interface,max}} \times L_{\text{segment}} = 15 \times L_{\text{segment}}
$$

| $L_{segment}$ (m) | $v_{max}$ (m/s) | $v_{max}$ (km/h) |
|------------------:|----------------:|-----------------:|
| 5 | 75 | 270 |
| 10 | 150 | 540 |
| 20 | 300 | 1,080 |
| 50 | 750 | 2,700 |
| 100 | 1,500 | 5,400 |

Take $L_{segment} ≥ 100 m$ (achievable in lunar/space factories), speed limit about 5,400 km/h.

**Conclusion**: Take $v_{limit} = 1,500 km/h = 416.67 m/s$ as the engineering recommended upper limit for the rack system—this value corresponds to a rack segment length ≥100 m, and retains about 3.6x resonance safety margin (1,500 vs 5,400 km/h).


## 5.6 Scheme A—Drive Wheels Directly Clamping Main Cable

*(As Scheme A has been thoroughly demonstrated as infeasible in Section 4.4 of Volume 4, only the conclusion is retained here. See Volume 4 for the derivation process.)*

**Conclusion**: **Scheme A (drive wheels directly clamping CNT cable) is mechanically infeasible**. Contact stress exceeds the cable's transverse load capacity, making safe operation impossible in both ascent and descent. Protective and functional interfaces (track sheath) are required for the cable.


## 5.7 Scheme B—Multiple Rows of Friction Wheels + Track Sheath UHMWPE Outer Layer

*(As Scheme B has been thoroughly demonstrated as infeasible in Section 4.12 of Volume 4, only the conclusion is retained here. See Volume 4 for the derivation process.)*

**Conclusion**: **Scheme B (friction wheels + track sheath UHMWPE outer layer) is mechanically and thermally infeasible in all ascent and descent conditions**:
1. UHMWPE contact stress (~96 MPa) exceeds its yield strength (20–25 MPa) by about 4–5 times.
2. Frictional power (109–229 MW) exceeds the system's heat dissipation limit (~6 MW) by about 18–38 times.


## 5.8 Scheme C—Rack and Pinion Drive (Gear-Rack Engagement)

### 5.8.1 Scheme Description

Drive method is changed from friction to gear-rack rolling engagement. The rack is integrated into the mid-layer of the track sheath, made of aluminum alloy 7075-T6, and formed integrally with the mid-layer. The gear is also aluminum alloy 7075-T6. Both are micro-arc oxidized (surface hardness ≥HV1000).

Rack parameters: module 20 mm, pressure angle 20°, trapezoidal teeth, overlap ratio ε≈2.0, tooth width 300 mm.
Gear parameters: pitch circle diameter 1.0 m, 50 teeth, **40 pairs** (arranged in 5 layers, 8 pairs per layer).

### 5.8.2 Rack and Pinion Mechanical Analysis

**(1) Design Traction Force**

Full load 200 t, including 0.05g₀ acceleration, safety factor S=2.0:

$$
F_{\text{traction}} = W \times 1.05 = 1.962\times10^6 \times 1.05 \approx 2.060\times10^6 \, \text{N}
$$
$$
F_{\text{design}} = F_{\text{traction}} \times S = 2.060\times10^6 \times 2.0 = 4.12\times10^6 \, \text{N}
$$

**(2) Number of Gear Pairs and Normal Force per Tooth**

40 pairs of gears (5 layers, 8 pairs per layer). Total normal force (pressure angle 20°):

$$
F_{n,\text{total}} = \frac{F_{\text{design}}}{\cos 20^\circ}
$$
$$
= \frac{4.12\times10^6}{0.9397} \approx 4.384\times10^6 \, \text{N}
$$

Overlap ratio ε=2.0, normal force per tooth:

$$
F_n = \frac{F_{n,\text{total}}}{N_{\text{pairs}} \times \varepsilon}
$$
$$
= \frac{4.384\times10^6}{40 \times 2} = \frac{4.384\times10^6}{80} \approx 5.48\times10^4 \, \text{N}
$$

**(3) Tooth Surface Contact Stress**

Gear tooth profile curvature radius at pitch circle ( $D_p=1.0 m$ ):

$$
\rho_1 = \frac{D_p}{2} \sin\alpha
$$
$$
= 0.5 \times \sin 20^\circ = 0.5 \times 0.3420 \approx 0.171 \, \text{m}
$$

Rack tooth profile curvature radius ∞, equivalent curvature radius $ρ_{eq} = 0.171 m$ .

Equivalent elastic modulus (both aluminum alloy 7075-T6, E=70 GPa, ν=0.33):

$$
E_{\text{eq}} = \frac{E}{2(1-\nu^2)}
$$
$$
= \frac{70\times10^9}{2 \times (1-0.33^2)} = \frac{70\times10^9}{2 \times (1-0.1089)}
$$
$$
= \frac{70\times10^9}{2 \times 0.8911} = \frac{70\times10^9}{1.7822} \approx 3.928\times10^{10} \, \text{Pa}
$$

Contact half-width (tooth width b = 300 mm = 0.30 m):

$$
a_h = \sqrt{\frac{4 F_n \rho_{\text{eq}}}{\pi b E_{\text{eq}}}}
$$
$$
= \sqrt{\frac{4 \times 5.48\times10^4 \times 0.171}{\pi \times 0.30 \times 3.928\times10^{10}}}
$$
$$
= \sqrt{\frac{3.748\times10^4}{3.703\times10^{10}}} \approx \sqrt{1.012\times10^{-6}} \approx 1.006\times10^{-3} \, \text{m} \approx 1.01 \, \text{mm}
$$

Maximum contact stress:

$$
\sigma_{\text{Hmax}} = \frac{2 F_n}{\pi a_h b}
$$
$$
= \frac{2 \times 5.48\times10^4}{\pi \times 1.006\times10^{-3} \times 0.30}
$$
$$
= \frac{1.096\times10^5}{9.483\times10^{-4}} \approx 1.156\times10^8 \, \text{Pa} \approx 116 \, \text{MPa}
$$

**Contact Stress Check**: Aluminum alloy 7075-T6 after micro-arc oxidation (surface hardness ≥HV1000), contact fatigue limit conservatively 300 MPa. Safety factor $S_H = 1.5$ :

$$
\sigma_{H,\text{allow}} = \frac{300}{1.5} = 200 \, \text{MPa}
$$

Actual 116 MPa < allowable 200 MPa, **margin about 1.72:1, passes**.

**(4) Tooth Root Bending Stress**

Total tooth height:

$$
h_{\text{tooth}} = 2.25 \times m_n = 2.25 \times 20 = 45 \, \text{mm} = 0.045 \, \text{m}
$$

Tooth root thickness (critical section, conservatively use standard trapezoidal tooth geometry):

$$
t_{\text{root}} \approx 1.5 \times m_n = 1.5 \times 20 = 30 \, \text{mm} = 0.03 \, \text{m}
$$

Section modulus (rectangular section, tooth width b = 300 mm):

$$
W = \frac{b \times t_{\text{root}}^2}{6}
$$
$$
= \frac{0.30 \times (0.03)^2}{6} = \frac{0.30 \times 9\times10^{-4}}{6} = 4.50\times10^{-5} \, \text{m}^3
$$

Tooth root bending moment (load at tooth tip, worst case):

$$
M_{\text{root}} = F_n \times h_{\text{tooth}}
$$
$$
= 5.48\times10^4 \times 0.045 \approx 2,466 \, N \cdotp m
$$

Bending stress:

$$
\sigma_F = \frac{M_{\text{root}}}{W}
$$
$$
= \frac{2,466}{4.50\times10^{-5}} \approx 5.48\times10^7 \, \text{Pa} \approx 55 \, \text{MPa}
$$

**Bending Stress Check**: Aluminum alloy 7075-T6 bending fatigue limit about 115 MPa (10⁷ cycles, conservative, source [5.8]). Safety factor $S_F = 2.0$ :

$$
\sigma_{F,\text{allow}} = \frac{115}{2.0} = 57.5 \, \text{MPa}
$$

Actual 55 MPa < allowable 57.5 MPa, **margin about 4.5%, passes in magnitude**.

### 5.8.3 Scheme C Ascent Full Kinematics—200 km/h Low Altitude Baseline

**Operation Logic**: Cabin departs ground at 200 km/h cruising speed for the low-altitude segment. Upon entering the mid-altitude segment, accelerates to 1,500 km/h (416.67 m/s) cruise. In the high-altitude segment, **runs at rack speed limit 416.67 m/s throughout** (cannot exceed limit), brakes to zero at GEO.

**(1) Low Altitude Ascent (0→5,000 km, cruise speed 200 km/h=55.56 m/s)**

Acceleration segment (0→55.56 m/s):

$$
s_{\text{acc,low}} = \frac{v_{\text{low}}^2}{2a}
$$
$$
= \frac{55.56^2}{2 \times 0.4905} = \frac{3,086.4}{0.981} \approx 3,146 \, \text{m} \approx 3.15 \, \text{km}
$$
$$
t_{\text{acc,low}} = \frac{v_{\text{low}}}{a}
$$
$$
= \frac{55.56}{0.4905} \approx 113.3 \, \text{s} \approx 0.0315 \, \text{h}
$$

Constant speed segment:

$$
s_{\text{const,low}} = 5,000 - 3.15 = 4,996.85 \, \text{km}
$$
$$
t_{\text{const,low}} = \frac{s_{\text{const,low}}}{v_{\text{low}}}
$$
$$
= \frac{4,996.85 \times 10^3}{55.56} \approx 89,930 \, \text{s} \approx 24.98 \, \text{h}
$$

**Low Altitude Ascent Total**: 5,000 km, 0.0315 + 24.98 = **25.01 h**.

**(2) Mid Altitude Ascent (5,000→14,000 km, from 200 km/h to 1,500 km/h)**

Initial speed 55.56 m/s, final speed 416.67 m/s. Acceleration segment:

$$
s_{\text{acc,mid}} = \frac{v_{\text{high}}^2 - v_{\text{low}}^2}{2a}
$$
$$
= \frac{416.67^2 - 55.56^2}{2 \times 0.4905}
$$
$$
= \frac{173,611 - 3,086}{0.981} \approx 173,800 \, \text{m} \approx 173.8 \, \text{km}
$$
$$
t_{\text{acc,mid}} = \frac{v_{\text{high}} - v_{\text{low}}}{a}
$$
$$
= \frac{416.67 - 55.56}{0.4905} = \frac{361.11}{0.4905} \approx 736 \, \text{s} \approx 0.204 \, \text{h}
$$

Constant speed segment:

$$
s_{\text{const,mid}} = 9,000 - 173.8 = 8,826.2 \, \text{km}
$$
$$
t_{\text{const,mid}} = \frac{s_{\text{const,mid}}}{v_{\text{high}}}
$$
$$
= \frac{8,826.2 \times 10^3}{416.67} \approx 21,183 \, \text{s} \approx 5.88 \, \text{h}
$$

**Mid Altitude Ascent Total**: 9,000 km, 0.204 + 5.88 = **6.08 h**.

**(3) High Altitude Ascent (14,000→GEO, 28,164 km, full speed 416.67 m/s)**

First, calculate terminal braking distance, i.e., distance required to brake from 416.67 m/s to zero at a=0.4905 m/s²:

$$
s_{\text{brake,high}} = \frac{v_{\text{high}}^2}{2a}
$$
$$
= \frac{416.67^2}{2 \times 0.4905} = \frac{173,611}{0.981} \approx 177,000 \, \text{m} = 177 \, \text{km}
$$

This braking segment is at the end of the high-altitude segment, 178 km before GEO (rounded). Braking time:

$$
t_{\text{brake,high}} = \frac{v_{\text{high}}}{a}
$$
$$
= \frac{416.67}{0.4905} \approx 849 \, \text{s} \approx 0.236 \, \text{h}
$$

Constant speed segment:

$$
s_{\text{const,high}} = 28,164 - 178 = 27,986 \, \text{km}
$$
$$
t_{\text{const,high}} = \frac{s_{\text{const,high}}}{v_{\text{high}}}
$$
$$
= \frac{27,986 \times 10^3}{416.67} \approx 67,180 \, \text{s} \approx 18.66 \, \text{h}
$$

**High Altitude Ascent Total**: 28,164 km, 18.66 + 0.236 = **18.90 h**.

**(4) Ascent Full Summary (200 km/h Low Altitude Scheme)**

| Segment | Distance (km) | Accel Time (h) | Const Time (h) | Brake Time (h) | Total Time (h) |
|---------|:-------------:|:--------------:|:--------------:|:--------------:|:--------------:|
| Low Altitude | 5,000 | 0.03 | 24.98 | — | 25.01 |
| Mid Altitude | 9,000 | 0.20 | 5.88 | — | 6.08 |
| High Altitude | 28,164 | — | 18.66 | 0.24 | 18.90 |
| **Total** | **42,164** | — | — | — | **49.99** |

### 5.8.4 Scheme C Ascent Full Kinematics—1,500 km/h Full-Speed Low Altitude (Reference, Heat Dissipation Pending)

**(1) Low Altitude Ascent (0→5,000 km)**

Acceleration segment (0→416.67 m/s):

$$
s_{\text{acc}} = \frac{416.67^2}{2 \times 0.4905} \approx 177 \, \text{km}, \quad t_{\text{acc}} \approx 0.236 \, \text{h}
$$

Constant speed segment (**no braking needed**, final speed is initial speed for mid-altitude):

$$
s_{\text{const}} = 5,000 - 177 = 4,823 \, \text{km}
$$
$$
t_{\text{const}} = \frac{4,823 \times 10^3}{416.67} \approx 11,575 \, \text{s} \approx 3.22 \, \text{h}
$$

**Low Altitude Ascent Total**: 0.236 + 3.22 = **3.46 h**.

**(2) Mid Altitude Ascent**: Full speed 416.67 m/s throughout, **6.00 h**.

**(3) High Altitude Ascent**: Same as 200 km/h scheme, **18.90 h**.

**Ascent Full Summary (Full-Speed Scheme)**:

| Segment | Time (h) |
|---------|:--------:|
| Low Altitude | 3.46 |
| Mid Altitude | 6.00 |
| High Altitude | 18.90 |
| **Total** | **28.36** |

### 5.8.5 Scheme C Descent Full Kinematics—200 km/h Low Altitude Scheme

**Operation Logic**: Descent starts from GEO, gravity assists acceleration to rack speed limit 416.67 m/s, runs at constant speed into mid-altitude. Mid-altitude remains at speed limit. **Before entering low altitude (end of mid-altitude), must decelerate to 200 km/h** to ensure no overspeed in low altitude. Low altitude cruises at 200 km/h, brakes to zero at ground station.

**(1) High Altitude Descent (GEO→14,000 km, 28,164 km)**

Gravity at GEO ~0.224 m/s², gravity assists acceleration. Accelerate to 416.67 m/s:

$$
s_{\text{acc}} = \frac{416.67^2}{2 \times 0.4905} \approx 177 \, \text{km}, \quad t_{\text{acc}} \approx 0.236 \, \text{h}
$$

Constant speed segment (at 416.67 m/s, **no braking needed**, directly enters mid-altitude):

$$
s_{\text{const}} = 28,164 - 177 = 27,987 \, \text{km}
$$
$$
t_{\text{const}} = \frac{27,987 \times 10^3}{416.67} \approx 67,180 \, \text{s} \approx 18.66 \, \text{h}
$$

**High Altitude Descent Total**: 0.236 + 18.66 = **18.90 h**.

**(2) Mid Altitude Descent (14,000→5,000 km, 9,000 km)**

Full speed 416.67 m/s throughout, **but must decelerate to 200 km/h (55.56 m/s) at end of mid-altitude** to ensure no overspeed in low altitude.

Braking segment (416.67→55.56 m/s):

$$
s_{\text{dec}} = \frac{416.67^2 - 55.56^2}{2 \times 0.4905}
$$
$$
= \frac{173,611 - 3,086}{0.981} \approx 173,800 \, \text{m} \approx 173.8 \, \text{km}
$$
$$
t_{\text{dec}} = \frac{416.67 - 55.56}{0.4905} \approx 736 \, \text{s} \approx 0.204 \, \text{h}
$$

Constant speed before braking:

$$
s_{\text{const}} = 9,000 - 173.8 = 8,826.2 \, \text{km}
$$
$$
t_{\text{const}} = \frac{8,826.2 \times 10^3}{416.67} \approx 21,183 \, \text{s} \approx 5.88 \, \text{h}
$$

**Mid Altitude Descent Total**: 5.88 + 0.204 = **6.08 h**.

**(3) Low Altitude Descent (5,000→0 km, cruise speed 200 km/h)**

Entry speed is 55.56 m/s (ensured by mid-altitude end braking), full constant speed.

Constant speed segment:

$$
s_{\text{const}} = 5,000 - 3.15 = 4,996.85 \, \text{km}
$$
$$
t_{\text{const}} = \frac{4,996.85 \times 10^3}{55.56} \approx 89,930 \, \text{s} \approx 24.98 \, \text{h}
$$

Terminal braking segment (55.56→0 m/s):

$$
s_{\text{brake}} = \frac{55.56^2}{2 \times 0.4905} \approx 3,146 \, \text{m} \approx 3.15 \, \text{km}
$$
$$
t_{\text{brake}} \approx 0.0315 \, \text{h}
$$

**Low Altitude Descent Total**: 5,000 km, 24.98 + 0.0315 = **25.01 h**.

**(4) Descent Full Summary (200 km/h Low Altitude Scheme)**

| Segment | Distance (km) | Time (h) |
|---------|:-------------:|:--------:|
| High Altitude | 28,164 | 18.90 |
| Mid Altitude | 9,000 | 6.08 |
| Low Altitude | 5,000 | 25.01 |
| **Total** | **42,164** | **49.99** |

**Ascent and descent times are symmetric, one-way about 50 h.**

### 5.8.6 Scheme C Descent—1,500 km/h Full-Speed Low Altitude (Reference)

Entry speed to low altitude is 416.67 m/s (no need for mid-altitude pre-braking), constant speed 4,823 km/3.22 h, terminal braking 177 km/0.236 h. Total about **3.46 h**.

Full descent: high altitude 18.90 + mid altitude 6.00 + low altitude 3.46 = **28.36 h**.

### 5.8.7 Scheme C Power Requirement and Heat Dissipation (Considering Gravity Variation)

**Ascent Traction Force** (including acceleration, based on local gravity):

$$
F_{\text{traction}}(z) = m \times [g(z) + a_{\text{comfort}}]
$$

At ground (z=0):

$$
F_{\text{traction,max}} = 2\times10^5 \times (9.81 + 0.4905) \approx 2.060\times10^6 \, \text{N}
$$

Low altitude cruise at 200 km/h (55.56 m/s), traction power (take ground maximum as conservative design):

$$
P_{\text{low}} = F_{\text{traction,max}} \times v_{\text{low}} = 2.060\times10^6 \times 55.56 \approx 1.144\times10^8 \, \text{W} \approx 114.4 \, \text{MW}
$$

Rack system total efficiency η≈0.93 (gear 98% + motor 95%), heat generation:

$$
P_{\text{heat,low}} = P_{\text{low}} \times (1 - \eta) = 114.4 \times 0.07 \approx 8.0 \, \text{MW}
$$

Mid altitude cruise at 1,500 km/h (416.67 m/s), gravity drops to 3.08–0.96 m/s². At mid altitude start (5,000 km):

$$
F_{\text{traction,mid}} = 2\times10^5 \times (3.08 + 0.4905) \approx 7.14\times10^5 \, \text{N}
$$

Mid altitude power:

$$
P_{\text{mid}} = F_{\text{traction,mid}} \times v_{\text{high}} = 7.14\times10^5 \times 416.67 \approx 2.975\times10^8 \, \text{W} \approx 297.5 \, \text{MW}
$$
$$
P_{\text{heat,mid}} = 297.5 \times 0.07 \approx 20.8 \, \text{MW}
$$

High altitude gravity is even lower (0.96 m/s² at 14,000 km down to 0.224 m/s² at GEO). Take high altitude midpoint (~21,000 km) gravity about 0.59 m/s² as average:

$$
F_{\text{traction,high}} \approx 2\times10^5 \times (0.59 + 0.4905) \approx 2.16\times10^5 \, \text{N}
$$
$$
P_{\text{high}} = 2.16\times10^5 \times 416.67 \approx 9.00\times10^7 \, \text{W} \approx 90 \, \text{MW}
$$
$$
P_{\text{heat,high}} = 90 \times 0.07 \approx 6.3 \, \text{MW}
$$

**Heat Dissipation Summary**:

| Segment | Power (MW) | Heat (MW) | Heat Dissipation Scheme |
|---------|:----------:|:---------:|------------------------|
| Low Altitude (200 km/h) | 114.4 | 8.0 | Convection + radiation + liquid cooling, controllable (see 5.10.5) |
| Mid Altitude (1,500 km/h) | 297.5 | 20.8 | Radiation + liquid cooling, to be evaluated in Volume 7 |
| High Altitude (1,500 km/h) | 90 | 6.3 | Radiator panels sufficient |

**Conclusion**: Scheme C passes mechanical checks, 200 km/h low altitude heat is controllable. Gravity decreasing with altitude reduces mid altitude power to 297.5 MW (not previous 858 MW), greatly improving thermal management feasibility.


## 5.9 Scheme D

**Scheme D** is naturally invalidated due to B being rejected, and will not be independently derived.


## 5.10 Drive Separation Concept and DM/PM Design

### 5.10.1 Concept Proposal and Operation Logic

The drive separation concept separates the drive mechanism as DM, with the cabin as PM mounted below. DM can be adapted to Schemes A–C; since A and B are rejected, this volume only derives full parameters for Scheme C (rack DM).
Only preliminary concepts are discussed here for basic derivation; specific drive mechanisms will be adjusted as needed. For example, multiple DMs can be used simultaneously above and below the cabin (PM) for traction and pushing.

**DM is not routinely loaded/unloaded with PM.** When the cabin (PM) arrives at the ground station, the DM remains on the cable, fixed by ground station mechanisms (robotic arm or clamp); the DM's own clamping mechanism then releases and detaches from the track sheath, exerting no force on the track sheath or main cable, fully supported by ground mechanisms. The PM is then laterally moved to the loading/unloading area. After loading, the PM reconnects to the DM, the DM's clamping mechanism re-engages the track sheath, and the ground fixture releases.

### 5.10.2 DM Geometric Dimensions

40 pairs of gears in 5 layers, 8 pairs per layer, interlayer spacing 1.8 m. DM length = **10.0 m**.

Radial envelope (including gears, motors, liquid cooling pipes) about 3.5 m, outer diameter = **4.0 m**. Deployable radiator panels ≥ **500 m²**.

### 5.10.3 Drive Force Feasibility Verification

DM must generate sufficient traction/braking force through 40 pairs of gears. Single gear pair rated tangential force ( $F_{design} =4.12×10⁶ N$ , see 5.8.2):

$$
F_{\text{single pair}} = \frac{F_{\text{design}}}{N_{\text{pairs}}} = \frac{4.12\times10^6}{40} \approx 1.03\times10^5 \, \text{N}
$$

Gear pitch circle diameter 1.0 m, single pair gear torque:

$$
\tau_{\text{single pair}} = F_{\text{single pair}} \times \frac{D_p}{2} = 1.03\times10^5 \times 0.5 \approx 5.15\times10^4 \, N \cdotp m
$$

After 5:1 reduction, motor side torque:

$$
\tau_{\text{motor}} = \frac{\tau_{\text{single pair}}}{i} = \frac{5.15\times10^4}{5} \approx 1.03\times10^4 \, N \cdotp m
$$

40 motors total mechanical power (200 km/h low altitude, $P_{low} =114.4 MW$ , see 5.8.7):

$$
P_{\text{total}} = \frac{P_{\text{low}}}{\eta_{\text{gear}}} = \frac{114.4}{0.98} \approx 116.7 \, \text{MW}
$$

Single motor power:

$$
P_{\text{single}} = \frac{116.7}{40} \approx 2.92 \, \text{MW}
$$

Within the range of large PMSMs. During ascent and descent, gear engagement force direction is symmetric, and DM structural design accounts for this.

### 5.10.4 DM/PM Mass

| Component | DM (t) | PM (t) |
|-----------|:------:|:------:|
| Gears (40 pairs, aluminum alloy) | 12.0 | — |
| Reducers (5:1 planetary, 40 units) | 10.0 | — |
| Motors (PMSM, 40 units) | 6.0 | — |
| Brakes/liquid cooling/PCM/panels/frame/power/other | 21.3 | — |
| Structural shell (CFRP, spindle surface area ~942 m²) | — | 9.4 |
| Life support/interior/guide wheels/interfaces | — | 10.0 |
| Buffer battery (25 MWh, solid-state Li battery 500 Wh/kg) | — | 50.0 |
| **Subtotal** | **≈49.3 t** | **≈69.4 t** |

(Material property data: aluminum alloy 7075-T6 density and fatigue data [5.8], CFRP surface density 10 kg/m², solid-state Li battery energy density 500 Wh/kg [5.3].)

Full load total mass = 49.3 + 69.4 + ≤81.3 (payload) = 200 t.

### 5.10.5 DM Thermal Analysis—Full Range

**Low Altitude (200 km/h)**: Heat generation ~8 MW (see 5.8.7 $P_{heat,low}$ ). Heat dissipation paths:

| Path | Capacity | Condition |
|------|:--------:|-----------|
| Atmospheric convection (0–5 km dense segment) | ≤5 MW | DM surface area 125 m², convection coefficient 50 W/m²·K, ΔT 150 K |
| Radiator panels (500 m², 400 K, ε=0.85) | ≈0.62 MW | — |
| Body radiation (125 m², 350 K) | ≈0.15 MW | — |
| Phase change storage (LiF 500 kg, 1 MJ/kg) | 500 MJ buffer | Covers about 62 s full power heat |
| Liquid cooling for remainder | ~2.2 MW | NaK working fluid, ΔT 100 K, flow ~20 kg/s |

**Low altitude heat dissipation is fully controllable**.

**Mid Altitude (1,500 km/h)**: Heat generation ~20.8 MW (see 5.8.7 $P_{heat,mid}$ ). Out of atmosphere, only radiation. 500 m² panel ≈0.62 MW, expand to 2,000 m² ≈2.5 MW, LiF buffer 500 MJ ≈24 s full power. Remaining ~17.7 MW must be handled by active liquid cooling + large radiator panels (≥3,000 m²) combined. **Mid altitude heat dissipation scheme to be determined in Volume 7.**

**High Altitude**: Heat generation ~6.3 MW (see 5.8.7), 1,000 m² radiator panel suffices.

## 5.11 Power Supply Scheme

### 5.11.1 Onboard Battery Scheme

Using 200 km/h low altitude as baseline, segment power and time as per 5.8.3 and 5.8.7.

Total ascent energy:

$$
E_{\text{low}} = P_{\text{low}} \times t_{\text{low}} = 114.4 \times 25.01 \approx 2,861 \, \text{MWh}
$$
$$
E_{\text{mid}} = P_{\text{mid}} \times t_{\text{mid}} = 297.5 \times 6.08 \approx 1,809 \, \text{MWh}
$$
$$
E_{\text{high}} = P_{\text{high}} \times t_{\text{high}} = 90 \times 18.90 \approx 1,701 \, \text{MWh}
$$
$$
E_{\text{total}} = 2,861 + 1,809 + 1,701 \approx 6,371 \, \text{MWh}
$$

Specific energy requirement:

$$
k = \frac{E_{\text{total}}}{m_{\text{total}}} = \frac{6,371\times10^6 \times 3,600}{200,000} \approx 1.147\times10^8 \, \text{J/kg} \approx 31,900 \, \text{Wh/kg}
$$

Compare battery technology: Li-ion 250 Wh/kg, solid-state 500 Wh/kg, Li-S 800 Wh/kg, Li-air future 2,000 Wh/kg [5.3]. **Specific energy requirement 31,900 Wh/kg far exceeds any foreseeable electrochemical storage system. Pure onboard battery scheme is physically invalid.**

### 5.11.2 Hybrid Power Supply Scheme

As proven in 5.11.1, pure onboard battery scheme is physically infeasible (specific energy requirement 31,900 Wh/kg, far beyond battery technology limits). This section provides a complete derivation of external power supply schemes.

#### Power Supply Architecture

Full range uses segmented hybrid power supply, external supply options include:

| Scheme | Principle | Physical Limitation | Judgment |
|--------|-----------|--------------------|:--------:|
| Full-length conductive rail | Conductive rail along entire track sheath, ground power station direct supply | Track sheath mid-layer aluminum cross-section only ~5,010 mm², 42,164 km total resistance about 875 Ω, transmission loss far exceeds cabin power demand | Rejected |
| Full-length microwave power | Ground/on-orbit microwave transmission, cabin reception | Wavelength long (cm), far-field diffraction requires huge receiving antenna (hundreds of m²), cabin geometry cannot accommodate | Rejected |
| Full-length laser power (ground station) | Single ground laser station for full range | Laser attenuation and scattering after passing through dense atmosphere increases sharply over hundreds of km; after 5,000 km, atmosphere is thin, but single ground station beam aiming and tracking accuracy is hard to maintain over tens of thousands of km | Rejected |
| Full-length laser power (GEO station) | Single GEO laser station for full range | Requires large-scale laser and power supply at GEO; passing through atmosphere downward also faces attenuation and scattering | Rejected |
| **Segmented hybrid power** | **0–100 km conductive rail + 100–5,000 km ground laser + 5,000 km–GEO on-orbit laser** | **Each segment uses the most physically reasonable supply method for that segment** | **Recommended** |

**Physical logic for segmentation**:

- **0–100 km (dense atmosphere)**: Laser and microwave are severely affected by atmospheric attenuation and turbulence, while conductive rail can use existing track sheath aluminum layer, no extra wiring needed. Within 100 km, aluminum rail resistance loss is acceptable (see below), and low altitude convection aids heat dissipation.
- **100–5,000 km (low altitude)**: Atmospheric density drops sharply (at 100 km, less than 10⁻⁶ of ground), laser attenuation greatly reduced. Ground laser station can be deployed near anchor node, using stable ground platform for emission. This segment is not suitable for continued use of conductive rail—distance from ground exceeds 100 km, rail extension causes excessive cumulative resistance and unacceptable loss.
- **5,000 km–GEO (mid/high altitude)**: Too far from ground, ground laser beam divergence and aiming accuracy become bottlenecks. But this segment coincides with the GEO ring—large solar arrays can be deployed on the ring (see overview), powering lasers to illuminate the cabin from above or horizontally. On-orbit laser power comes from on-orbit PV, no need to transmit energy from ground.
- **Full range**: Onboard buffer battery handles short interruptions and peak smoothing, as any external supply chain has risk of momentary interruption (e.g., brief laser tracking loss, conductive rail switching segment power loss).

#### Conductive Rail Power Supply (0–100 km)

Conductive rail uses track sheath mid-layer aluminum (cross-section ~5,010 mm²).

**(1) Circuit Resistance**

Power supply uses dual-rail system (aluminum layer divided into two poles by axial insulation grooves). Total round-trip length L = 200 km = 2×10⁵ m.

Single pole effective cross-section $A_{single} ≈ 2,505 mm² = 2.505×10⁻³ m²$ .

Aluminum alloy 7075-T6 resistivity $ρ_{Al} = 5.2×10⁻⁸ Ω·m$ [4.4].

Single pole resistance:

$$
R_{\text{single}} = \rho_{\text{Al}} \frac{L}{A_{\text{single}}} = \frac{5.2\times10^{-8} \times 2\times10^5}{2.505\times10^{-3}} \approx 4.15 \, \Omega
$$

Dual pole series total circuit resistance $R_{circuit} = 2 × 4.15 = 8.30 Ω$ .

(If four-way parallel is used, circuit resistance can be reduced to about 2.08 Ω. This derivation uses dual-pole as a conservative baseline.)

**(2) Supply Voltage and Current**

Cabin low altitude power required (see 5.8.7): $P_{req} = 114.4 MW$ (200 km/h scheme).

Supply voltage U = 25 kV (AC, compatible with railway traction supply). Power factor cosφ = 0.85.

Required current:

$$
I = \frac{P_{\text{req}}}{U \times \cos\phi} = \frac{114.4\times10^6}{25\times10^3 \times 0.85} = \frac{114.4\times10^6}{21,250} \approx 5,384 \, \text{A}
$$

(Note: For four-way parallel, each path current about 2,692 A; if voltage raised to 50 kV, current halves to 2,692 A.)

**(3) Transmission Loss**

$$
P_{\text{loss}} = I^2 R_{\text{circuit}} = (5,384)^2 \times 8.30 = 2.899\times10^7 \times 8.30 \approx 2.406\times10^8 \, \text{W} \approx 240.6 \, \text{MW}
$$

Transmission loss 240.6 MW exceeds cabin power demand 114.4 MW, transmission efficiency only about 32%. **Dual-pole 25 kV scheme is unacceptable due to excessive circuit resistance loss.**

**(4) Optimization Schemes**

**Scheme 1 (Increase voltage to 50 kV):**

Current halves to 2,692 A:

$$
P_{\text{loss}} = (2,692)^2 \times 8.30 \approx 7.247\times10^6 \times 8.30 \approx 60.2 \, \text{MW}
$$

Transmission efficiency ≈ 114.4/(114.4 + 60.2) ≈ 65.5%, much improved but still low.

**Scheme 2 (Four-way parallel + 50 kV):**

Circuit resistance drops to 2.08 Ω, current 2,692 A:

$$
P_{\text{loss}} = (2,692)^2 \times 2.08 \approx 7.247\times10^6 \times 2.08 \approx 15.1 \, \text{MW}
$$

Transmission efficiency ≈ 114.4/(114.4 + 15.1) ≈ 88.3%, **acceptable**.

**Scheme 3 (Increase voltage to 100 kV + four-way parallel):**

Current drops to 1,346 A:

$$
P_{\text{loss}} = (1,346)^2 \times 2.08 \approx 1.812\times10^6 \times 2.08 \approx 3.8 \, \text{MW}
$$

Transmission efficiency ≈ 114.4/(114.4 + 3.8) ≈ 96.8%, **excellent**.

**Insulation Risk Note**: 100 kV AC scheme under vacuum, low pressure, and surface creepage conditions imposes very strict insulation requirements on the 20 mm UHMWPE outer layer, with much higher local discharge and surface flashover risk than the 50 kV scheme. Engineering-wise, 50 kV + four-way parallel is recommended as the design baseline, 100 kV scheme to be evaluated after future insulation technology advances.

**(5) Conductive Rail Heat Check (Scheme 2 Baseline)**

Transmission loss 15.1 MW over 200 km conductor, per meter heat:

$$
q' = \frac{P_{\text{loss}}}{L} = \frac{15.1\times10^6}{2\times10^5} \approx 75.5 \, \text{W/m}
$$

Track sheath circumference about 1.73 m (regular octagon circumscribed circle ø0.552 m). Aluminum surface after anodizing emissivity 0.8 [4.5]. Steady-state temperature $T_s$ for radiative cooling:

$$
q' = \varepsilon \sigma (T_s^4 - T_{\text{env}}^4) \times \text{circumference}
$$
$$
75.5 = 0.8 \times 5.67\times10^{-8} \times (T_s^4 - 250^4) \times 1.73
$$
$$
T_s^4 - 3.906\times10^9 = \frac{75.5}{7.848\times10^{-8}} \approx 9.62\times10^8
$$
$$
T_s^4 \approx 4.868\times10^9
$$
$$
T_s \approx 264 \, \text{K} \, (-9^\circ\text{C})
$$

Far below aluminum alloy 7075-T6 long-term working limit (~150°C). **Conductive rail heat is fully controllable.**

**(6) Recommended Conductive Rail Parameters**

| Parameter | Recommended Value | Basis |
|-----------|------------------|-------|
| Supply Voltage | 50–100 kV AC | Balance efficiency and insulation safety |
| Parallel Paths | 4 (divide full circle into four poles) | Reduce circuit resistance |
| Circuit Resistance | ≈2.08 Ω | Four-way parallel |
| Transmission Current | 1,346–2,692 A | Varies with voltage |
| Transmission Loss | 3.8–15.1 MW | Varies with voltage |
| Transmission Efficiency | 88%–97% | — |
| Conductor Temperature Rise | <30 K | Far below material limit |

> Final voltage level, insulation design (whether 20 mm UHMWPE outer layer meets local discharge requirements at 100 kV), and ground substation configuration for the conductive rail to be optimized in Volume 9 (Energy and Communication Infrastructure).

#### Ground Laser Power Transmission (100–5,000 km)

**(1) Link Equation**

$$
P_{\text{recv}} = P_{\text{emit}} \times \eta_{\text{atm}} \times \eta_{\text{opt}} \times \eta_{\text{PV}}
$$

Efficiency factors:

| Parameter | Symbol | Value | Note |
|-----------|:------:|:-----:|------|
| Atmospheric transmittance | $η_{atm}$ | 0.85 | 1.06 μm band, zenith to 5,000 km slant, MODTRAN typical [4.6] |
| Optical system efficiency | $η_{opt}$ | 0.80 | Emission telescope + tracking + beam expansion |
| PV conversion efficiency | $η_{PV}$ | 0.50 | Multi-junction GaInP/GaAs/Ge concentrator, AM0 spectrum [4.7] |

**(2) Emission Power**

Low altitude ascent power required (see 5.8.7): $P_{req} = 114.4 MW$ .

$$
P_{\text{emit}} = \frac{P_{\text{req}}}{\eta_{\text{atm}} \times \eta_{\text{opt}} \times \eta_{\text{PV}}} = \frac{114.4}{0.85 \times 0.80 \times 0.50} = \frac{114.4}{0.34} \approx 336.5 \, \text{MW}
$$

Round to **350 MW** (with safety margin).

(Note: Previous version used 650 MW due to overestimated low altitude power at 218 MW. Corrected to 114.4 MW, laser power demand greatly reduced.)

**(3) Laser Type and Scale**

| Parameter | Scheme |
|-----------|--------|
| Type | Fiber laser array (Yb-doped, λ≈1.06 μm) |
| Single fiber power | ~10 kW (current commercial)–100 kW (in development) |
| Synthesis method | Spectral + coherent combination |
| Array size | ~3,500–35,000 units |
| Footprint | ~70×70 m² (incl. cooling and beam director) |

**(4) Cabin PV Receiving Area**

PV cells directly receive laser (not sunlight), calculated by laser irradiance. Fiber laser array with adaptive optics can control far-field spot diameter to several meters. Receiving area about 3 m × 3 m = **9 m²**.

**(5) Link Power Balance**

$$
P_{\text{recv}} = 350 \times 10^6 \times 0.85 \times 0.80 \times 0.50 = 350 \times 10^6 \times 0.34 \approx 119 \, \text{MW}
$$

Slightly above cabin power demand 114.4 MW, about 4% margin. **Ground laser power transmission scheme closes.**

#### Mid Altitude On-Orbit Solar-Pumped Laser Power Transmission (5,000–14,000 km)

**(1) Power Demand**

Mid altitude power required (see 5.8.7): $P_{req} = 297.5 MW$ .

Atmospheric attenuation negligible ( $η_{atm} ≈ 1.0$ ), optical and PV efficiency as above.

$$
P_{\text{emit}} = \frac{297.5}{1.0 \times 0.80 \times 0.50} = \frac{297.5}{0.40} \approx 743.8 \, \text{MW}
$$

Round to **750 MW**.

**(2) On-Orbit Laser Electrical Power Demand**

Laser electrical-optical conversion efficiency $η_{laser} = 0.35$ (fiber laser conservative) [4.9].

$$
P_{\text{elec}} = \frac{P_{\text{emit}}}{\eta_{\text{laser}}} = \frac{750}{0.35} \approx 2,143 \, \text{MW}
$$

Round to **2,200 MW**.

**(3) On-Orbit PV Array Area**

On-orbit AM0 solar irradiance $S_0 = 1,361 W/m²$ . PV efficiency $η_{sun_{PV}} = 0.45$ (future multi-junction GaAs under AM0). Array fill factor 0.85.

$$
A_{\text{PV}} = \frac{P_{\text{elec}}}{S_0 \times \eta_{{sun_{PV}}} \times \text{FF}} = \frac{2,200\times10^6}{1,361 \times 0.45 \times 0.85} = \frac{2,200\times10^6}{520.4} \approx 4.227\times10^6 \, \text{m}^2 \approx 4.23 \, \text{km}^2
$$

6 elevators simultaneous coefficient 0.5 (average 3 of 6 at full power), actual deployment area:

$$
A_{\text{actual}} = 4.23 \times 0.5 \approx 2.12 \, \text{km}^2
$$

Distributed along ring circumference 265,458 km, average width only **8.0 m**.

**(4) Link Power Balance**

On-orbit PV output: 2,200 × 10⁶ × 0.35 (laser efficiency) × 0.80 (optical) × 0.50 (PV) = 308 MW. Slightly above mid altitude power demand 297.5 MW, about 3.5% margin. **On-orbit laser power transmission scheme closes.**

#### High Altitude On-Orbit Solar-Pumped Laser Power Transmission (14,000 km–GEO)

**(1) Power Demand**

High altitude power required (see 5.8.7): $P_{req} = 90 MW$ .

$$
P_{\text{emit}} = \frac{90}{1.0 \times 0.80 \times 0.50}
$$
$$
= \frac{90}{0.40} \approx 225 \, \text{MW}
$$

$$
P_{\text{elec}} = \frac{225}{0.35} \approx 643 \, \text{MW}
$$

PV area:

$$
A_{\text{PV}} = \frac{643\times10^6}{520.4} \approx 1.236\times10^6 \, \text{m}^2 \approx 1.24 \, \text{km}^2
$$

6 elevators simultaneous coefficient 0.5, about **0.62 km²**, average width along ring about 2.3 m.

Mid and high altitude share the same on-orbit PV array, take the larger value (mid altitude 2.12 km²) as design baseline, high altitude demand automatically met.

#### Onboard Buffer Battery

Buffer battery for short laser link interruptions (≤30 s) and peak smoothing.

Low altitude 114.4 MW, 30 s energy = 114.4×30 ≈ 3,432 MJ ≈ **0.95 MWh**.

Take **25 MWh** as design capacity (covers multiple interruptions and startup surges). Solid-state Li battery energy density 500 Wh/kg [5.3], battery mass = 25×10³/500 = **50 t**. Included in PM mass budget (see 5.10.4).

#### Power Supply Scheme Summary

| Segment | Altitude | Power Supply | Emission/Supply Power | Received Power | Efficiency |
|---------|---------|-------------|:---------------------:|:--------------:|:----------:|
| Atmosphere | 0–100 km | Conductive rail (50 kV AC, four-way parallel) | — | 114.4 MW | ~88% |
| Low Altitude | 100–5,000 km | Ground laser power | 350 MW | ~119 MW | ~34% (total link) |
| Mid Altitude | 5,000–14,000 km | On-orbit laser power | 2,200 MW (elec) | ~308 MW | ~14% (sun→elec→laser→elec) |
| High Altitude | 14,000 km–GEO | On-orbit laser power | 643 MW (elec) | ~90 MW | ~14% |
| Full Range | 0–GEO | Buffer battery | 25 MWh, 50 t | — | — |

> Final voltage level for conductive rail (whether 20 mm UHMWPE outer layer meets discharge and insulation requirements at 50 kV AC), ground substation, and on-orbit PV array detailed engineering design to be handled in Volume 9.


## 5.12 Atmospheric Effects on the Cabin

The elevator cabin in the low altitude segment (0–100 km dense atmosphere) is subject to significant aerodynamic forces. This section derives aerodynamic loads under crosswind and headwind conditions for both spindle and disc configurations, evaluating their impact on the drive system and structure.

### 5.12.1 Basic Aerodynamic Parameters

**Atmospheric Parameters** (sea level standard, worst case):

| Parameter | Symbol | Value | Unit |
|-----------|--------|-------|------|
| Air density | $ρ_{air}$ | 1.225 | kg/m³ |
| Category 10 typhoon wind speed | $v_{wind}$ | 30 (≈108 km/h) | m/s |
| Kinematic viscosity | ν | 1.5×10⁻⁵ | m²/s |

**Cabin Operation Parameters**:

| Parameter | Spindle | Disc |
|-----------|:-------:|:----:|
| Dimensions | ø5 m × 60 m | ø10 m × 10 m |
| Frontal area $A_{front}$ | π×(2.5)² ≈ 19.63 m² | π×(5)² ≈ 78.54 m² |
| Side projection area $A_{side}$ | ≈60×5 = 300 m² (conservatively 245 m²) | ≈10×10 = 100 m² |
| Drag coefficient $C_d$ (front) | 0.05 [5.2] | 0.8 |
| Side shape coefficient $C_{side}$ | 0.5 (spindle side) | 0.8 (disc side) |
| Cruise speed $v_{cruise}$ | 200 km/h = 55.56 m/s | 200 km/h = 55.56 m/s |

### 5.12.2 Crosswind Condition

Crosswind refers to wind perpendicular to the cabin's direction of travel (i.e., perpendicular to cable axis). During low-speed cruise or docking, crosswind side force may cause overturning moment.

**(1) Spindle Crosswind**

Side projection area, mid-section cylinder simplified $A_{side} ≈ 60×5×0.7 ≈ 210 m²$ (spindle taper factor 0.7), conservatively use 245 m² for check.

Side wind force:

$$
F_{\text{cross,spindle}} = \frac{1}{2} \rho_{\text{air}} v_{\text{wind}}^2 A_{\text{side}} C_{\text{side}}
$$
$$
= \frac{1}{2} \times 1.225 \times (30)^2 \times 245 \times 0.5
$$
$$
= 0.6125 \times 900 \times 122.5 \approx 6.75\times10^4 \, \text{N}
$$

Moment arm is spindle half-length (30 m), overturning moment:

$$
M_{\text{cross,spindle}} = F_{\text{cross,spindle}} \times 30 = 6.75\times10^4 \times 30 \approx 2.03\times10^6 \, N \cdotp m
$$

**(2) Disc Crosswind**

Side projection area $A_{side} ≈ 10×10 = 100 m²$ (disc as flat cylinder, windward as rectangle). Considering disc may have curved transition, conservatively use projection coefficient 0.8, effective area about 80 m².

$$
F_{\text{cross,disc}} = \frac{1}{2} \times 1.225 \times (30)^2 \times 80 \times 0.8
$$
$$
= 0.6125 \times 900 \times 64 \approx 3.53\times10^4 \, \text{N}
$$

Moment arm is disc half-height (5 m), overturning moment:

$$
M_{\text{cross,disc}} = F_{\text{cross,disc}} \times 5 = 3.53\times10^4 \times 5 \approx 1.76\times10^5 \, N \cdotp m
$$

**(3) Crosswind Condition Check**

Under Scheme C (rack), the cabin or DM's guide wheel sets clamp the track sheath's regular octagon outer surface, providing radial and lateral restraint. The 40 pairs of gears and racks also provide lateral constraint. The rack and pinion's lateral load capacity depends on tooth width and engagement depth. With 300 mm tooth width, module 20 mm, lateral allowable load per tooth is several thousand N, total for 40 pairs >10⁵ N.

Crosswind overturning moment is counteracted by the guide wheel set's restraint moment. Spindle's long moment arm (30 m) produces large overturning moment (~2.03×10⁶ N·m), requiring multiple guide wheel sets distributed along the cable axis, each providing about 10⁵ N·m (wheel diameter 0.3 m, preload 10⁴ N), distributed over 60 m length to meet requirements.

Disc's overturning moment (~1.76×10⁵ N·m) is only about 1/12 of spindle's, easier for guide wheel sets to handle.

> Under crosswind, both spindle and disc can meet stability requirements through guide wheel sets and rack and pinion lateral constraint. Detailed guide wheel arrangement and restraint moment verification to be handled in Volume 7.

### 5.12.3 Headwind Condition

Headwind refers to wind opposite to the cabin's direction of travel. During **ascent**, headwind relative speed is maximum:

$$
v_{\text{rel}} = v_{\text{cruise}} + v_{\text{wind}} = 55.56 + 30 = 85.56 \, \text{m/s} \approx 308 \, \text{km/h}
$$

This produces maximum frontal drag, directly affecting drive power demand and clamping force (Scheme B) or gear tangential force (Scheme C).

**(1) Spindle Headwind Drag**

$$
F_{\text{drag,spindle}} = \frac{1}{2} \rho_{\text{air}} v_{\text{rel}}^2 A_{\text{front}} C_d
$$
$$
= \frac{1}{2} \times 1.225 \times (85.56)^2 \times 19.63 \times 0.05
$$
$$
= 0.6125 \times 7,320.5 \times 0.9815 \approx 4,400 \, \text{N}
$$

This is only about **0.22%** of full load weight (1.962×10⁶ N).

**Impact on Scheme C (rack)**: During ascent, gears must overcome this aerodynamic drag, extra tangential force required = 4,400 N, compared to design traction force (4.12×10⁶ N, incl. safety factor) is about 0.11%, **completely negligible**.

**(2) Disc Headwind Drag**

$$
F_{\text{drag,disc}} = \frac{1}{2} \times 1.225 \times (85.56)^2 \times 78.54 \times 0.8
$$
$$
= 0.6125 \times 7,320.5 \times 62.83 \approx 2.82\times10^5 \, \text{N}
$$

This is about **14.4%** of full load weight.

**Impact on Scheme C (rack)**: Extra tangential force required about 2.82×10⁵ N, about 6.8% of design traction force, within gear design margin (tooth surface contact stress margin 1.72:1 covers this increment).

**Impact on Scheme B (friction drive, already rejected)**: If friction drive existed, this headwind drag would require extra clamping force. Extra clamping force = 2.82×10⁵/0.15 ≈ 1.88×10⁶ N, total clamping force increases from 26.1 MN to about 28.0 MN, within 2.8×10⁷ N envelope, **but Scheme B is already rejected for mechanical and thermal reasons, not implying B is feasible**.

During descent, cabin movement and gravity are in the same direction. If low altitude descent cruise is 200 km/h (55.56 m/s), with 10th-level tailwind (downward, 30 m/s), relative wind speed drops to about 25.56 m/s. Disc aerodynamic drag:

$$
F_{\text{drag,disc,tail}} = \frac{1}{2} \times 1.225 \times (25.56)^2 \times 78.54 \times 0.8 \approx 2.51 \times 10^4 \, \text{N}
$$

With 10th-level headwind (upward), relative wind speed increases to 85.56 m/s, drag about 2.82×10⁵ N.

During descent at constant speed, drive system must provide braking force $F_{\text{brake}} = W = 1.962 \times 10^6 \, \text{N}$ . Under headwind:

$$
\frac{F_{\text{drag,disc,head}}}{F_{\text{brake}}} = \frac{2.82 \times 10^5}{1.962 \times 10^6} \approx 14.4\%
$$

Under tailwind:

$$
\frac{F_{\text{drag,disc,tail}}}{F_{\text{brake}}} = \frac{2.51 \times 10^4}{1.962 \times 10^6} \approx 1.3\%
$$

Descent braking segment also needs to provide extra comfort deceleration (0.4905 m/s²), total braking force about 2.060×10⁶ N. Under headwind, aerodynamic drag contributes about 13.7%, under tailwind only about 1.2%.

Overall, disc headwind drag under certain wind directions provides some auxiliary effect for low altitude descent braking, but cannot be relied upon as the main braking method—uncontrollable meteorological conditions mean the braking system must independently meet all deceleration needs. **Aerodynamic drag assistance should be considered passive safety margin, not an active design dependency.**

**(3) Headwind Vortex-Induced Vibration Assessment**

Spindle (D=5 m, v=85.56 m/s):

$$
Re = \frac{v D}{\nu} = \frac{85.56 \times 5}{1.5\times10^{-5}} \approx 2.85\times10^7
$$

In supercritical Reynolds number range, vortex shedding irregular, weak periodic excitation.

Vortex shedding frequency (St≈0.2):

$$
f_{\text{vortex,spindle}} = \frac{0.2 \times 85.56}{5} \approx 3.42 \, \text{Hz}
$$

Disc (D=10 m):

$$
Re = \frac{85.56 \times 10}{1.5\times10^{-5}} \approx 5.70\times10^7
$$

$$
f_{\text{vortex,disc}} = \frac{0.2 \times 85.56}{10} \approx 1.71 \, \text{Hz}
$$

Cabin/DM structure fundamental frequency estimated >10 Hz (spindle slender, lower stiffness; disc higher stiffness). Vortex shedding frequencies are below structure fundamental frequency, **no resonance risk**. But disc's 1.71 Hz low-frequency excitation may couple with cabin rigid body swing mode, to be confirmed in Volume 7 modal analysis.

### 5.12.4 Tailwind Condition

During **descent**, wind and movement are in the same direction, relative wind speed decreases:

$$
v_{\text{rel,desc}} = v_{\text{cruise}} - v_{\text{wind}} = 55.56 - 30 = 25.56 \, \text{m/s}
$$

Aerodynamic drag is minimal, beneficial for drive system, not a design constraint.

Spindle tailwind drag:

$$
F_{\text{drag,spindle,tail}} = 0.6125 \times (25.56)^2 \times 19.63 \times 0.05 \approx 393 \, \text{N}
$$

Disc tailwind drag:

$$
F_{\text{drag,disc,tail}} = 0.6125 \times (25.56)^2 \times 78.54 \times 0.8 \approx 2.51\times10^4 \, \text{N}
$$

Both negligible.

### 5.12.5 Summary of Atmospheric Wind Loads on Cabin Design

| Condition | Cabin | Load Type | Magnitude | Impact on Scheme C | Impact on Scheme B (Rejected, for Reference) |
|-----------|:-----:|----------|:---------:|-------------------|---------------------------------------------|
| Crosswind (30 m/s) | Spindle | Side force/overturning moment | 6.75×10⁴ N / 2.03×10⁶ N·m | Guide wheel set restraint + gear lateral constraint sufficient | Extra clamping force ~4.5×10⁵ N needed |
| Crosswind (30 m/s) | Disc | Side force/overturning moment | 3.53×10⁴ N / 1.76×10⁵ N·m | Same as above, greater margin | Extra clamping force ~2.4×10⁵ N needed |
| Headwind (85.56 m/s) | Spindle | Frontal drag | ~4.4×10³ N (0.22% weight) | Negligible | Negligible |
| Headwind (85.56 m/s) | Disc | Frontal drag | ~2.82×10⁵ N (14.4% weight) | Extra tangential force 6.8% of design, margin covers | Extra clamping force 7.2% of original design |
| Vortex-induced vibration | Spindle | Periodic excitation | ~3.42 Hz | Below structure fundamental frequency, no resonance | — |
| Vortex-induced vibration | Disc | Periodic excitation | ~1.71 Hz | Rigid body swing mode to be confirmed | — |

**Comprehensive Conclusion**:

- Spindle cabin has excellent aerodynamic performance, headwind drag only 0.22% of weight, negligible impact on drive system; crosswind overturning moment handled by guide wheel set, long moment arm is main challenge.
- Disc cabin headwind drag is 14.4% of weight, within rack scheme margin (design margin 1.72:1 covers 6.8% extra tangential force); crosswind overturning moment is much less due to short moment arm, easier to handle.
- Scheme B (friction drive, rejected) would require extra clamping force for disc in headwind, but the base scheme is already rejected for contact stress and heat issues, only for reference.
- Vortex-induced vibration frequencies are below estimated structure fundamental frequency, no resonance risk. Disc's low-frequency component to be confirmed in later modal analysis.

> Detailed guide wheel set arrangement, rack lateral restraint moment verification, disc cabin modal analysis to be comprehensively evaluated in Volume 7 (Engineering Verification).


## 5.13 Scheme E—Multi-Index Cable Pulley Traction Scheme

Scheme E is fundamentally similar to traction elevators used in buildings. It separates load-bearing and drive functions: the main load-bearing cable only bears axial tension, the cabin is clamped to multiple index cables via pulley sets, and index cables are driven in a loop by ground and GEO end drive pulleys.

**Basic Architecture**:
- **Main Load-Bearing Cable**: A CNT braided cable bearing all self-weight tension ( $T_{GEO} ≈2.09×10^{10} N$ , see Volume 4, 4.3.3). Serves only as a guide axis, cabin slides along track sheath outer surface via guide wheels, track sheath provides radial and lateral restraint. No extra drive interface (no rack) on main cable.
- **Index Cables**: Multiple thinner CNT braided cables, also extending from ground to GEO. Index cables form a closed loop via drive pulleys at ground and GEO ends, driven by motors. Each index cable operates independently, single cable failure does not affect overall system. Index cables loop by passing over GEO end return pulleys, with drive pulleys at both ends providing tension and motion.
- **Cabin Interface**: Cabin equipped with multiple pulley sets clamped to index cables. When index cables are driven, the cabin moves up/down accordingly. Pulley sets on the cabin maintain constant clamping force via spring preload or hydraulic devices.

This scheme centralizes all heavy drive equipment (motors, brakes, heat dissipation) at ground and GEO stations, greatly reducing cabin self-weight. Index cables can be designed redundantly, single cable failure does not affect overall system.

#### (1) Core Contradiction: Uniform Cross-Section Looping and Self-Weight Tension

Index cables must loop from ground to GEO. Unlike the main load-bearing cable's static suspension, index cables are constantly moving—current high-altitude segment will later move to low altitude, and vice versa. Therefore, index cables must be of uniform cross-section—same diameter throughout, to pass through fixed-size drive and return pulleys. If a tapered cross-section is used (different diameters at ground and GEO), the same cable segment would have changing diameter as it passes through pulleys, which have fixed groove sizes—this is a geometric contradiction, unsolvable by pulley design.

Uniform cross-section means the cable at the ground end bears the maximum self-weight tension of the entire length, cannot be optimized by tapering.

For a cable of length L, cross-section A, uniform flexible cable suspended from GEO, self-weight tension at any height T(z) equals the cumulative weight of all cable below:

$$
T(z) = \int_z^{L} \rho_{\text{eng}} A g(z') \mathrm{d}z'
$$

Where L = 42,164 km, $ρ_{\text{eng}} = 390 kg/m³$ (see Volume 4, 4.2), g(z') is local gravity. At ground (z = 0), tension is maximum. Using gravitational potential difference, self-weight tension:

$$
T_{\text{self,max}} = \rho_{\text{eng}} A \int_0^{L} g(z) \mathrm{d}z = \rho_{\text{eng}} A \times GM_e \left( \frac{1}{R_e} - \frac{1}{R_{GEO}} \right)
$$

Substitute values: $GM_e = 3.986×10^{14} m³/s², R_e = 6.371×10⁶ m, R_{GEO} = 4.2164×10⁷ m$ .

$$
\int_0^{L} g(z) \mathrm{d}z = 3.986\times10^{14} \times \left( \frac{1}{6.371\times10^6} - \frac{1}{4.2164\times10^7} \right)
$$
$$
= 3.986\times10^{14} \times (1.5696\times10^{-7} - 2.3717\times10^{-8})
$$
$$
= 3.986\times10^{14} \times 1.3324\times10^{-7} \approx 5.311\times10^7 \, \text{J/kg}
$$

This integral is the gravitational potential energy difference per unit mass, i.e., the energy required to lift 1 kg from ground to GEO. Equivalent integral height:

$$
H_{\text{eq}} = \frac{1}{g_0} \int_0^{L} g(z) \mathrm{d}z = \frac{5.311\times10^7}{9.81} \approx 5.41\times10^6 \, \text{m}
$$

(Note: This $H_{eq}≈5,410 km$ differs from the main cable characteristic height $H≈2,091 km$ in Volume 4. The former is gravitational potential difference divided by surface gravity, used for uniform cross-section self-weight tension; the latter is the characteristic length for tapered cross-section, with different physical meaning.)

Self-weight stress:

$$
\sigma_{\text{self}} = \frac{T_{\text{self,max}}}{A} = \rho_{\text{eng}} g_0 H_{\text{eq}} = 390 \times 9.81 \times 5.41\times10^6 \approx 2.070\times10^{10} \, \text{Pa} = 20.70 \, \text{GPa}
$$

Strength condition requires self-weight stress not to exceed allowable stress:

$$
\sigma_{\text{self}} \leq \frac{\sigma_{\text{allow}}}{S}
$$

Where $σ_{allow} = 20 GPa$ (target, see Volume 2, 2.3.4), S = 2.5 (safety factor, see Volume 2, 2.7.1).

$$
\sigma_{\text{self}} = 20.70 \, \text{GPa} > \frac{20}{2.5} = 8.00 \, \text{GPa}
$$

**Self-weight stress exceeds allowable by about 2.6x. Under pure self-weight, uniform cross-section CNT cable cannot survive safely.**

Even at theoretical strength limit (no safety factor):

$$
\sigma_{\text{self}} = 20.70 \, \text{GPa} > 20 \, \text{GPa}
$$

Self-weight stress already exceeds CNT target engineering strength, cable would break before bearing any cabin load. Solutions: (1) Increase CNT engineering strength above 20.7 GPa (current lab max ~14 GPa [5.4], 48% shortfall); (2) Abandon uniform cross-section looping. The difficulty and timeline of material breakthrough means Scheme E is currently infeasible.

#### (2) Number of Index Cables and Lateral Stability Analysis

During operation, the cabin is subject to lateral wind-induced overturning moment. Index cables must provide sufficient restoring moment for lateral stability.

**Spindle Cabin (ø5 m × 60 m) Crosswind Condition** (Category 10 typhoon 30 m/s, see 5.12.2):

Lateral wind force about 6.75×10⁴ N, overturning moment $M_{wind} ≈ 2.03×10⁶ N \cdotp m$ .

Restoring moment from leeward index cables' tension increment. Let number of index cables n, each cable's attachment point evenly distributed around circumference. Full load 200 t, total weight W=1.962×10⁶ N, each index cable bears W/n. Cabin is pulled by ground/GEO motors via index cables, index cable rated tension $F_{single} = W \cdotp S / n$ , S=2.0 (includes friction loss and startup shock).

For n=6 (3 leeward cables, single cable ~6.54×10⁵ N), moment arm spindle radius ~2.5 m (attachment at cabin outer wall):

$$
F_{\text{single}} = \frac{1.962\times10^6 \times 2.0}{6} \approx 6.54\times10^5 \, \text{N}
$$
$$
M_{\text{restore,max}} \approx 3 \times (0.2 \times 6.54\times10^5) \times 2.5 \approx 9.81\times10^5 \, N \cdotp m
$$

$M_{restore} < M_{wind}$ (9.81×10⁵ < 2.03×10⁶), not sufficient. Increase to 10 cables (5 leeward, single cable ~3.92×10⁵ N):

$$
M_{\text{restore,max}} \approx 5 \times (0.2 \times 3.92\times10^5) \times 2.5 \approx 9.80\times10^5 \, N \cdotp m
$$

Still not sufficient. Spindle's long moment arm (30 m) causes huge overturning moment, hard to restore with index cable tension increment alone.

**Disc Cabin (ø10 m × 10 m) Crosswind Condition**:

Lateral wind force about 3.53×10⁴ N, overturning moment $M_{wind} ≈ 1.76×10⁵ N \cdotp m$ (see 5.12.2).

n=8 (4 leeward cables, single cable ~4.91×10⁵ N), moment arm disc radius 5 m:

$$
F_{\text{single}} = \frac{1.962\times10^6 \times 2.0}{8} \approx 4.905\times10^5 \, \text{N}
$$
$$
M_{\text{restore,max}} \approx 4 \times (0.2 \times 4.905\times10^5) \times 5 \approx 1.962\times10^6 \, N \cdotp m
$$

$M_{restore} > M_{wind}$ (1.962×10⁶ >> 1.76×10⁵), **disc with 8 index cables meets lateral stability with large margin (~11x)**.

| Cabin Shape | Min Index Cables | Wind Overturning Moment (N·m) | Restoring Moment (N·m) | Judgment |
|-------------|:---------------:|:-----------------------------:|:----------------------:|:--------:|
| Spindle | Not sufficient (even 10) | ~2.03×10⁶ | ~9.80×10⁵ (10 cables) | Not feasible |
| Disc | 8 | ~1.76×10⁵ | ~1.96×10⁶ | Pass (margin ~11x) |

Scheme E is naturally suited to disc cabins (short moment arm, small overturning moment), but hard to meet for spindle (long moment arm, large overturning moment). This complements Scheme C where spindle excels in aerodynamics but disc excels in lateral stability.

#### (3) Index Cable Diameter Design

Index cables are flexible (CNT braided), diameter determined by **pure self-weight** (controlling case). As in (1), even without any cabin load, uniform cross-section CNT cable self-weight stress is 20.70 GPa, exceeding allowable 8.00 GPa by 2.6x. This means, at current CNT engineering strength (20 GPa target), any cross-section uniform cable cannot survive—self-weight stress is independent of area, only depends on material specific strength.

**Therefore, Scheme E's index cable diameter cannot be meaningfully recommended in this volume.** Feasibility depends entirely on whether Volume 2's material development can raise CNT engineering strength above 20.7 GPa (about 48% increase, current lab max ~14 GPa), and meet safety factor requirements.

> As self-weight stress exceeds allowable by 2.6x, further detailed design (bending fatigue, drive pulley parameters, heat dissipation, etc.) for Scheme E is not pursued here. Only comparison with Schemes A–D and long-term positioning is retained.

#### (4) Kinematic Features of Scheme E

If material bottleneck is solved, Scheme E's kinematics are determined by ground/GEO drive pulley linear speed. Drive pulleys can run at variable speed, upper limit constrained by:

- CNT index cable bending stress at return pulleys ( $D_{pulley}/D_{cable} ≥ 40$ )
- Drive motor power and heat dissipation
- Cabin stable operation on guide track

These constraints are similar to Scheme C rack, theoretically can reach similar cruise speed (1,500 km/h). Not elaborated here.

#### (5) Comparison with Schemes A–D

| Dimension | Scheme B (Friction) | Scheme C (Rack) | Scheme E (Index Cable) |
|-----------|:-------------------:|:---------------:|:----------------------:|
| Main Cable Wear | High (direct drive wheel contact) | None (guide only, rack in mid-layer) | **Very low (guide only, index cable independent)** |
| Drive Equipment Location | On cabin | On cabin (DM separable) | **Ground + GEO centralized** |
| Cabin Self-Weight | High | High (lower after DM separation) | **Low (only pulley set + guide wheels)** |
| Low Altitude Heat Issue | Severe (rejected) | Controllable (rack), mid altitude still to be solved | **Centralized at drive station, controllable** |
| System Complexity | Medium | High (rack manufacturing, 40 gear pairs sync) | **High (multi-cable sync control, closed loop operation)** |
| Redundancy/Safety | Medium | Medium | **High (multi-cable independent redundancy)** |
| Core Tech Bottleneck | UHMWPE contact stress + heat | Rack wear life, mid altitude heat | **CNT strength must reach 20.7 GPa (self-weight exceeds by 2.6x)** |
| Current Feasibility | Rejected | Feasible in principle (low altitude 200 km/h) | **Long-term, depends on material breakthrough** |

#### (6) Conclusion

Scheme E, by moving drive system to ground and GEO, has unique advantages (centralized drive, lightweight cabin, cable redundancy), but feasibility is fundamentally limited by uniform cross-section CNT cable self-weight stress—exceeds allowable by about 2.6x, any cross-section cannot survive at current CNT engineering strength. **Scheme E is currently infeasible; its viability depends on whether Volume 2's material development (pending verification V2-M1 to V2-M3) can raise CNT engineering strength above 20.7 GPa, with required safety factor.** Scheme E is recorded as a long-term alternative.

## 5.14 Electromagnetic Drive Concept (Long-Term Alternative)

This section explores the long-term concept of replacing rack drive with linear synchronous motor (LSM) in the high altitude segment (14,000 km–GEO, 28,164 km). This is not included in the current design baseline, only as an upgrade direction after technological breakthroughs.

### 5.14.1 Basic Principle

LSM replaces the rack with electromagnetic coils (primary windings) along the cable, with permanent magnet arrays (secondary) on the cabin or DM. Energized coils create a traveling magnetic field, permanent magnets are driven by Lorentz force for non-contact operation. Unlike rack, drive force is transmitted via electromagnetic field, eliminating mechanical wear and interface resonance limits.

### 5.14.2 Traction Force Requirement

LSM must provide required traction for cabin acceleration near GEO. For full load 200 t at GEO, comfort acceleration $a_{comfort} =0.4905 m/s²$ :

$$
F_{\text{traction}} = m a_{\text{comfort}} = 2\times10^5 \times 0.4905 \approx 9.81\times10^4 \, \text{N}
$$

(GEO gravity only 0.224 m/s², much less than comfort acceleration, traction mainly for inertia.)

For more severe low altitude acceleration (near ground, must overcome gravity and provide acceleration), traction is 2.060×10⁶ N (see 5.8.7), but LSM concept is mainly for high altitude, where gravity is much less, so GEO case is design baseline.

### 5.14.3 Lorentz Force and Conductor Requirement

LSM air gap permanent magnet flux density B = 1 T (current high-performance NdFeB magnets). Primary winding current density J = 5 A/mm² (copper, short-term, active cooling).

Unit length conductor Lorentz force:

$$
f = B I = B \times (J A_{\text{conductor}})
$$

Single conductor area $A_{conductor} = 10⁻³ m²$ (1000 mm²), current $I = 5×10³ A$ , unit length force $f = 5×10³ N/m$ .

To generate required traction 9.81×10⁴ N, number of conductors (parallel):

$$
N_{\text{conductor}} = \frac{F_{\text{traction}}}{f} = \frac{9.81\times10^4}{5\times10^3} \approx 20
$$

Each conductor area 1000 mm², 20 in parallel total area about 2×10⁻² m². For three-phase LSM, each phase needs this area, total about 6×10⁻² m².

### 5.14.4 Conductor Mass Estimate

20 parallel copper conductors (1000 mm² each), copper density $ρ_{Cu} = 8,960 kg/m³$ . Along high altitude 28,164 km (2.8164×10⁷ m):

$$
m_{\text{conductor}} = \rho_{\text{Cu}} \times N_{\text{conductor}} \times A_{\text{conductor}} \times L
$$
$$
= 8,960 \times 20 \times 10^{-3} \times 2.8164\times10^7
$$
$$
= 8,960 \times 2\times10^{-2} \times 2.8164\times10^7
$$
$$
= 8,960 \times 5.6328\times10^5 \approx 5.047\times10^9 \, \text{kg} \approx 5.05\times10^6 \, \text{t}
$$

**Just the copper conductor mass for the high altitude segment exceeds 5 million tons**, not including insulation (about 10%–15% of conductor mass), coil support structure (about 50%–100% of conductor mass), and cooling pipes. Including three-phase windings and redundancy, total mass could reach **tens of millions of tons**. Even with aluminum (density 2,700 kg/m³), mass is about 1.5 million tons—hundreds of times the total mass of all current spacecraft.

**Such mass is completely infeasible with current and foreseeable space transport capacity.**

### 5.14.5 Ohmic Loss and Superconductivity Necessity

Copper resistivity $ρ_{Cu} = 1.68×10⁻⁸ Ω·m$ (20°C). 20 parallel, each 28,164 km, single conductor resistance:

$$
R_{\text{single}} = \rho_{\text{Cu}} \frac{L}{A_{\text{conductor}}} = \frac{1.68\times10^{-8} \times 2.8164\times10^7}{10^{-3}} \approx 473 \, \Omega
$$

20 parallel total resistance $R_{parallel} ≈ 23.7 Ω$ . Single phase current $I_{phase} = 20 × 5,000 = 1×10⁵ A$ , ohmic loss:

$$
P_{\text{loss}} = I_{\text{phase}}^2 R_{\text{parallel}} = (10^5)^2 \times 23.7 \approx 2.37\times10^{11} \, \text{W} \approx 237 \, \text{GW}
$$

This is equivalent to about 120 large nuclear power plants, far beyond any space power engineering feasibility, and heat must be radiated to deep space—corresponding radiator area (400 K panel):

$$
A_{\text{radiator}} = \frac{P_{\text{loss}}}{\varepsilon \sigma T^4} = \frac{2.37\times10^{11}}{0.85 \times 5.67\times10^{-8} \times 400^4} \approx 1.93\times10^8 \, \text{m}^2 \approx 193 \, \text{km}^2
$$

**Therefore, LSM implementation must rely on superconducting conductors**—zero DC resistance, eliminating ohmic loss. Current high-temperature superconducting tape (e.g., YBCO, critical temp ~92 K, engineering current density up to 10⁸ A/m²) is the technical route, but 28,164 km continuous superconducting wire manufacturing, deployment, and in-orbit cryogenic maintenance (active cooling below liquid nitrogen) are huge engineering challenges.

### 5.14.6 Segmented Power Supply and Control

LSM must be powered in segments—only the segment where the cabin is located and adjacent segments are energized, others are off to reduce loss (even with superconductivity, coil switching loss and control circuit power must be managed).

Cabin speed 1,500 km/h = 416.67 m/s. If each segment is 1 km, cabin passes a segment in about 2.4 seconds. Segmented power switching must be **millisecond-level**, and real-time cabin position must be obtained—position error must be less than segment length (<100 m).

Required position sensing accuracy and switch response exceed current spacecraft navigation and control, but in principle can be achieved by distributed fiber optic sensors (e.g., Brillouin scattering distributed strain/temperature) along the cable, with cabin laser reflectors. Engineering implementation needs at least 10–15 years of R&D.

### 5.14.7 Advantages and Timeline

**Advantages** (once realized):

- **No rack speed limit**: Electromagnetic drive has no mechanical engagement, not limited by interface resonance or engagement shock. In theory, high altitude segment time can be reduced from rack limit 18.90 h to ideal pure acceleration/deceleration 3.05 h (see 5.5.2)—saving about 16 h per trip.
- **No contact wear**: Cabin and cable coupled only by electromagnetic force, no rack or gear, eliminating mechanical wear and lubrication issues.
- **Efficient regenerative braking**: LSM can seamlessly switch to generator mode, descent braking energy can be directly fed back to cable coils or GEO storage, more efficient than mechanical braking.

**Timeline**: LSM realization depends on these key breakthroughs:

| Technology | Current Status | Expected Maturity |
|------------|---------------|:----------------:|
| Superconducting wire (HTS tape, YBCO) | km-scale samples made, 10,000 km continuous and cryogenic maintenance to be developed | ~2040 |
| Millisecond-level segmented power switching | Ground maglev (e.g., Japan's L0) has engineering practice, but no space-scale precedent | ~2040 |
| Distributed fiber optic position sensors | Mature for ground pipelines, space deployment needs verification | ~2035 |

**Conclusion**: LSM electromagnetic drive is a long-term upgrade for rack scheme; once superconducting wire and segmented power control mature, high altitude segment time can be reduced to ~3 h (saving 16 h). But due to high dependence on superconducting wire and large-scale space deployment, as of 2026, it is still at concept research stage, not a recommended scheme. Estimated engineering evaluation possible after ~2045.

### 5.14.8 Synergy with Scheme C

Scheme C (rack) currently solves the drive method, with 1,500 km/h limit set by interface resonance (see 5.5.3). After LSM breakthrough, low/mid altitude rack (0–14,000 km, atmosphere and transition still need mechanical engagement reliability) can be retained, with high altitude (14,000 km–GEO) replaced by LSM—forming a "low altitude rack + high altitude electromagnetic" relay drive. Existing rack investment is not wasted, but remains as reliable backup and main drive for low altitude.

## 5.15 Summary of Pending Verification Items

**Top Priority Key Technology Items** (to be scheduled for experimental verification in next project phase):

| No. | Item | Responsible Volume |
|-----|------|:-----------------:|
| V5-P0 | Ultra-long-life aluminum alloy micro-arc oxidation coating friction/wear life in simulated low altitude environment | Volume 7 |
| V5-P1 | High-power space radiation heat dissipation in mid altitude (active liquid cooling + deployable large radiator panels) | Volume 7 |

**Regular Pending Items**:

| No. | Item | Responsible Volume |
|-----|------|:-----------------:|
| V5-N1 | Aluminum alloy rack micro-arc oxide layer 10⁷ cycle contact fatigue limit | Volume 7 |
| V5-N2 | Aluminum gear-rack dry inert gas annual wear depth | Volume 7 |
| V5-N3 | 40 gear pairs synchronous drive load balancing and fault isolation | Volume 7 |
| V5-N4 | DM deployable radiator panel vacuum deployment and heat dissipation performance | Volume 7 |
| V5-N5 | Low altitude sealed dry inert gas protection effectiveness | Volume 7 |
| V5-N6 | C/SiC tapered transition segment fatigue (5.23×10¹⁰ N) | Volume 7 |
| V5-N7 | Spindle cabin vertical wind tunnel test | Volume 7 |
| V5-N8 | Mid altitude high-power heat dissipation (~20.8 MW) active liquid cooling verification | Volume 7 |
| V5-N9 | High altitude 6.3 MW radiator panel design and verification | Volume 7 |
| V5-N24 | GEO end heat pipe network and radiator combined efficiency | Volume 7 |
| V5-N25 | Index cable low altitude crosswind vortex-induced vibration and anti-tangling | Volume 7 |
| V5-N26 | Multi-index cable synchronous tension control system long-term reliability | Volume 7 |
| V5-N27 | CNT braided cable tension-bending coupled fatigue life | Volume 7 |


## 5.16 Parameter Output

| Parameter | Value | Status |
|-----------|-------|--------|
| Spindle Dimensions | ø5 m × 60 m | Locked |
| Disc Dimensions | ø10 m × 10 m | Locked |
| DM Dimensions | ø4.0 m × 10.0 m | Locked |
| DM/PM Mass | ≈49.3 t / ≈69.4 t | Locked |
| Rack Parameters | Aluminum 7075-T6 micro-arc oxidation, module 20 mm, tooth width 300 mm, 40 pairs | Locked |
| Contact/Bending Stress | ~116 MPa / ~55 MPa | Margin 1.72 / 1.04 |
| Low Altitude Cruise Speed | 200 km/h (safe) / 1,500 km/h (heat pending) | — |
| One-Way Time (200 low) | Ascent/descent ≈50 h | Locked |
| One-Way Time (full speed) | Ascent/descent ≈28.4 h | Reference |
| Rocket Drive | **Rejected** | Judgment |
| Scheme A/B | **Rejected** | Judgment |
| Scheme C | **Feasible in principle** | Judgment |
| Scheme E | **Long-term alternative** | Judgment |
| Pure Onboard Battery | **Rejected** | Judgment |


## 5.17 Volume 5 Conclusion

This volume completes the full-chain engineering demonstration of cabin configuration, all drive schemes' full ascent/descent derivations, power supply system, and full-range kinematics.

1. **Rocket-driven cabin is infeasible** (Δv requirement ~19 km/s, chemical rocket mass ratio >74x).
2. **Scheme A** (contact stress ~600 MPa) and **Scheme B** (UHMWPE contact stress ~78 MPa + heat exceeds by 38x) are both rejected.
3. **Scheme C** (aluminum rack 40 pairs + drive separation DM+PM) passes mechanical checks, 200 km/h low altitude heat is controllable. Gravity decreases with altitude, reducing mid altitude power to 297.5 MW (not previous 858 MW), greatly improving thermal management feasibility. One-way about 50 h (200 km/h low) or about 28 h (full speed). **Entire segment limited by rack speed 1,500 km/h, which determines the basic running time.**
4. **Scheme E**'s core issue is CNT strength bottleneck (self-weight stress exceeds allowable by 2.6x), currently a long-term alternative.
5. **Pure onboard battery scheme is physically infeasible** (specific energy 31,900 Wh/kg required), external power supply is the only path.

Parameters output in this volume can support on-orbit construction in Volume 6 and integrated physical demonstration in Volume 7.


## References (Index Table)

[5.1] NASA-STD-3001, Vol.2: Human Factors, Habitability, and Environmental Health, 2019.
[5.2] S.F. Hoerner, *Fluid-Dynamic Drag*, 2nd ed., 1965.
[5.3] Battery Energy Density Status and Forecast, NREL Battery Cost and Performance Database, 2025.
[5.4] Zhang, X., Bai, Y., et al., *Science* 384:1318–1323, 2024.
[5.5] NASA/TM-2010-216249, C/SiC Mechanical Properties.
[5.6] SAE AMS 5662M, 2019, Inconel 718 Bolt Allowable Stress.
[5.7] S.M. Kurtz, *UHMWPE Biomaterials Handbook*, 3rd ed., William Andrew, 2015.
[5.8] ASM Handbook, Vol.2: Properties and Selection: Nonferrous Alloys and Special-Purpose Materials, 1990, Aluminum Alloy 7075-T6 Mechanical Properties and Fatigue Data.


## Terminology Table

| Abbreviation | Chinese Name |
|--------------|-------------|
| CNT | Carbon Nanotube |
| GEO | Geosynchronous Orbit |
| UHMWPE | Ultra-High Molecular Weight Polyethylene |
| C/SiC | Silicon Carbide Fiber Reinforced Composite |
| PMSM | Permanent Magnet Synchronous Motor |
| LSM | Linear Synchronous Motor |
| DM | Drive Module |
| PM | Payload Module (Cabin) |
| NaK | Sodium-Potassium Alloy (liquid metal working fluid) |
| CFRP | Carbon Fiber Reinforced Polymer |

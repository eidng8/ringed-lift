# Volume VI: Circumferential Structure Construction and On-Orbit Assembly

**Version**: 3.2<br/>
**Compilation Date**: May 2026<br/>
**Currency Unit**: Renminbi (Yuan), symbol: ¥<br/>


## 6.1 Preface

This volume focuses on the core construction phase of the Space Ringed-Elevation project—how to manufacture segments of a closed-loop cable with a total length of approximately 265,000 km at the outer edge of the 42,264 km geosynchronous orbit, launch them into orbit, and use automated on-orbit systems to complete braiding, connection, and tensioning, ultimately forming a complete circumferential main structure.

This volume follows on from:
- **Volume I**: Orbital mechanics environment (perturbations, modes, thruster requirements)
- **Volume II**: Material parameters (CNT strength, lunar manufacturing schemes)
- **Volume III**: Six-point anchoring scheme
- **Volume IV**: Elevator cable cross-section design (tapered, cross-section ratio 13.31:1), sheath parameters, rack scheme, preliminary counterweight design
- **Volume V**: Car drive scheme (Scheme C rack drive + DM separation, full-section aluminum alloy rack)

Core tasks of this volume:

1. Clarify the structural states of the ring and elevator cables during construction.
2. Through rigorous mechanical derivation, assess the ring’s ability to share tension after closure and determine the final counterweight scheme.
3. Determine the segmentation strategy, transportation requirements, and on-orbit construction plan for the circumferential cable.
4. Design the configuration and process of the space spider robot.
5. Develop the braiding and inter-segment connection process and strength verification.
6. Plan the construction sequence and timing simulation to ensure ring symmetry and structural stability during construction.
7. Analyze major risks during construction and provide contingency plans.
8. Output key parameters for use in Volume VII verification and Volume VIII logistics planning.


## 6.2 Elevator Cable State During Construction

### 6.2.1 Definition of Independent Condition

During ring construction (before all cable segments are in place and form a complete closed loop), the GEO end of the elevator cable is in a **freely suspended state**. At this time, the ring cannot provide any geometric or mechanical constraint. Each of the six elevator cables is independent, and the entire tension at the GEO end must be borne independently by its own counterweight system.

This condition is defined as the "independent condition" in Section 4.2.2 of Volume IV, with a safety factor S ≥ 2.5. This volume explicitly defines it as the actual working state during construction.

### 6.2.2 GEO End Force Under Independent Condition

From Section 4.2.2 of Volume IV, under the independent condition, the maximum tension at the GEO end of the elevator cable is:

$$
T_{\text{GEO}} = \frac{\sigma_{\text{allow}} A_{\text{GEO}}}{S} = \frac{20 \times 10^9 \times 2.613}{2.5} \approx 2.09 \times 10^{10} \, \text{N}
$$

Where $A_{GEO} ≈ 2.613 m²$ is the cross-sectional area at the GEO end (Section 4.3.3 of Volume IV), $σ_{allow} = 20 GPa$ is the engineering strength target value for the CNT braided cable (Section 2.3.4 of Volume II).

This tension must be fully borne by the GEO end counterweight system.

### 6.2.3 Counterweight Scheme Under Independent Condition

The counterweight is located Δh = 200 km above GEO, with a counterweight orbital radius:

$$
R_{\text{counterweight}} = R_{\text{GEO}} + \Delta h = 42,164 + 200 = 42,364 \, \text{km} = 4.2364 \times 10^7 \, \text{m}
$$

Centrifugal and gravitational acceleration at the counterweight:

$$
a_c = \omega_e^2 R_{\text{counterweight}} = (7.2921 \times 10^{-5})^2 \times 4.2364 \times 10^7
$$
$$
\omega_e^2 = 5.3171 \times 10^{-9} \, \text{s}^{-2}
$$
$$
a_c = 5.3171 \times 10^{-9} \times 4.2364 \times 10^7 \approx 0.22525 \, \text{m/s}^2
$$

$$
a_g = \frac{GM_e}{R_{\text{counterweight}}^2} = \frac{3.986 \times 10^{14}}{(4.2364 \times 10^7)^2} = \frac{3.986 \times 10^{14}}{1.7947 \times 10^{15}} \approx 0.22210 \, \text{m/s}^2
$$

Net acceleration:

$$
\Delta a = a_c - a_g = 0.22525 - 0.22210 = 0.00315 \, \text{m/s}^2
$$

Required counterweight mass (excluding safety factor):

$$
M_{\text{counterweight}} = \frac{T_{\text{GEO}}}{\Delta a} = \frac{2.090 \times 10^{10}}{0.00315} \approx 6.635 \times 10^{12} \, \text{kg}
$$

With a safety factor of 1.2 (covering counterweight orbital control error and cable self-weight from GEO to counterweight), the designed counterweight mass:

$$
M_{\text{counterweight,design}} = 6.635 \times 10^{12} \times 1.2 \approx 7.96 \times 10^{12} \, \text{kg} \approx 8.0 \times 10^{12} \, \text{kg}
$$

Capturing 2–3 C-type asteroids with a diameter of about 1.5 km each will suffice (single mass about 3.5 × 10¹² kg, see Section 2.5.6 of Volume II).


## 6.3 Reassessment of the Counterweight System After Ring Closure

### 6.3.1 Problem Statement

After the ring is closed, the GEO ends of the six elevators are mechanically connected to the ring main body via C/SiC connectors (Section 4.7 of Volume IV). The natural question is: can the circumferential tension of the ring share the GEO end tension of the elevator cables, thereby reducing the counterweight mass? This section answers this question through rigorous mechanical analysis.

### 6.3.2 Static Equilibrium Tension of the Ring

The design linear density of the ring in the full-cable state is λ = 300 kg/m (Section 4.3 of Volume IV, d = 0.7 m, fill factor 0.6).

From Section 1.3.1 of Volume I, the circumferential tension of the ring in static equilibrium without perturbation is:

$$
T_{\text{ring}} = \frac{GM_e \lambda}{R_0}
$$

Substituting values: GMₑ = 3.986 × 10¹⁴ m³/s², λ = 300 kg/m, R₀ = 42,264 km = 4.2264 × 10⁷ m.

$$
T_{\text{ring}} = \frac{3.986 \times 10^{14} \times 300}{4.2264 \times 10^7} = \frac{1.1958 \times 10^{17}}{4.2264 \times 10^7} \approx 2.83 \times 10^9 \, \text{N}
$$

Comparing this value with the GEO end tension of a single elevator cable:

$$
\frac{T_{\text{GEO}}}{T_{\text{ring}}} = \frac{2.09 \times 10^{10}}{2.83 \times 10^9} \approx 7.39
$$

**The GEO end tension of a single elevator cable is about 7.4 times the total circumferential tension of the full-cable ring.** In other words, the ring’s circumferential tension is far from sufficient to balance the radial pull of the elevator cable. When all six elevators act simultaneously, the total pull = 6 × 2.09 × 10¹⁰ ≈ 1.254 × 10¹¹ N, about 44 times the ring’s circumferential tension.

### 6.3.3 Mechanical Response of the Ring Under Radial Concentrated Force

The effect of the elevator cable on the ring is essentially the application of a radial outward concentrated force F ( $F = T_{GEO} ≈ 2.09 × 10¹⁰ N$ ). The deformation and bearing capacity of the ring under this force depend on its bending stiffness and circumferential tension. The following evaluates two extreme models.

**(1) Considering Only Circumferential Tension (No Bending Stiffness Model)**

The ring is approximated as a flexible cable that can only bear tension (ignoring bending stiffness EI). Under the action of a radial concentrated force F, the ring forms a kink angle 2θ on both sides of the loading point. By force balance at the loading point (F upward, two cable tensions $T_{ring}$ each at angle θ to the horizontal):

$$
F = 2 T_{\text{ring}} \sin\theta
$$

Under the small deformation assumption after construction (θ ≪ 1), $\sin\theta \approx \theta$ :

$$
F \approx 2 T_{\text{ring}} \theta \quad \Rightarrow \quad \theta \approx \frac{F}{2 T_{\text{ring}}}
$$

The radial displacement δ at the loading point and the kink angle relationship (ring geometry):

With constant arc length, the relationship between radial displacement δ and θ is:

$$
\delta = R_0 \left(1 - \cos\left(\frac{\theta}{2}\right)\right) \approx R_0 \frac{\theta^2}{8}
$$

Eliminating θ, the force-displacement relationship is:

$$
\delta = \frac{R_0}{8} \cdot \left(\frac{F}{2 T_{\text{ring}}}\right)^2 = \frac{R_0 F^2}{32 T_{\text{ring}}^2}
$$

Substituting values:

$$
\delta = \frac{4.2264 \times 10^7 \times (2.09 \times 10^{10})^2}{32 \times (2.83 \times 10^9)^2}
$$
$$
= \frac{4.2264 \times 10^7 \times 4.3681 \times 10^{20}}{32 \times 8.0089 \times 10^{18}}
$$
$$
= \frac{1.846 \times 10^{28}}{2.563 \times 10^{20}}
$$
$$
\approx 7.20 \times 10^7 \, \text{m} = 72,000 \, \text{km}
$$

The required radial displacement is about 72,000 km, far exceeding the ring radius of 42,264 km. This result shows that under the small deformation assumption, $θ ≈ F/(2T_{ring}) ≈ (2.09 × 10¹⁰)/(5.66 × 10⁹) ≈ 3.69 rad$ , much greater than 1, so the small deformation assumption itself is invalid. This means **the ring will be completely straightened, forming a sharp kink, and cannot provide effective radial support.**

**Physical conclusion: relying solely on circumferential tension, the ring cannot balance the outward pull of a single elevator cable.**

**(2) Including Bending Stiffness (Elastic Ring Model)**

Ring cross-section diameter d = 0.7 m, cross-sectional moment of inertia:

$$
I = \frac{\pi d^4}{64} = \frac{\pi \times (0.7)^4}{64}
$$
$$
= \frac{\pi \times 0.2401}{64} \approx 0.0118 \, \text{m}^4
$$

CNT braided cable elastic modulus E ≈ 1,000 GPa = 1 × 10¹² Pa (Section 4.7.2 of Volume IV). Bending stiffness:

$$
EI \approx 1 \times 10^{12} \times 0.0118 \approx 1.18 \times 10^{10} \, N \cdotp m^2
$$

For the maximum radial displacement of an elastic ring under a radial concentrated force F (ignoring circumferential tension, pure bending solution), the radial displacement at the loading point is approximately:

$$
\delta_{\text{max}} \approx \frac{F R_0^3}{3\pi EI}
$$

Substituting values:

$$
\delta_{\text{max}} \approx \frac{2.09 \times 10^{10} \times (4.2264 \times 10^7)^3}{3\pi \times 1.18 \times 10^{10}}
$$
$$
= \frac{2.09 \times 10^{10} \times 7.55 \times 10^{22}}{1.112 \times 10^{11}}
$$
$$
= \frac{1.578 \times 10^{33}}{1.112 \times 10^{11}}
$$
$$
\approx 1.42 \times 10^{22} \, \text{m}
$$

This is a physically meaningless huge value—far exceeding the scale of the ring, the GEO orbital radius, and the Earth-Moon distance. The fundamental reason is: the ring’s slenderness ratio (circumference/cross-section diameter) ≈ 2.65 × 10⁸ m / 0.7 m ≈ 3.8 × 10⁸, so the bending stiffness is extremely small relative to its geometric scale. At this slenderness ratio, any concentrated force can easily straighten the ring.

**Physical conclusion: the ring’s bending stiffness is negligible in the face of the concentrated pull of the elevator cable and cannot provide support at all.**

### 6.3.4 Physical Conclusion

Analysis of both extreme models (pure tension, pure bending) leads to the same conclusion: **the ring cannot provide any effective support under the radial concentrated force of the elevator cable. After closure, the counterweight mass cannot be reduced due to the presence of the ring. The GEO end tension of the elevator cable must continue to be borne independently by each counterweight.**

This conclusion applies to any cross-section diameter, including larger cross-section designs beyond the 0.5–1.0 m range. As long as the allowable axial stress of the cable is fixed, the ring’s bearing capacity is proportional to its cross-sectional area, and the elevator cable tension also increases proportionally with its own cross-sectional area. There is always a geometric relationship-determined, insurmountable gap in bearing capacity between the two.

### 6.3.5 Actual Role of the Ring for Elevator Cables After Closure

Although the ring cannot share the elevator cable tension, after closure the ring still plays an important geometric constraint role for the elevator system:

- **Provides a fixed connection point**: The top end of the elevator cable no longer needs to rely on its own counterweight to maintain precise GEO position. The counterweight only needs to provide upward net tension, and its position can be maintained with the help of the ring.
- **Resists perturbation drift**: The ring forms a continuous equatorial closed loop, effectively limiting the long-period drift of the six elevator tops under lunar/solar perturbations. The counterweight and ring together form a more stable suspension system.
- **Possibility of extending the counterweight orbit outward**: Placing the counterweight in a more distant orbit (e.g., 50,000–100,000 km) can use stronger centrifugal force to greatly reduce the counterweight mass. The ring facilitates this—the counterweight can be connected to the ring via a longer cable segment, and the ring itself provides a stable intermediate anchor point. This is only a concept; subsequent calculations are based on the GEO+200 km scheme, with counterweight mass unchanged. Counterweight optimization is further evaluated in Volume IV and Volume IX.

### 6.3.6 Finalization of Counterweight Scheme During and After Closure

| Parameter | Before Closure | After Closure |
|------|------|------|
| Counterweight mass (per elevator) | 8.0 × 10¹² kg | **Unchanged** (ring cannot share tension) |
| Counterweight orbit | GEO + 200 km | Can be extended to farther orbits to reduce mass |
| Main function of counterweight | Independently bears all GEO end tension | Independently bears all tension + longitudinal displacement compensation |
| Auxiliary role of ring | None | Provides geometric constraint, resists perturbation drift |


## 6.4 Segmented Manufacturing and Launch of Circumferential Cable

### 6.4.1 Segmentation Strategy and Parameter Determination

The main ring cable consists of multiple independent CNT braided sub-cables. According to the design in Volume II, the final cross-section is formed by N ≥ 1000 redundant sub-cables bundled together, including the outer sheath. Directly launching the entire continuous cable into orbit is unrealistic; it must be manufactured into manageable segment lengths at ground or lunar factories, then transported to GEO for on-orbit assembly.

**Determination of single segment length**:

The choice of segment length $L_{segment}$ must comprehensively consider the following factors:

| Constraint | Impact |
|------|------|
| Launch capacity | Heavy-lift rockets (Starship/Long March 9) LEO capacity about 150–250 t, direct GEO capacity about 50–100 t |
| On-orbit operation convenience | Shorter segments mean more splices (about 530,000 segments for the whole ring); longer segments make each operation more complex |
| Node strength impact | Each node strength is ~90% of the cable body (can be compensated by redundancy design) |
| Packaging limitation | Rocket fairing envelope (ø8–9 m, length 20–30 m) |
| Cable flexibility | Can be wound on large drums like a cable, minimum bending radius limited by microfilament damage |

Considering the above, the recommended single segment length is $L_{segment} = 500 m$ .

### 6.4.2 Segment Parameter Table

| Parameter | Value | Derivation Basis |
|------|------|------|
| Single segment length | 500 m | Balances launch capacity and number of splices |
| Ring cable linear density | ≈300 kg/m | Volume IV, Section 4.3, d=0.7 m, fill factor 0.6 |
| Single segment mass | ≈150 t | 500 m × 300 kg/m |
| Single segment mass with sheath | ≈150.06 t | Sheath linear density increment ≈0.12 kg/m (Volume IV, Section 4.11.2) |
| Total required segments | ≈530,916 | Ring circumference 265,458 km / 500 m |
| Total cable mass | ≈7.96 × 10⁷ t | Excluding redundancy backup |

### 6.4.3 Cable Segment Packaging and Deployment

Each cable segment, after manufacturing, is wound with about 10 kN of pre-tension on a reusable mandrel.

**Packaging parameters**:

| Parameter | Value | Note |
|------|------|------|
| Mandrel diameter | 3 m (collapsible, deployable) | Compatible with rocket fairing envelope |
| Wound cable outer diameter | ≤8 m | Including mandrel |
| Cable roll length | ≤20 m | Fits fairing |
| Cable storage bending radius | 1.5 m (short-term acceptable) | 100× cable diameter = 70 m for long-term safety |
| Minimum bending radius after deployment | ≥70 m | 100× cable diameter, to avoid microfilament damage |

During bending storage, the cable’s bending tensile strain on a mandrel of radius 1.5 m is:

$$
\varepsilon = \frac{r_{\text{cable}}}{R_{\text{spool}}} = \frac{0.35}{1.5} \approx 0.233
$$

This value far exceeds the elastic limit of a single CNT fiber, but the braided cable consists of thousands of fine microfilaments, which can adapt to bending through inter-tube sliding. Long-term storage may cause microfilament creep and strength degradation; the maximum allowable storage time will be a verification item (V6-M1).

### 6.4.4 Launch and Transportation Strategy

A single segment mass of 150 t exceeds the single direct GEO launch capacity. The "LEO aggregation + tug transfer" mode is adopted:

| Stage | Transport Tool | Description |
|------|------|------|
| Ground → LEO | Reusable heavy-lift rocket (Starship/Long March 9) | Each launch delivers 1 segment to LEO (about 400 km orbit) |
| LEO → GEO | Nuclear thermal/electric space tug | Tows from LEO aggregation orbit to GEO construction orbit (42,264 km) |
| Construction orbit | Space spider robot receives | On-orbit braiding and connection at 42,264 km |

At peak, about 200 segments per month need to be launched (30,000 t/month), requiring about 200 Starship-class rocket launches to LEO per month, and a tug fleet of about 50 ships. This transport intensity is extremely high, highlighting the strategic necessity of lunar in-situ manufacturing (Volume II, Pathway 2).


## 6.5 Detailed Design of Space Spider Robot

### 6.5.1 Functional Requirements

The space spider is the main executor of on-orbit construction and must independently complete the following tasks:
- Grasp and climb along the already positioned cable
- Pull out new cable segments from the mandrel and guide them to the splice point
- Operate end effectors to perform braiding
- Precisely align and lock inter-segment connection nodes
- Install sheath segments and thrust rings
- Carry or connect to the ring’s power supply system

### 6.5.2 Overall Configuration

Adopts an **eight-legged symmetric embracing configuration**. The main body consists of a central ring frame, with eight six-DOF mechanical legs symmetrically mounted on the ring frame, each leg equipped with a quick-change end effector.

**Ring frame parameters**:

| Parameter | Value | Note |
|------|------|------|
| Inner diameter | 0.6 m | Fits sheath outer diameter 0.552 m (with margin) |
| Outer diameter | 1.5 m | Accommodates equipment |
| Length | 2.5 m | Along cable axis |
| Structural material | Titanium alloy/CFRP hybrid truss | Balances strength and lightweight |

**Mechanical leg parameters**:

| Parameter | Value |
|------|------|
| Number | 8 |
| DOF per leg | 6 (shoulder 3 + elbow 1 + wrist 2) |
| Max extension radius | 4 m |
| Max end load | 5 kN (meets cable gripping and pre-tension needs) |
| Mass per leg | ≈80 kg |
| Drive type | Harmonic reducer + PMSM |
| Repeat positioning accuracy | ±0.5 mm |

**End effector types** (quick-change):

| Type | Function |
|------|------|
| Clamp type | Grips cable segment, provides axial tension |
| Braiding head | Operates multiple sub-cables for braiding |
| Bolt gun | Installs Inconel bolts for C/SiC flange |
| Binder | Installs aramid fiber tape binding |
| Inspection probe | Laser ranging + visual inspection of node quality |

### 6.5.3 Power Scheme

During construction, the space spider cannot continuously rely on external power (ring solar power station not yet built), so it must carry its own energy. Uses a **small space nuclear reactor + lithium-ion buffer battery** combination.

| Parameter | Value |
|------|------|
| Total peak power for arms | 8 kW |
| Ring frame movement and sensing | 2 kW |
| Communication and computing | 0.5 kW |
| Total design power | 12 kW (with redundancy) |
| Nuclear power type | 10 kWe class KRUSTY/Kilopower type |
| Annual nuclear fuel consumption | <50 kg (highly enriched uranium) |
| Buffer battery | Lithium-ion, 50 kWh |

### 6.5.4 Autonomous Navigation and Control

The space spider achieves autonomous navigation along the cable through:
- **Differential GPS/pseudolite positioning**: Uses preset reference beacons on the ring, positioning accuracy better than 0.1 m
- **Star tracker**: Determines attitude
- **Distributed fiber optic strain sensors on cable**: Senses cable tension and bending state
- **LIDAR**: Short-range obstacle avoidance and alignment (splicing accuracy requirement ±1 mm)

Movement speed:
- Axial crawling along cable: 0.05 m/s
- Circumferential rotation around cable: 0.1 rad/s


## 6.6 On-Orbit Braiding and Connection Process

### 6.6.1 Multi-Strand Cable Bundling and Braiding

The ring cable consists of N ≥ 1000 independent sub-cables. Construction adopts a **phased cable addition** strategy:

1. **Guide cable phase (Year 1–2)**: First deploy 4 guide sub-cables (each with cross-section about 0.00005 m²) to form a basic closed loop at the outer edge of GEO. At this stage, the ring only provides geometric guidance, with very low linear density (≈1.2 kg/m) and tension.
2. **Batch bundling (Year 3–12)**: The space spider lays 1 new sub-cable along the guide cable each time, using parallel arrangement, binding with aramid fiber tape every ~10 m. As the number of sub-cables increases, the ring’s linear density and tension gradually increase.
3. **Full cable phase (from Year 15)**: After all sub-cables are in place, the outer sheath and UHMWPE outer layer are added.

The braiding method uses **parallel arrangement + interval binding** (similar to prefabricated parallel wire strand technology), rather than traditional twisting. This maximizes single filament strength and avoids additional strength loss from twisting. Twisting reduces the axial component of sub-cables by about 30%–50% (see Section 2.3.3 of Volume II, f₂ loss factor 0.5–0.7), while parallel arrangement minimizes this loss.

**Binding parameters**:

| Parameter | Value | Note |
|------|------|------|
| Binding material | Aramid fiber tape | Tensile strength ≥3 GPa, vacuum compatible |
| Binding interval | 10 m | Ensures bundle integrity |
| Single binding pre-tension | ≥10 kN | Prevents sub-cable loosening/slippage |
| Binding tape width | 50 mm | — |

### 6.6.2 Inter-Segment Connection Node Design

Each cable segment is pre-installed with C/SiC composite flanges at both ends (same material as GEO end connector in Section 4.7 of Volume IV, allowable stress 500 MPa). Inter-segment connection is achieved by flange mating + bolt pre-tensioning.

**Node design parameters**:

| Parameter | Value | Note |
|------|------|------|
| Flange material | C/SiC composite | Allowable stress 500 MPa (NASA/TM-2010-216249) |
| Bolt material | Inconel 718 | Yield strength ≥1,100 MPa |
| Bolt specification | M24 × 3 | — |
| Single bolt pre-tension | ≥500 kN | — |
| Number of bolts per node | ≥24 | Provides redundancy |
| Node strength | ≥90% of cable body design strength | Redundancy design compensates for 10% loss |
| Bending stiffness | ≥95% of cable | Flange conical transition ensures |
| Angular deviation | <0.05° | Ensures subsequent car DM passage |
| Node length | ≈1 m (including both conical transitions) | — |

**Connection process**:

1. Space spider grips new segment in place
2. Align flange faces (laser guided, accuracy ±0.5 mm)
3. Pre-tighten 50% of bolts (cross-symmetric sequence)
4. Apply axial tension to 80% of design pre-tension, measure elongation to confirm uniformity
5. Tighten all bolts to rated torque
6. Release grip, laser measure straightness of cable on both sides of node

### 6.6.3 Node Protection and Monitoring

Each node is fitted with a removable aluminum alloy protective cover to reduce direct micrometeoroid impact on bolts. The cover is embedded with wireless strain sensors for long-term monitoring of node stress, with data transmitted to ground via the ring communication network.


## 6.7 Construction Sequence and Timing Simulation

### 6.7.1 General Principles

Ring construction must strictly follow the principle of **symmetric tensioning, gradual thickening**. At all times, the deployed cables must form **at least one closed loop in the equatorial plane**, with no free ends allowed. The construction process is divided into four stages.

**Stage 1: Initial Closed Loop (Year 1–2)**

Launch 4 guide cables (each 500 m, total mass 600 t), docked at the outer edge of GEO 100 km to form a ring with radius 42,264 km and minimal cross-section.

Initial ring parameters:
- Ring linear density: ≈1.2 kg/m (only 1/250 of design value)
- Circumferential tension: ≈1.13 × 10⁷ N (only 1/250 of full-cable state)
- Number of space spiders: 4
- This ring only provides geometric guidance, no mechanical support for elevator cables
- The six elevator counterweights operate independently at 200 km above GEO

**Stage 2: Cable Addition Phase (Year 3–12)**

Launch cables at about 150 segments per month (about 22,500 t/month), space spiders braid sub-cables segment by segment along the guide ring.

Key parameters for this stage:
- Ring linear density increases from 1.2 kg/m to about 150 kg/m (half the design value)
- Circumferential tension increases from about 1.13 × 10⁷ N to about 1.42 × 10⁹ N
- Number of space spiders increases from 50 initially to 200 at peak
- Elevator cable counterweights continue to operate independently, with GEO end tension fully borne by counterweights
- Distributed ion thrusters are needed to actively maintain ring roundness and inclination (thrust requirements refer to Volume I and Section 6.7.3)

**Stage 3: Closed Loop Tuning (Year 13–14)**

Pause cable addition, perform precise tension uniformity measurement and tuning for the entire ring, eliminate accumulated geometric deviations.

Key transition tasks for this stage:
1. Precisely align the GEO end counterweights of the six elevators with the predetermined connection nodes of the ring (position error <1 m)
2. Install C/SiC connectors (ø11.5 m conical transition), mechanically connect elevator cable tops to the ring
3. Counterweights continue to independently bear all GEO end tension
4. Begin installation of sheath segments (from GEO gradually toward ground)
5. Number of space spiders: 100 (mainly for maintenance)

**Stage 4: Full Cable Operation (from Year 15)**

Complete the remaining sub-cable bundling, ring cable reaches design cross-section (N ≥ 1000, linear density 300 kg/m). Install rack (middle layer of sheath) to prepare for car trial operation.

Full cable parameters:
- Ring linear density: 300 kg/m
- Circumferential tension: ≈2.83 × 10⁹ N
- Six elevator counterweights continue to independently bear their respective GEO end tension
- Counterweight function: bear GEO end tension + longitudinal displacement compensation (winch stroke ≥1,000 m)
- Number of space spiders: 50 (mainly for maintenance)

### 6.7.2 Construction Timeline

| Stage | Time | Cumulative Segments | Ring Linear Density (kg/m) | Circumferential Tension (N) | Space Spiders | Elevator Counterweight State |
|------|------|:--:|:--:|:--:|:--:|------|
| Stage 1 | Year 1–2 | 4 | 1.2 | ≈1.13 × 10⁷ | 4 | Independent condition, counterweight fully loaded |
| Stage 2 (early) | Year 3–5 | ≈5,400 | ≈6.5 | ≈6.14 × 10⁷ | 50 | Independent condition, counterweight fully loaded |
| Stage 2 (mid) | Year 6–10 | ≈180,000 | ≈100 | ≈9.44 × 10⁸ | 200 | Independent condition, counterweight fully loaded |
| Stage 2 (late) | Year 11–12 | ≈360,000 | ≈200 | ≈1.89 × 10⁹ | 200 | Independent condition, counterweight fully loaded |
| Stage 3 | Year 13–14 | All in place | ≈200→300 | ≈1.89→2.83 × 10⁹ | 100 | Ring and elevator mechanically connected, counterweight still fully loaded |
| Stage 4 | Year 15+ | ≈530,916 | 300 | ≈2.83 × 10⁹ | 50 (maintenance) | Counterweight fully loaded, long-term operation |

### 6.7.3 Dynamic Stability During Construction

In the early construction phase (ring linear density far below design value), the ring is highly susceptible to large deformations from solar radiation pressure and lunar perturbations. Based on the perturbation model in Volume I and the ring bearing capacity analysis in Section 6.3:

- **n=0 mode** (uniform expansion/contraction): In early stage with λ < 30 kg/m, the ring’s n=0 mode may be unstable and requires active control
- **n=2 mode** (elliptical deformation): Lunar perturbation may induce large elliptical deformation at low linear density

**Active control strategy**: Use distributed ion thrusters installed at nodes to provide active damping.

| Construction Stage | Ring Linear Density (kg/m) | Single Thruster Thrust Requirement | Number of Thrusters |
|------|:--:|:--:|:--:|
| Stage 1 | 1.2 | 0.05 N/10° arc | ≥36 (one per 10°) |
| Stage 2 early | 6.5 | 0.1 N/10° arc | ≥72 |
| Stage 2 mid | 100 | 0.5 N/10° arc | ≥180 |
| Stage 3 | 200+ | 1 N/10° arc | ≥360 |

Thrusters are gradually deployed during construction, with the final number matching the design requirement in Volume I (≥36, total thrust 100–200 N). Precise thrust timing and control laws are determined by comprehensive simulation in Volume VII.

### 6.7.4 Expansion Possibility

The multi-strand redundant braided structure of the ring cable supports progressive expansion. By paralleling additional cable segments on the outside of the existing closed loop, each added sub-cable proportionally increases the overall bearing capacity of the ring. The sheath and rack can be installed after expansion. This allows the ring’s bearing capacity to be gradually increased from the initial design value to several times higher to meet future demand growth.


## 6.8 Major Risks and Countermeasures

| Risk | Description | Countermeasures |
|------|------|----------|
| Debris impact | Exposed thin cable bundles during construction are highly susceptible to being cut by 1 cm debris | Initial guide ring uses multiple parallel redundancies; after single break, space spider quickly locates and repairs; deploy debris monitoring satellites in construction area to avoid large debris in advance |
| Cable entanglement | Simultaneous deployment of multiple cable segments may cause tangling | Use single-segment sequential deployment strategy; before each segment is deployed, spider grips the end to ensure the free end does not rotate; mandrel equipped with tension control system |
| Orbital drift | Incomplete ring is easily perturbed away from intended position before full cable | Gradually deploy and activate ion thrusters during construction (per Section 6.7.3), actively maintain position |
| Spider failure | Single robot failure | Each robot has self-check and rescue mode; redundant spiders can be towed back to maintenance station by others |
| Node pre-tension loss | Long-term operation may cause bolt pre-tension loss in C/SiC flange | Built-in strain sensors in node for real-time monitoring; space spider regularly inspects and re-tightens |
| Counterweight drift under independent condition | Counterweight may deviate from orbit due to lunar/solar perturbations during construction | Install ion thrusters on counterweight, use active maintenance system per Volume I to maintain position |


## 6.9 Summary of Verification Items

| No. | Item | Description | Responsible Volume |
|------|------|------|:--:|
| V6-M1 | Long-term small-radius bending storage strength degradation of CNT braided cable | 1:1 sample cable winding-storage-deployment cycle test, measure residual strength | Volume VII |
| V6-M2 | Space spider microgravity precision operation accuracy | Ground suspension/underwater simulation, measure positioning accuracy of typical braiding operations | Volume VII |
| V6-M3 | Fatigue life of inter-segment C/SiC flange under repeated tension fluctuation | Scaled model fatigue test, ≥10⁵ cycles | Volume VII |
| V6-M4 | Dynamic stability boundary of incomplete ring during construction | Multi-flexible body simulation + small-scale on-orbit verification | Volume VII |
| V6-M5 | Long-term binding retention of aramid fiber tape in vacuum UV/atomic oxygen environment | Vacuum chamber accelerated aging test | Volume VII |
| V6-M6 | Space spider multi-robot collision avoidance and scheduling | Simulation + ground multi-robot collaboration test | Volume VII |


## 6.10 Parameter Output

| Parameter | Value | Status | Receiving Volume |
|------|------|------|:--:|
| Single cable segment length | 500 m | Locked | Volume VIII |
| Single segment mass | ≈150 t | Locked | Volume VIII |
| Total ring cable mass | ≈7.96 × 10⁷ t | Locked | Volume II, VIII |
| Total required segments | ≈530,916 | Locked | Volume VIII |
| Number of space spiders | 4 initially, 200 at peak | Stage target | — |
| Power per space spider | 12 kW | Locked | — |
| Total construction period | About 15 years (construction) + 2 years (tuning) | Reference | — |
| Counterweight mass under independent condition (per elevator) | 8.0 × 10¹² kg | Locked | Volume IV |
| Ring design circumferential tension (full cable) | ≈2.83 × 10⁹ N | Locked | Volume I |
| Elevator cable GEO end tension (per elevator) | ≈2.09 × 10¹⁰ N | Locked | Volume IV |
| **Counterweight mass change after closure** | **Unchanged (ring cannot share tension)** | **Locked** | — |
| Inter-segment node strength | ≥90% of design strength | Design requirement | Volume VII verification |
| Number of thrusters deployed | Final ≥360 | Matches Volume I | — |


## 6.11 Conclusion of Volume VI

This volume completes the design of the circumferential structure construction plan and **rigorously proves through mechanical derivation that the circumferential tension of the ring after closure cannot share the GEO end tension of the elevator cable**—the ring’s circumferential tension (≈2.83 × 10⁹ N) is only 1/7.4 that of a single elevator cable (≈2.09 × 10¹⁰ N), and the ring’s bending stiffness under radial concentrated force is extremely low (slenderness ratio about 3.8 × 10⁸). Whether in the pure tension model or the elastic ring model, the ring cannot provide effective support. The counterweight mass remains unchanged before and after closure.

Core conclusions:

1. **Elevator cable counterweight cannot be reduced due to ring closure**. The main function of the ring is to provide a stable geometric connection point for the elevator top and resist perturbation drift. The counterweight can be considered for outward orbital migration (using stronger centrifugal force to reduce its own mass), but this is a concept; subsequent calculations are based on the GEO+200 km scheme, with counterweight mass unchanged.
2. **Segmented construction of the ring**: 500 m per segment, 150 t/segment, about 530,000 segments in total. Uses "LEO aggregation + tug transfer" mode for orbit insertion.
3. **Space spider**: Eight-legged embracing nuclear-powered robot, autonomously completes braiding and connection.
4. **Total construction period**: About 17 years (15 years construction + 2 years tuning). At peak, about 200 heavy-lift rocket launches per month are required, with enormous transport pressure, highlighting the strategic necessity of lunar in-situ manufacturing.
5. **Progressive expansion**: The ring cable supports continued addition of parallel cables on the outside after completion, with bearing capacity gradually increased as needed.

The output parameters of this volume are sufficient to support the comprehensive simulation verification in Volume VII and the transport logistics system planning in Volume VIII.

# Appendix 2: Stratospheric Platform

## Volume 1: Platform Overall Design

**Version**: 1.13<br/>
**Date**: June 2026<br/>
**Currency**: Chinese Yuan (RMB), symbol: ¥<br/>
**Related Main Volumes**: Main Volume 3, Main Volume 4<br/>
**Prerequisites**: Main Volume *Overview*, Appendix 2 Overview


### Abbreviation Reference Table

| Abbreviation | Full Name | Description |
|------|----------|------|
| CFRP | Carbon Fiber Reinforced Polymer | Structural reinforcement material for lightweight gondolas and tether cables |
| CNT | Carbon Nanotube | Core material for tether cables |
| EVOH | Ethylene Vinyl Alcohol Copolymer | Gas barrier layer material for aerostat envelopes; extremely low helium permeability |
| FOG | Fiber Optic Gyroscope | Core angular rate sensor for inertial navigation systems |
| GPS | Global Positioning System | Used for platform horizontal positioning (only available below 40 km) |
| HAPS | High-Altitude Pseudo-Satellite | International standard designation for stratospheric platforms |
| MLI | Multi-Layer Insulation | Used for thermal control of gondolas and platform equipment bays |
| MoS₂ | Molybdenum Disulfide | Solid lubricant for moving components in high-altitude low-pressure environments |
| PTFE | Polytetrafluoroethylene | Envelope protective coating and sealing material |
| RFC | Regenerative Fuel Cell | Used for platform nighttime power supply and buoyant gas replenishment |
| SiC | Silicon Carbide | Power device material for solid-state transformers |
| TPU | Thermoplastic Polyurethane | Inner envelope sealing material |
| UHMWPE | Ultra-High Molecular Weight Polyethylene | Protective and insulating outer layer for tether cables |
| Work Gondola | Work Gondola | Mission payload carrier platform that moves along the tether cable |


### 1.1 Volume Preface

This volume is positioned as the **spatial carrier and kinematic foundation** of the stratospheric platform system, focusing on answering the following core questions:

> What should a high-altitude platform look like if it needs to continuously reside at 20–50 km altitude for more than 6 months and be able to move short distances along its own tether cable for routine maintenance? What envelope material can allow an aerostat to operate long-term at -80°C low temperatures and intense ultraviolet radiation? What is the maximum engineering mass limit for an aerostat? If no ground anchor is used, relying purely on its own propulsion, what level of positional accuracy can be maintained? Does a twin-hull airship configuration offer advantages over a single hull? Once CNT materials are mature, how can the same cable simultaneously serve as tether, power supply, and communication? How are the mechanical attachment, electrical connection, and fiber optic interface implemented at the platform end?

This volume builds upon:
- **Appendix 2 Overview**: which has established the strategic positioning of the stratospheric platform as "deployed before the ring elevator, operated independently of the ring elevator," along with the four-phase evolution timeline.

The core tasks of this volume:

1. Establish the architecture of the stratospheric platform system — the aerostat (an aerial base stationed long-term at 20–50 km altitude) and the work gondola (carrying various mission payloads, moving short distances along the platform's own tether cable).
2. Design the aerodynamic shape of the aerostat (including twin-hull configuration assessment), envelope materials, buoyant gas, and long-term station-keeping scheme; provide lift and hull volume estimates at multiple reference altitudes; and assess the maximum engineering feasible mass from three dimensions: envelope mass, structural stiffness, and helium leakage rate. Estimate the mass of fixed loads such as working platform, propellers, drive mechanisms, and batteries.
3. Assess the feasibility of electric propellers as an auxiliary lift means.
4. Design the work gondola's drive system (winch + movable pulley), clamping mechanism, position sensing scheme, and multi-cable guying stabilization mechanism. The gondola moves along the platform's own tether cable, has independent power supply, and can operate without ground anchoring.
5. Perform rigorous engineering mechanics derivation for the tether cable — starting from the maximum horizontal thrust on the platform, determine the diameter of a single CNT tether cable, and include cable self-weight superposition verification. Design the cross-section structure of the tri-functional cable (tethering + power supply + communication), and provide linear density and total mass comparison between the pure tether and tri-functional options. Design the mechanical attachment, electrical connection, and fiber optic interface of the tri-functional cable at the platform end. Design the ground winch shaft-motor separation scheme and the coil effect elimination scheme for the insulating transition section.
6. Assess the engineering feasibility of maintaining positional stability without any ground anchor, relying entirely on the platform's own propulsion, and the requirements for different accuracy levels.
7. Output key parameters for use by Volume 2 (Energy & Positioning), Volume 3 (Maintenance & Repair), and Volume 10 (Technical Interfaces).


### 1.2 Platform Function and Overall Architecture

The core of the stratospheric platform system is a stratospheric airship that resides long-term in the 20–50 km altitude range. It carries the platform's main structure, energy system (photovoltaic array + energy storage), communication system (Ka/Ku antenna + fiber optic interface), payload equipment bay, lightning attraction device, and maintenance supply warehouse.

The platform carries one **work gondola**. The gondola moves short distances along the platform's own tether cable, carrying various mission payloads (inspection equipment, sensors, communication relay modules, experimental instruments, etc.), flexibly configured according to mission requirements. The gondola has its own drive system and independent power supply; it departs from the docking port at the bottom of the aerostat, travels down or up the tether cable to the working position, and returns to the aerostat after completing the mission. Details of the gondola and its various tools and payloads are in Volume 3.

After the platform enters operation, various functional modules can be expanded in the payload equipment bay — communication relay (Volume 6), lightning protection (Volume 5), atmospheric science experiments (Volume 4), etc. The scaled verification gondola (Volume 4) and heavy climbing gondola (Volume 3) are integrated in later stages of platform development; Volume 1 only discusses the platform's own independent operating conditions. The aerostat can be tethered to a ground anchor (Section 1.5), or can operate completely without anchoring, maintaining positional stability purely by its own propulsion (Section 1.6).


### 1.3 Aerostat Design

The aerostat adopts a **stratospheric airship** as the primary option and a **tethered balloon** as the economical backup option.

**(a) Lift Principle**

The aerostat relies on the aerostatic buoyancy provided by helium to overcome its own gravity. The magnitude of net lift depends on the difference between the mass of displaced air and the mass of internal helium. At any altitude $h$, the net lift per cubic meter of helium is:

$$
L_{\text{net}}(h) = [\rho_{\text{air}}(h) - \rho_{\text{He}}(h)] \times g
$$

where $\rho_{\text{air}}(h)$ and $\rho_{\text{He}}(h)$ are the air density and helium density at that altitude respectively, and $g = 9.81 \text{ m/s}^2$ is gravitational acceleration. Helium density is estimated using the ideal gas equation:

$$
\rho_{\text{He}}(h) = \frac{p(h) \times M_{\text{He}}}{R \times T(h)}
$$

where $p(h)$ and $T(h)$ are the atmospheric pressure and temperature at that altitude, $M_{\text{He}} = 4.0026 \text{ g/mol}$ is the molar mass of helium, and $R = 8.314 \text{ J/(mol} \cdotp \text{K)}$ is the gas constant.

The airship has a main gas cell (helium) and a ballonets (air) inside. By adjusting the air volume in the ballonets, the net lift and altitude of the airship are controlled. When the airship needs to ascend or descend, an electric air compressor inflates or deflates the ballonets, changing the total mass of the airship, thereby achieving altitude adjustment without releasing the precious helium.

**(b) Lift and Hull Volume Estimates at Three Reference Altitudes**

The following uses a total airship mass of $m = 5{,}000 \text{ kg}$ (including airship structure, energy system, communication equipment, maintenance supply warehouse, excluding gondola) as the design baseline, giving lift and hull volume estimates at three reference altitudes (20 km, 30 km, 50 km).

**20 km reference altitude**:

At 20 km altitude, air density $\rho_{\text{air}} \approx 0.088 \text{ kg/m}^3$, temperature $T \approx -57^\circ\text{C}$ (216 K). Helium density under these conditions is approximately $0.014 \text{ kg/m}^3$.

$$
L_{\text{net}} = (0.088 - 0.014) \times 9.81 \approx 0.726 \text{ N/m}^3
$$

$$
V_{\text{required}} = \frac{5{,}000 \times 9.81}{0.726} \approx 67{,}600 \text{ m}^3
$$

Corresponding hull length approximately 91 m, maximum diameter approximately 21 m (fineness ratio 4.3:1). 20 km is currently the most common station-keeping altitude for international HAPS platforms — the Sceye HAPS SE2 (82 m long) has a design operating altitude of approximately 20 km [3], and Thales Alenia Space's Stratobus has a design volume of 85,000 m³, station-keeping altitude of 20 km, and payload capacity of 250–450 kg [11][14].

**30 km reference altitude**:

At 30 km altitude, air density $\rho_{\text{air}} \approx 0.018 \text{ kg/m}^3$, temperature $T \approx -47^\circ\text{C}$ (226 K). Helium density is approximately $0.003 \text{ kg/m}^3$.

$$
L_{\text{net}} = (0.018 - 0.003) \times 9.81 \approx 0.147 \text{ N/m}^3
$$

$$
V_{\text{required}} = \frac{5{,}000 \times 9.81}{0.147} \approx 333{,}700 \text{ m}^3
$$

Corresponding hull length approximately 152 m, maximum diameter approximately 35 m. 30 km is the performance balance point for mid-to-upper stratospheric airships — at this altitude there is still sufficient air density to provide considerable buoyancy, and it is in the relatively stable upper-middle stratosphere from a meteorological standpoint.

**50 km reference altitude**:

50 km is the physical upper limit for aerostats relying solely on aerostatic buoyancy. At 50 km altitude, air density $\rho_{\text{air}} \approx 0.00103 \text{ kg/m}^3$, temperature $T \approx -3^\circ\text{C}$ (270 K), atmospheric pressure approximately 80 Pa. Helium density is approximately $1.43 \times 10^{-4} \text{ kg/m}^3$.

$$
L_{\text{net}} = (0.00103 - 0.000143) \times 9.81 \approx 0.0087 \text{ N/m}^3
$$

$$
V_{\text{required}} = \frac{5{,}000 \times 9.81}{0.0087} \approx 5{,}640{,}000 \text{ m}^3
$$

Corresponding hull length approximately 385 m, maximum diameter approximately 90 m (fineness ratio 4.3:1). This volume is extremely large — approximately 83 times the volume required at 20 km. If the total airship mass is compressed to 2,000 kg (retaining only the minimum structure, communication equipment, and maintenance supply warehouse), the required volume is approximately 2,260,000 m³ — approximately 33 times the 20 km/5,000 kg scheme, still exceeding the engineering feasible range for the current and foreseeable future.

This means long-term aerostatic buoyancy station-keeping at 50 km altitude is extremely difficult in engineering terms. The preferred method for operations at 50 km altitude is to use vertical thrust propellers for short-term assisted hovering at 50 km (see Section 1.3(e)), or to be reached by a gondola that can operate over a larger altitude range (see Volume 3).

**Comparison of the three reference altitudes**:

| Parameter | 20 km | 30 km | 50 km |
|:---:|:---:|:---:|:---:|
| Air density $\rho_{\text{air}}$ (kg/m³) | 0.088 | 0.018 | 0.00103 |
| Temperature $T$ (°C) | -57 | -47 | -3 |
| Pressure (Pa) | 5,529 | 1,197 | 80 |
| Net lift per m³ (N) | 0.726 | 0.147 | 0.0087 |
| Required volume $V$ (m³) @ m=5,000 kg | ≈67,600 | ≈333,700 | ≈5,640,000 |
| Hull length (m) @ fineness ratio 4.3:1 | ≈91 | ≈152 | ≈385 |
| Hull diameter (m) @ fineness ratio 4.3:1 | ≈21 | ≈35 | ≈90 |
| Engineering feasibility | Validated by existing similar platforms | Larger volume needed but technically achievable | Pure aerostatic buoyancy scheme essentially infeasible |

Note: Design margin 15%, i.e., the lift system (hull volume and buoyant gas) is designed for a total mass of 5,750 kg.

The actual permanent station-keeping altitude of the airship is designed for the 25–35 km range — within this range, air density can still provide acceptable hull volume, and wind speed and temperature conditions are suitable for long-term station-keeping. When short-term missions at 50 km altitude are needed, vertical thrust propellers provide auxiliary lift.

**(c) Envelope Materials**

The aerostat envelope must operate long-term ≥6 months at -80°C low temperature, high ultraviolet radiation (above the ozone layer, UV-C unfiltered), and low pressure (0.1–0.01 atm) without significant performance degradation. Key performance indicators for stratospheric airship envelope materials include high strength, low density, good environmental resistance, tear resistance, high gas impermeability, and low creep [20][21]. The recommended multi-layer composite envelope structure is as follows:

| Layer | Material | Thickness | Function |
|:---|:---|:---|:---|
| Outer layer | PTFE-coated fabric (or PVF film Tedlar®) | 0.1–0.2 mm | UV radiation resistance, hydrophobic anti-icing, ozone resistance, low gas permeability [21] |
| Load-bearing layer | Vectran® or Kevlar® fiber woven layer | 0.3–0.5 mm | Provides tensile strength and tear resistance [12][13] |
| Gas barrier layer | EVOH film or PVDC-treated BOPET film | 0.05–0.1 mm | Prevents helium leakage (helium molecules are extremely small and easily penetrate common polymers) [12][13] |
| Inner layer | Thermoplastic polyurethane (TPU) sealing layer | 0.05 mm | Heat-seal bonding, prevents internal abrasion [21] |

Envelope areal density target: ≤200 g/m². Latest literature data indicate this target is technically achievable — research-grade ultra-light fiber-reinforced laminates have achieved areal densities of 103–113 g/m² [12]. The Kevlar-based composite laminate designed in this study has an areal density of 207–262 g/m², helium permeability as low as 0.04 L/m²/24 h, tensile strength up to 968 N/cm, and tear strength of 513 N [13]. After 700 hours of accelerated artificial aging and 8 months of natural aging testing, laminate performance degradation is minimal [20]. Service life target: ≥5 years (returned to ground for inspection every 6 months).

**(d) Buoyant Gas Management**

Helium is stored in high-pressure cylinders. When the airship returns to the ground, helium is compressed and recovered into the cylinders; it is released back into the gas cell when ascending again. Helium annual leakage rate target: ≤5% (controlled through gas barrier layer and periodic top-up). Regenerative fuel cells in electrolysis mode split water into hydrogen and oxygen; hydrogen can simultaneously serve as buoyant gas and energy storage medium. Modeling results based on the Stratobus design show that RFC-assisted pressure maintenance can extend airship endurance by 25.5%, and further to 118.2 days when a balloon storage system is used [10]. Air in the ballonets is drawn in and expelled through an electric air compressor, adjusting the net lift of the airship.

**(e) Electric Propeller Auxiliary Lift Assessment**

At altitudes where aerostatic buoyancy is insufficient to support the total airship mass (e.g., near 50 km), or when short-term missions need to be performed at a higher altitude than the aerostat's normal station-keeping altitude, electric propellers generating vertical downward thrust can be considered as a supplement to aerostatic buoyancy. The airship still relies primarily on aerostatic buoyancy for most of the time; propeller auxiliary lift is only used for special scenarios.

**(1) Applicable Scenarios**

| Scenario | Altitude Range | Description |
|:---|:---|:---|
| High-altitude breakthrough | 40–50 km | Aerostatic buoyancy has greatly diminished (net lift per cubic meter at 50 km is only 1/17 of that at 30 km); propellers supplement the lift deficit during short-term missions |
| Position maintenance under strong wind | 20–40 km | When encountering seasonal jet streams (wind speed >50 m/s), propeller vertical thrust assists the tether cable to jointly maintain positional stability |
| Emergency lift redundancy | Full altitude | When the airship experiences helium leakage or envelope damage causing partial buoyancy loss, propellers provide emergency supplemental lift to maintain altitude |

**(2) Lift Demand and Power Estimation**

Using a total airship mass of 5,000 kg (net buoyancy requirement approximately 49.1 kN) as the baseline, assuming aerostatic buoyancy can only provide 70% of the lift (approximately 34.4 kN), the remaining 30% (approximately 14.7 kN) must be provided by propeller assistance. Using 4 vertical thrust propellers, each providing approximately 3.7 kN thrust.

Propeller thrust in low-density atmosphere is given by momentum theory:

$$
T = \dot{m} \times v_{\text{ind}} = \rho_{\text{air}} \times A_{\text{disk}} \times v_{\text{ind}}^2
$$

where $\dot{m}$ is the mass flow rate through the propeller disk, $v_{\text{ind}}$ is the induced velocity, and $A_{\text{disk}}$ is the disk area.

Taking 50 km altitude ($\rho_{\text{air}} \approx 0.00103 \text{ kg/m}^3$), single propeller thrust 3.7 kN, disk diameter 3 m (disk area approximately 7.07 m²) as an example:

$$
v_{\text{ind}} = \sqrt{\frac{T}{\rho_{\text{air}} \times A_{\text{disk}}}} = \sqrt{\frac{3{,}700}{0.00103 \times 7.07}} \approx 713 \text{ m/s}
$$

Required power:

$$
P_{\text{single}} = T \times v_{\text{ind}} = 3{,}700 \times 713 \approx 2.64 \times 10^6 \text{ W} \approx 2{,}640 \text{ kW}
$$

Four propellers total approximately 10.6 MW. If short-term missions at 50 km altitude are performed (e.g., no more than 2 hours each), the required energy can be provided by the platform's energy storage system. If long-term station-keeping at 50 km is required, this scheme is unsustainable in terms of energy.

**(3) Optimization of Disk Area and Induced Velocity**

Increasing the disk area can reduce the induced velocity, thereby reducing power requirements. The following compares different disk diameters for producing 3.7 kN thrust per propeller at 50 km altitude:

| Disk Diameter (m) | Disk Area (m²) | Induced Velocity (m/s) | Single Power (kW) | Four Total Power (MW) |
|:---:|:---:|:---:|:---:|:---:|
| 3 | 7.07 | 713 | 2,640 | 10.6 |
| 5 | 19.63 | 428 | 1,580 | 6.3 |
| 8 | 50.27 | 267 | 990 | 4.0 |
| 10 | 78.54 | 214 | 790 | 3.2 |

**(4) Engineering Feasibility Assessment**

Electric propeller auxiliary lift is fully feasible in principle, but is only used for short-term missions (single duration ≤2 h) in the 40–50 km range. Motor heat dissipation at high altitude is extremely difficult (convective heat dissipation is essentially ineffective, and radiative heat dissipation must be relied upon), and must be designed uniformly within the energy and thermal management system in Volume 2.

**(f) Engineering Feasible Mass Upper Limit of the Airship**

The mass upper limit of the airship is not determined by a single factor, but is jointly constrained by envelope areal density and structural efficiency, hull volume and structural stiffness, and helium leakage rate.

**(1) Envelope Mass Constraint**

Envelope mass $m_{\text{env}}$ is determined by the envelope areal density $\sigma_{\text{env}}$ and the hull surface area $A_{\text{surface}}$. The hull is approximated as an ellipsoid (semi-major axis $a = L/2$, semi-minor axis $b = D/2$, fineness ratio $\lambda = L/D$), and the surface area is given by:

$$
e = \sqrt{1 - \frac{1}{\lambda^2}}
$$

$$
A_{\text{surface}} = 2\pi b^2 \left[1 + \frac{a}{b} \cdot \frac{\arcsin(e)}{e}\right]
$$

Hull volume $V = \frac{4}{3}\pi a b^2 = \frac{\pi}{6}\lambda D^3$, from which $D = \left(\frac{6V}{\pi\lambda}\right)^{1/3}$, $b = D/2$.

Define the envelope mass ratio $\alpha_{\text{env}} = m_{\text{env}}/m_{\text{total}}$. Taking $\alpha_{\text{env}} = 0.15$ (optimistic structural efficiency), $\sigma_{\text{env}} = 150 \text{ g/m}^2$ (current research-grade level) as an example, at 30 km altitude ($V \approx 333{,}700 \text{ m}^3$, $D \approx 35 \text{ m}$, $A_{\text{surface}} \approx 13{,}500 \text{ m}^2$):

$$
m_{\text{total,max}} = \frac{m_{\text{env}}}{\alpha_{\text{env}}} = \frac{\sigma_{\text{env}} \times A_{\text{surface}}}{\alpha_{\text{env}}} = \frac{0.150 \times 13{,}500}{0.15} \approx 13{,}500 \text{ kg}
$$

Mass upper limits at different altitudes and envelope areal densities (with $\alpha_{\text{env}}=0.15$):

| Station-Keeping Altitude | Hull Volume (m³) | Surface Area (m²) | $\sigma$=100 g/m² | $\sigma$=150 g/m² | $\sigma$=200 g/m² | $\sigma$=250 g/m² |
|:---:|:---:|:---:|:---:|:---:|:---:|:---:|
| 20 km | 67,600 | 5,200 | 3,470 kg | 5,200 kg | 6,930 kg | 8,670 kg |
| 30 km | 333,700 | 13,500 | 9,000 kg | 13,500 kg | 18,000 kg | 22,500 kg |

**(2) Hull Volume and Structural Stiffness Constraint**

As hull size increases, structural stiffness becomes the limiting factor. Taking 200 m as the current empirically feasible hull length upper limit (not ruling out future breakthroughs), the corresponding volume upper limit is:

$$
V_{\text{max}} = \frac{\pi}{6} \times 4.3 \times \left(\frac{200}{4.3}\right)^3 \approx 757{,}000 \text{ m}^3
$$

At 30 km altitude, the net lift of this volume is approximately $757{,}000 \times 0.147 \approx 111{,}000 \text{ N}$, capable of supporting a total mass of approximately 11,300 kg.

**(3) Multiplier Effect of Helium Leakage Rate**

The helium permeability of the gas barrier layer determines the top-up volume, which is proportional to the hull surface area — the larger the hull, the greater the total leakage. For very large airships, periodic top-up alone is no longer economical; RFC-assisted pressure maintenance must be relied upon [10].

**(4) Comprehensive Feasibility Domain**

The envelope mass constraint, hull structural stiffness constraint, and helium leakage rate together define the engineering feasibility domain of the airship. At a station-keeping altitude of 30 km, envelope areal density of 150 g/m², and envelope mass ratio of 15%, the envelope mass constraint gives a mass upper limit of approximately 13,500 kg; hull structural stiffness gives a mass upper limit of approximately 11,300 kg — the two converge at the 10–15 tonne range. In the long term, as envelope areal density drops below 100 g/m² and active structural control technology matures, this upper limit is expected to rise to 20–25 tonnes.

| Technology Scenario | Envelope Areal Density | Hull Length Limit | Feasible Mass Upper Limit (30 km) | Key Assumptions |
|:---|:---:|:---:|:---:|:---|
| Current conservative | 200 g/m² | 150 m | ≈5,000 kg | Validated by existing similar platforms |
| Near-to-mid-term feasible | 150 g/m² | 200 m | ≈11,000 kg | Envelope weight reduction + active structural control |
| Long-term optimistic | 100 g/m² | 250 m | ≈25,000 kg | Ultra-light envelope + rigid skeleton structural breakthrough |

**(g) Design Margin**

In the above lift and mass analysis, all calculated results are physical estimates under ideal conditions. The actual airship faces the following unforeseeable factors during long-term operation: the actual degradation rate of envelope material under the combined effect of ultraviolet radiation and low temperature may be faster than predicted by ground accelerated aging experiments [20]; local stratospheric wind fields may experience brief gusts exceeding the design baseline of 50 m/s; the actual efficiency of photovoltaic arrays may be lower than rated values due to lunar dust (if deployed near the lunar surface) or high-altitude ice crystal deposition. To cover these uncertainties, this design reserves a 15% design margin on the basis of a design total mass of 5,000 kg, i.e., the lift system (hull volume and buoyant gas) is designed for a total mass of 5,750 kg, to ensure that the airship can still safely station-keep and operate even if partial performance degradation occurs during actual operation. This margin has been incorporated into the safety factor considerations in Section 1.5 for tether cable tension calculation and Section 1.6 for anchor-free energy consumption assessment — the tether cable safety factor is 3.0, which already includes tolerance for uncertainty that the actual total mass of the airship may exceed the design value.

**(h) Twin-Hull Airship Configuration Assessment**

The above analysis is based on the traditional single-hull configuration. A twin-hull airship — with two parallel main gas cells connected by a central rigid platform — has several engineering advantages, but also inherent costs. The following provides a comparative assessment from five dimensions: lift, drag, structure, platform space, and tethering stability. Research has shown that the aerodynamic drag of a twin-hull airship configuration can be approximately 20%–30% less than a single hull at certain cruise speeds, but the mass increase of the connecting structure must be deducted from the lift [17].

**(1) Configuration Comparison**

| Dimension | Single Hull (fineness ratio 4.3:1) | Twin Hull (two hulls side by side, connected by central platform) |
|:---|:---|:---|
| Total volume of two gas cells | 333,700 m³ (ø35 m × 152 m) | Each 166,850 m³ (ø27 m × 116 m), total 333,700 m³ |
| Lift (at 30 km) | 49.1 kN (baseline) | Essentially unchanged (total displaced air mass the same; mass increase of central platform must be deducted. Lift loss <1% if central platform mass <400 kg) |
| Projected area (at 30 km) | ≈4,500 m² (side area) | Depends on spacing between gas cells. With spacing equal to 0.8 times single gas cell diameter (approximately 22 m), total projected area approximately 3,490 m² (reduction of approximately 22%) |
| Wind drag (30 m/s wind) | 208.6 kN (baseline) | Approximately 162 kN (due to 22% reduction in projected area) |
| Usable platform space | Bottom suspension | Between the two gas cells: a rigid connecting platform approximately 22 m wide × 60 m long, accommodating a larger area of payload equipment bays, maintenance supply warehouses, and docking interfaces |
| Tethering stability | Single-cable tethering; upwind stability depends on propulsion system | Spacing between two gas cells generates natural roll restoring moment (similar to catamaran principle); upwind stability superior to single hull |
| Structural complexity | Mature solution | Central rigid platform connecting structure adds mass (estimated increase of approximately 15%–20% structural mass), but reduces need for tail fins and stabilizing surfaces [18] |
| Total envelope area | ≈13,500 m² (baseline) | ≈10,900 m² (reduction of approximately 19%, as two gas cells have smaller diameters) |

The twin-hull airship configuration has obvious advantages in usable platform space and upwind tethering stability. The approximately 22 m wide central platform between the two gas cells provides far more space for payload equipment than the bottom-suspension scheme of a single hull. Under 30 m/s wind conditions, the projected area of the twin-hull configuration is approximately 22% less than the single hull, with correspondingly reduced wind drag, lowering tether cable tension requirements and position-maintenance energy consumption of the propulsion system. The lift of the twin-hull configuration is essentially the same as the single hull (total displaced air mass is the same), but the mass increase of the central rigid platform connecting structure must be deducted from the lift.

From the perspective of envelope area, the total surface area of the two gas cells in a twin-hull configuration is approximately 10,900 m², approximately 19% less than the single hull (13,500 m²) — this means that at the same envelope areal density, the total envelope mass of the twin-hull configuration is lighter, and this mass savings can partially offset the mass increase of the central platform.

**(2) Selection for This Design**

At the near-to-mid-term feasible technology level (envelope areal density 150 g/m², hull length limit approximately 150 m), the total airship mass is approximately 5,000 kg, and at this point the single-hull scheme is more mature and lower risk. The unique advantages of the twin-hull configuration (central platform space, upwind stability) will become significant when the total mass increases to approximately 10,000 kg or more. It is recommended to adopt the single-hull scheme for the first deployment phase, with an interface reserved for switching to the twin-hull configuration when the mass increases to more than 10 tonnes in the long term.

**(i) Fixed Load Mass Estimate**

The following provides the fixed load mass allocation table at the 5,000 kg design baseline; each sub-item mass is estimated based on conventional equipment selection for independent operating conditions. 5,000 kg is the design baseline target value; the sum of all sub-items totals approximately 6,290 kg, and this difference is fully covered by the 15% design margin (lift system designed for 5,750 kg). The tri-functional cable scheme requires waiting until the airship lift is increased to the near-to-mid-term feasible upper limit before it becomes mass-feasible.

| Load Sub-Item | Estimated Mass (kg) | Key Assumptions |
|:---|:---:|:---|
| Envelope (including gas barrier layer + load-bearing layer + protective layer) | 2,025 | $\sigma=150 \text{ g/m}^2$, $A \approx 13{,}500 \text{ m}^2$, $\alpha=0.15$ |
| Internal structure (frames, cable net, tail fins) | 750 | Approximately 15% of total mass |
| Photovoltaic array (including deployment mechanism) | 1,190 | Area 8,500 m², areal density 0.14 kg/m² (including flexible substrate and wiring) |
| Energy storage system (lithium-ion battery) | 400 | Approximately 100 kWh capacity, energy density 250 Wh/kg |
| Propulsion system (four electric propellers including controllers) | 200 | 50 kg each, including motor + blades + controller |
| Communication system (Ka/Ku antenna + fiber optic interface) | 80 | Including antenna, amplifier, modem |
| Main transformer (±100 kV/±10 kV DC, SiC solid-state) | 500 | See Section 1.5(g) |
| Secondary transformers (10 kV/690V AC + 10 kV/400V AC + low-voltage DC) | 200 | Three units total |
| Payload equipment bay (including maintenance supply warehouse) | 200 | Empty bay structural mass, excluding mission payloads |
| Work gondola (including drive system and maintenance toolkit) | 500 | See Section 1.4 |
| Helium management system (cylinders + valves + piping) | 120 | Including high-pressure cylinders (composite carbon fiber wound) and valve piping |
| Thermal control system (radiative heat dissipation panels + heat pipe network) | 65 | Covering all equipment |
| Backup and margin | 60 | — |
| **Total** | **≈6,290** | — |

> Note: The total of approximately 6,290 kg already exceeds the lift margin at the current conservative technology level (5,750 kg, including 15% design margin). At the current conservative technology level, the platform can only adopt the anchor-free pure-propulsion position-keeping scheme (Section 1.6). The tri-functional cable scheme requires waiting until the airship lift is increased to the near-to-mid-term feasible upper limit (≈11,000 kg, see Section 1.3(f)) before it becomes mass-feasible.


### 1.4 Work Gondola

The work gondola moves short distances along the platform's own tether cable (altitude range 20–50 km), carrying various mission payloads — inspection equipment, sensors, communication relay modules, experimental instruments, etc., flexibly configured according to mission requirements. The gondola has its own drive system and independent power supply; it departs from the docking port at the bottom of the aerostat, travels down or up the tether cable to the working position, and returns to the aerostat after completing the mission. Details of the gondola and its various tools and payloads are in Volume 3.

**(a) Overall Configuration and Drive Scheme**

The gondola adopts a **winch + movable pulley** drive scheme. The drive winch is installed inside the aerostat (rather than on the gondola itself), and a set of movable pulleys is installed on top of the gondola. The tether cable extends from the winch inside the aerostat, passes around the movable pulleys on top of the gondola, and returns to a fixed point on the aerostat. When the winch retracts the cable, the movable pulley block lifts the gondola; when the winch releases cable, the gondola descends under gravity. The movable pulley block amplifies the driving force of the winch by a factor of 2 (single movable pulley), while halving the lifting speed of the gondola, providing a natural deceleration and stabilization effect.

The engineering advantage of this scheme is that the gondola itself no longer needs to carry drive motors and rack-and-pinion clamping mechanisms, greatly reducing the structural mass of the gondola itself. All drive and braking equipment is concentrated inside the aerostat, facilitating maintenance and heat dissipation without being limited by gondola volume and mass. The tether cable also no longer needs a rack, simplifying it to a standard CNT braided cable (sharing the same material and specification as the anchor tether cable in Section 1.5).

| Parameter | Design Value | Description |
|:---|:---|:---|
| Total mass (unloaded) | ≤500 kg | Including movable pulley block, stabilization mechanism, various mission payload interfaces |
| Payload | ≥300 kg | Carrying inspection equipment, sensors, communication relay modules, experimental instruments, etc. according to mission requirements |
| Maximum operating altitude | 50 km | Consistent with the maximum altitude the aerostat can reach |
| Cable extension/retraction speed | 0–4 m/s (adjustable) | Actual gondola ascent/descent speed is 1/2 of cable speed (single movable pulley) |
| Drive method | Aerostat-mounted electric winch + gondola movable pulley block | Winch power approximately 25 kW (peak), powered by aerostat main battery |
| Braking system | Winch with integrated electromagnetic brake (normally closed) + gondola emergency mechanical brake (spring-loaded) | Dual redundancy; failure of either does not affect safety |
| Position sensing | FOG inertial navigation + cable markers + barometric altimeter + GPS/BeiDou | Accuracy ±10 cm |
| Winch cable capacity | ≥55 km (50 km operating altitude + 10% margin) | Cable diameter ≥6.2 mm (same specification as tether cable) |

**(b) Clamping and Safety Braking**

The gondola is connected to the tether cable through the movable pulley block; the bearings and cable guide grooves of the movable pulley block provide the gondola with the only degree of freedom for movement along the cable. In the event of winch failure (e.g., motor fault, reducer jamming), the winch's integrated electromagnetic brake automatically locks the drum upon power loss, preventing further cable release. If the cable breaks between the gondola and the winch, the spring-loaded emergency brake on the gondola automatically clamps the cable, locking the gondola near the break point and preventing it from falling.

**(c) Position Sensing Scheme**

The gondola obtains altitude and attitude information along the tether cable through multi-sensor fusion: a fiber optic gyroscope inertial navigation system provides continuous altitude change data; laser reflective markers placed every 100 m on the tether cable are read by the gondola's laser rangefinder to eliminate accumulated errors; a barometric altimeter serves as an independent altitude range verification means; GPS/BeiDou can assist positioning below 40 km.

**(d) Wind-Induced Oscillation Stabilization Mechanism and Multi-Cable Guying Stabilization**

The gondola hangs below the tether cable and is subject to the continuous action of stratospheric wind fields in the 20–50 km altitude range. Without stabilization mechanisms, the gondola would oscillate continuously like a pendulum hanging at the end of a rope under wind drag. The following four-stage stabilization scheme is used, from passive aerodynamic to active mechanical, covering the full wind speed range.

**Stage 1: Passive Aerodynamic Stabilizer Fins (Primary Scheme)**

A set of lightweight passive aerodynamic stabilizer fins is installed at the rear of the gondola. The fins are composed of a CFRP skeleton and PTFE-coated fabric skin, with total mass not exceeding 15 kg. When the gondola deflects due to wind drag, the aerodynamic restoring moment generated by the fins automatically aligns it with the wind direction, suppressing oscillation amplitude within an acceptable range. A similar design has been validated on NASA's AeroPod instrument platform — AeroPod uses a passive aerodynamic stabilizer to stably suspend payloads below a tethered balloon, greatly reducing oscillation amplitude compared to traditional cable suspension schemes [19].

**Stage 2: Low Center of Gravity Self-Alignment**

The center of gravity of the gondola is designed to be approximately 1.5–2.0 m below the movable pulley suspension point. This low center of gravity layout uses gravity to generate a natural centering restoring moment — when the gondola deviates from the vertical position, the moment generated by gravity automatically returns it to the vertical attitude. This scheme consumes no electrical power and is a completely passive stabilization means; its disadvantage is that it is effective for small-amplitude oscillations, and active control is needed in conjunction with it under strong wind conditions.

**Stage 3: Multi-Cable Guying Stabilization**

When the gondola needs to perform high-precision work under strong wind (>30 m/s) conditions, 2–3 auxiliary guying cables can be added between the gondola and the aerostat. The auxiliary cables extend from different positions at the bottom of the aerostat and are connected to lateral attachment points on the gondola, forming a triangular or quadrilateral cable constraint network. Multi-cable guying geometrically limits the maximum horizontal displacement of the gondola — when the gondola attempts to swing to one side, the cable on the opposite side tightens, directly suppressing the oscillation. The auxiliary cables use lightweight UHMWPE braided cable (diameter approximately 3 mm), with total mass not exceeding 20 kg; the gondola's own electric tensioner adjusts the tension of each cable in real time based on inertial sensor data.

The principle of multi-cable guying is similar to a Stewart platform — through parallel constraint by multiple cables, all six degrees of freedom of the working platform are geometrically limited. This scheme has been widely used in large tethered balloons and lifting equipment [23][24].

**Stage 4: Active Damping Control (Backup Scheme)**

Under extreme wind conditions (>40 m/s), a small electric flywheel or control moment gyroscope carried by the gondola provides active damping torque. When the gondola's inertial sensors detect that the oscillation angular velocity exceeds the threshold (>2°/s), the flywheel accelerates rotation to generate a reaction torque, attenuating the oscillation amplitude to an acceptable range within tens of seconds. The active damping system has low power consumption (peak <200 W) and is in sleep mode under most operating conditions.


### 1.5 Tether Cable Material and Anchoring Scheme

The stratospheric platform relies on **tether cables** anchored to the ground. Multiple tether cables (≥3, evenly distributed at 120° intervals) transmit the net lift and horizontal wind load of the airship to ground anchor points, while providing electricity through the CNT conductive layer and communication through embedded optical fibers. In scenarios where deploying anchors is inappropriate or uneconomical, the platform can switch to the anchor-free pure-propulsion position-keeping scheme (Section 1.6).

**(a) Design Conditions and Environmental Constraints**

The design basis for the cable takes the most unfavorable combination: the airship is stationed at the highest design altitude (50 km) and simultaneously encounters the highest recorded wind speed for that altitude range. The following atmospheric parameters are taken from the 1976 U.S. Standard Atmosphere (USSA-1976) and published data on extreme wind conditions.

**Atmospheric Parameters** (selected for 50 km):

| Parameter | Value | Source |
|:---|:---:|:---|
| Air density $\rho_{\text{air}}$ | 0.00103 kg/m³ | USSA-1976 standard atmosphere at 50 km altitude |
| Gravitational acceleration $g$ | 9.81 m/s² | — |

**(b) Airship Horizontal Thrust Estimation**

The following four standard wind conditions are adopted:

- **Operating condition** (wind speed 30 m/s): Typical stratospheric wind speed during continuous airship operation.
- **Safe shutdown condition** (wind speed 40 m/s): The airship must maintain tethering and positional stability after stopping active operations and stowing equipment.
- **Minimum tethering wind condition** (wind speed 20 m/s): Used to verify minimum cable pre-tension.
- **Maximum tethering wind condition** (wind speed 50 m/s): The highest 30-minute average wind speed on record for this altitude range. This is the **design baseline condition**.

> Note: The maximum tethering wind condition of 50 m/s is a 30-minute average wind speed; the corresponding instantaneous gust is approximately 60–75 m/s (gust factor 1.2–1.5). With a safety factor of 3.0, the cable design tension already covers the load uncertainty from instantaneous gusts exceeding the average wind speed, with ample safety margin.

The airship horizontal thrust (wind drag) is given by:

$$
F_{\text{horizontal}} = \frac{1}{2} \times \rho_{\text{air}} \times v_{\text{wind}}^2 \times A_{\text{proj}} \times C_d
$$

where $A_{\text{proj}}$ is the projected area of the airship in the horizontal direction and $C_d$ is the drag coefficient. The aerodynamic drag coefficient of a stratospheric airship is jointly influenced by wind speed, air density, and Reynolds number — CFD numerical simulation studies show that the aerodynamic drag coefficient decreases with increasing wind speed and air density, and first decreases then increases with increasing fineness ratio, with a drag coefficient of approximately 0.02–0.06 in the fineness ratio range of approximately 4:1–5:1 [1][2]. This design takes $C_d \approx 0.05$ (based on CFD simulation results for fineness ratio 4.3:1 and Reynolds number approximately 3×10⁶ at 30 km altitude [1]).

With $A_{\text{proj}} \approx 4{,}500 \text{ m}^2$ (projected area of the hull in the horizontal direction, approximated as the side area of the hull):

| Wind Condition | $v_{\text{wind}}$ (m/s) | $\frac{1}{2}\rho v^2$ (Pa) | $F_{\text{horizontal}}$ (kN) |
|:---:|:---:|:---:|:---:|
| Minimum tethering | 20 | 0.21 | 46.3 |
| Operating | 30 | 0.46 | 104.3 |
| Safe shutdown | 40 | 0.82 | 185.4 |
| Maximum tethering | 50 | 1.29 | 289.7 |

Taking the maximum tethering wind condition (50 m/s) as the design baseline: $F_{\text{horizontal,max}} \approx 289.7 \text{ kN}$.

**(c) Single Cable Maximum Static Tension and Self-Weight Superposition Verification**

The platform's tethering system consists of $n_{\text{cable}}$ cables ($n_{\text{cable}} \geq 3$). Horizontal thrust is jointly borne by the horizontal tension components of multiple cables. For $n_{\text{cable}} = 4$ (four-cable scheme, 90° symmetric distribution), the load distribution non-uniformity factor $\eta = 1.4$. Under maximum tethering wind conditions, the main load-bearing cable on the windward side bears the maximum load alone.

The maximum static tension of a single cable is conservatively taken as the equivalent horizontal force proportion it bears alone (in the most unfavorable condition, a single cable bears approximately 80% of the total horizontal thrust component) plus the vertical component of that cable, with a safety factor of 3.0:

$$
F_{\text{single,design}} \approx 200 \text{ kN}
$$

The above 200 kN is the external load (net airship lift and horizontal wind load component) borne by the cable at the airship connection end, excluding cable self-weight. The cable is 25–50 km long, and the tension generated by self-weight is superimposed on the external load, forming a gradually increasing tension distribution from the lower end to the upper end of the cable. The total tension at the upper end (connecting the airship) of the cable is:

$$
T_{\text{upper}} = F_{\text{single,design}} + W_{\text{cable}}
$$

where $W_{\text{cable}}$ is the self-weight of a single cable. The following provides self-weight superposition verification for three CNT engineering strength options.

**(1) Optimistic Option (CNT Engineering Strength 20 GPa)**

CNT conductive layer cross-sectional area 30 mm², cable diameter 6.2 mm, linear density approximately 0.06 kg/m including UHMWPE jacket. 25 km single cable self-weight:

$$
W_{\text{cable}} = 0.06 \times 25{,}000 \times 9.81 \times 10^{-3} \approx 14.7 \text{ kN}
$$

Total tension at single cable upper end:

$$
T_{\text{upper}} = 200 + 14.7 \approx 214.7 \text{ kN}
$$

CNT allowable tension = 30 × 10⁻⁶ × 20 × 10⁹ / 3.0 ≈ 200 kN (cross-sectional area for tethering requirement). After accounting for self-weight, 214.7 kN > allowable 200 kN — exceeds by approximately 7%; the cable cross-sectional area needs to be slightly increased to approximately 32.2 mm² to meet the allowable requirement after self-weight superposition.

If subsequent functional expansion requires a larger cross-sectional area (e.g., lightning attraction function in Volume 5), the value shall be taken according to the expansion requirements; here only verification against the tethering requirement is performed.

**(2) Conservative Option (CNT Engineering Strength 4.5 GPa)**

Cable cross-sectional area 133.3 mm², diameter 13.0 mm, linear density approximately 0.22 kg/m including UHMWPE jacket. 25 km single cable self-weight:

$$
W_{\text{cable}} = 0.22 \times 25{,}000 \times 9.81 \times 10^{-3} \approx 54.0 \text{ kN}
$$

Total tension at single cable upper end:

$$
T_{\text{upper}} = 200 + 54.0 \approx 254.0 \text{ kN}
$$

CNT allowable tension = 133.3 × 10⁻⁶ × 4.5 × 10⁹ / 3.0 ≈ 200 kN (cross-sectional area for tethering requirement). After accounting for self-weight, 254.0 kN > allowable 200 kN — exceeds by approximately 27%; the cable cross-sectional area must be increased to approximately 169 mm² to meet the allowable requirement after self-weight superposition.

**(3) Commercial Option (CNT Engineering Strength 3 GPa)**

Cable cross-sectional area 200 mm², diameter 16.0 mm, linear density approximately 0.33 kg/m including UHMWPE jacket. 25 km single cable self-weight:

$$
W_{\text{cable}} = 0.33 \times 25{,}000 \times 9.81 \times 10^{-3} \approx 80.9 \text{ kN}
$$

Total tension at single cable upper end:

$$
T_{\text{upper}} = 200 + 80.9 \approx 280.9 \text{ kN}
$$

CNT allowable tension = 200 × 10⁻⁶ × 3 × 10⁹ / 3.0 ≈ 200 kN (cross-sectional area for tethering requirement). After accounting for self-weight, 280.9 kN > allowable 200 kN — exceeds by approximately 40%; the cable cross-sectional area must be increased to approximately 281 mm² to meet the allowable requirement after self-weight superposition.

**Self-Weight Superposition Verification Summary**: The tether cable cross-sectional area must be re-determined based on the total tension at the upper end after self-weight superposition, on top of the original tethering requirement. In the optimistic option, the cross-sectional area needs to increase from 30 mm² to approximately 32.2 mm² (increase of approximately 7%); the increase is larger for the conservative and commercial options. Sections 1.5(d) and 1.5(f) for cable diameter derivation and linear density and total mass tables have been updated with the corrected cross-sectional areas after self-weight superposition.

**(d) Tether Cable Diameter and Safety Factor**

CNT braided cable is used as the tether cable material.

| Parameter | Symbol | Value | Source |
|:---|:---|:---|:---|
| CNT braided cable engineering strength | $\sigma_{\text{CNT}}$ | 20 GPa | Main Volume 2, Section 2.3.4 (optimistic value, engineering target) |
| CNT braided cable density | $\rho_{\text{CNT}}$ | 1,300 kg/m³ | Main Volume 2, Section 2.2.2 (approximately 1.3 g/cm³) |
| Safety factor | $S$ | 3.0 | Tether cable operating conditions (irregular wind loads + long-term creep risk + instantaneous gust uncertainty) |
| Allowable stress | $\sigma_{\text{allow}}$ | $\sigma_{\text{CNT}}/S \approx 6.67 \text{ GPa}$ | — |

**Single cable required cross-sectional area** (optimistic option, based on total upper end tension 214.7 kN after self-weight superposition, safety factor 3.0):

$$
A_{\text{single}} = \frac{T_{\text{upper}} \times S}{\sigma_{\text{CNT}}} = \frac{214{,}700 \times 3.0}{20 \times 10^9} \approx 3.22 \times 10^{-5} \text{ m}^2 = 32.2 \text{ mm}^2
$$

$$
d_{\text{single}} = \sqrt{\frac{4 \times A_{\text{single}}}{\pi}} = \sqrt{\frac{4 \times 3.22 \times 10^{-5}}{\pi}} \approx 6.40 \times 10^{-3} \text{ m} \approx 6.4 \text{ mm}
$$

If the conservative value ($\sigma_{\text{CNT}} = 4.5 \text{ GPa}$) is used, based on total upper end tension 254.0 kN after self-weight superposition, the single cable cross-sectional area needs to be approximately 169 mm², diameter approximately 14.7 mm; at the current commercial CNT level ($\sigma_{\text{CNT}} = 3 \text{ GPa}$), based on total upper end tension 280.9 kN after self-weight superposition, the single cable cross-sectional area needs to be approximately 281 mm², diameter approximately 18.9 mm.

**(e) Tri-Functional Cable Cross-Section Structure and Linear Density**

Once CNT materials are mature, the same cable can simultaneously serve the three functions of tethering tension, power supply, and communication. The cross-section structure of the tri-functional cable from inside to outside is: CNT load-bearing and conductive layer (core) → UHMWPE insulation layer → optical fiber (embedded in the insulation layer) → UHMWPE outer jacket.

**(1) CNT Conductive Layer Cross-Sectional Area**

The CNT conductive layer cross-sectional area is determined by the tethering requirement — taking the self-weight superposition corrected 32.2 mm² (optimistic option). This cross-sectional area also meets power supply requirements: with the platform peak power of 7,290 kW (30 m/s wind condition), transmission voltage ±100 kV DC, single pole transmission power approximately 3,645 kW, and 25 km cable length, the single pole current is approximately 36.5 A. Taking CNT resistivity equal to copper (1.68×10⁻⁸ Ω·m), single cable resistance approximately 13.0 Ω, transmission loss approximately 17.3 kW, efficiency approximately 99.8%. The tethering requirement fully covers the power supply requirement; no need to increase cross-sectional area separately for power supply.

**(2) UHMWPE Insulation Layer Thickness**

The insulation layer must withstand ±100 kV DC voltage. UHMWPE dielectric strength is approximately 20–30 kV/mm; taking the conservative value of 20 kV/mm, the required insulation thickness is approximately 5 mm. Including the outer jacket (approximately 1 mm), total UHMWPE thickness is approximately 6 mm. The cable outer diameter increases from pure CNT's 6.4 mm to approximately 18.4 mm.

**(3) Optical Fiber Specification**

Single-mode radiation-resistant optical fiber (G.652 or G.657), diameter approximately 0.25 mm, outer diameter approximately 0.9 mm including buffer layer, embedded in the UHMWPE insulation layer; linear density negligible.

**(4) Tri-Functional Cable Linear Density**

Total linear density of tri-functional cable = CNT 0.042 kg/m + UHMWPE insulation and jacket approximately 0.03 kg/m (total thickness 6 mm, UHMWPE density approximately 930 kg/m³, annular cross-sectional area approximately 370 mm² at outer diameter 18.4 mm) ≈ 0.072 kg/m. Optical fiber linear density negligible. 25 km single cable mass approximately 1,800 kg, four cable total mass approximately 7,200 kg.

**(f) Cable Linear Density and Total Mass Comparison**

| Parameter | Pure Tether Option (CNT+UHMWPE, optimistic) | Tri-Functional Option (tether+power+communication, optimistic) |
|:---|:---:|:---:|
| CNT cross-sectional area (after self-weight superposition correction) | 32.2 mm² | 32.2 mm² |
| Cable diameter | approximately 6.4 mm (approximately 7.0 mm including UHMWPE jacket) | approximately 18.4 mm (including 6 mm UHMWPE insulation layer) |
| Total linear density | ≈0.065 kg/m | ≈0.072 kg/m |
| 25 km single cable mass | ≈1,625 kg | ≈1,800 kg |
| Four cables 25 km total mass | ≈6,500 kg | ≈7,200 kg |
| Function | Tethering only | Tether + power supply + communication tri-functional |

Compared to the pure tether option, the tri-functional option increases the four-cable total mass by only approximately 700 kg (an increase of approximately 11%), in exchange for eliminating independently installed copper power supply conductors (25 km single cable copper conductor mass approximately 4,450 kg, see Volume 2, Section 2.4(e), Path 3). The tri-functional option's total mass of 7,200 kg is outside the bearing range of the airship's 5,000 kg design lift, but is approaching the airship's near-to-mid-term feasible mass upper limit (11,000 kg).

**(g) Platform End Installation Scheme**

The connection of the tri-functional cable at the aerostat end is divided into three independent channels: mechanical attachment (load-bearing connection), electrical connection (power interface), and fiber optic interface (communication interface).

**(1) Mechanical Attachment (Load-Bearing Connection)**

After the cable CNT load-bearing layer enters the bottom of the aerostat, it transfers the tension to the main load-bearing frame inside the airship through a tapered anchor fitting. The anchor fitting uses a CNT cable self-braided loop + high-strength aluminum alloy tapered sleeve structure — the cable is split into multiple strands of dispersed loops inside the sleeve, cured with epoxy resin filling, converting the axial cable tension into radial pressure between the sleeve and the cable, achieving damage-free clamping. The anchor fitting design allowable load is ≥300 kN (greater than the single cable upper end total tension of 214.7 kN, safety factor approximately 1.4, working in division with the cable body safety factor of 3.0 — the anchor fitting only needs to withstand static load, without the need to consider wind load uncertainty and long-term creep).

**(2) Electrical Connection (Power Interface)**

After the cable enters the aerostat, the UHMWPE insulation layer is stripped approximately 2 m downstream of the anchor fitting to expose the CNT conductive layer. Current is drawn out through multiple parallel conductors (8–12 conductors, single conductor cross-sectional area 3–4 mm², total cross-sectional area ≥32.2 mm², consistent with the CNT conductive layer). The conductor material is silver-plated copper (electrochemically compatible with the CNT conductive layer, avoiding contact corrosion), fixedly routed inside the aerostat and not subject to cable tension fluctuations. The routing paths of the multiple parallel conductors are independent; if a single one fails, the remaining conductors can still carry all current.

The multiple parallel conductors connect to the primary side of the main transformer. The main transformer is a SiC solid-state DC transformer, stepping down ±100 kV DC to ±10 kV DC (rated power ≥7,500 kW, efficiency ≥98%, mass approximately 500 kg [25]). The stepped-down ±10 kV DC connects to the ring bus inside the aerostat. Three secondary transformers (solid-state, SiC devices) take power from the ±10 kV DC bus and step down to the voltage levels required by each device:

| Secondary Transformer | Output Voltage | Power Bus | Powered Equipment |
|:---|:---|:---|:---|
| Secondary transformer 1 | 690V AC | Propulsion and industrial bus | Four electric propellers, winch |
| Secondary transformer 2 | 400V AC | Utilities and communication bus | Communication system, thermal control circulation pump, helium management system compressor |
| Secondary transformer 3 | Low-voltage DC (24V/48V) | Control and instrumentation bus | Control system, sensors, navigation and positioning system |

The three secondary transformers have a combined mass of approximately 200 kg and efficiency ≥98% each.

The drawn conductors are re-wrapped with UHMWPE insulating conduits at the stripped section, ensuring electrical isolation from the internal structure of the aerostat. The primary and secondary sides of the main transformer and all secondary transformers are equipped with three-level protection of anti-reverse diode + remote-controlled DC circuit breaker + manual isolation switch [26].

**(3) Fiber Optic Interface (Communication Interface)**

After the optical fiber is stripped downstream of the anchor fitting, it connects to the photoelectric converter in the aerostat's communication equipment bay. The optical fiber is protected by stainless steel armored flexible conduit at the stripped section, with bending radius ≥50 mm. The photoelectric converter is installed in a Faraday cage and isolated from external cables by surge protectors.

**(h) Ground Winch and Tension Compensation Mechanism**

The winch system at the ground anchor station is responsible for tension compensation, paying out, and storage of the tether cable. The winch adopts a **shaft-motor separated** design — the motor does not directly connect to the winch drum shaft, but drives it through an insulating gear set engagement. The pinion on the motor output shaft drives the bull gear on the winch drum shaft, with a gear ratio of 3:1 to 5:1, amplifying torque. The gear material is UHMWPE or ceramic matrix composite (insulating, wear-resistant, self-lubricating [27]), ensuring that the winch drum shaft and the CNT cable on it are completely electrically isolated from the motor and control system. The shaft-motor separated design allows a smaller and lighter motor to drive the winch.

The winch tension control system must ensure that the cable remains taut throughout and is not overloaded. The tension compensation stroke must cover all of the following factors: cable elastic elongation (elastic elongation of a 25 km CNT cable under maximum load — calculated based on CNT elastic modulus 1,000 GPa, single cable upper end total tension 214.7 kN, average tension approximately 107.4 kN, approximately 8.4 m), thermal expansion and contraction (temperature difference ±10°C, CNT coefficient of thermal expansion approximately 2×10⁻⁶/K, thermal expansion and contraction range of 25 km cable approximately ±0.5 m), and long-term creep (conservative estimate approximately 0.5 m). Total required winch compensation stroke approximately 10 m. Design stroke ≥15 m (50% margin).

**(i) Insulating Transition Section and Coil Effect Elimination**

When the CNT cable wound on a metal drum shaft is energized, it constitutes a huge solenoid coil — 25 km of cable wound in multiple turns on the drum shaft generates a strong magnetic field when energized, with the magnetic core (metal drum shaft) amplifying the magnetic field strength, and the inductance impeding rapid adjustment of the power supply current. To physically eliminate this coil effect, an insulating transition section is provided between the winch and the cable.

The insulating transition section is approximately 15 m long (matching the winch compensation stroke), with the cable passing through this section without winding, in a straight line. At the end of the transition section, an insulating flange is provided — the flange body is made of high-strength aluminum alloy, and the flange face is completely electrically isolated from the winch-side metal components by UHMWPE insulating pads. The insulating flange bears all mechanical tension transfer between the transition section and the winch.

The current path is: ground power grid → fixed cable → carbon brush or copper alloy slip ring (sliding contact with the CNT conductive layer at the end of the transition section) → CNT conductive layer (platform direction section) → platform. The winch drum shaft and the cable wound on it only bear mechanical tension and do not participate in any electrical circuit, physically eliminating the coil effect. The contact resistance at the sliding contact point is in the milliohm range, with virtually no additional loss during normal operation. The contact point is equipped with a UHMWPE insulating shield and surge protector, covering induced overvoltage during lightning strikes.

**(j) Anchoring and Cable Configuration**

The ground anchor station is located in a flat area near the equator with suitable natural conditions. Multiple tether cables (≥3) are anchored to the ground at evenly spaced angles. The cables are wound on automatic winches at the ground anchor station. The ground station draws current from the CNT conductive layer of the cable at the sliding contact point at the end of the insulating transition section and connects to the ground power grid; it connects to the global communication network through the fiber optic interface.


### 1.6 Anchor-Free Pure-Propulsion Position-Keeping Scheme

If the stratospheric platform does not rely on ground anchoring and maintains positional stability entirely by its own propulsion system, the required technical conditions depend on the precision requirements of position-keeping. The following separately assesses three precision levels.

**(a) Stratospheric Wind Field Energy Analysis**

The stratospheric wind field is dominated by horizontal motion, and the main force the airship needs to overcome for position-keeping is horizontal wind drag. Wind drag power is given by:

$$
P_{\text{drag}} = F_{\text{horizontal}} \times v_{\text{wind}} = \frac{1}{2} \times \rho_{\text{air}} \times v_{\text{wind}}^3 \times A_{\text{proj}} \times C_d
$$

At 30 km altitude, $\rho_{\text{air}} \approx 0.018 \text{ kg/m}^3$, airship side area approximately 4,500 m², drag coefficient $C_d \approx 0.05$ [1]. The airship's propulsion system (electric propellers) needs to provide thrust equal and opposite to the wind drag to maintain positional stability. Propeller total efficiency $\eta_{\text{thrust}}$ is taken as 0.75 (including motor efficiency and blade aerodynamic losses [15][16]), and the required electrical power is:

$$
P_{\text{elec}} = \frac{P_{\text{drag}}}{\eta_{\text{thrust}}} = \frac{\frac{1}{2} \times \rho_{\text{air}} \times v_{\text{wind}}^3 \times A_{\text{proj}} \times C_d}{0.75}
$$

Substituting the 30 km altitude parameters:

$$
P_{\text{drag}} = 0.5 \times 0.018 \times v_{\text{wind}}^3 \times 4{,}500 \times 0.05 = 2.025 \times 10^{-3} \times v_{\text{wind}}^3 \text{ (kW, when } v_{\text{wind}} \text{ is in m/s)}
$$

$$
P_{\text{elec}} = \frac{2.025 \times 10^{-3} \times v_{\text{wind}}^3}{0.75} = 2.70 \times 10^{-3} \times v_{\text{wind}}^3 \text{ (kW)}
$$

| Wind Speed $v_{\text{wind}}$ (m/s) | $v_{\text{wind}}^3$ (m³/s³) | Wind Drag $F_{\text{horizontal}}$ (kN) | Wind Drag Power $P_{\text{drag}}$ (kW) | Electrical Power $P_{\text{elec}}$ (kW) |
|:---:|:---:|:---:|:---:|:---:|
| 10 | 1,000 | 20.3 | 202.5 | **270** |
| 20 | 8,000 | 81.0 | 1,620 | **2,160** |
| 30 | 27,000 | 182.3 | 5,468 | **7,290** |
| 40 | 64,000 | 324.0 | 12,960 | **17,280** |
| 50 | 125,000 | 506.3 | 25,313 | **33,750** |

> Note: This power is used for propellers to generate horizontal thrust to counteract wind drag, which is a different physical requirement and power budget from the propeller auxiliary lift scheme in Section 1.3(e) (vertical thrust, used to supplement the aerostatic buoyancy deficit) — the two must not be confused or superimposed. Vertical auxiliary lift is a short-term emergency measure (≥40 km altitude); horizontal position-keeping is a routine operational measure (full altitude). Both share the same propulsion system but are time-multiplexed.

**(b) Position-Keeping Requirements for Three Precision Levels**

**Precision Level A: Precise Hovering (deviation ≤100 m)**. At 20 m/s wind speed, the required electrical power is approximately 2,160 kW. With photovoltaic peak power approximately 5,200 kW (photovoltaic area 8,500 m², AM0 1,361 W/m², efficiency 45%), the airship can use photovoltaic self-supply to achieve precise hovering at wind speeds below 20 m/s; above 30 m/s wind speed, the required electrical power already exceeds the photovoltaic peak power, and positional drift must be accepted.

**Precision Level B: Allowing 5 km Drift**. At 10 m/s wind speed, the electrical power is only approximately 270 kW, far below the photovoltaic peak power. The time for 5 km drift at 30 m/s high wind speed is given by:

$$
t_{\text{drift}} = \frac{\Delta x_{\text{max}}}{v_{\text{wind}}} = \frac{5{,}000 \text{ m}}{30 \text{ m/s}} \approx 167 \text{ s} \approx 2.8 \text{ min}
$$

The 2.8-minute drift window is far shorter than the full-power discharge time of the energy storage system (with a 400 kg lithium-ion battery pack, 100 kWh capacity, 250 Wh/kg energy density, at 7,290 kW power the discharge time is approximately 49 seconds), so intermittent corrections with propellers during drift periods are needed. The correction strategy is a cycle of drift → short-duration powered correction → drift → correction, with average energy consumption far below Precision Level A. This precision is fully acceptable for the vast majority of missions such as communication relay, atmospheric science observation, etc. — a 5 km drift represents only 1% of the platform coverage radius (approximately 500 km).

**Precision Level C: Allowing 10 km Drift**. At 10 m/s wind speed, drifting 10 km takes approximately 1,000 s (approximately 17 min); the airship can passively manage position with extremely low propulsion power over a drift cycle of several days, initiating a single brief correction (approximately 10–20 min of propulsion) when cumulative drift exceeds 10 km, with the propulsion system sleeping the rest of the time.

**(c) Summary of Technical Requirements for Different Precision Levels**

| Precision Level | Maximum Allowable Drift | Position-Keeping Method | Applicable Wind Conditions | Main Energy Consumption | Applicable Missions |
|:---:|:---:|:---|:---:|:---|:---|
| **A (Precise)** | ≤100 m | Real-time propulsion counteraction | ≤20 m/s | Very high (continuously counteracting wind drag) | Laser communication pointing, precision optical observation |
| **B (Moderate)** | ≤5 km | Intermittent correction | All wind conditions | Low (correction only when drift limit is exceeded) | Communication relay, atmospheric science observation, disaster prevention early warning |
| **C (Relaxed)** | ≤10 km | Passive drift + periodic correction | All wind conditions | Very low (correction once every few days) | Material exposure experiments, long-term climate monitoring, passive remote sensing |

**(d) Engineering Feasibility Conclusion**

Long-term position-keeping by an airship entirely by its own propulsion under anchor-free conditions is physically and engineering-wise feasible. Precision Level B (5 km drift) is the recommended scheme for the independent deployment phase — it can meet the vast majority of mission requirements except for precision optical observation, and the energy requirements can be fully covered by photovoltaic self-supply.


### 1.7 Parameter Output

| Parameter | Value | Status | Receiving Volume |
|:---|:---|:---|:---|
| Aerostat type | Single-hull stratospheric airship (with interface reserved for twin-hull configuration in the long term) | Design baseline | — |
| Aerostat permanent station-keeping altitude range | 25–35 km | Design baseline | Volume 4, Volume 6 |
| Aerostat maximum reachable altitude (aerostatic buoyancy only) | 50 km (volume approximately 5,640,000 m³, essentially infeasible) | Physical upper limit | — |
| Aerostat design total mass | 5,000 kg | Design baseline | Volume 2 |
| Design margin | 15% (lift system designed for 5,750 kg) | Design baseline | — |
| Aerostat engineering feasible mass upper limit | ≈5,000 kg (current conservative) / ≈11,000 kg (near-to-mid-term) / ≈25,000 kg (long-term optimistic) | Design baseline | Volume 2 |
| Aerostat hull volume | ≈67,600 m³ (20 km) / ≈333,700 m³ (30 km) | Design baseline | — |
| Aerostat envelope areal density | ≤200 g/m² (research grade has reached 103–113 g/m² [12]) | Design target | Volume 4 |
| Aerostat envelope service life | ≥5 years (inspection every 6 months) | Design target | Volume 8 |
| Helium annual leakage rate | ≤5% | Design target | — |
| RFC-assisted endurance extension | 25.5%–118.2 days (based on modeling results from Stratobus design [10]) | External research reference | Volume 2 |
| Electric propeller auxiliary lift scheme | Four ø5–8 m variable-pitch propellers, only activated for short-term missions at 40–50 km | Assessment conclusion | Volume 2 |
| Propeller auxiliary lift total power | 4–6.3 MW (50 km altitude, four ø5–8 m propellers) | Order-of-magnitude estimate | Volume 2 |
| Twin-hull configuration wind drag (30 m/s wind condition) | Approximately 162 kN (approximately 22% less than single hull) | Assessment conclusion | — |
| Design baseline wind condition | 50 m/s (30-minute average wind speed, instantaneous gust approximately 60–75 m/s) | Design baseline | — |
| Cable safety factor | 3.0 (covers uncertainty of instantaneous gusts) | Design baseline | — |
| Single cable design tension (external load component) | ≈200 kN (four-cable scheme, excluding self-weight) | Design baseline | Volume 10 |
| Single cable self-weight (25 km optimistic option) | ≈14.7 kN (linear density 0.06 kg/m) | Design baseline | — |
| Single cable upper end total tension (including self-weight) | ≈214.7 kN (optimistic option) | Design baseline | — |
| Single cable cross-sectional area (optimistic, after self-weight superposition correction) | 32.2 mm² | Design baseline | — |
| Single cable diameter (optimistic/conservative/commercial, after self-weight superposition correction) | 6.4/14.7/18.9 mm | Design baseline | — |
| Tri-functional cable total linear density (optimistic) | ≈0.072 kg/m | Design baseline | — |
| Tri-functional cable outer diameter (including 6 mm UHMWPE insulation layer) | ≈18.4 mm | Design baseline | — |
| Tri-functional four cables 25 km total mass (optimistic) | ≈7,200 kg | Order-of-magnitude estimate | Volume 2 |
| CNT power supply voltage | ±100 kV DC | Design baseline | — |
| Power transmission efficiency (25 km cable length) | ≈99.8% | Design baseline | — |
| Optical fiber specification | Single-mode radiation-resistant (G.652/G.657), outer diameter approximately 0.9 mm | Design baseline | — |
| Number of drawn conductors and single conductor cross-sectional area | 8–12 conductors, single 3–4 mm², total ≥32.2 mm² | Design baseline | — |
| Main transformer | SiC solid-state, ±100 kV/±10 kV DC, ≥7,500 kW, ≈500 kg | Design baseline | Volume 2 |
| Platform distribution bus | 690V AC (propulsion/industrial) + 400V AC (utilities/communication) + low-voltage DC | Design baseline | — |
| Ground winch scheme | Shaft-motor separated (UHMWPE/ceramic gear set, gear ratio 3:1–5:1) | Design baseline | — |
| Winch compensation stroke | ≥15 m (covers elastic elongation 8.4 m + thermal expansion ±0.5 m + creep 0.5 m, 50% margin) | Design baseline | — |
| Insulating transition section length | ≥15 m (matching compensation stroke) | Design baseline | — |
| Transition section electrical isolation | Insulating flange (UHMWPE pads) + carbon brush/copper alloy slip ring | Design baseline | — |
| Four cables 25 km total mass (optimistic/conservative/commercial, after self-weight superposition correction) | ≈6,500/27,000/44,000 kg | Order-of-magnitude estimate | Volume 2 |
| **Tether cable mass feasibility** | **Only valid when CNT engineering strength ≥20 GPa** | **Core constraint** | Volume 2 |
| Anchor-free position-keeping recommended precision | Precision Level B (≤5 km drift) | Design baseline | — |
| Precision B maximum electrical power (30 m/s wind speed) | Approximately 7,290 kW (intermittent correction is acceptable) | Order-of-magnitude estimate | Volume 2 |
| Work gondola drive method | Aerostat-mounted electric winch + gondola movable pulley block | Design baseline | Volume 3 |
| Work gondola total mass (unloaded) | ≤500 kg | Design baseline | Volume 3 |
| Work gondola payload | ≥300 kg | Design baseline | Volume 3 |
| Work gondola maximum ascent/descent speed | 2 m/s (winch cable speed 4 m/s, movable pulley halved) | Design baseline | Volume 3 |
| Winch power | Approximately 25 kW (peak) | Design baseline | Volume 2 |
| Gondola stabilization mechanism | Passive aerodynamic fins (primary) + low center of gravity self-alignment + multi-cable guying + active damping flywheel (backup) | Design baseline | Volume 3 |
| Photovoltaic peak power | ≈5,200 kW (area 8,500 m², AM0 1,361 W/m², η=45%) | Order-of-magnitude estimate | Volume 2 |


### 1.8 Volume 1 Conclusion

This volume has completed a comprehensive demonstration of the overall design of the stratospheric platform, establishing the dual-layer architecture of the aerostat (stratospheric airship) and work gondola (winch + movable pulley drive). Core conclusions:

1. **30 km altitude station-keeping is the currently technically achievable balance point for the aerostat**. A 333,700 m³ hull volume (ø35 m × 152 m) is achievable with current envelope material technology, and a 5,000 kg design total mass covers all fixed loads of the platform. The 15% design margin ensures the platform can still operate safely under adverse conditions such as envelope degradation and local wind field exceedances.

2. **The airship mass upper limit is defined by three constraints: envelope, stiffness, and leakage rate**. At the current conservative technology level (envelope 200 g/m², hull length 150 m), the feasible mass upper limit is approximately 5,000 kg; near-to-mid-term (envelope 150 g/m², hull length 200 m) it can be raised to 11,000 kg, and long-term (envelope 100 g/m², hull length 250 m) it can reach 25,000 kg. The twin-hull airship configuration has significant advantages in platform space and upwind stability in long-term large-mass scenarios, and should be considered during future capacity expansion.

3. **The tri-functional cable scheme achieves functional integration of tethering, power supply, and communication**. After self-weight superposition correction, the CNT conductive layer cross-sectional area of 32.2 mm² (optimistic option) can simultaneously meet tethering tension and power transmission requirements (±100 kV DC, efficiency approximately 99.8%). The tri-functional scheme's four-cable total mass is approximately 7,200 kg, only approximately 700 kg more than the pure tether scheme (an increase of approximately 11%). The tri-functional cable connects at the platform end through three independent channels: tapered anchor fitting (mechanical), multiple parallel conductor connections (electrical), and stainless steel armored flexible conduit-protected optical fiber (communication); at the ground end, the coil effect is eliminated through the shaft-motor separated winch and insulating transition section. The mass feasibility of the tether cable scheme is highly dependent on a breakthrough in CNT engineering strength — only when CNT braided cable reaches the 20 GPa target strength does the total cable mass after self-weight superposition fall within the bearing range of the airship's lift.

4. **The work gondola's winch + movable pulley scheme is superior to the rack-and-pinion scheme**. Drive and braking equipment is concentrated inside the aerostat, greatly reducing the gondola structural mass (500 kg unloaded), and increasing the payload ratio (≥300 kg). The four-stage stabilization mechanism (passive aerodynamic fins → low center of gravity → multi-cable guying → active damping) covers the full wind speed range, ensuring the gondola can perform precision operations even under strong wind conditions.

5. **Electric propeller auxiliary lift is a short-term feasible means in the 40–50 km range**, but energy consumption is extremely high (four ø5–8 m propellers require 4–6.3 MW), and it is only suitable for special mission scenarios of no more than 2 hours each. The daily station-keeping and operating altitude of the airship should be maintained within the effective aerostatic buoyancy range of 25–35 km.


### References

[1] Alam, M. I., & Pant, R. S. A rule-based online energy management strategy for long-endurance stratospheric airships. *Aerospace Science and Technology*, 2024: 109266.

[2] Gonzalo, J., Domínguez, D., García-Gutiérrez, A., & Escapa, A. On the development of a parametric aerodynamic model of a stratospheric airship. *Aerospace Science and Technology*, 2020, 107: 106316.

[3] Sceye. Sceye completes 24-hour stratospheric flight using solar+storage. *EEPOWER*, 2024-09-06.

[4] Zhao Panfeng, Liu Chuanchao. Overall parameter estimation of stratospheric airship. *Aeronautical Science and Technology*, 2006(5): 37-39.

[5] Persistent Monitoring Platforms Final Report. *UNT Digital Library*, 2016-09-22.

[6] Yang, J., Wang, X., Shen, L., & Chen, D. Availability analysis of GNSS signals above GNSSs constellation. *The Journal of Navigation*, 2020.

[7] Fraunhofer Institute. FluxCrawler: Robots inspect cables. *Fraunhofer Research News*, 2013-07.

[8] Hu, X., Zhang, L., Zhang, W., Lui, P., & Pang, X. Developing a climbing robot for stay cable maintenance with security and rescue mechanisms. *Journal of Field Robotics*, 2025, 42(6): 2532-2548.

[9] Preston, B. Reclaiming Elevator Power. *Elevator World*, 2023-08-22.

[10] Extending the flight endurance of stratospheric airships using regenerative fuel cells-assisted pressure maintenance. *Renewable Energy*, 2024, 227: 120470.

[11] CNIM designs and validates the rotation system that will enable the Stratobus airship to operate autonomously for up to one year. *Airframer*, 2019-06-05.

[12] Ultra-lightweight fiber-reinforced envelope material for high-altitude airship. *Journal of the Textile Institute*, 2022, 113(9).

[13] Mechanical and Gas Barrier Properties of Naturally and Artificially Weathered High-Performance Fiber Reinforced Laminated Structures for Stratospheric Airship Envelope. *KCI*, 2025-08-04.

[14] Stratospheric pseudo-satellites nearing commercial role in hybrid space networks. *SpaceNews*, 2025-09-18.

[15] Mira Aerospace completes HAPS test flight in Rwanda. *SDxCentral*, 2026-03-02.

[16] From Specialty Fibers to Sensor Systems: Engineering Optical Sensing for the Most Demanding Applications. *Photonics.com*, 2026-04-01.

[17] Zhang, L., Lv, M., Meng, J., & Du, H. Optimization of solar-powered hybrid airship conceptual design. *Aerospace Science and Technology*, 2017.

[18] Design and Analysis of a New Bionic Airship with Combined Floatation. *IEEE*, 2024-01-08.

[19] NASA. AeroPod: A Passive Aerodynamic Stabilizer for Tethered Payloads. 2020.

[20] Influence of processing and external storage conditions on the performance of envelope materials for stratospheric airships. *Advances in Space Research*, 2021, 67(1): 571-582.

[21] Research on Environmental Adaptability of Stratospheric Airship Materials. *Springer*, 2024-09-29.

[22] Gear Racks for Rack Railways: Precision Drive Systems That Conquer Britain's Steepest Gradients. *Ever Power*, 2026-03-11.

[23] Application of sliding power transmission technology on steel cables. *Journal World*.

[24] A universal tethering scheme for tethered balloons. *Chinese Patent*, 2020-06-17.

[25] She, X., Huang, A. Q., & Burgos, R. Review of solid-state transformer technologies and their application in power distribution systems. *IEEE Journal of Emerging and Selected Topics in Power Electronics*, 2013, 1(3): 186-198.

[26] IEEE. *IEEE Std 242-2001 – IEEE Recommended Practice for Protection and Coordination of Industrial and Commercial Power Systems*. 2001.

[27] Kurtz, S. M. *UHMWPE Biomaterials Handbook*, 3rd ed. William Andrew, 2015.

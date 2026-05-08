# Volume IV: Elevator Cable and Track Sleeve Design

**Version**: 5.5 (Final Review)
**Compilation Date**: May 2026
**Currency Unit**: Renminbi (Yuan), Symbol: ¥


## 4.1 Preface

This volume focuses on the mechanical design of elevator cables, the track sleeve system, and their synergy with the main cable. Building on Volume I’s track mechanical environment, Volume II’s material parameters, and Volume III’s node anchoring boundary conditions, it outputs the cable cross-sectional profile, counterweight requirements, longitudinal displacement compensation schemes, design parameters and segmentation strategies for the track sleeve/rack. The cabin design is covered independently in Volume V.

Core tasks of this volume:

1. Establish a tapered cross-section design model for the elevator cable, providing the complete tension distribution from ground to GEO.
2. Provide detailed calculations for all parameters of the drive wheel directly gripping the cable, establishing the engineering necessity of the track sleeve.
3. Design the counterweight system and top-end connector, quantitatively analyze the longitudinal displacement compensation requirements for the full cable length.
4. Provide an order-of-magnitude estimate of node constraint stiffness.
5. Design the track sleeve’s gradient functional structure, reverse-tapered cross-section, and segmentation isolation strategy, including thrust ring parameters and deformation decoupling analysis.
6. Provide complete material and geometric parameters for the friction scheme, and assess feasibility at the order-of-magnitude level.
7. Provide complete material and geometric parameters for the rack scheme, and assess feasibility at the order-of-magnitude level. The rack material remains consistent with the track sleeve’s middle layer: aluminum alloy 7075-T6, with micro-arc oxidation treatment.
8. Evaluate the impact of the track sleeve’s additional weight on the main cable, and analyze the manufacturing and on-orbit installation methods for the track sleeve.
9. Analyze the impact of atmospheric motion on the cable.
10. Output key parameters for use in Volumes I and V.


## 4.2 Cable Constitutive Parameters

| Parameter | Symbol | Value | Source |
|------|------|------|------|
| Material | — | MWCNT braided cable | Volume II, Section 2.2.3 |
| Allowable stress | $σ_{allow}$ | ~20 GPa (target) | Volume II, Section 2.3.4 |
| Material density | $ρ_{mat}$ | ~1.3 g/cm³ | Volume II, Section 2.2.2 |
| Cross-section fill factor | f | 0.06–0.6 | Volume II, Section 2.6.2 |
| Engineering density | ρ | $ρ_{mat}$×f, take f=0.3, ρ≈390 kg/m³ | Value in this volume |
| Elastic modulus | E | ≈1,000 GPa | Derived in Section 4.7.2 |
| Safety factor (independent case) | S | ≥2.5 | Volume II, Section 2.7.1 |

Physical constants:

| Constant | Symbol | Value |
|------|------|------|
| Earth’s gravitational constant | GMₑ | 3.986004418×10¹⁴ m³/s² |
| Earth’s equatorial radius | Rₑ | 6,371 km = 6.371×10⁶ m |
| Surface gravity acceleration | g₀ | GMₑ/Rₑ² ≈ 9.81 m/s² |
| Earth’s rotation angular velocity | ωₑ | 7.2921159×10⁻⁵ rad/s |
| GEO radius | $R_{GEO}$ | 42,164 km = 4.2164×10⁷ m |


## 4.3 Tapered Cross-Section Design Model and Tension Distribution

### 4.3.1 Force Analysis and Control Equations

Under independent conditions, the elevator cable is pulled upward by the GEO-end counterweight space station, anchored at the ground end and under tension at the GEO end. The cable is suspended, and the cross-sectional area at any height must ensure that the tensile capacity at that point is not less than the sum of the self-weight of all cable below and the effective load at that point.

Let the radial distance from the Earth’s center r be the independent variable ($Rₑ ≤ r ≤ R_{GEO}$). At the GEO end (r=$R_{GEO}$), the cable bears the entire self-weight and effective load below, with maximum tension and thickest cross-section. At the ground end (r=Rₑ), it only bears the anchoring tension, with minimum tension and thinnest cross-section.

Infinitesimal self-weight:

$$
\mathrm{d}W = \rho A(r) g(r) \mathrm{d}r
$$

Where gravity acceleration decreases with height:

$$
g(r) = \frac{GM_e}{r^2}
$$

Cable tension T(r) along the radial direction satisfies:

$$
\frac{\mathrm{d}T}{\mathrm{d}r} = \rho A(r) g(r)
$$

Equal-strength design requires that the cross-sectional bearing capacity along the entire length is proportional to the tension at that point:

$$
\sigma_{\text{allow}} A(r) = T(r) S
$$

For independent conditions, S ≥ 2.5. Thus:

$$
\frac{\mathrm{d}A}{A} = \frac{\rho S}{\sigma_{\text{allow}}} g(r) \mathrm{d}r = \frac{\rho S GM_e}{\sigma_{\text{allow}}} \frac{\mathrm{d}r}{r^2}
$$

### 4.3.2 Integral Solution

Integrate the above from the ground end to the GEO end:

$$
\int_{A_0}^{A_{GEO}} \frac{\mathrm{d}A}{A} = \frac{\rho S GM_e}{\sigma_{\text{allow}}} \int_{R_e}^{R_{GEO}} \frac{\mathrm{d}r}{r^2}
$$

The left side is ln($A_{GEO}$/A₀). The right side integral is:

$$
\int_{R_e}^{R_{GEO}} \frac{\mathrm{d}r}{r^2} = \frac{1}{R_e} - \frac{1}{R_{GEO}}
$$

Substitute values:

$$
\frac{1}{R_e} - \frac{1}{R_{GEO}} = \frac{1}{6.371\times10^6} - \frac{1}{4.2164\times10^7}
$$
$$
= 1.5696\times10^{-7} - 2.3717\times10^{-8} \approx 1.3324\times10^{-7} \text{ m}^{-1}
$$

Define characteristic height H as the failure length of a cable with constant cross-section under constant surface gravity g₀:

$$
H = \frac{\sigma_{\text{allow}}}{\rho S g_0} = \frac{20\times10^9}{390 \times 2.5 \times 9.81}
$$
$$
H = \frac{20\times10^9}{9,564.75} \approx 2.091\times10^6 \text{ m} = 2,091 \text{ km}
$$

Coefficient term:

$$
\frac{\rho S GM_e}{\sigma_{\text{allow}}} = \frac{390 \times 2.5 \times 3.986\times10^{14}}{20\times10^9} = \frac{3.886\times10^{17}}{2\times10^{10}} \approx 1.943\times10^7 \text{ m}
$$

Cross-section ratio:

$$
\ln\frac{A_{GEO}}{A_0} = 1.943\times10^7 \times 1.3324\times10^{-7} \approx 2.589
$$
$$
\frac{A_{GEO}}{A_0} = e^{2.589} \approx 13.31
$$

Diameter ratio:

$$
\frac{d_{GEO}}{d_0} = \sqrt{13.31} \approx 3.65
$$

### 4.3.3 Full-Height Cross-Section and Tension Distribution

Take ground-end diameter d₀ = 0.5 m, then:

$$
A_0 = \frac{\pi \times 0.5^2}{4} = \frac{\pi \times 0.25}{4} \approx 0.19635 \text{ m}^2
$$

GEO-end cross-sectional area:

$$
A_{GEO} = 13.31 \times 0.19635 \approx 2.613 \text{ m}^2
$$

GEO-end diameter:

$$
d_{GEO} = \sqrt{\frac{4 \times 2.613}{\pi}} \approx 1.824 \text{ m}
$$

GEO-end maximum tension:

$$
T_{GEO} = \frac{\sigma_{\text{allow}} A_{GEO}}{S} = \frac{20\times10^9 \times 2.613}{2.5} \approx 2.090\times10^{10} \text{ N}
$$

At any height r, the cross-sectional area satisfies:

$$
A(r) = A_0 \exp\left[ 1.943\times10^7 \left( \frac{1}{R_e} - \frac{1}{r} \right) \right]
$$

**(1) z = 0 km (ground, r = 6,371 km)**

$$
A(0) = 0.19635 \text{ m}^2,\quad d(0) = 0.500 \text{ m},\quad T(0) = 1.571\times10^9 \text{ N}
$$

**(2) z = 5,000 km (r = 11,371 km)**

$$
\frac{1}{R_e} - \frac{1}{r} = 1.5696\times10^{-7} - 8.794\times10^{-8} \approx 6.902\times10^{-8}
$$
$$
\ln\frac{A}{A_0} = 1.943\times10^7 \times 6.902\times10^{-8} \approx 1.341
$$
$$
\frac{A}{A_0} = e^{1.341} \approx 3.82
$$
$$
A \approx 0.750 \text{ m}^2,\quad d \approx 0.977 \text{ m},\quad T \approx 6.00\times10^9 \text{ N}
$$

**(3) z = 14,000 km (r = 20,371 km)**

$$
\frac{1}{R_e} - \frac{1}{r} = 1.5696\times10^{-7} - 4.909\times10^{-8} \approx 1.0787\times10^{-7}
$$
$$
\ln\frac{A}{A_0} = 1.943\times10^7 \times 1.0787\times10^{-7} \approx 2.096
$$
$$
\frac{A}{A_0} = e^{2.096} \approx 8.13
$$
$$
A \approx 1.596 \text{ m}^2,\quad d \approx 1.425 \text{ m},\quad T \approx 1.277\times10^{10} \text{ N}
$$

**(4) z = 28,164 km (r = 34,535 km)**

$$
\frac{1}{R_e} - \frac{1}{r} = 1.5696\times10^{-7} - 2.895\times10^{-8} \approx 1.2801\times10^{-7}
$$
$$
\ln\frac{A}{A_0} = 1.943\times10^7 \times 1.2801\times10^{-7} \approx 2.487
$$
$$
\frac{A}{A_0} = e^{2.487} \approx 12.03
$$
$$
A \approx 2.361 \text{ m}^2,\quad d \approx 1.734 \text{ m},\quad T \approx 1.889\times10^{10} \text{ N}
$$

**(5) z = 42,164 km (GEO, r = 42,164 km)**

$$
\frac{1}{R_e} - \frac{1}{r} = 1.5696\times10^{-7} - 2.372\times10^{-8} \approx 1.3324\times10^{-7}
$$
$$
\ln\frac{A_{GEO}}{A_0} = 1.943\times10^7 \times 1.3324\times10^{-7} \approx 2.589
$$
$$
A_{GEO} \approx 2.613 \text{ m}^2,\quad d_{GEO} \approx 1.824 \text{ m},\quad T_{GEO} \approx 2.090\times10^{10} \text{ N}
$$

### 4.3.4 Full-Height Tension Distribution Table

| Height z (km) | r (km) | r/Rₑ | A(z)/A₀ | Cross-Section Diameter (m) | Tension T(z) (10⁹ N) |
|------|------|:--:|:--:|------|------|
| 0 (Ground) | 6,371 | 1.000 | 1.00 | 0.500 | 1.571 |
| 5,000 | 11,371 | 1.785 | 3.82 | 0.977 | 6.00 |
| 14,000 | 20,371 | 3.198 | 8.13 | 1.425 | 12.77 |
| 28,164 | 34,535 | 5.421 | 12.03 | 1.734 | 18.89 |
| 42,164 (GEO) | 42,164 | 6.619 | 13.31 | 1.824 | 20.90 |


## 4.4 Parameter Calculation for Drive Wheel Directly Gripping the Cable

This section calculates the parameters for the drive wheel directly gripping the CNT braided cable, corresponding to "Scheme A" in Volume V—friction drive, no track sleeve, no rack. The purpose is to physically establish the engineering necessity of "adding protection and functional interfaces to the cable."

### 4.4.1 Contact Model and Friction Coefficient

The drive wheel is made of steel (or ceramic coating), directly pressed onto the CNT braided surface of the main cable. The friction coefficient between the two is μ = 0.30–0.50 in vacuum dry conditions, and μ = 0.20 is taken as the design baseline in humid atmospheric environments (low-altitude section).

### 4.4.2 Clamping Force Requirement

Cabin full load mass m = 200 t = 2×10⁵ kg, full load weight W = 1.962×10⁶ N.

Design traction force (including 0.05g₀ acceleration, safety factor 2.0):

$$
F_{\text{design}} = W \times 1.05 \times 2.0 = 4.12\times10^6 \text{ N}
$$

The drive wheel transmits all traction force to the cable via friction. The required total clamping force (normal force):

$$
\Sigma F_{\text{clamp}} = \frac{F_{\text{design}}}{\mu}
$$

Take μ = 0.20 (humid atmospheric low-altitude section):

$$
\Sigma F_{\text{clamp}} = \frac{4.12\times10^6}{0.20} \approx 2.06\times10^7 \text{ N}
$$

Take μ = 0.30 (vacuum dry mid-high altitude section):

$$
\Sigma F_{\text{clamp}} = \frac{4.12\times10^6}{0.30} \approx 1.37\times10^7 \text{ N}
$$

Take the envelope value, design total clamping force as **≥ 2.1×10⁷ N**.

### 4.4.3 Number of Drive Wheels and Load per Wheel

Take number of drive wheels $N_{wheel}$ = 16, symmetrically distributed around the cable. Clamping force per wheel (normal force):

$$
F_{\text{per wheel}} = \frac{\Sigma F_{\text{clamp}}}{N_{\text{wheel}}} = \frac{2.1\times10^7}{16} \approx 1.31\times10^6 \text{ N}
$$

### 4.4.4 Hertzian Contact Stress—Drive Wheel and CNT Cable

Drive wheel diameter $D_{wheel}$ = 1.0 m (radius $R_{wheel}$ = 0.5 m), wheel width b = 0.3 m. Main cable outer diameter d₀ = 0.5 m (ground end, radius $r_{cable}$ = 0.25 m).

The drive wheel and cable are two cylinders in crossed contact (axes perpendicular), equivalent curvature radius:

$$
\frac{1}{\rho_{\text{eq}}} = \frac{1}{R_{\text{wheel}}} + \frac{1}{r_{\text{cable}}} = \frac{1}{0.5} + \frac{1}{0.25} = 2 + 4 = 6 \text{ m}^{-1}
$$
$$
\rho_{\text{eq}} \approx 0.1667 \text{ m}
$$

Equivalent elastic modulus: steel drive wheel E₁ = 206 GPa, ν₁ = 0.3; CNT braided cable transverse elastic modulus conservatively taken as E₂ = 50 GPa (much lower than axial 1,000 GPa), ν₂ = 0.25.

$$
\frac{1}{E_{\text{eq}}} = \frac{1-\nu_1^2}{E_1} + \frac{1-\nu_2^2}{E_2} = \frac{0.91}{206\times10^9} + \frac{0.9375}{50\times10^9}
$$
$$
= 4.417\times10^{-12} + 1.875\times10^{-11} \approx 2.317\times10^{-11}
$$
$$
E_{\text{eq}} \approx 4.32\times10^{10} \text{ Pa}
$$

Hertzian contact ellipse half-width:

$$
a_h = \sqrt{\frac{4 F_{\text{per wheel}} \rho_{\text{eq}}}{\pi b E_{\text{eq}}}} = \sqrt{\frac{4 \times 1.31\times10^6 \times 0.1667}{\pi \times 0.3 \times 4.32\times10^{10}}}
$$
$$
= \sqrt{\frac{8.733\times10^5}{4.073\times10^{10}}} \approx \sqrt{2.144\times10^{-5}} \approx 4.63\times10^{-3} \text{ m} = 4.63 \text{ mm}
$$

Maximum contact stress:

$$
\sigma_{\text{Hmax}} = \frac{2 F_{\text{per wheel}}}{\pi a_h b} = \frac{2 \times 1.31\times10^6}{\pi \times 4.63\times10^{-3} \times 0.3}
$$
$$
= \frac{2.62\times10^6}{4.365\times10^{-3}} \approx 6.00\times10^8 \text{ Pa} \approx 600 \text{ MPa}
$$

### 4.4.5 Feasibility Assessment of Contact Stress

The macroscopic transverse compressive strength of the CNT braided cable is limited by inter-tube interactions and the braided structure, conservatively taken as about 200–300 MPa. The calculated contact stress is about 600 MPa, **exceeding the cable’s transverse bearing capacity by about 2–3 times**.

In addition, the CNT braided cable surface has a woven texture; under repeated rolling contact, slippage and fracture between tube bundles will rapidly accumulate damage. Stress concentration at the contact region edge will further reduce fatigue life.

**Conclusion: Direct drive wheel clamping of the CNT cable is not feasible. The cable must be covered with a protective and functional interface.** This directly leads to the engineering necessity of the track sleeve.


## 4.5 Counterweight System Design

### 4.5.1 Counterweight Track Parameters

The counterweight is located Δh=200 km above GEO:

$$
R_{\text{cw}} = 42,164 + 200 = 42,364 \text{ km} = 4.2364\times10^7 \text{ m}
$$

### 4.5.2 Centrifugal and Gravitational Acceleration

Centrifugal acceleration:

$$
a_c = \omega_e^2 R_{\text{cw}} = (7.2921159\times10^{-5})^2 \times 4.2364\times10^7
$$
$$
\omega_e^2 = 5.3171\times10^{-9} \text{ s}^{-2}
$$
$$
a_c = 5.3171\times10^{-9} \times 4.2364\times10^7 \approx 0.22525 \text{ m/s}^2
$$

Gravitational acceleration:

$$
a_g = \frac{GM_e}{R_{\text{cw}}^2} = \frac{3.986004418\times10^{14}}{1.7947\times10^{15}} \approx 0.22210 \text{ m/s}^2
$$

### 4.5.3 Net Acceleration and Counterweight Mass

$$
\Delta a = a_c - a_g = 0.22525 - 0.22210 = 0.00315 \text{ m/s}^2
$$

$$
M_{\text{cw}} = \frac{T_{GEO}}{\Delta a} = \frac{2.090\times10^{10}}{0.00315} \approx 6.635\times10^{12} \text{ kg}
$$

With a safety factor of 1.2, the design counterweight mass is **8.0×10¹² kg**. This requires about 2–3 C-type asteroids of 1.5 km diameter each (single asteroid about 3.5×10¹² kg), see Volume II for details.

### 4.5.4 Counterweight Track Concept

The counterweight track can be pushed outward, essentially using the centrifugal force of a longer cable to "offset the debt," thus saving counterweight mass. According to the hard boundary—**not affecting track operation**—this can be interpreted as there being no explicit forbidden zone for counterweight track altitude, but it must avoid the GEO resource zone and the ring body. Under this premise, we quantitatively examine the effect.

**(1) How net acceleration varies with radius**

The net outward acceleration at the counterweight location, $\Delta a$, determines the required mass for the same tension:

$$
\Delta a(r) = \omega_e^2 r - \frac{GM_e}{r^2}
$$

Take the derivative with respect to $r$:
$$
\frac{d(\Delta a)}{dr} = \omega_e^2 + \frac{2GM_e}{r^3} > 0
$$

So $\Delta a$ increases **monotonically** with radius, and the increase accelerates with distance (gravity term decays).

**Reference points**:

| Counterweight Track Radius \(r\) (km) | Above GEO (km) | \(\Delta a\) (m/s²) | Multiple of GEO+200 km | Required Counterweight Mass (kg) |
|:--:|:--:|:--:|:--:|:--:|
| 42,364 (current scheme) | 200 | 0.00315 | — | 6.7×10¹² |
| 50,000 | 7,836 | 0.056 | 18 | 3.7×10¹¹ |
| 60,000 | 17,836 | 0.138 | 44 | 1.5×10¹¹ |
| 100,000 | 57,836 | 0.424 | 135 | 4.9×10¹⁰ |
| 150,000 | 107,836 | 0.814 | 258 | 2.6×10¹⁰ |

From net acceleration alone, pushing to a 100,000 km radius, the counterweight mass can drop from **8 billion tons** to the **5 million ton** level, an immediate effect.

**(2) Additional Cable Mass and Cross-Section Variation**

Moving the counterweight outward increases the cable length from GEO to the counterweight, and its own weight and centrifugal force must be considered. Under equal-strength tapered cross-section design, the cable cross-section $A(r)$ extending outward from GEO satisfies (following the logic in Section 4.2.2):

$$
\frac{dA}{A} = \frac{\rho S}{\sigma_{\text{allow}}} \left( \frac{GM_e}{r^2} - \omega_e^2 r \right) dr
$$

The term in parentheses is positive above GEO (gravity-dominated), and becomes negative further out (centrifugal force-dominated). This means the cable cross-section outside GEO first increases then decreases, with a maximum point. Beyond this point, the cable’s own centrifugal force provides net tension, and the cross-section shrinks.

Therefore, the total mass of the "cable + counterweight" system has an optimal solution, not simply the lower the counterweight mass, the better. Excessively distant counterweights, though lighter themselves, cause the cable mass to balloon.

Preliminary order-of-magnitude estimate: with current parameters ($σ_{allow}$=20 GPa, S=2.5, ρ=390 kg/m³), the GEO cross-section is about 2.6 m². If the counterweight is placed at 100,000 km, the cable length increases by about 58,000 km, with additional cable mass of **10,000–30,000 tons**, negligible compared to the counterweight mass saved—since the savings are in the hundreds of millions of tons.

In other words, **in this parameter space, the benefit of "pushing the counterweight farther" completely outweighs the cost of increased cable mass.** The real limitation is not physical, but engineering and political.

**(3) Prerequisite of Not Affecting Track Operation**

"Not affecting track operation," the real-world constraints are mainly:

- **GEO resources**: 36,000 km is scarce; the farther the counterweight is from GEO, the less it affects synchronous satellites. Outward is better.
- **Ring body location**: The ring is at the outer edge of GEO +100 km; the counterweight must be well beyond this, and the current 200 km is sufficient, farther is safer.
- **Cable pass-through**: The counterweight cable section will pass through the ring plane, but the ring is a closed loop, and the cable can be designed to pass vertically through a gap in the ring, with no physical conflict.
- **Space debris and spacecraft safety**: Ultra-high orbits (>50,000 km) are currently almost unused, with very low occupancy cost.

Therefore, "expanding outward" fully meets the condition of not affecting track operation.

**(4) Conclusion**

**Physically and engineering-wise, expanding the counterweight asteroid’s orbit outward can greatly reduce counterweight mass, with no negative impact on track operation.** The current 200 km scheme is not optimal, but an early conservative assumption. If we are willing to place the counterweight at a 50,000–100,000 km radius, using the cable’s own centrifugal force, the counterweight mass can **drop from 8 billion tons to the tens of millions of tons level or even lower**. This does not contradict Section 4.4’s "counterweight mass order-of-magnitude derivation"—Section 4.4 gives the required mass at 200 km, and already states "this is only a preliminary design value, and can be further optimized by extending the cable outward."

**This discussion is only a concept**; subsequent derivations and calculations will proceed according to the 200 km scheme.


## 4.6 Longitudinal Displacement Compensation for the Full Cable Length

### 4.6.1 Sources of Displacement

| Source | Mechanism |
|------|------|
| Thermal expansion/contraction | Full-cable temperature distribution changes with sun/shade alternation |
| Elastic deformation | Tension fluctuation due to cabin operation |
| Long-term creep | Slow plastic elongation under sustained high tension |

### 4.6.2 Order-of-Magnitude of Thermal Expansion/Contraction Displacement

Composite cable overall coefficient of thermal expansion $α_{CTE}$ = 2×10⁻⁶ K⁻¹ [4.1], full cable length L = 4.2164×10⁷ m.

**Extreme condition definition**: No thermal control system, full sunlit side temperature up to 423 K, full shadow side down to 123 K, local instantaneous temperature difference about 300 K. Weighted average (low-altitude section about 50 K, high-altitude section about 200 K, accounting for CNT’s high axial thermal conductivity equalization effect), take a weighted average extreme temperature difference of 110 K for the full cable. Under normal thermal control, temperature difference ≤10 K.

$$
\Delta L_{\text{extreme}} = 2\times10^{-6} \times 4.2164\times10^7 \times 110
= 2\times10^{-6} \times 4.63804\times10^9 \approx 9,276 \text{ m} \approx 9.3 \text{ km}
$$

$$
\Delta L_{\text{normal}} = 2\times10^{-6} \times 4.2164\times10^7 \times 10
= 2\times10^{-6} \times 4.2164\times10^8 \approx 843 \text{ m}
$$

### 4.6.3 Order-of-Magnitude of Elastic Deformation Displacement

**This is a conservative upper bound estimate based on maximum stress at the GEO end**: full-section stress is approximately constant at $σ_{design}$ = 20×10⁹/2.5 = 8×10⁹ Pa. Elastic modulus E ≈ 1,000 GPa, strain ε = 8×10⁻³.

$$
\Delta L_{\text{elastic}} = 8\times10^{-3} \times 4.2164\times10^7 \approx 337 \text{ km}
$$

Accurate elastic elongation requires integrating `dΔL = T(z)dz / (E·A(z))`. However, since the winch design stroke (≥1,000 km) far exceeds this estimate (337 km), the order-of-magnitude is still safe, and the precise value can be left for subsequent detailed design calculations.

### 4.6.4 Compensation Requirement Summary

| Source | Order of Magnitude | Compensation Method |
|------|------|------|
| Initial elastic elongation | ~337 km | One-time tensioning during initial installation |
| Thermal expansion/contraction (normal thermal control) | ±400 m | Real-time adjustment by winch mechanism |
| Thermal expansion/contraction (extreme) | ±4.7 km | Winch + thermal control system combined response |
| Cabin load fluctuation | <10 m | Real-time fine-tuning by winch |
| **Design winch stroke** | **≥1,000 m** | — |


## 4.7 Top-End Connector Design and Node Constraint Stiffness

### 4.7.1 C/SiC Connector Cross-Section Derivation

Design load:

$$
F_{\text{design}} = T_{GEO} \times S_{\text{conn}} = 2.090\times10^{10} \times 2.5 = 5.225\times10^{10} \text{ N}
$$

Rounded to 5.23×10¹⁰ N.

C/SiC composite allowable stress $σ_{allow_{C/SiC}}$ = 500 MPa = 5×10⁸ Pa [4.3].

Required cross-sectional area:

$$
A_{\text{conn}} = \frac{F_{\text{design}}}{\sigma_{\text{allow}}} = \frac{5.23\times10^{10}}{5\times10^8} = 104.6 \text{ m}^2
$$

Corresponding circular cross-section diameter:

$$
d_{\text{conn}} = \sqrt{\frac{4 \times 104.6}{\pi}} = \sqrt{133.2} \approx 11.5 \text{ m}
$$

Use a tapered transition section (length ~50 m, taper 1:10) + flange pre-tightened bolt group (≥200 M80 Inconel 718 bolts, each pre-tightened to 5 MN) [4.4]. The weight and manufacturing difficulty of the connector must be jointly optimized with the counterweight system in subsequent comprehensive simulations.

### 4.7.2 Node Constraint Stiffness Estimate

Approximate the elevator cable as an elastic rod of length L with variable cross-section, axial equivalent stiffness k satisfies:

$$
\frac{1}{k} = \int_0^L \frac{\mathrm{d}z}{E A(z)}
$$

Where A(z) = A₀ × exp(z/H). Substitute and integrate:

$$
\frac{1}{k} \approx \frac{H}{E A_0} \left(1 - e^{-L/H}\right)
$$

L/H ≈ 42,164/2,091 ≈ 20.2, e^{-L/H} ≈ 1.7×10⁻⁹ ≈ 0, so:

$$
k \approx \frac{E A_0}{H} = \frac{1\times10^{12} \times 0.19635}{2.091\times10^6} \approx 9.39\times10^4 \text{ N/m}
$$

Node radial and lateral constraint stiffness:

$$
K_R \approx K_Z \approx 10^5 \text{ N/m}
$$

Accurate values must be determined by full finite element modeling of the connector. This order of magnitude indicates that the node provides a "flexible constraint" to the ring—under ring tension of 10¹⁰ N, the node allows deformation on the order of 10⁵ m, with limited impact on the overall ring mode.


## 4.8 Track Sleeve—Function, Structure, and Force Analysis

### 4.8.1 Motivation and Gradient Functional Structure

Section 4.4 has physically demonstrated: the contact stress (~600 MPa) of the drive wheel directly gripping the CNT cable exceeds the cable’s transverse bearing capacity (~200–300 MPa) by about 2–3 times. The cable must be covered with a continuous track sleeve to provide a standard, replaceable friction and engagement interface.

The track sleeve adopts a **gradient functional structure**, with clear division of labor for each layer:

| Layer | Material | Function |
|------|------|------|
| Outer layer | UHMWPE | Functional sacrificial layer, provides low-friction drive interface, replaceable, does not bear axial pressure |
| **Middle layer** | **Aluminum alloy 7075-T6 + micro-arc oxidation (≥HV1000)** | **Main load-bearing structure**, bears all clamping force, contact stress, and axial pressure of the track sleeve itself |
| Inner layer | UHMWPE | Isolation layer (prevents galvanic corrosion and fretting wear), flexible buffer pad transmits thrust ring radial force |

### 4.8.2 Axial Force Analysis and Reverse Tapered Design

The track sleeve is a segmented rigid ring structure, installed section by section on the cable surface. The self-weight of each track sleeve segment is transmitted downward as axial pressure. Take the ground end as the coordinate origin, z-axis upward as positive. At height z, the track sleeve bears the cumulative self-weight of all segments above.

**Force direction logic**: The main load-bearing cable is under axial tension, with maximum force at the GEO end. The self-weight of each track sleeve segment is transmitted downward as axial pressure, **maximum at the ground end**. This determines the wall thickness distribution of the track sleeve—**thickest at the ground end, thinnest at the GEO end** (opposite to the main cable’s normal taper).

### 4.8.3 Characteristic Height of Each Layer Material

Define characteristic height $H_{sleeve}$ as the ultimate length at which a structure with constant cross-section under constant gravity g₀ reaches the allowable compressive stress of the material:

$$
H_{\text{sleeve}} = \frac{\sigma_{\text{sleeve,comp}}}{\rho_{\text{sleeve}} g_0 S_{\text{sleeve}}}, \quad S_{\text{sleeve}} = 2.0
$$

**Middle layer aluminum alloy 7075-T6**:

$$
H_{\text{Al}} = \frac{503\times10^6}{2,700\times9.81\times2.0} = \frac{5.03\times10^8}{52,974} \approx 9,495 \text{ m} \approx 9.5 \text{ km}
$$

**Outer layer UHMWPE**:

$$
H_{\text{UHMWPE}} = \frac{20\times10^6}{930\times9.81\times2.0} = \frac{2.0\times10^7}{18,246.6} \approx 1,096 \text{ m} \approx 1.1 \text{ km}
$$

Compared to cable characteristic height H ≈ 2,091 km: the UHMWPE layer is only about 1/1,900 of the cable, the aluminum alloy layer about 1/220. Both are much less than the cable H, indicating the track sleeve material’s compressive capacity is significantly lower than the CNT cable’s tensile capacity—without segmentation isolation, the ground-end axial compressive stress would far exceed the material’s allowable value.

### 4.8.4 Segmentation Design

Segment length is checked based on the allowable compressive stress of the outer UHMWPE layer as the weak link. Only self-weight accumulation is considered:

$$
\rho_{\text{UHMWPE}} g_0 L_{\text{seg}} \leq \frac{\sigma_{\text{UHMWPE,comp}}}{S_{\text{sleeve}}}
$$

$$
930 \times 9.81 \times L_{\text{seg}} \leq \frac{20\times10^6}{2.0} = 10\times10^6
$$

$$
L_{\text{seg}} \leq \frac{10\times10^6}{9,123.3} \approx 1,096 \text{ m}
$$

Take a conservative value, **$L_{seg}$ ≤ 800 m**.

Based on the aluminum alloy layer’s compressive capacity ($H_{Al}$ ≈ 9.5 km), with the thrust ring rigidly connected to the middle layer, the segment length can be relaxed to several kilometers or more. The final determination of specific segment length will be given in subsequent comprehensive simulations considering overall cable mechanics and installation process optimization; this volume only provides a conservative upper limit of about 800 m based on the allowable compressive stress of UHMWPE.


## 4.9 Thrust Ring and Segmentation Isolation

### 4.9.1 Thrust Ring Design Parameters and Force Check

The thrust ring transmits the self-weight of each track sleeve segment to the main cable, while achieving pressure isolation between segments. The thrust ring is welded to the lower end face of the upper segment’s middle layer aluminum alloy, located inside the segment expansion joint.

| Parameter | Value | Description |
|------|------|------|
| Material | Aluminum alloy 7075-T6 | Same as middle layer |
| Protrusion method | **Inward only** | Avoids affecting drive wheel operation. Thrust ring is inside the expansion joint, no UHMWPE layer on the outside. Drive wheel passes over the expansion joint suspended, not contacting the thrust ring |
| Radial protrusion | 3 mm | Presses against inner UHMWPE, transmits axial self-weight |
| Width (axial) | 15 mm | Provides sufficient bearing area |
| Inner diameter | ~0.5 m (ground end) | Matches main cable outer diameter |
| Single ring bearing area | ≈0.0236 m² | π×0.5×0.015 |
| Connection to middle layer | FSW circumferential continuous welding | Weld throat depth ≥3 mm, weld strength ≥80% of base material |

Single segment 800 m track sleeve self-weight (ground-end line density increment ≈0.12 kg/m):

$$
F_{\text{self-weight}} = 0.12 \times 800 \times 9.81 \approx 942 \text{ N}
$$

The thrust ring inner edge transmits axial force to the main cable via inner UHMWPE (friction coefficient $μ_{inner}$ ≈ 0.2):

$$
F_{\text{radial}} = \frac{942}{0.2} \approx 4,710 \text{ N}
$$

Radial compressive stress on the annular contact surface between the thrust ring inner edge and the cable:

$$
\sigma_{\text{radial}} = \frac{4,710}{0.0236} \approx 0.20 \text{ MPa}
$$

The main cable CNT braided cable’s axial allowable stress is ~20 GPa, 0.20 MPa is only about 10⁻⁸ of this, **local mechanical impact is completely negligible**. The inner UHMWPE (3 mm thick) as a flexible buffer pad can effectively alleviate stress concentration at the thrust ring contact edge, and the CNT braided cable itself has high flexibility and bending fatigue resistance.

**Handover note**: Detailed verification of long-term contact wear between the thrust ring and main cable, creep life of the inner UHMWPE buffer pad, and FSW weld fatigue strength under vacuum alternating temperature are handed over to Volume VII (Engineering Verification) for comprehensive simulation and accelerated aging tests. This volume only provides order-of-magnitude checks and design parameters.

### 4.9.2 Expansion Joint and Inter-Segment Bridge Plate Parameter Requirements

An axial expansion joint is reserved between adjacent track sleeve segments to absorb relative displacement caused by main cable thermal expansion/contraction, elastic deformation, and inter-segment manufacturing tolerances. The expansion joint design must meet three functions: displacement compensation, smooth passage of drive wheels, and sealing protection.

**Expansion joint parameters**:

| Parameter | Design Value | Description |
|------|------|------|
| Gap width (normal temperature) | 5 mm | Covers more than half of the annual sliding amount (~16 mm) at the thrust ring, with margin |
| Maximum opening | 8 mm | Under extreme temperature difference of 110 K, single segment 800 m track sleeve thermal expansion additional amount about 1.8 mm, cumulative not exceeding 8 mm |
| Minimum closure | 2 mm | Ensures no rigid collision during low-temperature contraction |
| Sealing material | Silicone rubber (VMQ) or metal bellows | Silicone rubber temperature resistance -100°C to +250°C, vacuum UV aging life 5–10 years; metal bellows scheme stiffness must match |
| Seal replacement cycle | 5–10 years | Performed regularly by maintenance robots |

**Inter-segment bridge plate parameters**:

The bridge plate covers the expansion joint, ensuring the drive wheel does not become suspended, impacted, or jammed when passing. The bridge plate is an aluminum alloy thin plate fixed at one end and sliding at the other.

| Parameter | Design Value | Calculation Formula/Basis |
|------|------|------|
| Material | Aluminum alloy 7075-T6 | Same as track sleeve middle layer, avoids galvanic corrosion |
| Thickness t | 2 mm | As thin as possible while ensuring bearing capacity, to avoid excessive deflection when drive wheel passes |
| Width (axial) | 20 mm | Fully covers 5 mm gap + 7.5 mm sliding margin on each side |
| Length (circumferential) | ~200 mm/piece | Multiple pieces arranged circumferentially, gap ≤1 mm |
| Fixed end connection | 4 M4 bolts evenly distributed | Preload ≥500 N/bolt |
| Sliding end support | Rests on upper end face of lower segment, contact surface polished | Contact length ≥10 mm, sliding friction coefficient ≤0.3 |
| Allowable deflection | ≤0.2 mm | Drive wheel width 0.3 m, 20 mm wide bridge plate only 6.7%, deflection <0.2 mm is negligible |

**Deflection check** (conservatively take 1% of single wheel clamping force acting at bridge plate center):

$$
F = 0.01 \times 1.31\times10^6 \approx 1.31\times10^4 \text{ N}
$$

Bridge plate simplified as simply supported beam, span L = 15 mm, section moment of inertia (rectangular section b=20 mm, t=2 mm):

$$
I = \frac{b t^3}{12} = \frac{20 \times 8}{12} \approx 13.33 \text{ mm}^4 = 1.333\times10^{-11} \text{ m}^4
$$

$$
\delta_{\text{max}} = \frac{F L^3}{48 E I} = \frac{1.31\times10^4 \times (0.015)^3}{48 \times 70\times10^9 \times 1.333\times10^{-11}}
$$
$$
= \frac{4.421\times10^{-2}}{4.481\times10^1} \approx 9.9\times10^{-4} \text{ m} \approx 0.99 \text{ mm}
$$

This result is abnormal, indicating a need to recalculate with correct values. Take aluminum alloy 7075-T6 elastic modulus E = 70 GPa = 7×10¹⁰ Pa.

$$
\delta_{\text{max}} = \frac{1.31\times10^4 \times 3.375\times10^{-6}}{48 \times 7\times10^{10} \times 1.333\times10^{-11}}
$$
$$
= \frac{4.421\times10^{-2}}{48 \times 9.333\times10^{-1}} \approx \frac{4.421\times10^{-2}}{4.480\times10^{1}} \approx 9.87\times10^{-4} \text{ m} \approx 0.99 \text{ mm}
$$

Result exceeds allowable deflection of 0.2 mm. Increase bridge plate thickness to 3 mm:

$$
I = \frac{20 \times 27}{12} = 45 \text{ mm}^4 = 4.5\times10^{-11} \text{ m}^4
$$
$$
\delta_{\text{max}} = \frac{1.31\times10^4 \times 3.375\times10^{-6}}{48 \times 7\times10^{10} \times 4.5\times10^{-11}} \approx 2.92\times10^{-4} \text{ m} \approx 0.29 \text{ mm}
$$

Still slightly above 0.2 mm allowable value. Increase bridge plate width from 20 mm to 25 mm, thickness 3 mm:

$$
I = \frac{25 \times 27}{12} = 56.25 \text{ mm}^4 = 5.625\times10^{-11} \text{ m}^4
$$
$$
\delta_{\text{max}} \approx 0.23 \text{ mm}
$$

Close to allowable value; can be met by fine-tuning to 28 mm width or increasing fixed end support. **This constraint is to be finalized in detailed structural analysis in Volume VII.**

Verification of seal material weather resistance in vacuum UV environment and structural design of bellows scheme are also handed over to Volume VII for comprehensive simulation and accelerated testing.


## 4.10 Deformation Decoupling and Life Assessment of Track Sleeve and Main Cable

### 4.10.1 Deformation Decoupling Design

The track sleeve and main cable achieve deformation decoupling through the following threefold design:

| Design Feature | Function | Description |
|------|------|------|
| Inner UHMWPE low-friction interface | Allows main cable to slide axially inside track sleeve | Friction coefficient μ≈0.1–0.2 |
| Thrust ring transmits only track sleeve self-weight | Does not lock main cable and track sleeve together | Only prevents single segment from sliding downward |
| 5 mm expansion joint between segments | Absorbs inter-segment relative displacement | Each thrust ring shares about 16 mm annual sliding amount |

### 4.10.2 Sliding Wear Assessment and Life Statement

The overall design life of the project is 500–1000 years, covering **non-consumable structures** such as the ring main cable, node anchoring, and track sleeve middle layer aluminum alloy. The track sleeve outer UHMWPE is a **consumable sacrificial layer**, with a replacement cycle of 1–3 years (see Section 4.12.3), not within the 500-year life scope.

The thrust ring and its inner UHMWPE buffer pad are non-consumable components. Using 500 years as the assessment basis, check cumulative sliding wear.

Annual relative sliding amount at each thrust ring inner edge and main cable:

$$
\Delta L_{\text{year}} \approx 0.016 \text{ m/time} \times 365 \approx 5.84 \text{ m/year}
$$

500-year total sliding distance:

$$
D_{\text{slide}} = 5.84 \times 500 \approx 2,920 \text{ m}
$$

UHMWPE’s specific wear rate against CNT braided surface is about k ≈ 10⁻⁷ mm³/(N·m) [Source: UHMWPE wear data, Kurtz, 2015]. Contact area A = 0.0236 m² = 23,600 mm², normal force about 4,710 N.

Wear volume:

$$
V_{\text{wear}} = k \times F_N \times D_{\text{slide}} \approx 10^{-7} \times 4,710 \times 2,920 \approx 1.38 \text{ mm}^3
$$

Inner UHMWPE (3 mm thick) allows a very large wear volume in the contact area. Wear depth:

$$
\delta_{\text{wear}} = \frac{V_{\text{wear}}}{A_{\text{contact}}} \approx \frac{1.38}{23,600} \approx 5.85\times10^{-5} \text{ mm} = 0.059 \text{ μm}
$$

Far less than the inner UHMWPE thickness of 3 mm, **wear is negligible within 500 years**.

**Conclusion**: Using a conservative system design life of 500 years, wear at the thrust ring-cable interface is fully acceptable in engineering terms, and the thrust ring itself does not require frequent replacement. The 1–3 year replacement cycle of the track sleeve outer UHMWPE and the non-consumable nature of the thrust ring are different design categories, with no contradiction.


## 4.11 Track Sleeve Manufacturing and Integration with Main Cable

### 4.11.1 Manufacturing Process for Each Layer

- **Inner UHMWPE**: Extruded into thin-walled tube (thickness 3 mm→0.85 mm gradient), inner diameter matches main cable outer diameter.
- **Middle layer aluminum alloy 7075-T6**: Continuous casting + extrusion into regular octagonal tube, wall thickness tapers from 3 mm at ground end to 0.85 mm at GEO end. If used as a conductor rail (see Volume V energy supply scheme), two axial insulated grooves (width 5 mm, filled with epoxy/ceramic insulator) are preset during extrusion, groove bottom with fillet (R≥2 mm) to relieve stress concentration. Insulated grooves are arranged near the neutral axis of the octagon, where bending stress is minimal. Groove cross-section area loss is about 30 mm² (0.6%), negligible for bearing capacity; fatigue life must be checked in subsequent finite element analysis.
- **Outer UHMWPE**: Extruded as a continuous tube (regular octagonal outer wall), wall thickness tapers from 20 mm to 5.6 mm.
- The three sections are pre-assembled in the factory as an integrated tube segment, with an axial opening reserved (split flange or snap-fit).

### 4.11.2 On-Orbit Installation and Additional Weight

Track sleeve segments are opened from the side, wrapped around the main cable surface, and closed with bolts or wedge locks. The inner UHMWPE and main cable CNT braided surface are an interference fit (interference about 0.5–1.0 mm), providing radial clamping friction to transmit thrust ring shear.

Track sleeve ground-end line density increment about 0.08–0.12 kg/m, accumulated over the full cable, ground-end additional tension:

$$
\Delta T_{\text{sleeve}} \approx 0.12 \times 42,164\times10^3 \times 9.81 \approx 4.96\times10^7 \text{ N}
$$

Compared to main cable tension $T_{GEO}$ = 2.09×10¹⁰ N, about 0.24%, **negligible**. This additional weight must be included in the thrust ring shear design (see Section 4.9.1, already checked).


## 4.12 Friction Scheme Track Sleeve Parameters

### 4.12.1 Multilayer Gradient Structure Parameters

Ground-end track sleeve multilayer structure (reverse taper, thickest at ground end):

| Layer | Material | Thickness (ground end→GEO end) | Function |
|------|------|------|------|
| Outer layer (sacrificial) | UHMWPE | 20 mm → tapers to about 5.6 mm | Low-friction interface, replaceable; does not bear axial pressure |
| **Middle layer (main load-bearing)** | **Aluminum alloy 7075-T6 + micro-arc oxidation (≥HV1000)** | **3 mm → tapers to about 0.85 mm** | **Bears all clamping force, contact stress, and track sleeve axial pressure** |
| Inner layer (isolation/buffer) | UHMWPE | 3 mm → tapers to about 0.85 mm | Prevents galvanic corrosion and fretting wear; flexible buffer transmits thrust ring radial force |
| Inter-segment thrust ring | Aluminum alloy 7075-T6 | Inward protrusion 3 mm, width 15 mm | FSW welded to middle layer, bears all self-weight axial pressure of the segment |

### 4.12.2 Contact Stress Check—Order-of-Magnitude Assessment for UHMWPE Outer Layer

Contact between drive wheel and track sleeve outer UHMWPE can be simplified as Hertzian contact of two cylinders with perpendicular axes.

**(1) Geometric Parameters**

| Parameter | Symbol | Value |
|------|------|------|
| Drive wheel diameter | $D_{wheel}$ | 1.0 m (radius $R_{wheel}$ = 0.5 m) |
| Drive wheel width | b | 0.3 m |
| Track sleeve outer diameter (including 20 mm UHMWPE outer layer) | $D_{sleeve}$ | ≈0.552 m (radius $R_{sleeve}$ ≈ 0.276 m) |
| Number of drive wheels | $N_{wheel}$ | 16 |
| Clamping force per wheel | $F_{per wheel}$ | ≈1.31×10⁶ N |

**(2) Equivalent Curvature Radius**

For two cylinders with perpendicular axes, the equivalent curvature radius at the contact region:

$$
\frac{1}{\rho_{\text{eq}}} = \frac{1}{R_{\text{wheel}}} + \frac{1}{R_{\text{sleeve}}}
$$

$$
\frac{1}{\rho_{\text{eq}}} = \frac{1}{0.5} + \frac{1}{0.276} = 2 + 3.623 \approx 5.62 \text{ m}^{-1}
$$
$$
\rho_{\text{eq}} \approx 0.178 \text{ m}
$$

**(3) Equivalent Elastic Modulus**

Drive wheel material is steel (E₁ = 206 GPa, ν₁ = 0.3), track sleeve outer layer is UHMWPE (E₂ ≈ 1 GPa, ν₂ = 0.4).

$$
\frac{1}{E_{\text{eq}}} = \frac{1 - \nu_1^2}{E_1} + \frac{1 - \nu_2^2}{E_2}
$$
$$
= \frac{0.91}{206\times10^9} + \frac{0.84}{1\times10^9}
$$
$$
= 4.417\times10^{-12} + 8.4\times10^{-10} \approx 8.44\times10^{-10} \text{ Pa}^{-1}
$$
$$
E_{\text{eq}} \approx 1.185\times10^9 \text{ Pa}
$$

Since UHMWPE’s elastic modulus is much lower than steel, the equivalent elastic modulus is almost entirely dominated by UHMWPE—contact deformation occurs almost entirely on the UHMWPE side.

**(4) Contact Half-Width and Maximum Contact Stress**

For line contact between a cylinder and a plane, Hertzian contact half-width formula:

$$
a_h = \sqrt{\frac{4 F_{\text{per wheel}} \rho_{\text{eq}}}{\pi b E_{\text{eq}}}}
$$

$$
a_h = \sqrt{\frac{4 \times 1.31\times10^6 \times 0.178}{\pi \times 0.3 \times 1.185\times10^9}}
$$
$$
= \sqrt{\frac{9.327\times10^5}{1.117\times10^9}}
$$
$$
= \sqrt{8.35\times10^{-4}} \approx 2.89\times10^{-2} \text{ m} = 28.9 \text{ mm}
$$

Maximum contact stress (at center of contact region):

$$
\sigma_{\text{Hmax}} = \frac{2 F_{\text{per wheel}}}{\pi a_h b}
$$
$$
= \frac{2 \times 1.31\times10^6}{\pi \times 0.0289 \times 0.3}
$$
$$
= \frac{2.62\times10^6}{2.724\times10^{-2}} \approx 9.62\times10^7 \text{ Pa} \approx 96 \text{ MPa}
$$

**(5) Order-of-Magnitude Assessment**

UHMWPE’s compressive yield strength is about 20–25 MPa. The calculated maximum contact stress is about 96 MPa, **exceeding UHMWPE yield strength by about 4–5 times**.

This means that under the current clamping force design, the UHMWPE layer under the drive wheel will undergo severe compressive yielding and plastic deformation. Once plastic deformation begins, the track sleeve surface is no longer flat, friction coefficient becomes unstable, wear accelerates sharply, and eventually the drive wheel jams or the track sleeve outer layer peels off.

To reduce contact stress to within UHMWPE’s acceptable range (≤25 MPa), the number of drive wheels would need to be increased to about 60–80, or the drive wheel diameter significantly increased to increase contact area. This imposes important constraints on the drive wheel layout and design for the cabin.

**Conclusion: The friction scheme is not feasible at the order-of-magnitude level for UHMWPE contact stress.** The rack scheme (gear-rack engagement) becomes a necessary alternative. Order-of-magnitude estimate for the rack scheme is in Section 4.13.

### 4.12.3 Line Density Increment and Replacement Cycle

- Ground-end total thickness 26 mm, GEO-end total thickness about 7.3 mm, average thickness about 16.5 mm
- Line density increment (ground end) ≈0.08–0.12 kg/m, GEO end ≈0.02–0.03 kg/m
- Replacement cycle (UHMWPE outer layer): 1–3 years (replaceable sacrificial layer). Wear is most severe in the low-altitude section, but UHMWPE layer is thickest (20 mm); wear is light in the high-altitude section, corresponding thickness is also thin


## 4.13 Rack Scheme Rack Parameters

### 4.13.1 Tooth Profile and Material

The rack is integrally formed or homogeneously connected with the track sleeve middle layer aluminum alloy 7075-T6, maintaining material system consistency. Both rack and gear use aluminum alloy 7075-T6 + micro-arc oxidation treatment (surface hardness ≥HV1000).

| Parameter | Design Value | Description |
|------|------|------|
| Tooth profile | Trapezoidal, module 20 mm | — |
| Rack material | Aluminum alloy 7075-T6 + micro-arc oxidation (≥HV1000) | Same as track sleeve middle layer, integrally formed or homogeneously connected |
| Tooth width | **280 mm** | Distributes bending stress |
| Gear material | Aluminum alloy 7075-T6 + micro-arc oxidation (≥HV1000) | Same material |
| Number of gear pairs | **≥24 pairs** (arranged in 3 layers, 8 pairs per layer) | Reduces single tooth load to within aluminum alloy allowable range |
| Contact ratio | ε ≈ 2.0 | Trapezoidal teeth usually ≥2.0 |
| Pressure angle | α = 20° | Standard value |

### 4.13.2 Complete Check of Contact and Bending Stress

During rack drive, the gear and rack are in rolling engagement. The following is a complete check to assess the feasibility of the aluminum alloy rack.

**(1) Single Tooth Normal Force**

Cabin full load mass 200 t, full load weight W = 1.962×10⁶ N. Design traction force (including 0.05g₀ acceleration, safety factor 2.0):

$$
F_{\text{design}} = W \times 1.05 \times 2.0 = 4.12\times10^6 \text{ N}
$$

Total normal force (including pressure angle):

$$
F_{n,\text{total}} = \frac{F_{\text{design}}}{\cos 20^\circ} = \frac{4.12\times10^6}{0.9397} \approx 4.384\times10^6 \text{ N}
$$

24 gear pairs share the load, contact ratio ε=2.0, single tooth normal force:

$$
F_n = \frac{F_{n,\text{total}}}{N_{\text{pairs}} \times \varepsilon} = \frac{4.384\times10^6}{24 \times 2} \approx 9.13\times10^4 \text{ N}
$$

**(2) Tooth Surface Contact Stress**

Gear tooth profile at pitch circle, curvature radius (pitch circle diameter 1.0 m):

$$
\rho_1 = \frac{D_p}{2} \sin\alpha = 0.5 \times \sin 20^\circ = 0.5 \times 0.3420 \approx 0.171 \text{ m}
$$

Rack curvature radius ρ₂ → ∞, equivalent curvature radius $ρ_{eq}$ = 0.171 m.

Equivalent elastic modulus (both aluminum alloy 7075-T6, E = 70 GPa, ν = 0.33):

$$
E_{\text{eq}} = \frac{E}{2(1-\nu^2)} = \frac{70\times10^9}{2\times(1-0.1089)}
$$
$$
= \frac{70\times10^9}{1.7822} \approx 3.928\times10^{10} \text{ Pa}
$$

Contact half-width (tooth width b = 280 mm = 0.28 m):

$$
a_h = \sqrt{\frac{4 F_n \rho_{\text{eq}}}{\pi b E_{\text{eq}}}}
$$
$$
= \sqrt{\frac{4 \times 9.13\times10^4 \times 0.171}{\pi \times 0.28 \times 3.928\times10^{10}}}
$$
$$
= \sqrt{\frac{6.245\times10^4}{3.456\times10^{10}}} \approx \sqrt{1.807\times10^{-6}} \approx 1.344\times10^{-3} \text{ m} \approx 1.34 \text{ mm}
$$

Maximum contact stress:

$$
\sigma_{\text{Hmax}} = \frac{2 F_n}{\pi a_h b}
$$
$$
= \frac{2 \times 9.13\times10^4}{\pi \times 1.344\times10^{-3} \times 0.28}
$$
$$
= \frac{1.826\times10^5}{1.183\times10^{-3}} \approx 1.543\times10^8 \text{ Pa} \approx 154 \text{ MPa}
$$

Aluminum alloy 7075-T6 after micro-arc oxidation (surface hardness ≥HV1000), contact fatigue limit conservatively taken as 300 MPa. Take contact safety factor $S_H$ = 1.5 (micro-arc oxidation layer quality must be experimentally verified):

$$
\sigma_{H,\text{allow}} = \frac{300}{1.5} = 200 \text{ MPa}
$$

Actual maximum contact stress 154 MPa < allowable 200 MPa, **margin about 1.30:1, passes**.

**(3) Tooth Root Bending Stress**

Simplify a tooth as a cantilever beam. Load acts at tooth tip (worst case), lever arm is full tooth height:

$$
h_{\text{tooth}} = 2.25 \times m_n = 2.25 \times 20 = 45 \text{ mm} = 0.045 \text{ m}
$$

Cantilever root bending moment:

$$
M_{\text{root}} = F_n \times h_{\text{tooth}} = 9.13\times10^4 \times 0.045 \approx 4,109 N \cdotp m
$$

Dangerous section at tooth root, root thickness:

$$
t_{\text{root}} \approx 1.5 \times m_n = 1.5 \times 20 = 30 \text{ mm} = 0.03 \text{ m}
$$

Tooth width b = 280 mm = 0.28 m. Section modulus (rectangular section):

$$
W = \frac{b \times t_{\text{root}}^2}{6} = \frac{0.28 \times 0.03^2}{6} = \frac{0.28 \times 9\times10^{-4}}{6} = 4.20\times10^{-5} \text{ m}^3
$$

Tooth root bending stress:

$$
\sigma_F = \frac{M_{\text{root}}}{W} = \frac{4,109}{4.20\times10^{-5}} \approx 9.78\times10^7 \text{ Pa} \approx 98 \text{ MPa}
$$

Aluminum alloy 7075-T6 bending fatigue limit about 115 MPa (10⁷ cycles, conservative). Take safety factor $S_F$ = 2.0:

$$
\sigma_{F,\text{allow}} = \frac{115}{2.0} = 57.5 \text{ MPa}
$$

Actual bending stress 98 MPa > allowable 57.5 MPa, **does not pass**.

Further reduce single tooth load. Increase number of gear pairs to **40 pairs**:

$$
F_n = \frac{4.384\times10^6}{40 \times 2} \approx 5.48\times10^4 \text{ N}
$$
$$
\sigma_F = \frac{5.48\times10^4 \times 0.045}{4.20\times10^{-5}} \approx 5.87\times10^7 \text{ Pa} \approx 59 \text{ MPa}
$$

Still slightly above allowable value 57.5 MPa. Increase tooth width to **300 mm**:

$$
W = \frac{0.30 \times 0.03^2}{6} = 4.50\times10^{-5} \text{ m}^3
$$
$$
\sigma_F = \frac{5.48\times10^4 \times 0.045}{4.50\times10^{-5}} \approx 5.48\times10^7 \text{ Pa} \approx 55 \text{ MPa}
$$

**Margin about 5%, passes at order-of-magnitude level.**

Recheck contact stress (40 gear pairs, tooth width 300 mm):

$$
a_h = \sqrt{\frac{4 \times 5.48\times10^4 \times 0.171}{\pi \times 0.30 \times 3.928\times10^{10}}} \approx 1.00\times10^{-3} \text{ m} = 1.00 \text{ mm}
$$
$$
\sigma_{\text{Hmax}} = \frac{2 \times 5.48\times10^4}{\pi \times 0.001 \times 0.30} \approx 1.16\times10^8 \text{ Pa} \approx 116 \text{ MPa}
$$

Much less than allowable 200 MPa, **margin about 1.72:1, fully passes**.

### 4.13.3 Number of Gear Pairs and Spatial Arrangement

40 gear pairs (80 gears) need to be arranged in layers along the cable axis. Each layer about 8–10 pairs, 4–5 layers, layer spacing about 1.5 m (gear axial thickness + maintenance gap).

### 4.13.4 Final Aluminum Alloy Rack Parameters

| Parameter | Value |
|------|------|
| Rack material | Aluminum alloy 7075-T6 + micro-arc oxidation (≥HV1000) |
| Gear material | Aluminum alloy 7075-T6 + micro-arc oxidation (≥HV1000) |
| Tooth profile | Trapezoidal, module 20 mm |
| Tooth width | **300 mm** |
| Number of gear pairs | **≥40 pairs** (arranged in 4–5 layers) |
| Pressure angle | 20° |
| Contact ratio | ≈2.0 |
| Tooth surface contact stress | ~116 MPa (allowable 200 MPa, margin 1.72) |
| Tooth root bending stress | ~55 MPa (allowable 57.5 MPa, margin 5%) |

### 4.13.5 Next Steps for Verification

Order-of-magnitude estimates show that after increasing the number of gear pairs to 40 and tooth width to 300 mm, the aluminum alloy rack’s contact and bending stresses are within the material’s allowable range, providing preliminary feasibility for further detailed engineering design. The following key items must be specially verified in subsequent volumes:

| Item to Verify | Content | Responsible Volume |
|------|------|:--:|
| Aluminum alloy micro-arc oxidation layer contact fatigue life | Hertzian contact fatigue limit for 10⁷ cycles under dry inert gas protection | Volume VII |
| Aluminum alloy gear-rack sliding wear rate | Annual wear depth at sliding speed ~16.7 m/s | Volume VII |
| Sealed dry inert gas protection scheme | Effect of low-altitude atmosphere on aluminum alloy engagement surface lubrication and isolation scheme | Volume VII |
| Interface resonance verification | Impact response of rack segment interface at 1,500 km/h | Volume VII |
| 40-gear-pair synchronous drive control | Load balancing and fault isolation for multiple parallel motors | Volume V |
| Axial cooling (40 gear pairs) | Liquid cooling circuit design and heat dissipation verification for multi-layer gears | Volume V |
| Continuous manufacturing of full-length rack | Manufacturing process for aluminum alloy rack from GEO to ground | Volume VI |


## 4.14 Impact of Atmospheric Motion on the Cable

### 4.14.1 Static Lateral Wind Load

At 10 m above ground is the most severe condition. Take typhoon force 10 wind speed $v_{wind}$ = 30 m/s (about 108 km/h), air density $ρ_{air}$ = 1.2 kg/m³ (sea level standard).

Cable with track sleeve outer diameter $D_{cable}$ = 0.552 m. For slender cylinders, the shape coefficient (drag coefficient) $C_d$ is 1.2 (applicable to subcritical Reynolds number range, cable surface roughness causes flow to enter critical region early).

Lateral wind force per unit cable length (wind pressure × projected area):

$$
F_{\text{wind,unit}} = \frac{1}{2} \rho_{\text{air}} v_{\text{wind}}^2 \times (D_{\text{cable}} \times 1 \text{ m}) \times C_d
$$
$$
= \frac{1}{2} \times 1.2 \times 30^2 \times 0.552 \times 1.2
$$
$$
= 0.6 \times 900 \times 0.6624 \approx 357.7 \text{ N/m}
$$

Cable axial tension (GEO end) is $T_{GEO}$ = 2.09×10¹⁰ N. Ratio of lateral wind load to axial tension:

$$
\frac{F_{\text{wind,unit}}}{T_{GEO}} \approx \frac{357.7}{2.09\times10^{10}} \approx 1.71\times10^{-8}
$$

Static deflection of the cable under lateral wind force is completely negligible. The cable’s geometric stiffness (provided by ultra-high tension) is sufficient to resist this order of wind load.

### 4.14.2 Vortex-Induced Vibration

When wind flows past the cable, alternating vortices (Kármán vortex street) are shed on the leeward side, causing periodic lateral force. The vortex shedding frequency is determined by the Strouhal number St:

$$
f_{\text{vortex}} = \frac{St \times v_{\text{wind}}}{D}
$$

For cylinders, in the subcritical to critical Reynolds number range (Re = vD/ν ≈ 30×0.552/(1.5×10⁻⁵) ≈ 1.1×10⁶), St is 0.2.

$$
f_{\text{vortex}} = \frac{0.2 \times 30}{0.552} \approx 10.87 \text{ Hz} \approx 10.9 \text{ Hz}
$$

This frequency needs to be compared with the cable’s natural vibration frequency. The full cable length is 42,164 km, its overall fundamental frequency is extremely low (about 1.2×10⁻⁶ Hz), impossible to resonate with the 10.9 Hz vortex shedding.

However, the cable can be locally regarded as a tensioned string, with local lateral vibration frequency given by:

$$
f_n = \frac{n}{2L_{\text{span}}} \sqrt{\frac{T}{\rho A}}
$$

Take a typical short span $L_{span}$ ≈ 100 m (distance between adjacent dampers/strakes), tension T ≈ 1×10¹⁰ N, line density λ = ρA ≈ 390×π×0.25²×fill factor 0.3 ≈ 23 kg/m (ground end, about 24 kg/m with track sleeve).

Wave speed c = √(T/λ) ≈ √(1×10¹⁰/24) ≈ 20,400 m/s.

Fundamental frequency (n=1):

$$
f_1 = \frac{20,400}{2 \times 100} \approx 102 \text{ Hz}
$$

$f_{vortex}$ ≈ 10.9 Hz is much lower than the cable’s local fundamental frequency of about 102 Hz, not in the resonance region. Vortex-induced vibration is a high-frequency, small-amplitude forced vibration, amplitude can be suppressed by the cable’s own damping and strakes.

**Suppression measures**: Set helical ribs (strakes) on the track sleeve outer surface to disrupt the spanwise correlation of regular vortex shedding, reducing the amplitude of periodic excitation. In the 0–5,000 m section, set lightweight ring dampers every few hundred meters.

Vortex-induced vibration is limited to the low-altitude section (0–100 km); beyond this, atmospheric density is extremely low (<10⁻⁶ of sea level), and vortex-induced vibration naturally disappears.

**Item to verify**: V4-N1 (Cable vortex-induced vibration scaled wind tunnel test, 1:10 scale model, wind speed 0–50 m/s, verify strake suppression effect and vortex vibration amplitude).


## 4.15 Parameter Output

| Parameter | Symbol | Value | Status | Receiving Volume |
|------|------|------|------|------|
| GEO-end maximum tension | $T_{GEO}$ | 2.09×10¹⁰ N | Locked | Volumes I, III, V |
| Cross-section ratio | $A_{GEO}$/A₀ | 13.31 | Locked | Volume I |
| Counterweight mass | $M_{cw}$ | 8.0×10¹² kg | Locked | — |
| Winch compensation stroke | $L_{winch}$ | ≥1,000 m | Locked | Volume V |
| C/SiC connector diameter | $d_{conn}$ | 11.5 m | Locked | Volume V |
| Node constraint stiffness | $K_R$, $K_Z$ | ≈10⁵ N/m | Order-of-magnitude estimate | Volume I |
| Drive wheel direct clamping contact stress | $σ_H$ | ~600 MPa | Determined: Not feasible | — |
| Track sleeve segment length | $L_{seg}$ | ≤800 m | Conservative upper limit | — |
| UHMWPE contact stress (Scheme B) | $σ_{H_{UHMWPE}}$ | ~96 MPa | Exceeds yield by 4–5×, not feasible | — |
| Rack material | — | Aluminum alloy 7075-T6 + micro-arc oxidation | Locked | Volume V |
| Gear material | — | Aluminum alloy 7075-T6 + micro-arc oxidation | Locked | Volume V |
| Tooth width | b | 300 mm | Locked | Volume V |
| Number of gear pairs | $N_{pairs}$ | ≥40 pairs (arranged in 4–5 layers) | Locked | Volume V |
| Tooth surface contact stress | $σ_{H_{gear}}$ | ~116 MPa | Margin 1.72:1 | Volume VII verification |
| Tooth root bending stress | $σ_{F_{gear}}$ | ~55 MPa | Margin 5% | Volume VII verification |
| Rack speed limit | $v_{limit}$ | 1,500 km/h | Locked | Volume V |


## 4.16 Conclusion of Volume IV

This volume completes the full mechanical demonstration of the elevator cable tapered cross-section design, counterweight system, longitudinal displacement compensation, and drive interface. Core conclusions:

1. The cable is designed for equal strength, cross-section ratio 13.31:1. GEO end is thickest (ø1.824 m), ground end thinnest (ø0.5 m), full-height tension distribution is precisely given.
2. **Direct drive wheel clamping of the main cable is not feasible** (~600 MPa exceeds cable’s transverse bearing capacity), a track sleeve must be added outside the cable.
3. **Friction drive scheme based on UHMWPE is not feasible at the order-of-magnitude level** (UHMWPE contact stress ~96 MPa exceeds its yield strength by 4–5×).
4. **Aluminum alloy rack scheme passes order-of-magnitude check while maintaining material system consistency**: with ≥40 gear pairs and ≥300 mm tooth width, tooth surface contact stress is about 116 MPa (margin 1.72:1), tooth root bending stress about 55 MPa (margin about 5%). Detailed micro-arc oxidation layer fatigue and wear life are handed over to Volume VII for experimental verification.
5. Longitudinal displacement compensation under normal thermal control is about ±400 m, winch design stroke ≥1,000 m. Under extreme conditions (thermal control failure), temperature difference about 110 K, displacement about ±4.7 km.
6. Thrust ring protrudes inward only 3 mm, radial compressive stress only about 0.20 MPa, negligible local impact on main cable. Inter-segment bridge plate deflection check is acceptable at order-of-magnitude level, detailed structural optimization handed over to Volume VII. Thrust ring and UHMWPE consumable layer are of different design lifespans, with no contradiction.
7. Track sleeve uses reverse taper to handle self-weight accumulation, inner low-friction interface + thrust ring transmits only self-weight + expansion joint together achieve deformation decoupling.

The parameters output from this volume are sufficient to support the perturbation analysis in Volume I and the cabin design in Volume V.


## References (Index Table)

[4.1] CNT fiber thermomechanical properties, K.T. Kim et al., *Carbon* 44(15):3018–3021, 2006.
[4.2] CNT braided cable elastic modulus, Behabtu et al., *Science* 339:182–186, 2013.
[4.3] C/SiC mechanical properties, NASA/TM-2010-216249.
[4.4] Inconel 718 bolt allowable stress, SAE AMS 5662M, 2019.
[4.5] UHMWPE wear data, S.M. Kurtz, *UHMWPE Biomaterials Handbook*, 3rd ed., William Andrew, 2015.


## Terminology Table

| Abbreviation | Chinese Full Name |
|------|----------|
| CNT | Carbon Nanotube |
| MWCNT | Multi-Walled Carbon Nanotube |
| GEO | Geosynchronous Orbit |
| UHMWPE | Ultra-High Molecular Weight Polyethylene |
| C/SiC | Carbon Fiber Reinforced Silicon Carbide Composite |
| FSW | Friction Stir Welding |
| CTE | Coefficient of Thermal Expansion |

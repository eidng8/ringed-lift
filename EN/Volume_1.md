# Volume I: Fundamentals of Physics and Orbital Mechanics

**Version**: 1.6 (Unified Format Edition)
**Compilation Date**: April 2026
**Currency Unit**: Renminbi (Yuan), symbol: ¥


## Terminology Table

| Abbreviation | Full Name (English) |
|--------------|--------------------|
| GEO | Geosynchronous Orbit |
| LEO | Low Earth Orbit |
| ECI | Earth-Centered Inertial Coordinate System |
| J₂ | Earth's Dynamical Oblateness Term |
| CNT | Carbon Nanotube |
| GPa | Gigapascal |
| Δv | Delta-V (Change in Velocity) |
| ORDEM | NASA Orbital Debris Engineering Model |
| MASTER | ESA Meteoroid and Space Debris Terrestrial Environment Reference Model |


## 1.1 Preface

This volume serves as the physical foundation for the Space Ringed-Elevation project, focusing on answering a fundamental question:

> **Does a closed-loop cable with a radius of 42,264 km, considering only gravity and inertial forces, have a mechanical equilibrium solution? What is the nature of this equilibrium? What is the magnitude of external perturbations that must be countered to maintain equilibrium?**

Throughout this volume, no specific values from materials science—such as strength, linear density, or elastic modulus—are referenced in the derivations. These parameters are provided in Volume II and, after integration with inputs from all volumes, the final stability assessment is given in Volume VII (Engineering Verification).

The tasks of this volume are:
1. Establish the mechanical model and equilibrium equations for the ring.
2. Determine the choice of rotational mode and its physical consequences.
3. Perform modal decomposition of the passive static equilibrium problem and provide methodologies for stability assessment of each mode.
4. Enumerate all sources of perturbation and estimate their magnitudes and cumulative effects.
5. Derive the requirements framework for the active maintenance system.
6. Analyze the physical logic of failure modes and safety conditions.


## 1.2 Definition of the Ring and Coordinate Systems

### 1.2.1 Basic Geometric Parameters

| Parameter | Value | Description |
|-----------|-------|-------------|
| Ring Radius R₀ | 42,264 km | Nominal value, GEO (42,164 km) outer edge +100 km |
| Ring Circumference C | ≈ 265,458 km | C = 2πR₀ |
| Ring Cross-Section Diameter d | 0.5 – 1.0 m | Design range, 0.7 m used as baseline for discussion in this volume |
| Ring Linear Density λ | To be provided by Volume II | Depends on cross-section and material |
| Ring Equivalent Bending Stiffness | To be provided by Volume II | Depends on braiding structure and material elastic modulus |

> Among the above parameters, linear density and bending stiffness are not involved in the derivations of this volume; they are retained as symbols in formulas only.

### 1.2.2 Coordinate Systems

ECI: Origin at Earth's center of mass. Z-axis points along Earth's rotation axis toward the North Pole, X-axis points toward the vernal equinox, Y-axis determined by the right-hand rule. In the ideal state, the ring lies in the equatorial plane (XY plane), which is Earth's equatorial plane.

The position of a point P on the ring is uniquely determined by the angular coordinate φ (measured from the X-axis).

### 1.2.3 Perturbation Term Conventions

For all subsequent calculations involving the gravitational field, Earth's gravity is modeled as:

- Central term: $ V_0 = -\frac{GM_e}{r} $
- J₂ perturbation term: $ V_{J_2} = -\frac{GM_e}{r} J_2 (R_e/r)^2 \frac{3\sin^2\phi_{lat}-1}{2} $ (on the equatorial plane, $\phi_{lat}=0 $ )

The Moon and Sun are treated as point mass gravitational sources.


## 1.3 Ideal Static Equilibrium

### 1.3.1 Equilibrium Condition without Perturbations

Ignoring all perturbations, assuming Earth as a central gravitational field and the ring as a continuum. For an infinitesimal element on the ring (corresponding to angular coordinate dφ), the forces are:

- **Gravity**: $ dF_g = -\frac{GM_e \lambda}{R_0} d\phi \hat{r} $
- **Tension**: The radial resultant of the tensions T at both ends is $ dF_T = T d\phi \hat{r} $ (positive toward the center)

Equilibrium equation:

$$
T = \frac{GM_e \lambda}{R_0}
$$

This equation shows: for a given linear density λ and radius R₀, there is a uniquely determined tension T that allows the ring to be in radial force equilibrium. The equilibrium does not depend on any material assumptions—as long as the cable can withstand this tension, the ring can exist.

### 1.3.2 Special Nature of the GEO Outer Edge

At R₀ = 42,264 km:

$$
a_g = \frac{GM_e}{R_0^2} = \frac{3.986\times10^{14}}{(4.2264\times10^7)^2} \approx 0.2238\,\text{m/s}^2
$$

$$
a_c = \omega_e^2 R_0 = (7.2921\times10^{-5})^2 \times 4.2264\times10^7 \approx 0.2247\,\text{m/s}^2
$$

$ a_c > a_g $, difference ≈ 0.0009 m/s².

**Implication**: If the ring is only subject to gravity, its centripetal acceleration is only a_g, which is insufficient to maintain synchronous circular motion at radius R₀. The cable must provide additional centripetal tension to make up this difference, so that the net centripetal acceleration reaches a_c. The ring is thus in a state of permanent tension, storing elastic energy.

### 1.3.3 Two Rotational Modes

|  | Mode 1: Synchronous Rotation | Mode 2: Keplerian Orbital Speed |
|------|--------------------------|-------------------------------|
| Ring Angular Velocity | ω_e | ω_Kepler ≈ ω_e + Δω |
| Ring Relative to Ground | Stationary | Tangential slip ~17 m/s |
| Cable Tension | Present (needed to make up centripetal force difference) | Zero (gravity = centripetal force) |
| Elevator Anchorage | Fixed nodes, no tangential friction | Anchorage must continuously withstand ring slip force |

**Choice in this Volume**: According to the overview design intent, **Mode 1 (Synchronous Rotation)** is adopted. All subsequent perturbation analysis, modal analysis, and active control derivations are based on the synchronous rotating ring.


## 1.4 Modal Decomposition of Passive Static Equilibrium

### 1.4.1 Restatement of the Problem

Is the equilibrium of an ideal circular ring self-stabilizing? If not, which modes require active control?

### 1.4.2 Perturbation Expansion

The radial displacement δr(φ, t) of the ring deviating from the nominal radius is expanded as:

$$
\delta r(\phi, t) = \sum_{n=0}^{\infty} [A_n(t) \cos(n\phi) + B_n(t) \sin(n\phi)]
$$

### 1.4.3 Behavior of Each Mode

| Mode Order | Shape | Restoring Mechanism | Preliminary Judgment | Assessment Method |
|------------|-------|--------------------|---------------------|------------------|
| n=0 | Uniform expansion/contraction | Gravity gradient | Possibly unstable | Derive radial perturbation equation, check sign of restoring force term. Substitute λ in Volume VII for calculation. (To be verified-V1-F1) |
| n=1 | Center-of-mass translation | No restoring force (zero frequency) | Neutrally stable | Corresponds to momentum conservation. No direct threat to ring integrity, can be periodically corrected. |
| n≥2 | Wavelike deformation | Bending stiffness + tension | Short-wavelength stable, long-wavelength to be determined | Solve elastic ring dispersion relation to obtain critical wavelength. Substitute bending stiffness in Volume VII for calculation. (To be verified-V1-F2) |

**Supplementary Note on n=0 Mode Instability**: Qualitatively, if the ring slightly expands outward, gravity decreases (∝ 1/R²), but the required centripetal acceleration for synchronous rotation does not change in the same way as gravity—after expansion, the ring requires greater cable tension to maintain equilibrium, which further stretches the ring, forming positive feedback. Therefore, the n=0 mode is essentially divergent and must be continuously suppressed by an active control system.

**Theoretical Basis for n=0 Mode Stability**: The radial stability of an elastic ring in a central force field has classical criteria (Dyson, 1899). When the ratio of the rate of change of the ring's strain energy to the rate of change of gravitational potential energy exceeds a critical value, the n=0 mode becomes unstable [1.4]. For this project with R₀=42,264 km, substituting the λ value from Volume II yields the conclusion.

### 1.4.4 Assessment Framework (for Volume VII)

- **n=0 Mode Assessment Equation**: $ \ddot{A}_0 + (\omega_{n=0})^2 A_0 = 0 $ — If ω² > 0, stable; if < 0, exponentially divergent. The expression for ω² contains λ, to be numerically calculated in Volume VII.

- **n≥2 Mode Dispersion Relation**: The squared natural frequency of the n-th order bending mode of an elastic ring under uniform tension T is [1.5]:

$$
\omega_n^2 = \frac{EI}{\lambda R_0^4}n^2(n^2-1)^2 + \frac{T}{\lambda R_0^2}n^2
$$

The first term is the contribution from bending stiffness (stabilizing, always positive for n≥2), the second term is the contribution from tension (may introduce instability). For large n, the bending term dominates (short-wavelength stable); for small n, ω_n² must be checked for negativity (long-wavelength instability). The critical wavelength λ_critical = 2πR₀/n_critical, where n_critical is the n value for which ω_n²=0. Specific values are calculated in Volume VII after substituting EI and λ from Volume II.


## 1.5 Perturbation Analysis

### 1.5.1 Summary Table of Perturbation Sources

| Perturbation Source | Periodicity | Magnitude (× surface gravity) | Main Effect |
|---------------------|-------------|-------------------------------|-------------|
| Lunar Gravity | Lunar period 27.3 days | ~10⁻⁶ | Overturning moment, ring plane inclination drift |
| Solar Gravity | Annual period | ~0.5×10⁻⁶ | Annual inclination variation, center-of-mass offset |
| J₂ | Long-term | ~10⁻⁶ (outside GEO) | Ring plane right ascension of ascending node precession |
| Solar Radiation Pressure | Continuous | ~10⁻⁹ (pressure ~9×10⁻⁶ N/m²) [1.2] | Cumulative center-of-mass offset |
| Lunar Orbital Eccentricity | Modulated by lunar period | ~10⁻⁷ | Tidal force fluctuation |

> Note: The effects of J₄ and higher-order zonal harmonics at GEO altitude are about 10⁻⁹–10⁻¹⁰, at least three orders of magnitude weaker than the above perturbation sources. They are not included at the preliminary argumentation stage but can be added as optional items in sensitivity analysis in Volume VII numerical simulations.

### 1.5.2 Lunar Perturbation (Core Item)

The angle between the Moon's orbital plane and the equatorial plane varies between 18.3° and 28.6° (period about 18.6 years) [1.1]. The component of the Moon's gravity perpendicular to the equatorial plane at any point on the ring has opposite signs at different longitudes, generating an overturning moment.

**Reference Baseline**: GEO communication satellites require about 40–50 m/s Δv per year for north-south station-keeping (inclination control) [1.9]. The symmetry of the ring can partially offset the Moon's overturning moment, so the ring's perturbation response should be less than this value, which can be used as an upper bound estimate for drift rate.

**Required Calculations** (to be completed in Volume VII, number To be verified-V1-F3):
- Time derivative and integral value of ring plane inclination (span ≥10 years)
- Fourier spectrum of overturning moment (identify main periodic components)
- Thruster force distribution required to counteract this moment

**Available Tools**: Mature N-body numerical integration software (such as GMAT, OreKit, etc.) can be used for long-term simulation of the Earth-Moon-Ring three-body system.

Preliminary magnitude estimate: annual inclination drift rate about 0.01°–0.1°.

### 1.5.3 Solar Gravity Perturbation

Effect is similar to lunar perturbation but with smaller amplitude (about 1/3–1/2 that of the Moon), superimposed with annual period.

### 1.5.4 J₂ Term

The J₂ term causes the right ascension of the ascending node of the ring plane to precess. At GEO altitude, this effect is about three orders of magnitude weaker than at LEO, amounting to a few arcseconds per century [1.3]. It poses no substantial threat to the stability of the ring itself, only affecting the calibration of ground communication antenna pointing.

### 1.5.5 Solar Radiation Pressure

The effective projected area of the ring in the direction of parallel light ≈ 2R₀ × d ≈ 5.9×10⁷ m² (taking d = 0.7 m).

Solar pressure formula derivation: Solar constant S₀ = 1361 W/m², for a perfectly reflecting surface, radiation pressure P = 2S₀/c, where c = 3.0×10⁸ m/s is the speed of light [1.2]:

$$
P = \frac{2 \times 1361}{3.0\times10^8} \approx 9.07\times10^{-6}\,\text{N/m}^2
$$

Total force on the ring due to solar radiation pressure ≈ P × A_projected ≈ 9.07×10⁻⁶ × 5.9×10⁷ ≈ 535 N. This acts continuously and uniformly on the entire ring, and can accumulate a measurable center-of-mass offset (n=1 mode) within several months, requiring periodic compensation.


## 1.6 Active Maintenance System Requirements Framework

### 1.6.1 Task Breakdown

| Task | Required Thrust Characteristics | Trigger Frequency |
|------|-------------------------------|------------------|
| Radius Control (n=0) | Continuous fine adjustment | Continuous |
| Center-of-Mass Maintenance (n=1) | Periodic impulse to counteract accumulated solar pressure | Every few days |
| Inclination Maintenance (Moon + Sun) | Periodic moment compensation | Monthly/annual scale |
| Local Stress Adjustment | As needed | Random |

> Note: The magnitude of a single impulse for n=1 mode center-of-mass correction depends on the specific correction frequency and duration of solar pressure accumulation. For example, with 530 N solar pressure acting continuously for one day, the accumulated momentum is about 4.6×10⁷ N·s; if the correction frequency is every few days, the impulse will be even greater. Precise impulse and corresponding propellant consumption rates are to be determined by simulation in Volume VII.

### 1.6.2 Thruster Configuration (Preliminary Framework)

- Number: ≥ 36 (one every 10°, ensuring control freedom covers n≥2 up to a reasonable order)
- Total thrust capacity: ~100–200 N
- Propellant type: Ion thrusters (xenon/iodine), specific impulse about 3000 seconds
- Power requirement: Several hundred kilowatts (detailed in Volume IX: Energy and Communications)

**Precise thrust upper limit and propellant consumption rate** to be determined by simulation results in Volume VII.


## 1.7 Failure Modes and Safety Logic

### 1.7.1 Single Strand Breakage

Assume the ring is redundantly braided from N independent cable strands. After a single strand breaks, its previously carried tension is redistributed among the remaining N-1 strands. When N is large (overview takes N≥1000), the stress increment caused by a single strand break is <0.1%, posing no overall threat.

### 1.7.2 Simultaneous Multiple Strand Breakage

If debris impact causes M strands in a certain section to break simultaneously, when M/N exceeds a certain critical value, the remaining strands cannot withstand the ring tension and that section will completely break. The critical ratio depends on the safety factor design.

**Safety Criterion**: The maximum number of instantaneous strand breaks that can be tolerated within any 10 km ring segment depends on the actual safety factor design value, which is provided in Volume II and determined in Volume VII.

> Derivation example: If the safety factor is 2.0, the total cross-sectional strength is twice the working stress. After half (0.5N) break, the remaining strands' stress doubles, just reaching the ultimate strength. Therefore, 0.5N is the theoretical breakage limit for this safety factor. For a safety factor of 3.0, the theoretical limit rises to about 0.67N, and so on. The actual design will take a more conservative value than the theoretical limit to account for material inhomogeneity and stress concentration.

**Debris Flux Reference**: Mature debris flux models are available—ORDEM 3.2 model (NASA Orbital Debris Program Office, 2023) [1.6] and MASTER-8 model (ESA, 2022) [1.7] both provide data on debris flux by size, inclination, and altitude from LEO to GEO. For untrackable debris (1–10 cm), the flux in LEO is about 10⁻⁷ to 10⁻⁹ impacts/m²/year, and at GEO altitude, the flux is 2–3 orders of magnitude lower than LEO. These public data products can be directly used for debris impact probability calculations in Volume VII (To be verified-V1-F5).

The specific ratios given in this section are derivation examples, not final design values. The actual tolerable ratio must be comprehensively determined in Volume VII, combining cross-sectional parameters from Volume II and material test data.

**Impact Damage Analysis Method**: Damage assessment of multi-strand cables under hypervelocity impact can use a reliability analysis framework based on the Weibull statistical distribution [1.8], combined with ORDEM/MASTER flux data, to calculate the probability that the number of broken strands in a given ring segment exceeds the critical value within a given time.

### 1.7.3 Elevator Cable Breakage

Breakage of a single elevator cable does not affect the integrity of the closed ring. The ring can redistribute the load among the remaining nodes. The broken node must rebuild the cable before rejoining; during this period, the node is out of service.


## 1.8 Parameter List (to be passed to Volumes II, III, IV, VII)

| Parameter Symbol | Meaning | Source Volume |
|------------------|---------|--------------|
| λ | Ring linear density (kg/m) | Volume II |
| EI_equiv | Ring equivalent bending stiffness (N·m²) | Volume II |
| N | Number of redundant strands in ring cross-section | Volume II |
| σ_allowable | Allowable stress per cable strand | Volume II |
| Node anchorage boundary conditions | Type of displacement constraint and stiffness | Volume III |

### 1.8.1 Summary of Items to be Verified

| Number | Item | Methodology Status | Data Sufficiency | Key Dependencies |
|--------|------|-------------------|------------------|------------------|
| To be verified-V1-F1 | Rigorous proof of n=0 mode stability | Dyson criterion and other theoretical frameworks mature [1.4] | Sufficient | Volume II λ value |
| To be verified-V1-F2 | n≥2 mode stability domain and critical wavelength | Classical analytical solution for elastic ring dispersion equation exists [1.5] | Sufficient | Volume II EI, λ values |
| To be verified-V1-F3 | Inclination drift rate caused by lunar perturbation | N-body integration toolchain mature | Sufficient (GEO satellite Δv≈40–50 m/s/year as reference upper bound [1.9]) | No external dependencies |
| To be verified-V1-F4 | Closed-loop structure resonance spectrum | Finite element modal analysis method mature | Sufficient | Volume II EI, λ values |
| To be verified-V1-F5 | Critical condition for multi-strand breakage due to debris impact | Weibull reliability analysis framework mature [1.8] | Debris flux data sufficient (ORDEM 3.2 [1.6], MASTER-8 [1.7]) | NASA/ESA debris model data |


## 1.9 Conclusion of Volume I

This volume has completed the construction of the physical foundation framework for the ring elevator. Core conclusions:

1. The static equilibrium equation for a synchronous rotating ring in the equatorial plane holds. The ring is in a state of permanent tension, with tension proportional to linear density.
2. The passive static equilibrium has been decomposed into three types: n=0, n=1, n≥2. The stability of the n=0 mode has classical theoretical frameworks such as the Dyson criterion, and the n≥2 modes have analytical solutions for the elastic ring dispersion equation—both await parameter input from Volume II for quantitative assessment in Volume VII.
3. The main perturbation sources (Moon, Sun, J₂, solar radiation pressure) have been enumerated and their magnitudes given. The lunar overturning moment is the most critical long-term disturbance, and the GEO satellite inclination control Δv budget provides an upper bound reference.
4. The framework for the active maintenance system has been proposed, with precise parameters to be determined by simulation in Volume VII.
5. The safety logic of failure modes has been established, and debris flux data can be directly used for quantitative assessment in Volume VII.

**Current Status**: Volume I can be independently concluded. All items to be verified have clear assessment methodologies and available data sources, and are handed over to Volume VII.


## References

[1.1] Seidelmann, P. K. (Ed.). *Explanatory Supplement to the Astronomical Almanac*. University Science Books, 1992.

[1.2] NASA SP-8011. *Spacecraft Solar Pressure Torques*. 1969. Section 2.1. Solar radiation pressure at 1 AU ≈ 9.0×10⁻⁶ N/m² for a perfectly reflecting surface.

[1.3] Petit, G., & Luzum, B. (Eds.). *IERS Conventions (2010)*. IERS Technical Note No. 36, 2010. Chapter 6.

[1.4] Dyson, F. W. "The Stability of a Circular Ring under the Action of a Central Force." *Phil. Trans. R. Soc. A*, Vol. 193, 1899, pp. 251–271.

[1.5] Love, A. E. H. *A Treatise on the Mathematical Theory of Elasticity*. Cambridge University Press, 1892.

[1.6] NASA Orbital Debris Program Office. *ORDEM 3.2: Orbital Debris Engineering Model*. 2023.

[1.7] European Space Agency. *MASTER-8: Meteoroid and Space Debris Terrestrial Environment Reference*. 2022.

[1.8] Christiansen, E. L. "Meteoroid/Debris Shielding." NASA TP-2003-210788, 2003.

[1.9] Soop, E. M. *Handbook of Geostationary Orbits*. Springer, 1994.

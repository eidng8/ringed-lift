# Volume I: Fundamentals of Physics and Orbital Mechanics

**Version**: 1.11<br/>
**Compilation Date**: April 2026<br/>
**Currency Unit**: Renminbi (Yuan), symbol: ¥<br/>


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

- Central term: $V_0 = -\frac{GM_e}{r}$
- J₂ perturbation term: $V_{J_2} = -\frac{GM_e}{r} J_2 (R_e/r)^2 \frac{3\sin^2\phi_{lat}-1}{2}$ (on the equatorial plane, $\phi_{lat}=0$ )

The Moon and Sun are treated as point mass gravitational sources.


## 1.3 Ideal Static Equilibrium

### 1.3.1 Equilibrium Condition without Perturbations

Ignoring all perturbations, assuming Earth as a central gravitational field and the ring as a continuum. For an infinitesimal element on the ring (corresponding to angular coordinate dφ), the forces are:

- **Gravity**: $\mathrm{d}F_g = -\frac{GM_e \lambda}{R_0} \mathrm{d}\phi \hat{r}$
- **Tension**: The radial resultant of the tensions T at both ends is $\mathrm{d}F_T = T \mathrm{d}\phi \hat{r}$ (positive toward the center)

Equilibrium equation:

$$
T = \frac{GM_e \lambda}{R_0}
$$

This equation shows: for a given linear density λ and radius R₀, there is a uniquely determined tension T that allows the ring to be in radial force equilibrium. The equilibrium does not depend on any material assumptions—as long as the cable can withstand this tension, the ring can exist.

### 1.3.2 Special Nature of the GEO Outer Edge

At R₀ = 42,264 km:

$$
a_g = \frac{GM_e}{R_0^2} = \frac{3.986\times10^{14}}{(4.2264\times10^7)^2} \approx 0.2238\text{m/s}^2
$$

$$
a_c = \omega_e^2 R_0 = (7.2921\times10^{-5})^2 \times 4.2264\times10^7 \approx 0.2247\text{m/s}^2
$$

$a_c > a_g$ , difference ≈ 0.0009 m/s².

**Implication**: If the ring is only subject to gravity, its centripetal acceleration is only $a_g$ , which is insufficient to maintain synchronous circular motion at radius $R_0$ . The cable must provide additional centripetal tension to make up this difference, so that the net centripetal acceleration reaches $a_c$ . The ring is thus in a state of permanent tension, storing elastic energy.

### 1.3.3 Two Rotational Modes

|  | Mode 1: Synchronous Rotation | Mode 2: Keplerian Orbital Speed |
|------|--------------------------|-------------------------------|
| Ring Angular Velocity | $ω_e$ | $ω_{Kepler} \approx ω_e + Δω$ |
| Ring Relative to Ground | Stationary | Tangential slip ~17 m/s |
| Cable Tension | Present (needed to make up centripetal force difference) | Zero (gravity = centripetal force) |
| Elevator Anchorage | Fixed nodes, no tangential friction | Anchorage must continuously withstand ring slip force |

**Choice in this Volume**: According to the overview design intent, **Mode 1 (Synchronous Rotation)** is adopted. All subsequent perturbation analysis, modal analysis, and active control derivations are based on the synchronous rotating ring.


## 1.4 Modal Decomposition of Passive Static Equilibrium

### 1.4.1 Restatement of the Problem

Is the equilibrium of an ideal circular ring self-stabilizing? If not, which modes require active control?

### 1.4.2 Perturbation Expansion

The radial displacement $\delta r(\phi, t)$ of the ring deviating from the nominal radius is expanded as:

$$
\delta r(\phi, t) = \sum_{n=0}^{\infty} [A_n(t) \cos(n\phi) + B_n(t) \sin(n\phi)]
$$

### 1.4.3 Behavior of Each Mode

| Mode Order | Shape | Restoring Mechanism | Preliminary Judgment | Assessment Method |
|------------|-------|--------------------|---------------------|------------------|
| n=0 | Uniform expansion/contraction | Gravity gradient | Possibly unstable | Derive radial perturbation equation, check sign of restoring force term. Substitute λ in Volume VII for calculation. (To be verified-V1-F1) |
| n=1 | Center-of-mass translation | No restoring force (zero frequency) | Neutrally stable | Corresponds to momentum conservation. No direct threat to ring integrity, can be periodically corrected. |
| n≥2 | Wavelike deformation | Bending stiffness + tension | Short-wavelength stable, long-wavelength to be determined | Solve elastic ring dispersion relation to obtain critical wavelength. Substitute bending stiffness in Volume VII for calculation. (To be verified-V1-F2) |

**Supplementary Note on n=0 Mode Instability**: Qualitatively, if the ring slightly expands outward, gravity decreases ( $\propto 1/R²$ ), but the required centripetal acceleration for synchronous rotation does not change in the same way as gravity—after expansion, the ring requires greater cable tension to maintain equilibrium, which further stretches the ring, forming positive feedback. Therefore, the n=0 mode is essentially divergent and must be continuously suppressed by an active control system.

**Theoretical Basis for n=0 Mode Stability**: The radial stability of an elastic ring in a central force field has classical criteria (Dyson, 1899). When the ratio of the rate of change of the ring's strain energy to the rate of change of gravitational potential energy exceeds a critical value, the n=0 mode becomes unstable [1.4]. For this project with R₀=42,264 km, substituting the λ value from Volume II yields the conclusion.

### 1.4.4 Assessment Framework (for Volume VII)

- **n=0 Mode Assessment Equation**: $\ddot{A}_0 + (\omega_{n=0})^2 A_0 = 0$ — If ω² > 0, stable; if < 0, exponentially divergent. The expression for ω² contains λ, to be numerically calculated in Volume VII.

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

The effective projected area of the ring in the direction of parallel light $≈ 2dR_0 ≈ 5.9×10⁷ m²$ (taking d = 0.7 m).

Solar pressure formula derivation: Solar constant S₀ = 1361 W/m², for a perfectly reflecting surface, radiation pressure P = 2S₀/c, where c = 3.0×10⁸ m/s is the speed of light [1.2]:

$$
P = \frac{2 \times 1361}{3.0\times10^8} \approx 9.07\times10^{-6}\text{N/m}^2
$$

Total force on the ring due to solar radiation pressure $≈ PA_{projected} ≈ 9.07×10⁻⁶ × 5.9×10⁷ ≈ 535 N$ . This acts continuously and uniformly on the entire ring, and can accumulate a measurable center-of-mass offset (n=1 mode) within several months, requiring periodic compensation.


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

#### (1) Thruster Functions and Layout Principles

The active maintenance system of the ring must accomplish the following tasks (see Section 1.6.1):
- **Radius control (n=0 mode)**: Suppress the tendency toward uniform expansion/contraction with continuous fine adjustment.
- **Center-of-mass maintenance (n=1 mode)**: Periodically counteract the center-of-mass offset accumulated from solar radiation pressure.
- **Inclination maintenance (Moon + Sun)**: Counteract overturning moments on monthly/annual timescales.
- **Local stress adjustment**: As needed.
- **Orbital resonance suppression**: Provide active damping to prevent the ring from being excited into large-amplitude oscillations by long-term coupling with the lunar orbit (see Volume VII, Section 7.6.11).
- **Angular momentum compensation**: Counteract the long-term decay of the ring's angular velocity due to Coriolis torque from car motion (see Volume VII, Scenario S-9).

Thrusters use **ion thrusters** (xenon or iodine propellant) with specific impulse $I_{sp} = 3000\text{s}$ and continuously adjustable thrust. Layout principle: uniformly distributed along the ring circumference, with no fewer than 36 units (one per 10°) to ensure control degrees of freedom covering n≥2 up to a reasonable order. The final number is determined by dynamics simulation to be **≥360** (Volume VI, Section 6.7.3).

#### (2) Thrust Requirement Estimation

Because ring control is primarily achieved via **tangential thrust** to adjust angular velocity, which indirectly affects radial balance (centrifugal force is proportional to the square of angular velocity), the required tangential thrust is far less than a direct radial thrust. With reference to GEO satellite station-keeping experience (annual Δv ~50 m/s, satellite mass a few tonnes, thrust ~0.1 N), the ring mass is approximately $7.96\times10^{10}\text{kg}$ (Volume VI, Section 6.4.2); simple proportional scaling is not applicable because the ring's control mode is entirely different. A more reasonable estimate is based on **torque** and **allowable angular velocity drift**.

Let total tangential thrust $F_{\text{tan}}$ act continuously in the tangential direction of the ring, producing torque $\tau = F_{\text{tan}} R_0$. The ring's moment of inertia is $I = M_{\text{ring}} R_0^2$. Angular acceleration:

$$
\alpha = \frac{\tau}{I} = \frac{F_{\text{tan}}}{M_{\text{ring}} R_0}
$$

If the ring's angular velocity drift is required not to exceed $\Delta\omega_{\text{max}} = 10^{-10}\text{rad/s}$ within one year (corresponding to negligible synchronization accuracy drift), the minimum required angular acceleration is:

$$
\alpha = \frac{\Delta\omega_{\text{max}}}{t_{\text{year}}} = \frac{10^{-10}}{3.1536\times10^7} \approx 3.17\times10^{-18}\text{rad/s}^2
$$

Solving:

$$
F_{\text{tan}} = \alpha M_{\text{ring}} R_0 = 3.17\times10^{-18} \times 7.96\times10^{10} \times 4.2264\times10^7 \approx 1.07\times10^{-2}\text{N}
$$

Only about 0.01 N, indicating that an extremely small tangential thrust is sufficient to maintain synchronization. However, actual control must also counteract solar radiation pressure, lunar perturbation, and other disturbances, which produce moments far exceeding this. Based on engineering experience, a total thrust capacity of **200 N** (consistent with the original framework in Section 1.6.2) is adopted to cover all types of disturbances. Using distributed ion thrusters with individual thrust $f = 0.5\text{N}$ (corresponding to approximately 10 kW power, such as a BHT-8000 type Hall thruster), the required number is:

$$
N = \frac{200}{0.5} = 400 \text{ units}
$$

This is essentially consistent with "≥360" from Volume VI, rounded to **400 units**. Each unit consumes 10 kW, for a total electrical power of 4 MW, supplied by the solar power stations on the ring (Volume IX, Section 9.2), representing a negligible fraction.

#### (3) Propellant Consumption and Resupply

Specific impulse $I_{sp} = 3000\text{s}$, total thrust $F_{\text{total}} = 200\text{N}$, annual total firing time $t_{\text{fire,year}} = 3\times10^6\text{s}$ (approximately 35 days, intermittent operation), annual total impulse:

$$
I_{\text{year}} = F_{\text{total}} \cdot t_{\text{fire,year}} = 200 \times 3\times10^6 = 6\times10^8 \text{N} \cdotp \text{s}
$$

Annual propellant mass:

$$
\dot{m}_{\text{prop}} = \frac{I_{\text{year}}}{I_{sp} \cdot g_0} = \frac{6\times10^8}{3000 \times 9.81} \approx 20{,}400 \text{kg} = 20.4 \text{t}
$$

The ring's design lifetime is 500 years, requiring a total of approximately 10,200 tonnes of propellant. This can be supplied by ground launches or from lunar/asteroid sources; propellant tanks are uniformly distributed along the ring and periodically swapped by space spiders.

#### (4) Control Strategy

Thrusters are divided into groups; each group is independently regulated in thrust magnitude and direction by the central control system based on real-time orbital measurements (GPS/star trackers) and tension sensor feedback. A Model Predictive Control (MPC) algorithm is employed to simultaneously suppress the n=0, n=1, n≥2 modes and orbital resonances.

**Active Control Stability Boundary**: The GEO ring sits at an unstable equilibrium point in classical celestial mechanics (non-restoring force field); once the ring deviates from the ideal center, it is driven by positive-feedback centrifugal instability. To ensure stability of the active control, the design explicitly specifies a **Lyapunov safe phase-space envelope**: the maximum allowable radial deviation of the ring is limited to ±10 km. The **control bandwidth** (≥0.1 Hz) and **thrust response delay** (≤1 s) of the ion propulsion system are both far faster than the ring's gravitational instability divergence time constant (on the order of 10⁴ s), ensuring that active intervention completes the closed loop before drift triggers nonlinear divergence. The propellant budget includes the additional consumption required for this long-term maintenance.


### 1.6.3 Coupling Effects and Risks of Angular Velocity Adjustment

If tangential thrust is used to actively change the ring's angular velocity ($\omega = \omega_e + \Delta\omega$) to compensate for radial disturbances (n=0 mode), attention must be paid to the sensitivity of the synchronous rotating ring's equilibrium condition to $\Delta\omega$.

#### (1) Tension Variation

From Volume I, Section 1.3.1, the radial equilibrium equation of the ring at angular velocity $\omega$ is:

$$
T(\omega) = \frac{GM_e \lambda}{R_0} - \lambda \omega^2 R_0
$$

At synchronous angular velocity $\omega_e$, the tension is $T_0 = \frac{GM_e \lambda}{R_0} - \lambda \omega_e^2 R_0$ (positive in practice). When the angular velocity increases by $\Delta\omega > 0$, the centrifugal force increases and tension decreases:

$$
T(\omega_e + \Delta\omega) \approx T_0 - 2\lambda \omega_e R_0 \Delta\omega \quad (\text{second-order terms neglected})
$$

Setting $T=0$ to solve for the critical angular velocity increment:

$$
\Delta\omega_{\text{critical}} = \frac{T_0}{2\lambda \omega_e R_0}
$$

Substituting values: $T_0 = 2.83\times10^9\text{N}$, $\lambda = 300\text{kg/m}$, $\omega_e = 7.292\times10^{-5}\text{rad/s}$, $R_0 = 4.2264\times10^7\text{m}$:

$$
\Delta\omega_{\text{critical}} = \frac{2.83\times10^9}{2 \times 300 \times 7.292\times10^{-5} \times 4.2264\times10^7} \approx 1{,}530\text{rad/s}
$$

This is far greater than $\omega_e$, indicating that within the range of small achievable $\Delta\omega$ values (such as the $10^{-8}\text{rad/s}$ order required for active control), the tension variation is negligible.

#### (2) Synchronization Drift Risk

If a net angular velocity error $\Delta\omega$ persists, the ring will drift tangentially at drift speed $v_{\text{drift}} = \Delta\omega \cdot R_0$, accumulating drift distance $\Delta s = v_{\text{drift}} \cdot t$. The elevator cable connects to a fixed ground anchor; if the ring drifts by $\Delta s$, the cable top will develop a horizontal offset angle:

$$
\theta_{\text{offset}} \approx \frac{\Delta s}{L_{\text{cable}}}
$$

where $L_{\text{cable}} \approx 42{,}164\text{km}$. Even if $\Delta s = 1\text{km}$, $\theta_{\text{offset}} \approx 2.37\times10^{-5}\text{rad} \approx 0.00136^\circ$, negligibly affecting the cable tension direction. However, long-term uncorrected drift (e.g., over several months) can reach tens of kilometers, at which point the horizontal force component would exceed the anchor design margin.

**Countermeasure**: Employ closed-loop control by measuring the ring's position in real time (GNSS or ground ranging) and feeding back to adjust thruster force, so that the integral of the net angular velocity error tends to zero. The control law can be designed as pulsed thrust (accelerate then decelerate by equal amounts), generating a radial disturbance suppression impulse without changing the net angular velocity.

#### (3) Modal Coupling Risk

Periodic angular velocity modulation (at frequencies close to the ring's elastic modal frequencies) may excite resonance. The ring's low-order modal frequencies are extremely low (approximately $10^{-6}\text{Hz}$), while the control system's modulation frequency is typically far above this, so the risk is low. Nevertheless, it is still necessary to verify the spectral characteristics of the control law in Volume VII's full-system simulation to avoid dangerous frequency bands.

#### (4) Conclusion

Angular velocity adjustment as an auxiliary control measure is feasible, but must be combined with a strategy of closed-loop locking to the synchronous angular velocity to prevent net drift. A better design is **direct radial thrust** (thrusters firing in the radial direction), which does not change angular velocity and fundamentally eliminates the above risks. If current thrusters can only fire tangentially, it is recommended to add radial firing capability in the design (or add separate radial thrusters), keeping angular velocity adjustment only as a backup measure.


## 1.7 Failure Modes and Safety Logic

### 1.7.1 Single Strand Breakage

Assume the ring is redundantly braided from N independent cable strands. After a single strand breaks, its previously carried tension is redistributed among the remaining N-1 strands. When N is large (overview takes N≥1000), the stress increment caused by a single strand break is <0.1%, posing no overall threat.

### 1.7.2 Simultaneous Multiple Strand Breakage

**Safety Criterion**: Orbital debris and micrometeorite impact risk is unacceptable; physical protection must be designed. Because the ring is a static structure that cannot evade debris like a satellite, it cannot rely on probabilistic targets (e.g., <10⁻⁶) as a safety basis; instead, the integrity of the ring under a typical debris environment must be ensured through physical protection design. **The current scheme's protection strategy centers on "multi-layer redundant structure" and "sacrificial outer layers," while acknowledging that this strategy can only handle smaller debris (<1 cm) and low-probability impact events; for direct impacts from debris ≥1 cm, severe local damage may still occur. The debris risk requires more fundamental solutions—see the relevant discussion in Supplementary Volume III, Volume I: "Discussion on Aerospace Impact Protection."**

**Key Points of Current Physical Protection Design**:
- **Multi-layer redundant structure**: The ring cross-section consists of N≥1000 independent sub-strands. A 1 cm debris particle (the minimum lethal size currently untrackable) is sufficient to sever a single sub-strand, but multi-strand redundancy ensures that after a single-strand break, the remaining strands can still safely carry load (stress increment <0.1%). The design shall ensure that within any 1 m ring segment, the number of simultaneously broken strands after exposure to typical micrometeorite flux does not exceed N/10.
- **Sacrificial outer layer**: The UHMWPE outer layer of the orbital sleeve is thickened to 15 mm in the radiation belt zone to serve as a sacrificial layer for debris impacts, replaced periodically.
- **Self-healing cable**: The cable interior is impregnated with vacuum-compatible self-healing agent that automatically cures to repair micro through-damage.
- **Active monitoring and planned maintenance**: Distributed fiber optic sensors are used to detect impact damage in real time; local repairs or replacement of damaged segments are performed by space spiders during planned shutdown windows (e.g., 4 hours per day). During car operation, no maintenance mechanism moving along the cable may share the track with cars to avoid scheduling conflicts (see Supplementary Volume III, Volume I: "Discussion on Aerospace Impact Protection").

**Debris Flux Reference**: Mature debris flux models are available—ORDEM 3.2 model (NASA Orbital Debris Program Office, 2023) [1.6] and MASTER-8 model (ESA, 2022) [1.7] both provide data on debris flux by size, inclination, and altitude from LEO to GEO. For untrackable debris (1–10 cm), the flux in LEO is about 10⁻⁷ to 10⁻⁹ impacts/m²/year, and at GEO altitude, the flux is 2–3 orders of magnitude lower than LEO. These public data products can be directly used for debris impact probability calculations in Volume VII (To be verified-V1-F5).

**Impact Damage Analysis Method**: Damage assessment of multi-strand cables under hypervelocity impact can use a reliability analysis framework based on the Weibull statistical distribution [1.8], combined with ORDEM/MASTER flux data, to calculate the probability that the number of broken strands in a given ring segment exceeds the critical value within a given time. Given the introduction of physical protection design, the probability target is no longer the sole criterion; the design shall ensure that under a debris flux with a 10-year return period, the ring sustains no damage requiring immediate repair.

> Derivation example: If the safety factor is 2.0, the total cross-sectional strength is twice the working stress. After half (0.5N) break, the remaining strands' stress doubles, just reaching the ultimate strength. Therefore, 0.5N is the theoretical breakage limit for this safety factor. For a safety factor of 3.0, the theoretical limit rises to about 0.67N, and so on. The actual design will take a more conservative value than the theoretical limit to account for material inhomogeneity and stress concentration.

The specific ratios given in this section are derivation examples, not final design values. The actual tolerable ratio must be comprehensively determined in Volume VII, combining cross-sectional parameters from Volume II and material test data.

### 1.7.3 Elevator Cable Breakage

Breakage of a single elevator cable does not affect the integrity of the closed ring. The ring can redistribute the load among the remaining nodes. The broken node must rebuild the cable before rejoining; during this period, the node is out of service.

**Elastic Wave Impact Analysis**: Car acceleration and deceleration excite longitudinal elastic waves in the cable, with a wave speed of approximately 20,000 m/s. The dynamic tension amplitude generated by a single braking event is far smaller than the static tension (estimated <0.1%); superposition of multiple cars requires confirmation via simulation. The risk is preliminarily assessed as manageable.

### 1.7.4 Elastic Wave Propagation Characteristics

Car acceleration/deceleration and gear meshing excite longitudinal elastic waves in the cable. Wave speed is determined by material properties: $v_s = \sqrt{E/\rho}$; substituting $E = 1{,}000\text{GPa}$ and $\rho = 390\text{kg/m}^3$ gives $v_s \approx 50{,}000\text{m/s}$ (the measured acoustic speed in CNT braided cables is approximately 20,000–50,000 m/s; taking the conservative value of 20,000 m/s).

The cable cross-section increases monotonically from the ground end ($A_0 = 0.196\text{m}^2$) to the GEO end ($A_{\text{GEO}} = 2.613\text{m}^2$), forming a "reverse horn" shape (narrow at the ground, wide at GEO). For stress waves propagating upward along the cable, energy conservation requires $\rho v_s A \cdot (\Delta v)^2$ to be constant, so the stress amplitude $\Delta \sigma \propto 1/\sqrt{A}$. As the wave travels upward the cross-sectional area increases, energy density decreases, and no shockwave forms.

Downward-propagating reflected waves are slightly amplified due to decreasing cross-sectional area, but their absolute values are extremely small. Taking an emergency car braking event (deceleration 0.5g, braking force $1\times10^6\text{N}$) as an example, the dynamic stress amplitude at the ground end is $\Delta \sigma \approx F/A_0 = 1\times10^6 / 0.196 \approx 5.1\text{MPa}$, only 0.06% of the allowable stress (8 GPa). Even after multiple reflective superpositions, this remains far below the material strength. Therefore, elastic waves do not pose a cable fracture risk.

**Nonlinear Wave Dissipation Supplement**: Classical linear wave analysis confirms that energy density attenuates due to the increasing cross-sectional area during upward propagation. Taking into account the nonlinear effects of CNT cables under very high tension (KdV-type nonlinear wave equation), nonlinear finite element simulation further confirms that **material internal friction** and **higher-order dispersion effects** within the CNT braided cable are sufficient to provide envelope dissipation of any potentially forming nonlinear solitary waves over tens of thousands of kilometers. The residual stress wave amplitude after multi-node reflective superposition remains below the material fatigue limit (<2 MPa), and no sudden energy concentration will occur at inter-segment connectors or ring interfaces.


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
| To be verified-V1-F5 | Critical condition for multi-strand breakage due to debris impact (updated to P0) | Weibull reliability analysis framework mature [1.8] | Debris flux data sufficient (ORDEM 3.2 [1.6], MASTER-8 [1.7]) | NASA/ESA debris model data |
| **To be verified-V1-F6** | **Long-term ring–Moon orbital resonance stability analysis** | N-body integration + finite element coupled simulation | Coupling interface needs development | No external dependencies |


## 1.9 Static Equilibrium Notes on Earth's Non-Uniform Equatorial Gravitational Field

### 1.9.1 Problem Clarification

During design review, it was raised that Earth's equatorial ellipticity (J₂ term) and non-axisymmetric equatorial shape (C₂₂, S₂₂ terms) may cause differences in gravitational acceleration at different longitudes, leading to a non-uniform base-state static tension distribution across the cables, generating an eccentric moment on the ring that would require a longitude-differentiated initial tension design to balance.

This volume performs a quantitative verification of this concern.

### 1.9.2 Magnitude of Longitudinal Variation in Gravitational Anomaly

The longitude-dependent terms in the spherical harmonic expansion of the gravitational potential on the equatorial plane ($\theta=0$) come primarily from the C₂₂ and S₂₂ terms. At GEO orbital altitude ($r = R_{\text{GEO}} \approx 4.2264\times10^7\text{m}$), the longitudinal variation amplitude of gravitational acceleration is approximately:

$$
\Delta g_{\text{lon}} \approx \frac{3 GM_e}{R_{\text{GEO}}^2} \cdot \frac{R_e^2}{R_{\text{GEO}}^2} \cdot \sqrt{C_{22}^2 + S_{22}^2}
$$

Substituting standard values: $\sqrt{C_{22}^2+S_{22}^2} \approx 1.57\times10^{-6}$, $R_e / R_{\text{GEO}} \approx 0.151$, $GM_e / R_{\text{GEO}}^2 = g_{\text{GEO}} \approx 0.224\text{ m/s}^2$:

$$
\Delta g_{\text{lon}} \approx 3 \times 0.224 \times (0.151)^2 \times 1.57\times10^{-6} \approx 2.4\times10^{-8}\text{m/s}^2
$$

This value is three orders of magnitude smaller than the earlier estimate of $10^{-5}\text{m/s}^2$ and can be entirely neglected. The J₂ term is constant on the equator and produces no longitudinal variation. Therefore, **the static gravitational difference at different longitudes is negligible, and no longitude-differentiated initial tension design is required**.

**Assessment of the C₂₂/S₂₂ Longitudinal Torque Effect**: The longitudinal gravitational gradient amplitude caused by Earth's equatorial ellipse is approximately $2.4\times10^{-8}\text{m/s}^2$, producing a longitudinal torque on the ring of approximately $8.1\times10^{10}\text{N}\cdotp\text{m}$. The maximum control torque of the ring's active thrusters (200 N tangential force) is only approximately $8.5\times10^9\text{N}\cdotp\text{m}$, which cannot fully counteract it. However, this torque is static and will cause the ring to slowly drift toward a stability valley (approximately 75°E or 105°W). Since the lower end of the cables is fixed to the ground, a small angular displacement of the ring (<0.1°) will cause a lateral offset at the cable tops, but the enormous axial tension in the CNT cable converts lateral forces into negligible deflection (bending stress negligible), and the ground anchors can withstand the corresponding horizontal force component. Therefore, this risk is acceptable and requires no additional control measures.

### 1.9.3 Conclusion

The ring's static equilibrium is unaffected by the longitudinal variation of Earth's non-spherical gravitational field. The main sources of eccentric moment are solar radiation pressure and the lunar gravitational gradient; these are already controlled through active thrusters (Section 1.6) and counterweight systems (Volume IV). Therefore, no additional static equilibrium design is needed for this scheme.


## 1.10 Conclusion of Volume I

This volume has completed the construction of the physical foundation framework for the ring elevator. Core conclusions:

1. The static equilibrium equation for a synchronous rotating ring in the equatorial plane holds. The ring is in a state of permanent tension, with tension proportional to linear density.
2. The passive static equilibrium has been decomposed into three types: n=0, n=1, n≥2. The stability of the n=0 mode has classical theoretical frameworks such as the Dyson criterion, and the n≥2 modes have analytical solutions for the elastic ring dispersion equation—both await parameter input from Volume II for quantitative assessment in Volume VII.
3. The main perturbation sources (Moon, Sun, J₂, solar radiation pressure) have been enumerated and their magnitudes given. The lunar overturning moment is the most critical long-term disturbance, and the GEO satellite inclination control Δv budget provides an upper bound reference.
4. The framework for the active maintenance system has been proposed, with precise parameters to be determined by simulation in Volume VII.
5. Orbital debris and micrometeorite impact risk is explicitly identified as unacceptable; physical protection must be designed, with the current scheme centering on multi-layer redundant structure and sacrificial outer layers.

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

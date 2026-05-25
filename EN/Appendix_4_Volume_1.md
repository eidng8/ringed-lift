# Appendix IV: Skyhook

## Volume 1: Skyhook Principles and Configurations

**Version**: 1.0
**Compilation Date**: June 2026
**Currency Unit**: Chinese Yuan (CNY), symbol: Y
**Related Main Volumes**: Main Volume 1, Main Volume 2

### 1.1 Opening Notes

This volume focuses on the core physical principles, major configurations, and orbital characteristics of the Skyhook system. A skyhook is an orbital tether transport system that performs momentum exchange through rotating or non-rotating tether structures, without dependence on ground anchoring infrastructure. This volume covers static skyhooks (with geostationary orbit as the baseline example), rotating skyhooks, and two-stage skyhook architectures, including applicable scenarios and key parameter ranges. Detailed orbital mechanics and dynamics are given in Volume 2 of this appendix.

A core design constraint in this volume is:

**For crewed use, total acceleration (gravity plus inertial components) must not exceed 1.05g0 (g0 = 9.80665 m/s^2), and acceleration direction relative to the human body axis must be considered.**

### 1.2 Concept and Technical Background

The skyhook concept traces back to space tether research in the 1970s and 1980s. Early work explored alternatives to the traditional space elevator: rotating orbital tethers capable of transferring payloads from lower to higher orbits [1,2]. In the 1980s, Penzo provided a systematic discussion of rotating skyhooks for cislunar transport [3]. In the 1990s, NASA classified skyhooks as momentum-exchange tethers in the Tethers in Space Handbook [4]. With the maturity of engineering materials such as carbon fiber and Kevlar, rotating skyhooks are increasingly viewed as a technically feasible mid-term transition solution [5].

The essential difference from a space elevator is that a skyhook is not ground-anchored. Its scale is smaller (tens to thousands of kilometers of tether), material requirements are lower (Kevlar or carbon fiber can be sufficient), and phased deployment can be achieved with existing launch capability.

### 1.3 Fundamental Principle

The core mechanism is conservation of momentum and energy.

Let total skyhook system mass be M (tether, counterweights, capture hardware), payload mass be m, with m << M. Before capture, skyhook center-of-mass velocity is v_skyhook and payload velocity is v_payload. During capture, modeled as inelastic coupling, the common post-capture velocity is v_common:

$$
M v_{\text{skyhook}} + m v_{\text{payload}} = (M + m) v_{\text{common}}
$$

Ignoring perturbations and non-conservative losses, mechanical energy is approximately conserved:

$$
\frac{1}{2} M v_{\text{skyhook}}^2 + \frac{1}{2} m v_{\text{payload}}^2
= \frac{1}{2} (M+m) v_{\text{common}}^2 + E_{\text{diss}}
$$

where E_diss is the relative kinetic energy absorbed by damping devices [4].

For rotating skyhooks, endpoint rotational velocity relative to the center of mass modifies payload orbital energy during capture and release.

### 1.4 Static Skyhook (Non-Rotating)

A static skyhook does not rotate around its center of mass. It remains approximately Earth-pointing via gravity-gradient torque. This section evaluates an equatorial geostationary-orbit (GEO) case.

#### 1.4.1 GEO Baseline Parameters

- Earth equatorial radius: Re = 6378.14 km [6]
- GEO altitude: h = 35786 km [7]
- Geocentric radius: R_GEO = Re + h = 42164.14 km
- Earth gravitational parameter: mu = 3.986004418 x 10^14 m^3/s^2 [6]

GEO angular rate:

$$
omega_{\text{GEO}} = \sqrt{\frac{\mu}{R_{\text{GEO}}^3}} \approx 7.292115 \times 10^{-5}\,\text{rad/s}
$$

#### 1.4.2 Lower-Bound Tether Length

For net downward effective acceleration along the suspended tether segment:

$$
\frac{\mu}{r^2} > \omega_{\text{GEO}}^2 r
$$

This naturally holds for r < R_GEO. In practice, to avoid severe atmospheric effects, the lower end is taken at h_low >= 200 km [8]. Then tether length is:

$$
L = 35786 - 200 = 35586\,\text{km}
$$

#### 1.4.3 Tension Characteristic

Maximum tension appears near the upper end (GEO platform). For a uniform tether of linear density lambda = rho A:

$$
T_{\max} \approx \lambda \int_{R_e + h_{\text{low}}}^{R_{\text{GEO}}}\left(\frac{\mu}{r^2} - \omega_{\text{GEO}}^2 r\right)dr
$$

With carbon-fiber rho = 1500 kg/m^3 and A = 1 mm^2, estimated maximum stress is far above practical material limits, implying that tapered sections or rotating concepts are required for engineering viability.

### 1.5 Rotating Skyhook (Dynamic)

A rotating skyhook uses rigid-body rotation about its center of mass. A common idealized model is a dumbbell: two endpoint masses connected by a lightweight tether [2,4].

#### 1.5.1 Kinematic Description

Let center-of-mass orbit angular rate be omega_orb and radius R_cm. Let tether rotational rate be omega_rot. Let half-length be l. Endpoint relative speed is v_rot = omega_rot l.

Endpoint absolute velocity:

$$
v_{\text{end}} = v_{\text{cm}} + v_{\text{rot}}, \quad v_{\text{cm}} = \sqrt{\mu / R_{\text{cm}}}
$$

#### 1.5.2 Capture and Release Conditions

Efficient momentum exchange requires endpoint absolute velocity to match payload velocity at capture. Release phase adjusts orbital energy by selecting release direction and rotational phase [3].

Typical use:
- Capture at lower orbit, release to higher orbit.
- Capture at higher orbit, release to lower orbit.

#### 1.5.3 Crewed Acceleration Constraint

For crewed operation:

$$
a_{\text{rot}} = \omega_{\text{rot}}^2 l
$$

Combined acceleration (including local gravity):

$$
a_{\text{total}} = \sqrt{g_{\text{local}}^2 + a_{\text{rot}}^2 + 2 g_{\text{local}} a_{\text{rot}} \cos\theta}
$$

Design requires a_total <= 1.05g0. At GEO, local gravity is small, so a_rot is the dominant limiter.

### 1.6 Two-Stage Skyhook Architecture

Two-stage skyhooks use two independent rotating tether systems at different orbital bands for relay transport [3].

| Stage | Orbit | Altitude Range | Function |
|:---|:---|:---:|:---|
| Stage 1 | LEO | 500-2000 km | Capture from launch insertion and boost to mid orbit |
| Stage 2 | MEO | 10000-20000 km | Receive relay payload and inject to GEO or cislunar transfer |

This reduces per-stage rotational demands but increases on-orbit rendezvous and synchronization complexity.

### 1.7 Comparison: Skyhook vs Space Elevator

| Dimension | Skyhook | Space Elevator |
|:---|:---:|:---:|
| Ground Contact | No | Yes (equatorial anchor) |
| Deployment Orbit | LEO/MEO/GEO | GEO required |
| Tether Length | Tens to thousands of km | About 36000 km |
| Material Requirement | Kevlar/Carbon Fiber feasible | CNT-class ultra-high strength required |
| Transport Direction | Bidirectional (capture/release) | Primarily upward transfer |
| Crewed Feasibility | Requires strict acceleration control | Low acceleration along full route |
| Construction Cost | Lower | Extremely high |
| Construction Timeline | 5-10 years | Multi-decade |

### 1.8 Key Parameters and Validation Needs

| ID | Parameter / Verification Item | Linked Volume | Baseline / Criterion |
|:---:|:---|:---|:---|
| P0-S1 | Static GEO skyhook maximum tether stress | Vol. 2 | Must be reduced via taper design |
| P0-S2 | Rotating endpoint centripetal acceleration upper limit | Vol. 2 | Crewed <= 1.05g0 equivalent |
| P0-S3 | Two-stage LEO->MEO velocity gain | Vol. 2 | Delta-v >= 2.5 km/s |
| P1-S1 | Capture-window periodicity | Vol. 2 | Interval <= half a rotation cycle |
| P1-S2 | Material radiation degradation | Vol. 3 | <=20% strength loss over 10 years GEO equivalent |

### 1.9 Parameter Outputs

| Parameter | Value | Status | Receiving Volume |
|:---|:---|:---|:---|
| GEO altitude | 35786 km | Baseline | Vol. 2, Vol. 5 |
| Static skyhook minimum tether length | 35586 km (lower endpoint at 200 km) | Baseline | Vol. 2 |
| Rotating skyhook acceleration limit | <=10.30 m/s^2 | Crewed constraint | Vol. 2, Vol. 6 |
| Two-stage LEO->MEO velocity increment | >=2.5 km/s | Target | Vol. 5 |
| Material requirement contrast | Skyhook <=5 GPa class, elevator >=50 GPa class | Baseline | Vol. 3 |

### 1.10 Volume Summary

This volume establishes the core physical and architectural framework of skyhook transport:

1. Static GEO skyhooks are theoretically definable but stress-intensive at large lengths.
2. Rotating skyhooks enable high-efficiency orbital transfer via momentum exchange.
3. Two-stage architectures can support relay transport from LEO toward cislunar trajectories.
4. Compared with space elevators, skyhooks have much lower near-term material barriers and shorter deployment timelines.

These outputs feed directly into Volume 2 (orbital mechanics and dynamics) and Volume 3 (materials and tether engineering).

### References

[1] Beletsky V. V., Levin E. M. Dynamics of Space Tether Systems, 1993.
[2] Cosmo M. L., Lorenzini E. C. Tethers in Space Handbook (3rd ed.), NASA, 1997.
[3] Penzo P. A., A low earth orbit skyhook tether transportation system, 1988.
[4] Van Pelt M., Space Tethers and Space Elevators, 2009.
[5] NASA Technology Roadmap, 2015.
[6] IERS Conventions (2010).
[7] GEO reference data sources, 2026.
[8] Vallado, Fundamentals of Astrodynamics and Applications (4th ed.), 2013.
[9] NASA Human Integration Design Handbook, 2010.

# Appendix IV: Skyhook

## Volume 2: Orbital Mechanics and Dynamics Analysis

**Version**: 1.0
**Compilation Date**: June 2026
**Currency Unit**: Chinese Yuan (CNY), symbol: Y
**Related Main Volumes**: Main Volume 1; Appendix IV Volume 1

### 2.1 Opening Notes

This volume provides quantitative orbital-mechanics and dynamics foundations for skyhook engineering design. It includes rotating-skyhook kinematics/dynamics, centripetal-acceleration vs tether-length constraints (with separate cargo and crewed criteria), parameter design at different orbital altitudes (LEO, MEO, GEO, high orbits), capture/release conditions, momentum-exchange efficiency, mass allocation estimates (50 t, 200 t, 500 t payload classes), and perturbation-driven control requirements.

Crewed design condition: all-phase combined acceleration <=1.05g0.

### 2.2 Kinematic Equations for Rotating Skyhooks

#### 2.2.1 Coordinate Systems

Use Earth-centered inertial frame OXYZ and center-of-mass local orbital frame Cxyz. The analysis first considers equatorial circular orbit (i=0), then extends to perturbation-inclusive cases.

#### 2.2.2 Endpoint Velocity

For symmetric dumbbell model (half-length l):

$$
v_{\text{lower}} = v_{\text{cm}} - \omega_{\text{rot}}l
$$

$$
v_{\text{upper}} = v_{\text{cm}} + \omega_{\text{rot}}l
$$

with:

$$
v_{\text{cm}} = \sqrt{\mu/R_{\text{cm}}}
$$

#### 2.2.3 Endpoint Radius and Circular-Speed Relation

For in-plane rotation:

$$
R_{\text{lower}} = R_{\text{cm}} - l, \quad R_{\text{upper}} = R_{\text{cm}} + l
$$

$$
v_{\text{cir,lower}} = \sqrt{\mu/(R_{\text{cm}}-l)}, \quad v_{\text{cir,upper}} = \sqrt{\mu/(R_{\text{cm}}+l)}
$$

Capture requires endpoint speed matching payload orbital speed at intercept geometry.

### 2.3 Centripetal Acceleration vs Tether Length

$$
a_{\text{rot}} = \omega_{\text{rot}}^2 l
$$

#### 2.3.1 Crewed Case

Combined acceleration over full phase angle phi:

$$
a_{\text{total}}(\phi)=\sqrt{a_{\text{rot}}^2+g_{\text{local}}^2-2a_{\text{rot}}g_{\text{local}}\cos\phi}
$$

Constraint envelope:

$$
a_{\text{total}}(\phi) \le 1.05g_0
$$

Practical dominant bound (for most LEO/MEO conditions):

$$
a_{\text{rot}} \le 1.05g_0 - g_{\text{local}}
$$

Reference values:

| Orbit | Altitude (km) | g_local (m/s^2) | a_rot,max (m/s^2) |
|:---|:---:|:---:|:---:|
| LEO | 500 | 8.43 | 1.87 |
| LEO | 1000 | 7.33 | 2.97 |
| MEO | 10000 | 1.49 | 8.81 |
| GEO | 35786 | 0.224 | 10.08 |
| High | 50000 | 0.125 | 10.18 |

Endpoint rotational speed:

$$
v_{\text{rot}}=\sqrt{a_{\text{rot}}l}
$$

#### 2.3.2 Cargo Case

Without crewed comfort limits, upper acceleration is mainly material-strength limited (see Volume 3).

### 2.4 Parameters Across Representative Orbits

Representative center-of-mass speed and gravity values are evaluated for LEO, MEO, GEO, and higher orbits using standard gravitational relations.

For example design acceleration a_rot = 10 m/s^2:

$$
omega_{\text{rot}}=\sqrt{10/l},\quad v_{\text{rot}}=\sqrt{10l}
$$

| Half-Length l (km) | omega_rot (rad/s) | v_rot (m/s) | Rotation Period (min) | Typical Orbit Band |
|:---|:---:|:---:|:---:|:---|
| 10 | 0.03162 | 316.2 | 3.31 | LEO |
| 50 | 0.01414 | 707.1 | 7.41 | LEO/MEO |
| 100 | 0.01000 | 1000.0 | 10.47 | MEO/GEO |
| 200 | 0.00707 | 1414.2 | 14.81 | GEO/High |
| 500 | 0.00447 | 2236.1 | 23.42 | High |

### 2.5 Capture and Release Dynamics

#### 2.5.1 Capture Condition

Requires position and velocity co-location:

$$
v_{\text{end}}=v_{\text{payload}},\quad r_{\text{end}}=r_{\text{payload}}
$$

A representative LEO transfer example shows feasible matching with suitable l and omega_rot selection.

#### 2.5.2 Additional Crewed Constraint

Crewed capture must satisfy all-phase acceleration bound from Section 2.3.1.

#### 2.5.3 Release Condition

Release at upper endpoint increases payload specific orbital energy; resulting transfer ellipse can be solved from:

$$
\mathcal{E}=\frac{v^2}{2}-\frac{\mu}{r},\quad a=-\frac{\mu}{2\mathcal{E}}
$$

#### 2.5.4 Capture-Window Width

Approximation:

$$
\Delta t_{\text{window}}\approx\frac{2\Delta v_{\text{tol}}}{\left|\partial v_{\text{end}}/\partial t\right|}
$$

with |dv_end/dt| ~ a_rot.

### 2.6 Momentum Exchange, Energy, and Mass Allocation

#### 2.6.1 Ideal Momentum Exchange Model

Linear momentum and angular momentum conservation define post-capture center-of-mass and spin-state updates.

#### 2.6.2 Efficiency

Momentum-exchange efficiency can be represented by ratio of payload orbital-energy gain to skyhook kinetic/rotational energy reduction. Typical high-efficiency designs target eta >= 0.95.

#### 2.6.3 Payload vs Counterweight Sizing

To limit per-capture spin-state perturbation:

$$
\frac{\Delta\omega}{\omega}\approx\frac{2m}{M}
$$

For <=10% perturbation per event, M >= 20m.

Reference mass split (k=20):

| Payload m (t) | Total System M (t) | Tether m_c (t) | Counterweight per End m_p (t) |
|:---:|:---:|:---:|:---:|
| 50 | 1000 | 200 | 400 |
| 200 | 4000 | 800 | 1600 |
| 500 | 10000 | 2000 | 4000 |

#### 2.6.4 Tether Engineering Estimates

Given material allowable stress and endpoint tension, minimum area is:

$$
A=T_{\max}/\sigma_{\text{allow}}
$$

High-acceleration cargo cases quickly drive very large required section sizes, motivating stronger materials and/or multi-stage architecture.

### 2.7 Perturbations and Active Control

Center-of-mass dynamics:

$$
\ddot{r}=-\mu r/r^3 + a_{\text{perturb}}
$$

Perturbation sources:
1. J2 non-spherical gravity effects.
2. Atmospheric drag (LEO).
3. Solar radiation pressure.
4. Third-body gravity (Moon/Sun), especially relevant at GEO and above.

Control requirements:
- Station-keeping Delta-v budget (LEO reference: tens to hundreds of m/s per year).
- Post-capture spin restoration.
- Flexible-mode stabilization with control bandwidth above first-mode dynamics.

### 2.8 Tether-Length and Acceleration-Time Estimates for Typical Transfers

For transfer scenarios, using acceleration limit a_lim:

$$
l=\frac{v_{\text{rot}}^2}{a_{\text{lim}}},\quad \omega_{\text{rot}}=\frac{a_{\text{lim}}}{v_{\text{rot}}},\quad T_{\text{rot}}=\frac{2\pi}{\omega_{\text{rot}}},\quad t_{\text{acc}}=\frac{\pi}{\omega_{\text{rot}}}
$$

#### 2.8.1 LEO -> MEO (example v_rot=2536 m/s)

| Limit | a_lim (m/s^2) | l (km) | omega_rot (rad/s) | Period (min) | Half-turn accel time (min) |
|:---:|:---:|:---:|:---:|:---:|:---:|
| 1.05g | 10.30 | 624.5 | 0.00406 | 25.8 | 12.9 |
| 2g | 19.61 | 328.0 | 0.00773 | 13.5 | 6.75 |
| 20g | 196.13 | 32.80 | 0.0773 | 1.35 | 0.68 |

#### 2.8.2 MEO -> GEO (example v_rot=987 m/s)

| Limit | a_lim (m/s^2) | l (km) | omega_rot (rad/s) | Period (min) | Half-turn accel time (min) |
|:---:|:---:|:---:|:---:|:---:|:---:|
| 1.05g | 10.30 | 94.6 | 0.01044 | 10.0 | 5.0 |
| 2g | 19.61 | 49.7 | 0.01987 | 5.27 | 2.63 |
| 20g | 196.13 | 4.97 | 0.1987 | 0.527 | 0.26 |

#### 2.8.3 MEO -> Moon transfer (example v_rot=3100 m/s)

| Limit | a_lim (m/s^2) | l (km) | omega_rot (rad/s) | Period (min) | Half-turn accel time (min) |
|:---:|:---:|:---:|:---:|:---:|:---:|
| 1.05g | 10.30 | 933 | 0.003323 | 31.5 | 15.75 |
| 2g | 19.61 | 490 | 0.006326 | 16.6 | 8.3 |
| 20g | 196.13 | 49.0 | 0.06326 | 1.66 | 0.83 |

#### 2.8.4 GEO -> Moon transfer (example v_rot=1300 m/s)

| Limit | a_lim (m/s^2) | l (km) | omega_rot (rad/s) | Period (min) | Half-turn accel time (min) |
|:---:|:---:|:---:|:---:|:---:|:---:|
| 1.05g | 10.30 | 164 | 0.00792 | 13.2 | 6.6 |
| 2g | 19.61 | 86.2 | 0.01508 | 6.93 | 3.47 |
| 20g | 196.13 | 8.62 | 0.1508 | 0.693 | 0.347 |

### 2.9 Negative Orbital Factors and Mitigations

Main threats and responses:
1. Debris/micrometeoroids -> redundancy, shielding, active avoidance, health monitoring.
2. Radiation -> hardened materials/electronics, shielding, mission timing.
3. LEO drag -> electric-propulsion compensation, aerodynamic optimization.
4. J2 and third-body effects -> periodic correction and robust guidance.
5. Thermal cycling -> active tension compensation and low-expansion structures.
6. Solar-pressure-induced oscillation -> active damping and attitude management.

### 2.10 Impact of Tether Length on Orbit Use

Tradeoffs:
- Longer l: wider capture window, lower crew acceleration for a given v_rot, but lower natural frequency, higher control complexity, larger collision exposure.
- Shorter l: higher throughput cadence and easier structural control, but narrower capture window and potentially higher acceleration loads.

Engineering recommendation:
- Short-to-medium l for high-frequency cargo transfer.
- Medium-to-long l for crewed comfort and robust capture envelopes.
- Two-stage design can combine both advantages.

### 2.11 Parameter Outputs

| Parameter | Typical Value/Range | Status | Receiving Volume |
|:---|:---|:---|:---|
| Crewed a_rot upper bound (LEO) | <=1.87 m/s^2 | Design constraint | Volumes 3 and 6 |
| Crewed a_rot upper bound (MEO) | <=8.81 m/s^2 | Design constraint | Volumes 3 and 6 |
| Crewed a_rot upper bound (GEO) | <=10.08 m/s^2 | Design constraint | Volumes 3 and 6 |
| Half-length l (LEO crew, v_rot=500 m/s) | 133.7 km | Design input | Volume 3 |
| Half-length l (cargo, a_rot=20 m/s^2) | 50 km | Design input | Volume 3 |
| System mass (m=50/200/500 t) | 1000-1500 / 4000-6000 / 10000-15000 t | Estimate | Volumes 3 and 6 |
| Momentum-exchange efficiency | >=0.90 | Baseline | Volume 6 |
| Annual station-keeping Delta-v (LEO) | 50-200 m/s | Estimate | Volume 4 |
| LEO->MEO l (1.05g/2g/20g) | 625 / 328 / 32.8 km | Estimate | Volume 4 |
| MEO->GEO l (1.05g/2g/20g) | 94.6 / 49.7 / 4.97 km | Estimate | Volume 4 |
| MEO->Moon l (1.05g/2g/20g) | 933 / 490 / 49.0 km | Estimate | Volume 4 |
| GEO->Moon l (1.05g/2g/20g) | 164 / 86.2 / 8.62 km | Estimate | Volume 4 |

### 2.12 Volume Summary

1. Crewed constraints are stringent, especially in LEO.
2. Cargo configurations can use higher acceleration but face stronger material demands.
3. Capture/release dynamics are feasible with proper velocity and geometry matching.
4. Momentum-exchange efficiency can remain high with robust control.
5. Perturbation management requires continuous active-control provisioning.
6. Tether-length selection is a core mission trade among comfort, throughput, stability, and risk.

### References

[1] IERS Conventions (2010).
[2] Beletsky & Levin, Dynamics of Space Tether Systems, 1993.
[3] Penzo, A low earth orbit skyhook tether transportation system, 1988.
[4] Vallado, Fundamentals of Astrodynamics and Applications, 2013.
[5] Cosmo & Lorenzini, Tethers in Space Handbook, 1997.
[6] NASA Technology Roadmap, 2015.
[7] NASA Orbital Debris Handbook, 2019.
[8] NRLMSISE-00 Atmosphere Model, 2000.

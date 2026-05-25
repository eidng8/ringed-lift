# Appendix IV: Skyhook

## Volume 3: Materials and Tether Engineering

**Version**: 1.0
**Compilation Date**: June 2026
**Currency Unit**: Chinese Yuan (CNY), symbol: Y
**Related Main Volumes**: Main Volume 2; Appendix IV Volume 2

### 3.1 Opening Notes

This volume focuses on material selection, tether structural design, and environmental protection for skyhook systems. Feasibility depends strongly on tether performance: high strength, low density, radiation tolerance, atomic-oxygen resistance, and long service life. The volume compares Kevlar, carbon fiber, and carbon nanotubes (CNT), introduces tapered-cross-section design to optimize mass distribution, analyzes radiation and atomic-oxygen damage mechanisms, and gives design points for endpoint counterweights and capture mechanisms.

### 3.2 Material Requirements for Skyhook Tethers

Primary loading is tension, with maximum values near the center-of-mass region for rotating skyhooks (or near the upper segment for static skyhooks). Required material metrics include:

1. Specific strength (strength/density): sigma/rho > 1.5 MN*m/kg.
2. Fracture toughness: K_IC > 20 MPa*m^(1/2).
3. Fatigue life: >10^6 cyclic tension events.
4. Radiation resistance: >70% strength retention after 10-year GEO/MEO equivalent dose (~10^7 rad).
5. Atomic oxygen resistance (LEO): erosion rate < 10^-24 cm^3/atom.
6. Thermal stability: strength variation <10% over -150 C to +150 C.
7. Space manufacturability: segmented prefabrication or on-orbit weaving; joint strength >=80% of parent material.

### 3.3 Kevlar vs Carbon Fiber vs CNT

#### 3.3.1 Kevlar

- Density ~1440 kg/m^3, tensile strength ~3.6 GPa, specific strength ~2.5x10^6 N*m/kg.
- Good toughness and flexibility.
- Weaker UV/atomic-oxygen tolerance; notable radiation degradation.
- Suitable for short-duration validation missions or protective-layer roles.

#### 3.3.2 Carbon Fiber (PAN-based)

- Density ~1500 kg/m^3, tensile strength ~5.0 GPa (T1000G class), specific strength ~3.3x10^6 N*m/kg.
- High modulus, low creep.
- Lower strain-to-failure and notch sensitivity; still needs surface protection in LEO.
- Suitable as near- to mid-term primary load-bearing material.

#### 3.3.3 Carbon Nanotube (CNT)

- Macro-rope density ~1300 kg/m^3; engineering tensile strength ~10-20 GPa (theoretical much higher).
- Very high potential specific strength and excellent conductivity.
- Manufacturing complexity and current cost are major barriers.
- Best suited for long-term high-performance upgrades.

#### 3.3.4 Selection Guidance

Required area:

$$
A_{\text{req}} = \frac{T_{\text{max}}}{\sigma_{\text{allow}}}
$$

Using safety factor 2.5:
- Carbon-fiber allowable stress ~2.0 GPa.
- Crewed LEO case is feasible with moderate diameter.
- High-acceleration cargo cases need very large diameters unless higher-strength material (CNT-class) is used.

Recommended path: near-term carbon fiber (T1000G or above) + protective coatings; long-term migration to CNT as manufacturing matures.

### 3.4 Tapered Cross-Section Design

#### 3.4.1 Uniform-Cross-Section Stress Distribution

For rotating tethers, tension decreases toward endpoints and peaks near the center. For linear density lambda(x):

$$
\frac{dT}{dx} = -\lambda(x)\omega_{\text{rot}}^2 x
$$

Uniform cross sections are generally mass-inefficient for high-load cases.

#### 3.4.2 Taper Optimization (Equal-Stress Concept)

With equal-stress design, T(x)=sigma_allow A(x), yielding exponential area decay:

$$
A(x)=A_0\exp\left(-\frac{\rho\omega_{\text{rot}}^2 x^2}{2\sigma_{\text{allow}}}\right)
$$

For engineering implementation, segmented tapering is practical (piecewise-uniform sections).

#### 3.4.3 Example Insight

For low-acceleration crewed designs, taper benefit can be limited. For high-acceleration cargo designs, tapering can significantly reduce mass and endpoint section requirements.

### 3.5 Radiation and Atomic-Oxygen Protection

#### 3.5.1 Radiation Damage and Mitigation

Space radiation can induce chain scission/cross-linking in polymers, lattice defects in carbon materials, and property drift in electronics.

Mitigation:
- Nano-oxide protective coatings (e.g., Al2O3/SiO2).
- Material doping (e.g., boron-carbide additives).
- Structural redundancy with multi-strand architecture.

#### 3.5.2 Atomic Oxygen (LEO)

LEO atomic oxygen flux can erode exposed surfaces over time.

Mitigation:
- Metalized surfaces (e.g., Al coating, ~0.5-1 um).
- Self-passivating protective layers.
- Prefer higher operating altitudes (>800 km) where AO flux drops substantially.

### 3.6 Endpoint Counterweights and Capture Mechanisms

#### 3.6.1 Counterweight Design

Functions:
- Provide required centrifugal tension.
- Host capture, damping, and propulsion subsystems.
- Enable momentum-management mass configuration.

Recommended architecture: modular stacks (e.g., 10-t modules) for scalable mass tuning.

#### 3.6.2 Capture Interface

Capture hardware must tolerate impact and alignment errors over broad payload classes.

Design requirements:
- Payload range from small satellites to heavy cargo classes.
- Relative capture velocity capability up to mission-defined limits.
- Energy absorption sized to worst-case capture mismatch.

Stress-isolation interfaces are required between capture system and primary tether load path.

#### 3.6.3 Propulsion Integration

Endpoint propulsion supports spin-up and angular-momentum management.

- Chemical propulsion for high-thrust maneuvers.
- Electric propulsion for long-term station-keeping and fine control.

### 3.7 Volume Summary

1. Carbon fiber (T1000G class) is the most practical near-term choice; CNT is a long-term upgrade path.
2. Tapered sections are critical in high-acceleration cargo regimes; less critical in low-acceleration crewed regimes.
3. Radiation and AO protection are manageable via coatings, material engineering, and orbit selection.
4. Counterweight and capture modules must be designed as integrated dynamic subsystems, not passive masses.

Outputs feed Volume 4 (deployment and assembly), Volume 6 (economics), and Volume 7 (risk and verification).

### Parameter Outputs

| Parameter | Value | Status | Receiving Volume |
|:---|:---|:---|:---|
| Carbon-fiber allowable stress (SF=2.5) | 2.0 GPa | Design value | Volume 4 |
| CNT allowable stress (long-term target) | 8.0 GPa | Target | Volume 6 |
| Crewed LEO tether diameter (uniform estimate) | ~22 mm | Estimate | Volume 4 |
| Cargo 20g tether diameter (carbon-fiber estimate) | ~226 mm | Estimate | Volume 4 |
| Tapered area ratio (cargo case, end/core) | 0.687 | Design | Volume 4 |
| Al coating thickness | 0.5-1 um | Protection baseline | Volume 7 |
| Counterweight module mass | 10 t/module | Baseline | Volume 4 |
| Capture-system max absorbed energy | 25 MJ | Design | Volume 4 |

### References

[1] Du Shanyi, carbon-fiber aerospace applications, 2018.
[2] NASA, Carbon Nanotube Tether for Space Applications, 2018.
[3] Zhang Jin et al., space-environment effects on composites, 2015.
[4] De Vries, Kevlar vs Carbon Fiber in Space Tether Designs, 2020.
[5] Cosmo & Lorenzini, Tethers in Space Handbook, 1997.
[6] Banks et al., Atomic Oxygen Erosion of Spacecraft Materials, 2006.

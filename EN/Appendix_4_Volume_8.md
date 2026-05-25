# Appendix IV: Skyhook

## Volume 8: Interfaces with Main and Appendix Volumes

**Version**: 1.0
**Compilation Date**: June 2026
**Currency Unit**: Chinese Yuan (CNY), symbol: Y
**Related Main Volumes**: Main Volumes 2, 8, 9; Appendix I Volumes 3 and 6; Appendix III Volume 2

### 8.1 Opening Notes

This volume defines technical, data, and engineering interfaces between the skyhook system and the main ring-elevator program plus related appendices. As a precursor-validation and supplementary transport subsystem, skyhook design parameters, validation results, and operations data must integrate cleanly with program-wide architecture and lunar-industry/rail subsystems.

### 8.2 Interface with Main Volume 2 (Materials)

Main Volume 2 sets CNT performance targets for ring-elevator tethers. Skyhook material data (radiation exposure, atomic-oxygen performance, multi-strand residual strength) provide practical reference inputs.

| Output Source | Parameter | Value | Receiver | Use |
|:---|:---|:---|:---|:---|
| Appendix IV Vol. 3 | Carbon-fiber strength retention after LEO 10^7 rad | >=70% | Main Vol. 2 | CNT radiation-protection baseline |
| Appendix IV Vol. 3 | Al-coated AO erosion depth (annual) | <0.1 um | Main Vol. 2 | CNT coating reference |
| Appendix IV Vol. 7 | Multi-strand residual strength after micrometeoroid impact | >=50% | Main Vol. 2 | Redundancy design baseline |
| Main Vol. 2 | CNT target specific strength sigma/rho | 3.85x10^7 N*m/kg | Appendix IV Vol. 6 | Long-term upgrade economics |

Data sync recommendation: quarterly update from TetherSat material dataset to the main materials database.

### 8.3 Interface with Main Volume 8 (Transport)

Main Volume 8 defines ground->GEO ring-elevator transport. Appendix IV Volume 5 defines ring+skyhook relay architecture.

| Output Source | Parameter | Value | Receiver | Use |
|:---|:---|:---|:---|:---|
| Appendix IV Vol. 5 | GEO capture-point altitude | 42164 km | Main Vol. 8 | GEO terminal orbit design |
| Appendix IV Vol. 5 | GEO capture window cycle | 27.2 min | Main Vol. 8 | Handoff scheduling |
| Appendix IV Vol. 5 | Single-lift skyhook capacity (cargo) | 50/200/500 t | Main Vol. 8 | Capacity matching |
| Appendix IV Vol. 5 | GEO->Moon half-length (cargo case) | 84.5 km | Main Vol. 8 | Terminal docking-space reservation |

Recommended protocol: dedicated GEO station link (Ka-band class) for payload handoff confirmation and emergency command exchange.

### 8.4 Interface with Main Volume 9 (Energy)

Skyhook momentum-management and ring-mounted ejector operations introduce power and storage demands that must be co-designed with GEO energy infrastructure.

| Output Source | Parameter | Value | Receiver | Use |
|:---|:---|:---|:---|:---|
| Appendix IV Vol. 4 | Core-capsule peak power demand | 500 kW | Main Vol. 9 | GEO station power capacity |
| Appendix IV Vol. 4 | Magnetic torque system voltage/current | 300 V / 1000 A | Main Vol. 9 | Power-interface design |
| Appendix IV Vol. 5 | Ring ejector single-launch energy | ~5x10^9 J | Main Vol. 9 | Storage sizing |

### 8.5 Interface with Appendix I (Lunar Industry)

Skyhook lunar operations and asteroid-assist workflows interface with lunar industry transport and resource-development chains.

| Output Source | Parameter | Value | Receiver | Use |
|:---|:---|:---|:---|:---|
| Appendix IV Vol. 5 | Lunar cargo skyhook half-length | 100 km | Appendix I Vol. 6 | Rail-terminal siting |
| Appendix IV Vol. 5 | Lunar capture altitude | 100 km polar orbit | Appendix I Vol. 6 | Launch trajectory design |
| Appendix IV Vol. 5 | Skyhook speed shift after asteroid capture | 150 m/s | Appendix I Vol. 3 | Mining trajectory planning |

### 8.6 Interface with Appendix III (Lunar Rail)

Skyhook low-point geometry and rail terminal operations must be synchronized for efficient handoff.

| Output Source | Parameter | Value | Receiver | Use |
|:---|:---|:---|:---|:---|
| Appendix IV Vol. 5 | Lowest endpoint altitude | R_cm - l | Appendix III Vol. 2 | Terminal elevation design |
| Appendix IV Vol. 5 | Lunar skyhook period | ~5-30 min | Appendix III Vol. 2 | Departure interval constraints |
| Appendix III Vol. 2 | Rail terminal coordinates | TBD | Appendix IV Vol. 5 | Orbital inclination planning |

### 8.7 Master Parameter Output Table

| Parameter | Value/Range | Source Volume | Status | Receiver |
|:---|:---|:---:|:---:|:---|
| GEO altitude | 35786 km | Vol. 1 | Baseline | Main Vol. 8 |
| Static skyhook minimum tether length | 35586 km | Vol. 1 | Baseline | - |
| Crewed centripetal acceleration limit (LEO) | 1.87 m/s^2 | Vol. 2 | Constraint | Vol. 7 |
| Crewed centripetal acceleration limit (GEO) | 10.08 m/s^2 | Vol. 2 | Constraint | Vol. 7 |
| LEO->MEO half-length (cargo, 20g) | 32.8 km | Vol. 2 | Estimate | Vol. 4 |
| GEO->Moon half-length (cargo) | 84.5 km | Vol. 2 | Estimate | Vol. 5 |
| Skyhook system mass (50 t payload case) | 1000 t | Vol. 2 | Estimate | Vol. 6 |
| Carbon-fiber allowable stress | 2.0 GPa | Vol. 3 | Design value | Vol. 4 |
| CNT long-term allowable stress target | 8.0 GPa | Vol. 3 | Target | Vol. 6 |
| Crewed LEO tether diameter | 22 mm | Vol. 3 | Estimate | Vol. 7 |
| Deployment launch count (50 t case) | 15-20 | Vol. 4 | Estimate | Vol. 6 |
| Deployment cost (50 t case) | 56.2 billion CNY | Vol. 4 | Estimate | Main Vol. 10 |
| Spin-up duration | 3.15 days | Vol. 4 | Estimate | Vol. 5 |
| Ring->skyhook handoff window cycle | 27.2 min | Vol. 5 | Design | Main Vol. 8 |
| Ring ejector max speed (CNT) | 2.5-3 km/s | Vol. 5 | Estimate | Main Vol. 8 |
| Unit transfer cost to GEO segment | 13-26 CNY/kg | Vol. 6 | Estimate | Main Vol. 10 |
| Two-stage payback period | 1.5-8.5 years | Vol. 6 | Estimate | Main Vol. 10 |
| Annual tether break probability | 3x10^-3 | Vol. 7 | Estimate | Main Vol. 7 |
| Number of P0 verification items | 5 | Vol. 7 | Baseline | Main Vol. 7 |
| TetherSat cost | 0.3 billion CNY | Vol. 7 | Estimate | Main Vol. 10 |
| Lunar crewed skyhook half-length | 373 km | Vol. 5 | Estimate | Appendix I Vol. 6 |

### 8.8 Volume Summary

1. Material interface: skyhook environmental data supports ring-elevator material decision making; ring-elevator CNT targets guide skyhook long-term upgrades.
2. Transport interface: layered ring+skyhook transport requires strict orbit, timing, and handoff matching.
3. Energy interface: power/energy requirements for skyhook momentum systems must be integrated with GEO energy architecture.
4. Lunar-industry interface: skyhook, rail, and mining systems should be co-optimized for throughput and resilience.
5. Data-chain integrity: this interface map defines a complete parameter transfer chain across mechanics, materials, deployment, economics, and risk.

### References

[1] Main Volume 2: Materials Engineering, 2026.
[2] Main Volume 8: Transport System, 2026.
[3] Main Volume 9: Energy System, 2026.
[4] Appendix I Volume 3, 2026.
[5] Appendix I Volume 6, 2026.
[6] Appendix III Volume 2, 2026.
[7] CCSDS 701.1-B-2, 2019.

# Appendix IV: Skyhook

## Volume 6: Economics and Commercialization Path

**Version**: 1.0
**Compilation Date**: June 2026
**Currency Unit**: Chinese Yuan (CNY), symbol: Y
**Related Main Volumes**: Main Volume 10; Appendix IV Volumes 2, 3, 4, 5

### 6.1 Opening Notes

This volume evaluates skyhook feasibility and business potential from an economic perspective. It includes system mass and throughput estimates, capex decomposition (launch, materials, orbital assembly), opex (maintenance, propellant, staffing), cost comparison with rockets, payback analysis for two-stage skyhooks, and service models (cargo, crewed, deep-space launch).

### 6.2 System Mass and Throughput

Using M = 20m (system-to-payload mass ratio), beta=0.2 tether mass share, and endpoint counterweight m_p = 0.4M:

| Payload m (t) | System Mass M (t) | Tether Mass m_c (t) | Counterweight per End m_p (t) | Core+Propulsion (t) |
|:---:|:---:|:---:|:---:|:---:|
| 50 | 1000 | 200 | 400 | 100 |
| 200 | 4000 | 800 | 1600 | 400 |
| 500 | 10000 | 2000 | 4000 | 1000 |

Operational frequency is constrained by payload supply, synchronization windows, and post-capture momentum recovery time, so practical yearly mission counts are far below theoretical spin-limited maxima.

### 6.3 Construction Cost

#### 6.3.1 Launch Cost

Reference crewed LEO case requires multi-launch campaigns (order of 15-20 launches), combining medium and heavy-lift missions for tether segments, hub, and endpoint masses.

#### 6.3.2 Material Cost

Carbon-fiber material cost scales with tether mass and is typically a smaller component than launch costs in near-term deployment cases.

#### 6.3.3 On-Orbit Assembly and Test Cost

Includes robotic systems, docking interface production, and integrated simulation/test campaigns.

#### 6.3.4 Aggregated CAPEX (reference estimates)

| Payload Class | Launch Cost | Tether Material | Orbital Assembly | Total CAPEX |
|:---:|:---:|:---:|:---:|:---:|
| 50 t | dominant | low-share | moderate | ~56.2 billion CNY |
| 200 t | dominant | low-share | moderate | ~149.9 billion CNY |
| 500 t | dominant | low-share | moderate | ~367.3 billion CNY |

(Excludes full R&D program burden.)

### 6.4 Operating Cost

Components:
- Maintenance (inspection, repair, docking upkeep).
- Propellant (station-keeping + momentum recovery support).
- Staffing and operations control.
- Insurance and risk reserve.

Representative annual opex estimates:

| Payload Class | Annual OPEX |
|:---:|:---:|
| 50 t | ~0.89 billion CNY |
| 200 t | ~2.07 billion CNY |
| 500 t | ~4.72 billion CNY |

### 6.5 Cost Comparison with Rockets

For high-frequency reusable operations, skyhooks can deliver very low marginal transfer cost in specific mission segments, especially where repeated momentum exchange offsets upper-stage propellant burden. However, full mission economics must include the upstream transfer leg needed to reach skyhook capture orbit.

### 6.6 Payback Analysis (Two-Stage Skyhook)

Two-stage example:
- Stage 1: LEO skyhook for LEO->MEO boost.
- Stage 2: MEO skyhook for MEO->GEO/cislunar injection.

Revenue depends on mission cadence and pricing relative to equivalent rocket service. Under high-utilization assumptions, payback can be short; under lower cadence, payback extends but can remain viable.

### 6.7 Commercial Service Models

1. Cargo transfer services (LEO->GEO, GEO->cislunar).
2. Crewed transfer services (subject to strict acceleration constraints).
3. Deep-space launch support.
4. On-orbit verification and test-platform services.

### 6.8 Volume Summary

1. CAPEX is launch-dominated in near-term deployment scenarios.
2. OPEX remains moderate relative to capex but includes significant risk reserve.
3. Repeated-use mission profiles can provide strong unit-cost advantages.
4. Two-stage architecture improves service coverage and market flexibility.
5. Mixed service portfolio (cargo + crewed + deep-space + verification) improves revenue resilience.

### Parameter Outputs

| Parameter | Value | Status | Receiving Volume |
|:---|:---|:---|:---|
| 50 t skyhook CAPEX | 56.2 billion CNY | Estimate | Main Volume 10 |
| Annual OPEX (50 t case) | 0.89 billion CNY | Estimate | Main Volume 10 |
| Per-kg transfer cost to GEO segment | 13-26 CNY/kg (scenario dependent) | Estimate | Main Volume 10 |
| Two-stage payback period | 1.5-8.5 years (utilization dependent) | Estimate | Main Volume 10 |
| Crewed tourism ticket target | 5 million CNY/person | Target | - |
| Conservative annual cargo mission count | 500-1000 | Estimate | Volume 4 |

### References

[1] SpaceX Starship user documentation, 2024.
[2] Chinese launch vehicle price references, 2025.
[3] NASA cost-benefit study for tether systems, 2015.
[4] Appendix IV Volume 2, 2026.
[5] Appendix IV Volume 4, 2026.
[6] Main Volume 10, 2026.

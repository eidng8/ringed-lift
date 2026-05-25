# Appendix IV: Skyhook

## Volume 7: Risk and Verification Planning

**Version**: 1.0
**Compilation Date**: June 2026
**Currency Unit**: Chinese Yuan (CNY), symbol: Y
**Related Main Volumes**: Main Volume 7; Appendix IV Volumes 2, 3, 4

### 7.1 Opening Notes

This volume identifies and structures lifecycle risk for skyhook systems (construction, deployment, operation, retirement), and defines a verification roadmap. It covers technical risk (tether failure, capture failure, orbital instability), environmental risk (debris, micrometeoroids, radiation), crew-safety risk (high-g exposure and radiation-belt transit), P0/P1 validation item definitions, ground-test plans, and on-orbit demonstration missions.

All crewed concepts must satisfy total acceleration <=1.05g-equivalent constraints.

### 7.2 Technical Risks

#### 7.2.1 Tether Breakage

Risk: structural failure due to defects, fatigue, impact, or overload. Potential outcomes include high-energy mass release and secondary debris hazards.

Mitigation:
- Multi-strand braided redundancy.
- Continuous health monitoring (fiber-optic sensing).
- Conservative design safety factors (>=3).
- Redundant lock paths at interfaces.
- Fault-triggered containment/safe fragmentation strategy.

#### 7.2.2 Capture Failure

Risk: velocity/attitude mismatch or mechanism malfunction during rendezvous and lock-on.

Mitigation:
- Multiple capture attempts over successive rotation cycles.
- Passive guidance geometry at endpoint capture stations.
- Primary/backup capture hardware per endpoint.
- Safety standoff and abort envelopes.

#### 7.2.3 Orbital Instability

Risk: perturbation accumulation or control faults causing drift, window loss, or conjunction hazards.

Mitigation:
- Autonomous station-keeping with electric propulsion.
- Backup emergency propulsion mode.
- Ground-validated orbit determination and command authority.

### 7.3 Environmental Risks

#### 7.3.1 Debris and Micrometeoroids

Highest risk in LEO. Requires combined active avoidance plus passive hardening.

#### 7.3.2 Radiation

Moderate-to-high depending on orbit and mission type. Crewed cases require dedicated shielding and dose monitoring.

#### 7.3.3 Atomic Oxygen (LEO)

Requires coating and/or altitude strategy.

#### 7.3.4 Thermal Environment

Large thermal cycling requires low-expansion materials and active tension compensation.

### 7.3.5 Orbital-Use Conflict and International Coordination

Because skyhooks are long linear structures, they create non-trivial traffic-management, interference, and policy implications.

Key points:
1. Collision-risk quantification must be continuously maintained with live ephemeris updates.
2. Coordination with satellite operators is mandatory, including conjunction protocols.
3. Dedicated orbital corridor governance and end-of-life disposal standards are required.
4. Real-time transparency of skyhook geometry states is needed for safe multi-operator coexistence.

### 7.4 Crew-Safety Risks

#### 7.4.1 High-g Exposure

Control-system faults can force acceleration above crew limits.

Mitigation:
- Hard overspeed limits and autonomous braking.
- Human-rated seating and orientation design.
- Redundant acceleration sensing and fault switching.

#### 7.4.2 Radiation-Belt Transit

Mitigation:
- Orbit and mission timing optimization.
- Local storm-shelter shielding inside crew modules.
- Solar event forecast-based operational gating.

#### 7.4.3 Emergency Return

Mitigation:
- Docked standby return vehicle.
- Periodic refresh/rotation of return craft.
- Independent emergency life-support margin.

### 7.5 P0/P1 Validation Checklist

| ID | Item | Level | Validation Phase | Pass Criterion | Linked Volume |
|:---:|:---|:---:|:---|:---|:---:|
| V0-T1 | Long-term tether fatigue resistance | P0 | Ground + orbit | >=80% retained strength after 10^7 load cycles | Vol. 3 |
| V0-T2 | Repeated on-orbit docking reliability | P0 | Demo satellite | 100 successful cycles in test campaign | Vol. 4 |
| V0-T3 | Capture impact-energy absorption | P0 | Ground + orbit | 25 MJ-class event with no permanent loss of structural function | Vol. 4 |
| V0-E1 | Micrometeoroid resilience | P0 | Ground + orbit | >=50% residual load capacity after representative impact | Vol. 7 |
| V0-S1 | Crewed acceleration all-phase compliance | P0 | Crewed analog test | <=1.05g-equivalent envelope across all phases | Vol. 2 |
| V0-S2 | Radiation-shielding effectiveness | P0 | Orbit demo | crew cabin dose within target limits | Vol. 7 |
| P1-T1 | On-orbit tether weaving robot | P1 | Demo mission | 1 km successful weave, >=80% parent-strength joints | Vol. 4 |
| P1-E1 | Debris avoidance algorithm | P1 | Simulation + orbit | >=99.9% success against trackable conjunctions | Vol. 2 |
| P1-S1 | Emergency return-undock test | P1 | Orbit demo | autonomous undock/return within landing accuracy envelope | Vol. 7 |

### 7.6 Ground Experiment Plan

1. Fatigue cycling test for representative tether sections.
2. Hypervelocity impact test campaign.
3. Radiation aging and post-dose mechanical characterization.
4. Scaled rotating-system integrated dynamics demonstration.

### 7.7 On-Orbit Verification Missions

#### 7.7.1 TetherSat (small-scale demonstrator)

- Example: ~1 km half-length micro-skyhook class.
- Validates deployment, spin-up, small capture/release, structural sensing, and controlled deorbit.

#### 7.7.2 Skyhook-Demo (engineering demonstrator)

- Mid-scale operational demonstration.
- Validates segmented assembly, payload transfer to higher orbit, and sustained operations.

#### 7.7.3 Optional Crewed Validation

After successful uncrewed engineering demonstration, crewed analog validation can be executed with strict acceleration and abort criteria.

### 7.8 Volume Summary

1. Tether breakage and debris interaction are top technical/environmental risks.
2. Multi-layer mitigation (design redundancy + monitoring + avoidance + policy coordination) is required.
3. Crewed operations require hard acceleration and radiation safety envelopes.
4. A phased validation path (ground -> small orbit demo -> engineering demo -> optional crewed demo) is essential.
5. Risk-reduction budget should be treated as a core program investment rather than optional overhead.

### Parameter Outputs

| Parameter | Value | Status | Receiving Volume |
|:---|:---|:---|:---|
| Annual tether-break probability (reference estimate) | 3x10^-3 | Estimate | - |
| Capture failure rate with multi-attempt protocol | 10^-6 class target | Target | Volume 4 |
| Number of P0 verification items | 5 | Baseline | Main Volume 7 |
| Ground test package cost | 0.5 billion CNY | Estimate | Main Volume 10 |
| TetherSat cost | 0.3 billion CNY | Estimate | Main Volume 10 |
| Skyhook-Demo cost | 5.0 billion CNY | Estimate | Main Volume 10 |
| Optional crewed validation add-on | 1.0 billion CNY | Estimate | Main Volume 10 |

### References

[1] NASA Human Integration Design Handbook, 2010.
[2] Main Volume 7: Verification and Risk Control, 2026.
[3] Appendix IV Volume 2, 2026.
[4] Appendix IV Volume 3, 2026.
[5] Appendix IV Volume 4, 2026.
[6] ESA Space Debris Mitigation Guidelines, 2014.

# Orbital Ringed-Elevator Project Overview
(太空环梯工程概览)

**Statement**: This proposal does not discuss political or military factors, and only explores the project from technical and economic perspectives. All site selection, construction sequence, cost estimation, etc. are based on engineering feasibility, resource utilization efficiency, and economic benefits, without involving any geopolitical, national security, or military application considerations.

**Version**: 3.0<br/>
**Revision Date**: May 2026<br/>
**Currency Unit**: Renminbi (Yuan), symbol: ¥<br/>
**Exchange Rate Reference**: 1 USD ≈ 7.2 Yuan [0.1]

---

## I. Project Vision

Construct a permanent closed-loop framework at the outer edge of geosynchronous orbit (equatorial plane), and set up 6 space elevators along the equator to achieve:

- Integrated, all-weather ground–GEO–global circumferential transport
- Support for large-scale Earth–Moon logistics, deep space launches, global communications, and energy transmission
- Ultimately form humanity's first "space highway" and "orbital industrial base platform"

**Carrying Capacity and Industrial Scale**: The ring-elevator itself has a mass of about 170 million tons. While maintaining structural static equilibrium and safety margin, it can additionally support up to 1 billion tons of auxiliary facilities. This level of capacity will support:

- A single space solar power station with 500 GW output
- Permanent orbital residential and tourism stations for 30,000–50,000 people
- Megaton-class on-orbit manufacturing platforms, fuel depots, deep space launch ports
- Space mining and processing centers capable of handling thousands of tons of asteroid ore per day
- Kilometer-scale particle accelerators, mid-frequency gravitational wave observatories, and other large-scale scientific facilities

**Drive Scheme and Transport Efficiency**: After exhaustive derivation of multiple schemes in Volume V, **Scheme C—rack-and-pinion drive (aluminum alloy 7075-T6 micro-arc oxidized gear–rack engagement)** is determined as feasible. Low-altitude cruise speed is 200 km/h, mid-high altitude is 1,500 km/h (limited by rack speed), with a one-way trip time of about **50 hours**. The fully loaded cabin has a total mass of 200 t, including a drive module of about 49.3 t, payload module of about 69.4 t, and **effective payload of about 81.3 t per trip**.

**Energy Supply**: Pure onboard battery solution (specific energy demand ~31,900 Wh/kg) is physically infeasible. A **segmented hybrid power supply** scheme is adopted: 0–100 km powered by conductive rails (50 kV AC, four-way parallel, efficiency ~88%), 100–5,000 km by ground-based laser power transmission (350 MW), 5,000 km–GEO ring by solar-pumped laser transmission (with about 2.12 km² photovoltaic array).

**Force Relations After Closure**: As strictly derived in Volume VI, the circumferential tension in the fully loaded cable state is about 2.83×10⁹ N, only 1/7.4 of the GEO-end tension of a single elevator cable. **The ring cannot share the counterweight requirement of the elevator cable; the counterweight mass remains unchanged before and after ring closure** (about 8.0×10¹² kg per elevator, achieved by capturing a C-type asteroid).

---

## II. Core Engineering Parameters

| Parameter | Value | Source |
|:-----|:-----|:-----|
| Ring Radius | 42,264 km (GEO outer edge, ΔR = 100 km) | Volume I, Section 1.2.1 |
| Ring Circumference | ≈ 265,458 km | Volume I, Section 1.2.1 |
| Main Ring Material | Multi-walled carbon nanotube (MWCNT) braided cable | Volume II, Section 2.2.3 |
| Cable Engineering Strength Target | ≥ 20 GPa | Volume II, Section 2.3.4 |
| Full Cable Design Linear Density | 300 kg/m | Volume II, Section 2.6.2 / Volume VI, Section 6.3.2 |
| Ring Cross-section Diameter | 0.7 m (multi-strand redundant braid, N≥1000 strands) | Volume II, Section 2.6.2 / Volume VI, Section 6.3.2 |
| Total Mass of Ring Cable | ≈ 7.96×10⁷ t | Volume VI, Section 6.4.2 |
| Number of Elevators | 6 (evenly distributed along the equator) | Volume III, Section 3.2.2 |
| Elevator Cable Cross-section Ratio (GEO/ground) | 13.31:1 | Volume IV, Section 4.3.2 |
| Elevator Cable GEO-end Diameter | ≈ 1.824 m | Volume IV, Section 4.3.3 |
| Elevator Cable Ground-end Diameter | 0.5 m | Volume IV, Section 4.3.3 |
| Single Elevator Counterweight Mass | 8.0×10¹² kg (achieved by capturing C-type asteroid) | Volume IV, Section 4.5.3 / Volume VI, Section 6.2.3 |
| Cabin Cruise Speed | Low altitude 200 km/h, mid-high altitude 1,500 km/h (rack speed limit) | Volume V, Section 5.8.3 / Volume V, Section 5.5.3 |
| One-way Trip Time | ≈ 50 h | Volume V, Section 5.8.3 |
| Fully Loaded Cabin Mass | 200 t (effective payload ≈81.3 t/trip) | Volume V, Section 5.10.4 / Volume VIII, Section 8.2.1 |
| Total Construction Period | ≈ 28 years (to full cable operation) | Volume VIII, Section 8.4.1 |
| Design Service Life | 500–1000 years (via active maintenance and progressive upgrades) | Overview / Volume XII, Section 12.3 |

---

## III. The 6 Elevator Nodes and Construction Sequence

| Order | Node Name | Longitude | Type | Latitude Deviation | Anchorage Method | Estimated Main Construction Period |
|:-----|:-----|:-----|:-----|:-----|:-----|:-----|
| 1 | Macapá/Fara Bay, Brazil | 51°W | Land-based (continent) | ≈0° | Pure uplift type | 8 years |
| 2 | Port-Gentil, Gabon | 8°47'E | Land-based (continent) | ≈0°43'S | Uplift + shear composite type | 6 years |
| 3 | Manta, Ecuador | 80°43'W | Land-based (continent) | ≈0°57'S | Uplift + shear composite type | 7 years |
| 4 | Kiritimati (Christmas Island), Kiribati | 157°W | Island (coral reef) | ≈2°N | Suction anchor, inclined mooring type | 8 years |
| 5 | Belitung, Indonesia | 108°E | Land-based (island) | ≈0° | Pure uplift type | 6 years |
| 6 | Indian Ocean Deep Sea Floating Platform | 73°E | Deep sea floating platform | ≈0° | Floating platform + tension leg type | 9 years |

**Construction Sequence Logic**: Elevators first, then the ring. The first elevator (Brazil) has the longest construction period (about 10 years including trial operation), subsequent elevators proceed in parallel. Ring construction starts in year 13, geometric closure in year 22, and full cable operation in year 28. (See Volume VIII, Section 8.3)

---

## IV. Key Technology Pathways

| Level | Technology | Maturity | Deployment Stage |
|:-----|:-----|:-----|:-----|
| **Transport** | Reusable heavy-lift rockets (Starship/Long March 9) | Commercialized | Stage 1–2 |
| | Offshore launch platform | Commercially mature | Stage 1–2 |
| | Space tug (nuclear thermal/electric propulsion) | Under development | Stage 2–3 |
| | Electromagnetic launch assist | Experimental validation | Stage 3–4 |
| **Materials** | Ground-based CNT manufacturing (FCCVD method) | Lab → small batch | Stage 1–2 |
| | In-situ lunar regolith CNT manufacturing | Lab validation | Stage 2–3 (acceleration option) |
| | C-type asteroid carbon source capture | 1-meter capture bag ISS validation | Stage 1–3 |
| **Drive** | Rack-and-pinion drive (aluminum alloy micro-arc oxidized gear–rack) | Provisionally feasible (requires experimental validation) | Stage 3–4 |
| | Segmented hybrid power supply (conductive rail + laser power transmission) | Scheme closed (requires experimental validation) | Stage 3–4 |
| **Construction** | Space spider robot (eight-legged embracing, nuclear powered) | Needs development | Stage 3–4 |
| | Multi-strand redundant braiding and on-orbit splicing | Needs development | Stage 3–4 |
| **Energy** | Space solar power station (500 GW, 960 km²) | Long-term engineering | Stage 4 |
| | Microwave wireless power transmission (5.8 GHz, end-to-end efficiency 48%) | Concept mature | Stage 4 |
| **Survival** | Ring firewall segment isolation + Whipple debris protection | Scheme design completed | Integrated in all stages |

**Schemes Proven Infeasible** (detailed derivation in Volume V):
- Rocket drive (Δv ~19 km/s, mass multiplication ratio >74×) [Volume V, Section 5.4]
- Direct friction wheel clamping (contact stress ~600 MPa > CNT transverse strength) [Volume IV, Section 4.4]
- UHMWPE friction drive (contact stress ~96 MPa > yield strength 20–25 MPa) [Volume IV, Section 4.12]
- Pure onboard battery (specific energy required 31,900 Wh/kg, far exceeds electrochemical storage limits) [Volume V, Section 5.11.1]
- Constant cross-section index cable (self-weight stress exceeds allowable by 2.6×) [Volume V, Section 5.13]

---

## V. Implementation Phases and Costs

### Total Investment

Based on the first unified modeling of all capital expenditures (CAPEX) in Volume X, the total investment for the Orbital Ringed-Elevator Project from technical validation to full cable operation (about 28 years) is about **¥55–58 trillion**.

| Phase | Time | Core Tasks | Investment Share |
|:-----|:-----|:-----|:-----|
| Phase 1 | Years 1–10 | Technical validation, first elevator (Brazil) construction and trial operation | ~9% |
| Phase 2 | Years 5–16 | Construction of 5 elevators, counterweight capture, launch facilities | ~40% |
| Phase 3 | Years 13–24 | Ring construction and closure, large-scale rocket launches | ~40% |
| Phase 4 | From Year 25 | Full cable operation, orbital sleeve/rack installation, commercial operation launch | ~10% |

### Main Cost Magnitude Estimates

| Cost Category | Magnitude (trillion yuan) |
|:---------|:-----|
| Heavy-lift rocket launches (about 15,000–18,000 times, ring cable segments + elevator cable materials) | ~15–20 |
| Elevator cable system (6 units, including CNT braided cable + orbital sleeve + anchorage construction + cable deployment) | ~10–15 |
| Counterweight system (12–18 asteroid captures including towing) | ~10–12 |
| Main ring cable (about 530,000 segments, including C/SiC flange connectors) | ~8–12 |
| Orbital sleeve, rack, and ring facilities (including phase I solar power station) | ~5–8 |
| Space spiders and cabins (200 spiders + ≥40 DM/PM) | ~3–5 |
| Space tugs and on-orbit facilities (50 tugs + LEO/GEO hub stations) | ~3–5 |
| Ground facility construction (expansion of 4 equatorial launch sites) | ~1–2 |
| Technical validation, contingency, and management (including all 8 P0-level experiments) | ~2–3 |

---

## VI. Major Risks and Countermeasures

| Risk | Level | Countermeasure | Related Volume |
|:-----|:-----|:-----|:-----|
| Heavy-lift rocket launch frequency bottleneck (peak 1,000–1,500/year) | High | Promote lunar manufacturing (acceleration option); large-scale rocket mass production and reuse | Volume VIII |
| Rack wear life below expectation | **P0** | 10⁷-cycle experimental validation in Volume VII; reserve for rack replacement or switch to steel rack scheme | Volume V/VII |
| CNT filament-to-yarn strength transfer efficiency f₁ insufficient | **P0** | Target f₁≥0.5; if f₁<0.3, re-evaluate entire scheme | Volume II/VII |
| High-altitude segment high-power heat dissipation (~20.8 MW) infeasible | **P0** | If validation fails, lock to 200 km/h low-speed scheme (one-way 50 h) | Volume V/VII |
| Space debris cascade collision (Kessler syndrome) causing ring disintegration | Extremely high | Ring firewall segment isolation + Whipple shield + self-healing cable | Volume VII/XII |
| Lunar factory delay | Strategic | Earth launch as baseline; lunar manufacturing as acceleration option only | Volume II/VIII |
| First elevator/Christmas Island/Indian Ocean platform construction delay | High | Parallel advancement, independent teams, early start of counterweight capture | Volume VIII |
| Single elevator cable breakage | Medium | Does not affect ring closure integrity; post-disaster rapid reconstruction per Volume XII lifeline engineering | Volume I/XII |
| Economic feasibility (including discounted payback period ~45 years) | Medium | Multiple revenue streams (transport + power + communications + tourism); phased commercial operation | Volume X |

---

## VII. Milestone Timeline

| Milestone | Time | Marker |
|:-----|:-----|:-----|
| First elevator (Brazil) achieves commercial operation | Year 10 | 2-year trial run completed, annual effective capacity about 5,700 t |
| All 6 elevators in place | Year 15 | Total annual effective capacity about 34,200 t |
| Ring geometric closure | Year 22 | Last arc segment of the ring closed |
| Ring completed and full cable operation | Year 28 | λ=300 kg/m, N≥1000 strands, all revenue streams activated |

---

## VIII. Application Prospects

- **Earth–Moon and Deep Space Transport Hub**: Orbit insertion cost reduced to 1%–5% of rockets; deep space launch port on the ring
- **Space Solar Power Station**: 500 GW installed, 58 GW ground power output
- **Global Communications and Data Relay**: DWDM fiber ring capacity about 3.8 Pbps, seamless Earth coverage, navigation enhanced to centimeter level
- **Scientific Research Platform**: Long baseline interferometer, mid/low-frequency gravitational wave observatory
- **Space Industry and Tourism**: On-orbit manufacturing, fuel plants, orbital hotels
- **Emergency and Safety**: Asteroid deflection, debris removal, disaster response

---

## IX. Summary

The Orbital Ringed-Elevator Project is a comprehensive engineering blueprint based on cross-disciplinary evidence from physics and materials engineering. Its scheme evolution follows a rigorous spiral path of "discovering physical bottlenecks → adding engineering interfaces → re-examining new bottlenecks," ultimately converging on the rack-and-pinion drive (Scheme C) and segmented hybrid power supply technology combination.

Through systematic demonstration in twelve volumes:

- **Physically**: The static equilibrium equation for the synchronous rotating ring holds; the mechanical relationship that counterweight mass cannot be reduced after ring closure has been strictly proven.
- **Engineering**: The rack-and-pinion scheme passes magnitude checks for contact stress (margin 1.72) and bending stress (margin 5%). All 11 P0-level key uncertainties (including 8 experiments, 1 simulation, 2 comprehensive verifications) have clear validation paths in Volume VII.
- **Construction**: The total global construction period is about 28 years. The total transport system cost is about ¥25–29 trillion, and total project CAPEX is about ¥55–58 trillion.
- **Economically**: In the baseline scenario, the discounted payback period is about 45 years. The project may be profitable, but economic feasibility is highly dependent on revenue from space solar power and communication services.
- **Survival**: "Firewall" segment isolation, "shield and blood" debris protection, and post-disaster "lifeline" rapid reconstruction constitute a three-layer survival guarantee system.
- **Governance**: A multilateral governance framework centered on the United Nations Orbital Ringed-Elevator Organization (UNORE) has been proposed, covering the full chain of investment, settlement, security, liability, and dispute resolution.

---

## References

[0.1] People's Bank of China, RMB central parity rate, May 2026.
[0.2] Detailed technical parameters and derivations for each volume, see Volumes I through XII of this project.

# Volume 9: Energy and Communication Infrastructure

**Version**: 2.1 (Final Review)
**Compilation Date**: May 2026
**Currency Unit**: Renminbi (Yuan), symbol: ¥


## 9.1 Preface

This volume is positioned as the **energy supply and information transmission infrastructure planning** for the Space Ringed-Elevation project, focusing on answering the following core questions:

> After the ring elevator is completed, where does the electricity come from for the operation of 6 elevators, thousands of devices on the ring, and hundreds of people living and working online simultaneously? How is the global communication backbone network of the ring elevator structured? How can solar energy from GEO orbit be transmitted back to the ground to form commercial power output?

This volume continues from:
- **Overview**: Space solar power stations (500 GW to TW scale), fiber/laser backbone network, navigation enhancement system
- **Volume 5**: Power supply schemes for the elevator cars (conductive rails, laser power transmission, onboard buffer batteries)
- **Volume 6**: Deployment of facilities on the ring after the main structure is completed
- **Volume 8**: Timeline for full cable operation of the ring (commercial operation from year 28)

Core tasks of this volume:

1. Design the deployment plan, total installed capacity, integration method with the ring main structure, and wireless power transmission links for the space solar power station on the ring, providing a complete link power balance derivation.
2. Plan the energy distribution network on the ring (superconducting/high-voltage DC transmission, energy storage schemes), and provide quantitative derivation of transmission losses and storage capacity.
3. Design the topology, redundant routing, and node switching capabilities of the fiber/laser communication backbone network on the ring.
4. Plan ground communication coverage and navigation enhancement services.
5. Provide cost magnitude estimates for the energy and communication systems for use in Volume 10 (Economic Model).


## 9.2 Space Solar Power Station on the Ring

### 9.2.1 Physical Advantages of Deployment

Geostationary orbit (GEO) is the prime location for deploying space solar power stations. Compared to ground-based photovoltaics, GEO solar power stations have the following physical advantages:

- **No day-night alternation**: Only around the vernal and autumnal equinoxes, for about 42 days each, does the shadow period occur, with each shadow lasting up to 72 minutes. The annual average sunlight time ratio ≈ 1 − (84 × 1.2)/365 ≈ 99.72%.
- **No atmospheric attenuation**: AM0 solar irradiance S₀ = 1,361 W/m², without atmospheric absorption and scattering.
- **No weather impact**: Not affected by clouds, rain, sandstorms, or other meteorological conditions.
- **Fixed geometry**: The ring is located at the outer edge of GEO, stationary relative to the ground, requiring no solar tracking mechanism (the cell array is fixed on the ring, automatically maintaining sun orientation with Earth's revolution).

The closed-loop cable structure of the Space Ringed-Elevation provides a unique platform advantage—the ring itself is a natural truss with a circumference of about 265,000 km, allowing the solar cell array to be directly mounted or suspended on the ring cable, eliminating the need for independent launch and assembly of giant truss structures.

### 9.2.2 Load-Bearing Capacity of the Ring Cable for Additional Loads

Before installing the solar cell array, it is necessary to verify whether the tension margin of the ring cable is sufficient to bear its additional weight.

The design linear density of the ring in full cable state λ = 300 kg/m (Volume 4, Section 4.3), ring tension $T_{ring}$ ≈ 2.83×10⁹ N (Volume 6, Section 6.3.2).

The solar cell array is in the form of a flexible thin film, with a target areal density ≤ 1.0 kg/m². Distributed evenly along the ring circumference, the deployment width is about w. Let w = 10 m (including maintenance passage and safety spacing), then the additional linear density per unit ring length:

$$
\Delta \lambda = \rho_A \times w = 1.0 \, \text{kg/m}^2 \times 10 \, \text{m} = 10 \, \text{kg/m}
$$

The additional linear density is only about 3.3% of the ring cable's own linear density. According to the ring's static equilibrium equation T = GMₑ λ / R₀, the ring tension is proportional to the linear density, so the increase in ring tension after installing the cell array is about:

$$
\Delta T_{\text{ring}} = \frac{GM_e \Delta \lambda}{R_0} \approx \frac{3.986 \times 10^{14} \times 10}{4.2264 \times 10^7} \approx 9.43 \times 10^7 \, \text{N}
$$

The allowable tension of the ring cable cross-section can be deduced from the design parameters:
- Cable cross-section diameter d = 0.7 m, cross-sectional area A ≈ 0.385 m² (Volume 4, Section 4.3, including effective load-bearing area after filling factor)
- CNT engineering allowable stress $σ_{allow}$ = 20 GPa / 2.5 = 8 GPa
- Ultimate load-bearing tension of the ring cable $T_{ultimate}$ ≈ 8 × 10⁹ × 0.385 ≈ 3.08 × 10⁹ N

The additional tension 9.43 × 10⁷ N is only about 3.1% of the ultimate load-bearing tension, well within the safety margin. **The ring cable can fully bear a large-area solar cell array.**

### 9.2.3 Derivation of Total Installed Capacity and Area

With **500 GW** as the initial installed target (reference: about 250 times the output of the Three Gorges Dam). The required photovoltaic array area is derived as follows.

| Parameter | Symbol | Value | Source |
|-----------|:-----:|-------|--------|
| AM0 solar irradiance | S₀ | 1,361 W/m² | Standard value |
| PV cell efficiency | $η_{PV}$ | 45% | Future multi-junction GaAs, value cited from Volume 5 |
| Array fill factor | FF | 0.85 | Includes support structure and wiring gaps |
| Power per unit area | $P_A$ | S₀ × $η_{PV}$ × FF | — |

$$
P_A = 1,361 \times 0.45 \times 0.85 \approx 520.6 \, \text{W/m}^2
$$

Total area required for 500 GW:

$$
A_{500\text{GW}} = \frac{500 \times 10^9}{520.6} \approx 9.60 \times 10^8 \, \text{m}^2 = 960 \, \text{km}^2
$$

Distributed along the ring circumference L = 265,458 km = 2.65458 × 10⁸ m, the average deployment width:

$$
w_{\text{avg}} = \frac{9.60 \times 10^8}{2.65458 \times 10^8} \approx 3.62 \, \text{m}
$$

Even considering safety spacing, maintenance passages, and wiring space, increasing the actual width to 10 m, the total area is about 2,650 km², which is fully accommodated on the scale of the ring.

### 9.2.4 Power Interruption and Storage Demand During Shadow Periods

**(1) Shadow Geometry and Affected Range**

The Earth's shadow (umbra) at GEO orbit does not cover the entire orbit. The maximum cross-sectional diameter of the shadow cone at GEO altitude (about 42,164 km) is:

$$
D_{\text{shadow}} \approx 2 \times \left( R_e - \frac{R_e}{R_{\text{sun}} - R_e} \times (R_{\text{GEO}} - R_e) \right)
$$

Substituting $R_e$ = 6,371 km, $R_{sun}$ ≈ 696,340 km, $R_{GEO}$ ≈ 42,164 km:

When the sun is regarded as a point source, the half-angle of the shadow cone is about 0.0046 rad. At 42,164 km, the shadow cone radius is about:

$$
r_{\text{shadow}} \approx R_e - (R_{\text{GEO}} - R_e) \times \tan(0.0046) \approx 6,371 - 35,793 \times 0.0046 \approx 6,371 - 165 \approx 6,206 \, \text{km}
$$

This value is about 97% of the Earth's radius, and the cross-sectional diameter of the shadow at GEO is about 12,400 km. However, the GEO orbit is circular, and the ring is only at the outer edge of this orbit. The projection of the shadow cone on the ring plane is a circular area with a diameter of about 300 km (most severe at the vernal equinox, less at the autumnal equinox).

The ring circumference is about 265,458 km, and the shadow region arc length $l_{shadow}$ ≈ 300 km (maximum at the vernal equinox), accounting for only about **0.11%** of the ring circumference. This means—**during the shadow period, the vast majority of the photovoltaic area on the ring still receives sunlight, with only a very small arc segment entering the shadow cone temporarily losing illumination.**

**(2) Energy Gap During Shadow Period**

Conservatively taking the shadow region arc length as 1,000 km (including the penumbra), accounting for about 0.38% of the ring circumference. The photovoltaic area and corresponding power generation in this arc segment:

$$
P_{\text{shadow}} = 500 \, \text{GW} \times 0.0038 \approx 1.88 \, \text{GW}
$$

Shadow duration is up to 72 min = 1.2 h, so the energy gap during this period:

$$
E_{\text{gap}} = 1.88 \times 10^9 \times 4,320 \approx 8.12 \times 10^{12} \, \text{J} \approx 2.25 \, \text{GWh}
$$

### 9.2.5 Energy Storage Scheme

| Storage Type | Capacity | Purpose |
|--------------|----------|---------|
| **Superconducting Magnetic Energy Storage (SMES)** | 0.5 GWh | Instantaneous power balancing, second-level response |
| **Hydrogen Storage (Electrolysis + Fuel Cell)** | 2.5 GWh | Continuous power supply for equipment in the affected arc segment during shadow periods |

The round-trip efficiency of the hydrogen storage system is about 41%, requiring storage of about 6.1 GWh of hydrogen chemical energy, which is about 183 tons of hydrogen (33.3 kWh/kg). Lithium batteries can also be an alternative (500 Wh/kg, 2.5 GWh requires about 5,000 tons).

### 9.2.6 Mass Estimate of the Solar Cell Array

| Parameter | Value |
|-----------|-------|
| Areal density (including support foil and wiring) | ≤1.0 kg/m² |
| Total area (960 km², 500 GW) | 9.6 × 10⁸ m² |
| **Total mass** | ≈9.6 × 10⁸ kg = **960,000 tons** |
| Deployment method | Reel launch → space spiders deploy along the ring |
| Maintenance method | Space spiders regularly inspect and replace failed panels |


## 9.3 Wireless Power Transmission Link

### 9.3.1 Microwave Power Transmission—Ground Power Output

Most of the solar power on the ring is transmitted to ground receiving stations via **microwave wireless power transmission**.

**(1) Frequency Selection**

The 5.8 GHz ISM band is selected for the following reasons:
- Low atmospheric attenuation (about 0.3 dB at zenith, 2–3 dB at low elevation angles)
- Wavelength about 5.2 cm, moderate antenna size
- The International Telecommunication Union (ITU) has allocated this band for industrial, scientific, and medical applications

**(2) Link Equation**

The end-to-end efficiency of microwave wireless power transmission consists of the following segments:

$$
\eta_{\text{total}} = \eta_{\text{DC-RF}} \times \eta_{\text{tx}} \times \eta_{\text{atm}} \times \eta_{\text{rx}} \times \eta_{\text{RF-DC}}
$$

| Segment | Symbol | Efficiency | Description |
|---------|:-----:|:----------:|-------------|
| DC to microwave conversion | $η_{DC}$-RF | 70% | Solid-state power amplifier (GaN HEMT) |
| Transmitting antenna gain and beam efficiency | $η_{tx}$ | 95% | Phased array beamforming |
| Atmospheric attenuation | $η_{atm}$ | 95% | 5.8 GHz, zenith direction |
| Receiving antenna aperture efficiency | $η_{rx}$ | 90% | Rectenna array |
| Microwave to DC conversion | $η_{RF}$-DC | 85% | Schottky diode rectification |
| **End-to-end efficiency** | $η_{total}$ | **≈48%** | — |

**(3) Transmitting and Receiving Antenna Size**

The transmitting antenna is a phased array antenna deployed above the 6 nodes on the ring. Taking a single node transmitting 20 GW of electric power as an example.

Transmitting end DC power $P_{DC_{tx}}$ = 20 GW, after $η_{DC}$-RF = 70% conversion, microwave power ${P_{RF}}$ = 14 GW.

Transmitting antenna area $A_{tx}$ is determined by the power density limit: to avoid ionospheric breakdown and ensure safety, power density $P_{density}$ ≤ 250 W/m² (safety standard).

$$
A_{\text{tx}} = \frac{P_{\text{RF}}}{P_{\text{density}}} = \frac{14 \times 10^9}{250} = 5.6 \times 10^7 \, \text{m}^2
$$

Corresponding circular antenna diameter:

$$
d_{\text{tx}} = \sqrt{\frac{4 A_{\text{tx}}}{\pi}} = \sqrt{\frac{4 \times 5.6 \times 10^7}{\pi}} \approx 8,440 \, \text{m} \approx 8.4 \, \text{km}
$$

The receiving antenna (ground rectenna) area is deduced from the link efficiency. After atmospheric attenuation, the microwave power reaching the ground is $P_{RF}$ × $η_{tx}$ × $η_{atm}$ = 14 × 0.95 × 0.95 ≈ 12.6 GW. The power density at the receiving antenna is about 60%–80% of that at the transmitting antenna (depending on beam spread), taking an effective receiving power density of about 150 W/m²:

$$
A_{\text{rx}} = \frac{12.6 \times 10^9}{150} \approx 8.4 \times 10^7 \, \text{m}^2
$$

Corresponding diameter is about 10.3 km. The ground rectenna can be built on offshore platforms or desert areas near the anchor nodes, with an area of about 80 km² per node.

**(4) Total Power Transmission Capacity**

| Parameter | Value |
|-----------|-------|
| Single node transmitting power (DC) | 20 GW |
| Single node power delivered to ground (DC) | ≈20 × 0.48 ≈ 9.6 GW |
| Total power delivered to ground by 6 nodes | ≈58 GW |
| Ground power grid price | ¥0.3–0.6/kWh |

### 9.3.2 Laser Power Transmission—Car Power Supply

A complete derivation of car laser power transmission is given in Volume 5, Section 5.11.2. This volume only supplements the deployment location of lasers on the ring: distributed above the 6 nodes, each node equipped with about 400 MW electric power pump lasers (corresponding to the hollow section's 297.5 MW car power demand, after link efficiency about 750 MW laser emission power is required, with 35% electro-optical efficiency, pump power about 2,200 MW, shared by 6 nodes).


## 9.4 Energy Distribution Network on the Ring

### 9.4.1 Power Transmission Topology and Voltage Level

The closed-loop structure of the ring is naturally suitable for a **dual-redundant ring bus** topology. Two independent high-voltage DC (HVDC) buses are laid along the ring cable, serving as backups for each other. In case of local failure of any bus, power can be rerouted through the other side.

| Parameter | Recommended Scheme | Description |
|-----------|-------------------|-------------|
| Transmission type | **High-voltage DC (HVDC)** ±100 kV | — |
| Bus material | Aluminum alloy conductor (integrated with the middle layer of the track sheath) | Utilizing the existing conductive rail structure |
| Conductor cross-sectional area | ≈5,000 mm² (shared with track sheath conductive rail) | Volume 4, Section 4.11 |
| Single bus resistance (full ring) | ≈875 Ω | Aluminum resistivity 5.2×10⁻⁸ Ω·m, length 265,458 km |
| Single bus current capacity | ≈10 kA | — |
| Single bus transmission capacity | ≈2 GW (±100 kV, 10 kA) | — |
| Dual bus total capacity | ≈4 GW | — |

**Transmission Loss Derivation**:

Single bus resistance $R_{line}$ = 875 Ω, current I = 10 kA, full ring transmission loss:

$$
P_{\text{loss}} = I^2 R_{\text{line}} = (10,000)^2 \times 875 = 8.75 \times 10^{10} \, \text{W} = 87.5 \, \text{GW}
$$

This value far exceeds the 2 GW transmission capacity—indicating extremely high losses for long-distance HVDC transmission. In actual operation, power is **used locally**, not transmitted long distances from one side of the ring to the other. The solar cell arrays at the 6 nodes each supply power to the local elevator and adjacent ring segments, with only a small amount of power scheduled across hemispheres via HVDC. Under normal circumstances, the transmission distance of a single ring segment does not exceed 1/6 of the ring circumference (about 44,000 km), with losses of about 14.6 GW (still high, further limited to only 1/12 of the circumference, about 22,000 km, losses about 7.3 GW).

If **superconducting DC transmission** is adopted in the future (high-temperature superconducting tape YBCO, critical temperature about 92 K), the full ring resistance can be reduced to nearly zero, and transmission losses are almost eliminated. The superconducting scheme requires an active cooling system (liquid nitrogen temperature zone 77 K), which is a direction for future upgrades.

### 9.4.2 On-Ring Power Demand

| Power Equipment | Single Unit Power | Quantity | Total Power |
|-----------------|:----------------:|:--------:|:-----------:|
| Elevator car DM (6 elevators, each with 1 up and 1 down car running simultaneously) | ~114.4 MW (low altitude) | 12 units | ≈1,370 MW |
| Space spiders (for maintenance) | 12 kW | 50 units | ≈0.6 MW |
| On-ring communication equipment (6 nodes) | ≈1 MW/node | 6 nodes | ≈6 MW |
| On-ring thrusters (≥360 units) | ≈100 W/unit | 360 units | ≈0.04 MW |
| Life support and lighting | ≈10 MW | — | ≈10 MW |
| **Total** | — | — | **≈1,400 MW** |

The total on-ring power demand is about 1.4 GW, directly supplied by the solar cell arrays at nearby nodes, not exceeding the HVDC transmission capacity limit.


## 9.5 On-Ring Communication Backbone Network

### 9.5.1 Topology

The ring has a circumference of about 265,000 km, and on-ring communication must meet:
- **Ultra-low latency**: Millisecond-level latency between any two points globally (light speed transmission along the ring, maximum antipodal point latency about 89 ms)
- **Extremely high bandwidth**: Supports on-ring scientific data, car video monitoring, and space tourism broadband access
- **Resilience**: Any segment break does not affect overall network communication

A **dual-redundant DWDM fiber ring** scheme is adopted: two independent fiber bundles (each containing 12–24 single-mode fibers) are laid along the ring cable, transmitting in both directions (clockwise and counterclockwise). In case of any segment break, signals automatically reroute via the reverse path.

**Topology Parameters**:

| Parameter | Value |
|-----------|-------|
| Fiber type | Single-mode (G.652 or G.657), radiation-hardened |
| Band | C+L band (1530–1625 nm) |
| Channel spacing | 50 GHz (DWDM standard) |
| Total available bandwidth in C+L band | ≈12 THz |
| Per channel modulation format | 64-QAM, symbol rate 64 Gbaud |
| Net rate per channel | ≈400 Gbps |
| Maximum number of channels (dual polarization) | ≈240 |
| Theoretical capacity per fiber | ≈96 Tbps |
| Actual per fiber capacity (including FEC overhead) | ≈80 Tbps |
| Dual bundle (24+24 fibers) total capacity | ≈3.8 Pbps |

### 9.5.2 Optical Amplifier Spacing and Signal-to-Noise Ratio

Fiber signals attenuate with distance during transmission and require periodic regeneration by optical amplifiers. Erbium-doped fiber amplifiers (EDFA) provide about 20–25 dB gain in the C band, with a noise figure of about 5 dB.

Single segment fiber loss (including splicing and connectors):

$$
\alpha = 0.2 \, \text{dB/km} \quad (\text{typical value for radiation-hardened single-mode fiber})
$$

The spacing of optical amplifiers must ensure that the received optical signal-to-noise ratio (OSNR) is above the forward error correction (FEC) threshold. For 64-QAM 64 Gbaud signals, the typical FEC threshold OSNR is about 15 dB.

Per span fiber loss = α × $L_{span}$. EDFA gain = fiber loss. The post-amplifier OSNR is given by:

$$
\text{OSNR} = P_{\text{out}} - \text{NF} - 10 \log_{10}(h \nu B)
$$

Where $P_{out}$ is the amplifier output power (take 20 dBm), NF is the amplifier noise figure (5 dB), hν is the photon energy (C band about 1.27×10⁻¹⁹ J), B is the reference bandwidth (take 0.1 nm ≈ 12.5 GHz).

$$
\text{OSNR} \approx 20 - 5 - 10 \log_{10}(1.27 \times 10^{-19} \times 12.5 \times 10^9) - 30
$$
$$
= 15 - 10 \log_{10}(1.59 \times 10^{-9}) \approx 15 + 88 \approx 103 \, \text{dB} \, (\text{per span})
$$

After N spans, OSNR cumulative degradation is $OSNR_N$ = $OSNR_1$ − 10 log₁₀(N). Let $OSNR_N$ ≥ 15 dB (FEC threshold), then:

$$
103 - 10 \log_{10}(N) \geq 15 \Rightarrow 10 \log_{10}(N) \leq 88 \Rightarrow N \leq 10^{8.8}
$$

Take optical amplifier spacing as **100 km**, requiring about 2,655 amplifiers for the full ring. At this spacing, after N=2,655 spans, OSNR degrades to 103 − 10 log₁₀(2,655) ≈ 103 − 34 = 69 dB, far above the FEC threshold. **100 km spacing is fully feasible.**


## 9.6 Ground Communication Coverage and Navigation Enhancement

### 9.6.1 Ground Coverage Geometry

The antenna platforms directly above the 6 nodes at GEO (radius 42,264 km) have a line-of-sight coverage range of:

$$
\theta = \arccos\left(\frac{R_e}{R_{\text{GEO}}}\right) = \arccos\left(\frac{6,371}{42,264}\right) \approx 81.3^\circ
$$

That is, each platform can cover the Earth's surface from 81.3°N to 81.3°S. The 6 nodes are spaced about 60° apart in longitude, with no coverage blind spots at the equator and mid-low latitudes.

For high latitudes (>60°), coverage is provided by polar region floating platforms (see Appendix 2) as relay nodes connecting to the ring backbone network.

### 9.6.2 Navigation Enhancement

The 6 node platforms on the ring are equipped with high-precision atomic clocks and navigation signal transmitters, serving as **space-based differential correction stations** for GNSS (GPS/BeiDou/Galileo/GLONASS). The fixed geometric position of the ring (stationary relative to the ground) makes it an ideal position reference—the three-dimensional coordinates of any point on the ring can be pre-calibrated to millimeter-level accuracy.

Correction signals are broadcast via L1 (1575.42 MHz) and L5 (1176.45 MHz) dual frequencies, enabling users in the coverage area to achieve centimeter-level real-time positioning accuracy.


## 9.7 Cost Magnitude Estimate

| Item | Magnitude (trillion ¥) | Description |
|------|:---------------------:|-------------|
| Solar cell array (960 km²) | ≈5–8 | Flexible film manufacturing + launch + in-orbit deployment |
| Microwave power transmission antennas (6 nodes) | ≈2–3 | Phased array antennas + ground rectennas |
| On-ring HVDC transmission network | ≈1–2 | Aluminum alloy conductor + insulation + converter stations |
| Energy storage system (SMES + hydrogen) | ≈0.5–1 | — |
| Fiber communication backbone network | ≈0.5–1 | Fiber + optical amplifiers + 6 node switches |
| Ground antennas + navigation enhancement | ≈0.3–0.5 | — |
| **Total for energy and communication systems** | **≈10–15 trillion ¥** | — |


## 9.8 Conclusion of Volume 9

This volume completes the quantitative planning of the energy and communication infrastructure for the Space Ringed-Elevation. Core conclusions:

1. **Space Solar Power Station**: 500 GW installed capacity requires about 960 km² of flexible film cell array, with an average distribution width of only about 3.6 m along the ring. **During the shadow period, the affected arc segment on the ring is only about 300 km (vernal equinox), with a storage demand of about 2.5 GWh**, significantly reduced from previous versions. Microwave power transmission end-to-end efficiency is about 48%, with a total ground power delivery of about 58 GW from 6 nodes.
2. **On-Ring Power Distribution Network**: HVDC ±100 kV dual-redundant ring bus, resistance about 875 Ω, power is mainly consumed locally, on-ring self-use power about 1.4 GW.
3. **Communication Backbone**: DWDM dual-redundant fiber ring with a total capacity of about 3.8 Pbps, optical amplifier spacing of 100 km is feasible. The 6 node platforms achieve seamless ground coverage and centimeter-level GNSS enhancement.
4. **Total cost of energy and communication systems is about 10–15 trillion ¥**, accounting for about 15%–25% of the total project investment.

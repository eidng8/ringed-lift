# Appendix 2: Stratospheric Platform

## Volume 6: Communication Relay Subsystem

**Version**: 1.2<br/>
**Compiled Date**: June 2026<br/>
**Currency Unit**: Chinese Yuan (RMB), Symbol: ¥<br/>
**Related Main Volume**: Main Volume 9<br/>
**Prerequisites**: Volume 1, Volume 2, Volume 3 of this Appendix


### Abbreviation Table

| Abbreviation | Full Name | Description |
|------|----------|------|
| BER | Bit Error Rate | Bit Error Rate |
| BPSK | Binary Phase Shift Keying | Binary Phase Shift Keying |
| CCSDS | Consultative Committee for Space Data Systems | Consultative Committee for Space Data Systems |
| CNR | Carrier-to-Noise Ratio | Carrier-to-Noise Ratio |
| DTN | Delay-Tolerant Networking | Delay-Tolerant Networking |
| DWDM | Dense Wavelength Division Multiplexing | Dense Wavelength Division Multiplexing |
| EIRP | Effective Isotropic Radiated Power | Effective Isotropic Radiated Power |
| FEC | Forward Error Correction | Forward Error Correction |
| Gbps | Gigabits per second | Gigabits per second |
| GEO | Geostationary Earth Orbit | Geostationary Earth Orbit |
| GNSS | Global Navigation Satellite System | Global Navigation Satellite System |
| GPS | Global Positioning System | Global Positioning System |
| HAPS | High Altitude Pseudo-Satellite | Internationally accepted designation for stratospheric platforms |
| IF | Intermediate Frequency | Intermediate Frequency |
| ITU | International Telecommunication Union | International Telecommunication Union |
| LEO | Low Earth Orbit | Low Earth Orbit |
| LNA | Low Noise Amplifier | Low Noise Amplifier |
| Mbps | Megabits per second | Megabits per second |
| MEO | Medium Earth Orbit | Medium Earth Orbit |
| MLI | Multi-Layer Insulation | Passive thermal control for electronics bays |
| QAM | Quadrature Amplitude Modulation | Quadrature Amplitude Modulation |
| QPSK | Quadrature Phase Shift Keying | Quadrature Phase Shift Keying |
| RHU | Radioisotope Heater Unit | Used to maintain equipment operating temperature in high-altitude low-temperature environments |
| SNR | Signal-to-Noise Ratio | Signal-to-Noise Ratio |
| TVS | Transient Voltage Suppressor | Transient Voltage Suppressor |
| UHMWPE | Ultra-High Molecular Weight Polyethylene | Insulation and wear-resistant material |


### 6.1 Volume Preface

This volume is positioned as the **communication and data transmission infrastructure** of the stratospheric platform system, focusing on answering the following core questions:

> How can a stratospheric platform, stationed long-term at an altitude of 20–50 km, achieve high-speed, reliable communications with ground stations, Ring Elevator GEO nodes, other stratospheric platforms, and working gondolas? How do the Ka/Ku-band antennas carried by the platform interface with the Ring Elevator's DWDM fiber optic backbone network? How can the platform's altitude advantage be leveraged to provide broadcast and navigation augmentation services to the ground? How can real-time video and telemetry data during maintenance operations be returned with low latency? How can data be stored and reliably forwarded after link restoration in case of communication link interruption?

This volume builds upon:
- **Volume 1 of this Appendix (Platform Overall Design)**: The aerostat's station-keeping altitude range (25–35 km), the fiber optic embedded within the tethering cable, and the platform's basic power supply capability have been established.
- **Volume 2 of this Appendix (Energy and Positioning Systems)**: The platform's energy supply and navigation/positioning capabilities have been established, providing the basis for the power budget and antenna pointing for the communication equipment in this volume.
- **Main Volume 9 (Energy and Communication Infrastructure)**: The Ring Elevator's DWDM fiber optic backbone network, ground-facing communication coverage, and navigation augmentation scheme have been designed. This volume defines the communication interface between the stratospheric platform and the Ring Elevator; detailed design is in Main Volume 9, Sections 9.5–9.6.

Core tasks of this volume:

1. Design the ground-facing communication link (Ka/Ku-band) for the stratospheric platform to achieve high-speed data exchange with ground stations.
2. Design the communication link between the stratospheric platform and Ring Elevator GEO nodes, specifying interface parameters.
3. Design the inter-platform networking communication scheme (multi-platform collaboration).
4. Design the broadcasting scheme for ground-directed broadcast and navigation augmentation signals, enhancing the coverage capability of the Ring Elevator navigation augmentation system.
5. Design real-time video and telemetry/command links between the working gondola and the aerostat, ensuring remote monitoring during maintenance operations.
6. Design a data storage and Delay-Tolerant Networking (DTN) scheme to handle communication interruption scenarios.
7. Provide the equipment list, mass estimates, power consumption, and key parameters such as antenna aperture for the communication subsystem.
8. Output key parameters for use by Volume 8 (Deployment and Maintenance) and Volume 9 (Economic Model), and interface with relevant volumes of the Main Volumes.


### 6.2 Communication Requirements Analysis

The communication requirements of the stratospheric platform are divided into the following categories:

| Requirement Type | Communication Target | Data Rate | Latency Requirement | Availability Requirement |
|:---|:---|:---:|:---:|:---:|
| Ground-Facing Backbone Data | Ground control centers, terrestrial networks | ≥100 Mbps (uplink) / ≥500 Mbps (downlink) | ≤500 ms | ≥99.9% |
| Ring Elevator Backbone Access | Ring Elevator GEO nodes (via relay) | ≥1 Gbps (bidirectional) | ≤100 ms | ≥99.99% |
| Inter-Platform Collaboration | Other stratospheric platforms | ≥10 Mbps | ≤200 ms | ≥99% |
| Gondola Operations Link | Working gondola (during ascent/descent) | ≥50 Mbps (video + telemetry) | ≤50 ms | ≥99.9% |
| Navigation Augmentation Signal | Ground users (GNSS differential) | ≤50 kbps (broadcast) | ≤1 s | ≥99% |
| Data Storage and Forwarding | Local storage (during interruptions) | As required | Delay-tolerant | — |


### 6.3 Ground-Facing Communication Link Design

#### 6.3.1 Link Architecture

The communication between the stratospheric platform and the ground adopts a **Ka-band** (27–40 GHz) and **Ku-band** (12–18 GHz) dual-frequency redundant design:
- **Ka-band**: Primary link, high bandwidth (≥500 Mbps downlink), suitable for high-capacity data return (e.g., high-resolution video, sensor data).
- **Ku-band**: Backup link, lower bandwidth (≥50 Mbps), but with better rain fade characteristics than Ka-band, maintaining basic communications in severe weather.

Ground stations are deployed at the stratospheric platform anchoring points (shared with Ring Elevator ground stations or independently constructed), with antenna apertures ≥3 m and automatic tracking capability.

#### 6.3.2 Link Budget (Ka-Band)

Using station-keeping altitude $h = 30  \text{km}$, ground station antenna aperture $D_g = 3  \text{m}$, platform antenna aperture $D_p = 0.6  \text{m}$, and frequency $f = 30  \text{GHz}$ (wavelength $\lambda = 0.01  \text{m}$) as the baseline.

**(a) Free-Space Path Loss**

$$
L_{\text{fs}} = \left(\frac{4\pi R}{\lambda}\right)^2
$$

where $R$ is the slant range. At zenith $R = h = 30  \text{km}$; increases at lower elevation angles. Conservatively taking the zenith direction:

$$
L_{\text{fs}} = \left(\frac{4\pi \times 3 \times 10^4}{0.01}\right)^2 = \left(3.77 \times 10^7\right)^2 \approx 1.42 \times 10^{15}
$$

In logarithmic form:

$$
L_{\text{fs,dB}} = 10 \lg(1.42 \times 10^{15}) \approx 151.5  \text{dB}
$$

**(b) Atmospheric Attenuation**

At 30 GHz Ka-band, atmospheric attenuation mainly includes oxygen absorption and water vapor absorption. According to the ITU-R P.676-13 model, integrated oxygen absorption over a 30 km zenith path is approximately 1 dB, and water vapor absorption is approximately 1 dB (standard atmosphere, moderate humidity). Rain fade is estimated at approximately 2 dB for moderate rainfall intensity (10 mm/h), but to meet link availability ≥99.9%, a margin must be reserved for heavy rainfall (50 mm/h) of approximately 10 dB.

Therefore the design values are:
- Typical value: $L_{\text{atm,typ}} = 1 + 1 + 2 = 4  \text{dB}$
- Design value (with margin): $L_{\text{atm,des}} = 1 + 1 + 10 = 12  \text{dB}$

**(c) Antenna Gain**

Platform antenna aperture $D_p = 0.6  \text{m}$, efficiency $\eta = 0.6$:

$$
G_p = \eta \left(\frac{\pi D_p}{\lambda}\right)^2 = 0.6 \times \left(\frac{\pi \times 0.6}{0.01}\right)^2 = 0.6 \times (188.5)^2 \approx 0.6 \times 35,500 \approx 21,300
$$

In logarithmic form:

$$
G_{p,\text{dB}} = 10 \lg(21,300) \approx 43.3  \text{dB}
$$

Ground station antenna aperture $D_g = 3  \text{m}$:

$$
G_g = 0.6 \times \left(\frac{\pi \times 3}{0.01}\right)^2 = 0.6 \times (942.5)^2 \approx 0.6 \times 888,000 \approx 533,000
$$

$$
G_{g,\text{dB}} = 10 \lg(533,000) \approx 57.3  \text{dB}
$$

**(d) Transmit Power and Received Carrier-to-Noise Ratio**

Platform transmitter RF output power $P_{t,\text{RF}} = 10  \text{W}$, corresponding to $40  \text{dBm}$. DC input power of the power amplifier is approximately 2.5 times the output power (40% efficiency). The link is calculated using RF power below.

Signal power received at the ground station (design value, including rain fade margin):

$$
P_r = P_t + G_p + G_g - L_{\text{fs}} - L_{\text{atm,des}}
$$

Substituting values (in dB):

$$
P_r = 40 + 43.3 + 57.3 - 151.5 - 12 = 40 + 43.3 + 57.3 - 163.5 = 140.6 - 163.5 = -22.9  \text{dBm}
$$

Ground station receiver noise temperature $T = 150  \text{K}$ (including LNA and antenna noise), noise power:

$$
N = kTB = 1.38 \times 10^{-23} \times 150 \times B
$$

Bandwidth $B = 500  \text{MHz} = 5 \times 10^8  \text{Hz}$:

$$
N = 1.38 \times 10^{-23} \times 150 \times 5 \times 10^8 = 1.035 \times 10^{-12}  \text{W}
$$

In logarithmic form:

$$
N_{\text{dBm}} = 10 \lg(1.035 \times 10^{-12} \times 1000) = 10 \lg(1.035 \times 10^{-9}) = 10 \times (-8.99) \approx -89.9  \text{dBm}
$$

Carrier-to-noise ratio:

$$
\text{CNR} = P_r - N_{\text{dBm}} = -22.9 - (-89.9) = 67.0  \text{dB}
$$

With QPSK modulation requiring CNR of approximately 12 dB, the margin is >55 dB, which is very ample. Higher-order modulation (e.g., 64QAM) can be adopted to improve spectral efficiency. Under typical atmospheric conditions ($L_{\text{atm,typ}} = 4 \text{dB}$), CNR can reach 75 dB.

#### 6.3.3 Antenna Design

| Parameter | Ka-Band Antenna | Ku-Band Antenna | Description |
|:---|:---:|:---:|:---|
| Type | Parabolic reflector | Parabolic reflector | — |
| Aperture | 0.6 m | 0.4 m | Installed on the underside of the aerostat or the top of the gondola |
| Operating Frequency | 27–31 GHz (transmit) / 30–40 GHz (receive) | 12–14 GHz (transmit) / 14–18 GHz (receive) | Compliant with ITU allocations |
| Polarization | Dual linear polarization (vertical/horizontal) | Dual linear polarization | Supports frequency reuse |
| Tracking Method | Program tracking + monopulse auto-tracking | Program tracking | Maintains pointing when platform moves |
| Radome | Sandwich structure (hail-resistant, UV-resistant) | Same as left | Protects antenna from high-altitude environment |
| Mass | ≤25 kg | ≤15 kg | — |
| Power Consumption (including servo) | ≤100 W | ≤50 W | — |


### 6.4 Interface Design with Ring Elevator Backbone Network

#### 6.4.1 Interface Architecture

The stratospheric platform accesses the Ring Elevator's DWDM fiber optic backbone network via a **GEO relay link**. The communication path is:

```
Stratospheric Platform → GEO Relay (Ka-band) → Ring Elevator GEO Node → Ring Elevator Fiber Backbone → Any Ground Station
```

The Ring Elevator GEO node (located 100 km from the GEO outer edge, integrated with the elevator top counterweight space station) is equipped with ground-facing/space-facing communication antennas.

#### 6.4.2 GEO Relay Link Budget

Link parameters: platform antenna aperture $D_p = 0.8  \text{m}$, Ring Elevator antenna aperture $D_g = 1.2  \text{m}$, frequency $f = 30  \text{GHz}$ ($\lambda = 0.01 \text{m}$), slant range $R \approx 36,000 \text{km}$.

**Antenna Gain** (efficiency $\eta = 0.6$):

$$
G_p = 0.6 \times \left(\frac{\pi \times 0.8}{0.01}\right)^2 = 0.6 \times (251.3)^2 \approx 0.6 \times 63,200 \approx 37,900 \quad (45.8  \text{dB})
$$

$$
G_g = 0.6 \times \left(\frac{\pi \times 1.2}{0.01}\right)^2 = 0.6 \times (377.0)^2 \approx 0.6 \times 142,100 \approx 85,300 \quad (49.3  \text{dB})
$$

**Free-Space Path Loss**:

$$
L_{\text{fs}} = \left(\frac{4\pi R}{\lambda}\right)^2 = \left(\frac{4\pi \times 3.6 \times 10^7}{0.01}\right)^2 \approx (4.52 \times 10^{10})^2 \approx 2.04 \times 10^{21}
$$

$$
L_{\text{fs,dB}} = 10 \lg(2.04 \times 10^{21}) \approx 213  \text{dB}
$$

**Atmospheric Attenuation** (high elevation angle, path shorter than zenith): take $L_{\text{atm}} \approx 2  \text{dB}$.

**Received Power** (platform transmit RF power $P_t = 20  \text{W} = 43  \text{dBm}$):

$$
P_r = 43 + 45.8 + 49.3 - 213 - 2 = 138.1 - 215 = -76.9  \text{dBm}
$$

**Noise Power** (bandwidth $B = 1  \text{GHz} = 1 \times 10^9  \text{Hz}，T = 150  \text{K}$):

$$
N = 1.38 \times 10^{-23} \times 150 \times 1 \times 10^9 = 2.07 \times 10^{-12}  \text{W} \quad (-86.8  \text{dBm})
$$

**Carrier-to-Noise Ratio**:

$$
\text{CNR} = -76.9 - (-86.8) = 9.9  \text{dB}
$$

With 64QAM + FEC (code rate 3/4), the required CNR is approximately 11–12 dB; 9.9 dB is slightly insufficient. QPSK (required CNR approximately 8 dB) can be used instead, or transmit power increased to 30 W ($44.8 \text{dBm}$), raising CNR to approximately 11.7 dB, meeting the requirement. **This volume sets platform transmit power ≤20 W, uses QPSK modulation; data rate ≥1 Gbps is feasible.**

#### 6.4.3 Interface Parameters

| Parameter | Design Value | Description |
|:---|:---|:---|
| Operating Frequency Band | Ka-band (uplink 29–31 GHz, downlink 19–21 GHz) | Coordinated with Main Volume 9, Section 9.5 Ring Elevator communication link |
| Modulation Scheme | QPSK + FEC (code rate 3/4) | High robustness |
| Data Rate | ≥1 Gbps (bidirectional) | Satisfies Ring Elevator-side aggregated traffic |
| Antenna Aperture (Platform Side) | 0.8 m | Including radome and dual-axis servo mechanism |
| Antenna Aperture (Ring Elevator Side) | 1.2 m | Installed at Ring Elevator GEO node |
| Transmit RF Power (Platform) | ≤20 W | DC input power ≤50 W (40% efficiency) |
| Link Availability | ≥99.99% | Including rain fade margin |
| Bit Error Rate (BER) | ≤10⁻⁷ (uncoded) | ≤10⁻¹² after FEC |

#### 6.4.4 Interface Notes with Main Volumes

Detailed frequency coordination, routing protocols, and network management between the stratospheric platform and the Ring Elevator backbone are defined in Main Volume 9, Sections 9.5–9.6. This volume only specifies the physical and link layer parameters on the platform side. When the stratospheric platform is deployed at a Ring Elevator anchoring node, the platform accesses the Ring Elevator network via the GEO relay link; when the platform is deployed independently (without a Ring Elevator), it connects to the Internet directly through a ground station.


### 6.5 Inter-Platform Communication (Multi-Platform Collaboration)

When multiple stratospheric platforms are deployed along the equator or polar regions, the platforms can form a **mesh network** for data relay and collaborative operations.

| Parameter | Design Value | Description |
|:---|:---|:---|
| Operating Frequency Band | Ku-band (14–14.5 GHz) | ITU-allocated point-to-point communication band |
| Modulation Scheme | QPSK / 8PSK | Adaptive based on link quality |
| Data Rate | 10–100 Mbps | Depends on inter-platform spacing (typically 200–500 km) |
| Antenna Type | Flat-panel phased array | Electronically scanned tracking, mass ≤10 kg per unit |
| Communication Protocol | IP-based DTN (see Section 6.8) | Tolerates delay and interruptions |
| Maximum Single-Hop Distance | ≥600 km (line-of-sight) | Platform altitude 30 km, horizon distance approximately 620 km |
| Coverage Extension | Multi-platform chain relay can extend to thousands of kilometers | — |

> At platform altitude 30 km, the horizon distance formula is $d = \sqrt{2R_e h}$, taking Earth radius $R_e = 6371 \text{km}, h = 30 \text{km}$, giving $d \approx 619 \text{km}$. Therefore, the maximum single-hop line-of-sight communication distance is approximately 600 km.


### 6.6 Ground-Directed Broadcast and Navigation Augmentation Signals

#### 6.6.1 Ground-Directed Broadcast Services

The stratospheric platform carries an **L-band broadcast antenna** (frequency 1.5–1.6 GHz) that can broadcast to users in its ground coverage area:
- Meteorological data (high-altitude wind fields, temperature, humidity profiles)
- Disaster warnings (tsunamis, earthquakes, volcanic ash dispersion)
- Traffic information (aviation, maritime)
- Emergency communications (when ground communications are interrupted by disasters)

Broadcast coverage: at platform altitude 30 km, horizon distance approximately 620 km. A single platform can cover an area with a radius of approximately 600 km. Multiple platforms networked together can achieve continuous coverage of the equatorial belt or polar regions.

| Parameter | Design Value | Description |
|:---|:---|:---|
| Operating Frequency | 1.5–1.6 GHz (L-band) | Adjacent to GNSS, facilitating shared receiver front-ends |
| Transmit RF Power | ≤50 W (EIRP ≤20 dBW) | Compliant with ITU broadcast power limits |
| Modulation Scheme | BPSK or QPSK | High robustness |
| Data Rate | ≤50 kbps | Broadcast mode |
| Antenna Type | Omnidirectional whip antenna (gain ≥2 dBi) | Mass ≤2 kg |

#### 6.6.2 Navigation Augmentation Signals

The stratospheric platform can serve as a **GNSS differential correction station**, broadcasting pseudorange and carrier-phase corrections to improve positioning accuracy for users in the coverage area from meter-level to centimeter-level (real-time kinematic) or millimeter-level (post-processing). This function operates in coordination with the Ring Elevator navigation augmentation system described in Main Volume 9, Section 9.6.2: the stratospheric platform provides high-density differential signals for the low-altitude (0–50 km) regional area, while Ring Elevator GEO nodes provide wide-area differential signals for global coverage.

| Parameter | Design Value | Description |
|:---|:---|:---|
| Operating Frequency | L1 (1575.42 MHz), L2 (1227.60 MHz), L5 (1176.45 MHz) | Compatible with GPS/BeiDou/Galileo |
| Transmit RF Power | ≤10 W (per frequency) | — |
| Differential Correction Update Rate | 1 Hz (static) / 5 Hz (dynamic) | — |
| Coverage Radius | ≥500 km (within line-of-sight) | — |
| Positioning Accuracy (Real-time) | Horizontal ≤5 cm, Vertical ≤10 cm | Theoretical values under dual-frequency carrier-phase differential conditions; actual accuracy depends on user receiver performance and environmental multipath effects |
| Coordination with Ring Elevator | Stratospheric platform differential signals serve as a supplement to the Ring Elevator navigation augmentation system | See Main Volume 9, Section 9.6.2 |


### 6.7 Working Gondola Communication Link

#### 6.7.1 Link Requirements

As the working gondola climbs along the tethering cable (altitude 0–50 km), it needs to maintain real-time communication with the aerostat, transmitting:
- High-definition video (≥1080p, for maintenance monitoring)
- Telemetry data (position, velocity, temperature, vibration)
- Control commands (gondola motion, tool operations)

#### 6.7.2 Communication Scheme

Since the gondola moves along the tethering cable, traditional wireless links may be obstructed by the cable. **Fiber optic embedded in the tethering cable** is used as the primary communication channel, with a wireless link as backup.

| Communication Method | Bandwidth | Latency | Availability | Description |
|:---|:---:|:---:|:---:|:---|
| **Embedded Fiber Optic (Primary)** | ≥1 Gbps | <1 ms | ≥99.99% | Uses the fiber optic embedded in the tethering cable from Volume 1, Section 1.5 of this Appendix |
| **Wireless (Backup, 5.8 GHz)** | ≥50 Mbps | <10 ms | ≥99% | Activated when fiber fails; gondola top-mounted antenna |

**Fiber Bending Reliability**: The tethering cable undergoes repeated bending during deployment and retrieval; the embedded fiber optic must withstand ≥10⁴ deployment/retrieval cycles without damage. Key design considerations:
- Winch drum diameter ≥0.5 m, cable bending radius ≥0.25 m.
- Use bend-resistant single-mode fiber (G.657.A1/A2), with minimum bending radius as low as 7.5 mm, meeting engineering requirements.
- Bending fatigue testing (≥10⁴ deployment/retrieval cycles, attenuation increase ≤0.1 dB) must be performed before deployment.

**Fiber Link Budget**: Single-mode fiber at 1,550 nm wavelength has attenuation of approximately 0.2 dB/km. For 50 km cable length, total attenuation is approximately 10 dB; adding connector and splice losses of approximately 2 dB, total is 12 dB. Using optical modules with output power ≥0 dBm and receive sensitivity ≤-20 dBm (1 Gbps), the margin is sufficient.

| Parameter | Design Value | Description |
|:---|:---|:---|
| Fiber Type | G.652.D / G.657.A1/A2 | Same type as Ring Elevator communication backbone, bend-resistant |
| Wavelength | 1,310 nm / 1,550 nm | Dual wavelength for bidirectional transmission |
| Data Rate | 1 Gbps (bidirectional) | Expandable to 10 Gbps |
| Optical Module Mass (Gondola Side) | ≤0.5 kg | Miniaturized SFP+ module |
| Wireless Backup Frequency | 5.8 GHz ISM band | Directional antenna, radiating along the cable |
| Wireless Backup Transmit RF Power | ≤1 W (EIRP) | No interference with other systems |


### 6.8 Data Storage and Delay-Tolerant Networking (DTN)

#### 6.8.1 Data Storage

The stratospheric platform is equipped with **large-capacity solid-state storage** for buffering the following data:
- Scientific data, video, and telemetry collected during communication interruptions
- Data packets awaiting forwarding to other platforms or the ground

| Parameter | Design Value | Description |
|:---|:---|:---|
| Storage Capacity | ≥10 TB | Solid-state drives (NVMe) |
| Write Speed | ≥500 MB/s | Matches high-speed data such as video streams |
| Storage Redundancy | RAID 1 (mirroring) | Prevents data loss due to single drive failure |
| Off-Site Backup | Critical data is automatically sent as copies to ground stations or other platforms via the DTN mechanism | Achieves off-site backup |
| Storage Mass | ≤5 kg | Including controller and enclosure |
| Power Consumption | ≤20 W (average) | ≤5 W in standby |

#### 6.8.2 Delay-Tolerant Networking (DTN) Protocol

Communication links between the platform and the ground, between the platform and the Ring Elevator, and between platforms may be interrupted due to weather, obstruction, or equipment failure. **DTN protocol** (RFC 4838) is used to implement store-and-forward:

- Each data packet is encapsulated as a "Bundle", containing source, destination, creation time, time-to-live, and other information.
- When a link is available, data is forwarded immediately; when unavailable, data is stored in local storage and awaits a future forwarding opportunity.
- Supports "Custody Transfer": once the next-hop node confirms receipt, the sending node may delete its local copy.
- Critical data (emergency commands, important telemetry) is simultaneously stored and automatically sent as copies to ground stations or other platforms via the DTN mechanism, achieving off-site backup.

The DTN protocol stack runs on the platform's control computer and is seamlessly integrated with the IP network.

| Parameter | Design Value | Description |
|:---|:---|:---|
| Protocol Standard | RFC 4838 / RFC 5050 (Bundle Protocol) | Compatible with CCSDS DTN |
| Maximum Bundle Size | 64 MB | Configurable |
| Time-to-Live | 7 days (default) | Discarded upon timeout |
| Store-and-Forward Queue | Priority queue (Control > Telemetry > Video > Scientific Data) | Ensures critical data is sent first |


### 6.9 Equipment List and Mass Estimates

| Equipment | Quantity | Unit Mass | Subtotal | Description |
|:---|:---:|:---:|:---:|:---|
| Ka-band antenna (0.6 m) | 1 set | ≤25 kg | ≤25 kg | Primary ground-facing link |
| Ku-band antenna (0.4 m) | 1 set | ≤15 kg | ≤15 kg | Backup ground-facing link |
| GEO relay antenna (0.8 m) | 1 set | ≤50 kg (target 40 kg) | ≤50 kg | Including radome and dual-axis servo mechanism |
| Inter-platform phased array | 2 units | ≤10 kg/unit | ≤20 kg | Both directions |
| L-band broadcast antenna | 1 set | ≤2 kg | ≤2 kg | Ground-directed broadcast |
| GNSS navigation augmentation transmitter | 1 set | ≤5 kg | ≤5 kg | Including power amplifier and antenna |
| Gondola optical transceiver | 1 set (gondola side) + 1 set (platform side) | ≤0.5 kg + ≤2 kg | ≤2.5 kg | — |
| Wireless backup module (5.8 GHz) | 1 set | ≤1 kg | ≤1 kg | Gondola wireless link |
| Solid-state storage (10 TB, RAID 1) | 1 set | ≤5 kg | ≤5 kg | — |
| Network switch (10 Gigabit) | 1 unit | ≤3 kg | ≤3 kg | Including optical-to-electrical conversion |
| DTN routing computer | 1 unit | ≤2 kg | ≤2 kg | Industrial-grade embedded |
| Cables, connectors, waveguides | 1 set | ≤5 kg | ≤5 kg | — |
| **Total** | — | — | **≤135.5 kg** | — |

> Note: The above are net masses of the components carried by the stratospheric platform, excluding ground station equipment. Ground station equipment (≥3 m antennas, RF equipment, etc.) is independently constructed at the anchoring station and is not launched with the platform.


### 6.10 Power Consumption Estimates

| Equipment | Average Input Power | Peak Input Power | Description |
|:---|:---:|:---:|:---|
| Ka-band transmitter | 50 W | 100 W | RF output power 10 W (average) / 20 W (peak), power amplifier efficiency 40% |
| Ku-band transmitter | 25 W | 50 W | ≤5 W in standby mode |
| GEO relay transmitter | 50 W | 100 W | RF output power 20 W, power amplifier efficiency 40% |
| Inter-platform phased array | 20 W (per unit) | 50 W | — |
| L-band broadcast transmitter | 10 W | 20 W | RF output power 4 W (average), power amplifier efficiency 40% |
| GNSS navigation augmentation transmitter | 15 W | 30 W | RF output power 6 W, power amplifier efficiency 40% |
| Optical transceiver (platform side) | 10 W | 15 W | — |
| Network switch | 15 W | 25 W | — |
| DTN computer + storage | 25 W | 40 W | — |
| **Total** | **≈230 W** | **≈450 W** | — |

> Note: The power consumption column for transmitters is DC input power; RF output power is calculated at 40% efficiency. The above power is supplied by the energy system (photovoltaic + battery) in Volume 2 of this Appendix. Some transmitters can be shut down during low communication loads to reduce power consumption.


### 6.11 Parameter Outputs

| Parameter | Value | Status | Receiving Volume |
|:---|:---|:---|:---|
| Ground-Facing Ka-Band Data Rate | ≥500 Mbps (downlink) / ≥100 Mbps (uplink) | Design baseline | — |
| Ground-Facing Ku-Band Backup Rate | ≥50 Mbps | Design baseline | — |
| GEO Relay Data Rate | ≥1 Gbps (bidirectional) | Design baseline | Main Volume 9 |
| Inter-Platform Communication Rate | 10–100 Mbps | Design baseline | — |
| Gondola Fiber Communication Rate | 1 Gbps (bidirectional) | Design baseline | Volume 3 |
| Navigation Augmentation Positioning Accuracy | Horizontal ≤5 cm, Vertical ≤10 cm | Design baseline | Main Volume 9 |
| Storage Capacity | ≥10 TB | Design baseline | — |
| Communication Subsystem Total Mass | ≤135.5 kg | Order-of-magnitude estimate | Volume 8 (Deployment) |
| Communication Subsystem Average Power | ≈230 W | Order-of-magnitude estimate | Volume 2 (Energy) |
| Ring Elevator Interface Frequency | Ka-band (uplink 29–31 GHz, downlink 19–21 GHz) | Interface parameter | Main Volume 9 |
| DTN Protocol | RFC 4838 / 5050, CCSDS-compatible | Design baseline | — |
| Gondola Fiber Minimum Bending Radius | ≥50 mm (long-term), winch drum diameter ≥0.5 m | Design constraint | Volume 1 |


### 6.12 Volume 6 Concluding Remarks

This volume has completed the full design of the communication relay subsystem for the stratospheric platform. The core contributions are:

1. **Designed a dual-frequency ground-facing communication link** (Ka-band primary, Ku-band backup), with the link budget accounting for atmospheric attenuation and rain fade margin; the margin is sufficient to meet ≥500 Mbps downlink rate.
2. **Supplemented the detailed budget for the GEO relay link**, confirming that ≥1 Gbps is feasible with QPSK modulation, with clear antenna mass targets.
3. **Clarified the interface parameters with the Ring Elevator backbone network**, coordinated with Main Volume 9.
4. **Designed inter-platform mesh communication** (Ku-band phased array, 10–100 Mbps), maximum single-hop distance ≥600 km, extendable to thousands of kilometers via multi-platform chain relay.
5. **Planned ground-directed broadcast and navigation augmentation services**, with explicitly stated preconditions for accuracy, complementing the Ring Elevator system.
6. **Designed the gondola communication link**: primary channel using bend-resistant fiber embedded in the tethering cable (1 Gbps), with 5.8 GHz wireless as backup, and specified bending radius and winch drum diameter constraints.
7. **Configured data storage and DTN protocol**: 10 TB solid-state storage + RAID 1 mirroring + off-site backup, using RFC 4838 Bundle Protocol to ensure no data loss during communication interruptions.
8. **Quantified equipment mass and power consumption**: total mass approximately 135.5 kg, average power approximately 230 W, impact on overall platform design is within acceptable range.

This volume's output parameters can support Volume 8 (Deployment and Maintenance) and Volume 9 (Economic Model), and are fully interfaced with Main Volume 9 (Energy and Communication Infrastructure). It is recommended to complete Ka-band link field testing and fiber bending fatigue testing before engineering implementation (items to be verified are suggested for inclusion in Volume 7).


### References

[1] ITU-R. *Recommendation P.676-13: Attenuation by atmospheric gases*. Geneva: International Telecommunication Union, 2022.

[2] RFC 4838. *Delay-Tolerant Networking Architecture*. IETF, 2007.

[3] CCSDS. *CCSDS 730.1-G-1: Delay-Tolerant Networking (DTN) Architecture for Space Communication*. Washington, DC: CCSDS, 2023.

[4] Standardization Administration of China. *GB/T 12572-2008 General Requirements for Parameters of Radio Transmission Equipment*. Beijing: Standards Press of China, 2008.

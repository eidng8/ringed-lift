# Appendix 2: Stratospheric Platform

## Volume 5: Lightning Attraction and Protection Subsystem

**Version**: 1.6<br/>
**Compiled Date**: June 2026<br/>
**Currency Unit**: Chinese Yuan (RMB), Symbol: ¥<br/>
**Related Main Volumes**: Main Volume 3, Main Volume 7<br/>
**Prerequisites**: Volume 1 of this Appendix, Volume 2 of this Appendix


### Abbreviation Table

| Abbreviation | Full Name | Description |
|------|----------|------|
| CFRP | Carbon Fiber Reinforced Polymer | Lightweight high-strength material for lightning attraction towers and conductor brackets |
| CNT | Carbon Nanotube | Candidate material for lightning attraction conductors |
| EDM | Electric field change meter | Used for real-time monitoring of thunderstorm electric fields |
| EMC | Electromagnetic Compatibility | Electromagnetic Compatibility |
| ESD | Electrostatic Discharge | Electrostatic Discharge |
| GFD | Ground Flash Density | Ground Flash Density |
| GIS | Geographic Information System | Geographic Information System |
| HAPS | High Altitude Pseudo-Satellite | Internationally accepted designation for stratospheric platforms |
| Inconel | Chromium-nickel-iron alloy | High-temperature and corrosion-resistant material used for lightning tips |
| LLS | Lightning Location System | Lightning Location System |
| MLI | Multi-Layer Insulation | Used for passive thermal control of electronics compartments |
| MoS₂ | Molybdenum Disulfide | Solid lubricant |
| PTFE | Polytetrafluoroethylene | Insulation and sealing material |
| RHU | Radioisotope Heater Unit | Used to maintain equipment operating temperature in high-altitude low-temperature environments |
| SPUA | Spray Polyurea Elastomer | Used for conductor sealing and insulation |
| UHMWPE | Ultra-High Molecular Weight Polyethylene | Insulation and wear-resistant material |


### 5.1 Volume Preface

This volume is positioned as the **active lightning protection and safety subsystem** of the stratospheric platform system, focusing on answering the following core questions:

> How does a stratospheric platform residing at 20–50 km altitude long-term avoid becoming a preferential discharge channel for atmospheric lightning? What technical approach should active lightning attraction adopt — fixed conductors, lightning rockets, laser lightning attraction, or leading-edge plasma jets? How should the lightning attraction device be designed? How can the lightning current be safely conducted into the ground? How can the platform itself survive in a thunderstorm environment? What is the complete lightning protection operating procedure from warning to response?

**Important Prerequisites**: The lightning attraction system designed in this volume (including fixed conductors, pulse power supplies, and ground dissipation networks) **relies on ground anchoring facilities** (grounding grids and equalization systems) to function properly. The lightning attraction conductor directs the lightning current into the embedded conductive layer of the tethering cable, which is then discharged into the ground through the grounding grid at the ground anchoring station. Without reliable ground anchoring (i.e., without forming a low-impedance path to ground), the lightning current cannot be safely dispersed, and the lightning attraction system will be rendered ineffective or even dangerous. Therefore, this scheme is only applicable to stratospheric platforms **that have already established ground anchoring facilities**. When a stratospheric platform is deployed at a Ring Elevator anchoring node, the Ring Elevator's grounding system can be directly utilized (see Main Volume 3, Section 3.3 and Main Volume 7, Section 7.6.1); if deployed at an independent anchoring point, a grounding network must be independently constructed as specified in Section 5.4.2 of this volume.

This volume builds upon:
- **Volume 1 of this Appendix (Platform Overall Design)**: The aerostat's residing altitude range (25–35 km), the lifting capability of the working gondola, and the strategic positioning of the lightning attraction function have been established.
- **Volume 2 of this Appendix (Energy and Positioning Systems)**: The platform's energy supply and communication/positioning capabilities have been established, providing power and communication interfaces for the warning system and lightning attraction trigger device in this volume.
- **Main Volume 3 (Node Site Selection and Anchoring Engineering)**: If the stratospheric platform shares an anchoring node with the Ring Elevator, the ground grounding system must meet the design requirements of Main Volume 3. This volume retains only the interface description; detailed design is found in Main Volume 3, Section 3.3 and Main Volume 7, Section 7.6.1.
- **Main Volume 7 (Engineering Verification)**: A three-layer defense system framework for lightning protection has been provided (active lightning attraction tower arrays, cable insulation with embedded shielding, and ground equalization grounding networks); this volume converts this framework into an executable engineering scheme for the stratospheric platform.

Core tasks of this volume:

1. Compare and analyze four lightning attraction schemes (fixed conductors, lightning rockets, laser lightning attraction, leading-edge plasma jets), and provide the basis for selection.
2. Analyze the corona discharge efficiency problem of the fixed conductor scheme in low-pressure environments, providing quantitative evaluation and countermeasures.
3. Design the overall scheme for the leading-edge trigger lightning attraction device — including material selection for the lightning attraction conductor, structural parameters, leading-edge trigger strategy, and active control logic.
4. Design the complete path for conducting lightning current from the stratospheric platform into the ground — including the embedded conductor in the tethering cable, ground dissipation network (interface only when shared with the Ring Elevator), and equalization grounding system.
5. Design the lightning protection system for the stratospheric platform itself — including structural lightning protection, electronic equipment surge protection, lightning electromagnetic pulse protection, and personnel safety.
6. Establish a thunderstorm warning and safe descent procedure — integrating ground-based lightning location systems, satellite-borne lightning monitoring, and electric field meters carried by the platform, forming a tiered warning and automatic response mechanism, and clarifying the physical necessity of descent.
7. Provide the equipment list, mass estimates, and energy consumption parameters for the lightning attraction and protection subsystem.
8. Output key parameters for use by Volume 8 (Deployment and Maintenance) and Volume 9 (Economic Model), and interface with relevant volumes of the Main Volumes.


### 5.2 Lightning Attraction Scheme Comparison and Selection Basis

There are currently four main technical pathways for active lightning attraction at stratospheric platform altitude (20–50 km): **fixed conductors (with active pulse triggering)**, **lightning rockets**, **laser lightning attraction**, and **leading-edge plasma jets**. The following comparison is made across four dimensions: engineering feasibility, reliability, mass, and cost.

#### 5.2.1 Lightning Rocket Scheme

**Principle**: A small rocket trailing a thin metal wire is fired toward the thundercloud area. As the rocket ascends, the wire connects the thundercloud charge to the ground, triggering lightning to discharge along the wire channel.

**Advantages**:
- Relatively mature technology, widely applied in artificial lightning attraction experiments (such as ground-based lightning rocket experiments in the United States, France, China, etc.) [3].
- High single-shot lightning attraction success rate (>80%).

**Disadvantages**:
- **Non-sustainable**: Each lightning attraction consumes one rocket and wire; it cannot repeatedly attract lightning during the duration of a thunderstorm (several hours). The stratospheric platform would need to carry a large number of rockets, drastically increasing mass.
- **Safety risk**: The rocket's trajectory may interfere with the tethering cable or aerostat structure; igniting the rocket engine at near-platform altitude poses a fire risk.
- **High-altitude adaptability**: The reliability of rocket engines operating in the low-pressure environment above 20 km has not been sufficiently verified.
- **Deployment cycle**: Requires reloading after each lightning attraction; continuous triggering cannot be achieved.

**Engineering applicability assessment**: **Not recommended**. The stratospheric platform requires continuous active lightning attraction during thunderstorms (trigger frequency 5–10 Hz); lightning rockets cannot meet the continuity requirement.

#### 5.2.2 Laser Lightning Attraction Scheme

**Principle**: High-power femtosecond laser pulses are fired toward the thundercloud, ionizing a conductive plasma channel in the air, guiding lightning to discharge along that channel.

**Advantages**:
- No consumables, reusable.
- Trigger frequency can be extremely high (kHz level), theoretically capable of continuously guiding lightning.
- The laser beam direction is controllable, allowing active selection of the discharge channel direction.

**Disadvantages**:
- **Enormous energy requirements**: Generating a plasma channel longer than 100 m requires a femtosecond laser system with TW-level peak power; current laboratory devices are large (occupying >10 m²), weigh >1,000 kg, and consume >10 kW [4].
- **High-altitude propagation attenuation**: When laser light passes through low-density atmosphere at 20–50 km altitude, the nonlinear filamentation effect is significantly affected by air pressure, greatly reducing plasma channel stability and length.
- **Low technology readiness level**: Currently only ground-level short-range (<50 m) experimental verification exists; high-altitude, long-range lightning attraction has no engineering precedent.
- **Extremely high cost**: A femtosecond laser system can cost tens of millions to hundreds of millions of yuan.

**Engineering applicability assessment**: **Viable long-term option, not currently feasible**. Once laser technology achieves breakthroughs (system mass <200 kg, power consumption <5 kW), it can serve as an upgrade scheme. This volume records it as a long-term alternative.

#### 5.2.3 Leading-Edge Plasma Jet Scheme

**Principle**: A miniature plasma jet device (such as arc discharge or pulsed plasma thruster) is installed near the tip of the lightning attraction conductor. When the thunderstorm electric field intensifies, a high-temperature, high-conductivity plasma jet is sprayed toward the thundercloud, artificially creating a locally ionized channel to guide the upward leading edge to develop along this channel.

**Advantages**:
- Much lower energy consumption than pure laser lightning attraction (approximately 1–10 kJ per pulse, rather than megajoule-level).
- Plasma jets diffuse more rapidly and extend further in low-pressure environments (the lower the pressure, the more pronounced the jet expansion).
- Can be used in conjunction with fixed conductors as a supplementary means of active triggering.

**Disadvantages**:
- Each injection consumes a small amount of propellant (such as argon, helium, or solid ablation material), requiring gas cylinders or material storage, with consumable limitations.
- The jet direction is affected by platform attitude, requiring precise pointing control.
- The plasma channel maintenance time is short (millisecond level); precise triggering is needed at the moment of maximum electric field.
- Technology readiness level: Laboratory validation exists (e.g., plasma contactors for active potential control of spacecraft), but no engineering precedent for lightning attraction [5].

**Engineering applicability assessment**: **Optional supplementary scheme**. Can serve as an auxiliary to fixed conductor pulse triggering, "igniting" the initial ionization channel when the electric field intensity is insufficient, improving lightning attraction success rate. However, due to its consumable nature and additional mass (estimated additional 50–100 kg), it is not recommended as the primary scheme. This volume records it as an optional enhancement.

#### 5.2.4 Fixed Conductor (Active Pulse Triggering) Scheme

**Principle**: A CNT braided cable conductor 1–2 km long is suspended below the aerostat. High-voltage pulses are applied to the conductor tip to actively generate an upward leading edge, guiding lightning to discharge along the conductor.

**Advantages**:
- **No consumables**: The conductor is reusable; only periodic inspection and maintenance are required after lightning current impact.
- **Continuous triggering**: The pulse power supply can work continuously (5–10 Hz), covering the entire thunderstorm process.
- **Relatively high technology readiness level**: High-voltage pulse technology (solid-state Marx generators) is mature; CNT materials are high-temperature resistant, lightweight, and high-strength.
- **Controllable mass**: 2 km CNT conductor weighs only about 15 kg; pulse power supply about 200 kg; total system <400 kg.
- **Controllable cost**: Main costs are the pulse power supply and CNT material, far lower than laser lightning attraction systems.

**Disadvantages**:
- The conductor is exposed to the high-altitude environment and requires periodic inspection for wear and corrosion.
- Spacers are needed to maintain the gap between the conductor and tethering cable (adding approximately 80 kg).
- Extremely high peak currents (>200 kA) may cause ablation of the conductor (life expectancy must be determined through experiments).
- **Corona discharge efficiency degradation problem in low-pressure environments** (see Section 5.3.6).

**Engineering applicability assessment**: **Recommended primary scheme**. Comprehensively optimal in terms of mass, energy consumption, reliability, and continuous working capability. The corona discharge efficiency degradation problem in low-pressure environments can be addressed by increasing pulse voltage, optimizing tip geometry, and adding leading-edge plasma auxiliary triggering.

#### 5.2.5 Selection Conclusion

| Scheme | Continuous Working Capability | Mass | Energy Consumption | Technology Readiness | Cost | Recommended |
|:---|:---:|:---:|:---:|:---:|:---:|:---:|
| Lightning Rocket | Poor (single-shot) | High (multiple rockets) | Low | High | Medium | No |
| Laser Lightning Attraction | Excellent | Extremely high (>1,000 kg) | Extremely high (>10 kW) | Extremely low | Extremely high | Long-term alternative |
| Leading-Edge Plasma Jet | Medium (limited attempts) | Medium (+50–100 kg) | Medium | Low | Medium | Optional auxiliary |
| Fixed Conductor + Active Pulse | Excellent | Low (<400 kg) | Medium (<5 kW peak) | Medium | Medium | **Yes** |

**Selection for this volume**: **CNT braided cable fixed conductor + active high-voltage pulse triggering** as the primary scheme. Leading-edge plasma jets serve as an optional auxiliary enhancement (enabled when electric field intensity is insufficient); this volume reserves installation interfaces (compressed gas piping and nozzle positions). In the long term, if laser lightning attraction technology achieves breakthroughs (system mass <200 kg, power consumption <2 kW, plasma channel length >500 m), it can serve as an upgrade replacement; this volume reserves an optical path channel.


### 5.3 Leading-Edge Trigger Lightning Attraction Device Design

#### 5.3.1 Physical Principles and Engineering Necessity of Lightning Attraction

Natural lightning typically originates from locally intensified electric fields between the charge region at the base of the thundercloud and protruding objects on the ground. When the electric field intensity exceeds the air breakdown threshold (approximately $3 \times 10^6 \text{ V/m}$ at sea level, decaying exponentially with altitude), an **upward leading edge** is generated from the protruding object on the ground. If the upward leading edge connects with the downward leading edge from the thundercloud in the air, a lightning discharge channel is formed.

The stratospheric platform is at an altitude of 20–50 km; the lightning attraction conductor suspended below it is one of the most prominent conductive structures across the entire altitude range. Without active protective measures, the platform may still be struck by lightning, but through active lightning attraction, lightning can be guided along a dedicated path to protect the platform body and tethering cable.

The basic engineering principle of lightning attraction is to **artificially create a lower breakdown threshold than the protected object**:
- The tip radius of the lightning attraction conductor is extremely small (≤1 mm), generating higher tip electric field intensity under the same ambient electric field.
- High-voltage pulses can be actively applied to the lightning attraction conductor to actively trigger initial streamers before the thundercloud electric field reaches the natural breakdown threshold.

#### 5.3.2 Lightning Attraction Conductor Material Selection

The lightning attraction conductor must withstand peak lightning currents of up to hundreds of thousands of amperes (typical values 20–200 kA, duration tens of microseconds to milliseconds) during a lightning strike, as well as high-altitude low temperatures, intense ultraviolet radiation, and ozone erosion.

| Material | Conductivity (% IACS) | Density (g/cm³) | Melting Point (°C) | Tensile Strength (MPa) | Applicability Assessment |
|:---|:---:|:---:|:---:|:---:|:---|
| Copper | 100 | 8.96 | 1,084 | 200–400 | Excellent conductivity, but high density, large mass penalty at high altitude |
| Aluminum | 61 | 2.70 | 660 | 70–200 | Lightweight, but low melting point, prone to ablation at high temperatures |
| Copper-clad steel | 30–40 | 7.80 | 1,500 (steel core) | 400–1,200 | High strength, high-temperature resistant, acceptable conductivity |
| CNT braided cable | ~100 (theoretical) | 1.3–1.5 | >3,000 (inert) | 500–2,000 | **Recommended** — extremely light, high-temperature resistant, high-strength, corrosion-resistant |
| Nickel-base alloy (Inconel) | 15–25 | 8.20 | 1,350–1,400 | 600–1,100 | High-temperature and corrosion-resistant, but high density and lower conductivity |

**Selection for this volume**: **CNT braided cable** as the primary lightning attraction conductor material (diameter ≥6 mm, cross-section area ≥28 mm²), supplemented by **copper-clad steel** as the connecting conductor in the ground section and dissipation network. CNT cables have the following irreplaceable advantages:
- Density is only about 1/6 that of copper; mass reduced by about 80% for the same current-carrying capacity.
- High-temperature resistant (can withstand >3,000°C in inert or vacuum conditions); risk of lightning current thermal ablation far lower than aluminum.
- Same material as Ring Elevator cables, consistent technical approach, facilitating manufacturing and maintenance.

**Verification Item (V5-M1)**: The temperature rise, ablation degree, and electrical performance degradation of CNT braided cable under simulated lightning current impact (peak 200 kA, waveform 8/20 μs) must be verified through ground high-voltage laboratory experiments.

#### 5.3.3 Lightning Attraction Conductor Structural Parameters

The lightning attraction conductor extends vertically downward from the aerostat bottom to approximately 1,000–2,000 m below the platform, with the tip exposed to the atmosphere. The conductor is laid parallel to the outside of the tethering cable, maintained at a fixed distance (≥0.5 m) from the tethering cable by dedicated insulating spacers.

| Parameter | Design Value | Description |
|:---|:---|:---|
| Total conductor length | 1,000–2,000 m | From the aerostat bottom to the tip, covering the altitude range most likely to trigger upward leading edges (15–35 km) |
| Conductor diameter | ≥6 mm (CNT braided cable) | Cross-section area ≥28 mm², current-carrying capacity ≥200 kA (peak) |
| Conductor outer insulation | Silicone rubber or PTFE, thickness ≥3 mm | Prevents bypass discharge between the lightning attraction conductor and non-grounded metal components |
| Tip shape | Conical, tip radius ≤1 mm | Tungsten alloy or Inconel material, high-temperature resistant, oxidation-resistant |
| Number of tips | 1 main tip + 4 auxiliary tips (umbrella arrangement) | Main tip pointing downward, auxiliary tips inclined at 60° downward, expanding the trigger range |
| Conductor-to-tethering cable spacing | ≥0.5 m | Maintained by insulating spacers, one spacer every 50 m along the conductor |
| Spacer material | Aluminum alloy + PTFE coating | Insulating, UV-resistant, low mass |

#### 5.3.4 Active Leading-Edge Trigger Strategy

Under natural conditions, an upward leading edge is generated only when the thundercloud electric field reaches the breakdown threshold. The stratospheric platform lightning attraction device adopts **active high-voltage pulse triggering** technology to actively generate initial streamers before the thundercloud electric field falls below the natural breakdown threshold, greatly improving lightning attraction success rate and controllability.

**(a) Trigger Principle**

A rapidly rising high-voltage pulse (typically positive polarity, to match the polarity of the negative charge at the base of the thundercloud) is applied to the tip of the lightning attraction conductor, generating a locally strong electric field (> $5 \times 10^6 \text{ V/m}$) around the tip, exciting initial streamers. The streamers develop upward driven by the thundercloud background electric field, forming a continuous upward leading edge that ultimately connects with the downward leading edge from the thundercloud.

**(b) Pulse Power Supply Parameters**

| Parameter | Design Value | Description |
|:---|:---|:---|
| Pulse peak voltage (current design) | 500–1,000 kV | Positive polarity, rise time ≤1 μs |
| Pulse peak voltage (long-term upgrade) | 1,500–2,000 kV | Requires breakthroughs in insulation and component voltage ratings |
| Pulse energy | ≤50 kJ/shot | Single trigger energy |
| Repetition rate | 0.5–1 Hz (intermittent triggering during warning) | Increased to 5–10 Hz as thundercloud approaches |
| Power supply type | Solid-state Marx generator or Tesla transformer | Small volume, light weight, high controllability |
| Power supply mass | ≤200 kg | Including energy storage capacitors, switches, and control circuits |
| Power supply consumption (standby) | ≤500 W | Full-power charging on standby during warning period |
| Power supply consumption (trigger instant) | Peak ≤5 MW (duration <10 μs) | Instantaneous discharge from the aerostat energy storage system |

**(c) Trigger Strategy**

| Thunderstorm Warning Level | Trigger Mode | Trigger Frequency | Description |
|:---|:---|:---:|:---|
| **Level V (Attention)** | Standby | No trigger | Monitor electric field intensity |
| **Level IV (Alert)** | Intermittent trigger | 0.5 Hz | Electric field intensity >2 kV/m, active "probing" |
| **Level III (Alarm)** | Continuous trigger | 5–10 Hz | Electric field intensity >5 kV/m, full lightning attraction |
| **Level II (Emergency)** | Continuous trigger + platform descent | 10 Hz | Thunderstorm about to pass overhead; attract lightning while lowering platform |
| **Level I (Disaster Response Phase)** | Switch to ground lightning attraction tower | — | Platform has descended and locked to ground; ground lightning attraction tower is primary, platform on standby |

**(d) Intelligent Control Requirements**

The trigger control system must autonomously determine trigger timing and pulse parameters based on real-time electric field measurement data (see Section 5.6), lightning location system (LLS) data, and platform GPS position. If communication between the platform and the ground is interrupted, the system must continue operating without ground instructions and automatically adjust the trigger mode according to preset logic.

#### 5.3.5 Lightning Attraction Conductor Tension and Wind Vibration Control

The lightning attraction conductor is 1–2 km long and exposed to strong winds in the high-altitude environment; the following engineering issues must be considered:

- **Wind-induced oscillation**: The spacing between the conductor and tethering cable is maintained by spacers; spacers must withstand the oscillation stress induced by wind loads. Spacers are designed to the spacer standards of high-voltage transmission lines: aluminum alloy frame + rubber damping elements, mass ≤2 kg each.
- **Tension control**: The lower end of the conductor (tip) hangs freely; the upper end is fixed to the insulated winch at the bottom of the aerostat. The winch is equipped with a constant tension control system (tension set at approximately 500 N) to prevent excessive oscillation of the conductor in strong winds or entanglement with the tethering cable.
- **Anti-entanglement**: Anti-entanglement rotary devices (one every 100 m) are installed between the conductor and tethering cable, allowing relative rotation but limiting entanglement angle.

#### 5.3.6 Corona Discharge Efficiency Problem in Low-Pressure Environments and Countermeasures

**(a) Problem Description**

At high altitude (20–50 km), air density is only $1/100$ to $1/1000$ of sea level. Corona discharge (including the formation of streamers and leading edges) depends on air molecular collision ionization; at low pressure, the electron mean free path increases but collision frequency decreases, causing changes in the electric field threshold required for initial streamers.

According to Paschen's Law, the breakdown voltage $U_b$ in a uniform electric field gas is related to the product of gas pressure $p$ and electrode spacing $d$:

$$
U_b = \frac{B(pd)}{\ln(pd) + C}
$$

where $B$ and $C$ are gas-related constants. At extremely low pressure (very small $pd$), the breakdown voltage actually increases. For tip-to-plane electrodes (highly non-uniform electric field), the variation of breakdown voltage with decreasing pressure is more complex, but the qualitative conclusion is: as $p$ decreases from 1 atm to the $10^{-2}$ atm level, the breakdown voltage first decreases then increases, with a minimum value. For air, the minimum breakdown voltage occurs at approximately $pd \approx 0.5-1 \text{ Pa·m}$ [6].

At 30 km altitude ($p \approx 1.2 \times 10^3 \text{ Pa} \approx 0.012 \text{ atm}$), tip radius $r = 1 \text{ mm} = 0.001 \text{ m}$, then $p \cdot d \approx 1.2 \times 10^3 \times 0.001 = 1.2 \text{ Pa·m}$, exactly close to the minimum value region of the Paschen curve. This means that at this pressure, the corona onset voltage **may be lower than at sea level**, rather than higher — because although collision frequency decreases, electrons acquire higher energy during acceleration, and ionization efficiency does not necessarily decrease. Experimental research shows that in the 0.01–0.1 atm range, the DC breakdown voltage of a tip-to-plate gap can decrease to 50%–70% of sea level values [7].

**However, successful lightning attraction not only depends on the generation of initial streamers, but also on whether the streamers can continuously develop and transform into an upward leading edge in the background electric field.** At low pressure, the ionization rate at the streamer head decreases, the resistance of the streamer channel increases, and the extension distance of streamers decreases under the same background electric field. This means the **lightning attraction radius** (the distance within which the lightning attraction conductor can effectively "capture" the downward leading edge from the thundercloud) may be significantly reduced.

**(b) Qualitative Estimation of Lightning Attraction Radius and Verification Requirements**

The lightning attraction radius $R_p$ is related to the streamer length $L_s$ generated at the conductor tip and the thundercloud base electric field intensity $E_c$. Under ideal conditions, the streamer length can be roughly estimated as:

$$
L_s \sim \frac{U_{\text{tip}}}{E_c}
$$

where $U_{\text{tip}}$ is the tip potential (pulse voltage plus background electric field contribution), and $E_c$ is the critical electric field required to maintain streamer propagation (approximately $5 \times 10^5 \text{ V/m}$ at sea level, possibly higher at low pressure). This formula is only a dimensional approximation and does not account for streamer development dynamics, background electric field gradients, space charge screening, or other key factors. Therefore, **the precise values of streamer length and lightning attraction radius must be determined through low-pressure discharge experiments (Verification Item V5-M6) and numerical simulations (e.g., fluid-PIC models)**. As a design reference, at simulated 30 km pressure, with a pulse voltage of 1,000 kV, streamer length is expected to reach the order of hundreds of meters; actual values must be experimentally calibrated.

**(c) Countermeasures**

1. **Increase pulse voltage**: Raising the pulse peak voltage from 500–1,000 kV to 1,500–2,000 kV can compensate for streamer length loss. **However, ultra-high voltage pulses on the aerostat platform present a major engineering challenge for insulation and packaging**. The current design uses 1,000 kV as the baseline; 1,500–2,000 kV is a long-term upgrade option, to be implemented after breakthroughs in insulation materials, creepage distances, and component voltage ratings.
2. **Optimize tip geometry**: Use an umbrella arrangement of multiple tips (5 tips), leveraging the electric field superposition effect between tips to enhance local ionization.
3. **Leading-edge plasma auxiliary injection**: Simultaneously with pulse triggering, inject a brief plasma burst (using argon or helium) to pre-establish a locally ionized channel in front of the tip, lowering the electric field threshold for streamer initiation. This scheme serves as an optional enhancement.
4. **Combined with ground lightning attraction towers**: When the platform descends to near the ground (altitude ≤500 m), the ground lightning attraction towers (see Main Volume 7, Section 7.6.1 and Section 5.6.4 of this volume) have significantly larger lightning attraction radii (due to higher air density and lower breakdown threshold) and can take over the platform's lightning attraction function.

**(d) Verification Requirements**

The above analysis is a theoretical estimate; it must be verified through **low-pressure discharge experiments** (simulating 20–50 km altitude) to determine actual streamer lengths and lightning attraction radii. This has been included in Verification Item V5-M6.


### 5.4 Lightning Current Conduction and Ground Dissipation Network

#### 5.4.1 Current Path Design

When a lightning strike occurs, the lightning current (peak up to 200 kA) at the upper end of the lightning attraction conductor must be conducted into the ground safely with low impedance.

**Current path**: Lightning attraction conductor tip (struck) → lightning attraction conductor → insulated winch at aerostat bottom → embedded lightning attraction conductor in tethering cable → ground anchoring station → dissipation network → ground.

**(a) Internal Transition Section of the Aerostat**

After the lightning attraction conductor enters from the bottom of the aerostat, it passes through dedicated **penetrating insulating bushings** to enter the embedded conductor of the tethering cable. Insulating bushings are made of ceramic or PTFE material, inner diameter ≥20 mm, external creepage distance ≥500 mm, withstanding lightning impulse voltage ≥1,500 kV. Shielding rings are installed between the bushing and the aerostat structure to prevent lightning current from bypassing to the aerostat skin.

**(b) Embedded Lightning Attraction Conductor in the Tethering Cable**

According to the design in Section 1.5 of Volume 1 of this Appendix, the tethering cable already has an embedded CNT conductive layer (cross-section area ≥32.2 mm²) as the shared conductor for power supply and communication. This conductive layer also serves as the main channel for lightning current. The lightning current enters the CNT conductive layer of the tethering cable from the aerostat through the cable entrance and travels down the cable to the ground anchoring station.

**Current-carrying capacity check**: CNT conductive layer cross-section area $A = 32.2 \text{ mm}^2 = 3.22 \times 10^{-5} \text{ m}^2$. Direct engineering data for the pulsed current density tolerance limit of CNT materials is currently lacking. Based on theoretical electrothermal coupling estimates for carbon-based materials under microsecond pulses, the current density is expected to reach the $10^9 - 10^{10} \text{ A/m}^2$ level. Using this to estimate the theoretical peak current tolerance:

$$
I_{\text{max}} = J_{\text{max}} \times A = 10^9 \times 3.22 \times 10^{-5} = 3.22 \times 10^4 \text{ A} = 32.2 \text{ kA}
$$

to $10^{10} \times 3.22 \times 10^{-5} = 3.22 \times 10^5 \text{ A} = 322 \text{ kA}$.

Typical lightning current peaks are 20–200 kA; therefore the CNT conductive layer can theoretically withstand most lightning strikes, but may approach material limits near the upper boundary (200 kA). **This check is a theoretical estimate and must be confirmed through Verification Item V5-M2 (lightning current impact experiment).**

**(c) Ground Anchoring Station Transition Section and Interface**

After the tethering cable reaches the ground, the CNT conductive layer is connected to the ground dissipation network through an insulating transition section (Section 1.5(i) of Volume 1 of this Appendix).

**Interface description when sharing anchoring with the Ring Elevator**: If the stratospheric platform is deployed at a Ring Elevator anchoring node (such as Macapá, Brazil or Port-Gentil, Gabon), the ground grounding system can be directly connected to the grounding network already built at the Ring Elevator anchoring station. In this case, the stratospheric platform does not need to independently build grounding electrodes, but must ensure that the impulse grounding resistance at the connection point meets the requirements of this volume (≤4 Ω). The grounding design of the Ring Elevator anchoring station is detailed in Main Volume 3, Section 3.3 and Main Volume 7, Section 7.6.1. This volume only requires: when sharing anchoring, the grounding terminal of the stratospheric platform lightning attraction system should be reliably connected to the Ring Elevator grounding network (connection impedance ≤0.5 Ω), with a detachable isolation switch installed at the connection point to allow independent maintenance of the platform.

If the stratospheric platform is deployed at an independent anchoring point (without Ring Elevator facilities), build a dissipation network independently as described in Section 5.4.2 below.

#### 5.4.2 Independent Ground Dissipation Network Design (Non-Shared Scenario)

The dissipation network safely spreads the energy of the lightning current into the ground, avoiding dangerous step voltages and contact voltages at the ground surface.

**(a) Grounding Resistance Target**

According to GB 50057-2010 "Code for Design of Lightning Protection of Buildings," Article 4.2.1, the impulse grounding resistance of an independent lightning protection rod should not exceed 10 Ω [1]. Since the stratospheric platform undertakes Ring Elevator maintenance and personnel rescue tasks, it is classified as an important facility; the impulse grounding resistance target is set at **≤4 Ω** (≤10 Ω in high-resistivity areas), and must be adjusted based on on-site measured data.

**(b) Grounding Electrode Configuration**

| Grounding Electrode Type | Material | Quantity | Individual Size | Burial Depth | Description |
|:---|:---|:---:|:---|:---|:---|
| Deep well grounding electrode | Copper-clad steel (copper plating thickness ≥0.25 mm) | ≥10 | Diameter ≥50 mm, length ≥50 m | Well depth ≥50 m | Utilizes deep moist layers to reduce resistance |
| Horizontal grounding grid | Copper strip (cross-section ≥50×4 mm²) | 1 set | Grid spacing ≤5 m, total area ≥10,000 m² | ≥0.8 m | Large-area grid reduces total resistance |
| Ring equalization band | Copper strip | 2 rings | Width ≥50 mm, thickness ≥4 mm | 0.5 m below ground surface | Surrounding the outer edge of the anchoring station, double-ring arrangement |
| Resistivity-reducing agent | Bentonite + graphite (conductivity ≤1 Ω·m) | — | Fill around grounding electrodes | — | Reduces contact resistance |
| Conductive concrete | Graphite content ≥5% | — | Poured in grounding trenches | — | Permanent resistance reduction |

**Grounding resistance estimation** (using Shackleton Antarctic bedrock area as an example, $\rho = 10,000 \text{ Ω·m}$):

Single deep well grounding electrode ($L = 50 \text{ m}, d = 0.05 \text{ m}$) grounding resistance formula:

$$
R_{\text{single well}} = \frac{\rho}{2\pi L} \ln\left(\frac{4L}{d}\right)
$$

where $L$ — electrode length (m), $d$ — electrode diameter (m).

Substituting values:

$$
R_{\text{single well}} = \frac{10,000}{2\pi \times 50} \ln\left(\frac{4 \times 50}{0.05}\right) = \frac{10,000}{314.16} \ln(4000) \approx 31.83 \times 8.294 \approx 264 \text{ Ω}
$$

10 deep wells in parallel (utilization factor $\eta = 0.6$):

$$
R_{\text{well group}} = \frac{264}{10 \times 0.6} \approx 44 \text{ Ω}
$$

Horizontal grid (area $S = 10,000 \text{ m}^2$) grounding resistance approximate formula:

$$
R_{\text{grid}} = \frac{\rho}{4} \sqrt{\frac{\pi}{S}} = \frac{10,000}{4} \sqrt{\frac{3.1416}{10,000}} = 2,500 \times \sqrt{0.00031416} = 2,500 \times 0.01772 \approx 44.3 \text{ Ω}
$$

Total resistance after parallel connection of well group and grid:

$$
R_{\text{total}} = \frac{1}{\frac{1}{44} + \frac{1}{44.3}} \approx 22 \text{ Ω}
$$

Adding resistivity-reducing agent, **conservative estimate** can reduce grounding resistance to about 40% of original value (multiply by 0.4):

$$
R_{\text{total}} \approx 22 \times 0.4 = 8.8 \text{ Ω}
$$

Still does not meet the 4 Ω target. The number of deep wells needs to be increased to 15 and the horizontal grid area expanded to 20,000 m², with conductive concrete backfill. **The final design must be optimized through grounding calculation software based on on-site soil resistivity measurements, targeting ≤10 Ω (high-resistivity areas) or ≤4 Ω (after enhanced measures).** The figures in this volume are order-of-magnitude estimates only and do not serve as final design values.

**(c) Equalization Grounding Grid and Step Voltage Protection**

When lightning current flows into the ground, it creates a potential gradient (step voltage) at the surface. To prevent personnel or equipment from electric shock, an equalization grounding grid must be installed around the anchoring station. Safe step voltage limit (calculated for a person weighing 50 kg, lightning current duration $t = 0.1 \text{ s}$) [1]:

$$
U_{\text{step limit}} = (50 + 0.3\rho_s) \times \frac{0.116}{\sqrt{t}}
$$

where $\rho_s$ is the surface layer resistivity ($\text{Ω·m}$). For crushed stone or concrete ground ($\rho_s \approx 3,000 \text{ Ω·m}$):

$$
U_{\text{step limit}} = (50 + 0.3 \times 3,000) \times \frac{0.116}{\sqrt{0.1}} = (50 + 900) \times 0.367 \approx 950 \times 0.367 \approx 349 \text{ V}
$$

Design requires ground potential gradient ≤200 V/m (1 m step length), with sufficient safety margin.


### 5.5 Platform Self Lightning Protection

The stratospheric platform itself (aerostat envelope, gondola, electronic equipment) may be subject to bypass induction and ground potential backfire from the lightning current when the lightning attraction device is in operation. The following protective measures must be taken:

#### 5.5.1 Structural Lightning Protection

| Protected Object | Measure | Description |
|:---|:---|:---|
| Aerostat skin | Apply conductive grid on the outer layer of the skin (copper mesh or aluminum mesh, grid spacing ≤5 m), grounded | Guides lightning current to the lightning attraction conductor, prevents charge accumulation and electrostatic discharge |
| Gondola shell | Aluminum alloy shell reliably connected to grounding system (grounding impedance ≤1 Ω) | Forms a Faraday cage to protect internal electronic equipment |
| Tethering cable connectors | Surge protection devices (SPD, Class I test, $I_n \geq 20 \text{ kA}$) installed at all connectors | Prevents lightning current from entering the platform interior along the cable |
| Skylight lifting system | Metal tracks, gears, and hoist housings all connected to grounding system | Prevents potential backfire |

#### 5.5.2 Electronic Equipment Surge Protection

Communication equipment (Ka/Ku antennas, fiber optic interfaces), navigation equipment (GPS/inertial navigation), control systems, and scientific instruments carried on the stratospheric platform must be equipped with tiered surge protection:

| Protection Level | Installation Location | SPD Type | Nominal Discharge Current $I_n$ | Voltage Protection Level $U_p$ |
|:---|:---|:---|:---:|:---:|
| Level 1 | Power inlet (tethering cable connection point) | 10/350 μs waveform switching type | ≥20 kA | ≤2.5 kV |
| Level 2 | Distribution panel inlet | 8/20 μs waveform voltage-limiting type | ≥10 kA | ≤1.5 kV |
| Level 3 | Terminal equipment power socket | 8/20 μs waveform | ≥5 kA | ≤0.8 kV |

Signal lines (antenna feedlines, fiber optic interfaces, sensor signal lines) must be equipped with dedicated signal SPDs, insertion loss ≤0.5 dB, response time ≤1 ns.

#### 5.5.3 Lightning Electromagnetic Pulse Protection

Transient electromagnetic fields generated by lightning strikes will induce high voltages in cable loops, antenna feedlines, and unshielded electronic modules inside the platform, potentially causing logic errors, data corruption, or even hardware burnout. The following supplementary measures must be taken:

| Protective Measure | Description |
|:---|:---|
| **Cable shielding and grounding** | All signal lines and power lines entering the gondola use double-shielded cables (braided mesh + aluminum foil), shields grounded at both ends. Shield grounding impedance ≤0.1 Ω/m |
| **Rational wiring** | Power lines and signal lines routed in separate conduits, spacing ≥100 mm. Avoid forming large loop areas (loop area ≤0.05 m²) |
| **Isolation transformers** | Use isolation transformers (1:1, bandwidth ≥1 MHz) for critical analog signals (e.g., electric field meter output) to block common-mode interference |
| **Fiber optic isolation** | Control buses and communication buses preferentially use fiber optics (embedded fiber in tethering cable satisfies this requirement), completely isolating electrical coupling |
| **Transient suppressor arrays** | Install transient voltage suppressors (TVS, breakdown voltage slightly above signal level) between each pin of multi-pin connectors and ground, response time ≤1 ns |
| **Cabinet shielding** | Electronic equipment cabinets use conductive gaskets (beryllium copper or conductive rubber), ensuring shielding effectiveness at seams ≥60 dB (10 kHz–1 GHz) |

**Verification requirement**: Lightning electromagnetic pulse protection effectiveness must be verified through laboratory pulse injection tests (Verification Item V5-M7).

#### 5.5.4 Personnel Safety

Safety protection for personnel working on the stratospheric platform (including maintenance staff in the gondola) during thunderstorm warnings:

- **Personnel evacuation**: When thunderstorm warning reaches Level III (Alarm), all personnel evacuate to the shielded shelter at the ground anchoring station.
- **Equipotential bonding**: Grounding terminals are installed inside the gondola and aerostat; EVA personnel connect to the shell through grounding wrist straps (resistance ≤1 MΩ) for equipotential connection, preventing electrostatic accumulation.
- **Insulating shoes and gloves**: All personnel approaching the lightning attraction conductor or grounding system during thunderstorm conditions must wear insulating shoes (withstand voltage ≥15 kV) and insulating gloves (withstand voltage ≥10 kV).


### 5.6 Thunderstorm Warning and Safe Descent Procedure

#### 5.6.1 Multi-Source Warning System

Lightning warning uses a **ground-based + satellite-borne + platform in-situ** three-tier detection network to achieve advance identification, tracking, and intensity assessment of thunderstorms.

**(a) Ground-Based Lightning Location System (LLS)**

Within 100 km of the stratospheric platform anchoring point, deploy a high-precision lightning location network (VLF/LF band, detection efficiency ≥90%, positioning accuracy ≤500 m). LLS data is transmitted in real-time to the control center; after processing, it can predict the movement path and intensity of thunderstorms within 30–60 minutes.

**(b) Satellite-Borne Lightning Imager**

Utilize lightning imagers carried by geostationary meteorological satellites (such as Fengyun-4 and GOES-R) to obtain full-disk lightning distribution maps with temporal resolution ≤2 ms and spatial resolution ≤10 km. Data is used for initial thunderstorm identification and long-range warning (1–3 hours in advance).

**(c) Platform In-Situ Electric Field Monitoring**

The aerostat carries an **Electric field change Meter (EDM)** and an **atmospheric electric field meter**, monitoring the ambient electric field intensity at the platform altitude (25–35 km) in real time. The rate of change of electric field intensity is the most direct indicator of thunderstorm approach.

| Electric Field Intensity ($E$) | Hazard Level | Warning Color | Response Action |
|:---|:---|:---|:---|
| $E < 1 \text{ kV/m}$ | Safe | Green | Normal operations |
| $1 \text{ kV/m} \leq E < 2 \text{ kV/m}$ | Level V (Attention) | Yellow | Initiate intensive LLS data analysis |
| $2 \text{ kV/m} \leq E < 5 \text{ kV/m}$ | Level IV (Alert) | Orange | Platform begins intermittent lightning attraction triggering, notify ground to prepare |
| $5 \text{ kV/m} \leq E < 10 \text{ kV/m}$ | Level III (Alarm) | Red | Continuous lightning attraction triggering, personnel evacuate platform, initiate descent procedure |
| $E \geq 10 \text{ kV/m}$ | Level II (Emergency) | Dark red | Platform emergency descent, lightning attraction system at full power continuous operation, ground lightning attraction towers (if available) activated |
| **Platform has descended to ground and locked, and ground lightning attraction tower is available** | **Level I (Disaster Response Phase)** | **Black** | **Lightning attraction primary control switches to ground lightning attraction tower; platform lightning attraction system enters low-power standby (backup); if ground lightning attraction tower unavailable, platform lightning attraction system continues full-power operation** |

> **Note**: Level I is no longer triggered solely by electric field intensity; instead, "platform has descended to ground and locked" serves as the marker, representing the transfer of lightning protection from the platform to ground facilities. Under any circumstances, lightning protection must not be interrupted.

#### 5.6.2 Safe Descent Procedure

**(a) Physical Necessity of Descent**

The core physical reasons for descent (lowering the stratospheric platform from the 25–35 km residing altitude to near the ground) are three:

1. **Reducing the effective length of the lightning attraction conductor**: In a thunderstorm electric field, the probability of triggering an upward leading edge is positively correlated with the length of the lightning attraction conductor. After descent, the conductor length shortens, reducing the probability of lightning "capture," while the lightning current path shortens, making energy dissipation more controllable.
2. **Utilizing the protection of ground lightning attraction towers**: When the platform altitude is ≤500 m, the ability of ground lightning attraction towers (50–100 m high) to trigger upward leading edges is far stronger than the platform (due to higher air density at low altitude and lower breakdown threshold), directing lightning preferentially to the ground tower, achieving a "relay" style protection. The platform itself no longer serves as the primary lightning attractor, but the lightning attraction system remains on standby.
3. **Reducing the risk of direct lightning damage**: High-altitude thundercloud discharge typically has larger current amplitudes and steeper wavefronts than low-altitude ground lightning. After descent, even if lightning strikes, the lightning current enters the ground along a shorter lightning attraction conductor (hundreds of meters rather than kilometers), significantly reducing the electromagnetic coupling effect on the tethering cable and aerostat structure.

**(b) Descent Operating Procedure**

1. **Command confirmation**: After the warning system issues a Level III alarm, the control system automatically sends a descent request to the ground control center; if no rejection command is received within 30 seconds, descent is automatically executed.
2. **Auxiliary envelope venting**: The vent valves of the aerostat's auxiliary envelope (air) open, reducing buoyancy.
3. **Winch cable retrieval**: Ground winches reel in the tethering cable at speed ≤5 m/s (safe speed), while the constant-tension winch of the lightning attraction conductor synchronously reels in the cable.
4. **Altitude feedback**: Altitude and electric field intensity are monitored in real-time during descent; if electric field intensity drops below the safe threshold (<2 kV/m), descent can be paused.
5. **Anchoring lock**: After the aerostat reaches the ground anchoring station, the mechanical locking device secures the platform to the tethering tower.
6. **Lightning attraction switching**: The control system determines the status of the ground lightning attraction tower:
   - If the ground lightning attraction tower is available (built and grounding resistance meets specifications), the primary lightning attraction control switches to the ground tower; the platform lightning attraction system enters low-power standby (maintaining monitoring and communication, ready to take over at any time).
   - If the ground lightning attraction tower is unavailable (not built or malfunctioning), the platform lightning attraction system **continues full-power operation** as the last line of defense to protect the Ring Elevator cables.

**(c) Descent Time Estimation**

Residing altitude $h = 30 \text{ km}$, descent speed $v = 5 \text{ m/s}$ (safe upper limit):

$$
t_{\text{descent}} = \frac{h}{v} = \frac{30,000}{5} = 6,000 \text{ s} \approx 100 \text{ min} \approx 1.67 \text{ h}
$$

With higher speed $v = 10 \text{ m/s}$ emergency descent:

$$
t_{\text{emergency}} = \frac{30,000}{10} = 3,000 \text{ s} = 50 \text{ min}
$$

Vertical acceleration felt by persons at 10 m/s descent speed:

$$
a = \frac{\Delta v}{\Delta t} \approx 0 \text{ (constant-speed descent)}, \text{ start/brake acceleration} \leq 0.5 \text{ m/s}^2 \ll 1.05g_0
$$

Safety requirements met.

**(d) Lightning Attraction Strategy During and After Descent**

| Phase | Altitude | Primary Lightning Attractor | Lightning Attraction System Status | Description |
|:---|:---|:---|:---|:---|
| Before descent | >5 km | Stratospheric platform | Continuous trigger (5–10 Hz) | Active lightning attraction, protecting platform and cables |
| During descent | 500 m – 5 km | Stratospheric platform + ground lightning attraction tower (if available) | Dual systems operating simultaneously | Handover transition phase |
| After descent (ground tower available) | ≤500 m | Ground lightning attraction tower | Platform switches to standby (backup) | Ground tower is primary, platform ready to take over at any time |
| After descent (ground tower unavailable) | ≤500 m | Stratospheric platform | Platform continues full-power operation | Last line of defense, protecting Ring Elevator cables |

#### 5.6.3 Emergency Power and Communication Assurance

During descent, all critical systems of the aerostat (winches, lightning attraction power supply, electric field meter, communications) must be powered by **uninterruptible power supply (UPS)** and **emergency battery packs**. UPS capacity ≥10 kWh, supporting ≥2 h of descent operations. Communication links preferentially use fiber optics (embedded in tethering cable), with Ka/Ku satellite links as backup.

#### 5.6.4 Ground Lightning Attraction Tower Interface Parameters

When the stratospheric platform shares anchoring with the Ring Elevator, the technical parameters summary for the ground lightning attraction tower array is as follows (detailed design in Main Volume 7, Section 7.6.1):

| Parameter | Design Value | Description |
|:---|:---|:---|
| Number of lightning attraction towers | 3–4 | Arranged in a ring around the anchoring station |
| Tower height | 50–100 m | Based on the principle of exceeding any non-insulated point of the cable at low altitude (0–100 m) |
| Tower tip leading-edge tip | Tungsten alloy, radius ≤1 mm | Actively generates upward leading edge |
| Grounding resistance | ≤4 Ω (per tower) | Shared grounding network with anchoring station |
| Lightning attraction radius | Determined by Main Volume 7 | Depends on tower height, tip design, and grounding resistance |
| Coordination with platform lightning attraction system | Switching determined by control center | Automatic switching after platform descent |

The grounding terminal of the stratospheric platform lightning attraction system should be reliably connected to the Ring Elevator grounding network (connection impedance ≤0.5 Ω), with a detachable isolation switch installed at the connection point to allow independent maintenance of the platform.


### 5.7 Summary of Verification Items

| ID | Item | Verification Method | Success Criteria | Priority |
|:---:|:---|:---|:---|:---:|
| **V5-M1** | CNT lightning attraction conductor lightning current impact tolerance | Apply 8/20 μs waveform to CNT sample cable in high-voltage laboratory, peak current 20–200 kA | No significant ablation (diameter reduction ≤5%), resistance increase ≤20% | **P0** |
| **V5-M2** | CNT conductive layer lightning current-carrying capacity | Simulate embedded CNT conductor in tethering cable, apply lightning current impulse, measure temperature rise and mechanical strength degradation | Temperature rise ≤200°C at peak current 200 kA, tensile strength degradation ≤10% | **P1** |
| **V5-M3** | Ground grounding system resistance compliance verification | Use three-terminal method to measure impulse grounding resistance after on-site construction at anchoring node (non-shared scenario) | Impulse grounding resistance ≤10 Ω (≤4 Ω after enhancement) | **P1** |
| **V5-M4** | Leading-edge trigger pulse power supply high-altitude environment adaptability | Test pulse power supply discharge stability and insulation performance in simulated high-altitude low-temperature (-60°C) and low-pressure (0.01 atm) environment | 100 consecutive triggers without failure, pulse peak voltage variation ≤±10% | **P2** |
| **V5-M5** | Full system linkage test of descent procedure | Simulate Ⅲ-level warning triggering full descent process on ground simulation or actual tethered balloon | Time from warning to locking ≤2 h, systems coordinated without conflict | **P2** |
| **V5-M6** | Streamer length and lightning attraction radius verification at low pressure | Apply pulsed high voltage to tip-to-plate gap in low-pressure discharge chamber (0.01–0.1 atm), measure streamer length and breakdown voltage | Experimentally determine streamer length; design target ≥500 m @1,000 kV (design parameters may be revised based on test results) | **P2** |
| **V5-M7** | Lightning electromagnetic pulse protection effectiveness verification | Conduct pulse injection test on platform electronics cabinets (waveform 1.2/50 μs, voltage level per IEC 61000-4-5) | Equipment undamaged, bit error rate ≤10⁻⁶ | **P2** |


### 5.8 Equipment List and Mass Estimates

| Equipment | Quantity | Unit Mass | Subtotal | Description |
|:---|:---:|:---:|:---:|:---|
| Lightning attraction conductor (CNT braided cable, including insulation) | 1 (2,000 m) | ~12 kg (6 mm diameter, density 1.5 g/cm³) | ≤15 kg | Conductor body |
| Lightning attraction conductor constant-tension winch | 1 | ≤50 kg | ≤50 kg | Including insulating pulleys and tension sensors |
| High-voltage pulse power supply (solid-state Marx) | 1 set | ≤200 kg | ≤200 kg | Including energy storage capacitors, switches, control circuits |
| Lightning attraction tips (tungsten alloy) | 1 set | ≤2 kg | ≤2 kg | Main tip + 4 auxiliary tips |
| Insulating spacers (one every 50 m) | 40 | ≤2 kg each | ≤80 kg | Aluminum alloy + PTFE |
| Electric field change meter (EDM) | 2 | ≤5 kg each | ≤10 kg | Redundant configuration |
| Atmospheric electric field meter | 2 | ≤3 kg each | ≤6 kg | Redundant configuration |
| Lightning location system (LLS) receiver | 1 set (ground station) | ≤50 kg | ≤50 kg | Deployed at anchoring station |
| Surge protection devices (SPD) | 1 set | ≤30 kg | ≤30 kg | Including power and signal SPDs |
| Leading-edge plasma jet device (optional) | 1 set | ≤50 kg | ≤50 kg | Including gas cylinders, nozzles, trigger circuits (optional installation) |
| Ground grounding materials (non-shared scenario) | 1 set | — | ≤2,000 kg | Only needed for independent anchoring, launch/transport required |
| **Total (aerostat-carried portion, excluding optional)** | — | — | **≤363 kg** | — |
| **Total (including optional enhancement)** | — | — | **≤413 kg** | — |

> Note: If the stratospheric platform shares anchoring with the Ring Elevator, the ground grounding materials (approximately 2 tons) are not launched with the platform; they are built as part of the Ring Elevator project. The platform only needs to provide a grounding connection interface.


### 5.9 Parameter Output

| Parameter | Value | Status | Receiving Volume |
|:---|:---|:---|:---|
| Lightning attraction scheme | CNT fixed conductor + active high-voltage pulse triggering | Design baseline | — |
| Lightning attraction conductor material | CNT braided cable (diameter ≥6 mm) | Design baseline | — |
| Lightning attraction conductor length | 1,000–2,000 m | Design baseline | Volume 8 (Deployment) |
| Pulse trigger voltage (current design) | 500–1,000 kV | Design baseline | — |
| Pulse trigger voltage (long-term upgrade) | 1,500–2,000 kV | Long-term option | — |
| Pulse power supply mass | ≤200 kg (basic) | Order-of-magnitude estimate | Volume 9 (Economics) |
| Lightning attraction system total mass (platform-carried) | ≤363 kg (basic) / ≤413 kg (with plasma auxiliary) | Order-of-magnitude estimate | Volume 8 (Deployment) |
| Ground grounding resistance target (independent anchoring) | ≤10 Ω (high-resistivity area, ≤4 Ω after enhancement) | **P1 pending verification** | — |
| Warning electric field threshold (Level III alarm) | 5 kV/m | Design baseline | — |
| Descent speed (safe mode) | ≤5 m/s | Design baseline | Volume 1 |
| Descent speed (emergency mode) | ≤10 m/s | Design baseline | Volume 1 |
| Total descent time (30 km) | 50–100 min | Estimate | — |
| Streamer length at low pressure (30 km simulation) | Pending experimental determination (design target ≥500 m @1,000 kV) | **P2 pending verification** | — |
| Laser lightning attraction / plasma jet long-term backup trigger conditions | System mass <200 kg, power consumption <2 kW, channel length >500 m | Design principle | — |
| Ground lightning attraction tower height | 50–100 m (when sharing with Ring Elevator) | Interface parameter | Main Volume 7 |


### 5.10 Volume 5 Conclusion

This volume completes the full design of the stratospheric platform lightning attraction and protection subsystem. Core contributions:

1. **Completed the comparison of four lightning attraction schemes**; fixed conductor + active pulse triggering is comprehensively optimal.
2. **Directly confronted and analyzed the corona discharge efficiency problem in low-pressure environments**, presented theoretical estimates and experimental verification requirements (V5-M6), and proposed countermeasures (increasing pulse voltage, multiple tips, plasma assist, etc.), with 1,500–2,000 kV clearly identified as a long-term upgrade option.
3. **Established CNT braided cable as the preferred lightning attraction conductor material**, lightweight, high-strength, and high-temperature resistant.
4. **Designed the active high-voltage pulse leading-edge trigger strategy** with tiered trigger logic.
5. **Planned the lightning current conduction path**, clarified interface requirements for shared anchoring with the Ring Elevator, with strict grounding resistance targets (≤4 Ω) and conservative resistance reduction factors.
6. **Established a three-tier warning and automatic descent procedure**, clarified the physical necessity of descent, corrected the Level I warning logic (switching of primary lightning attraction rather than shutdown), and supplemented ground lightning attraction tower interface parameters.
7. **Lightning electromagnetic pulse protection section**, supplemented shielding, isolation, TVS array, and other measures.
8. **Quantified equipment mass**; impact on overall platform design is controllable (<400 kg).

All key parameters in this volume have been given verification paths and interfaced with the P0/P1/P2 system of Main Volume 7. It is recommended to prioritize completion of V5-M1, V5-M2, and V5-M6 experimental verifications before engineering implementation.


### References

[1] Standardization Administration of China. *GB 50057-2010 Code for Design of Lightning Protection of Buildings*. Beijing: China Planning Press, 2010.

[2] IEC. *IEC 62305: Protection against lightning*. Geneva: International Electrotechnical Commission, 2010.

[3] Rakov, V. A., & Uman, M. A. *Lightning: Physics and Effects*. Cambridge: Cambridge University Press, 2003.

[4] IEEE. *IEEE Std 998-2012: Guide for Direct Lightning Stroke Shielding of Substations*. New York: IEEE, 2012.

[5] Wang Jianguo, Liu Shanghe, et al. Research progress on artificial lightning attraction technology and its applications. *High Voltage Engineering*, 2015, 41(5): 1421-1430.

[6] Zhao Wenhua, Zhang Guixin, et al. Study on breakdown characteristics of air gaps at low pressure. *Transactions of China Electrotechnical Society*, 2008, 23(6): 1-6.

[7] Liu Quanzhen, et al. Experimental study on corona discharge characteristics in high-altitude low-pressure environments. *High Voltage Engineering*, 2012, 38(10): 2567-2573.

[8] TransAstra. "Mini Bee Capture Bag: ISS Technology Demonstration Success." Press Release, October 2025.

[9] NASA. "Kilopower/KRUSTY Project: Fission Power for Space Exploration." 2018.

[10] China Meteorological Administration. *QX/T 79-2007 Lightning Monitoring and Location System Performance Assessment*. Beijing: China Standards Press, 2007.

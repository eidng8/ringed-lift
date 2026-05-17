# Appendix II: Stratospheric Platform

## Volume X: Technical Interfaces with the Main Volume and Appendix I

**Version**: 1.2<br/>
**Date of Preparation**: June 2026<br/>
**Currency Unit**: Renminbi (RMB), symbol: ¥<br/>
**Related Main Volumes**: Main Volume III, Volume IV, Volume V, Volume VII, Volume IX, Volume X, Volume XII<br/>
**Related Appendix I**: Appendix I, Volumes III, VIII, and IX<br/>
**Prerequisite Reading**: Volumes I through IX of this Appendix


### Glossary of Abbreviations

| Abbreviation | Full Name | Notes |
|------|----------|------|
| CNT | Carbon Nanotube | Lightning conductor and tether cable material |
| DTN | Delay-Tolerant Networking | Delay-Tolerant Networking |
| ECLSS | Environmental Control and Life Support System | Environmental Control and Life Support System |
| GEO | Geostationary Earth Orbit | Geostationary Earth Orbit |
| GNSS | Global Navigation Satellite System | Global Navigation Satellite System |
| HAPS | High Altitude Pseudo-Satellite | The internationally accepted designation for stratospheric platforms |
| ITU | International Telecommunication Union | International Telecommunication Union |
| LLS | Lightning Location System | Lightning Location System |
| MLI | Multi-Layer Insulation | Used for passive thermal control of equipment bays |
| UNORE | United Nations Orbital Ring Elevator | United Nations Orbital Ring Elevator |


### 10.1 Volume Preamble

This volume is positioned as a **technical interface summary** between the stratospheric platform system and the Main Volume *Orbital Ringed-Elevator Project* and Appendix I *Lunar Industry*, focused on answering the following core questions:

> How does the stratospheric platform interface mechanically, electrically, communicationally, and operationally with the orbital ring elevator anchor stations? How does the platform's lightning interception system connect to the elevator's grounding network? How do the platform's communication devices cooperate with the elevator's DWDM fiber optic backbone network? How do the platform's navigation augmentation signals complement the elevator's GNSS differential system? How does the platform's emergency system align with the elevator's "full-crew evacuation" protocol? Are there communication or transport interfaces between the stratospheric platform and the lunar industrial base?

This volume does not elaborate on the specific design content of the Main Volume or Appendix I; it only defines interface parameters and coordination rules. For detailed design, please refer to the corresponding sections of each volume.

This volume builds upon:
- **Volumes I through IX of this Appendix**: All technical parameters of the stratospheric platform have been defined.
- **Main Volume volumes**: Technical parameters and interface requirements of the orbital ring elevator have been defined.
- **Appendix I volumes**: Technical parameters of the lunar industry system have been defined.

Core tasks of this volume:

1. Summarize the interface relationships between the stratospheric platform and each Main Volume, clarifying interface parameters for mechanical, electrical, communication, and operational coordination aspects.
2. Summarize the interface relationships between the stratospheric platform and Appendix I (Lunar Industry).
3. Output the consolidated interface parameter table for reference in subsequent engineering implementation.


### 10.2 Interface with Main Volume III (Node Site Selection and Anchoring Engineering)

The stratospheric platform can be deployed at the orbital ring elevator's anchor nodes (Macapá, Brazil; Port-Gentil, Gabon; Manta, Ecuador; Christmas Island (Kiritimati), Kiribati; Belitung, Indonesia; Indian Ocean deep-sea floating platform), sharing ground anchor facilities.

| Interface Item | Stratospheric Platform Side Requirements | Elevator Anchor Station Side Requirements | Source (This Volume) | Source (Main Volume) |
|:---|:---|:---|:---|:---|
| **Mechanical Interface** | Tether cable connects to ground winch via diverter pulley at top of anchor tower. Winch is independent from the elevator anchor system; shares anchor tower structure | Anchor tower top pre-fitted with diverter pulley mounting point (load capacity ≥50 kN). Anchor tower foundation load capacity ≥20 tons | Section 8.2.2 of Volume VIII | Section 3.5.2 of Main Volume III |
| **Electrical Interface (Grounding)** | Lightning interception system grounding terminal connects to elevator grounding network; connection impedance ≤0.5 Ω; fitted with removable isolation switch | Grounding network pre-fitted with connection point; impulse grounding resistance ≤4 Ω (≤10 Ω in high-resistivity areas) | Section 5.4.1 of Volume V | Section 7.6.1 of Main Volume VII |
| **Safety Isolation** | Physical isolation between platform and elevator anchor system (firewall, safety distance ≥10 m) | Anchor station design reserves independent equipment room for stratospheric platform | Section 8.2.2 of Volume VIII | Section 3.3 of Main Volume III |
| **Shared Maintenance Facilities** | Shares repair workshops, spare parts warehouse, and personnel living quarters at elevator anchor station | Anchor station reserves maintenance area for stratospheric platform | Section 8.2.2 of Volume VIII | Section 3.5.2 of Main Volume III |
| **Investment Sharing** | Stratospheric platform bears 20%–30% of shared ground facilities investment (recommended ratio) | Elevator project CAPEX reserves budget for coordination interfaces | Section 9.8 of Volume IX | Main Volume X (Economic Model) |

> **Note**: The stratospheric platform tether cable tension (≤50 kN) is far less than the elevator cable tension (≥1.57×10⁹ N); therefore winches must be independently designed and must not be shared.


### 10.3 Interface with Main Volume IV (Elevator Cable and Track Sleeve)

When the stratospheric platform's work gondola performs inspection and maintenance tasks on the elevator cable, its rack-and-pinion drive system must be compatible with the rack parameters of the elevator track sleeve.

| Interface Item | Stratospheric Platform Gondola Side Requirements | Elevator Track Sleeve Side Requirements | Source (This Volume) | Source (Main Volume) |
|:---|:---|:---|:---|:---|
| **Rack Module** | Gear module 20 mm, meshing with elevator rack | Rack module 20 mm, pressure angle 20°, tooth width 300 mm | Section 3.4 of Volume III | Section 4.13 of Main Volume IV |
| **Gear Material** | Aluminum alloy 7075-T6 + micro-arc oxidation (≥HV1000) | Rack of the same material | Section 3.4 of Volume III | Section 4.13 of Main Volume IV |
| **Track Sleeve Outer Diameter** | Gondola clamping mechanism adapts to ø0.552 m outer diameter | Track sleeve outer diameter ø0.552 m (including UHMWPE outer layer) | Section 3.4 of Volume III | Section 4.8 of Main Volume IV |
| **Power from Conducting Rail** | Gondola draws power from the middle aluminum alloy conducting rail of the track sleeve. Recommended voltage level 50 kV AC (compatible with elevator conducting rail scheme); gondola side equipped with step-down transformer to gondola operating voltage (e.g., 400 V AC) | The middle aluminum alloy layer of the track sleeve can serve as a conducting rail (requires insulation segmentation) | Section 3.4 of Volume III | Section 4.11 of Main Volume IV |
| **Operational Safety** | Gondola maintains safe distance from elevator car during operation, coordinated by the elevator dispatch system. Warning distance ≥10 km; control center calculates minimum safe distance based on real-time speeds of both, and automatically dispatches evasion | Elevator control center provides real-time position and speed of elevator cars | Section 3.4 of Volume III | — |

> **Note**: The stratospheric platform gondola only operates in the atmospheric segment (0–100 km) and does not enter the mid-high altitude segment. Its operating range partially overlaps with the elevator car's range, requiring coordinated scheduling.


### 10.4 Interface with Main Volume V (Elevator Climber/Car)

The stratospheric platform gondola and the elevator car are functionally complementary (inspection vs. transportation) and must coordinate evasion during operation.

| Interface Item | Stratospheric Platform Gondola Side Requirements | Elevator Car Side Requirements | Source (This Volume) | Source (Main Volume) |
|:---|:---|:---|:---|:---|
| **Operating Range Coordination** | Gondola reports real-time position and speed to elevator control center during operation; upon receiving approaching car warning, actively evades to nearest maintenance station | Elevator control center provides real-time car position; issues warning when distance between car and gondola is <10 km (including relative speed information) | Section 3.4 of Volume III | Main Volume V (Operation Scheduling) |
| **Emergency Rescue Coordination** | Gondola can serve as rescue platform for trapped elevator cars (docking to transfer personnel) | Car top pre-fitted with emergency hatch and docking interface (compatible with gondola docking frame) | Section 3.5 of Volume III | Section 12.4.2 of Main Volume XII |
| **Shared Escape Capsule** | Gondola's escape capsule shares technical scheme with the elevator car's "last-resort survival capsule" | Car escape capsule and gondola escape capsule use compatible interfaces | Section 3.5 of Volume III | Section 12.4.2 of Main Volume XII |
| **Communication Link** | Gondola communicates with aerostat via embedded optical fiber in tether cable; aerostat then relays communication to elevator control center | Elevator control center receives gondola data via elevator fiber optic backbone network | Section 6.7 of Volume VI | Section 9.5 of Main Volume IX |


### 10.5 Interface with Main Volume VII (Engineering Verification)

The stratospheric platform can serve as an experimental platform for the elevator project's P0-level verification items, providing real high-altitude environment test data.

| Interface Item | Capabilities Provided by the Stratospheric Platform | Elevator Verification Requirements | Source (This Volume) | Source (Main Volume) |
|:---|:---|:---|:---|:---|
| **Low-Pressure Discharge Experiment (V5-M6)** | Provides real low-pressure environment at 30 km altitude to measure streamer length and lightning interception radius | Validates lightning interception efficiency under low pressure | Section 5.3.6 of Volume V | Section 7.7 of Main Volume VII |
| **Rack Wear Validation (E-P0-1)** | Operates scaled gondola on scaled cable to measure rack wear rate | Validates 10⁷-cycle fatigue life of aluminum alloy rack | Section 4.6.1 of Volume IV | Section 7.7.1 of Main Volume VII |
| **Vacuum Radiation Cooling Validation (E-P0-2)** | Tests radiant cooling panel efficiency in real high-altitude environment | Validates 20.8 MW cooling scheme for the mid-altitude segment | Section 4.6.2 of Volume IV | Section 7.7.1 of Main Volume VII |
| **Laser Power Transmission Atmospheric Attenuation Validation** | Measures ground-to-aerostat laser transmission efficiency | Validates laser power transmission link equation | Section 4.6.4 of Volume IV | Section 7.7 of Main Volume VII |
| **Conducting Rail High-Voltage Insulation Experiment (E-P0-8)** | Tests partial discharge characteristics of UHMWPE insulation layer at 20–50 km altitude | Validates 50–100 kV insulation scheme | Section 4.6.7 of Volume IV | Section 7.7.1 of Main Volume VII |

> **Note**: Volume IV of this Appendix (Experimental R&D Platform) has already planned a scaled elevator experiment system that can deploy a 500 m scaled cable and scaled gondola, operating in the 15–35 km altitude range, providing the only obtainable real-environment data for the elevator P0-level validation.


### 10.6 Interface with Main Volume IX (Energy and Communication Infrastructure)

The stratospheric platform and the elevator's energy and communication systems have a coordination and complementary relationship.

| Interface Item | Stratospheric Platform Side Requirements | Elevator Side Requirements | Source (This Volume) | Source (Main Volume) |
|:---|:---|:---|:---|:---|
| **Frequency Coordination** | Stratospheric platform Ka-band uplink 29–31 GHz, downlink 19–21 GHz; no conflict with elevator ground-communication frequencies. Pending ITU coordination (stratospheric platform operator responsible for submitting frequency coordination data; elevator engineering party assists by providing GEO node frequency usage information) | When elevator GEO nodes use the same frequency band, time-division or code-division multiplexing is required | Section 6.4.3 of Volume VI | Section 9.5 of Main Volume IX |
| **Navigation Augmentation Complementarity** | Stratospheric platform broadcasts L1/L2/L5 differential signals, covering the low-altitude region (0–50 km) | Elevator GEO nodes provide global wide-area differential; stratospheric platform serves as low-altitude supplement | Section 6.6.2 of Volume VI | Section 9.6.2 of Main Volume IX |
| **Communication Relay Complementarity** | Stratospheric platform serves as relay node for gondola video return to elevator | Elevator control center receives gondola data forwarded by the stratospheric platform | Section 6.7 of Volume VI | Section 9.5 of Main Volume IX |
| **Emergency Communication Coordination** | When elevator communication is interrupted, the stratospheric platform can serve as a temporary relay | Elevator GEO nodes have the capability to communicate with the stratospheric platform | Section 6.8 of Volume VI | Section 12.4.3 of Main Volume XII |
| **Space Solar Power Coordination** | Stratospheric platform can provide meteorological data (cloud cover prediction) for ground receiving stations of the elevator's space solar power station | — | Section 2.2 of Volume II | Section 9.2 of Main Volume IX |


### 10.7 Interface with Main Volume X (Economic Model)

The stratospheric platform's economic data serves as input for the elevator project's economic model.

| Interface Item | Stratospheric Platform Side Data | Usage in Elevator Economic Model | Source (This Volume) | Source (Main Volume) |
|:---|:---|:---|:---|:---|
| **Maintenance Service Fee** | ¥1.5–3 million/year (estimated based on 2–3 out of 6 elevator units outsourced to the stratospheric platform; actual contract amount depends on outsourcing ratio) | Included in the "External Service Procurement" item of elevator OPEX | Section 9.3.4 of Volume IX | Section 10.3 of Main Volume X |
| **Shared Anchor Investment Sharing** | Stratospheric platform bears 20%–30% of shared ground facilities investment | Corresponding reduction in elevator CAPEX | Section 9.8 of Volume IX | Section 10.2 of Main Volume X |
| **Communication Cost Savings** | Stratospheric platform provides gondola communication relay for elevator, replacing elevator's own communication system | Corresponding reduction in communication costs within elevator OPEX | Section 9.8 of Volume IX | Section 10.3 of Main Volume X |
| **Financing Channel Coordination** | Stratospheric platform and elevator share financing channels such as sovereign funds and multilateral banks | Joint financing can reduce overall financing costs | Section 9.5 of Volume IX | Section 10.4 of Main Volume X |
| **Insurance Coordination** | Stratospheric platform and elevator can be insured together to reduce rates | Joint insurance can negotiate discounts | Section 9.5.3 of Volume IX | Section 10.4 of Main Volume X |


### 10.8 Interface with Main Volume XII (Emergency, Redundancy, and Lifeline)

The stratospheric platform serves as an execution node of the elevator emergency system within the atmospheric segment.

| Interface Item | Stratospheric Platform Side Capabilities | Elevator Emergency Requirements | Source (This Volume) | Source (Main Volume) |
|:---|:---|:---|:---|:---|
| **Thunderstorm Warning and Altitude Reduction** | Platform automatically reduces altitude when electric field monitoring reaches Level III warning, while notifying elevator control center | Elevator suspends operation or reduces speed during thunderstorm warnings | Section 5.6 of Volume V | Section 7.6.1 of Main Volume VII |
| **Lightning Interception Coordination** | Stratospheric platform lightning interception system coordinates with elevator ground lightning towers; during thunderstorms, preferentially guides lightning to ground towers | Elevator ground lightning towers and stratospheric platform lightning interception system share grounding network; switching is coordinated through the control center | Section 5.6.2 of Volume V | Section 7.6.1 of Main Volume VII |
| **Elevator Car Rescue** | Stratospheric platform gondola can serve as rescue platform for trapped elevator cars, docking to transfer personnel | Car top pre-fitted with emergency hatch and docking interface | Section 3.5 of Volume III | Section 12.4.2 of Main Volume XII |
| **Emergency Communication Relay** | When elevator communication is interrupted, the stratospheric platform can serve as a temporary communication relay | Elevator GEO nodes and stratospheric platform establish backup communication links | Section 6.8 of Volume VI | Section 12.4.3 of Main Volume XII |
| **Post-Disaster Assessment** | Stratospheric platform gondola can rapidly inspect cable damage after a disaster | Elevator control center retrieves gondola inspection data | Section 3.2 of Volume III | Section 12.5 of Main Volume XII |


### 10.9 Interface with Appendix I (Lunar Industry)

The interface between the stratospheric platform and the lunar industrial base is relatively limited, focusing primarily on communication relay, scientific data forwarding, and emergency coordination.

| Interface Item | Stratospheric Platform Side Capabilities | Lunar Industry Side Requirements | Recommended Mapping Direction (for UNORE Reference) | Source (This Volume) | Source (Appendix I) |
|:---|:---|:---|:---|:---|:---|
| **Earth-Moon Communication Relay** | Stratospheric platform can serve as an atmospheric relay node in the communication link between the elevator and the lunar base (forwarded via elevator GEO nodes) | Lunar base requires a stable communication link with Earth | — | Section 6.4 of Volume VI | Section 2.6.2 of Appendix I, Volume II |
| **Scientific Data Relay** | Stratospheric platform can forward Earth atmospheric observation data (high-altitude wind fields, temperature/humidity, ozone, aerosols) to the lunar base, supporting Earth-Moon space weather research | Lunar base requires Earth atmospheric data for space weather modeling and deep-space launch window decisions | — | Section 4.2 of Volume IV | Appendix I, Volume III (Energy), Volume IV (Resource Exploration) |
| **Deep-Space Launch Meteorological Support** | Stratospheric platform provides high-altitude wind field data to support launch window decisions for lunar spacecraft | Lunar base launch windows require Earth high-altitude wind field data | — | Section 4.2 of Volume IV | Appendix I, Volume VI (Deep-Space Launch) |
| **Emergency Level Mapping** | Stratospheric platform's four-level warning system and Appendix I's six-level warning system need to establish a mapping relationship | Lunar base emergency system links with stratospheric platform warnings | Platform Level I ↔ Appendix I Level II; Level II ↔ Level IV; Level III ↔ Level VI | Section 7.3 of Volume VII | Section 8.3 of Appendix I, Volume VIII |
| **Emergency Response Coordination** | Elevator emergency system and lunar emergency system are uniformly coordinated through UNORE | Lunar base emergency system interfaces with elevator's tiered warning system | — | Section 7.3 of Volume VII | Section 8.3 of Appendix I, Volume VIII |
| **Investment Coordination** | Stratospheric platform and lunar industry share financing channels such as sovereign funds and multilateral banks | Joint financing can reduce overall costs | — | Section 9.5 of Volume IX | Section 9.5 of Appendix I, Volume IX |

> **Note**: The specific mapping relationship for emergency level mapping (which Appendix I level corresponds to Platform Level I) should be jointly formulated by experts from both parties organized by UNORE during the project advancement phase. This volume provides recommended mapping directions for reference only.


### 10.10 Consolidated Interface Parameter Table

| Interface Category | Interface Item | Stratospheric Platform Side Parameters | External System Side Parameters | Status | Responsible Party |
|:---|:---|:---|:---|:---|:---|
| **Mechanical** | Anchor tower connection | Winch independent, shares tower structure | Anchor tower pre-fitted mounting points | Defined | — |
| | Rack meshing | Module 20 mm, pressure angle 20°, tooth width 300 mm | Same as left | Defined (compatible) | — |
| | Gondola docking | Docking frame compatible with car emergency hatch | Car top pre-fitted emergency hatch | Defined | — |
| **Electrical** | Grounding connection | Connection impedance ≤0.5 Ω, isolation switch | Grounding network connection point, ≤4 Ω | Defined | — |
| | Power from conducting rail | Recommended 50 kV AC, gondola side steps down to 400 V AC | Track sleeve aluminum alloy layer insulation-segmented | Pending detailed design | Stratospheric platform party + elevator party jointly |
| **Communication** | Ka-band frequency | Uplink 29–31 GHz, downlink 19–21 GHz | Elevator GEO node same-band coordination | Pending ITU coordination | Stratospheric platform party leads; elevator party assists |
| | GNSS differential | L1/L2/L5, coverage radius 500 km | Elevator provides wide-area differential | Complementary operation | — |
| **Operational** | Gondola-car evasion | Warning distance ≥10 km, dynamic safe distance calculation | Elevator control center provides car position and speed | Defined | — |
| | Thunderstorm altitude reduction coordination | Level III warning triggers automatic altitude reduction, notifies elevator | Elevator suspends operation | Defined | — |
| **Economic** | Maintenance service fee | ¥1.5–3 million/year (estimated for 2–3 units) | Included in elevator OPEX | Estimated value | — |
| | Investment sharing | 20%–30% of shared facilities | Reserved in elevator CAPEX | Recommended ratio | — |
| **Emergency** | Elevator car rescue | Gondola docks to transfer personnel | Car emergency hatch | Defined | — |
| | Emergency communication relay | Takes over when elevator communication is interrupted | Elevator GEO node backup link | Defined | — |
| | Emergency level mapping | Four-level warning system | Appendix I six-level warning system | Pending UNORE coordination | UNORE |

> **Note**: Items marked "Pending detailed design" are to be completed jointly by the stratospheric platform engineering party and the elevator engineering party. Items marked "Pending ITU coordination" are led by the stratospheric platform operator with the elevator engineering party assisting. Items marked "Pending UNORE coordination" are to be formulated by experts from both parties organized by the United Nations Orbital Ring Elevator Organization during the project advancement phase.


### 10.11 Volume X Conclusion

This volume has completed the technical interface summary between the stratospheric platform and the Main Volume *Orbital Ringed-Elevator Project* and Appendix I *Lunar Industry*. Core conclusions:

1. **Mechanical interfaces are clearly defined**: The stratospheric platform can share anchor stations with the elevator (shared tower structure); gondola gear and elevator track sleeve rack parameters are compatible (module 20 mm); gondola docking frame is compatible with car emergency hatch.

2. **Electrical interfaces are clear**: The lightning interception system can connect to the elevator grounding network (connection impedance ≤0.5 Ω). The conducting rail power supply scheme is recommended to use 50 kV AC (compatible with elevator), with the gondola side equipped with a step-down transformer to operating voltage; pending joint detailed design.

3. **Communication frequencies require coordination**: The stratospheric platform and elevator GEO nodes share the Ka-band; ITU coordination is required (stratospheric platform operator responsible for submitting data; elevator party assists). Navigation augmentation signals and elevator wide-area differential operate in a complementary manner.

4. **Operational coordination rules are defined**: Gondola-car evasion rules (warning distance ≥10 km, dynamic safe distance calculation) and thunderstorm altitude reduction coordination (Level III warning linkage) have been clarified.

5. **Economic interfaces are quantified**: Maintenance service fee (¥1.5–3 million/year, estimated for 2–3 elevator units) and investment sharing ratio (20%–30%) are provided as estimates for use in the elevator economic model.

6. **Emergency coordination is complete**: Interfaces for elevator car rescue, emergency communication relay, and post-disaster inspection have been linked with Main Volume XII. Emergency level mapping (platform four-level vs. Appendix I six-level) has recommended mapping directions provided for UNORE reference.

7. **Lunar industry interface expanded**: Added scientific data relay interface (forwarding atmospheric observation data to lunar base); emergency level mapping directions clarified.

8. **Responsible parties clarified**: All items marked "Pending detailed design," "Pending ITU coordination," and "Pending UNORE coordination" have designated responsible parties noted, facilitating subsequent engineering progress.

All interface parameters in this volume have been consolidated in the Section 10.10 summary table and can be used directly for interface design in subsequent engineering implementation.


### References

[10.1] Main Volume III: Node Site Selection and Anchoring Engineering, 2026.

[10.2] Main Volume VII: Engineering Verification, 2026.

[10.3] ITU Radio Regulations, Article 5, 2024.

[10.4] Main Volume IX: Energy and Communication Infrastructure, 2026.

[10.5] Main Volume XII: Emergency, Redundancy, and Lifeline Engineering, 2026.

[10.6] Appendix I, Volume VIII: Emergency, Protection, and Rescue, 2026.

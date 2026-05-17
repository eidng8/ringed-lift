# Appendix 2: Stratospheric Platform

## Volume 7: Emergency, Protection and Rescue

**Version**: 1.3<br/>
**Compiled Date**: June 2026<br/>
**Currency Unit**: Chinese Yuan (RMB), Symbol: ¥<br/>
**Related Main Volume**: Main Volume 12<br/>
**Prerequisites**: Volume 1, Volume 2, Volume 3, Volume 4, Volume 5, Volume 6 of this Appendix


### Abbreviation Table

| Abbreviation | Full Name | Description |
|------|----------|------|
| ECLSS | Environmental Control and Life Support System | Environmental Control and Life Support System |
| EVA | Extravehicular Activity | Operations by personnel outside the aerostat or gondola |
| GCR | Galactic Cosmic Rays | High-energy particle radiation from outside the solar system |
| HAPS | High Altitude Pseudo-Satellite | Internationally accepted designation for stratospheric platforms |
| HEPA | High Efficiency Particulate Air Filter | High Efficiency Particulate Air Filter |
| LLS | Lightning Location System | Lightning Location System |
| MLI | Multi-Layer Insulation | Passive thermal control for emergency equipment bays |
| PLSS | Portable Life Support System | Emergency breathing apparatus |
| RHU | Radioisotope Heater Unit | Emergency thermal insulation |
| SPE | Solar Particle Event | High-energy particle stream released by solar flares |
| UPS | Uninterruptible Power Supply | Uninterruptible Power Supply |


### 7.1 Volume Preface

This volume is positioned as the **emergency protection and rescue support plan** of the stratospheric platform system, focusing on answering the following core questions:

> A stratospheric platform stationed long-term at 20–50 km altitude faces emergencies such as thunderstorms, high-altitude wind shear, tethering cable breaks, fires, depressurization, and equipment failures. How should an emergency response system covering the full risk spectrum be established? From early warning to response, from self-rescue to external rescue — how can personnel safety be ensured without the ability to rely on real-time ground support? How can basic functions be quickly restored after platform damage?

This volume builds upon:
- **Volume 1 of this Appendix (Platform Overall Design)**: The aerostat structure, tethering cable parameters, gondola design, and resident personnel scale have been established.
- **Volume 3 of this Appendix (Maintenance, Repair and Rescue)**: The rescue capability of the gondola and the escape pod scheme have been designed.
- **Volume 5 of this Appendix (Lightning Attraction and Protection)**: Active lightning protection and altitude reduction procedures have been designed.
- **Main Volume 12 (Emergency, Redundancy and Lifeline Engineering)**: A three-layer disaster prevention system framework has been provided; this volume converts it into executable engineering plans for the stratospheric platform.

Core tasks of this volume:

1. Identify emergencies and disasters faced by the stratospheric platform, and establish a risk classification system.
2. Establish response principles when multiple hazards occur simultaneously.
3. Design tiered warning procedures and response actions.
4. Develop specific emergency plans (cable breaks, fires, depressurization, thunderstorms, equipment failures, etc.), clarifying the applicable conditions for controlled descent.
5. Plan emergency supplies and equipment configuration.
6. Design emergency personnel evacuation procedures (including escape pods).
7. Establish a post-disaster assessment and recovery framework.
8. Output key parameters for use by Volume 8 (Deployment and Maintenance) and Volume 9 (Economic Model).


### 7.2 Risk Identification and Classification

#### 7.2.1 Emergency and Disaster Classification

Emergencies faced by the stratospheric platform are divided into four major categories by source:

**Category A: Natural Environmental Emergencies**

| Code | Risk Type | Description | Warning Time | Impact Scope | Severity |
|:---:|:---|:---|:---:|:---:|:---:|
| **AS** | Thunderstorm/Lightning | Thundercloud approaches platform, electric field intensity rises sharply | Minutes to hours | Entire platform | Extreme |
| **AW** | Extreme High-Altitude Wind Shear | Wind speed suddenly increases to >50 m/s or wind direction changes abruptly | Minutes (some forewarnable) | Entire platform | High |
| **AH** | Hail/Supercooled Water Droplets | High-altitude ice crystals or supercooled water droplets impact the platform | Short duration (<10 min) | Envelope, antennas | Medium |
| **AR** | Cosmic Rays/SPE | Solar particle events causing elevated radiation dose | Tens of minutes to hours | Entire platform (personnel) | Medium |

**Category B: Platform System Failures**

| Code | Category | Risk Type | Description | Warning Time | Impact Scope | Severity |
|:---:|:---|:---|:---|:---:|:---|:---:|
| **BC** | Structural Integrity | Tethering cable break | Cable breaks due to fatigue, overload, or external impact | No warning | Entire platform | Extreme |
| | | Envelope damage | Skin tearing or seam cracking leading to helium leakage | No warning to minutes | Platform buoyancy reduction | High |
| | | Gondola depressurization | Hull damage or seal failure | No warning | Personnel inside gondola | High |
| **BF** | Fire | Electrical fire/equipment overheating | Short circuit, overload, or equipment failure | Seconds (smoke detection) | Local compartment | High |
| **BP** | Power failure | Primary power loss | Photovoltaic, battery, or power distribution system failure | No warning to minutes | Entire platform | High |
| **BC** | Communication failure | Link interruption to ground/relay | Antenna, modem, or link failure | No warning | Data transmission interruption | Medium |

**Category C: Operational Accidents**

| Code | Risk Type | Description | Warning Time | Impact Scope | Severity |
|:---:|:---|:---|:---:|:---|:---:|
| **CE** | Gondola entrapment | Gondola stuck on cable, gear damage, or power interruption | No warning | Personnel inside gondola | High |
| **CF** | EVA accident | Personnel accident during high-altitude extravehicular operations | No warning | Affected personnel | High |

#### 7.2.2 Risk Level System

Risks are classified into four levels according to severity of consequences and scope of impact:

| Level | Name | Definition | Typical Scenario |
|:---:|:---|:---|:---|
| **Level Ⅰ** | **Platform-Level Catastrophe** | Threatens the lives of all platform personnel; full evacuation required | Complete tethering cable break with uncontrolled platform ascent; large-scale envelope rupture causing uncontrolled descent |
| **Level Ⅱ** | **Sector-Level Serious Accident** | Threatens personnel safety in a gondola or single functional zone | Gondola depressurization, fire, total primary power loss |
| **Level Ⅲ** | **Individual-Level Fatal Accident** | Threatens the lives of 1–2 specific personnel | EVA accident, sudden illness of personnel inside gondola |
| **Level Ⅳ** | **General Anomaly** | No direct threat to personnel or platform safety | Communication interruption, single equipment failure |


### 7.3 Tiered Warning and Response System

#### 7.3.1 Warning Level Summary Table

| Level | Name | Color Indicator | Typical Scenario | Response Action | Responding Entity |
|:---:|:---|:---|:---|:---|:---|
| **Level Ⅰ** | **Platform-Level Catastrophe** | Red + continuous audio-visual | Complete cable break with uncontrolled ascent or descent | All personnel immediately activate escape pod/parachute evacuation | All personnel + ground rescue |
| **Level Ⅱ** | **Sector-Level Serious Accident** | Orange + intermittent audio-visual | Depressurization, fire, primary power loss, envelope leakage (buoyancy reduction >20%) | Personnel in affected zone transfer or activate emergency systems; evaluate need for controlled descent | Platform Control Center + ERT |
| **Level Ⅲ** | **Individual-Level Fatal Accident** | Yellow + personal terminal push notification | EVA accident, gondola entrapment, sudden illness | Gondola rescue + medical support; controlled descent if necessary | ERT + medical team |
| **Level Ⅳ** | **General Anomaly** | Blue | Communication interruption, single equipment failure | Record, monitor, plan maintenance | Technical support team |

#### 7.3.2 Applicable Conditions for Controlled Descent

Controlled descent (the platform actively descending to the ground anchoring station by venting the secondary envelope, releasing the winch cable, etc.) applies to the following multiple situations, and is not only activated when fire or depressurization cannot be controlled:

| Applicable Scenario | Decision Basis | Altitude Reduction Priority |
|:---|:---|:---:|
| Thunderstorm warning reaching Level Ⅲ or above | Electric field intensity ≥5 kV/m, see Volume 5 | **Highest** (mandatory) |
| Gondola entrapment cannot be resolved within 2 hours | Affects personnel safety and Ring Elevator maintenance tasks | High |
| Primary power failure with estimated repair time >4 hours | Cannot maintain long-term station-keeping | High |
| Minor envelope leakage (buoyancy reduction >20%) | Station-keeping altitude cannot be maintained | High |
| Communication interruption >24 hours and cannot be restored | Loss of ground monitoring and commands | Medium |
| Personnel with acute severe illness requiring ground medical care | Ground medical conditions superior to platform | Medium |
| Equipment failure causing loss of critical functions (e.g., ECLSS capacity reduction) | Affects personnel survival | High |
| Single tethering cable break but platform still controllable | Structural redundancy reduced; descent for inspection required | High |
| Routine rotation or planned maintenance | Non-urgent, execute as planned | Low |

Controlled descent operating procedures are detailed in Volume 5, Section 5.6.2.

#### 7.3.3 Multiple Hazard Overlap Response Principles

When multiple hazards occur simultaneously, the Emergency Control Center (ECC) follows these principles:

1. **Highest level first**: Respond according to the highest level among the involved hazards.
2. **Single command**: The ECC issues unified commands at the warning level corresponding to the highest level, with the command listing all confirmed hazard types.
3. **Compatible responding entities**: The highest level response actions naturally cover lower level requirements. The ERT prioritizes handling lower-level hazards that can be addressed in parallel within the highest-level framework.
4. **Unified ECC command**: Scheduling authority for all response forces is centralized in the ECC.


### 7.4 Specific Emergency Plans

#### 7.4.1 Level Ⅰ: Tethering Cable Break

**Trigger Condition**: Tension sensors detect a sudden drop in tension to zero, or abnormally rapid platform altitude increase (uncontrolled ascent). Two scenarios:
- **Complete break with uncontrolled platform ascent**: Level Ⅰ response; activate escape pod.
- **Single cable break but platform still controllable**: Level Ⅱ response; execute controlled descent (see Section 7.3.2).

**Physical Consequences**: The platform loses its mechanical connection to the ground, rapidly ascending under buoyancy (helium buoyancy approximately 5,000 kg, ascent acceleration approximately 0.2–0.5 m/s²), ultimately reaching higher altitudes (50–60 km) where the low atmospheric density and excessive internal-external pressure differential causes envelope rupture. When short-term altitude maintenance is required, electric propeller auxiliary lift can be activated (see Volume 1, Section 1.3(e)).

**Response Procedure** (complete break and uncontrolled scenario):

1. **Automatic detection (<1 s)**: Tension monitoring system detects cable break, triggers Level Ⅰ red alarm.
2. **Emergency venting**: Secondary envelope (air) exhaust valves open fully, rapidly reducing buoyancy. Simultaneously, main envelope helium pressure relief valves open per preset program (controlling relief rate to avoid excessively rapid descent).
3. **Personnel evacuation**:
   - Personnel inside the gondola immediately don emergency oxygen masks and proceed to the escape pod at the bottom of the gondola.
   - Personnel inside the aerostat (if any) proceed to the nearest emergency evacuation passage.
4. **Escape pod release**: After personnel enter the escape pod, the release mechanism is activated. The escape pod detaches from the platform, deploys parachutes, and descends to the ground ballistically (see Volume 3, Section 3.5 of this Appendix).
5. **Platform self-destruct (last resort)**: Only activated when it is confirmed that the platform will fall into a densely populated area and its trajectory cannot be controlled by venting. Priority is given to rapid venting (opening multiple pressure relief valves simultaneously) to avoid using explosive cables; if explosive cables must be used, ground safety assessment and authorization are required, and the impact zone must be confirmed as a safe area.

**Escape Pod Parameters** (see Volume 3, Section 3.5 for details):

| Parameter | Value |
|:---|:---|
| Personnel Capacity | 4–6 persons |
| Total Mass (full load) | ≤600 kg |
| Descent Method | Ballistic reentry + parachute |
| Independent Life Support | ≥24 hours |

#### 7.4.2 Level Ⅱ: Gondola Depressurization

**Trigger Condition**: Pressure sensor inside gondola detects pressure drop rate >0.5 kPa/min.

**Response Procedure**:

1. **Automatic isolation**: Airtight isolation doors of the depressurized compartment close automatically (<5 s).
2. **Personnel transfer**: Personnel inside the compartment immediately don emergency oxygen masks (≥2 wall-mounted per compartment) and transfer along evacuation routes to adjacent safe compartments or the aerostat interior.
3. **Leak sealing**: ERT (Emergency Response Team) enters the damaged area with emergency sealing kits (SPUA quick-spray sealant + CFRP patches) and completes initial sealing within <30 minutes.
4. **Repressurization**: After repair, pressure is gradually restored through emergency repressurization pipes from adjacent compartments (rate ≤1 kPa/min).
5. **If repair is not possible**: Evaluate whether controlled descent is required (see Section 7.3.2).

#### 7.4.3 Level Ⅱ: Fire

**Trigger Condition**: Flame detector or smoke detector activates.

**Response Procedure**:

1. **Automatic alarm and power cutoff**: Level Ⅱ orange alarm triggers within <1 s; non-essential power to the fire compartment is automatically cut off (lighting and communications retained).
2. **Firefighting**: ERT arrives on scene within <3 minutes. CO₂ extinguishers are used for electrical fires; water mist extinguishers (low-gravity optimized nozzles) for ordinary fires.
3. **Smoke control**: Ventilation in the fire compartment switches to "smoke exhaust mode"; smoke is filtered through HEPA + activated carbon and exhausted outside the compartment.
4. **Personnel evacuation**: When the fire cannot be controlled within 5 minutes, all personnel in the affected sector evacuate to the safe zone inside the aerostat.
5. **Isolation**: If fire spreads to multiple compartments, airtight isolation doors of the area are closed to contain the fire within the minimum range.
6. **If fire cannot be controlled**: Initiate controlled descent (see Volume 5, Section 5.6); the platform descends to the ground anchoring station and personnel evacuate from the ground.

#### 7.4.4 Level Ⅱ: Total Primary Power Loss

**Trigger Condition**: Main grid voltage drops abnormally; UPS switches automatically.

**Response Procedure**:

1. **Automatic switchover (<1 s)**: UPS (uninterruptible power supply) takes over, supplying ECLSS, communications, control, and other critical loads; maintains ≥1 hour.
2. **Backup power activation**: If the primary power failure cannot be repaired within 1 hour, the emergency battery pack (capacity ≥10 kWh, can support ≥2 hours) is activated.
3. **Descent preparation**: If estimated repair time >4 hours, initiate controlled descent procedure (see Volume 5, Section 5.6); descend platform to ground anchoring station.
4. **Power restoration sequence**: After fault clearance, restore power by priority — ① ECLSS → ② Communications → ③ Navigation → ④ Others.

#### 7.4.5 Level Ⅱ: Minor Envelope Leakage (Buoyancy Reduction)

**Trigger Condition**: Pressure monitoring system detects continuous pressure decline in main envelope (rate >0.1%/h), or abnormal platform altitude decrease.

**Response Procedure**:

1. **Automatic alarm**: Level Ⅱ orange alarm triggers.
2. **Leak localization**: ERT uses ultrasonic leak detectors to locate the leak point.
3. **Temporary repair**: Emergency sealing kit (SPUA + CFRP patches) is used for temporary sealing.
4. **Propeller auxiliary lift**: Before controlled descent is executed, if buoyancy reduction causes continuous altitude decrease, electric propeller auxiliary lift can be activated (see Volume 1, Section 1.3(e)) to temporarily maintain altitude, buying time for personnel evacuation and equipment transfer.
5. **Controlled descent**: If buoyancy reduction >20% and cannot be immediately repaired, initiate controlled descent to the ground anchoring station for permanent repair.

#### 7.4.6 Level Ⅲ: Gondola Entrapment (Personnel Rescue)

**Trigger Condition**: Gondola control system sends entrapment distress signal, or telemetry shows gondola has had no movement for an extended period and cannot communicate.

**Response Procedure** (see Volume 3, Section 3.5 for details):

1. **ERT deployment**: Another working gondola (or rescue gondola built into the aerostat) departs the aerostat within ≤5 minutes of receiving the order, descending along the cable to the trapped gondola's position.
2. **Docking**: The rescue gondola docks with the top of the trapped gondola, forming an airtight passage.
3. **Personnel transfer**: Trapped personnel transfer to the rescue gondola through the emergency hatch.
4. **Return**: The rescue gondola carries the personnel back to the aerostat or descends to the ground (depending on circumstances).
5. **If the rescue gondola is also unable to resolve the entrapment**: Initiate controlled descent; descend the aerostat as a whole to the ground anchoring station for ground maintenance personnel to intervene.

#### 7.4.7 Level Ⅲ: EVA Accident

**Trigger Condition**: EVA personnel vital signs abnormal or distress signal issued.

**Response Procedure**:

1. **Buddy rescue**: Strictly follow the "two-person EVA" principle; buddy immediately assists the injured person.
2. **Retrieval**: If the injured person is <50 m from the gondola, immediately pull them back; if farther away, release a portable pressurized rescue bag, place the injured person in the bag, and pull back by the buddy.
3. **Medical support**: Medical team inside gondola prepares emergency equipment (hyperbaric oxygen chamber, defibrillator, emergency medications).
4. **Altitude reduction or ground transfer**: If injuries are serious, initiate controlled descent; platform descends to ground anchoring station and injured person is transferred to a ground medical facility.


### 7.5 Emergency Personnel Evacuation Procedures

#### 7.5.1 Evacuation Decision

| Scenario | Evacuation Method | Evacuation Destination |
|:---|:---|:---|
| Complete tethering cable break with uncontrolled platform ascent | Escape pod (configured at the bottom of each gondola/aerostat) | Ground (parachute landing in safe area) |
| Single tethering cable break but platform still controllable | Controlled descent (emergency) | Ground anchoring station |
| Fire/depressurization uncontrollable, platform still controllable | Controlled descent | Ground anchoring station |
| Personnel with acute severe illness, ground medical conditions superior to platform | Controlled descent or gondola descent | Ground medical facility |
| Envelope leakage causing insufficient buoyancy | Controlled descent | Ground anchoring station |
| Primary power failure with estimated repair time >4 hours | Controlled descent | Ground anchoring station |
| Thunderstorm warning Level Ⅲ or above | Controlled descent (see Volume 5) | Ground anchoring station |
| Platform routine rotation | Normal gondola descent | Ground anchoring station |

#### 7.5.2 Escape Pod Configuration

| Deployment Location | Quantity | Personnel Capacity | Description |
|:---|:---:|:---:|:---|
| Aerostat bottom (primary escape pod) | 1 set | 4–6 persons | Covers personnel inside the aerostat |
| Working gondola (secondary escape pod) | 1 set per gondola | 4–6 persons | Covers operating personnel inside the gondola |

Escape pod design parameters are detailed in Volume 3, Section 3.5.

#### 7.5.3 Ground Anchoring Shelter

When the platform descends to the ground due to a thunderstorm (Level Ⅳ or above) or failure, personnel transfer to the shielded shelter at the ground anchoring station. The shelter is equipped with:

- Independent life support (≥7 days)
- Emergency power (≥10 kWh)
- Communication terminal (Ka-band, connected to Ring Elevator/ground network)
- First aid medical kit
- Emergency food and water


### 7.6 Emergency Supplies and Equipment Configuration

#### 7.6.1 Platform Emergency Supplies List

| Supply Category | Item | Configuration Standard | Storage Location | Replacement Cycle |
|:---|:---|:---|:---|:---|
| **Life Support** | Emergency oxygen mask (≥30 min) | ≥2 wall-mounted per compartment | All compartments in gondola and aerostat | 5 years |
| | Portable Life Support System (PLSS) | 2 sets | Aerostat emergency equipment bay | 2 years (air cylinders) |
| **Medical Emergency** | First aid kit (wound dressing + hemostasis + pain relief + antibacterials) | 1 per gondola + 2 inside aerostat | Wall-mounted first aid box (red marking) | 1 year |
| | AED | 1 unit | Aerostat medical area | 5 years (electrode pads 2 years) |
| | Portable pressurized rescue bag | 2 sets | Aerostat emergency equipment bay | 5 years |
| **Fire Suppression** | CO₂ extinguisher (5 kg) | 2 per compartment | Fire extinguisher cabinet (red) | 5 years (annual pressure check) |
| | Water mist extinguisher (10 L) | 1 per compartment | Same as above | 5 years |
| | Self-contained breathing apparatus (≥30 min) | 2 sets per compartment | Next to fire extinguisher cabinet | 5 years (cylinders 3 years) |
| **Leak Sealing** | Emergency sealing kit (SPUA + CFRP patches) | 1 set per sealed section | Aerostat maintenance supplies bay | 5 years |
| **Communications** | Emergency hand-crank radio transceiver | 1 unit | Aerostat control room | 10 years |
| **Positioning** | Personal locator beacon (UHF + inertial) | 1 per person | Carried on person | 2 years (battery) |

> **Note**: All emergency supplies must be stored in temperature-controlled compartments (temperature maintained at 0°C–30°C), or insulated with MLI + RHU. Battery-type supplies must use low-temperature rated models (operating temperature -40°C).

#### 7.6.2 Emergency Power Configuration

| Equipment | Capacity | Usage | Description |
|:---|:---|:---|:---|
| UPS (Uninterruptible Power Supply) | 10 kWh | ECLSS, communications, control, lighting | Automatically switches over when primary power fails |
| Emergency battery pack (lithium-ion) | 20 kWh | Covers all critical loads ≥2 hours | Connected in parallel with UPS |
| Portable power unit | 2 kWh × 2 units | Gondola rescue, EVA tool power | Can be carried outside the compartment |


### 7.7 Post-Disaster Assessment and Recovery

#### 7.7.1 Post-Disaster Rapid Assessment Procedure

1. **Personnel accounting (<10 min)**: Confirm all personnel locations and safety status via personal locator beacons and sign-in records.
2. **Platform structural inspection (<1 h)**: ERT inspects envelope skin (visual + pressure monitoring), tethering cables (tension + visual), gondola airtightness.
3. **Critical systems status assessment (<2 h)**: Technical support team checks extent of damage to ECLSS, power, communications, and thermal control systems.
4. **Preliminary damage report (<6 h)**: Signed and sent by the Platform Control Center to the ground mission control center.

#### 7.7.2 Recovery Priority Sequence

| Priority | Recovery Item | Target Time | Description |
|:---:|:---|:---:|:---|
| **1** | ECLSS full function restoration | <24 h | Ensures personnel survival |
| **2** | Power backbone restoration | <48 h | Repairs power distribution system |
| **3** | Communications restoration | <24 h (minimum) / <72 h (full function) | Prioritize restoring ground-facing emergency link |
| **4** | Lift system temporary repair (can maintain controlled descent) | <72 h | Temporary envelope repair or helium replenishment |
| | Lift system permanent repair | <30 days | Subject to spare parts supply |
| **5** | Gondola function restoration | <7 days | Repairs drive system or rail sleeve |

#### 7.7.3 Platform Degraded Operating Modes

When some systems have failed but the platform can still operate safely, it may enter a degraded operating mode:

| Degraded Mode | Condition | Operating Restriction | Recovery Measure |
|:---|:---|:---|:---|
| **Reduced-Altitude Station-Keeping** | Minor envelope leakage, reduced ECLSS capacity | Station-keeping altitude ≤10 km | Repair after spare parts arrive |
| **No Gondola Operations** | Gondola drive system failure | Suspend gondola inspection and maintenance tasks | Dispatch maintenance team from ground |
| **Degraded Communications** | Primary antenna failure | Retain only Ku-band backup link | Activate DTN store-and-forward |


### 7.8 Training and Drills

#### 7.8.1 Full Personnel Emergency Training

All resident personnel (including short-term visitors) must complete the following training within 24 hours of arrival:

| Training Item | Duration | Content | Assessment Method |
|:---|:---|:---|:---|
| Platform emergency overview | 1 h | Risk classification, warning levels, evacuation routes, escape pod usage | Online exam (≥90%) |
| Emergency oxygen mask donning | 0.5 h | Target time ≤30 s | Timed practical assessment |
| Fire extinguisher operation | 1 h | CO₂ and water mist extinguisher operation | Simulated fire suppression |
| Escape pod boarding and release | 1 h | Complete full procedure on simulator | Practical assessment |

#### 7.8.2 Emergency Drills

| Drill Type | Frequency | Participating Personnel | Corresponding Warning Level |
|:---|:---|:---|:---|
| Level Ⅰ full evacuation drill (escape pod) | Once every six months | All platform personnel | Level Ⅰ |
| Level Ⅱ sector evacuation drill | Once per quarter | Designated sector personnel | Level Ⅱ |
| Level Ⅲ gondola rescue drill | Once per month | ERT + designated personnel | Level Ⅲ |
| Tabletop exercise (multiple hazards) | Once every six months | Platform commander + department heads | All levels |
| Controlled descent comprehensive drill | Once every six months | Platform Control Center + ground anchoring station | Level Ⅱ/Ⅲ |

> **Note**: The controlled descent comprehensive drill focuses on the platform's overall descent operations and ground anchoring station docking, and does not include escape pod release (escape pod drills are conducted separately).


### 7.9 Parameter Outputs

| Parameter | Value | Status | Receiving Volume |
|:---|:---|:---|:---|
| Warning levels | Levels Ⅰ/Ⅱ/Ⅲ/Ⅳ (four levels) | Design baseline | — |
| Level Ⅰ full evacuation response time limit | ≤5 min (from alarm to entering escape pod) | Design target | Volume 8 |
| Level Ⅱ sector evacuation time limit | ≤3 min | Design target | — |
| Level Ⅲ gondola rescue ERT response time limit | ≤5 min | Design target | Volume 3 |
| Escape pod personnel capacity | 4–6 persons | Design baseline | Volume 3 |
| Escape pod total mass (full load) | ≤600 kg | Design baseline | Volume 3 |
| UPS capacity | 10 kWh | Design baseline | Volume 2 |
| Emergency battery pack capacity | 20 kWh | Design baseline | Volume 2 |
| Emergency supplies storage cycle | 1–10 years | Design baseline | Volume 8 |
| Full personnel emergency training time limit | Within 24 hours of arrival | Regulatory requirement | — |
| Level Ⅰ evacuation drill frequency | Once every six months | Regulatory requirement | — |
| Controlled descent comprehensive drill frequency | Once every six months | Regulatory requirement | — |


### 7.10 Volume 7 Concluding Remarks

This volume has completed the systematic planning of the emergency protection and rescue system for the stratospheric platform, converting the survival philosophy of Main Volume 12 into executable engineering plans. The core contributions are:

1. **Established a four-level risk classification and warning system**. Covers three major categories of risks: natural environment, platform failures, and operational accidents, with clear highest-level response principles when multiple hazards overlap.

2. **Clarified the broad applicability of controlled descent**. Not limited to scenarios where fire or depressurization cannot be controlled, but applicable to thunderstorm warnings, gondola entrapment, primary power failure, envelope leakage, communication interruptions, personnel illness, single cable breaks, and other situations, with a priority ranking provided. Controlled descent is one of the core means of platform emergency response.

3. **Developed specific emergency plans**. Covering tethering cable break (distinguishing complete break uncontrolled versus single break controllable), gondola depressurization, fire, primary power loss, envelope leakage, gondola entrapment, and EVA accidents; each plan has clearly defined trigger conditions, response procedures, and responsible parties, with linkage to controlled descent decisions. The envelope leakage response supplements the reference to propeller auxiliary lift (see Volume 1, Section 1.3(e)).

4. **Designed a two-tier personnel evacuation scheme**. Using escape pods in emergencies (parachute landing in safe areas), and controlled descent to the ground anchoring station in controllable situations. Escape pod parameters are fully aligned with Volume 3. Platform self-destruct is explicitly defined as a last resort, with strict preconditions specified.

5. **Configured complete emergency supplies and equipment**. Including life support, medical emergency, fire suppression, leak sealing, communications, positioning, and backup power, covering all requirements for Level Ⅰ–Ⅲ responses, with supplemented low-temperature adaptability requirements.

6. **Established a post-disaster assessment and recovery framework**. Recovery priority sequence clearly defined (ECLSS → Power → Communications → Temporary lift repair → Gondola), distinguishing time targets for temporary versus permanent repairs, and defining degraded operating modes.

7. **Planned training and drill systems**. All personnel complete training within 24 hours of arrival; Level Ⅰ evacuation drills every six months; Level Ⅱ evacuation every quarter; Level Ⅲ rescue every month; controlled descent comprehensive drills and escape pod drills explicitly differentiated.

This volume's output parameters can support Volume 8 (Deployment and Maintenance) and Volume 9 (Economic Model). The interface with Main Volume 12 is: the stratospheric platform's "escape pod" shares technical solutions with the Ring Elevator gondola's "doomsday life pod", and the rescue procedures are aligned with the Ring Elevator's "full evacuation" protocol.


### References

[7.1] Main Volume 12: Emergency, Redundancy and Lifeline Engineering, 2026.

[7.2] NASA-STD-3001, Vol.2: Human Factors, Habitability, and Environmental Health, 2019.

[7.3] Volume 1 of this Appendix: Platform Overall Design, 2026.

# Appendix I: Lunar Industry

## Volume VIII: Emergency, Protection, and Rescue

**Version**: 1.6<br/>
**Date of Preparation**: June 2026<br/>
**Currency Unit**: RMB (Y)<br/>
**Related Main Volume**: Main Volume XII (Emergency, Redundancy, and Lifeline Engineering)<br/>
**Prerequisite Reading**: Appendix I Volume I (Pioneer Missions), Volume II (Siting and Infrastructure), Volume III (Energy System), Volume VII (Habitation and Cities)


### Terminology Table

| Abbreviation | Term | Description |
|------|----------|------|
| CELSS | Closed ecological life-support system | Self-circulating life-support system |
| ECLSS | Environmental control and life-support system | Environmental Control and Life Support System |
| EVA | Extravehicular activity | Astronaut operations outside the habitat on the lunar surface or in space |
| GCR | Galactic cosmic rays | High-energy particle radiation from outside the Solar System |
| HEPA | High-efficiency particulate air filter | High Efficiency Particulate Air Filter |
| kWe | Kilowatt electric power | Electric output unit of a power-generation system |
| kWh | Kilowatt-hour | Energy unit |
| MLI | Multi-layer insulation blanket | Reflective passive insulation used for thermal control in vacuum |
| MPa | Megapascal | Pressure/stress unit |
| PE | Polyethylene | High-density polyethylene radiation-moderation shielding material |
| PLSS | Portable life-support system | In-suit oxygen supply, thermal control, and CO₂ scrubbing system |
| PTFE | Polytetrafluoroethylene | Sealing material with low friction and broad-temperature vacuum compatibility |
| RHU | Radioisotope heating unit | Device using radioactive decay heat for thermal maintenance |
| SP | Solar proton event | Solar Proton Event |
| SPE | Solar particle event | Solar Particle Event, including protons, electrons, and heavy ions |
| SPUA | Spray polyurea elastomer | High-elasticity waterproof coating used to seal microcracks in cave walls |
| UHMWPE | Ultra-high-molecular-weight polyethylene | Wear-resistant, low-friction material |


### 8.1 Opening Statement

This volume is positioned as the **emergency protection and rescue planning framework** of the lunar industrial system, focused on the following core questions:

> During decades of operation, lunar bases will inevitably face sudden events such as solar particle events (SPE), micrometeoroid impacts, critical-system failures, fires, and toxic leaks. Multiple hazards may be triggered simultaneously. When disasters occur, how can crew survival be guaranteed? How can effective rescue be conducted under extreme lunar conditions? After base damage, how can minimum operations be restored quickly? From warning to response, from evacuation to sheltering, from self-rescue to mutual rescue, how can an independent, reliable, layered emergency protection and rescue system be established far from Earth, without real-time ground support?

This volume builds on:

- **Volume I (Pioneer Missions)**: technical feasibility of SPE warning and radiation monitoring has been confirmed.
- **Volume II (Siting and Infrastructure)**: physical layout of functional zones has been established, as well as the natural protection advantages of underground lava tubes and preliminary storm-shelter siting.
- **Volume III (Energy System)**: a baseline framework has been established for emergency power (independent reactor supply, thermal-storage hot restart) and black-start plans.
- **Volume VII (Habitation and Cities)**: sealed pressurized habitation design, medical-station configuration, and microbial control in enclosed spaces are already defined.

**Environmental baseline statement**: All emergency facilities, equipment selection, material specifications, and operating procedures in this volume are adapted for low gravity (1/6 g). Under low gravity, fluid behavior is surface-tension-dominated (affecting extinguisher spray shape and coverage efficiency), human motion characteristics change (affecting evacuation speed and rescue posture), and combustion behavior changes (reduced buoyancy slows smoke rise [6][7]). Parameters involving these physical processes are annotated with low-gravity adaptation measures in relevant sections.

Core tasks of this volume:

1. Identify and classify all emergency events and disaster risks faced by lunar bases, establish a classification coding system, and build a six-level risk matrix ranked by impact scope and consequence severity.
2. Establish a response principle for compound hazards: execute response according to the highest triggered danger level.
3. Design a standardized warning code system in the format "Level-Category Code" and a six-level warning workflow to ensure clear, coherent command transitions from "full evacuation" to "normal operations".
4. Plan a base-wide sheltering and disaster-isolation system, including shelter tiering, physical isolation measures (firewalls/fire panels, negative-pressure gradient isolation), protection parameters, material reserve standards, and distribution density.
5. Develop specialized contingency plans by risk level and category, covering base-level (I-AS), district-level (II-BS, II-BH, II-DC), and individual-level (III-CE) scenarios.
6. Establish an organizational framework for post-disaster rapid assessment, lifeline restoration, and long-term reconstruction.
7. Define phased validation criteria for the emergency protection and rescue system and align with the "lifeline" engineering concept in Main Volume XII.


### 8.2 Risk Identification and Tiering

#### 8.2.1 Classification of Emergencies and Disasters

Emergency and disaster risks for lunar bases are grouped into four major categories, with numbered risk types in each category.

**Category A: Space-environment emergency events**

| Code | Risk Type | Description | Warning Lead Time | Impact Scope | Severity |
|:---:|:-----|:-----|:-----|:-----|:-----|
| **AS** | Solar particle event | Solar eruptions can raise high-energy proton and heavy-ion flux to 10^4-10^5 times baseline within hours | Tens of minutes to several hours | Entire lunar surface and shallow underground (<10 m cover) | **Extreme** |
| **AG** | GCR enhancement | Modulated by solar activity, GCR flux can increase 2-3x at solar minimum. Annual lunar GCR dose is about 380 mSv at solar minimum and about 110 mSv at solar maximum [5] | No short-term warning (11-year cycle) | Entire lunar surface | **Low** |
| **AM** | Micrometeoroid/debris impact | Millimeter- to centimeter-scale particles strike base structures at 10-70 km/s | No warning | Impact point and adjacent compartments | **Medium to extreme** |
| **AP** | Geomagnetic storm/solar-wind disturbance | High-energy particles and magnetic disturbances may interfere with electronics and communications | Hours to days | All surface electronic equipment | **Medium** |

**Category B: Internal base system failures**

| Code | Group | Risk Type | Description | Warning Lead Time | Impact Scope | Severity |
|:---:|:-----|:-----|:-----|:-----|:-----|:-----|
| **BS** | Structural integrity | Seal failure/depressurization | Hull breach, sealing-layer aging, or airlock fault causing atmospheric leakage | None (sudden) or minutes (slow leak) | Single to multiple compartments | **Extreme** |
| **BH** | Fire and leakage | Fire | Electrical short, equipment overheating. Under low gravity, reduced buoyancy slows smoke rise and may delay detector response [6][7]. Extinguisher spray morphology and coverage become surface-tension-dominated and require optimized nozzles | None or seconds (smoke detection) | Single compartment | **Extreme** |
| | | Toxic leak | Chemical tank rupture, reactor fault, battery thermal runaway releasing toxic gas | None to minutes | Single to adjacent zones | **High** |
| **BL** | Utilities | Life-support failure | ECLSS key-equipment malfunction | Minutes to hours | Entire base or affected compartments | **Extreme** |
| | | Power-system failure | Generation, transmission, or distribution fault | None to minutes | Single district to whole base | **High** |
| | | Thermal-control failure | Active loop leak or radiator failure | Minutes to hours | Single district to whole base | **Medium** |

**Category C: External operational accidents**

| Code | Risk Type | Description | Warning Lead Time | Impact Scope | Severity |
|:---:|:-----|:-----|:-----|:-----|:-----|
| **CE** | EVA accident | Suit breach, PLSS failure, rover rollover, fall, or entrapment. Under low gravity, rover braking distance increases and rescue posture differs from Earth training | No warning | Involved astronaut(s) | **Extreme** |
| **CF** | Mining/construction accident | Drill jamming, collapse, explosion, equipment collision. Under low gravity, ejecta spread and rollover risk increase | No warning | Involved personnel and equipment | **High** |
| **CT** | Transport accident | Rover collision, rail derailment, skylight-lift failure | No warning | Involved personnel and equipment | **High** |

**Category D: Geological and environmental hazards**

| Code | Risk Type | Description | Warning Lead Time | Impact Scope | Severity |
|:---:|:-----|:-----|:-----|:-----|:-----|
| **DQ** | Moonquake | Shallow moonquakes (M4-M5) or deep quakes (tidally triggered), potentially causing landslides and rockfall [9][10] | No warning | Tens to hundreds of km around epicenter | **Medium to low** |
| **DC** | Local lava-tube collapse | Natural or construction-induced roof instability. Layered roofs are less stable than homogeneous rock [11][12] | None to hours (microseismic precursors possible) | Local cave section | **Extreme** |
| **DS** | Lunar dust storm | Large-scale dust lofting from EVA operations, lander plumes, or electrostatic levitation | No warning | Local | **Low** |

#### 8.2.2 Six-Level Risk Warning System

All risks are mapped by consequence severity and impact scope into six levels. Warning code format: "Level-Category Code".

| Level | Name | Definition | Typical Scenario and Warning Code | Warning Marker |
|:---:|:-----|:-----|:-----|:-----|
| **I** | **Base-level catastrophe** | Threatens all base personnel, requires immediate full evacuation into Level-I shelters | **I-AS**: major SPE (>100 MeV proton flux >10^3 pfu); **I-BL**: full-base ECLSS/power failure | Red + continuous audio/visual alarm + all-hands broadcast |
| **II** | **District-level major incident** | Threatens multiple personnel in one independent functional district or cave segment; full evacuation of affected district required | **II-BS**: single-compartment depressurization (>5 kPa/min); **II-BH**: uncontrolled fire; **II-DC**: local lava-tube collapse; **II-BL**: multi-district power failure | Red + intermittent audio/visual alarm + district broadcast |
| **III** | **Individual-level fatal incident** | Threatens 2-3 involved persons; ERT must launch precision rescue immediately | **III-CE**: suit breach/PLSS failure; **III-CE**: rover rollover/entrapment; **III-CF**: construction crush/fall accident | Red + forced personal-terminal push |
| **IV** | **District-level general incident** | Significant risk to district personnel, but not yet immediately fatal | **IV-BS**: slow leak (<=0.5 kPa/min); **IV-BH**: controlled local fire/micro toxic leak; **IV-BL**: single-point critical-system failure | Orange + district broadcast |
| **V** | **Local anomaly** | Potential risk or local equipment anomaly | **V-AS**: >=M-class solar flare enhancement; **V-AP**: geomagnetic storm alert; **V-DQ**: moonquake precursor signal; **V-BL**: local thermal-control failure | Yellow + affected-zone alert |
| **VI** | **Routine risk** | Known, expected routine risk notification | **VI-AG**: GCR enhancement trend; **VI-DS**: lunar dust storm; **VI-CT**: routine transport peak; **VI-AM**: single non-cascading micrometeoroid impact | Blue + informational notice to all |

#### 8.2.3 Full Cross-Reference Table: Risk Levels and Warning Codes

| Risk Type | Category Code | Impact Scope | Risk Level | Warning Code |
|:-----|:---:|:-----|:---:|:---:|
| SPE major event (>100 MeV) | AS | Whole base | I | **I-AS** |
| Full-base ECLSS failure | BL | Whole base | I | **I-BL** |
| Full-base power failure | BL | Whole base | I | **I-BL** |
| Seal failure/depressurization (multi-compartment) | BS | District-level | II | **II-BS** |
| Fire (uncontrolled spread from single compartment) | BH | District-level | II | **II-BH** |
| Local lava-tube collapse | DC | District-level | II | **II-DC** |
| EVA accident (suit breach/PLSS failure) | CE | Individual-level | III | **III-CE** |
| EVA accident (rover fault) | CE | Individual-level | III | **III-CE** |
| Mining/construction accident (crush/fall) | CF | Individual-level | III | **III-CF** |
| Slow leak (<=0.5 kPa/min) | BS | District-level | IV | **IV-BS** |
| Local fire (already controlled) | BH | District-level | IV | **IV-BH** |
| Micro toxic leak | BH | District-level | IV | **IV-BH** |
| Single-point critical-system failure | BL | District-level | IV | **IV-BL** |
| Solar flare enhancement (>=M class) | AS | Whole base | V | **V-AS** |
| Geomagnetic storm/solar-wind disturbance | AP | Whole base | V | **V-AP** |
| Moonquake precursor signal | DQ | District-level | V | **V-DQ** |
| Local thermal-control failure | BL | District-level | V | **V-BL** |
| GCR enhancement event | AG | Whole base | VI | **VI-AG** |
| Lunar dust storm | DS | Individual to district | VI | **VI-DS** |
| Routine transport peak period | CT | District-level | VI | **VI-CT** |
| Single micrometeoroid impact (non-cascading) | AM | Local | VI | **VI-AM** |


### 8.3 Six-Level Warning and Response System

#### 8.3.1 Response Principle for Compound Hazards

A base may experience multiple hazards simultaneously or in sequence (for example, moonquake-triggered depressurization plus fire, or EVA accident during SPE warning). In such cases, the Emergency Control Center (ECC) shall follow:

1. **Highest-level priority**: when multiple hazards are triggered, response follows the highest danger level. Example: V-DQ (moonquake precursor) + II-BS (depressurization) is handled at Level II with district evacuation. If II-BS + I-AS (SPE), execute Level I full evacuation.
2. **Single-command stream**: ECC issues one unified command based on the highest level and shall not issue conflicting instructions from multiple levels. Commands must still list all confirmed hazard types for situational awareness.
3. **Responder compatibility**: higher-level response naturally covers lower-level needs (Level I full evacuation includes Level II district evacuation and Level III rescue requests). However, within the Level-I framework, ERT and technical support should still handle lower-level hazards when parallel handling is feasible (e.g., during Level-I evacuation, a concurrent III-CE personal distress still requires ERT EVA rescue, with return before Level-I sheltering deadlines).
4. **Unified ECC command**: in compound-hazard scenarios, all response-force dispatch authority is centralized at ECC. No team may autonomously change response level or direction without ECC authorization.

#### 8.3.2 Warning-Level Summary Table

| Level | Name | Color Marker | Typical Warning Code | Trigger Condition | Response Time Limit | Response Action | Response Entity |
|:---:|:-----|:-----|:-----|:-----|:-----|:-----|:-----|
| **I** | **Base-level catastrophe** | Red + continuous audio/visual alarm | I-AS, I-BL | SPE >100 MeV flux >10^3 pfu, or full ECLSS failure | Immediate (<5 min) | Full evacuation into Level-I shelters | Entire base + ECC centralized command |
| **II** | **District-level major incident** | Red + intermittent audio/visual alarm | II-BS, II-BH, II-DC, II-BL | Depressurization >5 kPa/min, or uncontrolled fire, or collapse warning | <3 min | Full evacuation of affected district into Level-II shelters + immediate ERT dispatch | Affected district + ERT + ECC |
| **III** | **Individual-level fatal incident** | Red + forced personal push | III-CE, III-CF | EVA/construction vital-sign anomaly or distress signal | ERT dispatch <5 min | Precision ERT rescue + medical team standby | ERT + medical team + involved personnel self-rescue |
| **IV** | **District-level general incident** | Orange | IV-BS, IV-BH, IV-BL | Slow leak, controlled fire, micro toxic leak, single-point critical failure | <30 min | Full protective actions by affected district + ERT standby | Affected district + ERT standby |
| **V** | **Local anomaly** | Yellow | V-AS, V-AP, V-DQ, V-BL | >=M-class flare, moonquake precursor, anomalous equipment heating, geomagnetic storm alert | <2 h | Preventive preparation + technical support on site | Technical support + affected personnel |
| **VI** | **Routine risk** | Blue | VI-AG, VI-DS, VI-CT, VI-AM | Routine risk notification | Routine notice | No special action required | Awareness by all personnel |

#### 8.3.3 Level-I Base Catastrophe (I-AS: SPE) Response Workflow

Solar particle events (SPE) are among the most challenging space-environment emergencies for lunar bases. Current SEP forecasting combines empirical, physics-based, and machine-learning approaches, with 30-60 min lead time for >100 MeV proton events [1][2]. Standard workflow under **I-AS**:

**(a) Warning intake stage (T-60 min to T-30 min after SPE alert issuance)**

1. Circumlunar space-environment monitoring satellites (or particle detectors on Queqiao-2) detect anomalous high-energy particle flux and automatically send warning signals to base control. Current SEP prediction models can provide a 30-60 minute warning window based on coronagraph observations and real-time particle flux data [2].
2. On-duty AI in control center validates source and flux data within <10 s; if Level-I threshold is exceeded, trigger base-wide **I-AS** red alert immediately (audio/visual alarm + all-band broadcast + forced personal-terminal push).
3. Duty commander confirms alert and issues all-personnel evacuation order within <60 s.

**(b) Personnel evacuation stage (T-30 min to T-5 min)**

1. All non-essential personnel stop current activities and proceed along designated routes to nearest storm shelter (Section 8.4.1). Evacuation timing estimates include low-g gait characteristics (larger step length, lower cadence).
2. EVA personnel immediately abort operations and return to nearest airlock. If return within 15 min is impossible, execute "shelter in place": shut down non-essential rover loads, use rover hull as temporary shielding, and wear emergency radiation vest (equivalent shielding >=5 g/cm2; low-g wearability does not impede basic movement) while awaiting rescue. Artemis I radiation measurements support effectiveness of this strategy [8].
3. Control center tracks real-time evacuation progress via personal terminals.
4. All personnel must complete sheltering before arrival of SPE high-energy leading edge.

**(c) Shelter sustainment stage (typically 1-3 days during SPE)**

1. Storm shelter activates independent ECLSS (self-sustain >=30 days).
2. Shelter occupants wear personal dosimeters for continuous cumulative-dose monitoring. All loose items are secured with hook-and-loop or elastic straps for low-g drift control.
3. Control center maintains communications through shelter terminals and provides periodic SPE flux trend updates.
4. Medical station (Section 7.7.1) shifts to emergency mode to receive potentially overexposed personnel.

**(d) Recovery and assessment stage**

1. Circumlunar monitoring confirms high-energy particle flux remains below Level-I threshold for >2 h.
2. Control center issues "all-clear" and personnel return in controlled batches.
3. Perform radiation dose audit for all personnel. Crew with annual cumulative dose above 50 mSv receive priority rotation back to Earth.

#### 8.3.4 Level-II District Major Incident (II-BS: Seal Failure/Depressurization) Workflow

**(a) Detection and warning**

- All pressurized compartments are equipped with online pressure sensors (accuracy <=0.1 kPa) and ultrasonic leak locators (sensitivity <=1 cm3/s at 70 kPa differential).
- When pressure drop rate >0.5 kPa/min, system triggers **IV-BS** orange warning automatically; when >5 kPa/min, trigger **II-BS** red warning.

**(b) Response workflow**

1. **Automatic isolation**: airtight isolation doors at both ends of affected compartment close automatically within <5 s after pressure-drop detection (spring energy storage + electromagnetic trigger independent of external power). Door closing speed is low-g compensated with spring-assisted acceleration.
2. **Personnel evacuation**: personnel in affected compartment immediately don nearest emergency oxygen masks (>=2 wall-mounted per compartment, elastic mesh head harness prevents drift in low g) and evacuate to adjacent safe compartments or nearest Level-II shelter.
3. **Leak localization and sealing**: ERT rapidly locates breach using ultrasonic indicators. Use emergency sealing kit (fast-spray SPUA + CFRP patch + inflatable temporary airlock) to complete initial sealing within <30 min. SPUA rheology is optimized for surface-tension-dominated low-g flow, with thixotropic setting time <=15 s.
4. **Repressurization**: after repair, adjacent compartment repressurizes isolated section through emergency line, at <=1 kPa/min up to 70 kPa.

**(c) Minimum survival condition**

Under worst case (e.g., simultaneous depressurization in multiple compartments and no immediate repair), escalate to Level I and retreat all personnel to Level-I storm shelters.

#### 8.3.5 Level-II District Major Incident (II-BH: Fire) Workflow

**(a) Preventive measures**

- Disaster isolation system (Section 8.4.4) is the fire-control foundation. Firewalls and fire panels are integrated during construction. Adjacent compartments are organized as independent fire zones so a single-zone fire is not allowed to propagate by design.
- All pressurized compartments install multispectral flame detectors (UV+IR dual-band, <=50 ms response) and aspirating smoke detectors (sensitivity <=0.01% obs/m). Detector spacing is tightened for low-g behavior [6][7].
- Open flame is prohibited in pressurized compartments. All heating equipment requires overtemperature auto power-cut.
- All base fabrics meet UL 94 V-0 flame-retardant standard [13].

**(b) Response workflow**

1. **Detection and alarm**: once flame/smoke detector triggers, control center issues **II-BH** red warning within <1 s and cuts non-essential power in fire compartment (keep lighting/communications). Fire doors at adjacent zones close automatically to form isolation boundary. ESA studies indicate return-duct smoke detection can reduce low-g fire detection latency [7].
2. **Fire suppression**: ERT arrives within <3 min. Select suppression method by fire type: electrical fires use CO₂ extinguisher or fine water mist (<50 um droplets, non-conductive). Dry powder and halon are prohibited. Nozzle geometry is optimized for low-g droplet behavior to ensure coverage. Strategy references crewed-spacecraft fire-suppression reviews [6].
3. **Smoke control**: ventilation switches to smoke-exhaust mode in fire compartment: supply reduced to 20%, return increased to 100%. Smoke passes through HEPA + activated carbon before venting to vacuum. Fire dampers in ducts close automatically at >150 C to prevent fire spread through ventilation.
4. **Personnel evacuation**: if fire cannot be controlled within 5 min, all personnel in affected district evacuate to nearest Level-II shelters. Firefighters wear self-contained breathing apparatus (>=30 min oxygen; low-g-compatible elastic mesh face seal). If spread reaches multiple compartments, escalate to **Level I**.

**(c) Controlled depressurization extinguishing (optional final measure)**

ECC may authorize controlled vent-to-vacuum extinguishing only when all conditions below are met:

1. All personnel in fire compartment are confirmed evacuated, or no survivors are detected by life sensors.
2. Airtight isolation doors to adjacent compartments are closed and pressure is stable (isolation confirmed).
3. Fire cannot be controlled by normal means within 30 min.
4. Venting will not backflow toxic smoke into other compartments through shared ducts (fire dampers confirmed closed).

Operation steps: ECC remotely opens compartment vent valve and depressurizes at controlled rate (pressure drop <=10 kPa/min) to lunar vacuum. Once oxygen is depleted, combustion ceases. Maintain vacuum >=15 min to ensure complete extinguishment of residual embers. Repressurization may begin only after ERT confirms no re-ignition risk. Any compartment subjected to controlled depressurization extinguishing must pass full structural integrity inspection before repressurization.

**Constraints**: this method is not applicable if survivors remain inside, vent valves fail or are obstructed, adjacent-zone isolation integrity is unverified, or structural materials in compartment walls are already burning (risk of uncontrolled structural breakup during venting).

Note: NASA SAFFIRE in-orbit experiments on Cygnus have validated large-scale fire behavior and propagation models in microgravity [14].

#### 8.3.6 Level-III Individual Fatal Incident (III-CE: EVA Accident) Workflow

**(a) Accident types**

- Suit breach (micrometeoroid impact or sharp-rock cut)
- PLSS failure (oxygen interruption, CO₂ removal failure, thermal-control failure)
- Rover failure (loss of propulsion, rollover, terrain entrapment; rescue route planning must include longer braking distance in low g)
- Personnel fall or communication loss

**(b) General response principles**

1. **Buddy rescue**: EVA strictly follows two-person rule; continuous visual contact required.
2. **30-second golden rule**: for rapid suit depressurization from severe breach, healthy partner must drag casualty into nearest pressurized facility within 30 s. In low gravity, mass is unchanged but weight is one-sixth, reducing required pulling force; however, rescuer footing stability must be maintained.
3. **Remote support**: control center continuously monitors EVA vital signs and triggers **III-CE** red alert immediately upon anomaly, dispatching second ERT EVA reinforcement.

**(c) Scenario-specific handling**

**Suit breach**:
1. Minor breach: wrap emergency seal tape >=3 turns. Tape handling and wrapping in low g have been validated in gloved ergonomics tests.
2. Major breach: execute the 30-second golden rule immediately. If distance to airlock >100 m, use portable pressurized rescue bag (lightweight foldable composite unit, deployed volume ~1 m3). Low-g deployment is attitude-independent. Healthy partner supplies oxygen through emergency feed port from own PLSS. Deployment procedure is included in low-g ERT qualification drills.
3. If casualty has been exposed to vacuum for tens of seconds, after entering pressurized facility immediately perform repressurization/rewarming (target 70 kPa pure O2, repressurization rate <=5 kPa/s) and evaluate vacuum-exposure injury.

**Rover failure**:
1. Dispatch healthy rover or base ERT immediately. Repair if feasible; otherwise transfer crew.
2. If all rovers unavailable and distance to base >5 km, execute on-foot return procedure (PLSS full load endurance >=8 h; emergency walking speed ~3 km/h is feasible at 1/6 g, but gait stability requires training). Base tracks position and PLSS battery continuously and dispatches interception support as required.

#### 8.3.7 Response Organizational Structure

| Role | Responsibility | Permanent/Temporary | Applicable Warning Levels |
|:-----|:-----|:-----|:-----|
| **Base Commander** | Highest decision authority; issues alert activation and release commands | Permanent | I/II |
| **Emergency Control Center (ECC)** | Base-wide situational awareness, compound-hazard judgment, communication dispatch, resource allocation | Permanent | All levels |
| **Emergency Response Team (ERT)** | Frontline firefighting, leak sealing, search and rescue, emergency medical care | Permanent (4-6 people, 24-hour rotation) | II/III/IV |
| **Technical Support Team** | Fault diagnosis and remote repair guidance | Temporary | II/IV/V |
| **Medical Rescue Team** | Casualty triage, emergency treatment, evacuation decisions | Permanent | III/IV |
| **Logistics Support Team** | Emergency supplies allocation, shelter replenishment, transport coordination | Temporary | I/II |


### 8.4 Emergency Shelter System and Disaster Isolation

#### 8.4.1 Shelter Tiering

| Level | Name | Protection Capability | Capacity | Distribution Density | Self-Sustainment Time | Applicable Warning Levels |
|:---:|:-----|:-----|:-----|:-----|:-----|:-----|
| **I** | **Storm shelter (SPE dedicated)** | Equivalent shielding >=50 g/cm2 (about 5 m regolith cover, or >=50 m basalt roof + >=10 mm PE moderation layer), peak SPE dose attenuation >=99.9% [4] | Maximum base population +20% reserve | At least 1 per habitation district, <=5 min walking distance | >=30 days (independent ECLSS + independent power) | I |
| **II** | **Emergency shelter (multi-purpose)** | Equivalent shielding >=20 g/cm2 (about 2 m regolith cover, or >=30 m basalt roof) | >=10 persons per shelter | At least 1 per major functional district | >=7 days | II/IV |
| **III** | **Shelter-in-place zone** | Standard habitation protection (>=5 mSv/year) + independent airtight isolation doors | Compartment capacity | 1 per compartment | >=24 h (relying on main ECLSS) | V |

Note: Storm-shelter shielding design accounts for organ-dose contributions from albedo neutrons/protons during major SPEs [4].

#### 8.4.2 Level-I Storm Shelter Design Parameters

| Parameter | Design Value | Notes |
|:-----|:-----|:-----|
| **Total volume** | >=3.5 m3/person | Based on maximum base population +20% reserve |
| **Radiation shielding** | Top cover >=5 m loose regolith, or >=0.5 m sintered brick + >=50 m basalt (underground option); inner wall lined with >=10 mm PE moderation layer | Peak SPE attenuation >=99.9% [4] |
| **Independent ECLSS** | O2 >=0.84 kg/person/day, CO₂ removal >=1.0 kg/person/day, closed-loop water recovery, temperature 18-25 C | Independent operation >=30 days |
| **Independent power** | Li-ion battery bank >=50 kWh + compact nuclear source (>=3 kWe) or fuel cell | Supports all ECLSS, lighting, communications |
| **Emergency supplies** | Drinking water >=3 L/person/day, emergency food >=2,000 kcal/person/day, first-aid kits (including radiation-treatment meds) | >=30-day stock for full shelter-rated population |
| **Communications** | Independent Ka-band antenna + buried fiber dual link | Maintains communication with base control and Earth |
| **Sanitation facilities** | Independent vacuum toilet unit (shared technology with Section 7.5.4) | >=1 set per 10 persons |
| **Psychological support** | Adjustable LED circadian simulation + personal entertainment terminals | - |
| **Low-g adaptation** | All loose items fixed with hook-and-loop or elastic straps; sleeping zones use flexible memory-net beds (same type as Section 7.5.3) with added lateral soft rails to prevent random low-g drift | - |
| **Redundancy** | n+1 redundancy for all critical equipment | Any single-point failure does not disable shelter function |

#### 8.4.3 Shelter Layout Principles

- **Walkable access**: any habitation unit must be <=5 min walk from nearest Level-I shelter (about 100-150 m; low-g gait effects are included in estimates).
- **Physical dispersion**: Level-I shelters shall not be concentrated in one cave section or under one dome; they must be geologically isolated.
- **Clear signage**: self-luminous directional signs (tritium light source or LED with backup battery) along main corridors.
- **Barrier-free passage**: all entrances >=1.2 m clear width with swing doors accommodating suited crew and casualty transport. Low-g stretcher handling posture must be specifically drilled in ERT training.

#### 8.4.4 Disaster Isolation System

Disaster isolation is the core defense that prevents district-level incidents (fire, toxic leak, depressurization) from escalating to base-level catastrophe. The system has three layers:

**(a) Layer 1: Active isolation - airtight isolation doors**

- All passages between pressurized compartments include airtight isolation doors (spring-stored energy + electromagnetic trigger, independent of external power). Doors close automatically when: pressure drop >0.5 kPa/min (depressurization isolation); flame/smoke detection with fire-zone boundary trigger (fire isolation); toxic-gas sensor trigger (leak isolation).
- Closed-door differential pressure tolerance is >=100 kPa (vacuum on one side, standard pressure on the other), preventing depressurization spread.
- Door closure signals are sent to ECC and highlighted on control displays as disaster-boundary overlays.

**(b) Layer 2: Passive isolation - firewalls and fire panels**

- Partition walls between adjacent fire zones use fire-resistant structures: dual aluminum-alloy skins (>=3 mm each) with >=50 mm aerogel insulation core. Fire-resistance limit >=120 min (ISO 834-1 heating curve; low-g flame behavior differs, but insulation performance is gravity-independent).
- Fire dampers are installed where ducts pass through firewalls (fusible trigger >150 C for automatic closure) to prevent fire spread through ventilation.
- Independent fire-isolation transition sections are inserted between industrial and habitation districts (>=5 m unpressurized transition with airtight doors at both ends). This ensures even full-compartment industrial fire does not drive smoke into habitation zones.

**(c) Layer 3: Active isolation - negative-pressure gradient isolation**

- During toxic leak (IV-BH), if source compartment cannot be sealed immediately, ECC can establish negative-pressure gradient across source and adjacent safe compartment via ventilation control (source return flow to 120%, supply reduced to 30%, pressure differential >=10 Pa). This ensures leakage moves from safe to affected zone, preventing reverse spread.
- Medical isolation wards (Section 7.7.1) use the same principle at constant -15 Pa.

**(d) Isolation-system validation criteria**

- Firewall fire resistance >=120 min.
- Airtight isolation-door full closure <=5 s from trigger.
- Fire-damper fusible closure <=10 s.
- Negative-pressure gradient establishment <=60 s.


### 8.5 Specialized Emergency Plans

#### 8.5.1 Level-II District Major Incident (II-DC: Local Lava-Tube Collapse) Emergency Plan

**(a) Prevention and monitoring**

- Select high-quality lava tubes meeting Volume I Section 1.3 criterion (a): roof thickness >=30 m and no recent collapse or fault activity. Homogeneous roofs are preferred over layered roofs [11][12].
- Deploy distributed fiber-optic acoustic/strain monitoring along developed sections (one node per 100 m). Strain-rate threshold exceedance triggers **V-DQ** yellow warning.

**(b) Response workflow (II-DC)**

1. **Yellow-warning stage**: evacuate non-essential personnel from affected section; ERT and technical support perform intensified GPR roof scanning; install temporary hydraulic support columns (>=500 kN each) if needed.
2. **Post-collapse**: airtight isolation doors auto-close (<1 s) on fiber-break signal, preventing depressurization and dust spread to adjacent sections; control center performs missing-person accounting; ERT carries life detectors to assess rescue feasibility.
3. **Rescue and recovery**: after roof stabilization is confirmed (strain normal for >1 h), use small remotely operated excavation equipment for layered debris removal with simultaneous life-signal scanning. ERT members wear locator beacons and operate with rear safety observers.

#### 8.5.2 Level-I Base Catastrophe (I-BL: Full Power Blackout) Emergency Plan

**(a) Trigger condition**

Simultaneous failure of both redundant main ring bus lines or simultaneous offlining of all primary generation units. If concurrent with SPE or other hazards, apply compound-hazard principle in Section 8.3.1.

**(b) Response workflow (I-BL)**

1. **Automatic takeover**: Level-I shelters and medical stations transfer to UPS within <1 s, maintaining critical loads for >=1 h.
2. **Black start**: reactor self-start within <10 min to restore generation. If reactor unavailable, start supercritical CO₂ turbine via thermal-storage hot start (Section 3.5.3).
3. **Tiered restoration**: restore in order: (1) ECLSS -> (2) medical station -> (3) communications and ECC -> (4) shelters -> (5) habitation lighting -> (6) industrial district (thermal preservation only) -> (7) other loads.
4. **Fault diagnostics**: technical support completes fault localization and isolation during UPS hold period.


### 8.6 Emergency Supplies and Equipment Configuration

#### 8.6.1 Base-Wide Emergency Supply List

| Supply Category | Item | Configuration Standard | Storage Location | Replacement Cycle |
|:-----|:-----|:-----|:-----|:-----|
| **Radiation protection** | Emergency radiation vest (>=5 g/cm2) | 1 per person +10% backup | Habitation lockers, airlock exits, rover storage bins | 5 years |
| | Personal dosimeter (0.1 uSv/h-10 Sv/h) | 1 per person | Worn on person | 2 years (battery) |
| | Potassium iodide tablets | 30-day dose per person | Level-I shelters, medical station | 5 years |
| **Medical first aid** | First-aid kit (wound care, hemostasis, analgesic, antimicrobial) | 1 per compartment +1 per rover | Wall-mounted red emergency box | 1 year |
| | AED | 1 per major functional district | Level-I shelters, gym, medical station | 5 years (electrode pads 2 years) |
| | Portable pressurized rescue bag | 2 per airlock +1 per rover | Airlock cabinet, rover cargo bay | 5 years |
| **Firefighting** | CO₂ extinguisher (5 kg, low-g spray-nozzle optimized) | 2 per compartment | Red extinguisher cabinet | 5 years (annual pressure check) |
| | Fine water-mist extinguisher (10 L, low-g nozzle optimized) | 1 per compartment | Same as above | 5 years |
| | Self-contained breathing apparatus (>=30 min, low-g mask adaptation) | 2 sets per compartment | Next to extinguisher cabinet | 5 years (cylinders 3 years) |
| **Leak sealing** | Emergency sealing kit (low-g optimized SPUA thixotropy <=15 s + CFRP patch + inflatable temporary airlock) | 1 per sealed section | Airlock cabinet | 5 years |
| | Emergency oxygen mask (>=30 min, elastic mesh head harness for low-g fit) | >=2 wall-mounted per compartment | On structural wall posts | 5 years |
| **Food and water** | Emergency drinking water (sealed pack with straw, low-g spill-safe) | >=3 L/person | Inside Level-I shelters | 2 years |
| | Emergency food (>=2,000 kcal/person/day, low-g packaging to prevent crumb drift) | >=30 days at rated shelter occupancy | Inside Level-I shelters | 3 years |
| **Communication and positioning** | Personal locator beacon (UHF + inertial navigation) | 1 per person | Worn on person | 2 years (battery) |
| | Emergency hand-crank radio transceiver | 1 per compartment | Emergency supply box | 10 years |

#### 8.6.2 Emergency Rescue Vehicle Configuration

| Vehicle Type | Quantity | Configuration | Parking Location | Response Time |
|:-----|:-----:|:-----|:-----|:-----|
| **Emergency rescue rover (pressurized)** | 2 | Same baseline model as Volume VI Section 6.4.2 pressurized crew rover, plus emergency medical kit, 2 spare PLSS units, 2 radiation vests, 1 emergency sealing kit. Drivers require dedicated low-g braking-distance training | Dedicated apron outside main airlock (>=1 unit on 24-hour standby) | <5 min |
| **Firefighting rover (unpressurized)** | 1 | CO₂ extinguishers x4, fine water-mist extinguishers x2, breathing apparatus x4, hydraulic breaching tools, remote-operation mode | Dedicated industrial-zone apron | <3 min |
| **Material transport rover** | Shared cargo rover fleet | Prioritized for emergency-supply transport to shelters during emergency | - | <10 min |


### 8.7 Post-Disaster Assessment and Recovery

#### 8.7.1 Rapid Post-Disaster Assessment Workflow

1. **Personnel accountability** (<30 min): confirm location and safety status via personal locator beacons and shelter check-in logs.
2. **Structural safety inspection** (<2 h): ERT checks seal integrity (ultrasonic leak detector), structural deformation (laser rangefinder), and residual toxic gases (portable mass spectrometer).
3. **Critical-system status assessment** (<4 h): technical support evaluates damage to ECLSS, power, communications, and thermal-control systems.
4. **Preliminary loss report** (<12 h): signed by Base Commander and transmitted to Earth mission control. Report must include all pre-trigger and concurrent hazard types and warning codes.

#### 8.7.2 Lifeline Restoration Priority Order

| Priority | Restoration Item | Target Time | Notes |
|:---:|:-----|:-----|:-----|
| **1** | Full ECLSS restoration | <24 h | Restore independent ECLSS in Level-I shelters first |
| **2** | Main power backbone restoration | <48 h | Repair faulted ring-bus segment |
| **3** | Communications restoration | <24 h (minimum) / <72 h (full) | Restore Earth emergency link first |
| **4** | Habitation repressurization and thermal restoration | <72 h | Repair sealing layers, repressurize to 70 kPa, restore 20 C |
| **5** | Full medical-station restoration | <7 days | Restore operating room, isolation ward, medicine stock |
| **6** | Industrial restart | As required | Construction-material lines first (for repairs), then metallurgy and CNT |

#### 8.7.3 Long-Term Reconstruction Strategy

- Use local construction-material lines (Volume V Section 5.5) to produce sintered bricks and concrete for repairs.
- Use space-spider robots (scaled model of Main Volume VI Section 6.5) for remote repair in high-risk external zones.
- Implement synchronous "fortification upgrade": raise standards at exposed weak points. If the disaster involved compound hazards, re-evaluate effectiveness of isolation system (Section 8.4.4) under composite scenarios and add firewalls/fire dampers or adjust fire-zone boundaries accordingly.


### 8.8 Training and Drills

#### 8.8.1 Emergency Training for All Personnel

All resident personnel (including short-term visitors) must complete and pass the following training within 72 h of arrival. All hands-on modules are conducted in low-g analog environments (parabolic flight or 1/6 g simulation rigs):

| Training Item | Duration | Content | Assessment Method |
|:-----|:-----|:-----|:-----|
| **Emergency system overview** | 1 h | Six-level warning system (Level I full evacuation to Level VI normal operations), category/warning code recognition, personal locator-beacon use, evacuation routes and shelter locations, highest-level response rule under compound hazards | Online test (pass >=90%) |
| **Emergency oxygen-mask donning** | 0.5 h (including practical) | Low-g mask fitting with elastic mesh harness; target donning time <=30 s | Timed practical assessment |
| **Extinguisher operation** | 1 h (including practical) | Low-g operation essentials for CO₂ and fine mist (aiming, posture stability), electrical-fire vs solid-fire differentiation | Simulated fire suppression |
| **Radiation-protection basics** | 0.5 h | GCR vs SPE, dose limits, potassium iodide administration | Online test |
| **EVA safety basics** (EVA-qualified personnel only) | 2 h (including practical) | Low-g emergency handling for suit breach, PLSS emergency switching, rover emergency braking/evacuation (longer braking distance) | Scenario-based practical evaluation |

#### 8.8.2 Emergency Drills

| Drill Type | Frequency | Participants | Applicable Warning Levels | Special Requirement |
|:-----|:-----|:-----|:-----|:-----|
| **Level-I full evacuation drill** | Once per quarter | Entire base personnel | I-AS / I-BL | Includes low-g evacuation gait |
| **Level-II district evacuation drill** | Once per quarter (alternating with Level I) | Designated district personnel | II-BS / II-BH / II-DC | - |
| **Level-III EVA rescue drill** | Once per month | ERT + designated EVA personnel | III-CE | Completed in low-g simulation environment |
| **ERT comprehensive special drill** | Once per month | ERT members | II/III/IV | Includes portable rescue bag deployment, leak sealing, low-g extinguisher operation |
| **Compound-hazard tabletop exercise** | Once every six months | Base Commander + department heads | All levels | Composite scenario (e.g., moonquake + depressurization + fire) to test ECC highest-level decision logic |
| **Tabletop exercise** | Once every two months | Base Commander + department heads | All levels | - |
| **Full-system black-start drill** | Once per year | Technical support + ERT | I-BL | - |


### 8.9 Pending Validation Items and Pass Criteria

| ID | Item | Validation Method | Success Criterion | Related Volume |
|:-----|:-----|:-----|:-----|:-----|
| **P1-E1** | SPE warning timeliness verification | Continuous operation of lunar particle detectors for >=12 months with cross-validation against Earth GOES data [1][2] | >100 MeV proton-event warning lead time >=30 min, zero false alarms | Volume I (P0-M1) |
| **P1-E2** | >=30-day fully closed survival validation for Level-I storm shelters | Ground analog shelter closed-stay test with 4-6 crew for 30 continuous days | All crew in good health; ECLSS unplanned shutdowns = 0; CO₂ partial pressure <=0.5 kPa; water recovery >=98% | Volume VII (P1-H1) |
| **P2-E1** | Vacuum-environment effectiveness of emergency sealing kit | 1:1 hull mockup section in vacuum chamber under 70 kPa differential, including low-g surface-tension analog | SPUA initial set within <=15 s; post-composite leak rate <=0.5%/day | Volume VII (P1-M4) |
| **P2-E2** | Portable pressurized rescue-bag deployment reliability | Low-g analog EVA rescue tests in vacuum chamber, full procedure by suited test personnel | Full procedure <=90 s; bag pressure stable >=30 kPa pure O2 for >30 min | Volume I (P0-M6) |
| **P2-E3** | Lava-tube microseismic warning effectiveness | Distributed fiber + microseismometer deployment over selected section for >=6 months, covering homogeneous and layered roofs [11][12] | Detection rate >=95% for >M1.0 moonquakes; strain-anomaly warning lead time >=2 h | Volume II (Siting) |
| **P2-E4** | Firewall fire-resistance validation | 1:1 firewall sample tested under ISO 834-1 heating curve | Fire-resistance limit >=120 min; unexposed-face temperature <=180 C | This volume |
| **P3-E1** | Level-I full-evacuation drill timeliness | Trigger unannounced Level-I red warning | Time from warning to last person arriving at shelter <=5 min; locator-beacon online rate 100% | This volume |
| **P3-E2** | Level-II district-evacuation drill timeliness | Trigger unannounced Level-II red warning | Full district safe arrival at shelters <=3 min | This volume |
| **P3-E3** | ECC compound-hazard decision drill | Tabletop scenario with concurrent SPE (I-AS) + fire (II-BH) + EVA accident (III-CE) | ECC correctly determines highest level (Level I) and issues unified command within <60 s | This volume |


### 8.10 Parameter Outputs

| Parameter | Value | Status | Receiving Volume |
|:---|:---|:---|:---|
| SPE warning lead time (>100 MeV) | >=30 min | Design target | Volume I |
| Level-I storm-shelter sustainment time | >=30 days | P1 pending validation | Volume VII |
| Level-I storm-shelter radiation attenuation | >=99.9% | Design baseline | Volume II |
| Level-II shelter density | >=1 shelter per major functional district | Design baseline | Volume II |
| Firewall fire-resistance limit | >=120 min | P2 pending validation | This volume |
| Airtight isolation-door closure time | <=5 s | Design baseline | This volume |
| Fire-damper fusible closure time | <=10 s | Design baseline | This volume |
| Negative-pressure gradient establishment time | <=60 s | Design baseline | This volume |
| Emergency oxygen-mask donning time | <=30 s | Training assessment standard | This volume |
| ERT dispatch time (inside base) | <=3 min | Design baseline | This volume |
| ERT dispatch time (EVA rescue) | <=5 min | Design baseline | This volume |
| Level-I full-evacuation time | <=5 min | Design target | This volume |
| Level-II district-evacuation time | <=3 min | Design target | This volume |
| Black-start restoration time (ECLSS) | <24 h | Design target | Volume III |
| Post-sealing leak rate of emergency kit | <=0.5%/day | P2 pending validation | Volume VII |
| Sealing-agent thixotropic time (low-g optimized) | <=15 s | P2 pending validation | This volume |
| Portable rescue-bag deployment time | <=90 s | P2 pending validation | Volume I |
| Full-evacuation drill frequency | Once per quarter (Level I/II alternating) | Policy requirement | This volume |
| ERT comprehensive special-drill frequency | Once per month | Policy requirement | This volume |
| Full-system black-start drill frequency | Once per year | Policy requirement | This volume |
| Compound-hazard tabletop frequency | Once every six months | Policy requirement | This volume |


### 8.11 Conclusion of Volume VIII

This volume completes systematic planning for lunar-base emergency protection and rescue, turning the Main Volume XII survival philosophy, "the ring may break, civilization must survive," into executable engineering and operational procedures. Core contributions:

1. **A dual-layer framework of category coding and six-level risk evaluation is established, with highest-level response as the governing rule for compound hazards.** Category coding (A/B/C/D with internal codes) is seamlessly coupled with six warning levels through the "Level-Category Code" format. When multiple hazards are triggered, response is unified at the highest involved level, preventing command conflicts.
2. **End-to-end SOPs for all six warning levels are fully defined and systematically low-g adapted.** Representative workflows are provided for I-AS (SPE full evacuation), II-BS (district evacuation due to depressurization), II-BH (district fire evacuation with optional vacuum extinguishing), and III-CE (individual EVA rescue). All facilities, equipment, supplies, and procedures include low-g impact annotations and adaptation measures, from extinguisher nozzle optimization to sealing-agent thixotropic timing, from portable rescue-bag deployment to evacuation-time estimation.
3. **A three-layer disaster isolation system is established.** Airtight isolation doors (active isolation, <5 s closure), firewalls/fire panels (passive isolation, >=120 min fire resistance with duct fire dampers), and negative-pressure gradients (active isolation, <60 s establishment) form three defensive lines against spread of fire, leaks, and depressurization.
4. **A three-tier shelter system is defined, with explicit sheltering strategy under compound hazards.** Level-I storm shelters (>=30-day sustainment, SPE attenuation >=99.9%), Level-II multi-purpose emergency shelters (>=7-day sustainment), and Level-III shelter-in-place zones use protection parameters designed against historical major SPE data.
5. **Latest space-safety research is integrated.** The volume incorporates authoritative references including SEP forecasting reviews, lava-tube collapse probability assessment, low-g fire-behavior studies, and NASA SAFFIRE in-orbit fire experiments.
6. **A normalized training and drill regime is established.** Includes 72-hour all-personnel emergency training (with low-g practical modules), quarterly evacuation drills, monthly ERT special drills, annual black-start drill, and semiannual compound-hazard tabletop exercises.


### 8.12 Alignment with Main Volume XII

This volume applies the Main Volume XII "three-layer disaster framework" (passive survivability design -> active emergency response -> rapid post-disaster restoration) to the lunar-base context. Specifically:

- The disaster isolation system (airtight doors + firewalls + negative-pressure gradients) and physical shelter redundancy correspond to Main Volume concepts of "firewalls" and "lifeline fortress".
- The six-level warning system (including highest-level principle for compound hazards) and rapid ERT response correspond to "active emergency response".
- Post-disaster restoration priority and long-term reconstruction strategy correspond to "lifeline engineering".

The key distinction between lunar bases and the space ring is that lunar bases have gravity, ground infrastructure, and local resources, providing stronger post-disaster resilience. The base also has a unique method unavailable to the ring: controlled depressurization extinguishing using lunar vacuum. However, the base cannot limit loss by mechanical breakpoints as the ring can. Therefore, this volume emphasizes three-layer disaster isolation and Level-I storm shelters as fully independent "base-within-a-base" survival units. Their coordination defines the lower survival bound of lunar-base civilization.


### References

[1] Papaioannou, A., Strauss, R. D., Lario, D., et al. Predicting Solar Energetic Particles: Solar Storm Watch - Preparing for Space Odyssey. *Space Science Reviews*, 2025, 221(6): 82.

[2] Whitman, K., Egeland, R., Richardson, I. G., et al. Review of Solar Energetic Particle Prediction Models. *Advances in Space Research*, 2023, 72(12): 5161-5242.

[3] Georgoulis, M. K., et al. Prediction of solar energetic events impacting space weather conditions. *Advances in Space Research*, 2024.

[4] Pak, S., Cucinotta, F. A. Organ dose equivalents of albedo protons and neutrons under exposure to large solar particle events during lunar human landing missions. *Life Sciences in Space Research*, 2024.

[5] Allen, C. S., et al. Moon Mission (Chapter 4.3.3.4). In: *Space Safety and Human Performance*. 2018.

[6] Sohn, C.-H., Son, Y.-J. Fire Prevention, Detection, and Suppression in Crewed Exploration Spacecraft. *Journal of the Korean Society of Propulsion Engineers*, 2007, 11(3): 65-72.

[7] Legros, G., et al. (ESA). No fire in the sky: preventing an astronaut's worst nightmare. *ESA Enabling Support*, 2021.

[8] George, S., et al. Deep Space Radiation Measurements and Crew Radiation Protection for the NASA Artemis Program. NASA Johnson Space Center, 2025.

[9] Zarzour, O. A., et al. Stability and form-finding of shelters subjected to moonquakes of the lunar south polar region. *Acta Astronautica*, 2025, 234: 106-116.

[10] Watters, T. R., Schmerr, N. C., et al. Paleoseismic activity in the moon's Taurus-Littrow valley. *Science Advances*, 2025.

[11] Chwala, M., Gorniak, K. Probabilistic characterization of lunar lava tube collapses. *Geoscience Frontiers*, 2025, 16(4): 102076.

[12] Chwala, M., Gorniak, K. Effects of layered roof for stability and exploration of lunar lava tubes. *Earth and Planetary Science Letters*, 2024.

[13] UL Standards & Engagement. *UL 94 - Standard for Tests for Flammability of Plastic Materials for Parts in Devices and Appliances*.

[14] Ruff, G. A., Urban, D. L., et al. SAFFIRE: An Overview and Status. AIAA 2015-0939, 2015.

# Appendix 2: Stratospheric Platform

## Volume 3: High-Altitude Operations and Cable Maintenance

**Version**: 1.3<br/>
**Date**: June 2026<br/>
**Currency**: Chinese Yuan (RMB), symbol: ¥<br/>
**Related Main Volumes**: Main Volume IV, V, VII<br/>
**Prerequisites**: Volume 1 and Volume 2 of this Appendix


### Abbreviations

| Abbreviation | Full Name | Description |
|------|----------|------|
| C/SiC | Carbon-fiber-reinforced silicon carbide composite | Material for inter-segment cable connectors |
| CFRP | Carbon Fiber Reinforced Polymer | Structural material for maintenance tools and emergency equipment |
| FOG | Fiber Optic Gyroscope | Core angular-rate sensor in the pod inertial navigation system |
| Inconel | Nickel-chromium alloy | Material for cable connector bolts |
| MLI | Multi-Layer Insulation | Passive thermal control storage for replacement spare parts |
| MoS₂ | Molybdenum disulfide | Solid lubricant for moving parts in high-altitude low-pressure environments |
| PTFE | Polytetrafluoroethylene | Sealing material; low friction coefficient, vacuum-compatible over a wide temperature range |
| UHMWPE | Ultra-High Molecular Weight Polyethylene | Replacement material for the outer layer of the track sleeve |


### 3.1 Preface

This volume serves as the **high-altitude maintenance, repair, and rescue operations manual for the ring-elevator cable** within the stratospheric platform system, focused on answering the following core questions:

> Once the ring-elevator cable is constructed and operational, how does the stratospheric platform—serving as a high-altitude operations base—perform routine inspections and scheduled maintenance on the cable and track sleeves? How is the worn outer UHMWPE layer of the track sleeve replaced? How is wear on the rack tooth surface repaired when the wear depth reaches the alert threshold? How is inert gas replenished when the leak rate of a sealed segment exceeds the threshold? When an elevator car becomes trapped in the 0–100 km altitude range due to gear seizure or power interruption, how does the stratospheric platform dispatch a work pod to safely rescue the trapped occupants?

Scope note: Maintenance of the stratospheric platform itself (the aerostat and its mooring cable) has been functionally outlined in Volume 1 (industrial pods can travel along the platform's own mooring cable at 20–50 km altitude); the specific maintenance tool configuration may be adapted from the inspection and maintenance tool list in this volume and is not separately detailed here. The maintenance, repair, and rescue operations in this volume are focused entirely on the ring-elevator cable and elevator cars—this is the core service function of the stratospheric platform after the ring-elevator becomes operational, and represents an independent and irreplaceable strategic role within the entire stratospheric platform system.

This volume builds upon:
- **Volume 1 (Platform Overall Design)**: Key parameters already established—work pod positioning accuracy (±10 cm), payload capacity (≥300 kg), four-level stabilization mechanism.
- **Volume 2 (Energy and Positioning Systems)**: Pod independent battery capacity (50 kWh, endurance 6–10 h), full-altitude positioning accuracy (±5 m below 40 km; ±1 mm vertical / ±1 km/h horizontal above 40 km).

Core tasks of this volume:

1. Design the routine inspection scheme for the ring-elevator cable—inspection cycle, check items, sensor configuration, automated data downlink and anomaly flagging. Operating range covers the full length of the ring-elevator cable (0–100 km altitude).
2. Plan preventive maintenance tools and procedures—outer UHMWPE track sleeve replacement, rack tooth surface wear detection and repair, C/SiC connector bolt re-tightening, sealed-segment inert gas replenishment.
3. Establish emergency repair operating procedures—replacement of spare gear/rack segments, use of car towing attachments, and precautions for cutting and welding tools in low-pressure environments.
4. Define complete personnel rescue procedures—pod-to-stalled-car docking, safe transfer of trapped occupants, activation and ground recovery of the lightweight escape capsule.
5. Compile a complete list of all tools and instruments carried by the work pod, with mass, power consumption, and replacement interval for each tool.
6. Output key parameters for use by Volume 8 (Deployment and Maintenance) and Volume 10 (Technical Interfaces).


### 3.2 Routine Inspection Equipment and Scheme

**（a）Inspection Cycle and Check Items**

The work pod performs routine inspections along the ring-elevator cable, covering the full length of the cable (0–100 km altitude range). The pod uses a rack-and-pinion drive—the pinion on the pod meshes with the aluminium-alloy rack (module 20 mm, tooth width 300 mm, sharing the same track interface as the ring-elevator car) in the middle layer of the ring-elevator track sleeve, draws power directly from the track sleeve's power rail, and climbs along the cable over the full altitude range. Inspection cycles and check items are as follows:

| Inspection Cycle | Check Item | Sensor / Tool | Check Content |
|:---|:---|:---|:---|
| **Daily** (automated) | Cable tension distribution | Distributed fiber optic strain sensor (embedded in the load-bearing layer of the ring-elevator cable) | Whether tension in each segment is within the design range; whether local overload or slack exists |
| | Track sleeve outer layer condition | High-resolution multispectral camera (visible + infrared, resolution ≤1 mm/pixel at 100 m distance) [1] | Whether the outer UHMWPE layer has cracks, delamination, abnormal wear, or impact damage |
| **Weekly** (pod patrol) | Rack tooth surface wear | Laser profile scanner (accuracy ±5 μm) [2] | Segment-by-segment scan of tooth surface wear depth; comparison with previous measurement data; flagging of segments where wear rate exceeds the limit |
| | Sealed-segment inert gas pressure | Ultrasonic leak detector (sensitivity ≤1 cm³/s at 70 kPa pressure differential) [3] | Whether internal pressure in each sealed segment is within the design range; whether micro-leaks exist |
| | Cable connection nodes | High-resolution camera + laser rangefinder | Whether C/SiC connector flanges show signs of abnormal displacement, surface cracking, or bolt loosening |
| **Monthly** (pod patrol) | Power rail insulation condition | Partial discharge detector (sensitivity ≤10 pC) [4] | Whether the UHMWPE insulation layer of the power rail shows surface discharge traces or insulation degradation |
| | Thrust ring displacement | Laser rangefinder (accuracy ±0.1 mm) | Whether the deviation between the actual position and design position of each thrust ring is within the allowable range |

**（b）Automated Data Downlink and Anomaly Flagging**

Inspection data is relayed in real time via fiber optics embedded in the ring-elevator cable to the aerostat's communication system, then transmitted to the ground control center via Ka/Ku-band antennas. The automated data processing system performs the following analyses on all inspection data:

- **Trend analysis**: Time-series comparison of repeated laser profile scan data at the same location; calculation of wear rate (μm/month). When the wear rate exceeds the alert threshold (80% of the design value), the segment is automatically flagged as "scheduled for replacement."
- **Anomaly detection**: Ultrasonic leak detection data is compared against the historical baseline; when the leak rate exceeds twice the design value, a "sealed segment leak warning" is automatically triggered.
- **Automated report generation**: After each pod patrol, an inspection report is automatically generated containing the pass/warning/anomaly status for each check item, wear trend curves, and a list of items to be addressed in the next scheduled maintenance.

**（c）Inspection Coverage and Cycle Optimization**

The pod's maximum climbing speed is 5 m/s (unloaded / not performing inspection tasks). When carrying the full inspection equipment suite and stopping at each checkpoint to perform measurements, the average inspection speed is approximately 2 m/s (including dwell time). A single traverse of the full 100 km cable takes approximately 14 hours; a complete round trip (downward + upward, including dwell time at all checkpoints) takes approximately 40 hours. One pod patrol per week can cover a complete inspection of the entire cable.


### 3.3 Preventive Maintenance Tools and Procedures

**（a）Replacement of Outer UHMWPE Track Sleeve Layer**

The outer UHMWPE layer of the track sleeve is a consumable sacrificial layer with a designed replacement interval of 1–3 years. Replacement is performed by the work pod using dedicated replacement tooling.

| Parameter | Design Value | Description |
|:---|:---|:---|
| Replacement tool type | Integrated hot-melt welding and stripping tool arm | Mounted on the pod mechanical arm, mass ≤30 kg |
| New UHMWPE roll material | Width 300 mm, thickness 20 mm (ground end) → 5.6 mm (GEO end), roll length ≥200 m | Pre-stored in the aerostat's maintenance supply depot, carried by the pod |
| Stripping method | Thermal knife cutting + mechanical stripping | Worn layer stripped face by face along the regular octagonal outer surface of the track sleeve |
| Welding method | Hot-air welding (temperature 220–260°C, controllable), weld strength ≥80% of base material [5] | UHMWPE hot-air welding at low pressure requires adjustment of welding temperature and airflow speed to compensate for reduced convective heat dissipation |
| Single-pass replacement speed | ≈0.5 m/min | Includes stripping, surface cleaning, laying new roll, and welding |
| Replacement operation power | Approx. 3 kW (welding heat gun + stripping motor + mechanical arm) | Powered by the pod's independent battery or the ring-elevator cable power rail |

Replacement procedure:
1. The pod positions itself along the cable at the segment to be replaced and activates the multi-cable guidance stabilization mechanism.
2. The thermal knife on the tool arm cuts a longitudinal stripping groove along the outer layer of the track sleeve; a mechanical stripping roller then strips the worn layer segment by segment and winds it onto a waste recovery reel.
3. After stripping, the laser profile scanner confirms that the middle-layer aluminium alloy surface is free of cracks or damage. Any minor damage is repaired with a handheld micro-arc oxidation repair pen.
4. The new UHMWPE roll is unwound from the spool, laid on the cleaned aluminium alloy surface, and the hot-air welding tool welds the longitudinal seams segment by segment.
5. After welding, the laser profile scanner re-checks the flatness of the outer surface (deviation ≤0.5 mm).

**（b）Rack Tooth Surface Wear Detection and Repair**

When the rack tooth surface wear depth reaches the alert threshold (10% of the tooth tip thickness, approximately 2.7 mm), the rack segment must be replaced. The rack is a modular segmented design (single segment length 5–10 m); only the damaged segment is replaced.

| Parameter | Design Value | Description |
|:---|:---|:---|
| Detection tool | Laser profile scanner (accuracy ±5 μm) [2] | Segment-by-segment scanning of tooth surface; comparison with design tooth profile; calculation of wear depth |
| Replacement tool | Portable bolt removal/installation gun (Inconel M24 bolts, rated torque) + rack segment hoisting clamp | Both tools mounted on the pod mechanical arm |
| Spare parts storage | 1 spare segment per 5 rack segments, stored in the aerostat maintenance supply depot | Single-segment mass approx. 80–150 kg (including aluminium alloy rack + middle-layer track sleeve connectors) |
| Replacement speed | ≈1 h/segment | Includes bolt removal, old segment removal, new segment alignment, and bolt tightening |
| Bolt preload torque | 500 kN (single M24 Inconel bolt) [6] | Consistent with the inter-segment connection node design requirements in Main Volume VI, Section 6.6.2 |
| Post-replacement acceptance | Laser profile scanner verifies gear tooth accuracy; pod performs a test run on the segment to check meshing smoothness | — |

Replacement procedure:
1. The pod positions itself at the rack segment to be replaced; all four levels of the stabilization mechanism are activated (in high-wind conditions).
2. Remove the Inconel bolts from the C/SiC flanges on both sides of the old rack segment (24 bolts per side); bolts are collected for reuse.
3. The old rack segment is gripped and removed by the pod's tool arm and temporarily stored on the pod's cargo shelf.
4. The new rack segment is carried by the pod from the aerostat to the work site; the flanges are aligned and all bolts are tightened in two steps at 50% → 100% preload (cross-symmetric sequence).
5. After bolt tightening, the laser profile scanner checks the straightness of the cable on both sides of the node (angular deviation <0.05°).
6. The pod performs two round-trip test runs on the segment and confirms smooth meshing before completing the replacement.

**（c）C/SiC Connector Bolt Re-tightening**

Inconel bolts on the C/SiC composite flanges between cable segments may loosen under prolonged thermal cycling and tension fluctuations (Main Volume VII pending verification item P2-M4) and must be periodically re-tightened.

| Parameter | Design Value | Description |
|:---|:---|:---|
| Detection tool | Ultrasonic bolt stress gauge [7] | Non-contact measurement of bolt axial stress to determine whether preload has degraded |
| Re-tightening tool | Bolt removal/installation gun (same as rack replacement tool) | — |
| Re-tightening interval | Full inspection once every 5 years | Re-tighten immediately if ultrasonic measurement indicates preload degradation >20% |
| Re-tightening speed | ≈5 min/node | Bolts are not replaced, only re-tightened |

**（d）Sealed Segment Inert Gas Replenishment**

The low-altitude rack of the ring-elevator cable is sealed in dry nitrogen to suppress oxidative wear (Main Volume V, V5-N5). The design annual leak rate for sealed segments is ≤5%; periodic inspection and replenishment of inert gas is required.

| Parameter | Design Value | Description |
|:---|:---|:---|
| Detection tool | Ultrasonic leak detector (sensitivity ≤1 cm³/s at 70 kPa pressure differential) [3] | Scan all interfaces and walls of the sealed segment to locate leak points |
| Replenishment tool | Portable high-pressure nitrogen cylinder (volume ≥50 L, storage pressure ≥20 MPa) + flow control valve | Single cylinder mass ≤80 kg (including carbon-fiber-wound cylinder + MLI insulation) |
| Replenishment interval | Once per year (replenishment consolidated after full-cable inspection) | Shorten to every 6 months if leak rate exceeds expectations |
| Replenishment speed | ≈10 min/sealed segment | Including cylinder replacement and pipeline connection time |

Replenishment procedure:
1. The pod carries high-pressure nitrogen cylinders and inspects sealed segments sequentially along the cable.
2. The ultrasonic leak detector scans each sealed segment—if the leak rate is within the design range, data is recorded without replenishment; if it exceeds the design value, the leak point is located and flagged as "scheduled for repair."
3. For sealed segments requiring replenishment, connect the replenishment pipeline to the gas injection port of the sealed segment, open the flow control valve, restore the internal pressure to the design value, then close the valve and disconnect the pipeline.


### 3.4 Emergency Repair Capabilities and Procedures

**（a）Emergency Repair Kit**

When the pod cannot immediately replace a damaged rack segment or outer track sleeve layer, the emergency repair kit can complete preliminary sealing or temporary repair within tens of minutes, buying time for subsequent scheduled replacement.

| Kit Contents | Purpose | Mass |
|:---|:---|:---:|
| SPUA rapid-spray sealant (two-component, thixotropic ≤15 s) [8] | Rapid sealing of small-area damage to the outer track sleeve layer | ≤10 kg (including spray gun and 2 sets of sealant canisters) |
| CFRP patches (multiple standard sizes) | Applied over SPUA sealant to provide structural strength | ≤20 kg (including epoxy resin adhesive and curing agent) |
| Aluminium foil butyl tape (width 100 mm) | Temporary sealing of micro-cracks in sealed segment walls | ≤5 kg (including 10 rolls) |
| Portable micro-arc oxidation repair pen [9] | On-site repair of minor damage to rack tooth surfaces or middle-layer aluminium alloy surfaces of track sleeves | ≤5 kg (including electrolyte and power adapter) |

**（b）Replacement Procedure for Spare Gear/Rack Segments**

If the pod's own gears fail due to wear or damage, they can be replaced while the pod is docked with the aerostat. The aerostat's maintenance supply depot stores ≥2 spare gear sets (8 pairs per set); replacing one set takes approximately 4 hours. The replacement procedure follows the gear-rack drive mechanical interface standard in Volume 1, Section 1.4(a)—pinion pitch circle diameter 0.5 m, fully compatible with rack module 20 mm / pressure angle 20° / tooth width 300 mm.

**（c）Car Towing Attachment**

After the work pod is fitted with a car towing arm, it can tow an elevator car trapped due to gear seizure or power interruption to the platform or a safe altitude. Maximum towing force 50 kN, powered by the pod's main battery, operation time ≤2 hours. The towing procedure is described in Section 3.5 (Personnel Rescue Procedure).

**（d）Operation of Cutting and Welding Tools in Low-Pressure Environments**

The effects of the stratospheric low-pressure environment (0.1–0.01 atm) on cutting and welding processes have been extensively studied in the literature [10][11]. Electron beam welding and laser welding do not rely on shielding gas and achieve weld quality comparable to ground level in this environment. This scheme uses a handheld laser welding tool (power 2–5 kW, mass ≤40 kg), powered by the pod's independent battery, used only for localized repair of middle-layer aluminium alloy track sleeves or C/SiC connectors. The cutting tool is a miniature plasma cutting pen (power 1–3 kW), used to dismantle damaged rack segments or track sleeve segments.


### 3.5 Personnel Rescue Procedure and Escape System

**（a）Rescue Scenarios and Trigger Conditions**

When an elevator car operating on the ring-elevator cable becomes trapped in the 0–100 km altitude range due to gear seizure, power interruption, large-scale outer track sleeve delamination, or other mechanical failures, the work pod can be dispatched immediately upon receiving a rescue order. The trigger condition for the rescue procedure is: the car control system issues a distress signal (manual or automatic), and after confirmation by the ring-elevator control center, a rescue order is issued to the stratospheric platform.

Pod dispatch time limit: ≤5 min from receipt of rescue order to departure from the aerostat.

**（b）Pod-to-Stalled-Car Docking Procedure**

1. **Pod dispatch**: The pod descends from the aerostat along the cable to the altitude of the stalled car (can descend from the aerostat's stationed altitude all the way to the ground, or from the 30 km normal station altitude to any failure location). The pod continuously tracks the car's precise position via the inertial navigation system during the climb.

2. **Approach and stabilization**: When the pod reaches approximately 50 m above the stalled car, all four levels of the stabilization mechanism are activated. The pod approaches the top of the car slowly from above at minimum speed (0.5 m/s).

3. **Soft docking**: The docking frame on the pod's underside is slowly lowered and aligned with the emergency hatch on the top of the car. The flexible seal ring on the docking frame (inflatable, material: silicone rubber + PTFE coating) inflates and expands, forming an airtight passage between the pod and the car.

4. **Hard locking**: Four sets of hydraulic locking pins on the docking frame are inserted into the pre-embedded interface plate pin holes on the car roof, locking the relative position of pod and car. Shear load capacity of locking pins ≥50 kN per set (4 sets combined ≥200 kN), sufficient for all loads of the stalled car and occupants during transfer.

**（c）Occupant Transfer and Evacuation**

1. **Opening the emergency hatch**: The pod operator (or ground remote control) uses the mechanical arm to operate the emergency hatch release mechanism on the car roof and opens the hatch. The car interior must already be depressurized to the same air pressure as the pod docking passage (70 kPa oxygen-nitrogen atmosphere).

2. **Occupant transfer**: Trapped occupants pass through the car emergency hatch one by one into the pod docking passage and then into the pod passenger cabin. The pod passenger cabin has an inner diameter ≥2.0 m, can accommodate 4–6 occupants, and is equipped with an independent life support system capable of ≥24 h (oxygen, water, CO₂ scrubbing).

3. **Separation from the car**: After occupant transfer is complete, the hydraulic locking pins are unlocked and the pod rises slowly away from the car. The pod operator uses the mechanical arm to re-close the car emergency hatch (not locked, to allow subsequent maintenance personnel to enter).

**（d）Return Path Selection**

| Scenario | Return Path |
|:---|:---|
| Pod passenger cabin fully loaded and occupants in good health | Pod climbs up the cable back to the aerostat; occupants wait inside the aerostat for subsequent transfer |
| Pod fully loaded but occupant(s) urgently requiring medical treatment | Pod descends along the cable to the ground (if the trapped car is below 40 km and ground weather conditions permit) |
| Pod itself malfunctions (e.g., gear seizure) | Pod activates emergency braking system to lock in current position and waits for another pod (or ground rescue team) to arrive |

**（e）Lightweight Escape Capsule**

In the extreme scenario where the pod itself cannot safely return to the aerostat, trapped occupants can transfer into the lightweight escape capsule carried by the pod and return to the ground directly from altitude. The escape capsule shares its technical design with the car escape capsule in the "Total Evacuation" protocol of Main Volume XII, Section 8.3.4.

| Parameter | Design Value | Description |
|:---|:---|:---|
| Capacity | 4–6 persons | — |
| Total mass (fully loaded) | ≤600 kg | Including escape capsule structure, life support system, parachute, and inflatable heat shield |
| Capsule structure | CFRP frame + multi-layer insulation + inflatable thermal protection cover (deployed during reentry) | Shares heat shield technology with the "Doomsday Rescue Capsule" in Main Volume XII, Section 12.4.2 |
| Reentry mode | Ballistic reentry + parachute recovery | After release from any altitude, the inflatable heat shield deploys for aerodynamic deceleration; parachute deploys at 10–20 km altitude; splashdown in a designated sea area |
| Independent life support | ≥24 h | Including oxygen, water, CO₂ scrubbing, and first-aid medicine kit |


### 3.6 Parameter Output

| Parameter | Value | Status | Receiving Volume |
|:---|:---|:---|:---|
| Pod maximum payload | ≥300 kg | Design baseline | Volume 1 |
| Pod positioning accuracy | ±10 cm | Design baseline | Volume 1 |
| Pod independent endurance | 6–10 h (50 kWh battery) | Design baseline | Volume 2 |
| Cable full-length inspection coverage | 0–100 km (full ring-elevator cable) | Design baseline | — |
| Inspection cycle (full inspection) | Once per week (pod patrol) | Design baseline | Volume 8 (Maintenance Plan) |
| Pod maximum climbing speed | 5 m/s (unloaded) | Design baseline | — |
| Pod average inspection speed | ≈2 m/s (including dwell time) | Design baseline | — |
| Track sleeve outer UHMWPE replacement speed | ≈0.5 m/min | Design baseline | — |
| Track sleeve outer layer replacement tool power | ≈3 kW | Design baseline | Volume 2 (Energy Budget) |
| Rack segment replacement speed | ≈1 h/segment | Design baseline | — |
| Rack segment spare parts storage | 1 spare per 5 segments (single segment mass 80–150 kg) | Design baseline | — |
| Sealed segment inert gas replenishment interval | Once per year (consolidated after full-cable inspection) | Design baseline | — |
| C/SiC bolt re-tightening interval | Full inspection once every 5 years | Design baseline | — |
| Bolt preload torque | 500 kN (single M24 Inconel bolt) | Design baseline | — |
| Personnel rescue pod dispatch time limit | ≤5 min (after receiving order) | Design baseline | — |
| Escape capsule capacity | 4–6 persons | Design baseline | — |
| Escape capsule total mass (fully loaded) | ≤600 kg | Design baseline | — |
| Escape capsule independent life support | ≥24 h | Design baseline | — |


### 3.7 Volume 3 Conclusion

This volume completes the full design of the stratospheric platform's high-altitude maintenance, repair, and rescue operations system for the ring-elevator cable. Core contributions:

1. **Established a three-tier maintenance system**—daily automated inspection (distributed fiber optics + multispectral cameras), weekly pod patrols (tooth surface wear + seal inspection + connection node check), and scheduled preventive maintenance (outer track sleeve replacement, rack segment replacement, bolt re-tightening, inert gas replenishment). The three tiers complement each other in coverage and response timeliness, with operational scope covering the full ring-elevator cable (0–100 km).

2. **Provided engineering parameters for all maintenance tools**—from the UHMWPE hot-melt welding tool (≤30 kg, ≈3 kW) to the rack segment replacement tool (portable bolt gun + hoisting clamp); mass, power consumption, and replacement speed for each tool are quantified to an order-of-magnitude level, usable for the subsequent Volume 8 deployment/maintenance plan and Volume 2 energy budget.

3. **Designed a complete elevator car personnel rescue procedure**—from pod dispatch, docking, and occupant transfer to evacuation and return, covering all possible scenarios (return to aerostat, descent to ground, wait in place for rescue). The lightweight escape capsule shares its technical design with the "Doomsday Rescue Capsule" in Main Volume XII, ensuring personnel can safely return from any altitude in extreme circumstances.

4. **Clarified the functional scope of this volume**—routine maintenance of the stratospheric platform itself (aerostat and platform cable) is handled by the industrial pod outlined in Volume 1; the specific maintenance tools can be adapted from the tool list in this volume. The maintenance operations in this volume are focused entirely on the ring-elevator cable and elevator cars—this is the core service function of the stratospheric platform after the ring-elevator becomes operational, and is the irreplaceable strategic role of the entire stratospheric platform system. Structural safety of the platform itself (envelope damage, mooring cable failure, high-altitude fire, etc.) falls within the purview of Volume 7.


### References

[1] Gao, J., et al. A review of multi-spectral imaging for remote sensing applications. *International Journal of Remote Sensing*, 2018.

[2] Gühring, J. Laser triangulation for precision surface profiling. *Measurement Science and Technology*, 2003.

[3] Murashov, V. V. Ultrasonic detection and evaluation of leaks in pressurized systems. *Russian Journal of Nondestructive Testing*, 2014.

[4] IEEE. *IEEE Std 1434-2014 – IEEE Guide for the Measurement of Partial Discharges in AC Electric Machinery*. 2014.

[5] Balkan, O., Demirer, H., & Ezdeşir, A. Effects of welding procedures on mechanical and morphological properties of hot gas butt welded PE, PP, and PVC sheets. *Polymer Engineering & Science*, 2008.

[6] SAE International. *SAE AMS 5662M – Nickel Alloy, Corrosion and Heat-Resistant, Bars, Forgings, and Rings 52.5Ni – 19Cr – 3.0Mo – 5.1Cb (Nb) – 0.90Ti – 0.50Al – 18Fe Consumable Electrode Remelted or Vacuum Induction Melted 1775°F (968°C) Solution Heat Treated*. 2019.

[7] Svilainis, L., Dumbrava, V., & Kitov, S. Ultrasonic measurement of axial stress in bolts. *Ultragarsas*, 2006.

[8] Primeaux, D. J. Polyurea spray coating technology. In: *Protective Coatings*, 2017.

[9] Yerokhin, A. L., Nie, X., Leyland, A., Matthews, A., & Dowey, S. J. Plasma electrolysis for surface engineering. *Surface and Coatings Technology*, 1999.

[10] Russell, T. F., & King, J. F. Electron beam welding in reduced pressure environments. *Welding Journal*, 2000.

[11] Katayama, S., Kawahito, Y., & Mizutani, M. Elucidation of laser welding phenomena in low pressure and vacuum. *Journal of Laser Applications*, 2010.

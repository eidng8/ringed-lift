# Appendix 2: Stratospheric Platform

## Volume 4: Research and Development Platform

**Version**: 1.2<br/>
**Date**: June 2026<br/>
**Currency**: Chinese Yuan (RMB), symbol: ¥<br/>
**Related Main Volumes**: Main Volume IV, V, VII<br/>
**Prerequisites**: Volume 1 and Volume 2 of this Appendix


### Abbreviations

| Abbreviation | Full Name | Description |
|------|----------|------|
| AM0 | Air Mass Zero | Extra-terrestrial solar spectral standard |
| CFRP | Carbon Fiber Reinforced Polymer | Structural material for experimental equipment and scale models |
| CIGS | Copper Indium Gallium Selenide | Thin-film solar cell material |
| CNT | Carbon Nanotube | Core material for the scaled-down cable |
| FOG | Fiber Optic Gyroscope | Core angular-rate sensor in the pod inertial navigation system |
| GaAs | Gallium Arsenide | Multi-junction photovoltaic cell material |
| GaInP | Gallium Indium Phosphide | Top-junction material in multi-junction photovoltaic cells |
| MLI | Multi-Layer Insulation | Passive thermal control for experimental samples |
| MoS₂ | Molybdenum disulfide | Solid lubricant for moving parts in high-altitude low-pressure environments |
| PTFE | Polytetrafluoroethylene | Sealing material; low friction coefficient, vacuum-compatible over a wide temperature range |
| UHMWPE | Ultra-High Molecular Weight Polyethylene | Outer layer material of the scaled-down track sleeve |


### 4.1 Preface

This volume serves as the **research and development platform centered on scale-model validation of the Ring-Lift project** within the stratospheric platform system, focused on answering the following core questions:

> Before the Ring-Lift project is formally constructed, which P0-level pending verification items can be tested on the stratospheric platform in a real high-altitude environment using scaled-down models? How can a section of scaled-down CNT cable several hundred meters long be suspended beneath the aerostat so that a scaled-down pod can run back and forth on it to measure rack-and-pinion meshing efficiency, track sleeve wear rate, power transmission link atmospheric attenuation, sealed-segment inert gas protection effectiveness, and cable vortex-induced vibration amplitude? What measurement equipment is needed? What data can be produced to support the finalization of the Ring-Lift project design? Beyond the Ring-Lift scale experiments, what independent scientific experiments can the stratospheric platform—as a long-term high-altitude stationed facility—host, from atmospheric science to material exposure, from high-altitude biological culture to novel photovoltaic and communications technology validation?

This volume builds upon:
- **Volume 1 (Platform Overall Design)**: Key parameters already established—aerostat nominal altitude range (25–35 km), work pod payload capacity (≥300 kg), positioning accuracy (±10 cm), and four-level stabilization mechanism.
- **Volume 2 (Energy and Positioning Systems)**: Pod independent battery capacity (50 kWh, endurance 6–10 h), full-altitude positioning accuracy, and the interface scheme for drawing power from the ring-elevator power rail.
- **Volume 3 (High-Altitude Operations and Cable Maintenance)**: Rack-and-pinion drive scheme for pod climbing along the cable (module 20 mm, tooth width 300 mm).

Core tasks of this volume:

1. Establish the strategic role of the stratospheric platform as the "high-altitude test bench" of the Ring-Lift project—before formal construction of the ring-elevator, use the aerostat to suspend a scaled-down CNT cable and operate a scaled-down pod in a real atmospheric environment to provide real-environment measured data for Ring-Lift P0-level pending verification items.
2. Provide detailed designs for seven Ring-Lift scale experiments—rack-and-pinion drive system, track sleeve–thrust ring sliding wear, car aerodynamics, laser/microwave power transmission link atmospheric attenuation, sealed-segment inert gas protection effectiveness, cable vortex-induced vibration, and power rail high-voltage insulation and partial discharge—specifying scale parameters, measurement schemes, and expected data output.
3. Evaluate independent scientific experiments the stratospheric platform can host beyond the Ring-Lift scale experiments—atmospheric science observation, material exposure and lifetime assessment, high-altitude biological culture, and novel photovoltaic/communications technology validation—specifying experiment duration, sample configuration, and applicable altitude.
4. Output key parameters for use by Volume 8 (Deployment and Maintenance) and Volume 10 (Technical Interfaces).


### 4.2 Atmospheric Science Experiment Module

At its nominal altitude range of 25–35 km, the stratospheric platform can perform long-term continuous in-situ atmospheric measurements, filling the observational gap between radiosonde balloons (ceiling approximately 30 km) and sounding rockets (only minutes of profile data).

**（a）Measurement Parameters and Instrument Configuration**

| Measurement Parameter | Instrument | Accuracy | Mass | Description |
|:---|:---|:---:|:---:|:---|
| Temperature | Platinum resistance thermometer + radiation shield | ±0.1 K | ≤1 kg | Forced ventilation required at high altitude and low pressure to reduce radiation error [1] |
| Horizontal wind speed / direction | Ultrasonic anemometer | ±0.1 m/s, ±1° | ≤3 kg | Stratospheric wind speed typically <30 m/s; ultrasonic anemometer still operational at this air density |
| Air pressure | Capacitive barometer | ±0.1 hPa | ≤0.5 kg | Air pressure at 50 km is approximately 80 Pa; high-altitude-specific sensor required |
| Ozone concentration | UV absorption ozone photometer | ±1 ppb | ≤5 kg | Measures ozone concentration profile above the ozone layer [2] |
| Water vapor concentration | Chilled-mirror dew-point hygrometer | ±0.1 ppmv | ≤3 kg | Stratospheric water vapor is extremely low (2–10 ppmv); high-sensitivity instrument required [3] |
| Aerosol size distribution | Optical particle counter | 0.1–10 μm | ≤5 kg | Measures background concentration of stratospheric sulfate aerosols and volcanic perturbations [4] |
| CO₂/CH₄ concentration | Non-dispersive infrared gas analyzer | ±0.1 ppm | ≤5 kg | Used for stratospheric greenhouse gas profile measurements [5] |

Total mass of all instruments above ≤30 kg, total power consumption ≤200 W; can be permanently mounted in the aerostat's payload equipment bay with data relayed in real time via Ka/Ku antennas.

**（b）Multi-Altitude Coordinated Observation**

Multiple stratospheric platforms operating simultaneously at different altitudes (e.g., 20 km, 30 km, 40 km) can for the first time achieve coordinated profile observations of middle-atmosphere temperature, wind fields, and chemical composition. After time-synchronization of observations from multiple platforms, the propagation characteristics of gravity waves, tides, and planetary waves at different altitudes can be resolved.


### 4.3 Material Exposure and Lifetime Assessment Module

**（a）Exposure Environment Characteristics**

The material exposure environment at 25–35 km altitude has the following characteristics: UV irradiance approximately 2–3 times the ground level (UV-C not filtered by the ozone layer); temperature −80°C to −50°C with diurnal cycling; pressure 0.01–0.1 atm; ozone concentration in the upper ozone layer decreasing with altitude.

**（b）Exposure Sample Configuration**

| Sample Type | Exposure Purpose | Sample Size | Quantity | Exposure Period |
|:---|:---|:---:|:---:|:---|
| UHMWPE film (track sleeve outer layer material) | Assess effect of UV aging and low-temperature embrittlement on wear lifetime | 50×50 mm | 20 pieces | Batches retrieved at 6 months, 1 year, and 2 years |
| Multi-junction GaAs photovoltaic panels | Measure actual efficiency degradation rate under AM0 spectrum | 100×100 mm | 10 pieces | I-V curve measured every 6 months |
| CFRP laminates | Assess outgassing rate and microcrack formation under low pressure | 100×100 mm | 10 pieces | Samples retrieved every 6 months for SEM and mechanical testing |
| PTFE sealing strips | Assess effect of low-temperature cycling on elastic recovery rate | 50×10 mm | 20 strips | Compression set measured every 6 months |

All samples are mounted on a rotating exposure rack attached to the underside of the aerostat; every 6 months, the pod retrieves a batch of samples and lowers them to the ground for detailed analysis. The exposure rack carries a total solar irradiance meter and UV radiometer to continuously record the irradiation dose received by the samples.


### 4.4 High-Altitude Biological Experiment Module

**（a）Experimental Objectives**

UV irradiance and cosmic ray intensity in the lower stratosphere (20–30 km) are significantly higher than at ground level, but temperature and pressure remain within the tolerance range of microorganisms. This module uses the stratospheric platform to conduct long-term high-altitude microbial exposure experiments to study the effects of extreme environments on microbial survival, mutation, and gene expression.

**（b）Experiment Configuration**

| Parameter | Design Value | Description |
|:---|:---|:---|
| Incubator type | Sealed multi-layer culture dish array (quartz window) | Allows UV transmission while maintaining moderate internal pressure and humidity |
| Microbial strains | *Deinococcus radiodurans*, *Bacillus subtilis* spores, psychrotrophic bacteria, etc. | Known radiation-resistant and cold-tolerant strains selected as references |
| Incubator mass | ≤10 kg | Including temperature control and humidity regulation modules |
| Incubator power | ≤50 W | Powered by the aerostat's main battery |
| Experiment cycle | Batches retrieved at 3, 6, and 12 months | Each batch contains 3 parallel samples |
| Data recording | Continuous recording of temperature, humidity, UV irradiation dose, and cosmic ray dose | Data relayed in real time |

After retrieved samples are returned to the ground, genomic sequencing, proteomics analysis, and metabolite detection are performed to assess the mutagenic effects of the high-altitude environment on microorganisms. Experimental data also provides a reference baseline for closed-environment microbial management in Appendix 1, Volume 7.


### 4.5 Technology Validation Module

The stratospheric platform can serve as a field test bench for novel photovoltaic cells, communication equipment, and power transmission links. The experimental projects listed in the table represent the range of technology validation activities that can be conducted on the platform; each project can be independently deployed by different research institutions according to their own requirements, with the platform providing standardized power supply, communication, and installation interfaces. The technical parameters listed represent relatively favorable experimental values currently reported in the public literature.

| Validation Project | Experiment Content | Applicable Altitude | Experiment Duration | Relevance to Ring-Lift |
|:---|:---|:---:|:---:|:---|
| Novel photovoltaic panel field efficiency test | I-V curve measurement of perovskite/silicon tandem or CIGS thin-film panels under AM0 spectrum; comparison with nominal efficiency from ground-based AM0 simulator | 25–35 km | Continuous ≥12 months | Provides field efficiency data for selection of photovoltaic panels for the ring-elevator track sleeve power rails and elevator car |
| High-altitude laser communication terminal test | Bit error rate and atmospheric turbulence effect testing of Ka/Ku-band and laser communication links between platform and ground station [6] | 20–40 km | A few hours per session | Shares atmospheric channel characteristics with the communication link from the ring-elevator car to the ground |
| Novel energy storage system field validation | Testing of lithium-sulfur batteries and solid electrolytes for cycle lifetime and self-discharge rate under actual high-altitude thermal cycling | 25–35 km | Continuous ≥6 months | Provides comparison data for selection of buffer batteries for ring-elevator cars |


### 4.6 Ring-Lift Scale Experiments

The aerostat suspends a scaled-down CNT cable approximately 500 m long (diameter ø5–10 mm, with track sleeve and aluminium alloy rack, same material and process as Main Volume IV) from its stationed altitude of 25–35 km; a scaled-down verification pod runs back and forth on this cable, testing Ring-Lift P0-level pending verification items in a real atmospheric environment. By adjusting the amount of air in the secondary gas cell, the aerostat can descend to 15 km—at this altitude, air density is approximately 0.19 kg/m³, net lift per cubic meter is approximately 1.2 N/m³, far higher than at the 30 km nominal altitude, providing ample lift. The maximum operating altitude of the scale experiments equals the aerostat's stationed altitude (approximately 35 km); the minimum operating altitude is approximately 15 km (limited by the scaled-down cable length and the aerostat's minimum controllable stationed altitude). Experimental data is relayed in real time via the aerostat's communication link; samples are periodically retrieved by the pod and lowered to the ground for detailed analysis.


#### 4.6.1 Rack-and-Pinion Drive System Scale Experiment

**（a）Experimental Objectives**

Validate the contact fatigue lifetime and wear rate of aluminium alloy 7075-T6 micro-arc-oxidized rack and pinion in a real atmospheric environment, directly supporting Main Volume pending verification items V5-P0/N1/N2.

**（b）Experiment Configuration**

A section of scaled-down aluminium alloy rack (rack parameters: module 10 mm, pressure angle 20°, tooth width 150 mm, scaled 1:2 from the rack in Main Volume IV, Section 4.13) is installed on the scaled-down cable suspended by the aerostat. Scaled-down pinion pitch circle diameter 0.25 m, 4 gear pairs. Rack surface micro-arc oxidation treatment (hardness target ≥HV1000) identical to the full-size ring-elevator rack. Gear material identical to the rack; carried by the scaled-down pod, which runs back and forth along the cable at altitudes of 15–35 km. The pod carries an in-line laser profile scanner (accuracy ±5 μm) to record tooth surface wear depth segment by segment, and a torque sensor to measure rack-and-pinion meshing efficiency.

Scaled-down pod total mass ≤800 kg (including drive system and all experimental measurement equipment), payload ≥200 kg. Drive method: rack-and-pinion meshing (4 gear pairs); total drive power approximately 32 kW (peak, calculated for scaled module 10 mm and pinion pitch circle diameter 0.25 m at scaled dimensions and load); powered by the pod's independent battery (single experiment run duration ≥4 h, meeting the requirement for a complete altitude-profile round trip).

**（c）Experiment Duration and Measurement Scheme**

Continuous operation ≥6 months, cumulative meshing cycles ≥10⁷. Every 100 operating hours the pod automatically performs a full-length tooth surface scan; data is relayed in real time. After the experiment, all rack segments are returned to the ground for SEM and metallographic analysis. Directly measured parameters are: wear depth as a function of cycle count, fatigue lifetime of the micro-arc oxidation layer (number of cycles at first coating spallation), and the suppression effect of dry inert gas protection on wear rate.


#### 4.6.2 Track Sleeve–Thrust Ring Sliding Wear Scale Experiment

**（a）Experimental Objectives**

Measure the actual sliding wear rate between the inner edge of the thrust ring and the surface of the scaled-down CNT cable, validating the order-of-magnitude estimate of 500-year wear depth (approximately 0.059 μm) in Main Volume IV, Section 4.10.

**（b）Experiment Configuration**

A section of scaled-down track sleeve (middle-layer aluminium alloy + inner UHMWPE + thrust ring, same structure and material as Main Volume IV) is installed on the scaled-down cable with the design preload applied. The relative sliding between the inner edge of the thrust ring and the cable surface is naturally driven by the thermal expansion and contraction of the cable from pod operation and the platform's diurnal temperature cycling, requiring no additional active loading. The pod carries a laser rangefinder (accuracy ±0.1 mm) to periodically measure the actual displacement of each thrust ring to quantify wear depth.

**（c）Experiment Duration and Measurement Scheme**

Continuous exposure ≥12 months; every 3 months the pod measures the displacement of each thrust ring and records displacement-time curves, comparing them with the theoretical estimates in Main Volume IV, Section 4.10.2 to validate the order-of-magnitude estimate for 500-year wear.


#### 4.6.3 Elevator Car Aerodynamics Scale Experiment

**（a）Experimental Objectives**

Measure the aerodynamic drag coefficient and vortex-induced vibration frequency of two elevator car configurations—spindle-shaped (long axis along the cable) and disc-shaped (flat cylinder)—in a real atmosphere, validating the theoretical estimates in Main Volume V, Section 5.12.

**（b）Experiment Configuration**

The pod carries a 1:10 scale spindle-shaped car model (ø0.5 m × 6 m) and a disc-shaped car model (ø1 m × 1 m); models are released at different altitudes within the 15–35 km range and allowed to slide freely downward along the cable or towed upward by the pod. Each model carries a three-axis accelerometer, differential pressure sensor, hot-wire anemometer, and miniature camera to record drag force, vibration, and flow field data during operation. Experiments cover three movement directions: upward, downward, and translational.

**（c）Experiment Duration and Measurement Scheme**

Each configuration is operated ≥10 times at each of four altitudes (20 km, 25 km, 30 km, 35 km); drag coefficient, vortex shedding frequency, and vibration amplitude are measured in each run. Data is relayed in real time. Directly measured parameters include: actual C_d values for spindle and disc configurations (compared to the 0.05 and 0.8 cited in Main Volume V), variation of vortex-induced vibration frequency and amplitude with altitude and wind speed, and the suppression effect of the guide roller set on lateral wind loads.


#### 4.6.4 Laser/Microwave Power Transmission Link Atmospheric Attenuation Validation

**（a）Experimental Objectives**

Measure the transmission efficiency of the laser/microwave power transmission link between the ground→aerostat and ground→cable receiver panels under actual atmospheric conditions, validating the theoretical link equations in Main Volume V, Section 5.11.2 and Main Volume IX, Section 9.3.2.

**（b）Experiment Configuration**

A ground laser station (wavelength 1.06 μm ytterbium-doped fiber laser) transmits laser light to a receiver panel (multi-junction GaAs photovoltaic cells, area approximately 1 m²) installed on the underside of the scaled-down pod or aerostat. The pod carries a laser power meter and thermal imager to measure the actual irradiance on the receiver panel surface at different altitudes (15 km, 20 km, 25 km, 30 km, 35 km). The ground station simultaneously records transmitted power and atmospheric conditions (aerosol optical depth, water vapor column concentration). A microwave power transmission experiment at 5.8 GHz is conducted simultaneously; receiving antenna area approximately 1 m².

**（c）Experiment Duration and Measurement Scheme**

At each altitude, ≥10 transmission tests are performed under each of three atmospheric conditions: clear sky, thin cloud, and turbulent. Directly measured parameters include: end-to-end transmission efficiency as a function of altitude and atmospheric conditions, comparison of atmospheric attenuation coefficients with theoretical values (laser 17%, microwave 48%), and beam pointing accuracy and tracking error.


#### 4.6.5 Sealed-Segment Inert Gas Protection Effectiveness Validation

**（a）Experimental Objectives**

Measure the dry nitrogen leak rate of a sealed segment under real high-altitude pressure variation conditions, determine the actual replenishment interval for sealed-segment inert gas, and validate Main Volume V pending verification item V5-N5.

**（b）Experiment Configuration**

A section of sealed segment (aluminium alloy shell + UHMWPE sealing layer, internally filled with dry nitrogen at design pressure 70 kPa, same structure and material as the low-altitude rack sealing scheme in Main Volume V) is installed on the scaled-down cable. Miniature pressure sensors and oxygen concentration sensors are installed inside the sealed segment to continuously record internal pressure and oxygen partial pressure. An ultrasonic leak detector mounted externally on the sealed segment periodically scans all interfaces.

**（c）Experiment Duration and Measurement Scheme**

Continuous exposure ≥12 months. Directly measured parameters include: time variation curves of internal pressure and oxygen partial pressure of the sealed segment (from which the annual leak rate is calculated), dependence of leak rate on external pressure (validating the applicability of the Main Volume V sealing scheme at different altitudes), and the aging rate of the sealing layer under combined UV irradiation and low-temperature cycling.


#### 4.6.6 Cable Vortex-Induced Vibration Scale Experiment

**（a）Experimental Objectives**

Measure the vortex-induced vibration frequency and amplitude of the scaled-down CNT cable in a real atmospheric wind field, validate the suppression effect of helical strake spoilers, and directly support Main Volume IV pending verification item V4-N1.

**（b）Experiment Configuration**

Miniature three-axis accelerometers (spacing 10 m) are installed along the scaled-down cable (diameter ø5–10 mm, with the regular octagonal outer surface of the track sleeve) to continuously record the lateral vibration amplitude of each cable segment. Miniature hot-wire anemometers are installed every 50 m along the cable to simultaneously record local wind speed and direction. The cable also has a comparison section fitted with helical strake spoilers (helix pitch 5 cm, rib height 2 mm) and a control section without spoilers, to directly compare the suppression effect on vortex-induced vibration.

**（c）Experiment Duration and Measurement Scheme**

Continuous data collection ≥12 months, covering different wind speeds (10–50 m/s) and wind direction conditions. Directly measured parameters include: vortex shedding frequency and amplitude of each cable segment as a function of wind speed, suppression efficiency of helical strake spoilers on vibration amplitude (comparison section vs. control section), and the coupling characteristics between vortex-induced vibration and cable tension fluctuation.


#### 4.6.7 Power Rail High-Voltage Insulation and Partial Discharge Experiment

**（a）Experimental Objectives**

Measure the partial discharge inception voltage and surface flashover characteristics of the UHMWPE insulation layer under real high-altitude pressure variation conditions, directly supporting Main Volume VII pending verification item E-P0-8.

**（b）Experiment Configuration**

A section of UHMWPE insulation layer (thickness 5 mm) is applied to the middle-layer aluminium alloy of the scaled-down cable's track sleeve, with two parallel copper conductors embedded (simulating the ±100 kV DC bipolar configuration of the ring-elevator power rail). DC high voltage is applied between the conductors (provided by the aerostat's high-voltage power module, output 0–50 kV DC adjustable, simulating the actual operating voltage of the ring-elevator power rail). Fiber optic partial discharge sensors (sensitivity ≤10 pC) and surface potential meters are embedded in the insulation layer to continuously monitor partial discharge events and surface charge accumulation.

**（c）Experiment Duration and Measurement Scheme**

At each of five altitudes (15 km, 20 km, 25 km, 30 km, 35 km), ≥50 voltage ramp-up/ramp-down cycles are performed; partial discharge inception voltage and surface flashover voltage as a function of pressure are recorded. Directly measured parameters include: dependence of partial discharge inception voltage on external pressure (validating the safety margin of the Main Volume V insulation design at different altitudes), time constant of surface charge accumulation and decay on the UHMWPE insulation layer, and the trend of insulation degradation under high-humidity and ice-crystal deposition conditions.


### 4.7 Parameter Output

| Parameter | Value | Status | Receiving Volume |
|:---|:---|:---|:---|
| Atmospheric science instrument total mass / power | ≤30 kg / ≤200 W | Design baseline | — |
| Material exposure rack capacity | ≥60 sample pieces (including photovoltaic panels, UHMWPE, CFRP, PTFE) | Design baseline | — |
| Material exposure experiment duration | 6 months to 2 years | Design baseline | — |
| High-altitude biological incubator mass / power | ≤10 kg / ≤50 W | Design baseline | — |
| Biological experiment cycle | Batches retrieved at 3/6/12 months | Design baseline | — |
| Scaled-down CNT cable length | ≈500 m | Design baseline | — |
| Scaled-down cable diameter | ≈5–10 mm | Design baseline | — |
| Scaled-down rack parameters | Module 10 mm, pressure angle 20°, tooth width 150 mm (1:2 scale) | Design baseline | — |
| Scaled-down pinion pitch circle diameter | 0.25 m | Design baseline | — |
| Scaled-down pod operating altitude range | 15–35 km | Design baseline | — |
| Scaled-down pod total mass | ≤800 kg | Design baseline | — |
| Scaled-down pod payload | ≥200 kg | Design baseline | — |
| Scaled-down pod total drive power | Approx. 32 kW (peak) | Design baseline | Volume 2 |
| Rack-and-pinion scale experiment duration | ≥6 months, cumulative ≥10⁷ cycles | Design baseline | Main Volume VII |
| Track sleeve wear experiment duration | ≥12 months | Design baseline | Main Volume IV |
| Aerodynamic scale model dimensions | Spindle ø0.5 m×6 m, disc ø1 m×1 m (1:10 scale) | Design baseline | Main Volume V |
| Power transmission link experiment altitude points | 15/20/25/30/35 km | Design baseline | Main Volume V, IX |
| Sealed segment experiment duration | ≥12 months | Design baseline | Main Volume V |
| Vortex-induced vibration experiment duration | ≥12 months | Design baseline | Main Volume IV |
| Power rail insulation experiment voltage range | 0–50 kV DC | Design baseline | Main Volume VII |


### 4.8 Volume 4 Conclusion

This volume completes the full design of the stratospheric platform's research and development system. Core contributions:

1. **Established the irreplaceable strategic role of the stratospheric platform as the "high-altitude test bench" of the Ring-Lift project**. Before formal construction of the ring-elevator, operating a scaled-down pod on a scaled-down CNT cable suspended from the aerostat in a real atmospheric environment can provide the only obtainable real-environment measured data for Ring-Lift P0-level pending verification items—data that no ground-based vacuum chamber or numerical simulation can provide. The seven scale experiments cover the most critical technical bottlenecks of the ring-elevator: rack-and-pinion transmission, track sleeve wear, car aerodynamics, power transmission links, inert gas sealing, vortex-induced vibration, and high-voltage insulation.

2. **Provided a complete engineering scheme for each scale experiment**—from scale parameters (rack 1:2, car 1:10), scaled-down pod parameters (total mass ≤800 kg, payload ≥200 kg, total drive power approximately 32 kW), measurement equipment (laser profiler, torque sensor, accelerometers, partial discharge sensors, etc.), experiment duration (6–12 months of continuous operation), to expected data output (wear curves, efficiency degradation rate, vibration amplitude comparison, etc.)—with sufficient depth to directly guide subsequent engineering implementation.

3. **Four independent scientific experiment modules share stratospheric platform infrastructure with the Ring-Lift scale experiments**—atmospheric science observation, material exposure assessment, high-altitude biological culture, and technology validation. These experiments can generate independent scientific value and economic returns during the period before the ring-elevator is built, enhancing the investment attractiveness of the stratospheric platform in its early stage.


### References

[1] Nash, J., et al. Temperature measurements in the stratosphere: A review of techniques and challenges. *Atmospheric Measurement Techniques*, 2019.

[2] Proffitt, M. H., & McLaughlin, R. J. Fast-response dual-beam UV-absorption ozone photometer. *Journal of Atmospheric and Oceanic Technology*, 1983.

[3] Vömel, H., et al. The evolution of the frost point hygrometer. *Atmospheric Measurement Techniques*, 2016.

[4] Deshler, T., et al. Thirty years of in situ stratospheric aerosol size distribution measurements from Laramie, Wyoming. *Reviews of Geophysics*, 2019.

[5] Daube, B. C., et al. A high-precision fast-response airborne CO₂ analyzer for in situ sampling. *Journal of Atmospheric and Oceanic Technology*, 2002.

[6] Khalighi, M. A., & Uysal, M. Survey on free space optical communication: A communication theory perspective. *IEEE Communications Surveys & Tutorials*, 2014.

[7] Yerokhin, A. L., Nie, X., Leyland, A., Matthews, A., & Dowey, S. J. Plasma electrolysis for surface engineering. *Surface and Coatings Technology*, 1999.

[8] Kawamoto, H., & Shibata, T. Electrostatic cleaning system for removing dust adhering to solar panels on a planetary base. *Journal of Electrostatics*, Vol. 73, 2015, pp. 54–60.

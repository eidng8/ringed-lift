# Appendix I: Lunar Industry

## Volume I: Pioneer Missions and Orbital Validation

**Version**: 2.5<br/>
**Date of Preparation**: May 2026<br/>
**Currency Unit**: Renminbi (RMB), symbol: ¥<br/>
**Related Main Volumes**: Main Volume II, Main Volume VII


### Glossary

| Abbreviation | Term | Description |
|------|----------|------|
| CELSS | Closed Ecological Life Support System | A self-circulating life-support system used for long-duration crewed habitation |
| CLEP | China Lunar Exploration Program | China's national lunar exploration program led by CNSA |
| CNT | Carbon Nanotube | Core cable material for both the ring ladder and lunar industry |
| CVD | Chemical Vapor Deposition | Core process used in CNT manufacturing |
| EVA | Extravehicular Activity | Astronaut work outside a spacecraft on the lunar surface or in space |
| FCCVD | Floating Catalyst Chemical Vapor Deposition | Main process route for continuous CNT production |
| GCR | Galactic Cosmic Rays | High-energy particle radiation from outside the Solar System that poses long-term health risks to astronauts |
| GPR | Ground-Penetrating Radar | Radar system used to detect subsurface structures and voids beneath the lunar surface |
| GRAIL | Gravity Recovery and Interior Laboratory | NASA mission that performed precision mapping of the lunar gravity field in 2011-2012 |
| HEU | Highly Enriched Uranium | Fuel for space nuclear reactors, with U-235 enrichment >= 93% |
| ILRS | International Lunar Research Station | Sino-Russian-led lunar polar research station plan, with the basic phase scheduled for completion by 2035 |
| ISRU | In-Situ Resource Utilization | Use of local lunar resources for manufacturing and survival |
| KREEP | KREEP Rock | A class of lunar rocks enriched in potassium (K), rare earth elements (REE), and phosphorus (P) |
| LRO | Lunar Reconnaissance Orbiter | NASA lunar orbiter launched in 2009 |
| LRS | Lunar Radar Sounder | Subsurface radar sounder carried by the Kaguya probe |
| MLI | Multi-Layer Insulation | Reflective insulation used for passive thermal control in vacuum environments |
| NaK | Sodium-Potassium Alloy | Liquid-metal working fluid used as the heat-transfer medium in active liquid-cooling loops |
| NEΔT | Noise-Equivalent Temperature Difference | Sensitivity metric for infrared imaging systems |
| np-Fe | Nano-Scale Metallic Iron Particles | Naturally occurring nano-scale iron particles in lunar regolith, with particle size < 100 nm |
| PLSS | Portable Life Support System | Suit-integrated oxygen supply, thermal control, and CO₂ removal unit |
| PSR | Permanently Shadowed Region | Lunar polar regions that receive no sunlight year-round |
| RHU | Radioisotope Heating Unit | Unit that uses radioactive decay heat to keep equipment warm |
| Sabatier | Sabatier Reaction | Chemical reaction in which CO₂ and H₂ are catalytically converted into CH₄ and H₂O |
| SAR | Synthetic Aperture Radar | Radar system capable of subsurface imaging through the lunar surface |
| SPE | Solar Particle Event | High-energy particle outburst released by solar eruptions |
| SPA Basin | South Pole-Aitken Basin | The Moon's largest and oldest impact basin, located in the south polar region |
| XRF | X-Ray Fluorescence Spectrometer | Instrument for rapid in-situ analysis of elemental composition in lunar regolith |
| Ilmenite | Ilmenite (FeTiO3) | The most important iron-titanium oxide mineral in mare basalt |
| High-Calcium Plagioclase | High-Calcium Plagioclase (CaAl2Si2O8) | Major mineral in lunar highland anorthosite, rich in calcium and aluminum |
| Skylight | Lava-Tube Skylight | Natural opening formed by collapse of the roof of a lava tube |
| Lava Tube | Lunar Lava Tube | Large underground passage formed by ancient volcanic activity |
| Bimodal Grading | Bimodal Particle-Size Distribution | Regolith particle-size distribution characterized by two dominant size populations |
| Pathfinder Program | Lava Tube Pathfinder Program | Dedicated mission codename for on-site exploration of lava-tube skylights |


### 1.1 Introduction

This volume is positioned as the **foundational stage for technical feasibility** within the lunar industrial system. It focuses on answering the following core questions:

> Before trillions of yuan are invested and large construction teams are dispatched, which key technologies must first be validated in the real lunar environment? Should the first permanent base be built on the surface or underground, or can both paths advance in parallel? What kind of lava tube is truly suitable for development? What kind of regolith is best suited for building materials, and what kind is best suited for catalyst extraction? How can systematic surveying and experimentation answer the three fundamental questions: Does it exist? Can it work? Is it good enough?

This volume inherits the first stage defined in the overview, “Pioneer Missions and Habitation” (Years 1-8), and provides its concrete mission planning and validation roadmap.

One of the core strategic judgments of this volume is that **the first permanent base has two parallel technical pathways: “surface” and “subsurface (lava tube).”** The former has the advantage in energy access, while the latter has advantages in safety and room for spatial expansion. The mission of the pioneer phase is to gather sufficient decision-grade data across these two pathways, answering not only “whether it exists” but also “whether it is good enough,” rather than betting on one option in advance. Accordingly, the mission sequence planned in this volume serves the validation needs of both surface and subsurface site-selection paths, ensuring that all investments in equipment, technology, and human experience can be reused across both pathways.

**Regarding the strategic priority of polar lava tubes**, this volume adopts the following exploration strategy: the probability of finding lava tubes inside Shackleton crater itself is extremely low, and the exploration return is limited. However, conducting a regional strategic survey across **the tens-of-kilometers area surrounding Shackleton** to search for the golden combination of “Peak of Eternal Light + skylight” offers very high value and should be among the highest-priority objectives of Mission Groups II and III. This judgment directly affects the priority ranking of survey regions in Mission Group I, the landing-site decisions in Mission Group II, and the target selection for field lava-tube exploration in Mission Group III.

The core tasks of this volume are:

1. Systematically review completed, ongoing, and planned lunar exploration projects worldwide, and on that basis formulate the pioneer mission sequence for this project.
2. Identify the most critical technological uncertainties in lunar industrialization and convert them into verifiable scientific and engineering questions.
3. Define detailed screening criteria for ideal lava tubes, building-material regolith, and catalyst-feedstock regolith, to serve as the scientific targets for pioneer-mission exploration.
4. Plan a stepwise sequence of “look first, touch later, then stay” missions, from Earth orbit to the lunar surface, spanning uncrewed and crewed operations across three validation tracks: lunar water ice, lunar construction materials, and subsurface lava tubes.
5. Provide detailed engineering design parameter requirements for each mission. Surface operations equipment must explicitly account for the limitations imposed by Earth-Moon communication delay, about 1.3 seconds one-way and 2.6 seconds round trip, and its minimum autonomy level must be specified.
6. Establish P0-level pass/fail criteria under the rule of “pass to proceed, fail to terminate,” and connect them to Main Volume VII.


### 1.2 Current Status of Relevant Domestic and International Programs

The pioneer missions do not begin from zero. Global lunar exploration has already accumulated valuable technical heritage and infrastructure for lunar industrialization. The following are the key completed, ongoing, and planned programs on which the design of this volume is based.

#### 1.2.1 China Lunar Exploration Program (CLEP)

Since its establishment in 2004, the China Lunar Exploration Program has completed its three-step strategy of “orbit, land, return.”

**Completed missions**:

- **Chang'e-4** (2019): Humanity's first soft landing on the far side of the Moon, validating lunar far-side relay communications and laying the foundation for communications support in the polar regions [1].
- **Chang'e-5** (2020): Sample return from the near side of the Moon, bringing back 1,731 grams of lunar regolith [2]. These samples provide irreplaceable real material for ground validation of the in-situ resource-utilization technologies discussed in this volume. Sample analysis confirmed that mare basalt in the Oceanus Procellarum region is rich in ilmenite, with ilmenite content reaching 10%-20%, making it an excellent candidate catalyst feedstock [2].
- **Chang'e-6** (2024): Humanity's first far-side lunar sample return, collecting material from the South Pole-Aitken Basin; ranked first among China's Top Ten Scientific Advances of 2025. Sample analysis revealed that the mare basalt from the South Pole-Aitken Basin consists primarily of pyroxene, plagioclase, and ilmenite, and that ilmenite, titanium oxides, and various iron-based compounds can all serve as highly effective photo- and electrocatalysts [3,4].
- **Queqiao-2 relay satellite** (2024): Completed in-orbit communications link testing. It will provide relay support for Chang'e-7, Chang'e-8, and later crewed lunar missions [5].

**Ongoing and planned missions**:

- **Chang'e-7** (second half of 2026): China's first lunar south-pole exploration mission, targeting the South Pole-Aitken Basin above 85° south latitude to search for evidence of water ice. The mission includes an orbiter, lander, rover, and hopper probe. Landing accuracy is required to be better than 100 meters. The preferred candidate landing site is the rim of Shackleton crater [6,7]. This mission is the direct technical precursor of Mission Groups I and II in this volume, and its water-ice detection data will directly determine later base siting and mining plans.
- **Chang'e-8** (around 2029): Lunar south pole mission focusing on in-situ 3D printing construction, communications, and energy system experiments. It will provide local construction-technology validation for the basic ILRS phase and for the crewed habitation goals of Mission Group III in this volume [8].
- **International Lunar Research Station (ILRS)**: Basic phase to be completed in 2035 and expanded phase in the 2040s. Jointly led by China and Russia, with Venezuela, Pakistan, Azerbaijan, and others already participating. In May 2025, China and Russia signed a memorandum on construction of an ILRS nuclear power station [9,10]. The lunar industrial system planned in this appendix shares a south-polar siting logic with ILRS, allowing deep synergy in energy, communications, and transportation infrastructure.
- **Chinese crewed lunar landing program** (before 2030): Long March 10 heavy-lift launch vehicle, Mengzhou crewed spacecraft, Lanyue lunar lander, Wangyu lunar suit, and the crewed lunar rover have all completed prototype development [11,12]. This provides a mature human transport system that Mission Group III can leverage.

#### 1.2.2 U.S. and International Programs

- **NASA VIPER rover** (canceled, 2024): A USD 450 million mission equipped with drilling systems and spectrometers, designed for an operating life of around 100 days to explore polar water-ice distribution [13]. Its drilling and volatile-measurement design can serve as a reference baseline for the water-ice exploration equipment of this volume.
- **NASA Artemis program** (repeatedly delayed): Artemis 2, crewed lunar flyby, delayed to April 2026; Artemis 3 delayed to 2027. NASA plans to invest about USD 20 billion over the next seven years to establish a base at the lunar south pole, while pausing the Gateway lunar-orbit station plan [14,15]. The strategic overlap between China and the United States in polar siting has effectively made water-ice resources a global point of competition, which means this volume must maintain independence in its technical choices.
- **NASA PRIME-1** (payload on IM-2, landed March 2025): Carried the TRIDENT drill and the MSolo mass spectrometer to detect subsurface water ice. Although the mission ended early because of lander attitude anomalies, the payload design remains a valuable reference [16].
- **Commercial lunar landers** (multiple missions ongoing): Intuitive Machines' Nova-C lander has flown twice. IM-1 (February 2024) achieved the first commercial lunar landing; IM-2 (March 2025), although terminated early due to landing anomalies, still demonstrated the feasibility of polar-region landings [17,18]. Commercial lunar landing services may be considered as international procurement candidates for the landers in this volume.

#### 1.2.3 Status of Lunar Lava-Tube Exploration

Exploration of lunar subsurface space, especially lava tubes, is becoming a frontier of global lunar science.

**Key completed results**:

- **Japan's Kaguya/SELENE mission** (2007-2009): The onboard LRS radar sounder produced the first radar-echo data on the lunar subsurface structure. In the Marius Hills region, about 14°N, 56°W, LRS data clearly revealed underground cavity signals extending for dozens of kilometers, a milestone discovery in lunar lava-tube exploration [19]. Because GRAIL data also indicate large low-density anomalies there, the region is considered a candidate site for a very large lava-tube system.
- **NASA GRAIL gravity-field mission** (2011-2012): Using precise measurements of the lunar gravity field, the two spacecraft discovered low-density anomalies in the Marius Hills region that matched the LRS data, independently corroborating the presence of large lava tubes from the gravity perspective [20].
- **LRO Mini-RF radar exploration** (2009-present): NASA's Lunar Reconnaissance Orbiter has continuously imaged the lunar polar regions and candidate skylights using Mini-RF synthetic aperture radar. Results published in 2024 confirmed that the Mare Tranquillitatis Pit skylight, about 8°N, 33°E, connects at its base to an underground cave extending at least several tens of meters, making it the first large enterable lava-tube cavity directly confirmed by radar data [21,22].

**Preliminary evidence of polar lava tubes**:

- **Philolaus crater at the lunar north pole**: Scientists at the SETI Institute analyzed LRO imagery and found multiple suspected skylights in the region, considered direct clues to the existence of polar lava tubes. The LEAPS mission concept study suggests that if permanent shadow exists inside these high-latitude lava tubes, they may preserve water-ice resources [23,24].
- **South Pole-Aitken Basin**: As the Moon's largest and oldest impact basin, it is inferred to have experienced both impact and volcanic activity in the distant past. In theory, it has the geologic conditions needed to form lava tubes, but to date there is still no direct orbital detection evidence [25].

**Alignment with the ring-ladder schedule**: These findings provide ample scientific basis for designating “lava-tube pathfinding” as a P0-level strategic objective in this volume. The pioneer missions are precisely the phase that turns these preliminary findings into reliable data for engineering decision-making.


### 1.3 Overall Mission Sequence

Lunar industrialization must follow a progressive logic: “look first, touch later, live there after.” This volume divides the pioneer phase into three interlocking mission groups, and each group covers both the surface path and the subsurface path.

**Before the mission sequence begins, engineering screening criteria must be defined for the following three categories of resources.** These criteria directly determine the exploration targets and acceptance standards of the mission groups, and they are the scientific basis of the entire pioneer phase.

**(a) Screening criteria for ideal lava tubes**

A developable lunar lava tube must simultaneously satisfy the following engineering conditions:

- **Structural safety**: Roof thickness must be no less than 30 m, assuming dense basalt with low porosity and low permeability. When a lava tube's width exceeds 2.5 times the thickness of its roof, collapse probability rises significantly; therefore, the roof-thickness-to-width ratio must be >= 0.4. The upper basalt layer must have compressive strength of at least 50 MPa and tensile strength of at least 5 MPa, ensuring that after pressurization to one atmosphere it can withstand the resulting outward force without rupture or leakage.
- **Usable internal space**: Internal width must be at least 500 m, height at least 30 m, and continuously detectable length at least 1 km. Priority should be given to lava tubes with a natural skylight opening. The skylight slope must be gentle, inclination <= 30°, so that rovers or future large equipment can enter. The opening diameter must be at least 10 m to ensure adequate lighting and passage space.
- **Environmental stability**: Internal temperature variation must remain stable, with day-night fluctuation <= +/-5°C. There must be no evidence of recent collapse or fault activity within the last 100 million years. The skylight orientation should provide a stable line of communication to Earth.
- **Radiation-shielding performance**: The overlying rock must attenuate galactic cosmic ray flux by at least 90%, reducing the annual internal radiation dose to no more than 50 mSv, about one-eighth of the dose on the open lunar surface.

**(b) Screening criteria for construction-material regolith**

Regolith suitable for processing into construction materials such as 3D-printed bricks or cast concrete must meet the following conditions:

- **Mineralogical composition**: High-calcium plagioclase content must be at least 50% to provide cementitious behavior, while iron-titanium oxides, ilmenite plus titanomagnetite, should total 10%-20% to provide strength and aid sintering. Priority should be given to mixed regions where highland anorthosite and mare basalt coexist, such as breccia zones, so that beneficial elements such as calcium, aluminum, iron, and titanium can be obtained simultaneously.
- **Particle-size distribution**: The regolith should show a bimodal or multimodal grading pattern, with coarse particles of 100-500 μm accounting for 40%-60% and fine particles <50 μm accounting for 40%-60%. This natural grading reduces porosity and improves the density and compressive strength of the final product.
- **Natural additives**: Nano-scale metallic iron particles, np-Fe with particle size <100 nm, should be present at no less than 0.1 wt%, improving toughness during sintering. Glassy bonding material should be present at no less than 10 wt%, allowing it to act as a natural binder at high temperature and reducing the need for added binders.
- **Physical properties**: Loose bulk density should be 1.2-1.8 g/cm3, and porosity should be 40%-60%, making the material suitable for direct use as sintering feedstock without additional crushing.

**(c) Screening criteria for catalyst-feedstock regolith**

Regolith suitable for extracting CNT-growth catalysts, primarily iron and nickel, must satisfy the following conditions:

- **Critical mineral content**: Ilmenite content must be at least 10 wt%. Natural Fe-Ni metallic particles larger than 50 μm must be present at no less than 0.5 wt%.
- **Iron content in pyroxene**: Iron content in pyroxene must be at least 10 wt% as FeO. Iron hosted in pyroxene can serve as a supplementary source for chemical extraction.
- **Particle scale**: The average particle size of the target minerals must be at least 50 μm.
- **Potential for direct utilization**: If raw regolith or physically enriched ilmenite / Fe-Ni fractions, after only simple physical treatment such as crushing and magnetic separation and without hydrometallurgy, can demonstrate comparable catalytic activity in FCCVD experiments, with CNT yield reaching at least 80% of that achieved by Earth-produced catalysts of equivalent purity, then this pathway should be prioritized.

These three sets of criteria will govern all exploration activities from Mission Group I through Mission Group III, serving as the scientific basis for payload design, data collection, and P0-level judgments.

The overall arrangement of the three mission groups is as follows:

- **Mission Group I: Remote-Sensing Survey and Orbital Validation (Years 1-3)**. Core objective: obtain a high-resolution distribution map of polar resources and lava-tube skylights, **with priority coverage of the SPA basin margin area within a 100 km radius around Shackleton**; preliminarily screen candidate feedstock regions that satisfy the criteria above. Expected investment: about RMB 50-80 billion.
- **Mission Group II: Lunar Surface Robotic Deployment (Years 3-5)**. Core objective: conduct landing-based exploration to acquire in-situ surface samples and field-detection data for lava-tube skylights; **deploy at least one lander around Shackleton to carry out a gridded regional GPR scan of a skylight area**. Expected investment: about RMB 100-150 billion.
- **Mission Group III: First Crewed “Lunar Sentinel” Stay (Years 5-8)**. Core objective: achieve the first crewed stay longer than one month; complete all P0-level technology validation; **in the priority ranking of field lava-tube targets, the Shackleton periphery, if Mission Group II identifies a qualifying skylight there, and Philolaus crater are tied for top priority, ahead of Marius Hills**. Expected investment: about RMB 200-400 billion.

There is a clear chain of data and asset inheritance across the three mission groups: orbital survey results guide lander site selection, while lander-acquired samples provide input for the engineering design of the crewed mission. All key decision nodes in the pioneer mission groups are shared with Main Volume VII, Engineering Verification, and any P0-level failure triggers a comprehensive program review.

**Note on reusability of investment**: The transportation systems involved in Mission Groups II and III, including heavy-lift rockets, orbital transfer stages, and landers, as well as drilling and sampling equipment, autonomous navigation technologies, and communications relay systems, are fully shared between surface missions and lava-tube missions. There is no case in which an entire separate equipment stack must be developed solely for lava-tube exploration. Even if the final conclusion of lava-tube exploration is that such sites are not viable, the equipment, technologies, and human experience accumulated will still be used in full for subsequent surface-base construction.


### 1.4 Mission Group I: Remote-Sensing Survey and Orbital Validation (Years 1-3)

#### 1.4.1 Key Scientific Questions

Although missions such as Chang'e, LRO, and Chandrayaan have already accumulated significant data, the precision and dimensionality of the resource data required for lunar industrial site selection are still insufficient. In particular:

- **Exact distribution and occurrence form of polar water ice**: Does the ice exist as pure ice layers, ice-regolith mixtures, or hydrated minerals? How large is its spatial variability at the meter scale? This directly determines extraction methods and equipment selection.
- **Thermal stability of permanently shadowed polar regions**: Can water ice be maintained long-term without sublimation and escape? A precise 3D temperature-distribution model is a prerequisite for engineering-scale extraction. Existing studies based on LRO Diviner data have carried out preliminary thermal modeling of polar shadowed regions, but their spatial resolution is insufficient for engineering-scale decisions [26].
- **Reserves and occurrence of CO₂ cold traps**: As a supplementary local carbon source for CNT manufacturing, polar CO₂ cold-trap reserves must be supported by direct exploration data. Schorghofer and Williams, 2021, were the first to confirm the existence of lunar polar CO₂ cold traps based on LRO data, with a total area of about 200 km2, but their reserves remain unconstrained [27].
- **Moonquakes and geologic stability**: The geomechanical properties of candidate base sites, especially moonquake frequency, magnitude, and amplification effects in surface motion.
- **Spatial distribution and internal geometry of lava-tube skylights**: How many enterable lava tubes exist in the polar and high-latitude regions? Are their internal width, height, and length sufficient to host large industrial facilities? Existing GRAIL and LRO data have already preliminarily revealed lava-tube evidence in Marius Hills and the Mare Tranquillitatis Pit [19,20,21], but a systematic survey of the polar regions has not yet been carried out. **The center of gravity of this survey should be the SPA basin margin region within a 100 km radius around Shackleton**. In theory, this region has the geologic conditions required for lava-tube formation because basin impacts were accompanied by volcanic activity, and if confirmed it would create the optimal “eternal light + subsurface” synergy together with Shackleton.
- **Regional distribution of construction-material regolith**: Using the criteria in Section 1.3(b), multispectral data should be used to identify contact-mixed belts between highland anorthosite and mare basalt, and preliminarily delineate candidate resource zones matching the required mineral composition and bimodal particle-size distribution.
- **Regional distribution of catalyst-feedstock regolith**: Using the criteria in Section 1.3(c), multispectral data and hyperspectral mineral mapping should be used to identify titanium-rich mare basalt regions with ilmenite content >= 10 wt%, and preliminarily delineate candidate catalyst-feedstock zones.

#### 1.4.2 Orbital Exploration Mission Design

This pioneer mission plans to deploy two mutually redundant and payload-complementary polar-orbit survey satellites, along with a small-satellite formation for fine gravity-field exploration.

**(a) Polar low-orbit survey satellite**

- Orbit type: polar low orbit, mean altitude 30-50 km, near-circular orbit
- Mission life: at least 3 years, covering at least 36 full lunar-night cycles
- Platform mass: no more than 1,200 kg, including propellant and standard thermal control, excluding lunar-night survival add-on modules. Add-on modules such as RHUs are expected to require an additional 5%-8% mass margin and must be included during detailed design.
- Attitude control accuracy: <= 0.05° with three-axis stabilization
- Data transmission rate: >= 300 Mbps on Ka-band via Queqiao-2 relay [5]
- Total power consumption: <= 2,500 W peak
- High-resolution multispectral camera: visible-band resolution <= 0.3 m/pixel; near-IR and shortwave IR resolution <= 1 m/pixel; swath width >= 20 km. This payload is used for high-precision polar topographic mapping, screening of candidate lava-tube skylights, and skylight-slope measurement, with sufficient resolution to determine whether the access slope is <= 30°. **The camera's highest mission priority is the SPA basin margin area within 100 km of Shackleton**. During the first 6 months, that region must be treated as the top-priority coverage target, with at least three repeat imaging passes completed to support stereo terrain extraction of candidate skylights and analysis of seasonal illumination changes. It also serves to preliminarily identify contact-mixed belts of high-calcium plagioclase and titanium-rich basalt.
- Neutron spectrometer: thermal and epithermal neutron-flux sensitivity <= 5% at 2σ; spatial resolution <= 50 km. Used for preliminary estimation of polar water-ice abundance by detecting hydrogen content to a depth of about 1 m, a proxy for water ice.
- Infrared imaging spectrometer: spectral range 0.5-14 μm; at least 200 spectral channels; thermal-IR spatial resolution <= 50 m/pixel; NEΔT <= 0.1 K at 300 K. Used for modeling day-night surface-temperature variation, evaluating water-ice stability in permanently shadowed regions, detecting thermal anomalies inside lava-tube skylights, since lava tubes with near-constant internal temperatures stand out from surrounding terrain and those with day-night fluctuation <= +/-5°C are preferred, and performing regional mineral mapping of ilmenite, via absorption features around 1.0 μm and 2.0 μm, and high-calcium plagioclase, via absorption around 1.25 μm.

**(b) Synthetic aperture radar satellite**

- Orbit type: polar sun-synchronous orbit, altitude 100-150 km
- Mission life: at least 3 years
- Platform mass: no more than 2,500 kg, including propellant and standard thermal control, excluding lunar-night survival add-on modules. Add-on modules such as RHUs are expected to require an additional 5%-8% mass margin and must be included during detailed design.
- Attitude control accuracy: <= 0.01° with three-axis stabilization. SAR places tighter demands on pointing stability.
- Data transmission rate: >= 500 Mbps on Ka-band via Queqiao-2 relay [5]
- Total power consumption: <= 5,000 W peak during SAR transmission
- L-/P-band SAR: frequency either L-band at 1.26 GHz or P-band at 435 MHz; full-polarization mode, HH + HV + VH + VV; spatial resolution <= 5 m in StripMap mode; penetration depth >= 2 m in dry regolith. Used for 3D imaging of subsurface water-ice distributions at 2-5 m depth in permanently shadowed regions, independent of illumination conditions, and for high-detail subsurface scanning of known lava-tube candidate areas such as Marius Hills and Philolaus crater. **The highest SAR scanning priority is the SPA basin margin area within 100 km of Shackleton**. At least two complete StripMap coverages of this region must be completed within the first 12 months, targeting continuous basalt roofs >= 30 m thick and continuous subsurface cavity signals. It should also support inversion of regolith loose-layer thickness and particle-size roughness, providing preliminary input for assessing the bimodal grading of construction-material regolith. The design draws on the successful experience of Kaguya LRS and LRO Mini-RF [19,21].

**(c) Fine gravity-field exploration small-satellite formation**

- Two microsatellites, each <= 200 kg, operating in formation flight in polar low orbit
- Inter-satellite ranging accuracy <= 1 μm/s via Ka-band crosslink
- Mission life >= 2 years
- Core task: obtain fine gravity-field data for the polar regions, above 60° north and south latitude, with spatial resolution <= 20 km and precision <= 5 mGal. These data are used to cross-validate SAR evidence for low-density anomalies associated with lava tubes and must be sensitive enough to resolve gravity anomalies corresponding to cavities with widths >= 500 m. **The area within a 100 km radius around Shackleton must be revisited at least four times within the first 18 months** to support gravity time-variation analysis and to exclude false anomalies caused by moonquakes or thermal stress. The data-processing approach should reference the GRAIL mission [20].

#### 1.4.3 Orbital Technology Validation

The orbital exploration mission will also carry out first-of-its-kind principle validation for several key technologies.

**Microgravity CNT growth experiment** (carried by the polar survey satellite)

- Miniature FCCVD reactor with internal volume <= 2 L
- Controllable operating temperature of 600-1,200°C with precision of +/-10°C
- Carbon source is methane gas; catalyst is preloaded iron / nickel nanoparticles with purity >= 95%
- Target product is continuous CNT yarn, length >= 100 cm, with controllable diameter of 10-50 μm
- Power consumption <= 500 W; experiment duration >= 100 h
- Corresponds to pending validation item V2-M4 in Main Volume II, verifying that microgravity does not prevent CNT fiber formation. Existing ground experiments have already shown that JAXA successfully achieved in-situ CVD growth of CNTs on lunar-regolith simulant particles [28], and the discovery of natural SWCNTs in Chang'e-6 regolith provides environmental analogy support [29].

**Miniature catalyst extraction experiment** (carried by the polar survey satellite)

- Miniature hydrometallurgical module with preloaded regolith amount >= 500 g, using titanium-rich mare-basalt regolith simulant with ilmenite content >= 10 wt%
- Integrated acid-leaching and hydrogen-reduction reactor
- Target extracted elements: Fe, Ni, Co, with extraction efficiency >= 60%
- Solid residues must be sealed and immobilized
- Total module mass <= 15 kg
- Provides preliminary parameters for large-scale lunar catalyst production in Mission Group II and Volume III of this appendix

**Mission Group I P0-level acceptance criteria**:

- **P0-R1**: The spatial resolution of the polar water-ice distribution map, expressed as H-equivalent abundance, must be better than 50 km, and uncertainty in hydrogen abundance, in wt% H₂O equivalent, must not exceed +/-30% at 2σ.
- **P0-R2**: The microgravity CNT growth experiment must produce continuous CNT fibers at least 100 cm long, with no visible breakage under SEM observation, confirming that microgravity does not prevent fiber formation.
- **P0-R3**: A systematic survey of lava-tube skylights in the polar regions, above 60° north and south latitude, must be completed, with **the SPA basin margin area within a 100 km radius around Shackleton designated as the top-priority coverage region**. At least three high-priority candidate sites must be identified and cataloged. Each must show: continuous basalt roof thickness >= 30 m in SAR echoes, estimated cavity width >= 500 m, skylight slope <= 30° in visible imagery, and internal day-night temperature variation <= +/-10°C in infrared data. These sites will serve as candidate targets for field exploration in Mission Group II.
- **P0-R4**: Using multispectral data, at least five candidate construction-material regolith zones meeting the criteria of Section 1.3(b) must be preliminarily delineated, each with area >= 10 km2 and mineral-mapping resolution <= 100 m/pixel.
- **P0-R5**: Using multispectral data, at least five candidate catalyst-feedstock regolith zones meeting the criteria of Section 1.3(c) must be preliminarily delineated, each with ilmenite content >= 8 wt%, inferred from the strength of the 1.0 μm and 2.0 μm absorption features, and area >= 5 km2.


### 1.5 Mission Group II: Lunar Surface Robotic Deployment (Years 3-5)

#### 1.5.1 Overall Lander Design

This phase deploys 3-4 survey landers, each landing at a different candidate site, to be finalized based on the detailed survey results of Mission Group I. Priority is assigned as follows:

- **First priority**: At least one lander shall be deployed in the **SPA basin margin region around Shackleton**. If Mission Group I identifies a high-priority lava-tube skylight there that meets the P0-R3 criteria, this lander will be sent directly to the candidate coordinates of that skylight. Its mission focus includes: (a) hopper descent exploration and GPR scanning of the skylight; (b) in-situ XRF and particle-size measurements of nearby construction-material and catalyst-feedstock regolith; and (c) deployment of regolith 3D-printing and catalyst-extraction experiments.
- **Second priority**: At least one lander shall be deployed to another polar lava-tube candidate region, Philolaus crater, to carry out the same suite of exploration tasks.
- **Third priority**: At least one lander shall be deployed to a candidate area for construction-material and catalyst-feedstock regolith, preferably a highland-mare mixed contact zone or a titanium-rich mare-basalt zone that satisfies the criteria in Section 1.3(b) and (c).
- **Fourth priority**: If Mission Group I does not discover a qualifying skylight around Shackleton, the fourth lander shall be sent to Marius Hills or the Mare Tranquillitatis Pit to ensure that exploration data for the mid- and low-latitude subsurface pathway are not missing.

Key design requirements are as follows:

- Launch mass per lander <= 4,200 kg, including payload, cruise stage, and standard thermal control, but excluding lunar-night survival add-on modules. Add-on modules such as RHUs are expected to require an extra 5%-8% mass margin and must be included during detailed design. This mass class is compatible with Long March 5 and equivalent heavy-lift launch vehicles.
- The lander adopts an octagonal platform with a composite truss structure, providing at least 8 m2 of payload installation area.
- Landing accuracy <= 100 m at 3σ, inheriting and improving upon the polar landing-accuracy requirements of Chang'e-7 [6].
- Design life >= 12 Earth months, covering a full lunar day-night cycle.
- Energy system: solar arrays provide >= 1,500 W during the lunar day; RHUs maintain thermal control through the lunar night.
- Communications: direct-to-Earth X-band link >= 2 Mbps; Ka-band link via Queqiao-2 relay >= 50 Mbps [5].
- Total payload mass <= 150 kg.

**Autonomy requirements for lunar surface operations**: Because Earth-Moon communications have a round-trip delay of about 2.6 seconds, real-time remote control from Earth cannot support precise operations. All surface-operating equipment must satisfy the following minimum autonomous-capability levels:

- **Fault detection and safe shutdown**: Equipment must be able to autonomously detect critical anomalies, such as current spikes, temperature exceedance, or attitude instability, and trigger safe shutdown within 50 milliseconds without waiting for an Earth command.
- **Path planning and obstacle avoidance**: Rover autonomy systems must be able to plan the optimal route from Point A to Point B based on stereo vision or lidar data, recognizing and avoiding rocks of diameter >= 20 cm and pits of depth >= 15 cm. For skylight-approach missions, the rover must additionally recognize hazardous edges and maintain a safe stand-off distance of at least 5 m.
- **Autonomous execution of mission sequences**: Equipment must be capable of receiving high-level commands from the ground, such as “drill at coordinates X,Y to depth Z” or “hover-image the skylight at coordinates X,Y,” and autonomously decomposing them into lower-level action sequences without requiring step-by-step confirmation from Earth.
- **Autonomous survival during communications outage**: If Earth communications are lost, the equipment must autonomously enter a low-power safe mode, preserve critical thermal control and communications listening functions, and automatically resume the preplanned mission when the signal returns.

#### 1.5.2 Scientific Exploration Payloads

**Polar water-ice drilling and volatile-analysis package**

- Rotary-percussive drill with depth capability >= 3 m
- Penetration rate >= 5 cm/min in dry regolith and >= 1 cm/min in ice-bearing regolith
- Drill-bit diameter >= 25 mm
- Sample furnace: controllable heating rate of 0.1-10°C/s, maximum temperature 900°C, temperature-control precision +/-5°C
- Mass spectrometer: mass range 1-200 amu, resolution <= 0.5 amu, detection limit <= 1 ppb
- Total mass <= 35 kg, peak power <= 300 W
- **Autonomy requirement**: The drill must be able to infer lithology online and autonomously adjust rotation rate, feed rate, and impact energy based on drilling resistance and vibration spectrum. If bit sticking or bit wear occurs, it must autonomously attempt reverse withdrawal and variable-speed strategies. Only after three consecutive failed withdrawal attempts may it request Earth intervention.
- This payload directly validates water-ice occurrence form, abundance, and extraction energy cost, corresponding to P0-M1 of this volume and the mining-system design work in Main Volume IV. Its overall technical scheme draws on NASA VIPER's TRIDENT drill design [13,16].

**CO₂ cold-trap detector and sampler**

- Cold-trap scraping sampler with controllable scraping depth of 0-5 cm and single-sample mass >= 10 g
- Miniature gas chromatograph targeting CO₂, CH₄, and NH3, with CO₂ detection limit <= 10 ppm
- Total mass <= 8 kg
- **Autonomy requirement**: The sampler must be able to infer whether it has encountered bedrock or a hard interlayer from torque feedback during scraping, and automatically adjust scraping depth to avoid hardware damage.
- This payload confirms the raw-material basis for a supplementary CNT carbon-source pathway, directly supporting the carbon-source strategy of the CNT manufacturing system in Volume V. The existence of CO₂ cold traps has already been confirmed by Schorghofer and Williams, 2021, using LRO data [27].

**Regolith mechanical-properties test suite**

- Small penetrometer with penetration depth >= 1 m and penetration-force precision <= 1 N
- Direct-shear device with maximum normal stress >= 100 kPa
- Excavation-simulation scoop with bucket volume >= 0.001 m3
- Total mass <= 15 kg
- **Autonomy requirement**: During penetration, the penetrometer must continuously monitor the resistance curve. If abnormal resistance increase, likely indicating a rock, is detected, it must automatically pause penetration, mark the depth, and attempt penetration again at a preplanned offset position.
- The resulting data provide input parameters for base-foundation design in Volume II and mining-equipment design in Volume IV, including regolith bearing capacity, internal friction angle, cohesion, and excavability. The test data are also used to validate the physical-property criteria for construction-material regolith in Section 1.3(b).

**Long-duration lunar dust environment monitoring station**

- Electrostatic-field sensor with sensitivity <= 1 V/m
- Optical attenuation sensor covering wavelength range 400-1000 nm
- Wear sensor with material mass-loss precision <= 1 μg
- Continuous operation >= 12 months; total mass <= 5 kg; power <= 20 W
- **Autonomy requirement**: The station must be able to autonomously recognize and filter spurious data peaks caused by its own equipment actions, such as drilling vibration, and increase sampling frequency when anomalies occur so that events can be captured.
- Data are shared with the habitation-engineering design work in Volume VII.

**In-situ regolith mineralogy and particle-size analyzer**

- X-ray fluorescence spectrometer: excitation source is a miniature X-ray tube with Rh target; energy resolution <= 150 eV at 5.9 keV; analyzable elements from Na to U; detection limit <= 100 ppm for medium and heavy elements such as Fe and Ti. Used to directly measure the abundance of ilmenite, high-calcium plagioclase, and natural Fe-Ni particles in regolith.
- Miniature laser particle-size analyzer: measurement range 0.1-1,000 μm; repeatability <= +/-3%. Used for in-situ measurement of regolith particle-size distribution and determination of whether bimodal grading is present.
- Miniature magnetic susceptibility meter: sensitivity <= 10^-5 SI, used to measure the content of magnetic minerals in regolith, chiefly natural Fe-Ni particles and ilmenite. Magnetic-susceptibility values can directly serve as a preliminary indicator of magnetic-separation feasibility.
- Total mass <= 12 kg, power <= 30 W
- **Autonomy requirement**: Within a single analysis cycle of <= 5 minutes, the instrument must complete combined XRF elemental analysis, laser particle-size measurement, and magnetic-susceptibility scanning, compare the results against the threshold criteria for construction-material and catalyst-feedstock regolith, and return both the classification result, qualified / unqualified / pending, and the raw data.

**Lava-tube skylight exploration payload**

- Lightweight hopper probe: released from the lander and using cold-gas propulsion or hopping to conduct close-up observations of a skylight. Total mass <= 10 kg; single-flight duration >= 300 s. Carries a high-resolution micro-camera with resolution <= 5 cm/pixel at 100 m distance and a micro-lidar with ranging precision <= 2 cm and maximum range >= 500 m. During descent, the lidar must precisely measure skylight opening diameter, target >= 10 m, and wall inclination, target <= 30°, while the micro-camera acquires stratigraphic imagery of the wall rock.
- Ground-penetrating radar carried by the rover, with center frequency adjustable across 100-500 MHz. Frequency selection basis: in 500 MHz mode, vertical resolution can reach 0.3 m but penetration depth is limited to <= 5 m; in 100 MHz mode, penetration can reach 15 m but resolution drops to 1.5 m. Mission Group II should prioritize 300-500 MHz for high-resolution shallow probing of skylight roofs <= 10 m thick, while Mission Group III deep-hole work should use 100-200 MHz for deeper geologic structure probing. Lunar GPR operating frequency should be somewhat increased relative to terrestrial reference systems to accommodate lower water content and higher required resolution in lunar regolith. Required penetration depth is >= 10 m in dry regolith at 100 MHz, with vertical resolution <= 0.5 m at 500 MHz. This payload is used for non-invasive probing of subsurface structure around the skylight, to confirm underground cavity extension direction and roof thickness. Its design references WISDOM-class GPR technology [30]. **On the lander deployed around Shackleton, this payload has the highest-priority exploration task and must complete a gridded GPR survey of at least a 200 m by 200 m area around the skylight within 30 Earth days after landing, using grid spacing <= 5 m.**
- **Autonomy requirement**: The hopper probe must autonomously maintain a safe distance of at least 5 m from the skylight edge. If its distance to the cave wall drops below 2 m during descent, it must automatically initiate obstacle avoidance and climb back to a safe altitude. Initial horizon identification and cavity-signal marking from GPR data must be performed autonomously onboard the rover to reduce Earth-downlink volume.
- The design draws on the successful detection experience of Kaguya LRS and LRO Mini-RF at Marius Hills and the Mare Tranquillitatis Pit [19,21].

#### 1.5.3 Lunar Surface Technology Demonstrations

**Regolith 3D-printing experiment**

- Printing mode: direct concentrated-sunlight sintering as the main option; laser powder-bed fusion as backup
- Printed part size >= 300 x 300 x 100 mm
- Printing rate >= 100 cm3/h
- Printing precision, dimensional tolerance, <= +/-2 mm
- **Autonomy requirement**: The printing system must have online quality monitoring capability. By using a thermal-imaging camera to monitor melt-pool temperature in real time, it must autonomously adjust the scan speed and dwell time of the focused energy spot to keep melt-pool temperature within the target band of +/-30°C.
- The experiment must test the following three regolith samples separately: (a) high-quality construction-material regolith satisfying the criteria in Section 1.3(b); (b) single-grade regolith with >80% fine particles; and (c) unscreened raw regolith.
- Acceptance criteria: printed parts made from high-quality feedstock (a) must reach compressive strength >= 15 MPa, with a target of 20 MPa, dimensional deviation <= +/-3 mm, and production rate >= 5 blocks/h. Comparison samples (b) and (c) must achieve compressive strength >= 5 MPa.

**In-situ catalyst extraction experiment**

- Processing capacity >= 5 kg regolith per batch
- Target extracted elements: Fe, Ni, Co, preferably using titanium-rich mare-basalt regolith satisfying the criteria in Section 1.3(c), with ilmenite content >= 10 wt%
- Extraction consists of two stages: (a) physical concentration via crushing + magnetic separation; (b) chemical extraction via acid leaching + hydrogen reduction
- Product purity: >= 90% in metallic state after chemical extraction; after physical concentration, lower-purity products of 40%-60% are acceptable for direct testing of FCCVD catalytic activity
- Energy consumption <= 50 kWh/kg for the chemically extracted product and <= 5 kWh/kg for physical concentration
- **Autonomy requirement**: The reactor must monitor target metal-ion concentration in the leachate through online spectroscopy and autonomously determine the end point of leaching, then switch to the next process step.
- Acceptance criterion: the catalytic activity of the chemically extracted product in later FCCVD CNT-growth experiments must be comparable to that of Earth-produced catalysts of the same purity, with CNT yield deviation no greater than +/-20%.

**Small lunar nuclear power source validation**

- Reactor type: Kilopower-class Stirling space reactor as the primary option
- Backup options: if Kilopower-class systems are unavailable because of fuel supply-chain constraints, switch to a Chinese space reactor design, such as a lunar nuclear-power concept from the Chang'e pre-research program, or a Russian ABV-6E-class reactor, provided the same power-class requirement, >= 3 kWe, is met.
- Rated electric power >= 3 kWe
- Design life >= 5 years
- Fuel: highly enriched uranium, HEU, with U-235 enrichment >= 93%
- Total mass including shielding <= 1,500 kg
- **Autonomy requirement**: The reactor control system must be capable of fully autonomous power regulation, adjusting reactivity drum position according to load demand and heat-rejection conditions, and maintaining safe operation for at least 90 days without Earth command.
- Acceptance criterion: complete at least 12 months of continuous operation with zero unplanned shutdowns and electric-output degradation <= 5%. A technical scheme in this power class may reference NASA's Kilopower / KRUSTY project [31].


### 1.6 Mission Group III: First Crewed “Lunar Sentinel” Stay (Years 5-8)

#### 1.6.1 Mission Overview

“Lunar Sentinel” is the core mission of Stage I and the historic turning point that marks the transition from robotic prospecting to direct human participation.

#### 1.6.2 Overall Mission Parameters

- Crew size: 4-6 personnel
- Stay duration: no less than 30 Earth days, with a target of 60 days, covering at least one full lunar day and the initial part of the lunar night
- The mission includes two landing sites: the primary landing site is in the south polar region, a candidate area on the rim of Shackleton crater to be finalized from Mission Groups I and II data; the secondary site is a candidate lava-tube skylight chosen from Mission Groups I and II data as the best accessible target, to be explored up close by hopper probe or rover, while the crew does not land directly in the skylight area. **In the priority ranking for field lava-tube exploration targets, the Shackleton periphery, if Mission Group II identifies a qualifying skylight there, and Philolaus crater are tied for top priority, ahead of Marius Hills.**
- The launch window is selected at the start of lunar daytime in order to maximize surface working time.
- The transportation system may reuse the infrastructure of China's crewed lunar landing program: Long March 10 launch vehicle + Mengzhou crewed spacecraft + Lanyue lunar lander [11,12].
- Ascent and return concept: the crew returns from the surface using the ascent stage of the Lanyue lunar lander to lunar orbit, docks with the Mengzhou crewed spacecraft, and then returns to Earth.

#### 1.6.3 Design Requirements for Lunar Surface Facilities

**Pressurized habitation module** (pre-deployed by cargo lander)

- Internal usable volume >= 50 m3
- Radiation shielding: module structure must provide no less than 20 g/cm2 aluminum-equivalent shielding, or alternatively use lunar-regolith cover of no less than 50 cm thickness. The cover layer should preferably use sintered bricks made from high-quality construction-material regolith that satisfies the criteria in Section 1.3(b), so that radiation shielding, micrometeoroid protection, and thermal inertia requirements are met simultaneously. Its specific shielding effectiveness will be cross-validated after Mission Group III against P2-M3, precise radiation-shielding simulation.
- Airtightness: leakage rate <= 0.1% per day at cabin pressure 70 kPa with oxygen-nitrogen mixed atmosphere
- Design life >= 10 years, allowing reuse by later missions during uncrewed intervals
- Total mass <= 8,000 kg
- **Autonomy requirement**: The habitation module must be equipped with an autonomous environmental control system capable of maintaining internal temperature, pressure, and atmospheric composition without crew onsite. If anomalies occur, it must autonomously execute preset fault-handling and isolation procedures and send alerts to Earth through the relay network [5].

**Inflatable expansion module** (deployed by the crew)

# Appendix I: Lunar Industry

## Volume V: Manufacturing System

**Version**: 1.4<br/>
**Date**: May 2026<br/>
**Currency Unit**: RMB (Y)<br/>
**Related Main Volumes**: Main Volume II (Material Parameters), Main Volume VII (Engineering Verification)<br/>
**Prerequisite Reading**: Appendix I Volume I (Pioneer Missions), Volume II (Siting and Infrastructure), Volume III (Energy System), Volume IV (Resource Prospecting and Mining Engineering)


### Terminology Table

| Abbrev. | Chinese Term | Description |
|------|----------|------|
| 3D | Three-dimensional | Three-Dimensional |
| C/SiC | Silicon-carbide-fiber-reinforced composite | High-temperature structural material |
| CELSS | Closed ecological life-support system | Self-circulating life-support system |
| CFRP | Carbon-fiber-reinforced polymer | Lightweight high-strength structural material |
| CNT | Carbon nanotube | Core cable material for the ring and lunar industry |
| CVD | Chemical vapor deposition | Core CNT process, lunar mass-production version |
| DEM | Discrete element method | Discrete Element Method |
| EMS | Electromagnetic stirring | Non-contact stirring for high-temperature melt pools |
| EVA | Extravehicular activity | Astronaut operations on lunar surface or in space |
| FCCVD | Floating-catalyst chemical vapor deposition | Main route for continuous CNT production, lunar mass-production version |
| FFC | FFC Cambridge process | Fray-Farthing-Chen process; direct electroreduction of solid oxides |
| GCR | Galactic cosmic rays | High-energy radiation particles from outside the Solar System |
| HRA | Rockwell hardness A scale | Hardness scale for hard alloys |
| HRC | Rockwell hardness C scale | Hardness scale for hardened steels |
| HV | Vickers hardness | Microhardness scale |
| ISRU | In-situ resource utilization | Manufacturing and survival using local lunar resources |
| kWe | Kilowatt electric | Electric power output unit |
| kWh | Kilowatt-hour | Energy unit |
| LIBS | Laser-induced breakdown spectroscopy | Online elemental analysis |
| LISAP-MSE | Lunar In-Situ Aluminum Production via Molten Salt Electrolysis | Aluminum production route on the Moon |
| MLI | Multi-layer insulation | Reflective passive insulation for vacuum thermal control |
| MWe | Megawatt electric | Electric power output unit |
| MWt | Megawatt thermal | Thermal power unit for heat collection/storage |
| NaK | Sodium-potassium alloy | Liquid-metal working fluid for active cooling loops |
| NASA | National Aeronautics and Space Administration | U.S. space agency |
| np-Fe | Nanoscale metallic iron particles | Naturally occurring nano-iron in regolith, particle size <100 nm |
| PE | Polyethylene | High-density polyethylene radiation-moderation layer |
| PTFE | Polytetrafluoroethylene | Sealing material with low friction and wide-temperature vacuum compatibility |
| RHU | Radioisotope heating unit | Device that uses decay heat for thermal maintenance |
| SPE | Solar particle event | High-energy particle bursts from solar eruptions |
| SPUA | Spray polyurea elastomer | High-elasticity waterproof coating for cave-wall microcrack sealing |
| SSAP | Silicate-sulfuric-acid process | Sulfur extraction and sulfuric-acid production from lunar sulfides |
| WC-Co | Tungsten-carbide-cobalt hard alloy | High wear-resistance material |
| XRF | X-ray fluorescence spectrometer | In-situ rapid elemental analysis for regolith |
| Ilmenite | Ilmenite (FeTiO3) | Most critical Fe-Ti oxide mineral in mare basalt |
| High-calcium plagioclase | High-calcium plagioclase (CaAl2Si2O8) | Major mineral in highland anorthosite with high Ca and Al content |
| Anorthite | Anorthite (CaAl2Si2O8) | Al-rich silicate mineral broadly distributed in lunar highlands |
| Troilite | Troilite (FeS) | Common sulfide mineral in mare basalt |
| Hadfield steel | High-manganese steel | Wear-resistant material for crusher hammers and liners |
| Bimodal grading | Bimodal size distribution | Coarse/fine dual-dominant particle distribution in regolith |
| Cryolite | Cryolite (Na3AlF6) | Electrolyte for molten-salt aluminum electrolysis |
| Carbonaceous chondrite | Carbonaceous chondrite | Primitive asteroid material rich in C, H₂O, and organics; impact residues on Moon |
| Solar-wind implanted volatiles | Solar-wind implanted volatiles | H/He/C/N ions implanted into near-surface regolith grains |
| Curie temperature | Curie temperature | Critical temperature where ferromagnetism is lost |


### 5.1 Introductory Statement

This volume is positioned as the **manufacturing core** of the lunar industrial system and focuses on the following core questions:

> How are extracted lunar construction aggregates, metallic concentrates, water ice, and regolith mineral fractions converted on the Moon into practical construction materials, industrial feedstocks, and CNT cables? Where does aluminum come from? Where does carbon come from? Where does sulfur come from? Where does titanium come from? Is every key feedstock fully closed-loop and traceable? Is every major regolith element maximally utilized? How much electric power do lunar construction-material lines and metallurgical furnaces require? When can the CNT factory scale from experimental to industrial operation? What is the total launch mass of all Earth-supplied production equipment? Can these processes operate reliably under lunar vacuum and low gravity? Could coupled high-temperature and magnetic-field effects degrade product quality?

This volume inherits:

- **Volume I (Pioneer Missions)**: confirmed feasibility of in-situ CNT production (P0-M2) and reserves of construction and catalyst feedstocks (P0-M7, P0-M8).
- **Volume II (Siting and Infrastructure)**: determined deployment locations for construction-material lines and metallurgical furnaces (surface or underground industrial sections).
- **Volume III (Energy System)**: provided medium-/high-temperature process-heat interfaces for sintering, metallurgy, and CNT production.
- **Volume IV (Resource Prospecting and Mining Engineering)**: defined supply quantity and grade standards for construction aggregates, metallic concentrates, and water ice.

Core tasks of this volume:

1. Clarify all key materials in the full chain, Al, Fe, Ti, C, S, Si, O, including source, intermediate conversion path, and final destination, and remove logical gaps such as where Al comes from.
2. Build a **full-chain material-balance model** from Volume IV mining output to Volume V manufactured products, ensuring capacity matching without bottlenecks or redundant overbuild.
3. Design complete process flow and production targets for lunar construction-material lines.
4. Build a **cascaded utilization system** for each size fraction after aggregate screening, prioritize extraction of high-value components (Al, Ti, Fe, catalyst precursors), and route residual fractions to construction materials, upgrading regolith utilization from merely sufficient to optimized.
5. Design phased construction for CNT mass-production plants and process flow for metallurgical workshops.
6. Provide order-of-magnitude estimates for mass, energy consumption, and output of all manufacturing equipment.
7. Evaluate process adaptability in lunar vacuum and low gravity, especially the coupled effect of high temperature and magnetic fields on slag-metal separation quality.
8. Define phased validation criteria for the manufacturing system.


### 5.2 Full-Chain Feedstock Sources, Intermediates, and Final Products

Before detailing specific manufacturing steps, all key feedstocks must be fully mapped to eliminate any missing source logic.

#### 5.2.1 Aluminum Source: Complete Path from Regolith to Ingot

In mare basalt, Al is primarily hosted as alumina ($Al_2O_3$) in plagioclase/anorthite ($CaAl_2Si_2O_8$), not in ilmenite concentrate. Ilmenite itself does not contain Al, so aluminum ingots cannot be produced from ilmenite concentrate.

The primary aluminum source is regolith aluminosilicates, extracted through two routes.

**Route 1: Aluminothermic Reduction + Molten-Salt Electrolysis (Primary Route)**

This closed-loop route is designed for lunar ISRU. A Missouri S&T team has extracted aluminum above 85% purity from lunar simulants via molten-salt electrolysis [11]. Experiments on MLS-1 and NEU-1 simulants produced Al-Si-Ti-Fe alloy products [18]. Process:

1. **Aluminothermic reduction**: Use regolith containing plagioclase/anorthite ($Al_2O_3$ about 10%-20%) and metallic Al reducing agent at 940-2,200 C for 2-6 h. After slag-metal separation, products are Al-Si-Fe alloy and Al2O3-rich mixed oxide slag [18].
2. **Molten-salt electrolysis**: Dissolve Al2O3-rich mixed oxide slag into cryolite-based electrolyte and perform inert-anode electrolysis. Oxygen evolves at anode (supplementing life support), while metallic Al (>=85% purity) forms at cathode [10].

Key point is **initial Al closed-loop circulation**: most Al consumed in aluminothermic reduction is recovered in subsequent electrolysis, with net Al loss only about 10%-20%. However, cycle startup needs initial Al inventory, first batch about 500 kg launched from Earth. After startup, only limited make-up Al is needed to compensate unrecoverable losses.

**Route 2: LISAP-MSE Direct Molten-Salt Electrolysis (Long-Term Route)**

This route uses anorthite, widely distributed in lunar highlands, and directly reduces alumina to Al and O2 in molten salt, without aluminothermic pre-step. After chemical pre-treatment isolates Al2O3 from anorthite, molten-salt electrolysis produces Al and O2 [11]. This route removes dependence on Earth-supplied startup Al and becomes preferred in Stage 3 (mature industrial phase).

**Initial Al supply strategy**: Stage 1 (Infrastructure Phase II) uses Route 1 with first 500 kg Al from Earth. Stage 2 (early industrialization) raises Al loop recovery to >=90%, reducing make-up demand to <=50 kg/year. Stage 3 shifts to Route 2 (LISAP-MSE), eliminating Earth dependence for Al.

#### 5.2.2 Sources of Iron, Titanium, and Oxygen

Ilmenite ($FeTiO_3$) in mare basalt is the shared source of Fe, Ti, and O.

**Route 1: Hydrogen Reduction (Primary Route)**

Hydrogen reduction of ilmenite at about 1,000 C yields metallic Fe, TiO2 slag, and H₂O. Water is electrolyzed to recycle H₂, and oxygen supplements life support. TiO2 slag can then be lithium-reduced to Ti-Si alloy and electrorefined to metallic Ti [12]. A Ningbo Institute team found ilmenite has the highest hydrogen content among Chang'e-5 regolith minerals. At high temperature, hydrogen reacts with iron oxides to produce metallic iron and significant water, about 51-76 mg H₂O per gram regolith, published in *The Innovation* [20].

**Route 2: FFC Cambridge Molten-Salt Electrolysis (Long-Term Route)**

At 900 C in CaCl2 molten salt, electrolysis of JSC-1A simulant via FFC Cambridge process achieved 83.47% Fe extraction and 79.65% current efficiency [24]. This route needs neither hydrogen nor aluminothermic pre-step and can directly produce Fe from regolith.

**Oxygen co-production**: both routes co-produce O2. Stage 2 production of 100-500 kg Fe ingots per month co-produces about 30-150 kg O2 per month as supplemental life-support oxygen.

#### 5.2.3 Carbon Sources

Local lunar carbon mainly comes from four sources:

**(a) Carbonaceous-chondrite impact residues**

Carbonaceous-chondrite impact residues are distributed across lunar surface. CI-type carbonaceous chondrites are rich in carbon (about 3%-5%) and water (about 3%-22%) [Main Volume II references 2.12-2.13]. In 2021, Chinese researchers identified million-year-scale carbonaceous impact residues on the lunar surface using Chang'e-4 imagery and spectral data; hyperspectral imaging indicated high-concentration (47%) carbonaceous material. Results were published in *Nature Astronomy* [15]. Heating collected residues in sealed chambers to about 600-1,000 C pyrolyzes organics and carbonates, releasing $CO_2$, $CH_4$, and $H_2O$. Lunar volatile separation and purification can use lunar-night low-temperature condensation, achieving >90% volatile recovery and >99% purity [19].

**(b) Polar CO₂ cold traps**

Schorghofer and Williams (2021) first confirmed polar CO₂ cold traps using LRO data, total area about 200 km2 [13]. Collected CO₂ is converted to methane through Sabatier reaction as FCCVD carbon feedstock. This route scale depends on reserve confirmation by Volume I Mission Groups II/III.

**(c) Solar-wind implanted volatiles**

Solar-wind H/He/C/N ions are implanted into near-surface regolith grains over long timescales. Fine regolith (<1 mm) heated to about 700 C can release these volatiles: H (for H₂ production/reductant), He-3 (long-term fusion reserve), and C/N (CNT carbon source and life-support nitrogen supplement).

**(d) Asteroid-derived carbon capture (long-term main source)**

After capture of C-type asteroids and transfer to cislunar space, in-orbit pyrolysis extracts hydrocarbons that are chemically converted and supplied to lunar CNT plants. This route is handled in Main Volume II Section 2.5.6 and is long-term primary carbon source for large-scale CNT production. In Stages 1-2, carbonaceous residues and polar CO₂ cold traps are supplementary sources.

#### 5.2.4 Sulfur Sources

Sulfur in lunar regolith mainly occurs as troilite ($FeS$), broadly distributed in basalt, with sulfur abundance about 0.05%-0.2%. The silicate-sulfuric-acid process (SSAP) can extract sulfur and prepare sulfuric acid from native lunar sulfides such as troilite, then dissolve silicates to extract Fe, Si, O, and other resources [14]. Chang'e-6 analysis of troilite in 4.2 Ga high-Al basalt further confirms sulfur occurrence/evolution in lunar crust [Main Volume II reference 2.11].

Stage 1 (Infrastructure Phase II) uses simple thermal decomposition for sulfur extraction: heat to 800-1,000 C in sealed chambers, release sulfur vapor from troilite decomposition, and condense to solid sulfur. Stage 2 introduces SSAP, forming closed-loop synergy between sulfur extraction and metal extraction with significantly improved utilization.

#### 5.2.5 Sources of Silicon and Oxygen

Si and O are the two most abundant regolith elements. Nearly half of regolith is oxygen bound in oxides of Fe/Ti/Si/Al and others. Silicon occurs broadly as $SiO_2$ in plagioclase, pyroxene, and glassy phases. As major byproducts of aluminothermic reduction and molten-salt electrolysis, Si is produced as Al-Si-Fe alloy and can be used directly in structural materials. Oxygen is co-produced through multiple routes, aluminothermic byproducts, ilmenite hydrogen-reduction byproducts, and molten-salt electrolysis anode evolution, supplementing base life-support oxygen.

A Deep Space Exploration Laboratory molten-salt regolith electrolysis oxygen prototype has achieved simultaneous in-situ oxygen production and high-strength Si-Al alloy preparation, supporting future lunar life support and in-situ construction [23]. Blue Origin's Blue Alchemist reactor has also extracted oxygen from regolith simulants via electrochemical current and can further refine silicon for radiation-resistant solar cells [22].


### 5.3 Full-Chain Capacity Matching and Material Balance

#### 5.3.1 End-to-End Chain from Feedstock to Products

Before specific process design, this section builds full material balance from Volume IV mining output to Volume V manufacturing output, ensuring no chain breaks or redundant excess. All flows below use Stage 2 (Infrastructure Phase II) as baseline.

**(a) Construction aggregate -> construction-material chain**

- **Input (Volume IV Section 4.9.4)**: Stage 2 aggregate mining >=500 m3/month, about 750-1,000 t at loose bulk density 1.5-1.8.
- **Process chain**: coarse crushing/screening at mine -> transport to base -> cascaded sorting (Section 5.4) with high-value extraction priority -> residual materials to construction lines (Section 5.5).
- **Outputs**:
  - Sintered regolith bricks: >=500 standard bricks/day, >=15,000/month. Single-brick mass about 2.8 kg, monthly output about 42 t.
  - Regolith concrete: >=5 t/month.
- **Material balance**: from 500 m3/month, about 70% enters qualified size range (<=50 mm), about 560 t/month usable aggregate. After cascaded sorting, about 30%-40% high-value fractions are extracted first (about 170-220 t/month), leaving about 340-390 t/month for construction lines. Construction lines consume only about 47 t/month, so **aggregate supply has substantial margin**; surplus is used for roads, radiation cover, and temporary structures.

**(b) Ilmenite concentrate -> metallurgy chain**

- **Input (Volume IV Section 4.10.2)**: Stage 2 metal-mineral mining >=100 m3/month (about 200-300 t ROM ore). After magnetic separation, concentrate at >=30% $FeTiO_3$, monthly output about 20-30 t concentrate.
- **Process chain**: magnetic concentrate -> transport to base -> metallurgical workshop (Section 5.5).
- **Outputs (Stage 2)**:
  - Fe ingots: 100-500 kg/month (hydrogen reduction or aluminothermic route).
  - Al ingots: 100-500 kg/month (aluminothermic + molten-salt electrolysis, supplied from plagioclase feedstock, not ilmenite concentrate).
  - O2 byproduct: 30-150 kg/month.
- **Material balance**: 20-30 t/month concentrate greatly exceeds initial furnace demand at hundred-kg scale. Concentrate accumulates as strategic stock for Stage 3 scale-up.

**(c) Water ice -> CNT manufacturing chain**

- **Input (Volume IV Sections 4.8.2-4.8.3)**: Stage 1 (Infrastructure Phase II) about 200-500 L per lunar day (two drills). Stage 2 (early industrialization) about 2,000-5,000 L per lunar day (four drills + plant waste-heat assistance).
- **Process chain**: liquid water -> electrolysis to hydrogen -> CNT carbon feedstock from pyrolyzed carbonaceous residues + catalyst from magnetic concentrate or Fe ingots -> FCCVD reactor (Section 5.6).
- **Outputs**:
  - Stage 1: about 10-50 kg/month CNT yarn from pre-weaving line.
  - Stage 2: >=1,000 kg/month CNT yarn from industrial FCCVD line.
- **Material balance**: Stage 1 water is limited and carbon source is mainly carbonaceous residues. With 500 L/month water and carbon-source mass ratio about 2:1, max carbon feedstock is about 250 kg/month. At ~50% CNT yield, theoretical upper bound is about 125 kg/month CNT. In Stage 2, with >=2,000 L/month water and higher residue collection efficiency, CNT output can exceed 1,000 kg/month, aligned with Volume II P1-M4 criteria.

#### 5.3.2 Full-Chain Summary of Key Materials

| No. | Feedstock | Source | Intermediate | Final Product | Use | Capacity Node |
|:---:|:---|:---|:---|:---|:---|:---|
| 1 | Regolith (surface plagioclase fraction) | Volume IV aggregate pits | Al2O3-rich mixed oxides | Al metal (>=85% purity) | Structural Al alloys; reducing agent loop | Same stage as Fe output |
| 2 | Ilmenite concentrate | Volume IV metallic-mineral pits + magnetic separation | Fe metal + TiO2 slag + H₂O | Fe ingots (>=90%); Ti metal (Stage 3) | Structural, CNT catalyst, oxygen route | P2-F1 |
| 3 | Ilmenite concentrate + H₂ | Same as above + water electrolysis | $H_2O + Fe + TiO_2$ | $O_2 + Fe + Ti$ | Life support, catalyst precursor | Synchronous with Fe output |
| 4 | Carbonaceous-chondrite residues | Surface collection | $CO_2 + CH_4 + H_2O$ | $CH_4$ (via Sabatier) | CNT carbon source; life-support carbon loop | P1-F3 |
| 5 | Polar CO₂ cold traps | Polar PSRs | $CO_2$ | $CH_4$ (via Sabatier) | Same as above | Reserve confirmation pending Volume I |
| 6 | C-type asteroid carbon source | Asteroid capture and transfer | Hydrocarbon mixed gas | $CH_4$, $H_2$ | Main CNT carbon source (Stage 3) | Main Volume II |
| 7 | Mare basalt regolith | Volume IV metallic-mineral pits | H₂S, steam | Sulfur, H₂ | Regolith-concrete binder; oxygen route | P1-F2 |
| 8 | Troilite | Regolith magnetic-separation tailings | $SO_2 + H_2SO_4$ | Sulfuric acid + Fe + Si + O | Mineral dissolution, metal extraction, materials | Stage 3 |
| 9 | Water ice | Volume IV ice mining fields | $H_2 + O_2$ | H₂, O2, H₂O | Propellant, life support, CNT conversion | P1-R1 |
| 10 | Initial Al ingots | Earth launch (first 500 kg only) | - | - | Startup reductant for aluminothermic loop | Stage 1 |
| 11 | Fine surface regolith | Fine-screening output from Volume IV aggregate pits | Nano $TiO_2$ + nano Fe particles | Photocatalyst | Water splitting for H₂; $CO_2$ reduction to fuel | Stage 3 |


### 5.4 Cascaded Feedstock Sorting and Full-Component Utilization

Volume IV mining separates aggregate pits and metal-mineral pits, stabilizing feed grade for furnaces. However, aggregate-pit output still contains significant high-value components. Sending all of it directly to bricks/concrete wastes scarce resources. This section establishes cascaded utilization from post-screening fractions to raise full-component utilization from sufficient to optimized.

#### 5.4.1 Value Potential of Each Post-Screening Size Fraction

Regolith from Volume IV aggregate pits is divided into three fractions after crushing and screening. A **cascaded sorting step** is inserted before construction lines to extract high-value components first and send residuals to construction materials.

| Fraction | Size Range | Main Minerals | High-Value Uses | Recommended Separation Method |
|:---|:---|:---|:---|:---|
| **Coarse** | 10-50 mm | Basalt fragments, plagioclase fragments, breccia | (i) Plagioclase-rich fragments -> anorthite Al feedstock for molten-salt electrolysis; (ii) ilmenite-rich fragments -> crushed and routed to magnetic separation; (iii) residual -> construction aggregate | Machine vision + online LIBS sorting |
| **Medium** | 1-10 mm | Plagioclase, pyroxene, ilmenite, glassy phase | (i) ilmenite grains -> magnetic concentration; (ii) ilmenite+glassy grains -> hydrogen-reduction oxygen + Fe route; (iii) residual -> sintered-brick skeleton grains | High-gradient magnetic separation + electrostatic sorting |
| **Fine** | <1 mm | Powdered plagioclase, pyroxene, glassy phase, np-Fe, fine ilmenite | (i) np-Fe-rich part -> catalyst precursor (direct use after ball milling); (ii) fine ilmenite -> hydrogen-reduction oxygen route; (iii) nano $TiO_2$ + nano Fe -> photocatalyst (H₂ production by water splitting). Xinjiang-based teams have prepared fiber photocatalysts from regolith with in-situ rutile TiO2 and Fe nanoparticles, enabling efficient organic degradation by dual mechanisms [16]; (iv) fines with implanted solar-wind H/He -> volatile release by heating; (v) residual -> 3D-print powder-bed feedstock | Electrostatic traveling-wave screening (<100 um precision) + magnetic separation |

#### 5.4.2 Full-Component Utilization Flow

Following the principle high-value extraction first -> cascaded utilization -> residuals to construction, full-chain flow is:

```text
Raw regolith ore (Volume IV mining fields)
        |
        v
[Coarse crushing + screening]
        |
        |-- Coarse fraction (10-50 mm) --> machine-vision sorting
        |                                  |-- anorthite-rich fragments --> molten-salt electrolysis for Al --> Al ingots
        |                                  |                                         '-- O2
        |                                  |-- ilmenite-rich fragments --> crushing + magnetic separation --> concentrate
        |                                  |                                              '-- tailings --> construction aggregate
        |                                  '-- other fragments --> construction aggregate
        |
        |-- Medium fraction (1-10 mm) --> high-gradient magnetic separation
        |                                  |-- magnetic fraction (ilmenite + metallic Fe) --> concentrate storage
        |                                  |      |-- hydrogen reduction --> Fe ingot + H₂O + TiO2 slag
        |                                  |      |-- aluminothermic reduction --> Al-Si-Ti-Fe alloy
        |                                  |      '-- FFC electrolysis --> pure Fe
        |                                  '-- nonmagnetic fraction --> sintered-brick skeleton grains
        |
        '-- Fine fraction (<1 mm) --> electrostatic traveling-wave screening (<100 um)
                  |
                  |-- nano TiO2 + Fe particle phase --> photocatalyst production
                  |
                  |-- np-Fe enriched phase --> ball milling --> CNT catalyst precursor
                  |
                  |-- fines with solar-wind H/He --> thermal volatile release
                  |      |-- H₂ --> reductant, fuel
                  |      |-- He-3 --> long-term fusion reserve
                  |      '-- C, N --> CNT carbon source, life-support supplement
                  |
                  '-- residual fines --> 3D-print powder-bed feedstock
```

**Full-process utilization target**: by end of Stage 2 (Infrastructure Phase II), >=70% of high-value components in regolith entering construction lines are extracted in pre-sorting; only residuals go to bricks/concrete. In Stage 3 (mature industrialization), full-component utilization target is >=95%.

#### 5.4.3 Phased Cascaded-Utilization Strategy

When early infrastructure has limited equipment, full separation need not be completed in one step. Phased rollout:

**Stage 1 (Infrastructure Phase I):** only coarse crushing + screening. Medium and fine fractions directly feed bricks/concrete. Goal is immediate usability.

**Stage 2 (Infrastructure Phase II, primary scope of this volume):** add one high-gradient magnetic separator after medium-fraction screening (already listed in Volume IV Section 4.10.2 equipment list) to enrich ilmenite and other magnetic minerals into concentrate. For fine fractions, np-Fe-rich part (about 5%-10% of total fines) is separated by electrostatic traveling-wave screening and used as supplemental CNT catalyst precursor. Coarse-fraction machine-vision sorting is deferred to Stage 3.

**Stage 3 (mature industrialization):** add full-component sorting system (machine vision + fine electrostatic traveling-wave screening + online LIBS), enabling cascaded extraction of all high-value components. Construction lines mainly consume post-sorting residuals.


### 5.5 Construction-Material Production Lines

#### 5.5.1 Phased Capacity and Deployment

| Stage | Period | Sintered-Brick Capacity | Concrete Capacity | Deployment | Alignment with Infrastructure Progress |
|:-----|:-----|:-----|:-----|:-----|:-----|
| **Stage 1** | Infrastructure Phase I | 50-100 bricks/day (mobile sintering unit) | None (sulfur extraction line not yet online) | Surface or underground industrial section | Volume II Section 2.7.2 |
| **Stage 2** | Infrastructure Phase II | >=500 bricks/day (fixed automated line) | >=5 t/month | Surface or sealed underground industrial section | Volume II Section 2.7.3 |
| **Stage 3** | Early industrialization | >=2,000 bricks/day | >=20 t/month | Same location with expanded capacity | Volume II Section 2.6.1 |

#### 5.5.2 Automated Sintered-Brick Line (Stage 2)

**(a) Feed preparation**

- Use residual medium fraction (1-10 mm, skeleton grains) and residual fine fraction (<1 mm, filling powder) after cascaded sorting in Section 5.4.
- Mix two fractions at about 1:1 in automatic batching unit. If feed contains >=10 wt% glassy binder phase, no extra binder is required [5][6][7].

**(b) Sintering process**

- **Heating mode (Stage 2)**: use medium-temperature extraction steam from Volume III Section 3.5.7 (200-500 C) as auxiliary heating for mold/feed preheat to about 200 C; use concentrated-solar furnace or resistive electric heating as primary source up to 1,000-1,200 C.
- **Mold specification**: standard brick mold $240 x 115 x 53$ mm3, multi-brick loading.
- **Cycle time**: about 30-60 min per batch (preheat + ramp + soak).

**(c) Automation configuration**

- Automatic batching system: about 3 kW, <=500 kg.
- Automatic press: about 5 kW, <=800 kg; preload >=10 MPa.
- Tunnel sintering furnace: about 20 kW, <=3,000 kg; continuous preheat -> high-temperature -> cooling zones.
- Automatic palletizer: about 2 kW, <=400 kg.

**(d) Quality control**

Per batch (~100 bricks), randomly sample 5 for compressive testing (target >=20 MPa) and dimensional tolerance check (<=3 mm). Failed batches are crushed and returned to feed preparation.

#### 5.5.3 Regolith Concrete Line (Stage 2)

**(a) Sulfur binder extraction**

- Feed: troilite ($FeS$) in Volume IV magnetic-separation tailings or raw regolith, sulfur abundance about 0.05%-0.2% [14].
- Process: heat regolith powder to 800-1,000 C in sealed chamber. Troilite decomposes and releases sulfur vapor, collected as solid sulfur by condenser. Heat provided by high-temperature extraction steam from Volume III plant or electric heating. Lunar high vacuum favors thermal decomposition of solids by lowering decomposition temperature and accelerating kinetics.
- **Throughput**: about 500 kg regolith/day processed, sulfur output about 0.5-1 kg/day (assuming 0.1% sulfur and 70% recovery).
- **Extractor mass**: <=500 kg (sealed heating chamber + condenser).

**(b) Concrete mixing and casting**

- Mix aggregate and sulfur at about 10:1 by mass.
- Heat in sealed mixer to 140 C (using plant low-temperature waste heat 30-50 C for preheat, with electric boost). Molten sulfur mixes uniformly with aggregate.
- Cast into molds and cool to set (about 1-2 h), no water curing required.
- **Total concrete-line power**: about 10-15 kW (mixer heating + transfer pump).
- **Total concrete-line mass**: <=3,000 kg.

**(c) Quality control**

For each batch (~1 t), sample compressive strength (target >=20 MPa). After 100 thermal cycles (-150 C to +120 C), strength degradation <=20% (Volume II P1-M2).


### 5.6 Metallurgical Workshop

#### 5.6.1 Phased Capacity and Deployment

| Stage | Period | Al Ingot Capacity | Fe Ingot Capacity | Deployment | Alignment with Infrastructure Progress |
|:-----|:-----|:-----|:-----|:-----|:-----|
| **Stage 1** | Second half of Infrastructure Phase II | 100-500 kg/month | 100-500 kg/month | Underground industrial section | Volume II Section 2.7.3 |
| **Stage 2** | Early industrialization | >=2,000 kg/month | >=5,000 kg/month | Same area with expansion | Volume II Section 2.6.1 |

#### 5.6.2 Aluminum Metallurgy: Aluminothermic + Molten-Salt Electrolysis (Stages 1-2)

**(a) Feedstocks**

- Regolith containing plagioclase/anorthite, $Al_2O_3$ about 10%-20%, from Volume IV aggregate pits or dedicated regolith pits.
- Reductant: metallic Al (first 500 kg from Earth, then recycled from electrolysis).
- Electrolyte: cryolite ($Na_3AlF_6$), first batch from Earth then recycled (net loss about 1%-2% per batch, small make-up required).

**(b) Process**

**Aluminothermic step:**

- **Furnace type**: DC arc furnace (shared with Fe metallurgy, Section 5.6.3), >=50 kg per batch.
- **Temperature**: 940-2,200 C, reduction duration 2-6 h [18].
- **Reductant**: Al powder or granules (initially Earth-supplied, later recycled).
- **Products**: Al-Si-Fe alloy (denser, lower phase) + Al2O3-rich mixed oxide slag (upper phase) [18].
- **Lunar adaptability**: perform inside fully sealed pressure vessel (1 bar Ar) to suppress electrolyte volatilization and safely collect gaseous products (oxygen) [10].
- **EMS-enhanced slag-metal separation**: under 1/6 g, gravity-only separation is inefficient. Integrate electromagnetic stirring in arc furnace to enhance mass transfer and droplet coalescence. Four-step refining is adopted: (i) low-frequency pulsed field in early slag-metal reaction to strengthen interfacial transfer; (ii) switch to rotating field for macro stratification; (iii) apply one-way traveling magnetic field at tapping channel to capture suspended inclusions; (iv) stop stirring and allow static settling/slag removal. This raises separation efficiency from <30% (low-g natural settling) to >90% without increasing equipment mass.

**Molten-salt electrolysis step:**

- **Cell**: inert anode ($SnO_2$-based or $NiFe_2O_4$-based ceramic), cathode in graphite or metal [10].
- **Electrolyte**: cryolite-based molten salt ($Na_3AlF_6$), operating at 940-960 C.
- **Feed**: Al2O3-rich mixed oxide slag from aluminothermic step.
- **Anode product**: $O_2$ routed to life-support or oxygen storage.
- **Cathode product**: metallic Al (>=85% purity), mostly recycled to next aluminothermic batch, with remainder delivered as product ingots.
- **Lunar adaptability**: electrolysis also runs in sealed pressure vessel. Reduced buoyancy convection under 1/6 g affects thermal/compositional uniformity; corrosion-resistant ceramic stirrer or electromagnetic circulation is required.

**(c) Energy and mass assessment**

- **Arc-furnace power**: about 50-100 kWe (single unit, shared with Fe).
- **Electrolysis-cell power**: about 20-30 kWe (single unit).
- **Overall Al yield**: with regolith $Al_2O_3$ at 15%, each 50 kg batch contains ~7.5 kg $Al_2O_3$ (~4 kg Al). At 70%-80% comprehensive recovery, Al output is about 2.8-3.2 kg per batch.
- **Initial Al consumption**: aluminothermic step consumes about 10%-20% Al per batch as unrecoverable loss; replenished from electrolysis output.
- **Electrolysis-cell mass**: <=3,000 kg including vessel, electrodes, electrolyte.

#### 5.6.3 Iron Metallurgy: Ilmenite Hydrogen Reduction (Stages 1-2)

**(a) Feedstocks**

- Ilmenite concentrate from Volume IV Section 4.10, grade >=30% $FeTiO_3$.
- Reductant hydrogen from water electrolysis (Volume III Section 3.3.3) or from water produced in carbonaceous-residue pyrolysis path (Section 5.2.3).

**(b) Process**

- **Furnace type**: sealed reduction furnace (non-arc), reducing ilmenite at about 1,000 C with hydrogen, >=50 kg per batch [20].
- **Heating mode**: high-temperature extraction steam (500-750 C) from Volume III Section 3.5.7 as auxiliary heating, with electrical boost to target temperature.
- **Reaction**: $FeTiO_3 + H_2 -> Fe + TiO_2 + H_2O$. Steam is condensed and water is electrolyzed to regenerate H₂.
- **Batch cycle**: about 3-5 h (heat-up + reduction + cool-down).
- **Products**: Fe ingots (>=90% purity, see Volume II P2-M1) and TiO2 slag (stored for Stage 3 Ti extraction).
- **Lunar adaptability**: ultrahigh lunar vacuum ($10^{-12}$ bar) provides favorable non-equilibrium thermodynamic condition. Vacuum pumping maintains very low oxygen partial pressure and continuously removes steam byproduct, shifting equilibrium toward metallic Fe by Le Chatelier principle. Furnace remains fully sealed; hydrogen runs in closed loop.

**(c) Energy and mass assessment**

- **Reduction-furnace power**: about 30-50 kWe (single unit).
- **Reduction-furnace mass**: <=3,000 kg including vessel, heaters, H₂ recirculation system.
- **Monthly electricity**: for 500 kg/month Fe output, about 10-20 batches/month (50 kg each), total 1,500-6,000 kWh/month, <3% of Infrastructure Phase II monthly generation.
- **Slag handling**: $TiO_2$ slag stored for Stage 3 lithium reduction or FFC electrolysis for Ti extraction [12].

#### 5.6.4 Catalyst Preparation (Shared with Metallurgical Workshop)

Stage 1 high-purity Fe ingots (>=90%) are ball-milled in sealed mill to <=10 um and can directly serve as FCCVD catalyst precursor for CNT production. This route was validated by Volume I P0-M2 in-situ CNT manufacturing [1][2]. In Stage 2, hydrometallurgical purification (acid leaching/hydrogen reduction) is added to raise Fe purity to >=99% for higher catalyst activity.


### 5.7 CNT Manufacturing Plant

#### 5.7.1 Phased Capacity and Deployment

| Stage | Period | Capacity | Equipment Type | Deployment | Alignment with Infrastructure/Main Schedule |
|:-----|:-----|:-----|:-----|:-----|:-----|
| **Stage 1** | Second half of Infrastructure Phase II | 10-50 kg/month CNT yarn | Small pre-weaving line (1-2 micro FCCVD reactors) | Sealed and pressurized underground industrial section | Volume II Section 2.7.3 P1-M4 |
| **Stage 2** | Early industrialization | >=1,000 kg/month CNT yarn | Industrial FCCVD multi-reactor parallel line | Same area, sealed section expanded to >=5,000 m2 | Main Volume II (start of CNT supply for ring construction) |

Note: Stage 1 is primarily for satisfying Volume II P1-M4 criteria, with only 10-50 kg/month output. Stage 2 >=1,000 kg/month begins meaningful supply capability. True large-scale supply requires Stage 3 (mature industrialization) at >=100 t/month.

#### 5.7.2 Small Pre-Weaving Line (Stage 1)

**(a) Process principle**

Inherit basic lunar FCCVD principle validated in Volume I P0-M2: use local catalyst (Fe-Ni particles from Section 5.6.4 or direct magnetic concentrate product) and carbon-source gas (pyrolysis gas from carbonaceous residues or CO₂ from cold traps, Section 5.2.3) to grow CNT yarn in micro FCCVD reactors. JAXA has demonstrated in-situ CVD growth on lunar simulant particles [1], confirming methane-fed direct synthesis feasibility. Natural SWCNT discovery in Chang'e-6 regolith provides environmental analog support [2]. Lab CNT fibers have reached dynamic strength up to 14 GPa [4].

**(b) Equipment configuration**

| Equipment | Power | Mass | Notes |
|:-----|:-----|:-----|:-----|
| Micro FCCVD reactor (1-2 units) | <=1 kW/unit | <=200 kg/unit | 600-1,200 C operation; carbon source methane or CO/H₂ mix [1]. Lunar vacuum is advantageous; no bulky high-capacity vacuum pumping needed. Use micro-pump only for pre-run chamber cleanup, then maintain controlled gas flow/pressure during reaction |
| Online Raman monitor | <=0.5 kW | <=50 kg | Real-time product quality monitoring (graphitization/defect peak intensity) with feedback control [3] |
| Yarn pre-weaving machine | <=2 kW | <=300 kg | Parallel alignment + interval bundling (per Main Volume VI Section 6.6.1), continuous pre-woven cable length >=1 km. At 1/6 g, winding tension control needs precise sensors and control to compensate changed catenary behavior |
| Carbon-source gas preparation system | <=3 kW | <=500 kg | Carbonaceous-residue pyrolysis + Sabatier conversion from CO₂ to methane [15][19] |

**(c) Catalyst supply routes (Stage 1)**

- **Route 1 (preferred)**: natural Fe-Ni particles from Volume IV Section 4.10.2 magnetic separation (grade >=60% Fe+Ni, recovery >=90%), then simple ball milling to <=10 um for direct FCCVD catalyst use. Lunar high vacuum avoids common Earth wet-separation issues such as surface oxidation/water adsorption, yielding cleaner particle surfaces. This route was validated in Volume I P0-M2 [1].
- **Route 2**: Fe ingots from Section 5.6.4, then sealed ball milling.

**(d) Capacity and energy**

- **Single reactor CNT yield**: about 0.1-0.5 kg per batch, depending on carbon feed and catalyst activity [1][3].
- **Batch duration**: about 4-8 h [1].
- **Electricity for 10-50 kg/month CNT yarn**: about 200-1,000 kWh/month including heating, monitoring, and pre-weaving; <1% of Infrastructure Phase II monthly generation.

#### 5.7.3 Industrial FCCVD Mass-Production Line (Stage 2)

**(a) Process upgrade**

Stage 2 expands Stage 1 micro reactors into parallel industrial reactors and upgrades:

- **Catalyst supply**: from simple mechanical size reduction to hydrometallurgical purification (acid leaching/hydrogen reduction), raising Fe-Ni purity to >=99%.
- **Carbon supply**: add larger CO₂ cold-trap intake on top of carbonaceous-residue source; reserve interface for asteroid-derived carbon feed [13].
- **Heating mode**: switch primary heat to high-temperature extraction steam from Volume III Section 3.5.7 (500-750 C); retain electric heating for precision control only, reducing unit electric intensity of CNT output.
- **Online QC**: install Raman monitor at each reactor outlet for feedback control [3].

**(b) Equipment configuration**

| Equipment | Quantity | Power per Unit | Mass per Unit | Notes |
|:-----|:-----:|:-----|:-----|:-----|
| Industrial FCCVD reactor | 4-6 | <=5 kW/unit | <=800 kg/unit | 600-1,200 C operation; each unit about 100-300 kg/month CNT [1][3] |
| Online Raman monitor | 4-6 | <=0.5 kW/unit | <=50 kg/unit | One per reactor [3] |
| Expanded yarn pre-weaving machine | 2 | <=5 kW/unit | <=600 kg/unit | Parallel alignment + interval bundling, multi-yarn throughput |
| Expanded carbon-gas preparation system | 2 sets | <=10 kW/set | <=1,500 kg/set | Scaled Sabatier reactor arrays |
| Catalyst purification system | 1 set | <=8 kW | <=1,200 kg | Hydrometallurgical purification (acid leaching/hydrogen reduction) |

**(c) Capacity and energy**

- **Total installed power**: about 50-80 kWe.
- **Electricity for >=1,000 kg/month CNT yarn**: about 5,000-8,000 kWh/month, excluding thermal load supplied by plant extraction steam.
- **Product specification**: single-yarn length >=10 km, tensile strength >=10 GPa (aligned with Volume II P1-M4), with downstream plying/braiding to reach main ring-cable engineering targets (>=20 GPa) [3][4].

**(d) Quality inspection and grading**

Per batch (~50 kg), CNT yarn is graded after:

- Tensile strength test (target >=10 GPa, single-fiber basis)
- SEM inspection for surface defects and broken filaments
- Raman graphitization check (G/D ratio >=5)

Batches meeting main-volume requirements are transported to GEO ring-construction sites through Appendix I Volume VI Earth-Moon transport system. Substandard batches are downgraded for internal base applications (conductive cable, CFRP reinforcement components).


### 5.8 Energy and Mass Summary of Manufacturing System

#### 5.8.1 Total Equipment Launch Mass (Stage 1: Infrastructure Phase II)

| Equipment | Quantity | Unit Mass | Subtotal | Notes |
|:-----|:-----:|:-----|:-----|:-----|
| Automated sintered-brick line | 1 set | <=6,700 kg | <=6,700 kg | Includes batching, press, furnace, palletizer [5][6][7] |
| Regolith concrete line | 1 set | <=3,000 kg | <=3,000 kg | Includes sulfur extraction, mixing, casting [14] |
| DC arc furnace (with EMS) | 1 | <=5,000 kg | <=5,000 kg | Includes vessel, transformer, electrodes, EMS coils |
| Al electrolysis cell | 1 | <=3,000 kg | <=3,000 kg | Includes vessel, electrodes, electrolyte [10][11] |
| Fe reduction furnace | 1 | <=3,000 kg | <=3,000 kg | Includes vessel, heaters, H₂ circulation [20] |
| Sealed ball mill | 1 | <=600 kg | <=600 kg | Catalyst precursor milling |
| Micro FCCVD reactor | 2 | <=200 kg each | <=400 kg | [1] |
| Online Raman monitor | 1 | <=50 kg | <=50 kg | [3] |
| Small yarn pre-weaving machine | 1 | <=300 kg | <=300 kg | - |
| Small carbon-source preparation system | 1 set | <=500 kg | <=500 kg | Carbonaceous pyrolysis + Sabatier [15][19] |
| Cascaded sorting system (Stage 2) | 1 set | <=2,000 kg | <=2,000 kg | High-gradient magnetic + electrostatic traveling-wave + machine-vision sorting [17] |
| **Total manufacturing launch mass** | - | - | **<=24,550 kg (~24.6 t)** | Includes Al cell, Fe furnace, EMS system |

#### 5.8.2 Manufacturing Energy Overview (Stage 1: Typical Lunar-Day Operation)

| Equipment/System | Quantity | Unit Power | Daily Operating Hours | Daily Energy | Energy Type |
|:-----|:-----:|:-----:|:-----:|:-----:|:-----|
| Automated sintered-brick line | 1 set | ~30 kW | 12 h | ~360 kWh | Electric cable supply |
| Regolith concrete line | 1 set | ~12 kW | 8 h | ~96 kWh | Electric cable supply |
| DC arc furnace (aluminothermic, with EMS) | 1 | ~85 kW | 6 h (every 2-3 days) | ~510 kWh/run | Electric cable supply |
| Al electrolysis cell | 1 | ~25 kW | 8 h (alternating with arc furnace) | ~200 kWh | Electric cable supply |
| Fe reduction furnace | 1 | ~40 kW | 6 h (every 2-3 days) | ~240 kWh/run | Electric cable supply |
| Micro FCCVD reactors (2) | 2 | ~1 kW each | 24 h continuous | ~48 kWh | Electric cable supply |
| Yarn pre-weaving machine | 1 | ~2 kW | 8 h | ~16 kWh | Electric cable supply |
| Carbon-source preparation | 1 set | ~3 kW | 12 h | ~36 kWh | Electric cable supply |
| Lighting and auxiliaries | - | ~2 kW | 12 h | ~24 kWh | Electric cable supply |
| **Total (typical lunar-day, excluding metallurgy intermittency)** | - | - | - | **~780 kWh/day** | - |

Metallurgical furnaces (arc + Fe reduction) are non-continuous, operating every 2-3 days. Monthly cumulative electricity is about 8,000-15,000 kWh, <5% of Infrastructure Phase II monthly generation. EMS additional power is about 5 kW and already included in arc-furnace total.


### 5.9 Adaptability Assessment for Lunar Vacuum, Low Gravity, and Magnetic Separation

This section assesses process adaptability in lunar vacuum and 1/6 g conditions, with emphasis on magnetic-separation impacts on product quality and coupled high-temperature/magnetic-field effects in slag-metal separation.

#### 5.9.1 Vacuum Impacts and Countermeasures

**(a) Aluminum production: aluminothermic + molten-salt electrolysis**. Under lunar vacuum ($10^{-12}$ bar) and 1/6 g, both processes must run in fully sealed pressure vessels (1 bar Ar) to suppress electrolyte volatilization and safely collect oxygen. All high-temperature reactors are designed accordingly (Section 5.6.2).

**(b) Iron/oxygen production: ilmenite hydrogen reduction**. Ultrahigh vacuum provides favorable non-equilibrium thermodynamic conditions. Vacuum pumping maintains low oxygen partial pressure and continuously removes steam byproducts, shifting equilibrium toward Fe formation. Reactor must be fully sealed with closed-loop hydrogen circulation (Section 5.6.3).

**(c) Sulfur binder extraction: troilite thermal decomposition**. Lunar vacuum is favorable to solid thermal decomposition. Near-vacuum decomposition lowers required temperature and accelerates reaction. Sulfur vapor is efficiently condensed under low lunar thermal background (Section 5.5.3).

**(d) CNT production: FCCVD reactors**. Native lunar vacuum is a major process advantage. Large vacuum-pump systems are unnecessary for low-pressure operation. A micro vacuum pump purges residual gases pre-run; controlled methane flow and pressure are maintained during reaction. Supported by Volume I P0-M2 analysis and JAXA studies [1] (Section 5.7.2).

#### 5.9.2 Low-Gravity (1/6 g) Impacts and Countermeasures

**(a) Slag-metal separation efficiency**. This is a key step after aluminothermic reduction. Under 1/6 g, gravity-only separation is insufficient. EMS-integrated four-step refining (pulse -> rotation -> one-way purification -> static settling) raises separation efficiency from <30% to >90% without mass increase (Section 5.6.2).

**(b) Coupled high-temperature and magnetic-field effects during slag-metal separation**. EMS in high-temperature melt requires assessment of potential quality degradation or unintended magnetization effects:

- **Magnetic behavior at high temperature and control**: magnetic materials become paramagnetic above Curie temperature and lose ferromagnetism. Curie temperatures of lunar reduced products (Fe, ilmenite-derived phases) are hundreds of Celsius, higher than magnetic-separation operating temperature (<100 C), so strong magnetic response remains during post-cooling magnetic separation. However, in high-temperature reducing atmospheres, some weakly magnetic phases may transform into stronger magnetic phases; if they enter metal phase they could become trace impurities. Countermeasure: precisely control temperature and oxygen partial pressure and use staged multi-pass magnetic separation, weak-field first for strong-magnetic recovery, then strong-field pass for weak-magnetic recovery, reducing mixed carryover.

- **EMS parameter optimization to prevent slag entrainment**: while EMS improves separation, inappropriate settings (excess frequency/intensity) can induce violent oscillation and slag entrainment, lowering metal purity. Countermeasure: pre-optimize layout and parameters using CFD simulation. Use mild stirring modes (rotating/traveling-wave) during main separation to promote reaction and inclusion flotation; in final stage reduce/stop stirring and provide sufficient settling time for complete fine-slag rise and phase separation.

- **Conclusion**: under proper process control, coupled high temperature and magnetic fields are quality-enhancing tools, not degradation factors. EMS added power is about 5 kW, already included in arc-furnace power budget.

**(c) Molten-salt suspension and circulation**. Reduced buoyancy convection under 1/6 g affects electrolyte thermal/compositional uniformity. Use corrosion-resistant ceramic stirrers or EMS-assisted circulation (Section 5.6.2).

**(d) Material transfer and mixing**. For all granular solids (regolith powder, catalyst, aggregate), use sealed screw conveying or vibratory feeding and re-optimize vibration parameters by DEM simulation.

**(e) CNT yarn winding tension control**. Because yarn sag characteristics change under 1/6 g, winding systems require precise tension sensing and control (Section 5.7.2).

**(f) Inspection and sampling**. Destructive-testing devices (e.g., compression testers) require dedicated clamping/fixation design so samples do not destabilize or eject under low gravity.

**(g) Solid waste/byproduct handling**. Slag/tailings transport and stockpiling behavior differs in low gravity (shallower repose angles). Use sealed pneumatic transport to lined internal waste silos with storage and compaction optimized for low-g conditions.

#### 5.9.3 Special Assessment: Magnetic Separation Impact on Product Quality

This subsection evaluates potential quality issues in dry magnetic concentration of ilmenite and related lunar minerals.

**(a) Separation principle and purity assurance**

Dry magnetic separation uses differences in **specific magnetic susceptibility** among minerals. It is a **purely physical separation** with no chemical reaction, so it does **not alter chemical composition or crystal structure**. Product chemistry is unchanged from magnetic grains in feed; process only physically separates them from gangue. Therefore magnetic separation itself does not degrade Fe-ingot purity, CNT catalyst activity, or downstream metallurgy reliability. Ilmenite concentrate grade depends on feed grade, field strength, and stage count, not chemical interference from separation. This has been verified by COMSOL-DEM co-simulation from Chinese teams [17].

**(b) Potential for surface magnetic contamination and exclusion**

Lunar dry magnetic separation operates in high vacuum with **no liquid phase**. Particles interact by mechanical collision only, so adhesion probability of magnetic impurities onto nonmagnetic particles is very low. Even if trace adhesion occurs, subsequent hydrogen reduction or aluminothermic processing at >=1,000 C will reduce any trace iron oxides into metallic Fe incorporated into Fe product stream, not an independent contaminant source. For CNT catalyst route, lunar high vacuum avoids surface oxidation/water adsorption common in terrestrial wet magnetic separation and can provide **cleaner particle surfaces than Earth analogs** [1].

**(c) Recovery challenge for fine ilmenite and countermeasures**

Regolith ilmenite has wide size distribution; **fine ilmenite (<20 um)** is the principal recovery challenge. Under 1/6 g, weaker adhesion on magnetic drum surfaces can increase misrouting to tailings. Countermeasures: increase field strength (>=1.5 T) and gradient, implement multi-stage magnetic reprocessing of tailings, and use electrostatic traveling-wave sorting as complementary method [17][29].

**(d) Potential effect of magnetic agglomeration on sorting precision**

In strong/high-gradient fields, magnetic particles can form **magnetic agglomerates** by dipole interaction. Agglomeration can improve fine-particle recovery (larger effective mass/force) but may entrain gangue and reduce concentrate purity. Lower gravity can improve particle dispersion to some extent, mitigating entrainment. Optimizing separator speed and magnetic-field frequency can break excessive agglomeration and keep concentrate grade within target range (minor effect, roughly 2%-5% reduction if unoptimized).

**(e) Overall impact on downstream metallurgy and catalysts**

| Concern | Physical Principle | Actual Product Impact | Mitigation |
|:---|:---|:---|:---|
| Magnetic separation changes mineral magnetism | Conventional magnetic sorting does not alter composition; no phase transformation | **No impact** | Maintain current process |
| Surface magnetic contamination | No liquid medium in high vacuum; low adhesion probability | **Negligible impact** | Maintain high-vacuum operation |
| Low fine-particle recovery | Combined low-g and weak magnetic capture for ultrafines | **Needs attention** | Multi-stage magnetic + electrostatic traveling-wave supplement |
| Agglomeration entrains gangue | Magnetic dipole interactions | **Minor impact** (concentrate grade may drop by ~2%-5%) | Optimize rotor speed and field frequency |
| Surface oxidation/water adsorption | Common in terrestrial wet separation | **No impact** under lunar vacuum | Maintain high-vacuum operation |

**(f) Conclusion**

**Lunar dry magnetic separation does not pose substantive quality risk by physical principle.** The key pending technical item is reduced recovery of fine ilmenite under 1/6 g. This should be addressed by multiphysics simulation and ground analog tests to determine optimal field settings and stage count (covered by P2-F3). For CNT catalyst routes, dry magnetic separation in high vacuum yields naturally cleaner Fe-Ni particles than terrestrial wet routes and should be prioritized as Stage 1 FCCVD catalyst feedstock.


### 5.10 Pending Validation Items and Pass Criteria

| ID | Item | Validation Method | Success Criterion | Related Volume |
|:---|:---|:---|:---|:---|
| **P1-F1** | Automated sintered-brick line capacity and quality consistency | Continuous operation >=30 days in Stage 2 | >=500 bricks/day, compressive-strength COV <=15%, dimensional tolerance <=3 mm | Volume II P1-M1 |
| **P1-F2** | Lunar casting performance of regolith concrete | Cast standard sulfur-concrete cubes (150 mm) under lunar-vacuum/low-g conditions | Compressive strength >=20 MPa; <=20% degradation after 100 thermal cycles | Volume II P1-M2 |
| **P1-F3** | Full-process validation of CNT pre-weaving line | Operate micro FCCVD + pre-weaving with local catalyst and carbon source under lunar conditions | CNT yarn tensile strength >=10 GPa; filament-break density <=1 per km | Volume I P0-M2, Volume II P1-M4 |
| **P2-F1** | Lunar smelting efficiency of DC arc furnace | Run DC arc furnace (with EMS) using lunar magnetic concentrate (>=30% $FeTiO_3$) under simulated lunar vacuum and 1/6 g | Fe recovery >=80%, Al reduction efficiency >=30%, lining life >=100 batches | Volume II P2-M1 |
| **P2-F2** | Long-term stability of CNT mass-production line | Continuous operation of Stage 2 industrial FCCVD array >=3 months | >=1,000 kg/month output, >=90% pass rate, <=1 unplanned shutdown/month | Main Volume II |
| **P2-F3** | Cascaded aggregate-sorting efficiency | Ground simulant testbed with full sorting train (magnetic + electrostatic + machine vision) | Medium-fraction ilmenite recovery >=85%, fine-fraction np-Fe recovery >=80%, no degradation in residual-material construction performance [17] | Volume IV, this volume |
| **P2-F4** | Closed-loop validation of aluminothermic + molten-salt electrolysis | Ground simulant closed-loop operation >=10 batches (with EMS assistance) | Comprehensive Al recovery >=80%, net Al loss <=15% per batch, anode O2 purity >=90% [10][11][18] | Section 5.6.2 |
| **P2-F5** | EMS-assisted slag-metal separation efficiency | Run scaled arc-furnace model with EMS on simulated 1/6 g platform | In 1/6 g + EMS, slag-metal separation efficiency improves >=3x over no-stirring baseline; metal-phase inclusion level <=1.2x terrestrial process benchmark | Sections 5.6.2, 5.9.2 |


### 5.11 Parameter Outputs

| Parameter | Value | Status | Receiving Volume |
|:---|:---|:---|:---|
| Initial Al needed for first closed-loop startup (Earth launch) | <=500 kg | Design baseline | Volume X (transport cost) |
| Stage 2 high-value fraction extraction rate from aggregate | >=70% | Design target | Volume IV |
| Stage 3 full-component regolith utilization target | >=95% | Long-term target | Volume IV, Volume VI |
| Sintered-brick monthly capacity | >=15,000 bricks | Design target | Volume II (construction demand) |
| Regolith concrete monthly capacity (Stage 2) | >=5 t | Design target | Volume II |
| Metallurgy monthly capacity (Stage 2) | Al ingots 100-500 kg; Fe ingots 100-500 kg | Design target | Volume II |
| CNT yarn monthly capacity (Stage 1) | 10-50 kg | P1 pending verification | Main Volume II |
| CNT yarn monthly capacity (Stage 2) | >=1,000 kg | P2 pending verification | Main Volume II |
| Lunar oxygen production by metallurgy byproducts | >=500 kg/month (Stage 2) | Design target | Volume III (life support) |
| Total manufacturing equipment launch mass (Stage 2) | <=24.6 t (net mass) | Order-of-magnitude estimate | Volume X (economic transport model) |
| Total manufacturing electricity use (Stage 2) | ~25,000-40,000 kWh/month | Order-of-magnitude estimate | Volume III (grid load dispatch) |
| EMS additional power | <=5 kW (already included in arc-furnace total) | Design baseline | Volume III (grid load) |
| Slag-metal separation efficiency (low-g + EMS) | Target >90% (vs <30% for unstirred settling) | Design target | This volume |


### 5.12 Conclusion of Volume V

This volume completes integrated planning for the lunar manufacturing system. Key contributions:

1. **First complete closure of full-chain material balance.** Section 5.2 fully traces source and destination paths for eleven key elements and intermediates: Al (regolith plagioclase -> aluminothermic/molten-salt electrolysis), Ti (ilmenite concentrate -> hydrogen reduction/lithium reduction -> Ti-Si alloy -> electrorefining -> Ti), Fe (ilmenite -> hydrogen reduction/FFC electrolysis), C (carbonaceous residues + polar CO₂ cold traps + solar-wind volatiles + asteroid carbon -> pyrolysis/Sabatier -> methane), S (troilite -> thermal decomposition/SSAP), Si (regolith $SiO_2$ -> aluminothermic byproduct), O (aluminothermic byproduct + ilmenite hydrogen-reduction byproduct + molten-salt electrolysis anode), eliminating the where-does-Al-come-from logic gap.

2. **Systematic environmental adaptability assessment for lunar manufacturing.** Section 5.9 evaluates vacuum requirements for gas-product management, low-gravity effects on slag-metal separation and bulk handling, potential product-quality risks from magnetic separation, and coupled high-temperature/magnetic-field effects in slag-metal separation. EMS four-step refining can raise separation efficiency from <30% to >90%. Lunar dry magnetic separation shows no intrinsic quality penalty, and natural Fe-Ni catalyst precursor particles can have cleaner surfaces than terrestrial analogs.

3. **Clear and traceable phased material-balance model.** Section 5.3 defines stage-specific capacity and flow directions.

4. **Cascaded feedstock utilization upgrades resource use from sufficient to optimized.** Section 5.4 enables >=70% high-value extraction before construction-line entry in Stage 2. Stage 3 targets >=95% full-component utilization.

5. **Equipment mass and energy are consolidated in Section 5.8.** Net manufacturing-system equipment mass is about 24.6 t; total monthly electricity is about 25,000-40,000 kWh.

6. **All cited technical sources are referenced.** Coverage includes JAXA CNT synthesis validation, Missouri S&T and domestic groups on aluminothermic + molten-salt electrolysis closure, Ningbo ilmenite hydrogen-reduction verification, and Xinjiang regolith photocatalyst work.


### References

[1] JAXA Research Team. "Direct synthesis of carbon nanotubes on lunar regolith simulant particles." *Carbon*, Vol. 231, 2025, 119751.

[2] China News Service. "Natural single-walled carbon nanotubes discovered in Chang'e-6 lunar soil." January 21, 2026.

[3] Tsentalovich, D. E., et al. "Influence of carbon nanotube characteristics on macroscopic fiber properties." *ACS Nano*, Vol. 11, 2017, pp. 11008-11016.

[4] Zhang, X., Bai, Y., et al. "Carbon nanotube fibers with dynamic strength up to 14 GPa." *Science*, Vol. 384, 2024, pp. 1318-1323.

[5] Global Times. "Chinese academicians and experts unveil cutting-edge technologies for lunar research station construction." December 25, 2025.

[6] Ding Lieyun. "Fundamental scientific questions in lunar in-situ construction." China Aerospace News, January 15, 2026.

[7] Harbin Institute of Technology. Lunar in-situ 3D printing and microwave sintering validation. 2025.

[8] Deep Space Exploration Laboratory. Prototype principle system for lunar water-ice extraction. 4th Science and Technology Exchange Conference, April 26, 2026.

[9] NASA. "Kilopower/KRUSTY Project: Fission Power for Space Exploration." 2018.

[10] Fengguo Liu, et al. "Combined process of aluminothermic reduction, electrodeposition alloying, and molten salt electrolysis using inert anode for producing Al and O2 from lunar soil simulant." *Separation and Purification Technology*, Vol. 387, 2026.

[11] Missouri S&T. "Extraction of Aluminum from Lunar Regolith through Molten Salt Electrolysis (LISAP-MSE)." *Acta Astronautica*, Vol. 235, 2025, pp. 17-28.

[12] Method for in-situ preparation of water, oxygen, and metallic elements on the Moon. Chinese invention patent.

[13] Schorghofer, N., & Williams, J.-P. "Carbon dioxide cold traps on the Moon." *Geophysical Research Letters*, Vol. 48, 2021, e2021GL095533.

[14] Dottin, J. W., et al. "The Proposed Silicate-Sulfuric Acid Process: Mineral Processing for In Situ Resource Utilization (ISRU)." arXiv, 2021.

[15] Discovery of carbonaceous-chondrite impact residues on the lunar farside by Chang'e-4. 2022.

[16] Xinjiang Technical Institute of Physics and Chemistry. High-value utilization of lunar soil resources: photocatalyst materials. 2025.

[17] Simulation and optimization analysis for in-situ separation/enrichment of magnetic minerals in lunar soil under multiphysics fields. Hefei Simulation Journal, 2025.

[18] Journal of Materials and Metallurgy. Review of lunar metallurgy technologies: aluminothermic reduction and inert-anode molten-salt electrolysis.

[19] Method and system for separation and purification of lunar volatiles. Chinese invention patent.

[20] Ningbo Institute of Materials. Method for producing large quantities of water from lunar soil: ilmenite hydrogen reduction. 2024.

[21] Missouri University of Science and Technology. Validation of molten-salt electrolysis technology for lunar ISRU. 2025.

[22] Blue Origin. Blue Alchemist: Making Solar Cells and Oxygen from Lunar Regolith. 2023.

[23] Deep Space Exploration Laboratory. Molten-salt electrolysis oxygen prototype: simultaneous in-situ oxygen and high-strength Si-Al alloy production. 4th Science and Technology Exchange Conference, April 26, 2026.

[24] Experimental study of iron extraction from lunar simulants using the FFC Cambridge process. 2025.

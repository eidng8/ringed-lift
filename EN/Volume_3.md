# Volume III: Node Siting and Anchorage Engineering

**Version**: 1.9 (Unified Format · Complete Derivation Edition)
**Compilation Date**: April 2026
**Currency Unit**: Renminbi (Yuan), Symbol: ¥


## 3.1 Preface

This volume is positioned as the **ground-to-orbit connection foundation** for the Space Ring Elevator project, focusing on answering the following core questions:

> **How are the 6 space elevators anchored to the Earth's surface? How is the mechanical connection between the nodes and the ring main body achieved?**

This volume follows the orbital mechanics environment (perturbation loads, independent cable working conditions) from Volume I and the material parameters (CNT cable engineering strength, anchorage material performance) from Volume II, providing boundary conditions for the subsequent elevator climber and cable design volume (Volume IV) and the comprehensive physical demonstration volume (Volume VII) regarding the node anchorage system.

The tasks of this volume are:
1. Complete detailed engineering geological assessment and anchorage scheme design for the 6 ground nodes.
2. Output the displacement constraint types and stiffness at the node anchorage for use in the modal analysis of Volume VII.
3. Provide the full design of the ring segment arc length distribution and the mechanical connection interface between the ring and the nodes.

This volume does not cover the tension distribution and counterweight system of the elevator cable (handled in Volume IV), car design (Volume V), laying of the ring main cable (Volume VI), or economic cost accounting (Volume X). Any parameters that cannot be determined at this stage are marked as "to be verified" with a verification path provided.


## 3.2 Ground Node Siting and Engineering Geological Assessment

### 3.2.1 Engineering Constraints for Siting

1. **Latitude Constraint**: Anchorage points should be within ±1° of the equator (about ±111 km).
2. **Geological Constraint**: The anchorage area must have stable bedrock or soft rock/sedimentary layers suitable for suction anchor penetration. Avoid active volcanoes, strong seismic zones (PGA should be <0.3g), and liquefaction risk areas.
3. **Construction Accessibility**: Must have a deep-water port, international airport, and basic road/power infrastructure.
4. **Long-term Safety**: Over a design life of several centuries, avoid sites expected to fail due to sea level rise or intense geological activity.
5. **Land Area Constraint**: The anchorage body requires about 0.1–0.3 km². Supporting operation area requires an additional 0.3–1 km². Total about **0.4–2 km²**.

**Mechanical Impact Estimate of Latitude Deviation**:

If the latitude deviation of the anchorage point is Δφ (unit: degrees), the ratio of horizontal force to total tension is approximately:

$$
\frac{F_{horizontal}}{T} \approx \sin(\Delta\phi) \approx \frac{\Delta\phi \times \pi}{180}
$$

For Δφ=1° (about 111 km), the horizontal force is about 1.75% of the total tension (estimated at ground-end tension of 10¹⁰ N, about 1.75×10⁸ N).

**Siting Criteria for This Volume**: Prefer Δφ<0.5° (horizontal force <1%); Δφ<1° is acceptable; >1° is in principle excluded, only retained if there are no alternative land resources.

### 3.2.2 6-Node Selection Scheme

| Node No. | Node Name | Longitude | Latitude Deviation | Type | Key Advantages |
|------|------|------|------|------|------|
| 1 | Macapá/Farabay, Brazil | 51°W | ≈0° | Land-based (Continent) | Strictly equatorial, near Alcântara Launch Center |
| 2 | Port Gentil, Gabon | 8°47'E | ≈0°43'S (~80 km) | Land-based (Continent) | Δφ<0.5°, oil industry hub, large port |
| 3 | Manta, Ecuador | 80°43'W | ≈0°57'S (~105 km) | Land-based (Continent) | Δφ<1°, second largest port, mature industrial base |
| 4 | Kiritimati (Christmas Island), Kiribati | 157°29'W | ≈2°N (~222 km) | Island (Coral Reef) | Existing space launch site, equatorial doldrums |
| 5 | Belitung, Indonesia | 108°E | ≈0° | Land-based (Island) | Strictly equatorial, good granite bedrock exposure |
| 6 | Indian Ocean Deep Sea Floating Platform | 73°E | ≈0° | Deep Sea Floating Platform | Equatorial location, centrally serves Africa/Middle East/South Asia |

---

### 3.2.3 Unified Survey Project List

| Survey Item | Description |
|------|------|
| Bedrock Type | Main rock type beneath the site |
| Bedrock Condition | Overburden thickness, rock mass integrity, etc. |
| PGA | Seismic activity index |
| Volcanic Activity | Volcanic risk at and around the site |
| Water Depth Condition | Water depth at anchorage area for marine nodes; "None" for land-based |
| Ocean Current Condition | Surface/mid-layer current speed for marine nodes; "None" for land-based |
| Typhoon/Hurricane Frequency | Degree of tropical cyclone impact at the site |
| Available Land Area | Total required for anchorage and supporting operation area, about 0.4–2 km² |
| Port/Transport Condition | Convenience of transporting construction materials |
| Existing Aerospace/Industrial Facilities | Relevant infrastructure in the vicinity |
| Ecological/Environmental Sensitivity | Special ecological or environmental restrictions |

---

### 3.2.4 Detailed Engineering Geology of Each Node

#### (1) Node 1: Macapá/Farabay, Brazil (51°W, Land-based)

| Survey Item | Preliminary Assessment | Data Source |
|------|------|------|
| Bedrock Type | Precambrian granite-gneiss (southern edge of Guiana Shield) | CPRM Geological Survey of Brazil |
| Bedrock Condition | Exposed at surface to shallow overburden (<20 m), intact rock mass | Regional geological map |
| PGA | <0.05g (intraplate stable area) | GSHAP |
| Volcanic Activity | None | Global Volcanism Program |
| Available Land Area | Ample (city area 6,407 km²) | Brazilian Statistics Bureau |
| Port/Transport Condition | Amazon River deep-water channel, Macapá Port; BR-156 highway | Brazilian Port Authority |
| Existing Aerospace/Industrial Facilities | Near Alcântara Launch Center | Brazilian Space Agency |
| Ecological/Environmental Sensitivity | Amazon estuary ecology needs attention | Brazilian Ministry of Environment |

**Latitude Deviation Assessment**: Δφ≈0°, pure uplift anchorage design.

**Alternative Nodes**: Other deep-water ports near the equator in Brazil (e.g., Belém, about 1°S) have latitude deviation >1°, horizontal force is unacceptable. Macapá is the only site in South America that simultaneously meets strict equatorial location, deep-water port, and proximity to a space launch site.

---

#### (2) Node 2: Port Gentil, Gabon (8°47'E, Land-based)

| Survey Item | Preliminary Assessment | Data Source |
|------|------|------|
| Bedrock Type | Precambrian gneiss-granite (western edge of Congo Craton) | Gabon Geological and Mining Bureau |
| Bedrock Condition | Coastal plain overburden about 10–30 m | Regional geological map |
| PGA | <0.08g (edge of West African Rift System) | GSHAP |
| Volcanic Activity | None | Global Volcanism Program |
| Available Land Area | Urban area about 73.7 km², auxiliary facilities can cross the shore | Gabon Port Authority |
| Port/Transport Condition | Gabon's largest port, deep-water berth, international airport | Gabon Port Authority |
| Existing Aerospace/Industrial Facilities | Offshore platform manufacturing base; about 700 km from Guiana Space Center | Gabon Ministry of Petroleum |
| Ecological/Environmental Sensitivity | Coastal mangroves need attention | Gabon Ministry of Environment |

**Latitude Deviation Impact Assessment**: Δφ≈0.72°, horizontal force ratio ≈1.26% (about 1.26×10⁸ N). Countermeasures: shear keys on anchorage shaft wall + rock anchors inclined about 1.3°.

**Alternative Nodes**: Libreville, Gabon (0°23'N, 9°27'E) is also near the equator and has a deep-water port, but its port scale and industrial base (especially offshore platform manufacturing capacity) are far inferior to Port Gentil. São Tomé and Príncipe (about 0°20'N) has a smaller latitude deviation, but as a small island country, lacks deep-water ports and heavy industry to support anchorage construction, and the land area is insufficient.

---

#### (3) Node 3: Manta, Ecuador (80°43'W, Land-based)

| Survey Item | Preliminary Assessment | Data Source |
|------|------|------|
| Bedrock Type | Tertiary sedimentary rocks (sandstone, shale, limestone) | Ecuadorian Geological Survey |
| Bedrock Condition | Thin coastal plain overburden (<15 m) | Regional geological map |
| PGA | 0.15–0.25g (edge of Andes subduction zone) | GSHAP |
| Volcanic Activity | Distant source (volcanic arc about 150 km away) | Global Volcanism Program |
| Available Land Area | Ample (urban area about 60.5 km²) | Ecuadorian Statistics Bureau |
| Port/Transport Condition | Ecuador's second largest port, international airport | Ecuadorian Port Authority |
| Ecological/Environmental Sensitivity | Urban built-up area, no special restrictions | Ecuadorian Ministry of Environment |

**Latitude Deviation Impact Assessment**: Δφ≈0.95°, horizontal force ≈1.66% (about 1.66×10⁸ N). Countermeasures: similar to Node 2, increase anchorage diameter by 15%–20%.

**Alternative Nodes**: Galápagos Islands (0°35'S, 90°W) have a latitude deviation of only about 0.58°, geographically superior. **Reasons for rejection**—volcanically active (last eruption 2018), extremely sensitive ecology (UNESCO World Heritage, 97% national park), no large port, all heavy construction equipment would have to be transported by sea platform and helicopter. In addition, Manta is on the west coast of the South American continent, connected by road network to the capital Quito and the largest city Guayaquil, making construction logistics and operation/maintenance conditions far superior to the isolated Galápagos. Tumaco, Colombia (1°49'N, 78°45'W) has a latitude deviation of about 1.8°, exceeding the 1° baseline.

---

#### (4) Node 4: Kiritimati (Christmas Island), Kiribati (157°29'W, Coral Reef/Island)

| Survey Item | Preliminary Assessment | Data Source |
|------|------|------|
| Bedrock Type | Coral limestone (thickness several kilometers) | DSDP drilling data |
| Bedrock Condition | High porosity, medium strength | Published geological literature |
| PGA | <0.03g (intraplate) | GSHAP |
| Volcanic Activity | None | Global Volcanism Program |
| Available Land Area | Land about 388 km², population about 6,500 | Kiribati Statistics Bureau |
| Freshwater Supply | Severe shortage, needs seawater desalination | Kiribati Ministry of Environment |
| Port/Transport Condition | Existing small port and space launch site | Kiribati Ministry of Transport |
| Ecological/Environmental Sensitivity | Coral reef ecological reserve | Kiribati Ministry of Environment |

**Special Analysis of Latitude Deviation**: Δφ≈2° (exceeds 1° baseline), horizontal force ≈3.49% (about 3.49×10⁸ N). Reason for retention—no alternative available land near the equator in the central Pacific. Countermeasures: mooring cables inclined about 3.5°, at least 6 suction anchors (symmetrical arrangement), penetration depth +30%.

**Alternative Nodes**: Tarawa, Kiribati (1°20'N, 173°E) has a latitude deviation of about 1.33°, better than Kiritimati's 2°, but the total land area is only about 31 km², insufficient for a large anchorage turning platform. Howland Island (0°48'N, 176°37'W) has a latitude of only 0.8°, **rejected because**—it is uninhabited, has no port, airport, or freshwater infrastructure, and is more than 3,000 km from the nearest port (Hawaii), so all construction would rely on ocean-going fleets, with costs and difficulty far exceeding Kiritimati. Marshall Islands (about 7°N) have too large a latitude deviation (>7°).

---

#### (5) Node 5: Belitung, Indonesia (108°E, Land-based/Island)

| Survey Item | Preliminary Assessment | Data Source |
|------|------|------|
| Bedrock Type | Permian-Triassic granite, tin ore belt | Indonesian Geological Survey |
| Bedrock Condition | Good granite exposure, intact rock mass | Regional geological map |
| PGA | 0.05–0.12g (distance from subduction zone >500 km) | GSHAP |
| Volcanic Activity | Distant risk (>500 km) | Global Volcanism Program |
| Available Land Area | Ample (island about 4,800 km²) | Indonesian Statistics Bureau |
| Port/Transport Condition | Existing mining port | Indonesian Statistics Bureau |
| Ecological/Environmental Sensitivity | Existing industrial disturbance, avoids primary forest area | Indonesian Ministry of Environment |

**Latitude Deviation Assessment**: Δφ≈0°, pure uplift anchorage design.

**Alternative Nodes**: West coast of Kalimantan (e.g., Pontianak, 0°00'N, 109°20'E) is also strictly equatorial, **rejected because**—the coast is covered by thick alluvium (>50 m), bedrock is too deep, making anchorage construction costs significantly higher; Belitung granite is directly exposed, with lower construction costs. West coast of Sumatra (about 0°) faces the Indian Ocean subduction zone, with very high seismic risk (PGA>0.3g).

---

#### (6) Node 6: Indian Ocean Deep Sea Floating Platform (73°E)

| Survey Item | Preliminary Assessment | Data Source |
|------|------|------|
| Bedrock Type | Deep sea sediments (calcareous ooze + deep sea clay) | DSDP/ODP drilling |
| Bedrock Condition | Very low surface strength (<20 kPa) | Marine geology literature |
| PGA | <0.03g (far from plate boundaries) | GSHAP |
| Volcanic Activity | None | Global Volcanism Program |
| Water Depth Condition | About 2,000–4,000 m | Ocean depth map |
| Ocean Current Condition | Surface 0.2–0.8 m/s, mid-layer <0.1 m/s | Global ocean current model |
| Available Land Area | None (offshore platform, deck about 5,000–10,000 m²) | — |
| Ecological/Environmental Sensitivity | >50 km from Aldabra Atoll | UNESCO |

**Latitude Deviation Assessment**: Δφ≈0°, tension legs arranged nearly vertically. Use Gan Island Airport, Maldives as a construction transit station.

**Alternative Nodes**: Addu Atoll, Maldives (0°38'S, 73°09'E) has a latitude deviation of only about 0.63° (about 70 km), longitude coincides with current site, Gan Island has an international airport. **Rejected because**—the national average elevation is only about 1.5 m, making it the country most threatened by sea level rise; island land area is very small, unable to accommodate the anchorage body and supporting operation area; long-term safety as a permanent anchorage point is unacceptable. **However, Gan Island Airport can be used as a construction logistics transit station** (see Section 3.3.4). Diego Garcia, Chagos Archipelago (7°18'S) has too large a latitude deviation (>7°).

---

### 3.2.5 Overview of Node Siting Scheme

| Node | Site | Latitude Deviation | Horizontal Force Ratio | Anchorage Type |
|------|------|------|------|------|
| 1 | Macapá, Brazil | ≈0° | 0% | Pure uplift type |
| 2 | Port Gentil, Gabon | ≈0°43'S | ~1.26% | Uplift + shear composite type |
| 3 | Manta, Ecuador | ≈0°57'S | ~1.66% | Uplift + shear composite type |
| 4 | Kiritimati, Kiribati | ≈2°N | ~3.49% | Inclined mooring suction anchor type |
| 5 | Belitung, Indonesia | ≈0° | 0% | Pure uplift type |
| 6 | Indian Ocean Floating Platform | ≈0° | 0% | Floating platform + tension leg type |

---

## 3.3 Anchorage Scheme Design

### 3.3.1 Land-based Anchorage (Nodes 1, 5, Pure Uplift Type)

**Design Principle**: Elevator cable tension is transferred to bedrock via an inverted conical anchorage shaft + vertical prestressed rock anchor group. With Δφ≈0°, there is no horizontal force, so a pure uplift design is used.

**Working Load Derivation**: Derived from the conical section model and tension distribution in the cable design of Volume IV (see Volume IV, Section 4.2.2), the maximum ground-end tension:

$$
T_{max} = \frac{\sigma_{allow} \times A_0}{S}
$$

Where $σ_{allow}$ is taken as the target value ~20 GPa from Volume II, Section 2.3.4, A₀ is the ground-end cross-sectional area ~0.196 m², S is the independent working condition safety factor ≥2.5 from Volume II, Section 2.7.1.

$$
T_{max} = \frac{20\times10^9 \times 0.196}{2.5} \approx 1.57\times10^9\,\text{N}
$$
On this basis, consider anchorage safety factor (uplift) ≥3.0, the design load to be borne by the rock anchor group:

$$
F_{design} = T_{max} \times 3.0 \approx 4.71\times10^9\,\text{N}
$$

Number of rock anchors (each with 30–50 MN capacity):

$$
n_{anchor} \geq \frac{4.71\times10^9}{40\times10^6} \approx 118 \rightarrow \text{Take}\geq 120\,\text{units}
$$

| Parameter | Design Value/Range | Description |
|------|------|------|
| Working Load (Max Tension) | ~1.57×10⁹ N | Max ground-end tension under independent working condition (see Volume IV, Section 4.2.2) |
| Safety Factor (Uplift/Cable Break) | ≥3.0 / ≥2.5 | Uplift factor higher than ring cable's 2.0 due to rock mechanics uncertainty |
| Number of Rock Anchors | ≥120 units (each 30–50 MN capacity) | Calculated from design load |
| Anchorage Shaft Diameter/Concrete Volume | ~25 m / ~8,000 m³ | — |

### 3.3.2 Land-based Anchorage (Nodes 2, 3, Uplift + Shear Composite Type)

**Design Principle**: On the basis of pure uplift type, add inclined rock anchors (inclination ≈Δφ×1.3, with safety factor) and shaft wall shear keys, increase anchorage diameter by about 15%–20%.

**Horizontal Force Derivation**:

$$
F_{H2} = T_{max} \times \sin(\Delta\phi_2) \approx 1.57\times10^9 \times \sin(0.72°) \approx 1.10\times10^8\,\text{N}
$$

$$
F_{H3} = T_{max} \times \sin(\Delta\phi_3) \approx 1.57\times10^9 \times \sin(0.95°) \approx 1.45\times10^8\,\text{N}
$$

| Parameter | Node 2 (Δφ=0°43'S) | Node 3 (Δφ=0°57'S) | Description |
|------|------|------|------|
| Working Load (Max Tension) | ~1.57×10⁹ N | Same as left | See Volume IV, Section 4.2.2 |
| Safety Factor (Uplift/Cable Break) | ≥3.0 / ≥2.5 | Same as left | — |
| Horizontal Force | ~1.10×10⁸ N | ~1.45×10⁸ N | $T_{max}$×sin(Δφ) |
| Horizontal Force Ratio | ~1.26% | ~1.66% | sin(Δφ) |
| Rock Anchor Inclination | ≈1.3° | ≈1.7° | Δφ×1.3 |
| Number of Rock Anchors | ≥130 units | ≥140 units | Calculated from total load |
| Anchorage Shaft Diameter/Concrete | ~29 m / ~10,000 m³ | ~30 m / ~11,000 m³ | — |

### 3.3.3 Island/Deep Sea Suction Anchor Anchorage (Node 4, Inclined Mooring Type)

**Design Principle**: Kiritimati lacks large areas of stable bedrock, so a deep sea suction anchor + mooring cable + turning platform scheme is adopted. Horizontal force is about 3.49% of total tension (≈3.49×10⁸ N), countermeasures include: mooring cables inclined about 3.5°, at least 6 suction anchors (symmetrical arrangement), turning platform foundation with added horizontal shear keys, penetration depth +30%. Engineering volume increases by about 30%–50%.

| Parameter | Design Value/Range |
|------|------|
| Number/Diameter/Height of Suction Anchors | ≥6 units / 15–25 m / 25–50 m (+30% penetration depth) |
| Mooring Cable Material/Capacity | CNT braided cable, axial capacity ≥1.5×10⁹ N |
| Material/Fatigue Life | Offshore steel, yield ≥500 MPa / >10⁸ cycles |

### 3.3.4 Deep Sea Floating Platform Anchorage (Node 6)

**Design Principle**: No available land in the Indian Ocean, so a semi-submersible platform + tension leg scheme is adopted. Gan Island Airport, Addu Atoll, Maldives serves as a construction logistics transit station, not bearing structural loads.

| Parameter | Design Value/Range |
|------|------|
| Platform Displacement/Number of Tension Legs | ~50,000–100,000 t / 6–8 units |
| Tension Leg Pretension/Mooring Cable Inclination | >max uplift force ×1.5 / ≤5° (nearly vertical) |
| Design Life | ≥200 years |

---

## 3.4 Items to be Verified (Anchorage)

| No. | Item | Verification Method |
|------|------|------|
| V3-N1 | Detailed engineering geological drilling at each node | On-site drilling (≥100 m) + geotechnical testing |
| V3-N2 | Inclined penetration and bearing capacity of suction anchors in Kiritimati coral limestone | Sea trial + numerical simulation + scale model |
| V3-N3 | Penetration and bearing capacity of deep sea suction anchors in the Indian Ocean | Sea trial + numerical simulation |
| V3-N4 | Inclination and load transfer efficiency of composite anchorage rock anchors at Nodes 2, 3 | Finite element analysis + scale model |

---

## 3.5 Node and Ring Main Body Interface Design

### 3.5.1 Ring Segment Arc Length Distribution and Demonstration

Ring radius R₀=42,264 km (see Volume I, Section 1.2.1), circumference C=2πR₀≈265,458 km, arc length per degree $l_{deg}$≈737.4 km/°. The following calculations are based on the selected node longitudes (including Manta 80°43'W), reasons for node longitude selection are discussed in the alternative schemes for each node in Section 3.2.4.

Arc length of each ring segment:

| Segment | Arc Length (km) | % of Total Ring |
|------|------|------|
| Port Gentil → Indian Ocean Platform | ≈47,360 | 17.8% |
| Indian Ocean Platform → Belitung | ≈25,810 | 9.7% |
| Belitung → Kiritimati | ≈69,700 | 26.3% |
| Kiritimati → Manta | ≈56,600 | 21.3% |
| Manta → Macapá | ≈21,920 | 8.3% |
| Macapá → Port Gentil (closure) | ≈44,080 | 16.6% |

**Redundancy Verification**: If Kiritimati fails, the combined arc segment is about 126,300 km (47.6%, <50%), the ring does not collapse as a whole.

### 3.5.2 Mechanical Connection Interface—Ground-end Anchorage Docking Scheme

The ground-end docking mechanism provides a complete ground interface for the car to dock, fix, load/unload, and allow personnel passage. A lightweight ground terminal building is constructed atop the anchorage shaft, integrating the fixed support structure, loading/unloading platform, personnel passage, and waiting area.

**(1) Interface Functional Requirements**

- **Load Transfer**: Safely transfer the maximum ground-end cable tension ($T_{max}$≈1.57×10⁹ N, see Volume IV, Section 4.2.2) to the prestressed rock anchor group of the anchorage shaft. The ground-end anchorage point is a fixed node, and the cable does not undergo longitudinal displacement adjustment here.
- **Cable Longitudinal Displacement Compensation**: Fully handled by the counterweight system at the GEO end (see Volume IV, Section 4.5.5). The ground-end anchorage point remains stationary, and all fixed facilities in the terminal building require no displacement compensation.
- **Car Docking and Fixation**: When the car descends to the designated docking platform in the terminal building, a mechanical mechanism fixes it to the platform structure. The car remains vertical, without tilting.
- **Car Unloading and Loading**: After the car is stabilized and fixed, the drive wheel and cable disengagement mechanism disconnects the car from the cable, then a lateral transfer mechanism moves the car from the cable running position to the loading/unloading area.
- **Personnel and Cargo Loading/Unloading**: Personnel enter/exit directly at the car docking position via multi-level boarding bridges; cargo is loaded/unloaded in the vertical car position via a lift or crane adjacent to the docking platform.
- **Maintenance Accessibility**: The terminal building's engineering area is equipped with dedicated hoisting channels and transport paths.

The drive wheel clamping frame adopts a split design—the frame consists of two halves, installed on the cable side and the outer side of the car, respectively. In normal operation, the two halves are closed by a hydraulic locking device, and the drive wheels clamp the cable/track sleeve from both sides. When the car needs to be unloaded from the cable, the hydraulic locking device is released, the two halves slide apart (rails installed on the car frame), and the cable is completely released from the clamping frame, with no mechanical contact between the car and the cable. The car can then be laterally transferred from the cable running position to the loading/unloading area, unobstructed by the cable.

The opening and closing of the clamping frame is driven by hydraulic cylinders and equipped with a mechanical locking device. In emergencies, it can be unlocked by a manual hydraulic pump or mechanical lever.

**Mechanical Failure Safety Mechanism for Clamping Force**:

The clamping force of the drive wheels on the cable/track sleeve is provided by hydraulic cylinders, but the hydraulic system may lose pressure due to power failure, pipeline rupture, or seal failure. Therefore, the clamping frame is equipped with the following three mechanical safeguards:

1. **Spring Accumulator (Normally Closed Clamping)**: The hydraulic cylinder is a "spring clamping, hydraulic release" structure. Once hydraulic pressure is lost, the spring automatically pushes the clamping force to the maximum mechanical limit, ensuring the car will not slip off the cable under any circumstances.
2. **Mechanical Ratchet Self-locking**: The clamping frame's slide rail is equipped with a one-way ratchet mechanism. Once the clamping force is established, the ratchet automatically engages. The ratchet can only be released manually or by an independent hydraulic circuit.
3. **Wedge Self-locking Block**: A wedge self-locking block (wedge angle about 5°–8°, less than the friction angle between steel and steel) is set between the drive wheel bearing seat and the car frame. Once the clamping force is established, the wedge block only becomes tighter under vibration and will not slip out in reverse.

All three safeguards are purely mechanical passive mechanisms, not relying on external power or control systems. In any single failure, the car will not accidentally slip off the cable.

**(2) Complete Process for Car Unloading and Loading**

**Unloading Process (Car Arrives at Ground)**:

1. The car decelerates to zero, hovering at the cable running position. At this time, the drive wheels still maintain clamping, the car is stationary but not yet detached from the cable.
2. The bottom support platform rises from directly below the car, docking with the car bottom. At the same time, the arc-shaped clamping arms on both sides of the support platform extend to enclose the car's midsection shell, and the arm's front locking pins insert into the pre-embedded interface plate pinholes on the car. After mechanical locking is completed, the drive wheels gradually release the clamping force, and the car's weight is transferred to the support platform. Cable tension is unaffected throughout.
3. After the car drive wheels are fully released, the two halves of the drive wheel clamping frame slide apart (away from the cable), the cable is released from the clamping frame, and there is no longer any mechanical contact between the car and the cable.
4. The car is supported by the support platform, with the arc-shaped clamping arms maintaining clamping throughout to prevent lateral tipping during transfer. The lateral transfer mechanism moves the car, along with the support platform and clamping arms, from the cable running position to the loading/unloading area. During transfer, the cable remains in place, unaffected.
5. The car is loaded/unloaded with personnel and cargo in the loading/unloading area.

**Loading Process (Car Departure)**:

1. After loading in the loading/unloading area, the car, along with the support platform and clamping arms, is moved back to the cable running position by the lateral transfer mechanism.
2. The two halves of the drive wheel clamping frame close from both sides, the drive wheels contact the cable/track sleeve, and the clamping force is gradually increased to the rated value.
3. The arc-shaped clamping arms unlock and retract, the support platform lowers, and the car's weight is fully borne by the drive wheels.
4. The car starts ascending, leaving through the terminal building's dome skylight.

**(3) Car Fixed Support Mechanism**

The car remains vertical and is fixed when docked by the following mechanisms:

- **Main Support—Bottom Support Platform**: The platform is a welded steel frame, with a support seat on top matching the car bottom. The support seat consists of a grooved base and two sets of horizontally sliding wedge locks. After the car descends to the landing position, the wedge locks are pushed horizontally from both sides into the lock slots of the conical docking head, forming a form-fit lock, securing the car bottom to the support seat. The entire car weight is transferred from the support seat through the platform steel frame to the terminal building's independent pile foundation. Platform load capacity ≥300 t. After the car lands, the hydraulic cylinder is held in position by a mechanical locking device (wedge self-locking sleeve).

- **Lateral Stability—Two Pairs of Arc-shaped Clamping Arms**: The clamping arms extend from both sides of the support platform, enclosing the car's midsection shell from both sides. The front end of the arms is equipped with hydraulically driven locking pins, which insert into matching pinholes in the pre-embedded interface plate on the car shell. The inner side of the arms is lined with UHMWPE pads (10 mm thick), and the clamping force only needs to prevent the car from tilting, not bear the car's weight. The arms also serve as part of the lateral transfer mechanism, maintaining clamping throughout the car's transfer to prevent lateral tipping.

- **Locking Mechanism—Mechanical Lock Pins + Car Pre-embedded Interface**: The car shell is pre-embedded with locking interface plates at the corresponding docking positions (bottom and clamping arm enclosure area). The support platform wedge locks and arc-shaped clamping arm front ends each have 2 sets of hydraulically driven lock pins.

**Lock Pin Shear Check**: Lock pin diameter $d_{pin}$≥80 mm, material is high-strength steel (yield strength ≥1,000 MPa), single pin shear area:

$$
A_{shear} = \frac{\pi d_{pin}^2}{4} = \frac{\pi \times (0.08)^2}{4} \approx 5.03\times10^{-3}\,\text{m}^2
$$

Allowable shear stress $τ_{allow}$≈0.6×$σ_{yield}$≈600 MPa, single pin shear capacity:

$$
F_{single} = \tau_{allow} \times A_{shear} \approx 600\times10^6 \times 5.03\times10^{-3} \approx 3.02\times10^6\,\text{N}
$$

8 sets of lock pins (4 on support platform + 4 on clamping arms) total shear:

$$
F_{total} = 8 \times 3.02\times10^6 \approx 2.42\times10^7\,\text{N}
$$

Much greater than the gravity of a fully loaded 200 t car (about 1.96×10⁶ N), safety margin >12:1. In case of power or hydraulic failure, the lock pins are automatically held in the extended position by a spring accumulator.

**(4) Ground Terminal Building—Function and Structure**

The terminal building is constructed directly above the anchorage shaft, using a lightweight steel structure + CFRP roof panels, with a span of about 50–60 m and a height of about 50–60 m. The base of the terminal building is connected to the top of the anchorage shaft via seismic isolation bearings—the self-weight of the terminal building (about 3,000–5,000 t) is not transferred to the main load-bearing structure of the anchorage shaft, but is borne by independent pile foundations.

The car operates and docks entirely within the terminal building: the dome center is equipped with an openable skylight (opening diameter ≥10 m, larger than the maximum car diameter), through which the car enters the building.

The interior of the terminal building is arranged with multi-level platforms to accommodate the car's vertical operation needs:

| Floor | Functional Area | Description |
|------|------|------|
| **Top Floor (Dome)** | Cable passage area + skylight | Skylight is openable (sliding or petal-type opening) |
| **Upper Middle Floor (Car Docking Level)** | Car docking area + fixed support mechanism | After the car descends to the docking position, it is fixed by the support platform and clamping arms. This floor is the equipment level |
| **Lower Middle Floor (Loading/Unloading Level)** | Personnel boarding bridges + cargo transfer platform + lateral transfer mechanism | Multi-level boarding bridges arranged along car height |
| **Ground Floor (Engineering Equipment Level)** | Cable fixing mechanism + maintenance hoisting area + engineering elevator and transport channel | Not open to the public |
| **Basement (Ground Entrance/Exit)** | Waiting area + cargo transfer area + car maintenance area + engineering vehicle entrance/exit | Personnel access this floor to reach the loading/unloading level |

**(5) Multi-level Boarding Bridge Personnel Access and Fixed Position of Ground-end Anchorage**

The ground-end anchorage is a fixed position node (all longitudinal displacement compensation is handled at the GEO end), and all fixed facilities in the terminal building remain stationary. Each time the car docks, it precisely arrives at the same position, and the doors on each level automatically align with the corresponding boarding bridge.

**(6) Car Bottom Cargo Loading/Unloading Method**

The car's bottom cargo door is located directly above the bottom support platform. Heavy cargo (>50 t per piece) is hoisted directly from the cargo door by an overhead crane inside the building.

**(7) Ground-end Cable Fixing Method**

The ground-end cable is fixed via a fixed saddle + turning pulley set (2–4 pulleys, diameter ≥5.0 m, made of high-strength steel + ceramic coating), transferring vertical tension to horizontal direction into the anchorage shaft rock anchor group. The cable fixing mechanism is located on the ground floor (engineering equipment level) of the terminal building. The turning pulley's replacement cycle is ≥30 years, replaced via the engineering equipment level's hoisting gantry and transport channel.

**(8) Load Transfer Path to Anchorage Shaft**

Cable tension → fixed pulley set → fixed saddle → anchorage shaft top shear key and shaft wall → rock anchor group → bedrock. The weight of the car fixed support mechanism is borne by the terminal building steel structure, not through the main load-bearing path of the anchorage shaft.

**(9) Terminal Building Construction Indicators**

| Parameter | Design Value | Description |
|------|------|------|
| Total Building Area | ~5,000–8,000 m² | Estimated for 60 m span, 60 m high dome structure |
| Structure Type | Lightweight steel structure + CFRP roof panels | Self-weight ~3,000–5,000 t, borne by independent pile foundation |
| Design Life | ≥100 years | Shorter than anchorage's 500–1000 years, can be regularly renovated or rebuilt |
| Simultaneous Car Docking Capacity | ≥2 units | Docking level has 1 main docking position + 1 turnover/maintenance position |
| Skylight Opening Diameter | ≥10 m | Larger than maximum car diameter |

**(10) Items to be Verified**

| No. | Item | Verification Method |
|------|------|------|
| V3-N8 | Equivalent bending fatigue life of turning pulley set under rated tension | 1:5 scale pulley set + CNT cable short sample, simulate 1.57×10⁹ N wheel load, 10⁵ rotation bending cycles |
| V3-N9 | Opening/closing reliability and reset accuracy of split drive wheel clamping frame | 1:2 scale model, simulate 200 opening/closing cycles, measure alignment deviation after reset (requirement <1 mm) |
| V3-N10 | Positioning accuracy and lock pin reliability of car mechanical locking mechanism | 1:5 scale model, simulate 200 t fully loaded car landing and locking process, including lock pin holding and reset verification under power failure |
| V3-N11 | Synchronous docking accuracy of multi-level boarding bridges and car multi-cabin doors | 1:1 partial prototype (single-level bridge + single cabin door), measure docking seal effect and repeatability (target <5 mm) |

### 3.5.3 Displacement Constraint Boundary Conditions (for Volume VII)

| Degree of Freedom | Constraint Type | Stiffness | Description |
|------|------|------|------|
| Radial (R) | Elastic constraint | ≈1×10⁵ N/m | Coupled via connector and cable elasticity (see Volume IV, Section 4.2.5) |
| Tangential (φ) | Fixed (synchronous rotating ring) | — | Ring is stationary relative to ground |
| Axial (Z) | Elastic constraint | ≈1×10⁵ N/m | Node and cable lateral stiffness |

> Exact values to be determined by complete finite element modeling of the connector.

### 3.5.4 Items to be Verified (Interface)

| No. | Item | Verification Method |
|------|------|------|
| V3-N5 | Mechanical bearing and fatigue of ring-node connector | Finite element analysis + scale model |
| V3-N6 | Standardized design of 6-node connectors | Engineering design + manufacturing feasibility verification |
| V3-N7 | Positioning accuracy and reliability of GEO-end active capture arm | On-orbit docking simulation + ground scale verification |

---

## 3.6 Parameter Output (for Volumes IV, VII, and Others)

| Parameter Symbol | Meaning | Value/Range | Status |
|------|------|------|------|
| $K_R$, $K_Z$ | Node constraint stiffness | ≈1×10⁵ N/m | Order-of-magnitude estimate (see Volume IV, Section 4.2.5) |
| $F_{H2}$ | Node 2 horizontal force | ~1.10×10⁸ N (~1.26% $T_{max}$) | Latitude 0°43'S |
| $F_{H3}$ | Node 3 horizontal force | ~1.45×10⁸ N (~1.66% $T_{max}$) | Latitude 0°57'S |
| $F_{H4}$ | Node 4 horizontal force | ~3.05×10⁸ N (~3.49% $T_{max}$) | Latitude 2°N |

> Note: $T_{max}$ see Volume IV, Section 4.2.2.

---

## 3.7 Conclusion of Volume III

This volume completes the siting and anchorage engineering demonstration for the 6 space elevator nodes. Core conclusions:

1. **6 nodes selected**, each with alternative schemes and reasons for rejection, covering four anchorage schemes: pure uplift type, composite type, inclined mooring suction anchor type, and floating platform + tension leg type.
2. **Key anchorage design parameters provided**, with complete substitution calculation process for working load derivation (Section 3.3.1), derivation basis in Volume IV, Section 4.2.2.
3. **Arc length distribution passes redundancy verification**, Kiritimati failure does not cause ring collapse.
4. **Ground terminal building and docking mechanism scheme fully designed**: including car unloading and loading process, fixed support mechanism (bottom support platform with wedge locks + lateral arc-shaped clamping arms + mechanical lock pins, lock pin shear fully checked, margin >12:1), split drive wheel clamping frame (with triple mechanical failure safety mechanism), multi-level boarding bridge personnel access scheme, and five-level functional zoning of the terminal building.
5. **Complete GEO-end connection facility scheme** is discussed in detail in Volume IV, Section 4.5.5.
6. **Preliminary estimate of node constraint stiffness**, $K_R$≈$K_Z$≈1×10⁵ N/m, classified as flexible constraint. Derivation basis in Volume IV, Section 4.2.5.

**Current Status**: This volume is fully concluded at the node siting and anchorage engineering level. Detailed design related to cables and cars is handed over to Volume IV.


## References

[3.1] CPRM. *Geological Map of the Amazon Craton*. Scale 1:1,000,000.

[3.2] Gabon Ministry of Mines and Geology. *Carte Géologique du Gabon*. 2020.

[3.3] Ecuadorian Geological Survey. *Mapa Geológico del Ecuador*. 2021.

[3.4] GSHAP. *Global Seismic Hazard Map*. 1999.

[3.5] DSDP. *Initial Reports*, Legs 1–96.


## Terminology Table

| Abbreviation | Chinese Name |
|------|----------|
| GEO | Geosynchronous Orbit |
| CNT | Carbon Nanotube |
| PGA | Peak Ground Acceleration |
| UHMWPE | Ultra-High Molecular Weight Polyethylene |
| C/SiC | Carbon Fiber Reinforced Silicon Carbide Composite |
| CFRP | Carbon Fiber Reinforced Polymer |
| GSHAP | Global Seismic Hazard Assessment Program |
| DSDP | Deep Sea Drilling Project |
| ODP | Ocean Drilling Program |
| API | American Petroleum Institute |
| UNESCO | United Nations Educational, Scientific and Cultural Organization

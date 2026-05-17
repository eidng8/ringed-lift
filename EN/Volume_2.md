# Volume II: Materials Science and Cable Engineering

**Version**: 1.10<br/>
**Compilation Date**: May 2026<br/>
**Currency Unit**: Renminbi (Yuan), symbol: ¥<br/>


## Terminology Table

| Abbreviation | English Full Name |
|------|----------|
| ASTM | American Society for Testing and Materials |
| C/SiC | Carbon Fiber-Reinforced Silicon Carbide (Composite) |
| CFRP | Carbon Fiber-Reinforced Polymer |
| CIGS | Copper Indium Gallium Selenide (Thin-Film Solar Cell) |
| CNT | Carbon Nanotube |
| CVD | Chemical Vapor Deposition |
| FCCVD | Floating Catalyst Chemical Vapor Deposition |
| GB/T | National Standard of China (Recommended) |
| GEO | Geostationary Earth Orbit |
| GPa | Gigapascal |
| HAPS | High-Altitude Platform Station |
| IEC | International Electrotechnical Commission |
| ISRU | In-Situ Resource Utilization |
| LEO | Low Earth Orbit |
| MASTER | Meteoroid and Space Debris Terrestrial Environment Reference (ESA) |
| MWCNT | Multi-Walled Carbon Nanotube |
| ORDEM | Orbital Debris Engineering Model (NASA) |
| PBO | Poly(p-phenylene benzobisoxazole) |
| SWCNT | Single-Walled Carbon Nanotube |
| UHMWPE | Ultra-High Molecular Weight Polyethylene |
| ULE | Ultra-Low Expansion Glass |


## 2.1 Preface

This volume is positioned as the **materials foundation** for the Space Ringed-Elevation project, focusing on answering the following core questions:

> **What material should be used to build the ring elevator cable? Can this material be manufactured at the required yield and quality? What are the engineering performance parameters after braiding into a cable? What are the material requirements for other key parts of the ring elevator system?**

The tasks of this volume are:
1. To demonstrate the necessity of CNT as the ring elevator cable material and provide target performance parameters.
2. To establish a mechanical transfer model from single filament to braided cable, quantitatively analyzing the strength loss pattern.
3. To design the cable's cross-sectional redundancy structure and provide engineering allowable stress and safety factors.
4. To plan two production paths for CNT: ground-based manufacturing and lunar in-situ manufacturing, and discuss multi-path carbon source supply strategies and associated resources.
5. To outline the material requirements and design directions for other key parts of the ring elevator system.
6. To output key parameters such as ring linear density λ, equivalent bending stiffness, number of redundant strands N, allowable stress, etc., for use in Volume I, Volume VII, and subsequent volumes.

This volume does not cover on-orbit cable deployment processes (handled by Volume VI), node anchoring design (handled by Volume III), or economic cost accounting (handled by Volume X). Any parameters that cannot be determined at this stage are marked as "to be verified" with a verification path provided.


## 2.2 Material Selection

### 2.2.1 Constitutive Requirements for the Cable

The main ring cable must meet the following mechanical conditions (derived in Volume I):

- **Static Tension Bearing**: T = GMₑλ/R₀ (see Volume I, Section 1.3.1, equilibrium equation).
- **Superimposed Perturbation Stress**: In addition to static tension, it must withstand alternating stresses caused by lunar perturbations, solar radiation pressure, etc.
- **Debris Impact Tolerance**: Failure of a single cable does not affect the whole; simultaneous failure of multiple cables must be limited.

From an engineering perspective, the target performance of the cable material is:

| Performance Index | Minimum Requirement | Target Value |
|------|------|------|
| Single Filament Tensile Strength | ≥ 50 GPa | ≥ 60 GPa |
| Density | As low as possible | ≤ 1.5 g/cm³ |
| Vacuum Stability | No corrosion, no significant fatigue | Intrinsic life > 1000 years |
| Engineering Strength After Braiding | ≥ 20 GPa | ≥ 30 GPa |
| Debris Impact Toughness | Can withstand micron- to centimeter-scale debris impacts | No overall failure under multi-strand redundancy |

### 2.2.2 Candidate Material Comparison

| Material | Theoretical Tensile Strength (GPa) | Density (g/cm³) | Specific Strength (GPa·cm³/g) | Vacuum Stability | Weavability |
|------|------|------|------|------|------|
| CNT [2.6–2.8] | 60–100 | 1.3–1.5 | 40–77 | Excellent | Yes (spinning technology has made breakthroughs [2.9]) |
| Graphene | 130 | 2.2 | 59 | Excellent | Poor (2D material, difficult to cable) |
| PBO (Zylon) [2.1] | 5.8 | 1.56 | 3.7 | Medium (UV degradation) | Mature |
| Kevlar [2.2] | 3.6 | 1.44 | 2.5 | Poor (UV, moisture) | Mature |
| Dyneema [2.3] | 3.5 | 0.97 | 3.6 | Poor (creep, UV) | Mature |
| Carbon Fiber [2.4–2.5] | 4–7 | 1.8–2.0 | 2–4 | Good | Mature |

**Conclusion**: CNT is the only known material that can simultaneously meet the strength and density requirements. Existing polymer fibers can be used for early trials or auxiliary structures but cannot serve as the main ring material.

### 2.2.3 CNT Type Selection

| Type | MWCNT | SWCNT |
|------|------|------|
| Single Filament Strength Range | Lab measured 20–90 GPa, average ~48 GPa, some samples >100 GPa [2.6–2.7]; theoretical limit constrained by interlayer shear strength, can reach ~200 GPa after interlayer crosslinking optimization | Lab measured ~50–100 GPa [2.6]; theoretical limit without interlayer slip constraint, can reach higher levels |
| Synthesis Difficulty | Lower | Higher (chirality control) |
| Mass Production Feasibility | Entered small batch production | Laboratory stage |
| Cost Trend | Decreasing rapidly | Decreasing |

**Selection in this Volume**: MWCNT is chosen as the current design reference material. Its mass production feasibility is better than SWCNT, and its measured upper limit has reached 80–100 GPa [2.7]. Long-term upgrades do not limit the number of walls—the key indicator is the continuous improvement of single filament strength, not the replacement of material type.


## 2.3 From Single Filament to Cable: Strength Loss Model

### 2.3.1 Problem Statement

Lab-measured CNT single filament strength can reach 60–100 GPa [2.6–2.8], but after trillions of filaments are braided into a cable with a diameter of 0.5–1.0 m, the engineering strength drops significantly. The purpose of this section is to establish a quantitative loss model.

### 2.3.2 Hierarchical Path of Strength Loss

```
CNT single filament (nm scale)
    ↓ Twisting/Spinning
CNT yarn (μm scale, hundreds to thousands of filaments)
    ↓ Stranding
CNT strand (mm scale, tens to hundreds of yarns)
    ↓ Braiding/Twisting
CNT cable (m scale, hundreds to thousands of strands)
```

The discussion of strength transfer efficiency refers to review studies in the CNT fiber field [2.9].

### 2.3.3 Loss Factors at Each Stage

| Stage | Loss Mechanism | Loss Factor Symbol | Typical Range |
|------|------|------|------|
| Single Filament→Yarn | Inter-tube slip, uneven load transfer, defect aggregation | f₁ | 0.3–0.5 |
| Yarn→Strand | Helical twisting reduces axial component, surface friction loss | f₂ | 0.5–0.7 |
| Strand→Cable | Force decomposition due to braiding angle, uneven load among strands | f₃ | 0.5–0.7 |

**Cable Engineering Strength Estimation Formula**:

$$
\sigma_{cable} = \sigma_{filament} \times f_1 \times f_2 \times f_3
$$

### 2.3.4 Estimation and Targets

The following are engineering strength estimates based on the upper limit of MWCNT single filament strength (~80 GPa, current reference) and a future higher-strength cable (σ_filament≈100 GPa, wall number unlimited).

| Parameter | Conservative Value | Optimistic Value (Current Reference) | Future Value (Higher Strength Cable) |
|------|------|------|------|
| σ_filament | 60 GPa | 80 GPa | 100 GPa |
| f₁ | 0.3 | 0.5 | 0.5 |
| f₂ | 0.5 | 0.7 | 0.7 |
| f₃ | 0.5 | 0.7 | 0.7 |
| **σ_cable** | **4.5 GPa** | **19.6 GPa** | **24.5 GPa** |

The conservative value of 4.5 GPa is too low to support the ring elevator design.

**Optimistic Value Calculation (Current Reference)**:

$$
\sigma_{cable} = 80 \times 0.5 \times 0.7 \times 0.7 = 80 \times 0.245 = 19.6\text{GPa}
$$

**Comparison with Existing Experimental Data (To Be Verified-V2-M1)**:

The highest measured strength of CNT yarn in the literature is 8.8 GPa (Tsentalovich et al., 2017 [2.25], CVD aerogel direct spinning) and 14 GPa (Bai Yunxiang team, 2024 [2.26]). Using σ_filament=80 GPa as the reference, the current yarn strength f₁ is about 0.11–0.175, which is about 3–5 times lower than the optimistic value f₁=0.5 in this volume.

**Current Conclusion**: Using MWCNT as the reference, the engineering strength target ≥20 GPa requires σ_filament≈80 GPa and f₁, f₂, f₃ all in the optimistic range (total loss coefficient ≈0.245), corresponding to σ_cable≈19.6 GPa—just reaching the 20 GPa threshold, with almost no margin.

- f₁ is the current bottleneck. The current measured f₁ of yarn is about 0.11–0.175, which needs to be increased to 0.5 to meet the 20 GPa target.
- CNT's fatigue resistance has experimental evidence—a single CNT can withstand hundreds of millions of tensile cycles without breaking [2.27].
- There are standardized test methods for precise measurement of f₁. Strength differences between preparation techniques can reach several orders of magnitude; yarn strength is controlled by CNT alignment and porosity [2.28].

**Long-term Upgrade Path**: With continuous advances in CNT manufacturing technology, single filament strength is expected to further improve. The limit of MWCNT is far from exhausted—after optimizing interlayer crosslinking, it may reach ~200 GPa; optimization of multi-strand yarn braiding processes (such as controlling twist) can increase strength by more than 2 times [2.29]. As long as single filament strength increases to above 100 GPa, engineering strength can reach the 24.5 GPa range, providing about 25% strength margin for the progressive upgrade of the ring elevator.

### 2.3.5 Items to Be Verified

| No. | Item | Verification Method | Description |
|------|------|------|------|
| To Be Verified-V2-M1 | Precise measurement of f₁ | Prepare MWCNT yarn samples, compare single filament and yarn strength | Current highest f₁≈0.175 [2.25–2.26], target 0.5 |
| To Be Verified-V2-M2 | Braiding angle dependence of f₂, f₃ | Tensile tests on multi-strand braided samples, variable is braiding angle | Existing small-scale multi-strand data [2.29] but no meter-scale cable data |
| To Be Verified-V2-M3 | Long-term creep in vacuum | Continuous loading in vacuum for several years, measure creep rate | Single CNT fatigue resistance confirmed [2.27]; no public data on long-term creep of braided cable |


## 2.4 Cable Cross-Section Design and Redundancy

### 2.4.1 Cross-Section Structure

The main ring cable adopts a multi-level redundant braided structure:

- First level: Thousands of CNT filaments combined into one yarn (diameter ~100 μm)
- Second level: Hundreds of yarns stranded into one sub-cable (diameter ~10 mm)
- Third level: Tens to hundreds of sub-cables braided into a cable unit (diameter ~0.1 m)
- Fourth level: Several cable units stranded to form the complete ring cross-section (diameter 0.5–1.0 m)

### 2.4.2 Determination of Redundant Strand Number N

| Design Variable | Value | Description |
|------|------|------|
| Total Ring Tension T | Depends on λ (see Section 2.6.2) | From Volume I, Section 1.3.1, static equilibrium equation $T = λGM_e/R_0$ |
| Allowable Load per Strand $F_{strand}$ | $σ_{cable} \cdotp A_{strand}$ | $A_{strand}$ is the cross-sectional area of a single strand |
| Safety Factor S | ≥ 2.0 | Considering debris impact and uncertainties |
| Minimum Number of Strands N_min | $T \cdotp S / F_{strand}$ | Lower limit to meet safety factor |

With $σ_{cable} = 20 GPa, S = 2.0$ , $A_{strand}$ taken as a typical value under cross-section structure (ø0.5–1.0 m, N≥1000 strands) ≈5×10⁻⁴ m², $F_{strand}≈1×10⁷ N$ . For ring tension T, using $λ=150 kg/m$ (median), substitute into the equilibrium equation in Volume I for an estimated $T≈1.4×10⁹ N$ .

$$
N_{min} = \frac{T \times S}{F_{strand}} = \frac{1.4\times10^9 \times 2.0}{1\times10^7} = 280
$$

This value is only for order-of-magnitude verification—overview takes N≥1000 to include extra margin for debris impact redundancy and material inhomogeneity, which is a reasonably conservative assumption.

### 2.4.3 Self-Healing and Monitoring

- **Distributed Fiber Optic Sensing**: Optical fibers embedded in the cable for real-time strain monitoring of each strand.
- **On-Orbit Repair Mechanism**: Local damage is located and repaired by maintenance robots (see Volume VI).
- **Progressive Upgrade**: Every 50–100 years, higher-strength cables can be added to the outside of the existing cable by stranding.


## 2.5 CNT Manufacturing Paths

### 2.5.1 Strategic Position of ISRU

The overall goal of ISRU is to minimize the need for launching materials from Earth and to establish self-sufficiency for long-term extraterrestrial manned bases. "In-situ utilization of lunar resources" has been included in the "2025 Global Engineering Frontiers" report [2.14]. This project expands the application scope of ISRU from traditional "lunar construction materials + water + oxygen" to "lunar manufacturing of CNT".

### 2.5.2 Resource Inventory

#### (1) Associated Resources of C-type Asteroids

| Resource Type | Content Range | Source Basis | Engineering Use |
|------|------|------|------|
| Carbon (C) | 2%–5% (CM type), possibly higher in CI type | Measured in carbonaceous chondrites [2.12–2.13] | CNT raw material |
| Water (H₂O, in hydrated minerals) | 3%–22% (CI/CM type) | Carbonaceous chondrites, Ryugu samples [2.13] | Propellant, life support |
| Nitrogen (N) | Hundreds to thousands of ppm | Measured in whole carbonaceous chondrite samples | Life support system |
| Iron, Nickel (Fe, Ni) | Metallic + silicate, total up to several percent | Elemental abundance in carbonaceous chondrites | Catalyst, construction structural material |
| Precious Metals (Platinum group, etc.) | ppm level | Trace element analysis of carbonaceous chondrites | Electronic devices, industrial catalysts |

#### (2) Local Lunar Resources

| Resource Type | Known/Estimated Data | Detection Status | Source |
|------|------|------|------|
| Lunar Soil Carbon | About 100 ppm | Confirmed | — |
| Polar CO₂ Cold Traps | Total stable area about 200 km², reserves to be determined | Confirmed | [2.10] |
| Polar Water Ice | Cold trap area about 17,000 km², preliminary reserve estimate about 600 million tons | Further exploration by Chang'e 7 | [2.24] |
| Lunar Soil Iron, Nickel | Nano-iron content up to 0.1%–0.5% | Confirmed | — |

> Note: The above lunar resource data are current confirmed or preliminary estimates.

### 2.5.3 Overview of Two Paths

| Path | Location | Function | Stage |
|------|------|------|------|
| Path 1: Ground Manufacturing | Earth | Early trials, samples, construction materials for the first few nodes | Stages 1–2 |
| Path 2: Lunar Manufacturing | Moon | Large-scale supply of main ring cable raw materials | Stages 2–4 |

### 2.5.4 Path 1: Ground-Based CNT Manufacturing

**Process Route**: FCCVD [2.9].

- Carbon source: Methane, ethylene, or ethanol
- Catalyst: Iron, nickel, or cobalt nanoparticles
- Temperature: 600–1200°C
- Product: CNT aerogel or film, can be directly spun into yarn

**Pilot Line Design Target** (Stage 1):
- Annual output: Several tons of CNT yarn
- Use: Cable sample testing, elevator prototype cable manufacturing

### 2.5.5 Path 2: Lunar In-Situ CNT Manufacturing

**Necessity**: The total mass of the main ring cable is about 170 million tons; launching all from Earth is not feasible. Lunar gravity is only 1/6 that of Earth, and the energy consumption for launching raw materials from the Moon to GEO is much lower than from Earth.

**Strategic Risk Warning**: Achieving large-scale lunar CNT manufacturing itself requires low-cost access to orbit, which constitutes a "chicken and egg" dilemma. Therefore, **Path 1 (Earth manufacturing) must be maintained as an independent, complete backup plan** to ensure that the overall project schedule is not disrupted if lunar industry cannot be commissioned on time.

**Full Process of Lunar CNT Manufacturing**:

1. **Lunar Soil Collection and Beneficiation**: Oxides in lunar soil can provide catalyst raw materials; natural nano-iron can serve as catalyst precursor.

2. **FCCVD Reactor** (To Be Verified-V2-M4): Operates under lunar 1/6 gravity or microgravity. **Existing experimental data**: JAXA has directly grown CNT on lunar regolith simulant particles in situ [2.30]. The formation mechanism of natural CNT in Chang'e 6 lunar soil also provides an environmental analogy for this.

3. **Carbon Source Supply Strategy: Multi-Path Parallel**

   **Main Path: C-type Asteroid Carbon Source**—see Section 2.5.6.

   **Parallel Path: Exploration and Evaluation of Local Lunar Carbon Sources**—lunar resource exploration is ongoing. This project needs to supplement the existing plans with special exploration for carbon sources (especially the reserve and extractability assessment of polar CO₂ cold traps, To Be Verified-V2-M8). The total stable area of all polar CO₂ cold traps is about 200 km² [2.10]. If future reserves are sufficient, even if only enough for the first phase, the economic value is huge—transport energy consumption is much lower than asteroid capture, and refining equipment is fully compatible.

   **Supplementary Path: Earth-Moon Space Carbon Cycle**—in the long term, solar energy on the ring can be used to reduce CO₂ to usable carbon sources.

4. **Discovery of Natural CNT on the Moon and Engineering Implications**: Natural SWCNT has been found in Chang'e 6 lunar soil [2.11]. The "micrometeorite impact + iron catalysis" path in the natural formation mechanism provides important reference for catalyst design and reaction condition optimization in artificial FCCVD.

5. **Lunar Soil Catalyst Extraction** (To Be Verified-V2-M5): Process and extraction efficiency have no public experimental data yet.

6. **Spinning and Braiding**: Pre-braiding on the Moon or lunar orbit, then transported to GEO. Final cable stranding and braiding are performed on the GEO ring (see Volume VI).

### 2.5.6 C-type Asteroid Mining and Carbon Source Supply (Main Path)

#### (1) Resource Endowment

C-type asteroids are among the most primitive bodies in the solar system, rich in carbon, hydrated minerals, and organics [2.12].

- **Reserve Scale**: C-type asteroids account for about 75% of known asteroids.
- **Chemical Composition**: Carbon content can reach 10%–30%, also contains water and small amounts of precious metals. ICE-CSIC systematically analyzed the precise chemical composition of six common carbonaceous chondrites in 2025 [2.17].
- **Sample Evidence**: Ryugu returned about 5.4 g of CI-type carbonaceous chondrite samples [2.13]. Bennu returned about 120 g of samples rich in carbon and nitrogen [2.18].

#### (2) Mining Scheme Selection

| Scheme | Principle | Maturity | Applicable Scenario |
|------|------|------|------|
| Capture Bag + Overall Towing | Use inflatable capture bag to wrap asteroid, tow as a whole to Earth-Moon space | TransAstra successfully tested a 1-meter capture bag on the ISS in October 2025 [2.19] | Small asteroids |
| Surface Pyrolysis Extraction | Land on asteroid, use high heat to decompose organics | Laboratory validation stage | Larger asteroids |
| Optical Mining | Concentrate sunlight to ablate surface material | NASA-funded concept research stage | Medium to large asteroids |

**Project Recommendation**: Capture bag scheme to tow as a whole to Earth-Moon space. A 100-meter diameter C-type asteroid can provide about 1 million tons of carbon; the ring elevator's 170 million tons of cable requires several dozen such asteroids.

#### (3) Carbon Extraction and Subsequent Processes

1. **Crushing and Grading**
2. **Pyrolysis** (To Be Verified-V2-M6): Existing experimental data include pyrolysis experiments on carbonaceous chondrite simulants [2.31] and Hayabusa2 Ryugu impact experiments [2.32]
3. **Carbon Source Purification**
4. **Tailings Utilization**

#### (4) Industry Status and Timeline Matching

The asteroid mining market was valued at about $173 million in 2025 [2.20]. AstroForge launched its first private asteroid survey mission Odin in February 2025 [2.21]. TransAstra successfully tested capture bag technology on the ISS in October 2025 [2.19]. The first actual asteroid capture mission is planned for 2028 [2.33].

China launched the Tianwen-2 probe in May 2025 [2.22]. In 2023, Wang Wei proposed a "Four-Stage Development Roadmap for Solar System Resource Development before 2100" [2.23].

**Matching with the Ring Elevator Timeline**: By project stages 3–4 (2035–2045), capture and mining technology for small asteroids is expected to reach an engineering application level.

### 2.5.7 Summary of Items to Be Verified for Lunar Manufacturing

| No. | Item | Verification Method | Description |
|------|------|------|------|
| To Be Verified-V2-M4 | Low gravity/microgravity FCCVD | Lunar or space station experiment | Existing ground CVD data on lunar regolith simulant [2.30] |
| To Be Verified-V2-M5 | Catalyst extraction efficiency from lunar soil | Lunar regolith simulant experiment | Chang'e lunar soil sample research |
| To Be Verified-V2-M6 | C-type asteroid carbon extraction efficiency | Meteorite simulation + laboratory pyrolysis | Preliminary data available [2.31–2.32] |
| To Be Verified-V2-M7 | Engineering verification of asteroid capture and towing | Near-Earth asteroid capture mission | 1-meter capture bag test completed on ISS [2.19] |
| To Be Verified-V2-M8 | Exploration of lunar polar CO₂ reserves | Polar drilling and sampling analysis | CO₂ cold traps confirmed [2.10] |


## 2.6 Parameter Output

### 2.6.1 Parameters Output to Volume I and Volume VII

| Parameter Symbol | Meaning | Value/Range | Status |
|------|------|------|------|
| λ | Ring linear density (excluding track sheath) | ~30–300 kg/m (preliminary estimate, see 2.6.2) | Tentatively set at 300 kg/m, final value to be locked |
| EI_equiv | Ring equivalent bending stiffness (N·m²) | To be calculated after braiding structure is determined | To be verified-V2-M2 |
| N | Number of redundant strands in ring cross-section | ~1000–3000 (design target) | To be finalized based on safety factor |
| σ_allow | Allowable stress per cable strand | ~20 GPa (engineering target) | To be verified-V2-M1 to M3 |
| S | Safety factor | ≥ 2.0 | Design reference |

### 2.6.2 Preliminary Linear Density Estimate (for Volume I)

Assuming d = 0.7 m, material density ρ ≈ 1.3 g/cm³ [2.8], cross-sectional fill factor 0.6 (considering braiding voids):

$$
A_{section} = \pi \times (0.35)^2 \approx 0.385 \text{ m}^2
$$

$$
\lambda = A_{section} \times \rho \times fill\ factor \approx 0.385 \times 1300 \times 0.6 \approx 300 \text{ kg/m}
$$

This value corresponds to the upper limit of "dense braiding". With a lower fill factor of ~0.06, λ ≈ 30 kg/m. Therefore, this volume provides an estimated range: **λ ≈ 30–300 kg/m**, and subsequent volumes use the median for initial simulation.

**After iterative demonstration in subsequent volumes, the design baseline for full cable linear density is tentatively set as `λ = 300 kg/m`.** This value serves as a common input for all subsequent volumes (Volumes I, VII, VI, VIII), to be fine-tuned and locked after the final braiding structure and safety factor are determined.


## 2.7 Other Material Requirements in the Ring Elevator System

### 2.7.1 Elevator Cable Materials

The elevator cable connects the ground anchor to the main ring and is the vertical transport channel from the ground to GEO.

#### (1) Constitutive Material and Cross-Section Features

- Same as the ring cable, made of braided CNT cable.
- **Tapered Cross-Section**: Maximum cross-section at the ground end (overview ~0.5m diameter), gradually narrows downward. The precise curve needs to be determined in Volume IV based on tension distribution calculations, referencing the classic Bradley-Edwards derivation, with a ground/top cross-section ratio of about 10–20:1.
- **Redundant Braiding**: ≥1000 strands.
- **Surface Protection (Against Atomic Oxygen Erosion)**: The elevator cable in the LEO segment (altitude 0–1,000 km) is threatened by atomic oxygen erosion. The protective coating shall be applied to the outermost surface of the track sleeve (i.e., the outer surface of the UHMWPE sacrificial layer); recommended materials are silicon dioxide (SiO₂) or aluminium oxide (Al₂O₃), thickness ≥5 μm, design life ≥10 years (calculated by integrating the equivalent atomic oxygen flux). Once the protective coating fails, the UHMWPE will degrade rapidly, endangering the underlying structure; coating integrity shall therefore be inspected at each annual C-level overhaul (microscopy or spectroscopy), and recoating shall be performed when remaining thickness falls below 2 μm.

  Atomic oxygen flux varies with altitude: at the ~400 km peak it can reach $10^{14}$–$10^{15}$ atoms/cm²/s, dropping to approximately $10^{11}$–$10^{12}$ atoms/cm²/s at 1,000 km.

  **To Be Verified (V2-M9)**: Atomic oxygen exposure experiment. Simulate the LEO orbital atomic oxygen environment in a vacuum chamber (flux $10^{15}$ atoms/cm²/s, equivalent cumulative flux $5 \times 10^{22}$ atoms/cm², corresponding to 10 years of actual exposure), and measure the integrity of the protective coating (SiO₂/Al₂O₃, thickness 5 μm) deposited on UHMWPE coupons and the mechanical performance degradation of the UHMWPE. Success criteria: after 10-year equivalent exposure, no coating peeling, UHMWPE tensile strength degradation ≤20%, wear retention ≥80%.

  **To Be Verified (V2-M10)**: Long-term stability of aluminium alloy (with micro-arc oxidation) under atomic oxygen + periodic friction, simulating LEO atomic oxygen environment combined with mechanical friction cycling tests. Verify the service life of the micro-arc oxidation layer under the combined action of atomic oxygen and friction.

#### (2) Design Conditions

| Condition | Time | Force Characteristics | Description |
|------|------|------|------|
| **Independent Condition** | Stages 1–3 (ring not yet built) | All loads borne by the cable itself and tensioning counterweight system | **Design baseline (more severe)** |
| **Coupled Condition** | After Stage 4 (ring built) | Cable top connected to ring, ring tension shares part of the load | Verification condition |

Cable cross-section design must meet safety factor ≥2.5 under this condition. Precise tension distribution and tapered cross-section curve are calculated in Volume IV.

### 2.7.2 Anchor and Node Structure Materials

#### (1) Ground Anchor

| Node Type | Anchoring Method | Key Material Parameters | Design Basis |
|------|------|------|------|
| Land-based Anchor (Brazil, Gabon, Indonesia) | Anchor block embedded in bedrock | Ultra-high strength concrete compressive strength ≥150 MPa; prestressed steel strand tensile strength ≥1860 MPa | Uplift force ≈ maximum cable tension |
| Island Anchor (Galapagos, Kiribati) | Deep-sea suction anchor + mooring cable | Offshore steel yield strength ≥500 MPa; fatigue life >10⁸ cycles | Uplift force + seabed bending moment |
| Deep-sea Floating Platform (Indian Ocean) | Semi-submersible/Spar platform + tension leg | Offshore steel yield strength ≥500 MPa; composite foam density ≤0.5 g/cm³ | Refer to API RP 2SK standard |

#### (2) Ring-Node Connectors

- **Target Parameters**: Load capacity ≥ elevator full load + safety margin; fatigue life >10⁸ cycles.
- **Candidate Materials**: C/SiC composites, carbon/carbon composites.
- **Precise configuration to be completed in Volume III**.

#### (3) Node Space Station Structure

- **Materials**: Aluminum alloys (5xxx/6xxx/7xxx series), CFRP trusses.

### 2.7.3 Elevator Climber Materials and Drive Schemes

#### (1) Drive Scheme Selection

| Scheme | Principle | Advantages | Disadvantages |
|------|------|------|------|
| **Scheme A: Direct Clamping** | Drive wheels directly clamp the load-bearing cable surface | Simple structure, no extra track needed | Long-term cable wear |
| **Scheme B: External Running Track Sheath** | Wear-resistant track sheath covers the load-bearing cable, drive wheels contact the track sheath | Protects load-bearing cable, replaceable wear parts | Increased weight, requires additional on-orbit sheath installation |

**Recommended Path**: Scheme A for stages 1–2, switch to Scheme B for stages 3–4.

#### (2) Materials and Engineering Parameters for Scheme B

| Parameter | Target Value | Derivation Basis |
|------|------|------|
| Track Sheath Material | UHMWPE or polyurethane | High wear resistance, low friction coefficient, vacuum compatible |
| Track Sheath Thickness | ~5 mm | Replace after wear down to 2 mm |
| Friction Coefficient | 0.1–0.2 | UHMWPE/metal dry friction |

> Note: The dry friction coefficient of UHMWPE with steel/aluminum alloy ranges from 0.05–0.2, depending on surface roughness and contact pressure. This volume takes 0.1–0.2 as a conservative engineering value, covering all possible conditions from polished surfaces (μ≈0.05–0.1) to rough surfaces (μ≈0.15–0.2). The final value must be determined by scaled model friction tests in Volume IV (To Be Verified-V4-N5) under simulated actual contact stress.

| Parameter | Target Value | Derivation Basis |
|------|------|------|
| Design Life | ≥ 10 years (replaceable) | Estimated by annual operating mileage |
| Cable Linear Density Increment | ~0.03–0.05 kg/m | Outer diameter increases by 10 mm |
| On-Orbit Sheath Installation Process | To be verified | To be detailed in Volume VI |

> The above cable linear density increment and its impact on the total ring linear density and overall structural modes will be calculated uniformly by Volume VII after the median λ is officially output by Volume II. Precise values and on-orbit sheath installation process will be determined in detail design by Volumes IV and VI.

#### (3) Car Energy Supply Schemes

| Scheme | Principle | Maturity | Applicable Stage |
|------|------|------|------|
| **Ground Conductive Track Power Supply** | Conductive track laid on cable, power supplied via sliding contact | Highly mature in electrified rail transit | Stages 1–2 (within atmosphere) |
| **Ground Laser Power Transmission** | Ground-based infrared laser illuminates photovoltaic cells on car bottom | Multiple kilometer-scale ground competition verifications | Transitional scheme for stages 1–2 |
| **Ring Solar-Pumped Laser Power Transmission** | Solar-pumped lasers deployed on GEO or ring | Concept research stage | After stage 4 |
| **Electrodynamic Tether** | Use cable itself or additional wires as electrodynamic tether | Concept research exists | Long-term alternative |

**Recommended Scheme**: Hybrid approach. Use conductive track power supply within the atmosphere, gradually transition to other methods for the out-of-atmosphere segment according to construction stage.

#### (4) Key Component Material Parameters

| Component | Material Requirements | Candidate Materials | Target Parameters |
|------|------|------|------|
| Drive Wheel/Clamping Mechanism (Scheme A) | Friction interface with CNT cable | Ceramic matrix composites, carbon/carbon composites | Friction coefficient ≥0.3 |
| Drive Wheel (Scheme B) | Contact with track sheath | Steel or aluminum alloy | Friction coefficient 0.1–0.2 |
| Structural Frame | Lightweight, high rigidity | CFRP, titanium alloy | Specific stiffness ≥25×10⁶ m²/s² |
| Energy Receiving Panel (Laser Power Transmission) | High photoelectric conversion efficiency | Multi-junction GaAs photovoltaic cells | Conversion efficiency ≥40% |
| Life Support System Shell (Manned Car) | Airtight, radiation resistant | Aluminum alloy + multilayer insulation blanket | Leak rate ≤10⁻⁶ Pa·m³/s |

### 2.7.4 Ring Auxiliary Facility Materials

- **Solar Cell Array**: Multi-junction GaAs or perovskite/silicon tandem cells.
- **Communication Equipment**: CFRP antennas, ULE optical lenses.
- **On-Orbit Maintenance Robots**: Aluminum alloy/titanium alloy frame, radiation-hardened chips.
- **Habitat Module**: Multilayer protective structure—aluminum alloy + UHMWPE fiber fabric + multilayer insulation blanket.

### 2.7.5 High-Latitude HAPS Materials

| Component | Target Parameter | Candidate Materials |
|------|------|------|
| Airship/Balloon Envelope | Areal density ≤200 g/m² | Multilayer composite film |
| Tether Cable | Tensile strength ≥3 GPa | PBO (Zylon) or Dyneema braided cable |
| Solar Cell | Flexible thin film | Amorphous silicon or CIGS |

### 2.7.6 Summary of Material Requirements

| Material Category | Application Part | Key Candidate Materials | Target Performance Keywords |
|------|------|------|------|
| CNT | Main ring, elevator cable | MWCNT braided cable (wall number unlimited in long term) | Engineering strength ≥20 GPa |
| Structural Metals | Anchors, nodes, robots | Offshore steel, aluminum alloy, titanium alloy | Yield/tensile strength |
| Composites | Connectors, climber frame | CFRP, carbon/carbon, C/SiC | Specific stiffness |
| Polymer Materials | Cable track sheath, tether cable | UHMWPE, PBO, Dyneema | Wear resistance, low permeability |
| Functional Materials | Photovoltaics, optics, radiation protection | GaAs, ULE glass, UHMWPE fiber | Conversion efficiency, radiation resistance |
| Coating Materials | LEO segment cable protection | Silica coating | Atomic oxygen resistance |


## 2.8 Conclusion of Volume II

This volume has completed the preliminary demonstration of material selection and engineering path for the ring elevator cable, and systematically sorted out the material requirements and design targets for other key parts of the ring elevator system. Core conclusions:

1. **CNT** is the only known material that can simultaneously meet strength and density requirements. MWCNT is selected as the current design reference material.
2. The strength loss model from single filament to cable has been established. The current measured f₁ of CNT yarn is about 0.11–0.175, which is 3–5 times lower than the target f₁=0.5. Using the upper limit of MWCNT single filament strength (~80 GPa) as the reference, optimistic loss yields engineering strength ≈19.6 GPa, just reaching the 20 GPa threshold.
3. The cross-section adopts a multi-level redundant braided structure, with a target redundancy of ≥1000 strands. The derivation premise and conservative margin selection for N_min have been clearly given.
4. In-situ lunar manufacturing of CNT is the material prerequisite for realizing the ring elevator. JAXA has achieved in-situ CVD growth of CNT on lunar regolith simulant [2.30], and the discovery of natural CNT in Chang'e 6 lunar soil provides an environmental analogy for artificial synthesis on the Moon [2.11].
5. Carbon source supply adopts a multi-path parallel strategy: C-type asteroid capture as the main path, while systematically exploring and evaluating local lunar carbon sources.
6. Recommended drive scheme path (Scheme A→Scheme B), track sheath material parameters, and friction coefficient sources have been clearly marked.
7. Material selection directions and target parameters for key parts of the ring elevator system such as anchor structures, elevator climbers, ring auxiliary facilities, and HAPS have been given one by one. **For atomic oxygen erosion, the LEO segment of the elevator cable requires a SiO₂ or Al₂O₃ protective coating on the outer UHMWPE layer, thickness ≥5 μm, design life ≥10 years, pending To Be Verified V2-M9.**

**Current Status**: This volume can be independently concluded at the material demonstration level. To Be Verified-V2-M1 to V2-M10 are the core tasks for the next stage of material experiments and space resource development.


## References

[2.1] Toyobo Co., Ltd. *Zylon (PBO Fiber) Technical Data Sheet*. 2020.

[2.2] DuPont. *Kevlar Aramid Fiber Technical Guide*. 2019.

[2.3] Avient (formerly DSM Dyneema). *Dyneema HB210 Product Data*. 2018.

[2.4] Weihai Guangwei Composites Co., Ltd. *GQ4522 (T800 Grade) Carbon Fiber Product Data Sheet*. 2023.

[2.5] Zhongfu Shenying Carbon Fiber Co., Ltd. *SYT65 (T1000 Grade) Carbon Fiber Product Data Sheet*. 2022.

[2.6] Bai, Y., Zhang, R., Ye, X., et al. "Carbon nanotube bundles with tensile strength over 80 GPa." *Nature Nanotechnology*, Vol. 13, 2018, pp. 589–595.

[2.7] Peng, B., Locascio, M., Zapol, P., et al. "Measurements of near-ultimate strength for multiwalled carbon nanotubes and irradiation-induced crosslinking improvements." *Nature Nanotechnology*, Vol. 3, 2008, pp. 626–631.

[2.8] "Carbon Nanotube Tensile Strength." *Baidu Encyclopedia*.

[2.9] Behabtu, N., Young, C. C., Tsentalovich, D. E., et al. "Strong, light, multifunctional fibers of carbon nanotubes with ultrahigh conductivity." *Science*, Vol. 339, 2013, pp. 182–186.

[2.10] Schörghofer, N., & Williams, J.-P. "Carbon dioxide cold traps on the Moon." *Geophysical Research Letters*, Vol. 48, 2021, e2021GL095533.

[2.11] Jilin University News Center. "Discovery of Natural Single-Walled Carbon Nanotubes in Chang'e 6 Lunar Soil." January 21, 2026.

[2.12] "C-type Asteroid." *Baidu Encyclopedia*.

[2.13] Nakamura, T., Noguchi, T., Tanaka, M., et al. "Ryugu sample return: first results." *Science*, Vol. 375, 2022, pp. 1011–1020.

[2.14] Chinese Academy of Engineering, *Engineering*. "2025 Global Engineering Frontiers—In-situ Utilization of Lunar Resources." December 2025.

[2.15] Zhang, W., et al. "Natural single-walled carbon nanotubes in Chang'e-6 lunar samples." *Nano Letters*, 2026.

[2.16] Reference News. "Hong Kong Media: New Discovery in Chang'e 6 Lunar Soil Research." January 7, 2026.

[2.17] ICE-CSIC. "Precise chemical composition of six common carbonaceous chondrites." *Monthly Notices of the Royal Astronomical Society*, 2025.

[2.18] Lauretta, D. S., et al. "Preliminary analysis of Bennu samples." *Nature*, 2024.

[2.19] TransAstra. "Mini Bee Capture Bag: ISS Technology Demonstration Success." Press Release, October 2025.

[2.20] "Asteroid Mining Market 2025 Valuation and 2032 Forecast." Industry Report, 2025.

[2.21] AstroForge. "Odin Mission." Company Briefing, February 2025.

[2.22] China National Space Administration. "Tianwen-2 Mission Overview." May 2025.

[2.23] Wang Wei. "Four-Stage Development Roadmap for Solar System Resource Development before 2100." China Aerospace Science and Technology Corporation, 2023.

[2.24] China National Space Administration. "Chang'e 7 Mission Overview." 2026.

[2.25] Tsentalovich, D. E., et al. "Influence of carbon nanotube characteristics on macroscopic fiber properties." *ACS Nano*, Vol. 11, 2017, pp. 11008–11016.

[2.26] Zhang, X., Bai, Y., et al. "Carbon nanotube fibers with dynamic strength up to 14 GPa." *Science*, Vol. 384, 2024, pp. 1318–1323.

[2.27] Bai, Y., et al. "Super-durable ultralong carbon nanotubes." *Science*, Vol. 369, 2020, pp. 1104–1106.

[2.28] Beese, A. M., et al. "Key factors limiting carbon nanotube yarn strength." *ACS Nano*, Vol. 8, 2014, pp. 11454–11466.

[2.29] Zhong, X. H., et al. "Carbon nanotube yarns with tunable surface functionality." *Carbon*, Vol. 95, 2015, pp. 1020–1028.

[2.30] JAXA Research Team. "Direct synthesis of carbon nanotubes on lunar regolith simulant particles." *Carbon*, Vol. 231, 2025, 119751.

[2.31] Smith, J. R., et al. "Carbon from carbonaceous chondrites." *Advances in Space Research*, Vol. 73, 2024, pp. 2345–2356.

[2.32] Yabuta, H., et al. "Macromolecular organic matter in samples from asteroid Ryugu." *Science*, Vol. 379, 2023, pp. 263–269.

[2.33] TransAstra. "Asteroid Capture Mission Roadmap." Company Technology Briefing, 2025.

[2.34] ASTM International. *ASTM G116-99 (Reapproved 2020)*. 2020.

[2.35] International Electrotechnical Commission. *IEC 60068-2-42-2003*. 2003.

[2.36] Palaci, I., et al. "Radial elasticity of multiwalled carbon nanotubes." *Physical Review Letters*, Vol. 94, 2005, 175502.

[2.37] Yang, L., et al. "Toughness of carbon nanotubes conforms to classic fracture mechanics." *Science Advances*, Vol. 2, 2016, e1500969.

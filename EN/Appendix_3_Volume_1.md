# Appendix III: Engineering Project Discussion

## Volume I: Discussion on Space Impact Protection

**Version**: 1.1<br/>
**Date of Preparation**: June 2026<br/>
**Currency Unit**: Renminbi (RMB), symbol: ¥<br/>
**Related Main Volumes**: Main Volume I, Section 1.7.2; Main Volume VI, Section 6.8; Main Volume XII, Section 12.3.3


### Glossary of Abbreviations

| Abbreviation | Full Name | Notes |
|------|----------|------|
| CNT | Carbon Nanotube | Orbital ring elevator cable material |
| DM | Drive Module | Elevator car drive unit |
| GEO | Geostationary Earth Orbit | The orbit where the orbital ring elevator main structure resides |
| LEO | Low Earth Orbit | Low Earth Orbit |
| PM | Payload Module | Elevator car body |
| UHMWPE | Ultra-High Molecular Weight Polyethylene | Outer layer material of the track sleeve |


### 1.1 Volume Preamble

This appendix focuses on scheduling conflicts in single-cable mode and the dual-cable scheme discussion related to space impact protection. It aims to document the scheduling conflict issues among moving bodies (elevator cars, Space Spiders, elastic protection mechanisms, etc.) along the cable in single-cable mode during the orbital ring elevator project, to analyze the feasibility of various protection mechanisms, and to explore the technical and economic costs of the dual-cable scheme (independent ascending and descending cables at each elevator node). The content of this appendix constitutes an exploratory record and does not serve as a baseline requirement for the current engineering scheme.

This volume builds upon:
- **Main Volume I**: Physical protection strategies against orbital debris and micrometeorite impact risks.
- **Main Volume VI**: In-orbit construction and maintenance functions of the Space Spider.
- **Main Volume XII**: Emergency redundancy and lifeline engineering debris protection design.


### 1.2 The Core Contradiction of Single-Cable Scheduling Conflicts

In single-cable mode, elevator cars (high-speed operation, up to 416 m/s) and maintenance mechanisms such as Space Spiders (low-speed operation, approximately 0.05 m/s) share the same cable. When the two meet, evasion is almost infeasible:

- **Enormous speed differential**: From a 1 km warning distance to a rear-end collision is only approximately 2.4 seconds (at 416 m/s).
- **Low-speed mechanism cannot evade in time**: It is nearly impossible for a Space Spider to complete "detach from cable → evade → return" within 2.4 seconds.
- **Track monopolization**: Any other mechanism moving along the cable will block the elevator car passage.

The original scheme implicitly assumed that "after the construction phase, Space Spiders only operate during elevator car downtime windows," but this contradicts the commercial goal of "24/7 round-the-clock transportation." Forcing elevator car shutdowns for maintenance would result in a loss of approximately 10%–15% of capacity.


### 1.3 Discussion on Attached and Open-Close Protection Mechanisms

To counter debris impact threats, beyond fixed multi-layer redundancy and consumable outer layers, two types of movable/openable protection mechanisms were conceived. Upon analysis, both produce irreconcilable scheduling conflicts with elevator cars sharing the same cable, and both have extremely high engineering complexity.

#### 1.3.1 Attached Elastic Protection Mechanism

**Concept**: A Whipple shield device that can move along the cable, attaching to the cable rack via a small mechanism, detaching from the cable when an elevator car approaches, and re-attaching afterward.

**Problems**:
- Shares the same cable with elevator cars; moves extremely slowly (<0.1 m/s), making it impossible to complete detachment and evasion before a high-speed approaching elevator car.
- After detachment, requires guide wires and micro-thrusters to return and re-engage, demanding extremely high positioning accuracy in vacuum (±1 mm) with low reliability.
- If deployed along the entire cable, the mechanism's own mass (estimated 50–100 kg per unit) would create an enormous mass burden.

**Conclusion**: Not feasible. Documented as a theoretical concept only.

#### 1.3.2 Open-Close Protection Mechanism (Fixed Base + Openable Shield)

**Concept**: Ring-shaped Whipple shields are fixed on the cable and can open and close like clamshells. Elevator cars have corresponding slot positions; the shields open as the car passes, then close afterward.

**Problems**:
- Elevator cars are sealed pressurized cabins; top-to-bottom slots cannot be cut through the outer shell (this would compromise cabin wall integrity).
- Even if a non-pressurized guide rail housing is attached to the exterior of the shell, it adds extra mass and outer diameter, and sealing is difficult.
- The opening and closing mechanism must be precisely coordinated with elevator car scheduling; any failure could cause the shield to fail to close or the elevator car to jam.
- Full-cable deployment (especially at the LEO segment) requires thousands of units, with a total mass of hundreds of tons and sharply escalating costs.

**Conclusion**: Not feasible due to fundamental conflict with the sealed cabin structure. If fixed Whipple shields were installed only on the ring main structure (the segment without elevator car operation), no opening and closing would be required; however, the ring main structure is at the GEO segment where the debris threat is relatively small. Therefore, the open-close mechanism has no practical engineering value.


### 1.4 Dual-Cable Scheme Architecture and Feasibility Analysis

#### 1.4.1 Architecture Description

Two independent cables are set at each elevator node:
- **Ascending cable** (ground → GEO)
- **Descending cable** (GEO → ground)

Moving bodies such as elevator cars, Space Spiders, and protection mechanisms occupy different cables respectively, completely eliminating scheduling conflicts. Lateral connection mechanisms (such as openable trusses) can be set between the two cables, for use as emergency evasion routes, temporary anchor points, or mutual rescue.

#### 1.4.2 Advantages

- Scheduling conflicts are completely resolved; 24/7 parallel operation is achievable.
- Elastic protection mechanisms and Space Spiders can operate freely along the descending cable without affecting ascending passenger/freight service.
- When one cable fails, the other can temporarily operate bidirectionally (at reduced speed), providing redundant backup.
- Open-close Whipple shields can use the dual cables as mutual anchor points, simplifying the structure.

#### 1.4.3 Disadvantages and Challenges

| Challenge Item | Order-of-Magnitude Estimate | Notes |
|:---|:---:|:---|
| **Total cable mass doubles** | Original single cable ≈8.22×10⁴ t/node → dual cable 1.64×10⁵ t/node, total for 6 nodes ≈9.86×10⁵ t | Doubles |
| **Counterweight requirements double** | Each cable needs an independent counterweight asteroid (8.0×10¹² kg/node) → dual cable 1.6×10¹³ kg/node; asteroid capture missions increase from 12–18 to 24–36 | Doubles |
| **Anchor station scale expands** | Must accommodate fixing mechanisms, diverter pulleys, and independent winches for two cables; anchor well diameter expected to expand 40%–50% | +40%–50% |
| **Connection points on ring double** | Each node increases from 1 to 2 connection points | Doubles |
| **Construction cost doubles** | Cable materials, cable-laying construction, counterweight capture, winches, and other costs double; estimated total investment increases from approximately ¥55–58 trillion to approximately ¥100–110 trillion | ≈+100% |
| **Operational complexity** | Must manage tension balance, thermal compensation coordination, and orbital synchronization of two cables | — |

#### 1.4.4 Key Technical Issues

- **Cable spacing**: Sufficient spacing must be maintained (≥50 m) to prevent entanglement under wind loads and electromagnetic forces. Anchor points and GEO-end connectors must be designed with lateral span.
- **Counterweight scheme**: Independent counterweights (one asteroid per cable), or a shared large counterweight (must be positioned in the direction of resultant force; complex mechanism).
- **Lateral connection mechanisms**: Openable trusses set at regular intervals, adding mass (estimated one set per 10 km, each set weighing several tons).
- **Emergency switching mechanism**: If an elevator car needs to temporarily use the other cable, a switch or line-change mechanism must be designed, of extremely high complexity.


### 1.5 Economic Feasibility Conclusion

The dual-cable scheme resolves scheduling conflicts technically, but doubles the engineering scope and costs. Given that the current investment of ¥55–58 trillion for the orbital ring elevator is already at the margin of economic feasibility, doubling it to ¥100–110 trillion would essentially eliminate the project's investment value.

**Therefore, the dual-cable scheme is not adopted as the current engineering baseline and is documented only as a long-term technical reserve or a locally enhanced scheme for specific high-risk segments.**


### 1.6 Compromise Recommendations

- **Do not adopt full-line dual cable**, but instead set **short dual-cable sections as evasion zones** in **high-risk segments (such as the LEO segment, 400–800 km)**. Elevator cars and Space Spiders only temporarily switch to the other cable during encounters, then switch back after passing. This requires developing a cable switch mechanism; complexity remains high but costs are manageable.
- **Maintain single cable + window scheduling**: Accept the constraint that "Space Spiders only operate during elevator car downtime windows," and direct resources toward the more pressing needs of debris protection and materials research breakthroughs.


### 1.7 Volume Conclusion

This appendix documents the fundamental problem of single-cable scheduling conflicts and a comprehensive analysis of the dual-cable scheme. Current engineering decision: **Single cable + window scheduling as baseline; the dual-cable scheme is explored only as a long-term option**. If material costs decrease significantly or capacity demands surge in the future, the feasibility of the dual-cable scheme can be re-evaluated.

The attached and open-close protection mechanisms are not adopted as current engineering schemes, due to fundamental conflict with the sealed pressurized cabin structure and infeasibility of scheduling.


### References

[1] Main Volume I. *Physics and Orbital Mechanics Fundamentals*. Section 1.7.2.

[2] Main Volume VI. *Toroidal Structure Construction and In-Orbit Assembly*. Section 6.8.

[3] Main Volume XII. *Emergency, Redundancy, and Lifeline Engineering*. Section 12.3.3.

# Appendix IV: Skyhook

## Volume 4: Deployment Schemes and On-Orbit Assembly

**Version**: 1.0
**Compilation Date**: June 2026
**Currency Unit**: Chinese Yuan (CNY), symbol: Y
**Related Main Volumes**: Main Volume 6; Appendix IV Volumes 2 and 3

### 4.1 Opening Notes

This volume addresses engineering deployment and on-orbit assembly for skyhook systems. Because skyhooks are large rotating space structures, full one-piece launch is not practical for operational scales. Therefore, segmented launch, orbital assembly, and controlled deployment are required. This volume covers launch strategy tradeoffs, robotic assembly, tether deployment and tension control, spin-up and angular-momentum management, and early capture-verification mission design.

### 4.2 Launch Approaches

#### 4.2.1 Limitation of One-Piece Launch

Typical half-length l values are 50-500 km, giving total lengths of 100-1000 km. Current fairing envelopes cannot accommodate such continuous structures. One-piece launch is only suitable for very small demonstrations.

#### 4.2.2 Segmented Deployment (Primary Path)

Tether is divided into segments (e.g., 10-50 km each), launched with endpoint hardware, then docked and deployed in orbit.

Approach A: Prefabricated segments + orbital serial docking.
- Strength continuity is good, operation complexity moderate.
- Requires many launches and docking interfaces.

Approach B: On-orbit braided manufacturing.
- Potentially unlimited length and flexible section tuning.
- Technology immaturity and slow production rates.

Approach C: Hybrid (recommended).
- High-load core sections from prefabricated segments.
- Outer extension sections from in-space fabrication.
- Endpoint masses/capture systems launched as integrated units.

#### 4.2.3 Launch Count and Cost Estimate

Representative crewed LEO case (l=134 km, total 268 km):
- Multiple medium/heavy launches required for tether segments, hub, and endpoint masses.
- Total launch campaign on the order of 15-20 launches.
- Deployment cost estimate (excluding full R&D) in the several-hundred-billion-CNY class.

#### 4.2.4 Tether Length Between Platform and Counterweights

In a dumbbell skyhook:
- Core platform is at center of mass.
- Counterweights are at both ends.
- Distance from platform to each counterweight equals half-length l.

This is a mission-defining scale parameter, typically tens to hundreds of kilometers.

### 4.3 On-Orbit Assembly Scheme

#### 4.3.1 Space Spider Robots

Autonomous robots perform segment transport, docking, handling, and optional in-space weaving tasks.

Key capabilities:
- 6-DOF maneuvering (cold-gas/electric propulsion).
- End effectors for docking and tether handling.
- Stereo vision + lidar for cm-level positioning.
- Autonomous fault handling and retry logic.

#### 4.3.2 Docking Mechanism

Interfaces must provide high tensile transfer with low mass and repeatable locking/unlocking.

A cone-and-probe style mechanism is suitable, with guidance, capture, lock transfer path, and electrical pass-through.

#### 4.3.3 Assembly Sequence

1. Deploy core hub/platform first.
2. Add tether segments alternately on both sides.
3. Validate tension and sensors after each installation.
4. Install endpoint masses and capture mechanisms.
5. Conduct integrated commissioning and spin tests.

### 4.4 Tether Deployment and Tension Control

#### 4.4.1 Deployment Methods

- Centrifugal deployment (better for short segments).
- Gravity-gradient deployment (slow but passive in LEO).
- Active robotic deployment (recommended for long segments).

For active deployment, robotic pull-out at controlled line speed with synchronized spool release is preferred.

#### 4.4.2 Tension Control

- Static preload via endpoint thrusters.
- Active trim via telescopic actuators and tension feedback.
- Dynamic damping in capture/release phases to absorb impulse loads.

### 4.5 Spin-Up and Angular-Momentum Management

#### 4.5.1 Spin-Up Options

A. Differential endpoint thrust (primary method).
B. Gravity-gradient assisted spin-up (limited control authority).
C. Incremental momentum build-up through asymmetric operational captures (supplementary).

Primary recommendation: A, assisted by C where operationally useful.

#### 4.5.2 Momentum Management Subsystem

- Reaction-wheel cluster for small fluctuations.
- Endpoint thrusters for large corrections.
- Magnetic torque options in LEO if conductive loops are integrated.

### 4.6 Early Capture Verification Missions

Staged mission progression (low risk to high realism):

| Stage | Payload Type | Payload Mass | Capture Mode | Release Target | Primary Validation |
|:---:|:---|:---:|:---|:---|:---|
| V1 | Simulated mass | 100 kg | Passive hook capture | Same orbit | Endpoint tracking and mechanism function |
| V2 | Small satellite | 500 kg | Active damped capture | Higher orbit | Relative-velocity control, exchange efficiency |
| V3 | Standard cargo module | 5000 kg | Fully autonomous capture | Cislunar transfer | Large-mass tension response, safe release |
| V4 | Crewed analog capsule (uncrewed) | 8000 kg | Crewed-grade damping | Return trajectory test | Acceleration compliance verification |

### 4.7 Volume Summary

1. Segmented deployment is the only practical path for operational-scale skyhooks.
2. Robotic assembly and high-strength docking interfaces are central enabling technologies.
3. Active deployment and closed-loop tension control are preferred for reliability.
4. Differential-thrust spin-up plus dedicated momentum management is feasible.
5. Multi-stage capture verification is mandatory before commercial operation.

### Parameter Outputs

| Parameter | Value | Status | Receiving Volume |
|:---|:---|:---|:---|
| Typical launch count (operational skyhook) | 15-20 | Estimate | Volume 6 |
| Deployment total cost (excluding R&D) | 60-80 billion CNY class | Estimate | Volume 6 |
| Prefabricated segment length | 20-50 km | Design | Volume 3 |
| Spider robot mass | 200-500 kg | Baseline | Volume 6 |
| Docking-interface mass (per end) | 100-150 kg | Baseline | Volume 3 |
| Spin-up duration (reference case) | ~3.15 days | Estimate | Volume 5 |
| Spin-up propellant fraction | ~18.5% of system mass | Estimate | Volume 6 |
| Capture verification stage count | 4 | Baseline | Volume 7 |
| Platform-counterweight tether distance | equals half-length l | Design | Volumes 2 and 3 |

### References

[1] Long March 5 User Manual, 2020.
[2] NASA robotic assembly technical memo, 2020.
[3] Li Dong et al., large truss on-orbit assembly review, 2021.
[4] Cosmo & Lorenzini, Tethers in Space Handbook, 1997.
[5] Penzo, deployment and control of spinning tethers, 1992.
[6] NASA, International Docking System Standard, 2016.

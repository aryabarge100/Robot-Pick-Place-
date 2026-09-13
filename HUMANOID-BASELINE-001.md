# HUMANOID-BASELINE-001

## BHIV 17-DOF Humanoid — Mechanical Baseline Recovery & Evidence Register

**Task ID:** ARYA-HUMANOID-001
**Product:** BHIV 17-DOF Humanoid Robot
**Primary Owner:** Arya Barge
**Role:** Mechanical Realisation & Manufacturing Owner
**Architecture Integration Owner:** Manya
**Electronics / Telemetry Interface:** Dhruv / Siddhesh
**Authority:** TMS / GC / MDU
**Baseline ID:** HUMANOID-BASELINE-001
**Status:** RECOVERED BASELINE — PARTIAL EVIDENCE / OPEN ITEMS REMAIN

---

## 1. Purpose

This document establishes the recovered mechanical baseline for the existing BHIV 17-DOF Humanoid Robot.

The purpose is to document:

* the existing design information recovered so far;
* available CAD and mechanical evidence;
* known dimensions and mass properties;
* available actuator and electronics information;
* mechanical subsystem structure;
* current manufacturing/procurement evidence;
* known interface information;
* as-designed versus as-built status;
* missing CAD, parts, measurements and approvals;
* unresolved architecture and engineering questions.

This document is a **baseline recovery record**, not a redesign document.

Where the available evidence is incomplete, the value is explicitly marked as:

* `VERIFIED` — directly supported by available evidence;
* `REFERENCE` — available design/reference information but not sufficient to establish final canonical configuration;
* `PROPOSED` — engineering proposal/release from an integration document, not yet established as canonical;
* `TBD` — value is not yet frozen;
* `UNKNOWN` — information has not been recovered;
* `NOT VERIFIED` — information exists but physical/design verification has not been completed;
* `BLOCKED` — required evidence or hardware is unavailable.

No missing architecture value has been inferred or silently substituted.

---

# 2. Baseline Recovery Principle

The existing humanoid architecture must be recovered before making mechanical changes.

The following rules apply to this baseline:

1. Existing CAD and design intent are preserved as the source of truth wherever available.
2. No joint/DOF architecture is silently changed.
3. No actuator is assigned to a joint solely because it appears in a later procurement proposal.
4. No physical manufacturing status is claimed without physical evidence.
5. No qualification result is claimed without measured test evidence.
6. No final mass or centre-of-mass value is invented from incomplete CAD.
7. Reference dimensions are retained as reference until their corresponding CAD/revision is confirmed.
8. Proposed electronics and actuator selections remain clearly separated from the recovered canonical mechanical architecture.
9. Architecture changes affecting DOF, actuator selection, packaging, battery placement, major mounting interfaces or mass distribution require formal review.

---

# 3. Current Baseline Status

The BHIV humanoid is an existing **17-DOF humanoid robot programme**.

The mechanical baseline information recovered to date consists of:

* existing humanoid CAD/reference files;
* part dimensions and mass information from supplied CAD;
* torso, thigh, leg and motor reference data;
* earlier BOM/R&D information;
* actuator reference information;
* Siddhesh's latest electronics/mechanical integration release;
* electronics packaging requirements;
* proposed actuator envelopes and mounting requirements;
* battery and power-system planning information.

However, the complete set of humanoid mechanical parts and canonical CAD revisions has **not** been received/recovered.

Therefore, this baseline is classified as:

> **PARTIAL BASELINE — sufficient to establish the currently recovered design evidence, but not sufficient to claim complete physical or manufacturing closure.**

---

# 4. System-Level Mechanical Baseline

| Parameter                                  |                   Recovered Value | Status                      | Evidence / Note                                             |
| ------------------------------------------ | --------------------------------: | --------------------------- | ----------------------------------------------------------- |
| Robot                                      |                     BHIV Humanoid | VERIFIED                    | Existing project/task context                               |
| Degrees of Freedom                         |                            17 DOF | VERIFIED at programme level | Task definition                                             |
| Canonical joint-by-joint 17-DOF allocation |               Not fully recovered | UNKNOWN                     | Requires canonical architecture source                      |
| Overall CAD envelope                       |         1639.63 × 546.94 × 260 mm | REFERENCE                   | Reported from available Dynamixel assembly/reference data   |
| Final assembled physical dimensions        |                      Not measured | NOT VERIFIED                | Physical prototype evidence unavailable                     |
| Final robot mass                           |                   Not established | UNKNOWN                     | Available individual CAD masses are incomplete/inconsistent |
| Final centre of mass                       |                   Not established | UNKNOWN                     | Requires complete assembly and/or validated mass model      |
| Support polygon                            |                   Not established | UNKNOWN                     | Requires final foot geometry and complete mass/CoM          |
| Static stability                           |                     Not qualified | NOT VERIFIED                | No physical qualification evidence available                |
| Final actuator allocation                  | Not frozen from baseline evidence | TBD                         | Siddhesh release contains proposed actuator architecture    |
| Final battery                              |                        Not frozen | TBD                         | Dependent on power calculation and vendor selection         |
| Final electronics carrier/enclosure        |                        Not frozen | TBD                         | STM32 carrier and packaging details remain open             |

---

# 5. 17-DOF Baseline

## 5.1 Programme-Level DOF

The task establishes the product as a **17-DOF humanoid**.

The exact canonical joint allocation must be recovered from the authoritative humanoid architecture/CAD.

The previously circulated joint tables contained configurations that could total more than 17 DOF. Therefore those tables are **not treated as the canonical 17-DOF map without source verification**.

### Current status

| Requirement                       | Status                      |
| --------------------------------- | --------------------------- |
| 17-DOF product definition         | VERIFIED                    |
| Joint-by-joint allocation         | UNKNOWN / EVIDENCE REQUIRED |
| Joint axis definition             | UNKNOWN / EVIDENCE REQUIRED |
| Actuator per canonical joint      | UNKNOWN / EVIDENCE REQUIRED |
| Mechanical ROM per joint          | UNKNOWN / EVIDENCE REQUIRED |
| Joint mounting orientation        | PARTIAL                     |
| Final actuator mounting interface | PARTIAL / PROPOSED          |
| Final joint torque requirement    | NOT VERIFIED                |

### Baseline rule

The 17-DOF map shall be populated directly from the authoritative CAD/architecture record once available.

Until then:

> **No proposed 20-DOF table, actuator quantity table, or individual joint proposal is treated as the canonical 17-DOF architecture.**

---

# 6. Recovered Mechanical CAD Data

The following mechanical data has been recovered from the available CAD/reference information.

## 6.1 Torso Components

| Part / Reference | External Dimensions (L × W × H) | Reported Mass | Status       |
| ---------------- | ------------------------------: | ------------: | ------------ |
| Torso Proto K    |      210.23 × 150.53 × 38.86 mm |      595.43 g | REFERENCE    |
| Torso Proto D    |         210.23 × 150.53 × 90 mm |     1204.17 g | REFERENCE    |
| Torso Proto B    |        424.96 × 331.28 × 140 mm |    12342.28 g | NOT VERIFIED |
| Hip Motor        |                 80 × 80 × 70 mm |      681.30 g | REFERENCE    |

### Torso observation

The reported Torso Proto B mass is substantially larger than the other torso references and therefore requires confirmation against the source CAD/material definition before being used for final mass or actuator calculations.

It is retained in this baseline for traceability but **must not be treated as a validated final torso mass**.

---

## 6.2 Leg / Limb Components

| Part / Reference     | External Dimensions (L × W × H) | Reported Mass | Status                   |
| -------------------- | ------------------------------: | ------------: | ------------------------ |
| Thigh                |         421.04 × 100 × 84.96 mm |     7464.06 g | REFERENCE / NOT VERIFIED |
| Leg G                |         529.03 × 321.6 × 200 mm |    14925.45 g | NOT VERIFIED             |
| MG996R Servo Bracket |               63.3 × 40 × 24 mm |       21.22 g | REFERENCE                |

The reported masses for the Thigh and Leg G require source-CAD/material verification before they can be used in final robot mass, torque or CoM calculations.

---

# 7. Overall CAD Assembly Evidence

An available humanoid assembly/reference reports an overall envelope of approximately:

**1639.63 × 546.94 × 260 mm**

This is retained as a **reference CAD envelope**.

It is not claimed as the final physical robot envelope because:

* complete final CAD revision has not been recovered;
* physical prototype dimensions have not been measured;
* some individual component files remain unavailable or unresolved;
* assembly configuration/revision must be confirmed.

---

# 8. Mechanical Subsystem Baseline

The humanoid is decomposed into the following mechanical subsystems for baseline recovery and manufacturing:

1. Head
2. Neck
3. Torso
4. Left arm
5. Right arm
6. Shoulder joints
7. Elbow joints
8. Hand/finger mechanisms
9. Hip structure
10. Left leg
11. Right leg
12. Knee joints
13. Ankle joints
14. Feet
15. Battery mounting
16. Electronics packaging
17. Sensor mounting
18. Cable routing and service access

The subsystem list is a mechanical decomposition and does not itself define the canonical DOF count.

---

# 9. As-Designed / As-Built Matrix

| Subsystem             | CAD Exists    | Manufactured | Physically Tested | Evidence                          | Revision | Status  |
| --------------------- | ------------- | ------------ | ----------------- | --------------------------------- | -------- | ------- |
| Head                  | Partial       | Unknown      | No evidence       | CAD/reference files               | TBD      | PARTIAL |
| Neck                  | Partial       | Unknown      | No evidence       | Reference CAD + actuator proposal | TBD      | PARTIAL |
| Torso                 | Yes / Partial | Unknown      | No evidence       | Torso CAD references              | TBD      | PARTIAL |
| Left Arm              | Partial       | Unknown      | No evidence       | CAD/reference data                | TBD      | PARTIAL |
| Right Arm             | Partial       | Unknown      | No evidence       | CAD/reference data                | TBD      | PARTIAL |
| Shoulder              | Partial       | Unknown      | No evidence       | Actuator/mechanical reference     | TBD      | PARTIAL |
| Elbow                 | Partial       | Unknown      | No evidence       | Actuator/mechanical reference     | TBD      | PARTIAL |
| Hands/Fingers         | Partial       | Unknown      | No evidence       | XL330 reference                   | TBD      | PARTIAL |
| Hip                   | Partial       | Unknown      | No evidence       | Hip motor/reference CAD           | TBD      | PARTIAL |
| Left Leg              | Partial       | Unknown      | No evidence       | Thigh/leg references              | TBD      | PARTIAL |
| Right Leg             | Partial       | Unknown      | No evidence       | Thigh/leg references              | TBD      | PARTIAL |
| Knee                  | Partial       | Unknown      | No evidence       | Actuator proposal                 | TBD      | PARTIAL |
| Ankle                 | Partial       | Unknown      | No evidence       | Actuator proposal                 | TBD      | PARTIAL |
| Feet                  | Partial       | Unknown      | No evidence       | CAD/reference data                | TBD      | PARTIAL |
| Battery mounting      | Not complete  | No evidence  | No                | Packaging proposal                | TBD      | OPEN    |
| Electronics packaging | Partial       | No evidence  | No                | Siddhesh integration release      | V1 / TBD | OPEN    |
| Sensors               | Partial       | No evidence  | No                | IMU/camera planning               | TBD      | OPEN    |
| Cable routing         | Partial       | No evidence  | No                | Integration requirements          | TBD      | OPEN    |

**Important:** `Unknown` or `No evidence` means evidence was not available for this baseline. It does not mean that the corresponding component definitely does not exist.

---

# 10. Actuator Baseline

## 10.1 Earlier Actuator Reference

The earlier Phase-I electronics/R&D information referenced the:

**ROBOTIS XM430-W350-T**

Reference characteristics:

* Stall torque: approximately 4.1 N·m
* Rated torque: approximately 0.82 N·m
* Mass: approximately 82 g
* Encoder resolution: 4096-step class
* Communication: TTL / RS-485 class interface

This actuator is retained as a **historical/reference actuator**, not as the confirmed actuator for every humanoid joint.

---

# 11. Siddhesh Mechanical Integration Release

Siddhesh's latest mechanical-integration release proposed a BLDC actuator architecture for mechanical packaging.

This information is important for mechanical integration but is **not automatically the canonical 17-DOF baseline**.

## 11.1 Proposed AK60-39 V3.0

| Parameter         |             Proposed Value |
| ----------------- | -------------------------: |
| Actuator          | CubeMars AK60-39 V3.0 KV80 |
| Proposed quantity |                         12 |
| Voltage           |                       48 V |
| Rated torque      |                     24 N·m |
| Peak/stall torque |                     72 N·m |
| Envelope          |                Ø79 × 67 mm |
| Mass              |                 750 g each |
| Communication     |     CAN + power integrated |

Proposed application:

* Shoulder: 4
* Hip: 6
* Knee: 2

Total proposed AK60 mass:

**12 × 0.75 kg = 9.00 kg**

---

## 11.2 Proposed AK45-36

| Parameter         |        Proposed Value |
| ----------------- | --------------------: |
| Actuator          | CubeMars AK45-36 KV80 |
| Proposed quantity |                     8 |
| Voltage           |                  24 V |
| Rated torque      |                 8 N·m |
| Peak torque       |                24 N·m |
| Envelope          |           Ø55 × 54 mm |
| Mass              |            340 g each |
| Communication     |    CAN + power + UART |

Proposed application:

* Neck: 2
* Elbow: 2
* Ankle: 4

Total proposed AK45 mass:

**8 × 0.34 kg = 2.72 kg**

---

## 11.3 Proposed XL330 Finger Actuators

| Parameter           |       Proposed Value |
| ------------------- | -------------------: |
| Actuator            | ROBOTIS XL330-M288-T |
| Proposed quantity   |                   10 |
| Recommended voltage |                  5 V |
| Dimensions          |      20 × 34 × 26 mm |
| Mass                |            18 g each |
| Stall torque        |             0.52 N·m |
| Interface           |      TTL half-duplex |

Proposed application:

* 5 actuators per hand
* 10 actuators total

Total proposed XL330 mass:

**10 × 0.018 kg = 0.18 kg**

The stall torque is a momentary limit and must not be treated as continuous operating torque.

---

# 12. Proposed Actuator Quantity Summary

The latest integration release proposes:

| Actuator     | Quantity | Approx. Total Mass |
| ------------ | -------: | -----------------: |
| AK60-39      |       12 |            9.00 kg |
| AK45-36      |        8 |            2.72 kg |
| XL330-M288-T |       10 |            0.18 kg |
| **Total**    |   **30** |       **11.90 kg** |

### Baseline classification

**PROPOSED — NOT CANONICAL**

This quantity table must not be interpreted as proof that the 17-DOF humanoid contains 30 actuated axes.

The difference exists because the actuator release includes proposed actuator quantities for the mechanical/electronics integration architecture, including hand/finger actuators.

Final actuator allocation requires:

* canonical 17-DOF architecture;
* joint-by-joint mapping;
* torque calculation;
* actual limb geometry;
* mass/CoM calculation;
* official actuator drawings;
* formal architecture approval where required.

---

# 13. Actuator Mechanical Interface Evidence

## AK60-39

Reported mechanical envelope:

**Ø79 × 67 mm**

Reported interface information includes:

* 8 × M3 × 6 holes on approximately Ø68 mm pattern;
* additional M4 and locating-feature callouts;
* exact hole centre locations require confirmation from the official 2D manufacturer drawing.

Mechanical implementation requirement:

> Exact mounting-hole coordinates and fastener engagement shall be taken from the manufacturer drawing before final machining/drawing release.

---

## AK45-36

Reported mechanical envelope:

**Ø55 × 54 mm**

Reported interface information includes:

* 5 × M3 × 5 mounting features on approximately Ø48 mm pattern;
* additional M3 feature callouts;
* exact hole coordinates require manufacturer-drawing verification.

---

## XL330-M288-T

Reported envelope:

**20 × 34 × 26 mm**

Mechanical integration requires:

* servo frame geometry;
* horn geometry;
* mounting-hole locations;
* correct M2 fasteners;
* cable exit/service access.

Exact coordinates are to be taken from the applicable ROBOTIS CAD/drawing.

---

# 14. Electronics Mechanical Integration Baseline

The latest Siddhesh release provides the following planning envelopes.

| Component                  | Qty |          Planning Envelope | Mechanical Zone     | Status   |
| -------------------------- | --: | -------------------------: | ------------------- | -------- |
| STM32G431 controller       |   1 |           ~70 × 50 × 20 mm | Upper/central torso | PROPOSED |
| CAN interface              |  1+ |           ~30 × 25 × 10 mm | Near STM32          | PROPOSED |
| PDB                        |   1 |          ~100 × 70 × 25 mm | Lower/central torso | PROPOSED |
| 48→24 V DC-DC              |   1 |           ~60 × 40 × 25 mm | Power bay           | PROPOSED |
| 48→5 V DC-DC               |   1 |           ~60 × 40 × 25 mm | Torso/hand bay      | PROPOSED |
| 3.3 V regulator            |   1 |           ~50 × 30 × 20 mm | Electronics bay     | PROPOSED |
| MPU6050                    |   1 |           ~25 × 20 × 10 mm | Central torso       | PROPOSED |
| Fuse + holder              |   1 |           ~50 × 30 × 25 mm | Battery positive    | PROPOSED |
| Isolation switch/contactor |   1 |           ~60 × 40 × 30 mm | Battery/PDB         | PROPOSED |
| E-stop                     |   1 | ~50 × 30 × 25 mm interface | Accessible torso    | PROPOSED |
| Current sensor             | 1–2 |           ~30 × 20 × 15 mm | PDB                 | PROPOSED |
| Voltage sensing            |   1 |           ~30 × 20 × 15 mm | PDB                 | PROPOSED |

These are **mechanical planning envelopes**, not final manufacturing dimensions.

---

# 15. Power / Battery Mechanical Baseline

The latest integration release proposes a 48 V-class battery architecture for the AK60 system.

Reference battery class:

* approximately 960–1064 Wh;
* 48 V-class Li-ion/NMC;
* final BMS/pack current must be determined from the validated power budget.

A previously referenced 48 V / 20 Ah NMC example was approximately:

* 53.2 V nominal;
* 20 Ah;
* 1064 Wh;
* 248 × 159 × 95 mm;
* approximately 6.1 kg.

This is a **reference battery example only**, not the final selected battery.

Another reference was approximately:

* 48.1 V nominal;
* 20 Ah;
* ~962 Wh;
* 253 × 156 × 171 mm;
* approximately 8 kg.

This is also a reference only.

### Current baseline

**Final battery: TBD**

Battery selection must follow:

1. validated actuator current requirements;
2. validated duty cycle;
3. mechanical packaging volume;
4. mounting/interface requirements;
5. BMS capability;
6. connector rating;
7. safety requirements;
8. final mass/CoM impact.

---

# 16. Mechanical Packaging Zones

The recovered integration proposal divides the humanoid packaging into:

### Upper Torso

* STM32 controller
* CAN interface
* IMU
* USB/debug access

### Lower/Central Torso

* Battery
* PDB
* Fuse
* Isolation system
* E-stop

### Power Bay

* 48→24 V conversion
* 48→5 V conversion
* regulation and power distribution

### Limb Zones

* AK60 shoulder/hip/knee actuators
* AK45 neck/elbow/ankle actuators
* XL330 hand/finger actuators

These zones are **integration proposals**, not proof of final physical packaging.

---

# 17. Connector and Cable Routing Baseline

The latest integration information identifies the following mechanical requirements.

## AK60

* XT30-class power/CAN interface;
* connector directed toward protected cable channel;
* cable routing must not cross rotating interfaces;
* protected service loop required.

## AK45

* XT30PW-M power;
* CAN connector;
* UART connector;
* bend radius and service loop must remain outside pinch/interference regions.

## XL330

* 3-pin TTL interface;
* cable exits from servo side;
* hand actuators are planned as a daisy-chain bus;
* cable access must remain serviceable.

## STM32

* USB access required;
* CAN/UART/GPIO interfaces required;
* debug access should remain available after shell closure.

### Current status

**Cable routing: PARTIAL / NOT PHYSICALLY VERIFIED**

Final cable routing requires complete CAD assembly and physical interference validation.

---

# 18. Materials and Manufacturing Baseline

The recovered information indicates that the humanoid mechanical parts include a combination of:

* CAD-designed structural components;
* machined/manufactured components;
* 3D-printable components;
* purchased actuator/interface components;
* brackets and mounting hardware.

However, a complete part-by-part material and manufacturing-process record has not yet been recovered.

Therefore:

| Manufacturing Attribute       | Status  |
| ----------------------------- | ------- |
| Complete part manifest        | OPEN    |
| Complete material schedule    | OPEN    |
| Printable part classification | PARTIAL |
| Machined part classification  | PARTIAL |
| Purchased part classification | PARTIAL |
| Final STL package             | OPEN    |
| Dimensioned drawings          | PARTIAL |
| GD&T package                  | OPEN    |
| Print orientation             | OPEN    |
| Post-processing specification | OPEN    |
| Heat-set insert schedule      | OPEN    |
| Complete fastener schedule    | OPEN    |

No material has been assigned to a component solely from an assumption.

---

# 19. CAD File Recovery Status

The mechanical baseline currently includes multiple CAD/reference formats and supporting information.

Expected authoritative CAD package:

* `.SLDASM`
* `.SLDPRT`
* `.SLDDRW`
* STEP
* STL
* drawings/PDF
* renders/screenshots where useful.

Some STEP files supplied earlier opened correctly while some STEP AP214/AP242 files produced SolidWorks import issues such as:

> "File does not contain any geometry data"

and in some cases imported as graphics/reference data rather than usable solid geometry.

Therefore:

**CAD compatibility/import status must be recorded per file.**

A file that cannot be opened as usable solid geometry is not treated as a verified editable manufacturing source.

---

# 20. CAD Revision Baseline

The final canonical CAD revision has not yet been completely recovered.

Current revision status:

| Item                                 | Status          |
| ------------------------------------ | --------------- |
| Canonical humanoid assembly revision | TBD             |
| Canonical torso revision             | Partial         |
| Canonical limb revisions             | Partial         |
| Canonical joint revisions            | Partial         |
| Canonical actuator mount revisions   | Partial         |
| Final STL revision mapping           | TBD             |
| Drawing revision mapping             | TBD             |
| Full Pack-and-Go assembly            | Required / OPEN |

All submitted CAD files shall retain their original filenames/revisions wherever possible.

No `final_final`, `new_final`, or duplicate unnamed revision shall be treated as authoritative.

---

# 21. Mass and Centre-of-Mass Baseline

Available individual CAD mass values include:

* Torso Proto K: 595.43 g
* Torso Proto D: 1204.17 g
* Torso Proto B: 12342.28 g — requires verification
* Thigh: 7464.06 g — requires verification
* Leg G: 14925.45 g — requires verification
* Hip motor: 681.30 g
* MG996R bracket: 21.22 g

The proposed actuator architecture alone is approximately:

**11.90 kg**

However, this does **not** represent the final robot mass.

A valid final mass model requires:

* complete assembly;
* verified material density;
* all mechanical parts;
* actuators;
* battery;
* electronics;
* sensors;
* fasteners;
* cables;
* feet and end-effectors.

### Current status

**Final robot mass: UNKNOWN**

**Final CoM: UNKNOWN**

No final CoM or stability claim is made from the current incomplete dataset.

---

# 22. Mechanical Interface Baseline

The following interfaces have been identified as critical:

| Interface                         | Current Status     |
| --------------------------------- | ------------------ |
| Actuator ↔ structural joint       | PARTIAL            |
| Shoulder actuator ↔ arm structure | PROPOSED           |
| Hip actuator ↔ torso/leg          | PARTIAL / PROPOSED |
| Knee actuator ↔ thigh/leg         | PROPOSED           |
| Ankle actuator ↔ foot/leg         | PROPOSED           |
| Neck actuator ↔ head/torso        | PROPOSED           |
| Elbow actuator ↔ arm              | PROPOSED           |
| Finger actuator ↔ hand frame/horn | PROPOSED           |
| Battery ↔ torso                   | TBD                |
| PDB ↔ torso                       | PROPOSED           |
| Electronics ↔ mounting plate      | PROPOSED           |
| Sensor ↔ structural body          | PARTIAL            |
| Cable ↔ rotating joint            | OPEN               |
| Foot ↔ ground/support surface     | PARTIAL            |

Final interface records require:

* Interface ID
* interface name
* CAD reference
* revision
* owner
* approver
* date
* constraints
* evidence
* status.

---

# 23. BOM / R&D Baseline

The earlier BOM/R&D work provides the basis for separating the humanoid into:

### Mechanical

* torso structures;
* limb structures;
* joint housings;
* brackets;
* feet;
* actuator mounts;
* fasteners;
* cable-management hardware.

### Actuation

* XM430 reference;
* proposed AK60-39;
* proposed AK45-36;
* proposed XL330.

### Electronics

* STM32G431-class controller;
* CAN transceiver/interface;
* MPU6050;
* power distribution;
* DC-DC conversion;
* protection and isolation;
* current/voltage sensing.

### Power

* 48 V-class battery proposal;
* 24 V rail;
* 5 V servo rail;
* 3.3 V logic rail.

The complete BOM/BOQ remains a separate controlled deliverable and shall not be reconstructed from assumptions.

---

# 24. Manufacturing Readiness Classification

Each component is to be classified into one of the following categories:

* `ALREADY AVAILABLE`
* `PRINTABLE`
* `PURCHASABLE`
* `MACHINE REQUIRED`
* `SPECIFICATION MISSING`
* `CAD MISSING`
* `VENDOR MISSING`
* `BLOCKED`

Current high-level status:

| Category              | Current Baseline                                           |
| --------------------- | ---------------------------------------------------------- |
| Already Available     | Some reference/CAD/parts information                       |
| Printable             | Partial; complete manifest required                        |
| Purchasable           | Actuator/electronics candidates identified                 |
| Machine Required      | Structural parts require final drawings/process definition |
| Specification Missing | Multiple interfaces and electrical ratings                 |
| CAD Missing           | Several complete subsystem/final assembly files            |
| Vendor Missing        | Final battery and several electronics/power components     |
| Blocked               | Complete physical prototype reproduction                   |

---

# 25. Physical Prototype Status

The baseline does **not** claim that the complete humanoid has been physically fabricated or assembled.

Current physical evidence available to the mechanical owner is incomplete.

Therefore:

| Physical Activity             | Status       |
| ----------------------------- | ------------ |
| Complete humanoid fabrication | NOT VERIFIED |
| Complete assembly             | NOT VERIFIED |
| Joint-by-joint fit check      | NOT VERIFIED |
| Full cable routing check      | NOT VERIFIED |
| Static load test              | NOT VERIFIED |
| ROM test                      | NOT VERIFIED |
| Backlash measurement          | NOT VERIFIED |
| Deflection measurement        | NOT VERIFIED |
| Final mass measurement        | NOT VERIFIED |
| Final CoM measurement         | NOT VERIFIED |
| Physical qualification        | NOT VERIFIED |

This distinction is intentional so that the baseline remains evidence-backed.

---

# 26. Known Engineering Risks

## R-001 — Canonical 17-DOF joint map not fully recovered

**Condition:** Product is defined as 17 DOF, but complete joint-by-joint authoritative allocation has not been recovered.

**Risk:** Incorrect actuator or mechanical interface assignment.

**Action:** Recover authoritative architecture/CAD and freeze joint map.

**Status:** OPEN.

---

## R-002 — Proposed actuator architecture not yet mapped to canonical DOF

**Condition:** Siddhesh's latest release proposes 30 actuator units, while the product architecture is 17 DOF.

**Risk:** Treating a proposed integration quantity as the canonical architecture.

**Action:** Create joint-by-joint actuator mapping after architecture confirmation and torque/CoM analysis.

**Status:** OPEN.

---

## R-003 — Incomplete CAD package

**Condition:** Not all humanoid subsystem CAD has been received/recovered.

**Risk:** Manufacturing package cannot yet guarantee complete reproducibility.

**Action:** Collect authoritative native CAD/Pack-and-Go assembly and all referenced parts.

**Status:** BLOCKED / OPEN.

---

## R-004 — CAD import incompatibility

**Condition:** Some STEP files do not import into SolidWorks as usable geometry.

**Risk:** Manufacturing or modification may be based on incomplete/graphics-only data.

**Action:** Obtain valid native SolidWorks, Parasolid or confirmed solid STEP representation.

**Status:** OPEN.

---

## R-005 — Inconsistent mass values

**Condition:** Some supplied CAD masses are unusually high relative to other components.

**Risk:** Incorrect torque and CoM calculations.

**Action:** Verify material assignment, units, configuration and source CAD.

**Status:** OPEN.

---

## R-006 — Battery not frozen

**Condition:** Battery dimensions, mass, BMS capability and current rating are not final.

**Risk:** Packaging and mass-distribution changes.

**Action:** Freeze after validated power/current calculation.

**Status:** OPEN.

---

## R-007 — Physical fabrication evidence incomplete

**Condition:** Complete physical prototype evidence has not been recovered.

**Risk:** Cannot claim manufacturing or qualification completion.

**Action:** Record actual fabrication/assembly evidence when available.

**Status:** OPEN.

---

# 27. Baseline Evidence Classification

The recovered information is classified as follows.

### VERIFIED

* BHIV humanoid programme is defined as 17 DOF.
* Arya owns mechanical realisation/manufacturing baseline work.
* Available CAD/reference dimensions listed in this document.
* Siddhesh supplied a mechanical/electronics integration release.
* Proposed actuator specifications and planning envelopes are available from that release.

### REFERENCE

* Overall 1639.63 × 546.94 × 260 mm CAD envelope.
* Earlier XM430 actuator reference.
* Individual torso/thigh/leg/motor dimensions and masses where revision is not fully established.

### PROPOSED

* AK60-39 actuator architecture.
* AK45-36 actuator architecture.
* XL330 finger actuator architecture.
* 48 V battery architecture.
* Electronics packaging zones.
* Power-conversion architecture.
* Cable routing requirements.

### TBD / UNKNOWN

* Canonical joint-by-joint 17-DOF allocation.
* Final actuator-to-joint mapping.
* Final CAD revision.
* Final robot mass.
* Final CoM.
* Final battery.
* Final electronics carrier.
* Complete manufacturing process.
* Complete BOM/BOQ.
* Final mechanical qualification.

### NOT VERIFIED

* Complete physical fabrication.
* Complete physical assembly.
* Static stability.
* ROM.
* Backlash.
* Deflection.
* Load testing.
* Final dimensional qualification.

---

# 28. Baseline Blockers

The major blockers remaining after current baseline recovery are:

1. Complete canonical humanoid CAD assembly.
2. Authoritative joint-by-joint 17-DOF map.
3. Final CAD revision identifiers.
4. Complete mechanical part manifest.
5. Complete actuator-to-joint mapping.
6. Verified material assignments.
7. Complete manufacturing drawings.
8. Final battery selection.
9. Final electronics mounting dimensions.
10. Physical prototype access/evidence.
11. Measured complete-robot mass.
12. Measured CoM.
13. Physical fit/interference validation.
14. Mechanical qualification measurements.

---

# 29. Baseline Acceptance State

The baseline is considered **PARTIALLY RECOVERED**.

The current package provides enough evidence to:

* understand the major humanoid mechanical subsystems;
* identify available mechanical CAD references;
* identify known dimensions and masses;
* understand the proposed actuator/mechanical integration direction;
* establish preliminary mechanical packaging zones;
* identify manufacturing and procurement gaps;
* create the next controlled manufacturing package.

The current evidence does **not** support claiming:

* complete canonical 17-DOF joint mapping;
* complete CAD closure;
* complete manufacturing readiness;
* complete physical fabrication;
* complete assembly;
* final robot mass;
* final CoM;
* mechanical qualification completion.

---

# 30. Handover / Reproducibility Requirement

A new engineer receiving this baseline must be able to distinguish:

**Existing verified evidence → reference information → proposed integration → unresolved information.**

The final repository should therefore contain, wherever available:

```text
/humanoid/
├── baseline/
│   ├── HUMANOID-BASELINE-001.md
│   ├── 17-DOF_MAP.md
│   ├── AS_DESIGNED_AS_BUILT_MATRIX.md
│   └── KNOWN_UNKNOWNS.md
│
├── cad/
│   ├── native/
│   ├── step/
│   ├── stl/
│   ├── drawings/
│   └── renders/
│
├── manufacturing/
├── bom/
├── boq/
├── procurement/
├── assembly/
├── qualification/
├── risk/
├── evidence/
└── review_packets/
```

Every CAD asset submitted with the final task should be traceable to:

**Part ID → CAD file → revision → source/evidence → manufacturing status**

where that information is available.

---

# 31. Final Baseline Statement

This baseline establishes the **current evidence-backed mechanical state of the BHIV 17-DOF Humanoid Robot** based on the CAD, BOM/R&D, mechanical references and electronics/mechanical integration information recovered so far.

The baseline intentionally does not convert incomplete information into false certainty.

In particular:

* the robot remains a **17-DOF programme**;
* the exact canonical joint allocation remains an evidence-recovery item;
* Siddhesh's AK60/AK45/XL330 architecture is recorded as a **proposed mechanical integration release**, not silently declared the canonical 17-DOF architecture;
* supplied CAD dimensions and masses are preserved with their verification status;
* incomplete CAD and unavailable physical parts are explicitly recorded;
* final mass, CoM, manufacturing completion and qualification are not claimed without measurements;
* all future mechanical changes must remain traceable to evidence or formal architecture approval.

**Baseline Status: PARTIALLY RECOVERED / EVIDENCE-BACKED / OPEN ITEMS IDENTIFIED**

**Owner:** Arya Barge
**Task:** ARYA-HUMANOID-001
**Baseline:** HUMANOID-BASELINE-001


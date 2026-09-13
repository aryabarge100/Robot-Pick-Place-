# MECHANICAL-INTERFACE-MAP.md

**Programme:** BHIV 17-DOF Humanoid Mechanical Realisation, Manufacturing Package & Physical Prototype Programme
**Task ID:** `ARYA-HUMANOID-001`
**Owner:** Arya Barge — Mechanical Realisation & Manufacturing Owner
**Status:** CONDITIONAL / OPEN INTERFACES
**Purpose:** Revision-controlled map of mechanical interfaces between structural parts, actuators, hand mechanisms, electronics mounting zones and service interfaces.

---

## 1. Purpose

This document defines the known mechanical interfaces required to convert the recovered humanoid design into a manufacturable and integrable package.

It separates:

* verified dimensional evidence,
* proposed actuator interfaces,
* interfaces requiring native CAD/drawing confirmation,
* interfaces dependent on final architecture,
* interfaces not yet physically verified.

**No interface is considered manufacturing-final unless its mating geometry, hole pattern, fasteners, clearance and revision are verified.**

---

# 2. Interface Status Legend

| Status            | Meaning                                                                 |
| ----------------- | ----------------------------------------------------------------------- |
| `VERIFIED`        | Supported by available drawing/dimension evidence                       |
| `PARTIAL`         | Some dimensions/features are known, but mating definition is incomplete |
| `CAD VERIFY`      | Native CAD/drawing inspection required                                  |
| `SPEC MISSING`    | Required specification is not available                                 |
| `PHYSICAL VERIFY` | Physical part/interface must be inspected                               |
| `TBD`             | Architecture or interface has not yet been formally defined             |
| `BLOCKED`         | Cannot be released without missing information/approval                 |

---

# 3. System-Level Mechanical Interface Map

| Interface ID | From                | To                         | Interface Type                 | Current Status | Required Closure                    |
| ------------ | ------------------- | -------------------------- | ------------------------------ | -------------- | ----------------------------------- |
| MI-001       | Torso               | Shoulder actuator/yoke     | Structural + actuator mount    | CAD VERIFY     | Final shoulder interface drawing    |
| MI-002       | Shoulder actuator   | Upper arm structure        | Circular actuator mount        | CAD VERIFY     | Hole centres + fasteners            |
| MI-003       | Torso/hip structure | Hip actuator               | Structural + actuator mount    | CAD VERIFY     | Final hip mounting pattern          |
| MI-004       | Hip actuator        | Thigh                      | Actuator-to-link               | CAD VERIFY     | Final mating CAD                    |
| MI-005       | Thigh               | Knee actuator              | Structural + actuator mount    | TBD            | Joint-axis and mounting definition  |
| MI-006       | Knee actuator       | Lower leg                  | Actuator-to-link               | TBD            | Final CAD/interface                 |
| MI-007       | Lower leg           | Ankle actuator             | Structural + actuator mount    | TBD            | Joint-axis/interface definition     |
| MI-008       | Ankle actuator      | Foot                       | Actuator-to-foot               | TBD            | Foot CAD + mounting pattern         |
| MI-009       | Torso               | Neck actuator              | Structural + actuator mount    | CAD VERIFY     | Final neck interface                |
| MI-010       | Neck actuator       | Head                       | Actuator-to-head               | TBD            | Head mating CAD                     |
| MI-011       | Shoulder actuator   | Elbow/upper-limb structure | Mechanical transmission        | TBD            | Final limb architecture             |
| MI-012       | Elbow actuator      | Forearm                    | Actuator-to-link               | CAD VERIFY     | AK45 interface verification         |
| MI-013       | Forearm             | Hand/wrist                 | Structural                     | TBD            | Wrist architecture                  |
| MI-014       | Hand base           | Finger actuators           | Servo mounting                 | CAD VERIFY     | XL330 frame/horn geometry           |
| MI-015       | Finger actuator     | Finger linkage             | Horn/link interface            | CAD VERIFY     | Exact horn/link geometry            |
| MI-016       | Torso               | Battery                    | Mechanical enclosure/retention | TBD            | Battery dimensions + retention      |
| MI-017       | Torso               | PDB/DC-DC                  | Electronics mounting           | TBD            | Final component CAD                 |
| MI-018       | Torso               | STM32/CAN/IMU              | Electronics mounting           | TBD            | Carrier-board dimensions            |
| MI-019       | Torso               | Cable routing              | Service interface              | TBD            | Harness channels + bend radius      |
| MI-020       | Structural shell    | Removable covers           | Fastened service interface     | PARTIAL        | Final fastener/clearance definition |

---

# 4. Actuator Interface Map

## 4.1 Proposed Actuator Allocation

The current mechanical-integration release proposes:

| Actuator                   | Quantity | Intended Locations     | Envelope        |
| -------------------------- | -------: | ---------------------- | --------------- |
| CubeMars AK60-39 V3.0 KV80 |       12 | Shoulders, hips, knees | Ø79 × 67 mm     |
| CubeMars AK45-36 KV80      |        8 | Neck, elbows, ankles   | Ø55 × 54 mm     |
| ROBOTIS XL330-M288-T       |       10 | Fingers                | 20 × 34 × 26 mm |
| **Total**                  |   **30** | —                      | —               |

**Important:** 30 actuators does **not** mean 30 DOF. The programme-level humanoid architecture remains a **17-DOF programme**, while the exact joint-by-joint DOF allocation requires authoritative architecture closure.

---

# 5. AK60-39 Mechanical Interface

### Intended locations

* Shoulder: 4
* Hip: 6
* Knee: 2

### Known envelope

* Diameter: approximately 79 mm
* Length: approximately 67 mm
* Mass: approximately 750 g

### Known mounting features

| Feature                         | Current Evidence                      |
| ------------------------------- | ------------------------------------- |
| Main circular interface         | Present                               |
| 8 × M3 × 6 mounting screws      | Reported in actuator release          |
| Mounting circle                 | Ø68 mm                                |
| Additional M4/diameter features | Present on reference drawing          |
| Exact hole centres              | **CAD/drawing verification required** |
| Final fastener engagement       | **Verification required**             |

### Mechanical requirements

1. Verify the official actuator drawing against the humanoid mating CAD.
2. Confirm concentricity between actuator axis and joint axis.
3. Confirm screw access after assembly.
4. Confirm minimum material thickness around mounting holes.
5. Confirm cable exit direction.
6. Confirm rotating-interface clearance.
7. Confirm service-loop space.
8. Freeze interface only after revision-controlled review.

**Status:** `CAD VERIFY`

---

# 6. AK45-36 Mechanical Interface

### Intended locations

* Neck: 2
* Elbow: 2
* Ankle: 4

### Known envelope

* Diameter: approximately 55 mm
* Length: approximately 54 mm
* Mass: approximately 340 g

### Known mounting features

| Feature                 | Current Evidence                      |
| ----------------------- | ------------------------------------- |
| Main mounting interface | Circular                              |
| 5 × M3 × 5              | Reported                              |
| Mounting circle         | Ø48 mm                                |
| Additional M3 features  | Reported                              |
| Exact hole centres      | **CAD/drawing verification required** |
| Final engagement        | **Verification required**             |

### Integration requirements

* Joint axis must be coincident with actuator axis.
* Cable exit must remain outside the rotating/pinch region.
* Service loop and bend radius must be reserved.
* Mounting plate thickness must support the specified engagement.
* Final elbow/ankle/neck brackets require mating CAD.

**Status:** `CAD VERIFY`

---

# 7. XL330 Finger Interface

### Intended use

* 5 actuators per hand
* 10 actuators total

### Known envelope

**20 × 34 × 26 mm**

### Interface

| Feature                    | Status                        |
| -------------------------- | ----------------------------- |
| Servo frame                | Known                         |
| Servo horn                 | Known                         |
| Frame screws               | M2 × 8 reference              |
| Horn screws                | M2 × 6 reference              |
| Connector                  | 3-pin JST/EH-family interface |
| Exact mounting coordinates | CAD VERIFY                    |
| Finger linkage geometry    | CAD VERIFY                    |
| Final hand load capability | NOT VALIDATED                 |

The XL330 mounting must be checked against:

* hand-base geometry,
* finger-part geometry,
* horn rotation,
* linkage travel,
* mechanical stop,
* cable clearance.

**Status:** `CAD VERIFY`

---

# 8. Torso Interfaces

## 8.1 Torso Proto K

Available dimensional evidence:

* External envelope: **210.23 × 150.53 × 38.86 mm**
* Internal cavity: approximately **127.32 × 86.13 mm**
* Mounting row: approximately 8 × Ø3 mm features
* Central bore: Ø40 mm true R20
* Wall thickness: approximately 5.0–6.1 mm
* Side-wall taper: approximately 5.45°
* Two-piece lid/shell arrangement with mating lip
* Mass: **595.43 g**

Source evidence confirms these dimensions/features but does not establish the complete mating architecture.

**Status:** `PARTIAL`

### Required closure

* exact mounting-hole coordinates,
* mating component identification,
* bore purpose and axis,
* final shell/lid fastener specification,
* electronics mounting interfaces.

---

## 8.2 Torso Proto D

Available evidence:

* External envelope: **210.23 × 150.53 × 90 mm**
* Top opening: approximately **148.10 × 103.43 mm**
* approximately 8 × Ø3 mm mounting features
* Ø40 mm true-R20 bore shown
* Wall approximately 3.09 mm
* Mass: **1204.17 g**

The available documentation explicitly states that the bore interpretation requires CAD confirmation: it may represent a single through-shaft axis shown in two views or two orthogonal bores.

**Status:** `CAD VERIFY`

---

## 8.3 Torso Proto B / Shoulder-Yoke Structure

Available evidence:

* External envelope: **424.96 × 331.28 × 140 mm**
* Two Ø80 mm true-R40 bearing bores
* Base mounting pattern visible
* Base-hole diameter not called out
* Mass: **12342.28 g**

The source also identifies a naming/title-block mismatch that must be resolved against the actual CAD/revision.

**Status:** `BLOCKED — NAMING/CAD CONFIRMATION`

---

# 9. Thigh Interface

Reference evidence:

* Thigh 3 envelope approximately **420–421.04 × 100 × 84.96 mm**
* tapered structural profile
* cross-section approximately 89.70 → 53.05 mm
* approximately 42.84° angled facet
* listed mass: **7464.06 g**

Required interfaces:

* hip actuator mounting,
* knee actuator mounting,
* structural fasteners,
* cable passage,
* neighbouring-link clearance.

**Status:** `CAD VERIFY`

No final hole pattern should be released from the available dimensional table alone.

---

# 10. Leg Interface

Reference evidence:

* Leg Proto Others G: **529.03 × 321.60 × 200 mm**
* multiple visible mounting features
* servo-horn mounting cluster visible
* hole sizes/counts not toleranced on available sheet
* listed mass: **14925.45 g**

**Status:** `SPEC/CAD VERIFY`

The servo-horn cluster must not be converted into a manufacturing drawing until the native CAD and hole specifications are confirmed.

---

# 11. MG996R Bracket Interface

Known evidence:

* External: **63.30 × 40 × 24 mm**
* Inner slot: approximately **57.30 × 20 mm**
* 4 × Ø4 mm corner mounting holes
* wall thickness: approximately 3 mm
* mass: **21.22 g**

**Status:** `PARTIAL / VERIFY MATING PART`

Required:

* mounting-hole pitch,
* servo placement,
* mating plate thickness,
* screw length,
* horn alignment,
* servo rotation clearance.

---

# 12. Step Motor Interface

Known evidence:

* Body approximately **30.89 × 30.89 × 18 mm**
* Ø5 mm shaft
* Ø9.14 mm boss
* Ø4.20 mm mounting-tab hole
* mass: **13.04 g**

**Status:** `PARTIAL`

Required:

* shaft coupling,
* axial retention,
* mounting-tab pitch,
* driven mechanism,
* motor orientation.

---

# 13. Hand Mechanical Interfaces

Available reference components include:

| Component       |                  Envelope |
| --------------- | ------------------------: |
| Finger tip      |        45.85 × 20 × 20 mm |
| Finger part 1   |      59 × 22.42 × 20.5 mm |
| Finger part 5   |  65.42 × 24.86 × 19.84 mm |
| Wrist bone      |           55 × 10 × 10 mm |
| Hand step motor |     31.39 × 29.87 × 29 mm |
| Hand base       | 172.8 × 147.16 × 47.84 mm |
| Base of hand    |         150 × 150 × 50 mm |

**Status:** `PARTIAL`

The complete finger joint/linkage interface requires native assembly CAD.

---

# 14. Electronics-to-Mechanical Interfaces

| Electronics             | Mechanical Zone       | Interface Requirement                  | Status |
| ----------------------- | --------------------- | -------------------------------------- | ------ |
| STM32 controller        | Upper/central torso   | Standoff mounting                      | TBD    |
| CAN interface           | Adjacent STM32        | PCB/enclosure mounting                 | TBD    |
| PDB                     | Lower/central torso   | Secure mounting + service access       | TBD    |
| 48→24 V DC-DC           | Power bay             | Mounting + thermal clearance           | TBD    |
| 48→5 V DC-DC            | Torso/hand power bay  | Mounting + cable access                | TBD    |
| IMU                     | Central torso         | Rigid mounting + orientation reference | TBD    |
| Fuse/holder             | Near battery positive | Accessible service mounting            | TBD    |
| Isolation/contactor     | Battery/PDB           | Secure mounting                        | TBD    |
| E-stop                  | Accessible torso      | External mechanical actuation          | TBD    |
| Current/voltage sensing | PDB                   | Protected mounting                     | TBD    |

These interfaces remain dependent on final component SKUs/carrier dimensions where those are not yet frozen.

---

# 15. Battery Interface

Preferred architecture is a 48 V-class battery.

Mechanical interface must define:

* battery envelope,
* retention method,
* mounting holes/straps,
* insertion/removal path,
* connector access,
* fuse/isolation access,
* cable strain relief,
* centre-of-mass location,
* clearance from moving joints.

The battery should **not** receive a final mounting pattern until the selected physical battery pack is confirmed.

**Status:** `BLOCKED — BATTERY SELECTION`

---

# 16. Cable Routing Interfaces

Every actuator interface shall reserve:

1. connector access,
2. minimum bend radius,
3. service loop,
4. strain relief,
5. protection against rotating joints,
6. protection against pinch points,
7. removable-panel access.

### Critical rule

**No cable shall cross a rotating actuator interface unless the routing has been explicitly engineered and verified.**

---

# 17. Interface Freeze Requirements

An interface becomes `FROZEN` only when all are available:

* mating CAD,
* interface revision,
* hole coordinates,
* hole diameter/tolerance,
* fastener specification,
* engagement depth,
* datum definition,
* clearance,
* cable routing,
* assembly access,
* service access,
* physical verification where applicable.

---

# 18. Open Interface Register

| ID     | Open Item                          | Impact                |
| ------ | ---------------------------------- | --------------------- |
| OI-001 | Exact 17-DOF joint allocation      | Architecture          |
| OI-002 | Native torso CAD revisions         | Manufacturing         |
| OI-003 | AK60 exact hole centres            | Actuator brackets     |
| OI-004 | AK45 exact hole centres            | Actuator brackets     |
| OI-005 | XL330 exact frame/horn coordinates | Hand                  |
| OI-006 | Torso B naming/revision mismatch   | Baseline control      |
| OI-007 | Torso D bore interpretation        | Joint architecture    |
| OI-008 | Thigh mating interfaces            | Leg assembly          |
| OI-009 | Leg mounting-hole specifications   | Manufacturing         |
| OI-010 | Battery physical pack              | Torso packaging       |
| OI-011 | STM32 carrier PCB                  | Electronics mounting  |
| OI-012 | Final PDB/DC-DC physical SKUs      | Electronics packaging |
| OI-013 | Final hand linkage                 | Hand manufacturing    |
| OI-014 | Final foot CAD                     | Ankle interface       |
| OI-015 | Physical mating verification       | As-built closure      |

---

# 19. Interface-Control Rule

Any change to:

* actuator type,
* actuator axis,
* mounting pattern,
* joint location,
* structural thickness,
* battery location,
* electronics location,
* major cable path,
* mass distribution,

must be recorded as:

**Observed Condition → Evidence → Engineering Risk → Proposed Change → Authority Required**

No silent mechanical redesign is permitted.

---

# 20. Handover Evidence

The final mechanical interface package shall contain:

* interface-controlled STEP files,
* STL files where required,
* 2D manufacturing drawings,
* actuator interface drawings,
* exploded assemblies,
* fastener schedule,
* assembly orientation sheets,
* cable-routing drawings,
* revision identifiers,
* interface verification checklist,
* physical fit/clearance evidence.

---

## 21. Current Conclusion

The humanoid has a usable **partial mechanical interface baseline**, but the complete interface map is not yet manufacturing-frozen.

The strongest current evidence is for:

* Torso K,
* Torso D,
* Torso B/shoulder structure,
* Thigh 3,
* Leg Proto Others G,
* MG996R bracket,
* step motor,
* hand reference components.

The major remaining blockers are native CAD/revision confirmation, actuator mating-hole verification, final 17-DOF architecture, battery/electronics physical selection and physical mating verification.

**Mechanical Interface Status: CONDITIONAL — DO NOT RELEASE AS FINAL MANUFACTURING INTERFACE UNTIL OPEN ITEMS ARE CLOSED.**

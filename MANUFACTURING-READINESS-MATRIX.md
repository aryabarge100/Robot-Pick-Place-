# MANUFACTURING-READINESS-MATRIX.md

**Programme:** BHIV 17-DOF Humanoid Mechanical Realisation, Manufacturing Package & Physical Prototype Programme
**Task ID:** `ARYA-HUMANOID-001`
**Owner:** Arya Barge — Mechanical Realisation & Manufacturing Owner
**Related Package:** `HUMANOID-MFG-001.md` / Manufacturing Package Index
**Status:** CONDITIONAL / PROCUREMENT & FABRICATION READINESS OPEN

---

# 1. Purpose

This matrix classifies every currently identified mechanical/manufacturing item according to its readiness for procurement, fabrication or assembly.

### Classification

* `ALREADY AVAILABLE`
* `PRINTABLE`
* `PURCHASABLE`
* `MACHINE REQUIRED`
* `SPECIFICATION MISSING`
* `CAD MISSING`
* `VENDOR MISSING`
* `BLOCKED`

**Rule:** An item is not considered manufacturing-ready merely because a dimension or image exists.

---

# 2. Readiness Summary

| Class                 | Meaning                                                                        |
| --------------------- | ------------------------------------------------------------------------------ |
| ALREADY AVAILABLE     | Existing physical item or confirmed inventory evidence                         |
| PRINTABLE             | Geometry can be released for additive manufacturing after CAD/revision closure |
| PURCHASABLE           | Standard commercial item with sufficiently defined specification               |
| MACHINE REQUIRED      | Requires machining/fabrication from controlled drawing/material                |
| SPECIFICATION MISSING | Geometry exists but manufacturing specification is incomplete                  |
| CAD MISSING           | Native/manufacturing CAD is not available                                      |
| VENDOR MISSING        | Supplier/source must still be identified                                       |
| BLOCKED               | Cannot proceed without architecture/approval/evidence                          |

---

# 3. Structural Manufacturing Matrix

| ID      | Part                       | Current Evidence                | Classification               | Readiness | Required Before Release                    |
| ------- | -------------------------- | ------------------------------- | ---------------------------- | --------- | ------------------------------------------ |
| MFG-001 | Torso Proto K              | Dimensioned drawing evidence    | PRINTABLE / MACHINE REQUIRED | PARTIAL   | Native CAD + material + tolerances         |
| MFG-002 | Torso Proto D              | Dimensioned drawing evidence    | PRINTABLE / MACHINE REQUIRED | PARTIAL   | CAD + bore interpretation + material       |
| MFG-003 | Torso Proto B              | Dimensioned structural evidence | MACHINE REQUIRED             | BLOCKED   | Naming/revision + CAD + hole pattern       |
| MFG-004 | Thigh 3                    | Dimension/envelope evidence     | PRINTABLE / MACHINE REQUIRED | PARTIAL   | Native CAD + mounting interfaces           |
| MFG-005 | Leg Proto Others G         | Envelope + visible features     | MACHINE REQUIRED             | BLOCKED   | Hole dimensions + CAD                      |
| MFG-006 | MG996R bracket             | Dimensioned drawing evidence    | PRINTABLE / PURCHASABLE      | PARTIAL   | Confirm material/process + mating geometry |
| MFG-007 | Step motor mount/interface | Partial dimensional evidence    | MACHINE REQUIRED             | PARTIAL   | Final mating geometry                      |
| MFG-008 | Hand base                  | Reference dimensions            | PRINTABLE                    | BLOCKED   | Native CAD + final hand architecture       |
| MFG-009 | Finger tip                 | Reference dimensions            | PRINTABLE                    | BLOCKED   | Native CAD + hand revision                 |
| MFG-010 | Finger part 1              | Reference dimensions            | PRINTABLE                    | BLOCKED   | Native CAD + linkage interface             |
| MFG-011 | Finger part 5              | Reference dimensions            | PRINTABLE                    | BLOCKED   | Native CAD + linkage interface             |
| MFG-012 | Wrist bone                 | Reference dimensions            | PRINTABLE                    | BLOCKED   | Native CAD + wrist architecture            |
| MFG-013 | Base of hand               | Dimension/mass reference        | PRINTABLE                    | BLOCKED   | Native CAD + structural validation         |
| MFG-014 | Humanoid shell D/iCub      | Reference-only table            | CAD MISSING                  | BLOCKED   | Native CAD + revision                      |
| MFG-015 | TeslaBot torso references  | Reference-only table            | CAD MISSING                  | BLOCKED   | Confirm whether applicable to final design |

## The drawing evidence provides complete/stronger dimensional coverage for Torso K, Torso D, Torso B, Thigh 3, Leg Proto Others G, MG996R bracket and step motor, while several other structural items are reference-table-only.

# 4. Actuator Procurement Matrix

| ID      | Item                       |     Qty | Classification | Current Status              | Closure                         |
| ------- | -------------------------- | ------: | -------------- | --------------------------- | ------------------------------- |
| ACT-001 | CubeMars AK60-39 V3.0 KV80 |      12 | PURCHASABLE    | Proposed architecture       | Procurement/vendor confirmation |
| ACT-002 | CubeMars AK45-36 KV80      |       8 | PURCHASABLE    | Proposed architecture       | Procurement/vendor confirmation |
| ACT-003 | ROBOTIS XL330-M288-T       |      10 | PURCHASABLE    | Proposed architecture       | Procurement/vendor confirmation |
| ACT-004 | AK60 mounting hardware     | 12 sets | PURCHASABLE    | Interface known partially   | Final fastener verification     |
| ACT-005 | AK45 mounting hardware     |  8 sets | PURCHASABLE    | Interface known partially   | Final fastener verification     |
| ACT-006 | XL330 mounting hardware    | 10 sets | PURCHASABLE    | Reference screws identified | Verify actual supplied hardware |

### Actuator package

| Actuator | Envelope        |   Mass | Mechanical Readiness |
| -------- | --------------- | -----: | -------------------- |
| AK60-39  | Ø79 × 67 mm     | ~750 g | CAD VERIFY           |
| AK45-36  | Ø55 × 54 mm     | ~340 g | CAD VERIFY           |
| XL330    | 20 × 34 × 26 mm |  ~18 g | CAD VERIFY           |

**Important:** actuator selection is proposed for mechanical integration. Final torque/CoM validation and final mounting geometry remain required before manufacturing release.

---

# 5. Electronics Mechanical Packaging Matrix

| ID       | Component                  | Classification | Current Status              | Required Closure        |
| -------- | -------------------------- | -------------- | --------------------------- | ----------------------- |
| ELEC-001 | STM32 controller           | PURCHASABLE    | Planning envelope available | Final carrier/PCB       |
| ELEC-002 | CAN interface              | PURCHASABLE    | Planning envelope           | Final hardware          |
| ELEC-003 | PDB                        | PURCHASABLE    | Rating TBD                  | Electrical sizing       |
| ELEC-004 | 48→24 V DC-DC              | PURCHASABLE    | Rating TBD                  | Final SKU               |
| ELEC-005 | 48→5 V DC-DC               | PURCHASABLE    | High-current requirement    | Final SKU/rating        |
| ELEC-006 | 3.3 V regulator            | PURCHASABLE    | Planning item               | Final SKU               |
| ELEC-007 | MPU6050                    | PURCHASABLE    | Module SKU TBD              | Final module            |
| ELEC-008 | Fuse + holder              | PURCHASABLE    | Fuse rating TBD             | Current calculation     |
| ELEC-009 | Isolation switch/contactor | PURCHASABLE    | Specification TBD           | Final rating            |
| ELEC-010 | E-stop                     | PURCHASABLE    | Mechanical interface TBD    | Final switch            |
| ELEC-011 | Current sensor             | PURCHASABLE    | Quantity/rating TBD         | Final electrical sizing |
| ELEC-012 | Voltage sensing            | PURCHASABLE    | Specification TBD           | Final circuit           |
| ELEC-013 | Battery                    | PURCHASABLE    | Vendor/model not frozen     | Physical pack selection |

---

# 6. Battery Readiness

| Item                    | Status                      |
| ----------------------- | --------------------------- |
| 48 V-class architecture | PROPOSED                    |
| Energy target           | ~960–1064 Wh planning range |
| Physical battery pack   | NOT FROZEN                  |
| Battery dimensions      | NOT FROZEN                  |
| Battery mounting        | NOT FROZEN                  |
| Battery retention       | NOT FROZEN                  |
| Connector               | NOT FROZEN                  |
| Fuse rating             | NOT FROZEN                  |
| Main cable routing      | NOT FROZEN                  |
| Battery CoM             | NOT VERIFIED                |

**Classification:** `BLOCKED`

No final battery bracket should be manufactured before the physical battery model is selected and measured.

---

# 7. Hand Manufacturing Matrix

| ID       | Part              | Classification               | Status                          |
| -------- | ----------------- | ---------------------------- | ------------------------------- |
| HAND-001 | Finger tip        | PRINTABLE                    | CAD/revision required           |
| HAND-002 | Finger part 1     | PRINTABLE                    | CAD/revision required           |
| HAND-003 | Finger part 5     | PRINTABLE                    | CAD/revision required           |
| HAND-004 | Wrist bone        | PRINTABLE                    | CAD/revision required           |
| HAND-005 | Hand base         | PRINTABLE                    | CAD/revision required           |
| HAND-006 | Base of hand      | PRINTABLE / MACHINE REQUIRED | CAD/material required           |
| HAND-007 | XL330 actuator    | PURCHASABLE                  | Interface verification required |
| HAND-008 | M3 × 0.5 hex nuts | PURCHASABLE                  | Standard hardware               |
| HAND-009 | Hand gears        | PRINTABLE / PURCHASABLE      | Material/process TBD            |
| HAND-010 | Hand shafts       | MACHINE REQUIRED             | Drawing/material required       |

The available source identifies the hand components and their reference dimensions but does not establish a complete production-ready hand assembly drawing.

---

# 8. Fastener Matrix

| Category                          | Current Status                     |
| --------------------------------- | ---------------------------------- |
| M3 structural fasteners           | PURCHASABLE                        |
| M2 XL330 hardware                 | PURCHASABLE                        |
| M3 nuts                           | PURCHASABLE                        |
| Actuator-specific mounting screws | PURCHASABLE after interface freeze |
| Torso shell fasteners             | SPECIFICATION MISSING              |
| Battery mounting hardware         | SPECIFICATION MISSING              |
| Electronics standoffs             | SPECIFICATION MISSING              |
| Cable strain-relief hardware      | SPECIFICATION MISSING              |

---

# 9. Manufacturing Process Matrix

| Process                        | Parts                                          | Current Readiness          |
| ------------------------------ | ---------------------------------------------- | -------------------------- |
| FDM/3D printing                | Finger parts, brackets, shells where approved  | CAD REQUIRED               |
| Resin printing                 | Small/high-detail hand parts if selected       | CAD + material TBD         |
| CNC machining                  | Structural actuator brackets/links if metallic | Drawing/material required  |
| Laser cutting                  | Plates/brackets where applicable               | Drawing required           |
| Drilling/tapping               | Structural interfaces                          | Drawing/tolerance required |
| Press-fit/bearing installation | Torso/shoulder structures                      | Bore tolerance required    |
| Manual assembly                | Full humanoid                                  | Interface freeze required  |

---

# 10. Procurement Readiness

| Procurement Item       | Classification        | Current Status                    |
| ---------------------- | --------------------- | --------------------------------- |
| AK60 actuators         | PURCHASABLE           | Proposed                          |
| AK45 actuators         | PURCHASABLE           | Proposed                          |
| XL330 servos           | PURCHASABLE           | Proposed                          |
| Fasteners              | PURCHASABLE           | Partial                           |
| Bearings               | PURCHASABLE           | Specification required            |
| Battery                | VENDOR MISSING        | Vendor/model not frozen           |
| DC-DC converters       | SPECIFICATION MISSING | Rating required                   |
| PDB                    | SPECIFICATION MISSING | Rating required                   |
| Connectors             | SPECIFICATION MISSING | Final harness definition required |
| Structural material    | SPECIFICATION MISSING | Final material/process required   |
| PCB/enclosure hardware | SPECIFICATION MISSING | Final PCB required                |

---

# 11. Already Available / Physical Evidence

The following should only be marked `ALREADY AVAILABLE` when supported by actual inventory or physical evidence:

* existing structural components,
* existing motors/servos,
* existing fasteners,
* existing electronics,
* existing printed parts.

**Drawing evidence alone does not establish physical availability.**

## Current source documentation provides dimensions and masses, but that is not equivalent to proof that each corresponding physical component is present or manufactured. For example, the source records Torso K at 595.43 g, Torso D at 1204.17 g and Torso B at 12342.28 g, but these values remain design/reference evidence unless physically verified.

# 12. High-Risk Manufacturing Items

## MR-001 — Torso B

**Risk:** Very large reported mass and naming mismatch.

**Evidence:**

* 424.96 × 331.28 × 140 mm
* 12342.28 g
* two Ø80 mm bores
* drawing title block mismatch

**Action:** Confirm native CAD, revision and mass before actuator/structure release.

**Status:** `BLOCKED`

---

## MR-002 — Thigh

**Risk:** Reported mass of 7464.06 g is significant for a humanoid limb.

**Action:** Verify material, CAD mass properties and actual physical mass before final motor/CoM qualification.

**Status:** `SPECIFICATION/CAD VERIFY`

---

## MR-003 — Leg Proto Others G

**Risk:** Mounting-hole sizes/counts are not toleranced.

**Action:** Recover native CAD and define controlled hole pattern.

**Status:** `BLOCKED`

---

## MR-004 — Torso D Bore

**Risk:** Bore may represent one through-axis or two orthogonal bores.

**Action:** Confirm from native CAD.

**Status:** `CAD VERIFY`

---

## MR-005 — Hand Architecture

**Risk:** Individual component dimensions exist, but complete actuator/linkage interface is not frozen.

**Action:** Produce final hand assembly and exploded manufacturing package.

**Status:** `BLOCKED`

---

# 13. Manufacturing Release Gates

## Gate 1 — Baseline

Required:

* canonical CAD identified,
* revision recorded,
* 17-DOF architecture authority identified,
* as-designed/as-built distinction maintained.

**Status:** PARTIAL

---

## Gate 2 — Interface

Required:

* actuator interfaces frozen,
* joint axes frozen,
* mounting holes frozen,
* fasteners defined,
* clearances verified.

**Status:** OPEN

---

## Gate 3 — Manufacturing

Required:

* final STEP,
* STL where required,
* 2D drawings,
* material,
* tolerance,
* process,
* surface finish where required.

**Status:** OPEN

---

## Gate 4 — Procurement

Required:

* BOM,
* BOQ,
* supplier/vendor,
* quantity,
* specification,
* quotation evidence,
* procurement tracker.

**Status:** OPEN

---

## Gate 5 — Fabrication

Required:

* controlled manufacturing files,
* fabrication records,
* part identification,
* incoming inspection.

**Status:** NOT CLOSED

---

## Gate 6 — Assembly

Required:

* exploded assembly,
* fastener schedule,
* assembly sequence,
* torque/specification where applicable,
* physical fit evidence.

**Status:** NOT CLOSED

---

## Gate 7 — Qualification

Required:

* measured dimensions,
* joint movement,
* mechanical interference checks,
* load/stability tests where defined,
* failure log,
* change linkage.

**Status:** NOT CLOSED

---

# 14. Manufacturing Package Index

This matrix feeds:

`HUMANOID-MFG-001.md`

The final manufacturing package should contain:

```text
HUMANOID-MFG-001.md
│
├── 01_BASELINE/
│   ├── HUMANOID-BASELINE-001.md
│   ├── 17-DOF-MAP.md
│   ├── AS-DESIGNED-AS-BUILT-MATRIX.md
│   └── KNOWN-UNKNOWNS.md
│
├── 02_INTERFACES/
│   └── MECHANICAL-INTERFACE-MAP.md
│
├── 03_AUDIT/
│   └── HUMANOID-MECH-AUDIT-001.md
│
├── 04_CAD/
│   ├── STEP/
│   ├── STL/
│   ├── SOLIDWORKS/
│   └── REVISION-MANIFEST.md
│
├── 05_DRAWINGS/
│   ├── PART-DRAWINGS/
│   ├── ASSEMBLY-DRAWINGS/
│   └── ACTUATOR-INTERFACES/
│
├── 06_BOM_BOQ/
│   ├── BOM.md
│   ├── BOQ.md
│   └── PROCUREMENT-TRACKER.md
│
├── 07_MANUFACTURING/
│   ├── PRINTING/
│   ├── CNC/
│   ├── LASER/
│   └── FABRICATION-LOG.md
│
├── 08_ASSEMBLY/
│   ├── EXPLODED-VIEWS/
│   ├── ASSEMBLY-SEQUENCE.md
│   └── FASTENER-SCHEDULE.md
│
├── 09_QUALIFICATION/
│   ├── TEST-PLAN.md
│   ├── MEASUREMENTS/
│   └── FAILURE-LOG.md
│
└── 10_HANDOVER/
    ├── FINAL-REVISION-MANIFEST.md
    ├── AS-BUILT-RECORD.md
    └── HANDOVER-CHECKLIST.md
```

---

# 15. Current Readiness Summary

| Area                    | Status                                 |
| ----------------------- | -------------------------------------- |
| Baseline recovery       | PARTIAL                                |
| Structural dimensions   | PARTIAL / GOOD FOR IDENTIFIED DRAWINGS |
| Native CAD verification | OPEN                                   |
| 17-DOF joint map        | OPEN                                   |
| Actuator selection      | PROPOSED                               |
| Actuator interface      | CAD VERIFY                             |
| Hand architecture       | OPEN                                   |
| Electronics packaging   | OPEN                                   |
| Battery packaging       | BLOCKED                                |
| Manufacturing drawings  | OPEN                                   |
| Procurement package     | OPEN                                   |
| Fabrication             | NOT RELEASED                           |
| Assembly                | NOT CLOSED                             |
| Qualification           | NOT CLOSED                             |
| Handover                | NOT CLOSED                             |

---

# 16. Final Manufacturing Decision

**Current programme state: CONDITIONAL — MANUFACTURING PACKAGE NOT YET FULLY RELEASED.**

The project has sufficient information to continue **baseline recovery, CAD/interface verification, procurement preparation and manufacturing-package development**.

It is **not yet acceptable to claim**:

* all parts are manufactured,
* all parts are physically available,
* all interfaces are verified,
* assembly is complete,
* physical qualification is complete,
* final mass/CoM is validated,
* procurement is complete.

The next release gate is:

**Canonical CAD → Interface Freeze → Manufacturing Drawings → BOM/BOQ → Procurement → Fabrication → Physical Inspection → Assembly → Qualification → Handover.**

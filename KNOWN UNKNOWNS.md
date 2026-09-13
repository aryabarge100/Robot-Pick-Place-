# KNOWN-UNKNOWNS

## BHIV 17-DOF Humanoid — Missing Evidence, Specifications & Verification Register

**Task ID:** ARYA-HUMANOID-001
**Owner:** Arya Barge
**Status:** ACTIVE OPEN-ITEM REGISTER

---

# 1. Purpose

This document records information that is currently missing, ambiguous, unverified or physically unavailable for the BHIV humanoid mechanical realisation.

The purpose is to ensure that missing information is explicitly controlled rather than silently inferred.

---

# 2. Classification

| Category                  | Meaning                                                              |
| ------------------------- | -------------------------------------------------------------------- |
| MISSING CAD               | Required CAD model/assembly/drawing not available                    |
| MISSING PHYSICAL PART     | CAD/reference exists but physical part is not available to the owner |
| SPECIFICATION MISSING     | Required engineering specification not frozen                        |
| CAD VERIFICATION REQUIRED | Information exists but must be checked against CAD                   |
| NOT PHYSICALLY TESTED     | Physical validation has not been performed/evidenced                 |
| REVISION MISSING          | Exact CAD/design revision is unknown                                 |
| APPROVAL REQUIRED         | Architecture/interface decision requires authority confirmation      |
| REFERENCE ONLY            | Information exists but cannot be treated as canonical                |

---

# 3. DOF / Architecture Unknowns

| ID    | Unknown                                                        | Category                                  | Impact | Required Action                       | Status |
| ----- | -------------------------------------------------------------- | ----------------------------------------- | ------ | ------------------------------------- | ------ |
| U-001 | Authoritative joint-by-joint 17-DOF allocation                 | Specification Missing / Approval Required | High   | Recover canonical architecture        | OPEN   |
| U-002 | Exact actuator assigned to each DOF                            | Specification Missing                     | High   | Create approved actuator-to-joint map | OPEN   |
| U-003 | Final joint-axis orientations                                  | CAD Verification Required                 | High   | Verify complete assembly              | OPEN   |
| U-004 | Final joint ROM                                                | Specification Missing                     | High   | Measure/derive from validated CAD     | OPEN   |
| U-005 | Final joint torque requirements                                | Specification Missing                     | High   | Complete torque/CoM analysis          | OPEN   |
| U-006 | Whether proposed 30 actuator quantity is approved architecture | Approval Required                         | High   | Architecture review                   | OPEN   |

---

# 4. CAD Unknowns

| ID    | Unknown                                      | Category                  | Impact   | Required Action                           | Status |
| ----- | -------------------------------------------- | ------------------------- | -------- | ----------------------------------------- | ------ |
| U-007 | Complete canonical humanoid assembly         | Missing CAD               | Critical | Obtain authoritative assembly/Pack-and-Go | OPEN   |
| U-008 | Complete limb CAD                            | Missing CAD               | Critical | Recover left/right arm and leg assemblies | OPEN   |
| U-009 | Complete hand assembly CAD                   | Missing CAD               | High     | Recover final hand assembly               | OPEN   |
| U-010 | Final actuator mounting CAD                  | Missing CAD               | High     | Obtain/verify mounting interfaces         | OPEN   |
| U-011 | Final foot CAD                               | Missing CAD               | High     | Recover authoritative foot model          | OPEN   |
| U-012 | Exact CAD revisions                          | Revision Missing          | High     | Map files to controlled revisions         | OPEN   |
| U-013 | Some STEP files not usable as solid geometry | CAD Verification Required | Medium   | Obtain valid native/solid CAD             | OPEN   |

---

# 5. Specific CAD Ambiguities

## U-014 — Torso B Naming Mismatch

The supplied drawing information identifies a mismatch:

* drawing title block reads "torso K";
* dimensions correspond to "torso proto B".

This must be resolved using the actual CAD filename/revision and assembly reference.

**Status:** OPEN.

---

## U-015 — Torso D Bore Interpretation

The supplied drawing records a Ø40 true R20 bore and notes uncertainty regarding whether it represents:

* one through-shaft axis shown in two views; or
* two orthogonal bores.

CAD confirmation is required before manufacturing.

**Status:** OPEN.

---

## U-016 — Leg Proto Hole Details

The supplied sheet shows a servo-horn mounting cluster, but hole size/count are not toleranced on the available sheet.

**Required:** verify hole geometry directly from CAD.

**Status:** OPEN.

---

# 6. Mass / CoM Unknowns

| ID    | Unknown                               | Category                  | Impact   |
| ----- | ------------------------------------- | ------------------------- | -------- |
| U-017 | Final complete humanoid mass          | Specification Missing     | Critical |
| U-018 | Final CoM                             | Specification Missing     | Critical |
| U-019 | Verified mass of Torso B              | CAD Verification Required | High     |
| U-020 | Verified mass of Thigh                | CAD Verification Required | High     |
| U-021 | Verified mass of Leg Proto            | CAD Verification Required | High     |
| U-022 | Mass contribution of fasteners/cables | Specification Missing     | Medium   |
| U-023 | Battery mass                          | Specification Missing     | High     |
| U-024 | Electronics mass                      | Specification Missing     | Medium   |

## The source document explicitly provides the large Torso B and Leg Proto masses, but they should be confirmed before being used in final torque/CoM calculations.

# 7. Manufacturing Unknowns

| ID    | Unknown                            | Category              | Impact   |
| ----- | ---------------------------------- | --------------------- | -------- |
| U-025 | Complete mechanical part manifest  | Specification Missing | Critical |
| U-026 | Material for every structural part | Specification Missing | High     |
| U-027 | Manufacturing method per part      | Specification Missing | High     |
| U-028 | Final machining drawings           | Missing CAD           | Critical |
| U-029 | GD&T for critical interfaces       | Specification Missing | High     |
| U-030 | Printable-part STL package         | Missing CAD           | High     |
| U-031 | Print orientation                  | Specification Missing | Medium   |
| U-032 | Post-processing instructions       | Specification Missing | Medium   |
| U-033 | Heat-set insert specification      | Specification Missing | Medium   |
| U-034 | Final fastener schedule            | Specification Missing | High     |

---

# 8. Physical Hardware Unknowns

| ID    | Unknown                                              | Category              | Impact   |
| ----- | ---------------------------------------------------- | --------------------- | -------- |
| U-035 | Which listed CAD parts have actually been fabricated | Missing Physical Part | Critical |
| U-036 | Which fabricated parts are currently available       | Missing Physical Part | Critical |
| U-037 | Complete torso hardware availability                 | Missing Physical Part | High     |
| U-038 | Complete arm hardware availability                   | Missing Physical Part | High     |
| U-039 | Complete leg hardware availability                   | Missing Physical Part | High     |
| U-040 | Complete hand hardware availability                  | Missing Physical Part | High     |
| U-041 | Actuator physical availability                       | Missing Physical Part | Critical |
| U-042 | Battery physical availability                        | Missing Physical Part | High     |
| U-043 | Electronics physical availability                    | Missing Physical Part | High     |

---

# 9. Physical Verification Unknowns

The following are currently not physically verified:

* overall robot dimensions;
* joint fit;
* mounting-hole alignment;
* actuator mounting;
* interference;
* cable pinch points;
* serviceability;
* joint ROM;
* backlash;
* structural deflection;
* static load capacity;
* complete robot mass;
* centre of mass;
* support polygon;
* static stability;
* assembly time;
* maintenance procedure.

**Status:** NOT PHYSICALLY TESTED.

---

# 10. Electronics / Mechanical Integration Unknowns

| ID    | Unknown                                 | Category                  |
| ----- | --------------------------------------- | ------------------------- |
| U-044 | Final STM32 carrier-board dimensions    | Specification Missing     |
| U-045 | Final MPU6050 module/SKU                | Specification Missing     |
| U-046 | Final PDB dimensions/rating             | Specification Missing     |
| U-047 | Final 48→24 V converter                 | Specification Missing     |
| U-048 | Final 48→5 V converter                  | Specification Missing     |
| U-049 | Final fuse rating                       | Specification Missing     |
| U-050 | Final contactor/isolation device        | Specification Missing     |
| U-051 | Final battery vendor/model              | Specification Missing     |
| U-052 | Final connector ratings                 | Specification Missing     |
| U-053 | Final cable gauge                       | Specification Missing     |
| U-054 | Final electronics mounting-hole pattern | CAD Verification Required |

The electronics BOM itself identifies several of these as planning values rather than final manufacturing-certified dimensions and states that final actuator, power and interface details must be frozen before procurement/manufacturing release.

---

# 11. Procurement Unknowns

| ID    | Unknown                                     | Category                     |
| ----- | ------------------------------------------- | ---------------------------- |
| U-055 | Final supplier for body actuators           | Vendor Missing               |
| U-056 | Final supplier for hand actuators/mechanism | Vendor Missing               |
| U-057 | Final battery supplier                      | Vendor Missing               |
| U-058 | Final power-converter supplier              | Vendor Missing               |
| U-059 | Final connector supplier                    | Vendor Missing               |
| U-060 | Three comparable quotations                 | Procurement Evidence Missing |
| U-061 | Final landed cost                           | Procurement Evidence Missing |
| U-062 | Final lead time                             | Procurement Evidence Missing |

No supplier quote or purchase completion shall be claimed without actual evidence.

---

# 12. Hand Architecture Unknown

The supplied parts document contains a hand-part set including:

* finger tip;
* finger parts;
* wrist bone;
* step motor;
* shaft gear;
* rotor;
* gear;
* tray;
* hand base;
* DC motor;
* base of hand.

Several of these have recorded dimensions and masses.

However, the final relationship between this mechanical hand mechanism and the proposed XL330 actuator architecture is not established.

### Required

Confirm whether the final hand design uses:

1. the mechanical step-motor/gear arrangement; or
2. XL330-M288-T smart servos; or
3. another approved architecture.

**Status:** OPEN / ARCHITECTURE CONFIRMATION REQUIRED.

---

# 13. Safety / Power Unknowns

| ID    | Unknown                        | Impact   |
| ----- | ------------------------------ | -------- |
| U-063 | Validated peak current         | Critical |
| U-064 | Validated continuous current   | Critical |
| U-065 | Battery BMS current capability | Critical |
| U-066 | Main fuse rating               | Critical |
| U-067 | Connector current ratings      | High     |
| U-068 | DC-DC thermal performance      | High     |
| U-069 | E-stop implementation          | Critical |
| U-070 | Power isolation architecture   | Critical |

These cannot be finalized solely from actuator nameplate/stall values.

---

# 14. Evidence Gaps

The following evidence has not been established:

* complete physical prototype photographs;
* complete assembly photographs;
* dimensional inspection report;
* mechanical qualification report;
* torque validation report;
* CoM measurement;
* stability test;
* failure/rework log;
* final manufacturing acceptance record.

**Status:** NOT VERIFIED.

---

# 15. Closure Criteria

An unknown can be closed only when appropriate evidence exists.

Examples:

**Missing CAD →** authoritative CAD received and revision identified.

**Missing physical part →** physical part received and photographed/recorded.

**Specification missing →** controlled specification approved.

**CAD verification required →** CAD measurement or manufacturer drawing confirms value.

**Not physically tested →** actual test performed and evidence recorded.

**Revision missing →** revision identifier mapped to source file.

---

# 16. Current Closure Summary

| Category                    | Status                   |
| --------------------------- | ------------------------ |
| Product identity            | CLOSED                   |
| 17-DOF programme definition | CLOSED                   |
| Canonical joint map         | OPEN                     |
| Complete CAD                | OPEN                     |
| Part dimensions             | PARTIAL / GOOD REFERENCE |
| Drawing coverage            | PARTIAL                  |
| Physical availability       | OPEN                     |
| Manufacturing status        | OPEN                     |
| Final materials             | OPEN                     |
| Final actuator mapping      | OPEN                     |
| Final mass                  | OPEN                     |
| CoM                         | OPEN                     |
| Physical qualification      | OPEN                     |
| Procurement closure         | OPEN                     |
| Complete hand architecture  | OPEN                     |

---

# 17. Final Statement

This register intentionally preserves uncertainty.

The purpose is not to indicate failure of the mechanical programme; it is to provide a traceable record of what was available to the Mechanical Realisation Owner at the time of baseline submission.

All future closure actions must convert each unknown into evidence rather than assumption.

**Status:** OPEN ITEMS CONTROLLED / BASELINE EVIDENCE PRESERVED

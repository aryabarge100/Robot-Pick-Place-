# MANUFACTURING-LOG

**Project:** BHIV 17-DoF Humanoid Robot
**Document ID:** HUMANOID-MFG-002
**Owner:** Arya Barge
**Status:** ACTIVE TRACKER


---

## 1. Purpose

This log tracks the actual manufacturing and fabrication state of humanoid mechanical parts.

The tracker separates:

* CAD-ready parts,
* manufacturing-ready parts,
* fabricated parts,
* measured parts,
* failed/reworked parts,
* unverified parts.

No part is marked fabricated without physical evidence.

---

## 2. Manufacturing Status Definitions

| Status             | Definition                        |
| ------------------ | --------------------------------- |
| `CAD_ONLY`         | CAD/reference geometry exists     |
| `DRAWING_REQUIRED` | Manufacturing drawing incomplete  |
| `MFG_READY`        | Released for manufacturing        |
| `IN_PRODUCTION`    | Fabrication has started           |
| `FABRICATED`       | Physical part completed           |
| `MEASURED`         | Physical dimensions/mass recorded |
| `PASS`             | Inspection passed                 |
| `REWORK`           | Physical part requires correction |
| `FAILED`           | Manufacturing failure             |
| `UNKNOWN`          | Status not evidenced              |

---

## 3. Manufacturing Master Log

| Part ID | Part / Assembly      | CAD Rev | Method | Material | Date | Operator/Vendor | Expected Mass | Actual Mass | Critical Dimension | Actual Dimension | Result     | Evidence      |
| ------- | -------------------- | ------- | ------ | -------- | ---- | --------------- | ------------: | ----------: | ------------------ | ---------------- | ---------- | ------------- |
| TBD     | Torso Proto K        | TBD     | TBD    | TBD      | —    | —               |     595.43 g* |           — | TBD                | —                | `CAD_ONLY` | CAD reference |
| TBD     | Torso D              | TBD     | TBD    | TBD      | —    | —               |    1204.17 g* |           — | TBD                | —                | `CAD_ONLY` | CAD reference |
| TBD     | Torso B              | TBD     | TBD    | TBD      | —    | —               |   12342.28 g* |           — | TBD                | —                | `CAD_ONLY` | CAD reference |
| TBD     | Thigh                | TBD     | TBD    | TBD      | —    | —               |    7464.06 g* |           — | TBD                | —                | `CAD_ONLY` | CAD reference |
| TBD     | Leg Proto / Others G | TBD     | TBD    | TBD      | —    | —               |   14925.45 g* |           — | TBD                | —                | `CAD_ONLY` | CAD reference |
| TBD     | Humanoid Shell D     | TBD     | TBD    | TBD      | —    | —               |    6639.96 g* |           — | TBD                | —                | `CAD_ONLY` | CAD reference |
| TBD     | Hip Motor 1          | TBD     | TBD    | TBD      | —    | —               |     681.30 g* |           — | TBD                | —                | `CAD_ONLY` | CAD reference |

`*` CAD/reference mass only; not physically measured.

---

## 4. Manufacturing Evidence Rule

A part may only be changed from:

```text
CAD_ONLY
```

to:

```text
FABRICATED
```

when evidence exists, such as:

* photograph,
* fabrication receipt,
* vendor confirmation,
* print record,
* machining record,
* physical inspection record.

A part may only be changed to:

```text
MEASURED / PASS
```

after actual dimensional/mass measurements are recorded.

---

## 5. Fabrication Record Template

For every manufactured component, record:

```text
Part ID:
Part Name:
CAD Revision:
Drawing Revision:
Manufacturing Method:
Material:
Vendor / Operator:
Manufacturing Date:
Expected Mass:
Actual Mass:
Critical Dimension:
Expected Dimension:
Measured Dimension:
Tolerance:
Result:
Rework Required:
Failure Mode:
Evidence:
```

---

## 6. Additive Manufacturing Record

For 3D-printed components record:

| Field             | Required |
| ----------------- | -------- |
| Part ID           | Yes      |
| CAD revision      | Yes      |
| Material          | Yes      |
| Printer           | Yes      |
| Nozzle            | Yes      |
| Layer height      | Yes      |
| Infill            | Yes      |
| Print orientation | Yes      |
| Support strategy  | Yes      |
| Print time        | Yes      |
| Material consumed | Yes      |
| Actual mass       | Yes      |
| Defects           | Yes      |
| Reprint count     | Yes      |
| Photos            | Yes      |

---

## 7. Machining Record

For machined parts record:

* material certificate where available,
* stock dimensions,
* machining process,
* drawing revision,
* critical dimensions,
* tolerance,
* surface finish,
* deburring,
* inspection result,
* vendor,
* inspection evidence.

---

## 8. Failure / Rework Tracking

| Failure ID | Part ID | Failure                 | Cause | Corrective Action | Reprint/Rework | Final Status | Evidence |
| ---------- | ------- | ----------------------- | ----- | ----------------- | -------------- | ------------ | -------- |
| MFG-F-001  | TBD     | No failure recorded yet | —     | —                 | —              | `OPEN`       | —        |

No manufacturing failure is recorded until an actual event is observed.

---

## 9. Dimensional Inspection

Critical interfaces should be checked after fabrication.

Recommended checks:

* mounting-hole pattern,
* hole diameter,
* plate thickness,
* joint-axis alignment,
* actuator mounting,
* cable clearance,
* enclosure fit,
* mating-part clearance,
* fastener engagement.

---

## 10. Revision Control

Manufacturing shall always reference the released revision:

```text
CAD Revision
      ↓
Drawing Revision
      ↓
Manufacturing Record
      ↓
Physical Part
      ↓
Inspection Result
```

If CAD changes after fabrication, the existing physical part must be re-evaluated.

---

## 11. Current Manufacturing Status

**No physical fabrication result is claimed in this log without evidence.**

Current baseline:

**`CAD / MANUFACTURING PREPARATION — PHYSICAL FABRICATION STATUS TO BE UPDATED FROM EVIDENCE`**

---

## 12. Closure Requirements

Manufacturing phase can be closed only when:

* all required parts have a released CAD revision,
* drawings are available where required,
* material is specified,
* manufacturing method is specified,
* fabrication evidence exists,
* actual mass is recorded,
* critical dimensions are measured,
* failures/rework are logged,
* inspection status is recorded,
* final assembly revision is frozen.

**Status: `OPEN`**

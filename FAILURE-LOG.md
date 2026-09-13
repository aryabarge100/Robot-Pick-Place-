# FAILURE-LOG

**Project:** BHIV 17-DoF Humanoid Robot
**Document ID:** HUMANOID-MECH-FAIL-001
**Owner:** Arya Barge
**Status:** ACTIVE

---

# 1. Purpose

This document records mechanical manufacturing, assembly and qualification failures.

It provides traceability from:

```text
Failure
  ↓
Evidence
  ↓
Root Cause
  ↓
Corrective Action
  ↓
Rework
  ↓
Retest
  ↓
Closure
```

---

# 2. Failure Classification

| Category             | Description                                |
| -------------------- | ------------------------------------------ |
| `CAD`                | Geometry/revision/interface problem        |
| `MFG`                | Manufacturing/fabrication problem          |
| `DIMENSIONAL`        | Measured dimension outside requirement     |
| `ASSEMBLY`           | Fit/assembly problem                       |
| `FASTENER`           | Fastener/thread/insertion problem          |
| `STRUCTURAL`         | Crack/deformation/breakage                 |
| `ACTUATOR_INTERFACE` | Mechanical actuator mounting problem       |
| `CLEARANCE`          | Mechanical interference                    |
| `CABLE`              | Mechanical cable routing/clearance problem |
| `QUALIFICATION`      | Test failure                               |

---

# 3. Severity

| Severity      | Definition                                       |
| ------------- | ------------------------------------------------ |
| S1 — Critical | Safety/structural integrity or major system risk |
| S2 — Major    | Prevents intended mechanical operation           |
| S3 — Moderate | Requires rework but limited system impact        |
| S4 — Minor    | Cosmetic/non-critical issue                      |

---

# 4. Failure Register

| Failure ID | Date | Part/Joint | Category | Severity | Description                                         | Status | Evidence |
| ---------- | ---- | ---------- | -------- | -------- | --------------------------------------------------- | ------ | -------- |
| F-001      | —    | —          | —        | —        | **No physical failure evidence currently recorded** | OPEN   | —        |

---

# 5. Failure Record Template

For each failure create:

```text
Failure ID:
Date:
Part ID:
Joint ID:
CAD Revision:
Drawing Revision:
Manufacturing Revision:
Category:
Severity:
Observed Condition:
Expected Condition:
Measured Value:
Expected Value:
Evidence:
Immediate Action:
Root Cause:
Corrective Action:
Rework Required:
Rework Date:
Retest:
Retest Result:
Final Status:
Approver:
```

---

# 6. Root-Cause Classification

Use one or more:

* incorrect CAD geometry,
* incorrect CAD revision,
* incorrect manufacturing dimension,
* incorrect material,
* insufficient tolerance,
* incorrect fastener,
* incorrect actuator interface,
* assembly error,
* manufacturing defect,
* supplier error,
* unknown.

---

# 7. Rework Tracking

| Rework ID | Failure ID | Part | Revision | Action | Date | Result  | Evidence |
| --------- | ---------- | ---- | -------- | ------ | ---- | ------- | -------- |
| RW-001    | —          | —    | —        | —      | —    | PENDING | —        |

---

# 8. Reprint / Refabrication Tracking

For additive/manufactured parts:

| Part ID | Original Rev | Failure | Reprint/Rework | New Rev | Result  | Evidence |
| ------- | ------------ | ------- | -------------- | ------- | ------- | -------- |
| TBD     | TBD          | TBD     | TBD            | TBD     | PENDING | —        |

---

# 9. Qualification Failure Link

Any failure discovered during mechanical qualification must reference:

`HUMANOID-MECH-QUAL-001.md`

Example:

```text
Qualification Test:
Q06 — Static Load

Failure ID:
F-XXX

Evidence:
EV-XXX
```

---

# 10. Closure Rules

A failure may be marked `CLOSED` only when:

* failure is documented,
* evidence is attached,
* root cause is identified or formally accepted as unknown,
* corrective action is completed,
* affected component revision is recorded,
* rework is inspected,
* retest is completed where required.

---

# 11. Current Failure Status

No physical failure should be invented or inferred from CAD uncertainty.

Current status:

**`NO PHYSICAL FAILURE EVENTS RECORDED — FAILURE LOG READY FOR LIVE USE`**

CAD uncertainty, missing dimensions and unverified masses belong in the appropriate baseline/known-unknown documents unless they produce an actual physical failure.

---

# 12. Evidence Naming Convention

Recommended:

```text
EV-F001-01-photo.jpg
EV-F001-02-measurement.jpg
EV-F001-03-inspection.md
EV-F001-04-retest.md
```

---


# ASSEMBLY-MANUAL

**Project:** BHIV 17-DoF Humanoid Robot
**Document ID:** HUMANOID-ASM-001
**Owner:** Arya Barge
**Status:** CONTROLLED ASSEMBLY PROCEDURE — PRE-PHYSICAL BUILD

---

## 1. Purpose

This document defines the intended mechanical assembly sequence for the 17-DoF humanoid prototype.

It is a controlled assembly procedure and must be updated when the released CAD assembly or physical prototype changes.

---

## 2. Important Status

This document describes the **assembly procedure**, not evidence that assembly has already occurred.

Actual assembly completion must be recorded separately using:

* photographs,
* inspection records,
* measured dimensions,
* fastener verification,
* assembly log.

---

# 3. Assembly Preconditions

Before starting assembly verify:

* correct CAD revision,
* correct part revision,
* manufacturing inspection completed,
* actuator model confirmed,
* electronics mounting interfaces confirmed,
* fastener sizes confirmed,
* inserts installed where required,
* threaded holes clear,
* mating surfaces clean,
* no visible manufacturing defects.

---

# 4. Required Tools

Final tool list must be confirmed against the released hardware.

Typical tools:

* metric hex key set,
* screwdrivers,
* torque driver,
* digital caliper,
* thread gauges where required,
* pliers,
* deburring tools,
* cable-management tools,
* soft mallet if required,
* inspection light.

---

# 5. Fastener Control

Do not assume fastener size from a generic assembly.

For each fastener record:

| Fastener ID | Size | Length | Head Type | Quantity | Location | Torque | Status |
| ----------- | ---- | -----: | --------- | -------: | -------- | ------ | ------ |
| TBD         | TBD  |    TBD | TBD       |      TBD | TBD      | TBD    | TBD    |

Final torque values must come from:

* fastener specification,
* material/thread engagement,
* actuator manufacturer requirement,
* engineering approval.

---

# 6. Recommended Assembly Hierarchy

```text
HUMANOID
│
├── Torso Assembly
│   ├── Structural body
│   ├── Electronics mounting
│   └── Sensor interfaces
│
├── Head Assembly
│   ├── Head structure
│   └── Camera/sensor interface
│
├── Left Arm
│   ├── Shoulder interface
│   ├── Upper arm
│   ├── Elbow
│   └── Forearm / hand
│
├── Right Arm
│   ├── Shoulder interface
│   ├── Upper arm
│   ├── Elbow
│   └── Forearm / hand
│
├── Left Leg
│   ├── Hip
│   ├── Thigh
│   ├── Knee
│   └── Leg / foot
│
└── Right Leg
    ├── Hip
    ├── Thigh
    ├── Knee
    └── Leg / foot
```

The hierarchy must be reconciled with the recovered canonical CAD before physical assembly.

---

# 7. Assembly Sequence

## Step 1 — Part Identification

Lay out all parts.

Verify:

* Part ID,
* revision,
* quantity,
* left/right orientation,
* actuator interface,
* fastener requirement.

Do not install unidentified parts.

---

## Step 2 — Structural Subassemblies

Build the structural subassemblies individually.

For each:

1. clean mating surfaces,
2. inspect holes,
3. install inserts if applicable,
4. loosely install fasteners,
5. align mating faces,
6. verify dimensions,
7. tighten according to approved torque specification.

---

## Step 3 — Hip Assembly

Install:

1. hip structural interface,
2. actuator/motor interface,
3. associated brackets,
4. mechanical links,
5. fasteners.

Check:

* axis alignment,
* rotation clearance,
* cable clearance,
* mechanical end stops.

Do not force an actuator into a misaligned mounting pattern.

---

## Step 4 — Thigh Assembly

Install:

1. hip-side connection,
2. thigh structural component,
3. knee-side interface,
4. required actuator/brackets.

Check:

* straightness,
* joint-axis alignment,
* clearance through expected motion,
* fastener engagement.

---

## Step 5 — Lower-Leg Assembly

Install:

1. knee interface,
2. lower-leg structure,
3. ankle/foot interface where applicable.

Verify:

* left/right symmetry where intended,
* joint clearance,
* no interference,
* structural rigidity.

---

## Step 6 — Arm Assemblies

For each arm:

1. shoulder structure,
2. shoulder actuator/interface,
3. upper arm,
4. elbow interface,
5. forearm,
6. hand interface.

Perform left/right inspection separately.

---

## Step 7 — Hand Assembly

Where the reference architecture retains the five-actuator hand:

* verify the exact actuator MPN,
* verify bracket geometry,
* verify mounting pattern,
* verify tendon/linkage or joint interfaces,
* verify cable routing.

Do not substitute actuator models without revision-controlled approval.

---

## Step 8 — Head / Sensor Interfaces

Install head structural components.

Confirm:

* camera mounting,
* sensor clearance,
* cable exit,
* service access,
* vibration/isolation requirements.

The exact sensor/electronics package remains dependent on the approved electronics interface.

---

## Step 9 — Electronics Mounting

Install only the electronics that have an approved mechanical mounting interface.

Check:

* standoff position,
* connector access,
* cable bend radius,
* heat dissipation,
* serviceability,
* mechanical interference.

---

## Step 10 — Cable Routing

Route cables away from:

* moving joints,
* sharp edges,
* pinch points,
* high-temperature surfaces,
* rotating actuator components.

Maintain service loops where required.

Do not allow cables to become structural load paths.

---

# 8. Pre-Operational Mechanical Inspection

Before powered operation:

### Structural

* all structural parts installed,
* no cracks,
* no major print defects,
* no loose hardware.

### Joints

* actuator mounting secure,
* axes aligned,
* no unexpected mechanical binding,
* full intended range checked manually where safe.

### Fasteners

* correct quantity,
* correct length,
* torque status recorded.

### Electronics

* mounting secure,
* connectors accessible,
* cables protected.

---

# 9. Assembly Inspection Record

| Check           | Expected                  | Actual | Result | Evidence |
| --------------- | ------------------------- | ------ | ------ | -------- |
| Part revision   | Correct                   | TBD    | TBD    | —        |
| Structural fit  | No interference           | TBD    | TBD    | —        |
| Joint alignment | Within approved tolerance | TBD    | TBD    | —        |
| Fasteners       | Correct                   | TBD    | TBD    | —        |
| Cable clearance | No pinch                  | TBD    | TBD    | —        |
| Service access  | Available                 | TBD    | TBD    | —        |

---

# 10. Assembly Failure Handling

If a component does not fit:

**DO NOT force assembly.**

Follow:

```text
Stop assembly
    ↓
Record failure
    ↓
Check CAD revision
    ↓
Check manufactured part
    ↓
Check measured dimensions
    ↓
Identify root cause
    ↓
Approve corrective action
    ↓
Rework / revise
    ↓
Re-inspect
```

---

# 11. Assembly Evidence

Each completed major subassembly should have:

* photograph,
* assembly revision,
* part list,
* inspection result,
* measured critical dimensions,
* torque record where applicable.

---

# 12. Assembly Completion Criteria

Assembly may be marked complete only when:

* all required subassemblies are installed,
* revision consistency is confirmed,
* fasteners are verified,
* joint interfaces are inspected,
* cable routing is checked,
* critical dimensions are measured,
* deviations are recorded,
* evidence package is complete.

**Current status: `ASSEMBLY PROCEDURE DEFINED — PHYSICAL COMPLETION NOT CLAIMED`**

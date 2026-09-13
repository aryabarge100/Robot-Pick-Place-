# HUMANOID-BOM-001

**Project:** BHIV 17-DOF Humanoid Robot  
**Document:** Bill of Materials  
**Document ID:** HUMANOID-BOM-001  
**Revision:** BOM-001-R0  
**Owner:** Arya Barge — Mechanical Realisation & Manufacturing  
**Electronics / Embedded Integration:** Siddhesh  
**Status:** BASELINE / PROCUREMENT PLANNING  


---

## 1. Purpose

This BOM defines the controlled parts required to reproduce the existing BHIV 17-DOF
humanoid robot.

This is a procurement and manufacturing baseline.

It does NOT authorize an architecture change.

Any change to DOF, actuator type, battery architecture, compute placement,
electronics architecture or major mechanical interface requires review and approval.

---

## 2. BOM Status Definitions

| Status | Meaning |
|---|---|
| CONFIRMED | Directly supported by supplied CAD/documentation |
| PLANNING | Reasonable procurement/planning value; final confirmation required |
| SPECIFICATION-MISSING | Required item identified but exact specification is not frozen |
| CAD-MISSING | Mechanical interface cannot yet be released |
| QUOTE-REQUIRED | Supplier quotation required before purchase |
| BLOCKED | Cannot safely procure until dependency is resolved |

---

# 3. Mechanical BOM

| Part ID | Description | Category | Manufacturer / Source | MPN / Reference | Qty | Material / Specification | Criticality | Interface Dependency | Revision | Status |
|---|---|---|---|---|---:|---|---|---|---|---|
| HUM-MECH-001 | Torso K | Structural | Existing CAD | Torso K | 1 | CAD-defined | High | Torso electronics / body | Current CAD | CONFIRMED |
| HUM-MECH-002 | Torso D | Structural / electronics enclosure | Existing CAD | Torso D | 1 | CAD-defined | High | Electronics packaging | Current CAD | CONFIRMED |
| HUM-MECH-003 | Torso B | Major structural assembly | Existing CAD | Torso B | 1 | CAD-defined | Critical | Whole-body structure | Current CAD | CONFIRMED* |
| HUM-MECH-004 | Thigh assembly | Leg structure | Existing CAD | Thigh | 2 | CAD-defined | Critical | Hip / knee actuator | Current CAD | CONFIRMED* |
| HUM-MECH-005 | Leg Proto / Leg assembly | Leg structure | Existing CAD | Leg Proto / Others G | 2 | CAD-defined | Critical | Knee / ankle interfaces | Current CAD | CONFIRMED* |
| HUM-MECH-006 | Humanoid Shell D | External shell | Existing CAD | Shell D / iCub reference | 1 | CAD-defined | Medium | Torso / electronics | Current CAD | CONFIRMED* |
| HUM-MECH-007 | Hip motor housing/interface | Actuator interface | Existing CAD | Hip Motor 1 | 2 | CAD-defined | Critical | Hip actuator | Current CAD | CONFIRMED* |
| HUM-MECH-008 | Shoulder/arm structural parts | Arm structure | Existing CAD | CAD reference required | 2 sets | CAD-defined | High | Arm actuator | TBD | CAD-MISSING |
| HUM-MECH-009 | Forearm structural parts | Arm structure | Existing CAD | CAD reference required | 2 | CAD-defined | High | Wrist/elbow actuator | TBD | CAD-MISSING |
| HUM-MECH-010 | Hand/palm structure | End effector | Existing CAD | Hand CAD | 2 | CAD-defined | High | XL330 / finger actuators | TBD | SPECIFICATION-MISSING |
| HUM-MECH-011 | Finger mechanical links | End effector | Existing CAD | Finger CAD | 10 | CAD-defined | Medium | XL330 actuator | TBD | CAD-MISSING |
| HUM-MECH-012 | Actuator brackets | Mechanical interface | Existing CAD | Servo bracket CAD | As required | CAD-defined | Critical | Actuator mounting | TBD | CAD-MISSING |
| HUM-MECH-013 | Bearing / joint hardware | Joint hardware | TBD | TBD | As required | Bearing specification required | Critical | Joint shafts | TBD | SPECIFICATION-MISSING |
| HUM-MECH-014 | Joint shafts / pins | Joint hardware | TBD | TBD | As required | Steel / CAD-defined | High | Bearings / actuator | TBD | SPECIFICATION-MISSING |
| HUM-MECH-015 | Fastener set | Assembly hardware | TBD | M2.5/M3/etc. to CAD | As required | Grade to be frozen | High | All assemblies | TBD | SPECIFICATION-MISSING |
| HUM-MECH-016 | PCB mounting standoffs | Hardware | TBD | M3 | As required | M3 | Medium | Electronics plates | TBD | PLANNING |
| HUM-MECH-017 | Cable clips / strain relief | Integration hardware | TBD | TBD | As required | Nylon / equivalent | Medium | Moving joints | TBD | PLANNING |
| HUM-MECH-018 | Heat-set inserts | Assembly hardware | TBD | CAD-specific | As required | Brass threaded inserts | Medium | Printed parts | TBD | PLANNING |

### Existing CAD evidence

The latest supplied dimensions include:

| Part | External dimensions (mm) | Reported mass |
|---|---:|---:|
| Torso K | 210.23 × 150.53 × 38.86 | 595.43 g |
| Torso D | 210.23 × 150.53 × 90.00 | 1204.17 g |
| Torso B | 424.96 × 331.28 × 140.00 | 12342.28 g* |
| Thigh | ~421.04 × 100 × 84.96 | 7464.06 g* |
| Leg Proto / Others G | 529.03 × 321.60 × 200.00 | 14925.45 g* |
| Humanoid Shell D | 566.10 × 283.64 × 100.00 | 6639.96 g* |
| Hip Motor 1 | 80 × 80 × 70 | 681.30 g |
| Dynamixel assembly envelope | 1639.63 × 546.94 × 260.00 | Not supplied |

`*` Mass values require verification before being used for final robot mass or actuator sizing.

These dimensions are taken from the latest electronics/mechanical integration reference. :contentReference[oaicite:1]{index=1}

---

# 4. Actuator BOM

## 4.1 Hand actuators

| Part ID | Description | Manufacturer | MPN | Qty | Interface | Status |
|---|---|---|---|---:|---|---|
| HUM-ACT-001 | Smart finger servo | ROBOTIS | XL330-M288-T | 10 | TTL half-duplex | PLANNING / VERIFY |
| HUM-ACT-002 | XL330 mounting hardware | ROBOTIS / CAD | CAD-specific | 10 sets | Palm/finger mounting | SPECIFICATION-MISSING |

The current electronics baseline specifies 5 × XL330 per hand, giving 10 total if this hand architecture is retained. The document explicitly says the hand architecture must be confirmed against the mechanical CAD before ordering. :contentReference[oaicite:2]{index=2}

---

## 4.2 Main body actuators

| Part ID | Description | Qty | Required information | Status |
|---|---|---:|---|---|
| HUM-ACT-003 | Hip actuator | 2 | Exact MPN, torque, voltage, mounting pattern | SPECIFICATION-MISSING |
| HUM-ACT-004 | Knee actuator | 2 | Exact MPN, torque, voltage, mounting pattern | SPECIFICATION-MISSING |
| HUM-ACT-005 | Ankle actuator | TBD | Exact DOF allocation required | BLOCKED |
| HUM-ACT-006 | Shoulder actuator | TBD | Exact DOF allocation required | BLOCKED |
| HUM-ACT-007 | Elbow actuator | TBD | Exact DOF allocation required | BLOCKED |
| HUM-ACT-008 | Wrist actuator | TBD | Exact DOF allocation required | BLOCKED |

**Important:** Do NOT convert these TBD quantities into guessed actuator purchases.

The company specification requires the existing DOF and actuator architecture to be recovered before procurement. :contentReference[oaicite:3]{index=3}

---

# 5. Electronics / Embedded BOM

| Part ID | Component | Recommended specification | Qty | Planning envelope (mm) | Mounting location | Owner | Status |
|---|---|---|---:|---:|---|---|---|
| HUM-EL-001 | Main controller | STM32G431 development/control board | 1 | 70 × 50 × 20 | Central torso | Siddhesh | PLANNING |
| HUM-EL-002 | CAN transceiver | TJA1051T/3-compatible CAN board | 1 | 30 × 25 × 10 | Near STM32 | Siddhesh | PLANNING |
| HUM-EL-003 | Power Distribution Board | 24 V input, fused/branched outputs | 1 | 100 × 70 × 25 | Lower torso | Siddhesh | SPECIFICATION-MISSING |
| HUM-EL-004 | Main fuse + holder | DC fuse, rating from current budget | 1 | 50 × 30 × 25 | Battery positive | Siddhesh | BLOCKED |
| HUM-EL-005 | Main isolation switch | DC-rated switch/contactor | 1 | 60 × 40 × 30 | Battery/PDB | Siddhesh | PLANNING |
| HUM-EL-006 | Emergency stop | E-stop + safe power interruption | 1 | 50 × 30 × 25 + external switch | Accessible torso | Siddhesh | PLANNING |
| HUM-EL-007 | 24→12 V DC-DC | Regulated converter | 1 | 60 × 40 × 25 | Torso electronics bay | Siddhesh | BLOCKED |
| HUM-EL-008 | 24→5 V DC-DC | Regulated converter | 1 | 60 × 40 × 25 | Torso / hand power | Siddhesh | BLOCKED |
| HUM-EL-009 | 3.3 V regulator | Clean regulated logic supply | 1 | 50 × 30 × 20 | Near STM32 | Siddhesh | PLANNING |
| HUM-EL-010 | IMU | MPU6050 module | 1 | 25 × 20 × 10 | Central rigid torso | Siddhesh | PLANNING |
| HUM-EL-011 | Current sensor | Hall/shunt monitor | 1–2 | 30 × 20 × 15 | Main/branch rail | Siddhesh | SPECIFICATION-MISSING |
| HUM-EL-012 | Voltage sensing | Divider + ADC protection | 1 | 30 × 20 × 15 | PDB/battery | Siddhesh | PLANNING |
| HUM-EL-013 | USB service interface | USB interface for STM32 | 1 | 30 × 20 × 10 | Side/rear torso | Siddhesh | PLANNING |
| HUM-EL-014 | CAN network | CAN-capable actuator network | As per DOF | Actuator-specific | Body joints | Siddhesh | BLOCKED |
| HUM-EL-015 | TTL hand bus | Half-duplex TTL | 2 buses | Connector-dependent | Hands | Siddhesh | PLANNING |
| HUM-EL-016 | CAN cable | Twisted-pair CAN cable | As required | — | Torso → body | Siddhesh | PLANNING |
| HUM-EL-017 | Power wiring | Current-rated wiring | As required | — | Battery/PDB/actuators | Siddhesh + Arya | BLOCKED |
| HUM-EL-018 | Locking connectors | Power/signal connectors | As required | — | All electronics | Siddhesh + Arya | SPECIFICATION-MISSING |
| HUM-EL-019 | Cable management | Sleeves/clips/service loops | As required | — | Moving joints | Arya | PLANNING |
| HUM-EL-020 | PCB standoffs | M3 | As required | — | Torso electronics plate | Arya | PLANNING |
| HUM-EL-021 | Cooling hardware | Heat sinks / airflow hardware | As required | — | DC-DC/enclosed bays | Siddhesh | AFTER THERMAL TEST |

The current electronics reference defines this architecture as:

**Battery → Fuse → Isolation/E-stop → PDB → regulated rails / actuator power**

and

**STM32G431 → body actuator network + TTL hand bus + MPU6050 + USB service interface.** :contentReference[oaicite:4]{index=4}

---

# 6. Integration Ownership

| Domain | Arya | Siddhesh |
|---|---|---|
| Mechanical CAD | OWNER | CONSULT |
| Mechanical interfaces | OWNER | INPUT |
| Electronics packaging | OWNER | OWNER OF ELECTRONICS REQUIREMENT |
| Controller selection | CONSULT | OWNER |
| Actuator electrical interface | CONSULT | OWNER |
| Actuator mounting interface | OWNER | INPUT |
| Battery physical mounting | OWNER | POWER REQUIREMENT |
| Battery electrical specification | INPUT | OWNER |
| IMU physical mounting | OWNER | SENSOR REQUIREMENT |
| IMU electrical interface | CONSULT | OWNER |
| Cable routing | OWNER | INPUT |
| Connector specification | INPUT | OWNER |
| Firmware | — | OWNER |
| Embedded control | — | OWNER |
| Mechanical qualification | OWNER | SUPPORT |
| Electrical qualification | SUPPORT | OWNER |

---

# 7. Critical BOM Freeze Conditions

The following MUST be frozen before final procurement:

1. Final 17-DOF joint allocation.
2. Exact actuator MPN for every body joint.
3. Actuator voltage/current/torque.
4. Actuator mounting-hole pattern.
5. Battery voltage and capacity.
6. Peak and continuous current.
7. PDB rating.
8. Fuse rating.
9. DC-DC ratings.
10. CAN topology.
11. Hand actuator architecture.
12. Final electronics mounting dimensions.


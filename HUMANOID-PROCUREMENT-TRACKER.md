# HUMANOID-PROCUREMENT-TRACKER

**Project:** BHIV 17-DOF Humanoid Robot  
**Document:** Procurement Tracker  
**Document ID:** PROCUREMENT-TRACKER-001   
**Mechanical Owner:** Arya Barge  
**Electronics / Embedded Owner:** Siddhesh  
**Status:** ACTIVE  


---

## 1. Procurement State Definitions

| State | Meaning |
|---|---|
| NOT STARTED | Item identified but sourcing has not started |
| SPECIFICATION REQUIRED | Technical specification is incomplete |
| CAD INTERFACE REQUIRED | Mechanical interface must be confirmed |
| QUOTE REQUIRED | Supplier quotation needed |
| QUOTED | At least one quotation received |
| 3-QUOTE COMPLETE | Required supplier comparison completed |
| SELECTED | Supplier selected |
| ORDERED | PO/order placed |
| RECEIVED | Physical item received |
| INSPECTED | Incoming inspection completed |
| ACCEPTED | Accepted for integration |
| REJECTED | Failed incoming inspection |
| BLOCKED | Dependency prevents procurement |

---

# 2. Immediate Procurement Tracker

| ID | Part | Qty | Owner | Dependency | Current State | Next Action | Evidence Required |
|---|---|---:|---|---|---|---|---|
| PT-001 | XL330-M288-T | 10 | Siddhesh | Hand architecture | SPECIFICATION REQUIRED | Confirm final hand actuator choice | Datasheet + quote |
| PT-002 | STM32G431 board | 1 | Siddhesh | Embedded architecture | SPECIFICATION REQUIRED | Confirm exact board/PCB | MPN + datasheet |
| PT-003 | CAN transceiver | 1 | Siddhesh | CAN actuator network | SPECIFICATION REQUIRED | Freeze transceiver board | Datasheet + MPN |
| PT-004 | PDB | 1 | Siddhesh | Current budget | BLOCKED | Calculate peak/continuous current | Current budget |
| PT-005 | Main fuse | 1 | Siddhesh | Current budget | BLOCKED | Freeze fuse rating | Calculation + datasheet |
| PT-006 | Isolation switch | 1 | Siddhesh | Battery voltage/current | SPECIFICATION REQUIRED | Freeze DC rating | Datasheet |
| PT-007 | E-stop | 1 | Siddhesh | Safety architecture | SPECIFICATION REQUIRED | Freeze hardware shutdown path | Wiring diagram |
| PT-008 | 24→12 V DC-DC | 1 | Siddhesh | 12 V load | BLOCKED | Calculate load and select converter | Datasheet |
| PT-009 | 24→5 V DC-DC | 1 | Siddhesh | Hand/auxiliary current | BLOCKED | Calculate simultaneous load | Datasheet |
| PT-010 | 3.3 V regulator | 1 | Siddhesh | Logic load | SPECIFICATION REQUIRED | Select regulator | Datasheet |
| PT-011 | MPU6050 | 1 | Siddhesh | IMU architecture | QUOTE REQUIRED | Confirm module | Datasheet + quote |
| PT-012 | Current sensors | 1–2 | Siddhesh | Peak current | BLOCKED | Freeze sensing range | Datasheet |
| PT-013 | Voltage sensing | 1 | Siddhesh | Battery voltage | SPECIFICATION REQUIRED | Freeze ADC circuit | Schematic |
| PT-014 | CAN cable | As required | Siddhesh/Arya | CAN topology | NOT STARTED | Determine cable length | Wiring plan |
| PT-015 | Power wiring | As required | Siddhesh/Arya | Current budget | BLOCKED | Freeze gauges | Current calculation |
| PT-016 | Connectors | As required | Siddhesh/Arya | All electronics | BLOCKED | Freeze connector families | Connector schedule |
| PT-017 | PCB standoffs | As required | Arya | PCB dimensions | CAD INTERFACE REQUIRED | Confirm hole pattern | CAD evidence |
| PT-018 | Cable management | As required | Arya | Final routing | NOT STARTED | Define clips/service loops | CAD evidence |
| PT-019 | Fastener kit | 1 lot | Arya | Final CAD | CAD INTERFACE REQUIRED | Generate fastener schedule | Drawing/BOM |
| PT-020 | Bearings | As required | Arya | Joint design | SPECIFICATION REQUIRED | Extract bearing IDs from CAD | CAD/drawing |
| PT-021 | Shafts/pins | As required | Arya | Joint design | SPECIFICATION REQUIRED | Extract dimensions | Drawing |
| PT-022 | Actuator brackets | As required | Arya | Actuator MPN | BLOCKED | Wait for actuator freeze | Interface drawing |
| PT-023 | Torso K | 1 | Arya | Manufacturing method | QUOTE REQUIRED | Obtain fabrication quote | CAD + quote |
| PT-024 | Torso D | 1 | Arya | Manufacturing method | QUOTE REQUIRED | Obtain fabrication quote | CAD + quote |
| PT-025 | Torso B | 1 | Arya | Mass/CAD verification | BLOCKED | Verify CAD mass first | CAD evidence |
| PT-026 | Thigh | 2 | Arya | Material/process | QUOTE REQUIRED | DFM + quote | Drawing + quote |
| PT-027 | Leg | 2 | Arya | Material/process | QUOTE REQUIRED | DFM + quote | Drawing + quote |
| PT-028 | Shell D | 1 | Arya | CAD revision | CAD INTERFACE REQUIRED | Freeze manufacturing revision | Revision evidence |
| PT-029 | Hand/palm | 2 | Arya | XL330 interface | BLOCKED | Wait for Siddhesh actuator confirmation | Interface drawing |
| PT-030 | Finger links | 10 | Arya | XL330 interface | BLOCKED | Confirm actuator mounting | CAD revision |

---

# 3. Siddhesh Integration Gate

Before Arya releases mechanical procurement, Siddhesh must confirm:

### Electronics

- [ ] Exact STM32G431 board/PCB
- [ ] CAN transceiver
- [ ] CAN bus topology
- [ ] Exact actuator electrical interface
- [ ] Hand actuator architecture
- [ ] Battery voltage
- [ ] Battery capacity
- [ ] Peak current
- [ ] Continuous current
- [ ] PDB rating
- [ ] Fuse rating
- [ ] E-stop architecture
- [ ] 24→12 V converter rating
- [ ] 24→5 V converter rating
- [ ] 3.3 V rail requirement
- [ ] IMU model
- [ ] Current sensing range
- [ ] Voltage sensing range
- [ ] Connector family
- [ ] Cable gauge

### Mechanical interface information Siddhesh must provide to Arya

- PCB dimensions
- PCB mounting holes
- connector locations
- connector keep-out zones
- cable exit directions
- minimum bending radius
- actuator connector orientation
- CAN connector location
- USB access requirement
- IMU mounting/orientation requirement
- thermal clearance
- battery envelope
- service-access requirement

---

# 4. Arya → Siddhesh Interface Contract

Arya provides:

1. CAD mounting envelope.
2. Available mounting surfaces.
3. Hole locations.
4. Available volume.
5. Mechanical keep-out zones.
6. Cable-routing channels.
7. Moving-joint pinch zones.
8. Service-access openings.
9. Structural constraints.
10. Manufacturing constraints.

Siddhesh provides:

1. Component dimensions.
2. Mounting-hole pattern.
3. Connector positions.
4. Electrical loads.
5. Cable requirements.
6. Thermal requirements.
7. Communication interfaces.
8. Sensor orientation.
9. Battery requirements.
10. Embedded service requirements.

---

# 5. Procurement Evidence Register

Every purchased item must eventually have:

| Evidence | Required |
|---|---|
| Supplier | YES |
| Manufacturer | YES |
| MPN | YES |
| Datasheet | YES |
| Quotation | YES |
| Price | YES |
| GST | YES |
| Shipping | YES |
| Lead time | YES |
| Stock evidence | YES |
| Warranty | YES |
| Purchase order | YES |
| Delivery evidence | YES |
| Incoming inspection | YES |
| Physical photo | YES |
| Accepted/rejected status | YES |

---

# 6. Incoming Inspection

When a component arrives:

1. Photograph package.
2. Record supplier.
3. Record MPN.
4. Record quantity received.
5. Check physical dimensions.
6. Check connector/interface.
7. Check damage.
8. Compare against datasheet.
9. Record actual mass where relevant.
10. Mark ACCEPTED / REJECTED.
11. Link evidence.

---

# 7. Procurement Release Gate

No item is considered procurement-complete until:

`Specification → Supplier → Quote → Selection → Order → Receive → Inspect → Accept`

---

# 8. Current Blocking Items

The highest-priority blockers are:

### BLOCKER-01 — Body actuator architecture

Exact body actuator models and quantities are not fully frozen.

### BLOCKER-02 — Current budget

Battery, PDB, fuse and DC-DC ratings cannot safely be finalized without peak and continuous actuator current.

### BLOCKER-03 — Hand architecture

Current baseline proposes 10 × XL330-M288-T, but the mechanical reference also contains an alternative step-motor/gear arrangement.

### BLOCKER-04 — Electronics CAD interfaces

Final PCB dimensions, mounting holes and connector locations are required before finalizing torso electronics mounts.

### BLOCKER-05 — CAD mass anomalies

Torso B and Leg Proto reported masses are unusually high and must be checked before using them for system mass/CoM calculations.

### BLOCKER-06 — Mechanical actuator interfaces

Mounting-hole patterns, shaft dimensions and cable exits must match the final actuator MPN.

---

# 9. Release Rule

Arya must NOT release a mechanical mounting interface as final when the associated
electronics/actuator specification is still marked BLOCKED.

Siddhesh must NOT freeze an electronics component when its mechanical envelope,
mounting pattern or connector access has not been checked against the current CAD.

Both sides must record the interface revision before procurement.

---

# 10. Final Acceptance

Procurement is complete only when:

- every purchased item has supplier evidence;
- every custom part has a manufacturing route;
- every actuator has a verified mechanical interface;
- every electronics board has a verified mounting envelope;
- all power components have current-budget justification;
- all cables/connectors have defined interfaces;
- received components are inspected;
- BOM and BOQ revisions match;
- procurement evidence is linked to the relevant Part ID.

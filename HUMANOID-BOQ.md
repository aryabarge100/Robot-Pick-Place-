# HUMANOID-BOQ-001

**Project:** BHIV 17-DOF Humanoid Robot  
**Document:** Bill of Quantities  
**Document ID:** HUMANOID-BOQ-001  
**Revision:** BOQ-001-R0  
**Owner:** Arya Barge  
**Electronics / Embedded:** Siddhesh     
**Status:** PROCUREMENT PLANNING

---

## 1. Pricing Rules

All prices are planning values until supplier quotations are attached.

For every purchased component, obtain up to three quotations where reasonably
available.

Final supplier selection shall consider:

- specification correctness
- authenticity
- stock availability
- lead time
- landed cost
- warranty/support

Cheapest price alone must not determine selection.

---

# 2. Current Market Reference Prices

| BOQ ID | Part ID | Item | Qty | Reference unit price (₹) | Estimated material subtotal (₹) | GST treatment | Shipping | Status |
|---|---|---|---:|---:|---:|---|---|---|
| BOQ-001 | HUM-ACT-001 | ROBOTIS XL330-M288-T | 10 | 3,659 | 36,590 | Verify seller tax invoice | TBD | Planning |
| BOQ-002 | HUM-EL-001 | STM32G431 development board | 1 | 560 | 560 | Verify invoice | TBD | Planning |
| BOQ-003 | HUM-EL-010 | MPU6050 module | 1 | 151 | 151 | Verify invoice | TBD | Planning |
| BOQ-004 | HUM-EL-002 | CAN transceiver board | 1 | 500* | 500* | Quote required | TBD | Quote required |
| BOQ-005 | HUM-EL-003 | 24 V PDB | 1 | 1,500* | 1,500* | Quote required | TBD | Specification required |
| BOQ-006 | HUM-EL-004 | Main fuse + holder | 1 | 250* | 250* | Quote required | TBD | Current rating required |
| BOQ-007 | HUM-EL-005 | DC isolation switch | 1 | 500* | 500* | Quote required | TBD | Specification required |
| BOQ-008 | HUM-EL-006 | Emergency stop | 1 | 350* | 350* | Quote required | TBD | Specification required |
| BOQ-009 | HUM-EL-007 | 24→12 V DC-DC | 1 | 1,200* | 1,200* | Quote required | TBD | Current rating required |
| BOQ-010 | HUM-EL-008 | 24→5 V DC-DC | 1 | 1,000* | 1,000* | Quote required | TBD | Current rating required |
| BOQ-011 | HUM-EL-009 | 3.3 V regulator | 1 | 250* | 250* | Quote required | TBD | Planning |
| BOQ-012 | HUM-EL-011 | Current sensor | 2 | 154* | 308* | Verify rating | TBD | Rating required |
| BOQ-013 | HUM-EL-012 | Voltage sensing circuit | 1 | 150* | 150* | Quote required | TBD | Planning |
| BOQ-014 | HUM-EL-013 | USB service interface | 1 | 200* | 200* | Quote required | TBD | Planning |
| BOQ-015 | HUM-EL-016 | CAN cable | 5 m | 100/m* | 500* | Quote required | TBD | Planning |
| BOQ-016 | HUM-EL-017 | Power wiring | 10 m mixed gauge | 150/m* | 1,500* | Quote required | TBD | Current calculation required |
| BOQ-017 | HUM-EL-018 | Locking connectors | 1 lot | 1,500* | 1,500* | Quote required | TBD | Connector spec required |
| BOQ-018 | HUM-EL-019 | Cable management | 1 lot | 1,000* | 1,000* | Quote required | TBD | Planning |
| BOQ-019 | HUM-EL-020 | M3 PCB standoffs | 1 lot | 300* | 300* | Quote required | TBD | Planning |
| BOQ-020 | HUM-MECH-015 | Fastener kit | 1 lot | 1,500* | 1,500* | Quote required | TBD | CAD schedule required |
| BOQ-021 | HUM-MECH-017 | Cable clips / strain relief | 1 lot | 500* | 500* | Quote required | TBD | Planning |
| BOQ-022 | HUM-MECH-018 | Heat-set inserts | 1 lot | 500* | 500* | Quote required | TBD | Planning |

`*` = engineering planning allowance, NOT a supplier-confirmed quotation.

---

## 3. Verified Market References

### XL330

Current shopping reference found:

- ROBOTIS Dynamixel XL330-M288-T: approximately ₹3,659/unit.

Therefore:

**10 × ₹3,659 = ₹36,590**

This is a current market reference and still needs supplier/authenticity verification before PO release.

### STM32G431

Current Indian reference:

- WeAct STM32G431 core board approximately ₹559–₹688 depending on seller/variant.
- Use **₹600/unit planning value** until Siddhesh freezes the exact board/PCB.

### MPU6050

Current Indian reference:

- MPU6050 module approximately ₹151.
- The bare MPU6050 IC is much more expensive in some distributor listings, so the BOM must explicitly specify whether the requirement is a **module** or a bare IC.

### ESP32 / Teensy

These are NOT currently included as mandatory canonical humanoid controller items.

Current references show approximately:

- ESP32-WROOM-32 development board: ₹285–₹619 depending on board/vendor.
- Teensy 4.1: approximately ₹2,758–₹4,179 depending on vendor.

Do not add either to the production BOM unless Siddhesh confirms that the embedded architecture requires it.

---

# 4. Mechanical Fabrication BOQ

Custom mechanical components should NOT be assigned invented purchase prices.

| BOQ ID | Part | Qty | Manufacturing process | Material | Unit cost | Total | Status |
|---|---|---:|---|---|---:|---:|---|
| M-001 | Torso K | 1 | 3D print / machining per DFM | TBD | QUOTE | QUOTE | Material/process review |
| M-002 | Torso D | 1 | 3D print / machining | TBD | QUOTE | QUOTE | Material/process review |
| M-003 | Torso B | 1 | Manufacturing method TBD | TBD | QUOTE | QUOTE | Mass/CAD verification |
| M-004 | Thigh | 2 | 3D print / machining | TBD | QUOTE | QUOTE | DFM review |
| M-005 | Leg | 2 | 3D print / machining | TBD | QUOTE | QUOTE | DFM review |
| M-006 | Shell D | 1 | 3D print | TBD | QUOTE | QUOTE | CAD review |
| M-007 | Hip motor housing/interface | 2 | 3D print / machining | TBD | QUOTE | QUOTE | Interface verification |
| M-008 | Arm structural parts | 2 sets | 3D print / machining | TBD | QUOTE | QUOTE | CAD incomplete |
| M-009 | Hand/palm structure | 2 | 3D print | TBD | QUOTE | QUOTE | CAD/interface review |
| M-010 | Finger links | 10 | 3D print | TBD | QUOTE | QUOTE | CAD incomplete |
| M-011 | Actuator brackets | As required | 3D print / machining | TBD | QUOTE | QUOTE | CAD verification |
| M-012 | Shafts/pins/bearings | As required | Purchase/machine | Steel | QUOTE | QUOTE | Specification required |

---

# 5. Budget Summary

## Currently identifiable purchased electronics/actuator baseline

Known/reference-priced items:

- XL330 × 10 = ₹36,590
- STM32G431 ≈ ₹600
- MPU6050 ≈ ₹151

**Known/reference subtotal ≈ ₹37,341**

Planning allowances for the remaining electronics, wiring, connectors,
power distribution and mechanical hardware should be treated as provisional
until Siddhesh freezes specifications and supplier quotes are received.

**Do NOT present this as the final humanoid project cost.**

The final BOQ must be recalculated after:
1. actuator architecture freeze,
2. battery freeze,
3. current-budget calculation,
4. mechanical material selection,
5. supplier quotations.

---

# 6. Quote Requirement

For every purchasable component:

| Quote | Required information |
|---|---|
| Q1 | Vendor + MPN + unit price + GST + shipping + lead time |
| Q2 | Vendor + MPN + unit price + GST + shipping + lead time |
| Q3 | Vendor + MPN + unit price + GST + shipping + lead time |

Also record:

- stock status
- warranty
- datasheet
- authenticity evidence
- quotation date
- supplier URL
- selected supplier
- selection reason

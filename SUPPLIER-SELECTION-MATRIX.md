# SUPPLIER-SELECTION-MATRIX

**Project:** BHIV 17-DOF Humanoid Robot
**Owner:** Arya Barge — Mechanical / Manufacturing / Procurement Integration
**Document ID:** HUMANOID-PROC-004
**Status:** MARKET COMPARISON — PRE-QUOTE / PROCUREMENT DECISION
**Currency:** INR (₹)

---

## 1. Purpose

This document compares current India-market suppliers for electronics and actuator components relevant to the 17-DOF humanoid prototype.

The comparison considers:

* Exact part-number match
* Manufacturer authenticity / traceability
* Current listed price
* Availability / stock indication
* Technical suitability
* Datasheet/documentation availability
* Procurement risk
* Lead-time risk
* Warranty/support
* Quantity scalability
* Overall procurement suitability

This matrix is intended to support supplier selection before purchase.

> **Important:** Public website prices are treated as **market references**, not formal supplier quotations. A supplier is considered fully quote-qualified only after obtaining a dated quotation/invoice/proforma or equivalent supplier evidence.

---

# 2. Supplier Scoring Method

Each supplier is scored from 1–5.

| Criterion                       | Weight | Meaning                                                 |
| ------------------------------- | -----: | ------------------------------------------------------- |
| Exact specification / MPN match |    25% | Exact required component and manufacturer part number   |
| Authenticity / traceability     |    20% | Manufacturer/distributor traceability and documentation |
| Price competitiveness           |    15% | Current listed price / landed-cost potential            |
| Availability                    |    10% | Current stock / availability indication                 |
| Lead time                       |    10% | Expected procurement speed                              |
| Technical documentation         |     5% | Datasheet, manufacturer documentation, specifications   |
| Warranty / support              |     5% | Return, warranty and technical support                  |
| Quantity scalability            |     5% | Suitability for prototype + repeat procurement          |
| Procurement risk                |     5% | Counterfeit, listing ambiguity, specification risk      |

### Overall Rating

* **4.5–5.0:** Preferred
* **4.0–4.49:** Acceptable / Backup
* **3.0–3.99:** Conditional
* **<3.0:** Not preferred

---

# 3. Supplier Pool

The following suppliers were considered for current India-market procurement:

| Supplier       | Type                                 | Typical Strength                             |
| -------------- | ------------------------------------ | -------------------------------------------- |
| MG Super Labs  | Robotics/electronics distributor     | ROBOTIS / robotics hardware                  |
| Robu.in        | Indian robotics/electronics retailer | Modules, sensors, development boards         |
| Robocraze      | Indian robotics/electronics retailer | Modules, embedded hardware                   |
| Robokits India | Electronics/robotics retailer        | Sensors and modules                          |
| Evelta         | Electronics distributor              | Semiconductor/electronic components          |
| DigiKey India  | Authorized global distributor        | Original semiconductor/electronic components |
| Mouser India   | Authorized global distributor        | Original semiconductor/electronic components |
| FlyRobo        | Indian robotics/electronics retailer | Sensors/modules                              |

---

# 4. Actuator Selection — DYNAMIXEL XL330-M288-T

## Required Component

**Manufacturer:** ROBOTIS
**MPN:** XL330-M288-T
**Quantity:** 10 units if the current hand architecture is retained
**Application:** Humanoid hand actuator subsystem

The exact XL330-M288-T is important because an apparently similar servo must not be substituted without interface approval.

ROBOTIS identifies the XL330-M288-T as a compact smart actuator with integrated motor, gearing, controller and driver, supporting TTL/RS-485 serial control depending on configuration/interface.

## Current Market Comparison

| Supplier          | Exact MPN Evidence                                |         Current Listed Price | Availability         | Authenticity                 | Assessment                               |
| ----------------- | ------------------------------------------------- | ---------------------------: | -------------------- | ---------------------------- | ---------------------------------------- |
| **MG Super Labs** | **XL330-M288-T**                                  |              **₹3,659/unit** | Listed               | Robotics distributor listing | **Preferred**                            |
| ROBOTIS official  | Manufacturer reference                            | Manufacturer price/reference | Manufacturer channel | **Highest**                  | Reference / authenticity benchmark       |
| Robu.in           | Exact current public price not verified           |               Quote required | —                    | To be verified               | Backup quote candidate                   |
| Robocraze         | Exact current public price not verified           |               Quote required | —                    | To be verified               | Backup quote candidate                   |
| Mouser/DigiKey    | Exact XL330-M288-T retail listing not established |               Quote required | —                    | High if available            | Not preferred unless exact MPN confirmed |

MG Super Labs currently lists the XL330-M288-T at ₹3,659, with a lower displayed price for a 10-piece quantity listing.

### Price Reference

| Quantity | Reference Unit Price | Reference Subtotal |
| -------: | -------------------: | -----------------: |
|       10 |               ₹3,659 |            ₹36,590 |

**Important:** ₹36,590 is a current public-market reference, **not a formal 10-piece supplier quotation**.

### Actuator Decision

**Preferred supplier:** **MG Super Labs**

**Reason:**

1. Exact XL330-M288-T listing identified.
2. Current Indian price available.
3. Robotics-focused supplier.
4. ROBOTIS product identity is explicit.
5. Better traceability than substituting an unspecified servo.
6. Suitable for the current reference hand architecture.

**Procurement condition:** Obtain a dated quotation/invoice confirming:

* XL330-M288-T
* Quantity = 10
* Manufacturer = ROBOTIS
* MPN = XL330-M288-T
* GST
* Shipping
* Warranty
* Stock status
* Expected dispatch date

---

# 5. STM32G431 Controller

## Required Component

**Manufacturer:** STMicroelectronics
**Part family:** STM32G431
**Reference MCU:** STM32G431CBT6

The STM32G431CBT6 is listed by element14 India with current quantity pricing, including ₹762.01 at quantity 1 and lower unit pricing at larger quantities.

For prototype development, a development board can be used, but the development-board selection must not automatically be treated as the final production PCB.

---

## 5.1 STM32G431 MCU — Current Market Comparison

| Supplier            | Product          |                                         Current Price Evidence | Authenticity        | Assessment                                   |
| ------------------- | ---------------- | -------------------------------------------------------------: | ------------------- | -------------------------------------------- |
| **element14 India** | STM32G431CBT6    |                        ₹762.01 @ 1; ₹496.66 @ 10; ₹464.02 @ 25 | High                | **Preferred for production MCU procurement** |
| DigiKey India       | STM32G431 family |                    Quote / live listing required for exact MPN | High                | Backup                                       |
| Mouser India        | STM32G431 family | Current listing available; exact package/MPN must be confirmed | High                | Backup                                       |
| Evelta              | STM32G431CBT6    |                       Current listing/reference around ₹572.30 | Distributor listing | **Price-competitive backup**                 |

Current market search identifies an Evelta listing for STM32G431CBT6 around ₹572.30.

Mouser also carries STM32G431 development hardware and STM32G431-family components.

### MCU Selection

**Preferred:** element14 India

**Why:**

* Exact STM32G431CBT6 MPN is explicitly listed.
* Quantity pricing is available.
* Established electronics distributor.
* Better suitability for production BOM traceability than an unspecified development board.

### Backup

**Evelta**

Use as a price/availability comparison and request a formal quotation for the exact:

`STM32G431CBT6`

---

# 6. STM32G431 Development Board — Prototype

If a development board is required for firmware/integration testing before the production PCB is available:

| Supplier                   | Board                     |  Current Listed Price | Assessment                                |
| -------------------------- | ------------------------- | --------------------: | ----------------------------------------- |
| **Lofty Agrotech**         | WeAct STM32G431 Long Core |               ₹560.30 | **Preferred prototype board**             |
| Robu / Indian distributors | WeAct STM32G431 family    | ~₹559–₹600 range seen | Backup                                    |
| DigiKey                    | NUCLEO-G431RB             |             ₹2,039.04 | Higher-cost official development platform |
| IndustryBuying             | NUCLEO-G431RB             |                ₹2,713 | Backup                                    |

The WeAct STM32G431 Long Core listing is currently around ₹560.30.

The NUCLEO-G431RB is available through DigiKey India at approximately ₹2,039.04 in the current product results.

### Decision

For **low-cost prototype development:**

**Preferred:** WeAct STM32G431 Long Core

For **official ST development/debugging:**

**Preferred:** ST NUCLEO-G431RB

For the production BOM, however, use the **exact approved MCU/PCB design**, not the development board.

---

# 7. MPU-6050 IMU Module

## Required Component

**Part:** MPU-6050 6-axis accelerometer + gyroscope module
**Application:** Humanoid body IMU / development validation

The MPU-6050 is a low-cost sensor, so price is not the only selection criterion. Module quality, breakout-board implementation and sensor authenticity must be checked.

---

## Current Market Comparison

| Supplier          | Current Listed Price | Stock / Listing  | Price Score | Risk       | Assessment                    |
| ----------------- | -------------------: | ---------------- | ----------: | ---------- | ----------------------------- |
| **ElectroPi**     |          **₹136.80** | Listed           |         5/5 | Medium     | **Preferred low-cost source** |
| Quartz Components |             **₹127** | Listed           |         5/5 | Medium     | Price winner                  |
| Robu.in           |             **₹151** | Listed           |         5/5 | Low/Medium | **Preferred balanced source** |
| Robocraze         |             **₹154** | Listed           |         5/5 | Low/Medium | Backup                        |
| Robokits          |             **₹173** | Listed           |         4/5 | Low/Medium | Backup                        |
| FlyRobo           |             **₹218** | In-stock listing |         3/5 | Medium     | Backup                        |

Current product results show approximately ₹127 from Quartz Components, ₹136.80 from ElectroPi, ₹151 from Robu, ₹154 from Robocraze and ₹173 from Robokits.

FlyRobo currently lists an MPU-6050 module at ₹218 and indicates stock.

### Selection

**Preferred procurement source:** Robu.in

**Reason:**

The lowest price is not automatically the best choice. The difference between ₹127 and ₹151 is only ₹24, while the project benefits from a more established robotics/electronics procurement trail.

**Price winner:** Quartz Components

**Backup:** Robocraze

### Procurement rule

Before purchase, verify:

* MPU-6050 marking
* Board version
* Supply voltage
* I²C address
* Connector orientation
* Mounting-hole pattern
* Datasheet/source documentation
* Quantity
* GST
* Shipping

---

# 8. 24 V → 5 V DC-DC Converter

## Requirement

The humanoid reference architecture requires regulated low-voltage electronics power.

The converter must **not be selected by voltage alone**. Current capacity, thermal performance, input range, efficiency, isolation requirement and transient behaviour must be verified against the final electronics load.

---

## Current Market Comparison

| Supplier / Listing | Converter                           |  Current Price |     Current Capacity | Assessment                                            |
| ------------------ | ----------------------------------- | -------------: | -------------------: | ----------------------------------------------------- |
| **Robu.in**        | XY-3606 24/12 V → 5 V               |       **₹131** |          5 A listing | **Preferred low-cost candidate**                      |
| Ktron              | XY-3606                             |           ₹125 |          5 A listing | Price winner                                          |
| Robocraze          | XY-3606                             |           ₹159 |          5 A listing | Backup                                                |
| Nelsotech          | 5 V 3 A DC-DC                       |           ₹449 |                  3 A | Higher cost / lower current                           |
| Mouser             | Industrial/regulated DC-DC families | Quote required | Depends on exact MPN | **Preferred for production-grade design if required** |

Current product results show approximately ₹125 from Ktron, ₹131 from Robu, ₹159 from Robocraze, and ₹449 for a 5 V/3 A module from Nelsotech.

Mouser maintains a dedicated 24 V/5 V DC-DC converter selection, but the exact converter must be selected against the required current, isolation and environmental specification.

### Decision

For **prototype bench integration:**

**Preferred:** Robu XY-3606 candidate

**Price winner:** Ktron XY-3606

For **production / safety-critical electronics power:**

Do **not** freeze the generic XY-3606 automatically.

Select a manufacturer-specific DC-DC converter after confirming:

* Input voltage range
* Continuous output current
* Peak current
* Isolation/non-isolation
* Efficiency
* Thermal derating
* Short-circuit protection
* Over-voltage protection
* Over-current protection
* EMI behaviour
* Datasheet
* Manufacturer traceability

---

# 9. Consolidated Supplier Scorecard

| Supplier              | Exact MPN | Authenticity | Price | Availability | Documentation | Support |   Overall | Decision                            |
| --------------------- | --------: | -----------: | ----: | -----------: | ------------: | ------: | --------: | ----------------------------------- |
| **MG Super Labs**     |         5 |            4 |     4 |            4 |             4 |       4 | **4.3/5** | **Preferred for XL330**             |
| **element14 India**   |         5 |            5 |     4 |            5 |             5 |       5 | **4.8/5** | **Preferred for STM32 MCU**         |
| **DigiKey India**     |         5 |            5 |     3 |            5 |             5 |       5 | **4.6/5** | Backup / production electronics     |
| **Mouser India**      |         5 |            5 |     3 |            5 |             5 |       5 | **4.6/5** | Backup / production electronics     |
| **Robu.in**           |         4 |            4 |     5 |            5 |             4 |       4 | **4.4/5** | **Preferred for prototype modules** |
| **Robocraze**         |         4 |            4 |     5 |            4 |             4 |       4 | **4.2/5** | Backup                              |
| **Evelta**            |         5 |            4 |     5 |            4 |             4 |       4 | **4.4/5** | Strong STM32 backup                 |
| **Robokits**          |         4 |            4 |     4 |            4 |             4 |       4 | **4.0/5** | Backup                              |
| **ElectroPi**         |         3 |            3 |     5 |            4 |             3 |       3 | **3.6/5** | MPU6050 price candidate             |
| **Quartz Components** |         3 |            3 |     5 |            4 |             3 |       3 | **3.6/5** | MPU6050 price winner                |

---

# 10. Final Supplier Selection

## 10.1 Recommended Procurement Allocation

| Component                       | Preferred Supplier                            | Backup Supplier                  | Selection Reason                           |
| ------------------------------- | --------------------------------------------- | -------------------------------- | ------------------------------------------ |
| **DYNAMIXEL XL330-M288-T**      | **MG Super Labs**                             | ROBOTIS / alternate quote source | Exact robotics MPN + current India listing |
| **STM32G431CBT6 MCU**           | **element14 India**                           | Evelta / DigiKey / Mouser        | Exact MPN + distributor traceability       |
| **STM32G431 development board** | **Lofty Agrotech / WeAct**                    | DigiKey ST NUCLEO                | Lower-cost prototype development           |
| **MPU-6050 module**             | **Robu.in**                                   | Robocraze                        | Good price/availability balance            |
| **24→5 V prototype DC-DC**      | **Robu.in**                                   | Ktron / Robocraze                | Current 5 A module listing                 |
| **Production-grade DC-DC**      | **Mouser / DigiKey / authorized distributor** | element14                        | Manufacturer-specific part required        |

---

# 11. 3-Quote Requirement Status

The project requires three supplier comparisons where reasonably available.

Current status:

| Component         | Quote 1              | Quote 2                   | Quote 3                       | Status                            |
| ----------------- | -------------------- | ------------------------- | ----------------------------- | --------------------------------- |
| XL330-M288-T      | MG Super Labs ₹3,659 | **Formal quote required** | **Formal quote required**     | **OPEN**                          |
| STM32G431CBT6     | element14 ₹762.01 @1 | Evelta ~₹572.30           | DigiKey/Mouser quote required | **PARTIAL**                       |
| MPU-6050 module   | Quartz ₹127          | ElectroPi ₹136.80         | Robu ₹151                     | **3-market references available** |
| 24→5 V 5 A module | Ktron ₹125           | Robu ₹131                 | Robocraze ₹159                | **3-market references available** |

### Important distinction

The above public prices should **not** be labelled as formal “3 supplier quotations” in the procurement record.

For final procurement closure, capture:

```text
Supplier
Quotation Number
Quotation Date
Manufacturer
MPN
Quantity
Unit Price
GST
Shipping
Landed Cost
Stock
Lead Time
Warranty
Datasheet
Payment Terms
Validity
Evidence Link / PDF
```

---

# 12. Landed-Cost Selection Rule

The final supplier must not be selected using unit price alone.

Use:

```text
Landed Cost =
(Unit Price × Quantity)
+ GST
+ Shipping
+ Other Supplier Charges
```

Then evaluate:

```text
Procurement Value =
Specification Match
+ Authenticity
+ Availability
+ Lead Time
+ Documentation
+ Warranty
+ Landed Cost
```

The lowest price should only win when the specification and supplier-risk criteria are equivalent.

---

# 13. Procurement Decision Gates

Before purchase, each selected line item must pass:

### Gate 1 — Part Identity

* Manufacturer confirmed
* Exact MPN confirmed
* Datasheet available
* No uncontrolled substitute

### Gate 2 — Interface Compatibility

* Voltage confirmed
* Current confirmed
* Communication interface confirmed
* Connector confirmed
* Mechanical envelope confirmed
* Mounting/interface dependency checked

### Gate 3 — Supplier Evidence

* Supplier identified
* Current price captured
* Stock captured
* Lead time captured
* Quote/invoice captured
* Warranty/return conditions captured

### Gate 4 — Approval

* Mechanical dependency checked
* Electronics dependency checked
* Dhruv/electronics owner confirmation obtained where applicable
* Arya procurement decision recorded
* Revision linked to BOM

---

# 14. Current Recommended Purchase List

For the currently identified electronics/actuator requirements:

| Item                  | Qty | Recommended Source |      Current Market Reference | Procurement Status                                   |
| --------------------- | --: | ------------------ | ----------------------------: | ---------------------------------------------------- |
| XL330-M288-T          |  10 | MG Super Labs      |                   ₹3,659 each | **Quote required before purchase**                   |
| STM32G431CBT6         | TBD | element14          | ₹762.01 @1; lower at quantity | **Confirm production requirement**                   |
| WeAct STM32G431 board |   1 | Lofty Agrotech     |                       ₹560.30 | **Prototype candidate**                              |
| MPU-6050 module       |   1 | Robu               |                          ₹151 | **Prototype candidate**                              |
| 24→5 V 5 A converter  |   1 | Robu               |                          ₹131 | **Prototype candidate / electrical review required** |

---

# 15. Final Recommendation

### Preferred procurement strategy

**Tier 1 — Critical / exact components**

Use established distributors or exact robotics suppliers:

* **XL330-M288-T → MG Super Labs**
* **STM32G431CBT6 → element14**
* Production-grade DC-DC → **Mouser / DigiKey / element14 after exact MPN selection**

### Tier 2 — Low-cost prototype modules

Use:

* **Robu**
* **Robocraze**
* **Robokits**

provided the module specification and physical interface are verified.

### Tier 3 — Price-only alternatives

Quartz Components, ElectroPi and similar low-cost sources may be used for non-critical prototype modules when:

* the exact specification is verified,
* quantity is small,
* the component is not safety-critical,
* and the supplier evidence is retained.

---

# 16. Final Selection Status

| Component                   | Final Decision                                   | Confidence |
| --------------------------- | ------------------------------------------------ | ---------- |
| XL330-M288-T                | **MG Super Labs — preferred**                    | High       |
| STM32G431CBT6               | **element14 — preferred**                        | High       |
| STM32G431 development board | **WeAct / Lofty Agrotech — prototype preferred** | Medium     |
| MPU-6050 module             | **Robu — preferred balanced source**             | Medium     |
| 24→5 V converter            | **Robu — prototype candidate only**              | Medium     |
| Production DC-DC            | **NOT FROZEN — exact MPN/requirements required** | Low        |

---

## 17. Evidence Status

### Public market evidence captured

* Current XL330-M288-T listing from MG Super Labs.
* Current STM32G431CBT6 pricing from element14.
* Current WeAct STM32G431 development-board pricing.
* Current MPU-6050 market prices across multiple Indian suppliers.
* Current 24→5 V converter market prices across multiple suppliers.
* ROBOTIS manufacturer reference for XL330-M288-T.

### Still required before procurement closure

1. Three formal quotes for XL330-M288-T.
2. Three formal quotes for STM32G431CBT6 where commercially practical.
3. Formal landed-cost comparison.
4. Exact DC-DC converter MPN and electrical requirements.
5. Supplier quote PDFs / invoices.
6. Stock and lead-time confirmation on the purchase date.
7. Final approval linked to the corresponding BOM revision.

**Document conclusion:**
The current market evidence supports **MG Super Labs for XL330-M288-T, element14 for STM32G431CBT6, and Robu as a balanced source for prototype modules**. These are procurement recommendations based on currently visible market evidence, not fabricated supplier quotations. Final procurement closure requires dated supplier quote evidence.

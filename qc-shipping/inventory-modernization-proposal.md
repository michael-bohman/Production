---
description: 'Owner: James'
---

# Inventory Modernization Proposal

**Purpose:** Build a roadmap to centralize inventory, purchasing, receiving, and shipping while improving accuracy, traceability, and scalability for drone production operations.

## Summary

Current inventory receiving relies on manual counting and SOS data entry without barcode validation. Shipping operations are performed through separate UPS and FedEx applications, creating duplicate effort and limited visibility.

A phased approach is recommended: standardize processes, implement WMS and centralized shipping, then integrate to ERP (unless John Deere wants otherwise).

## Current State Challenges

* Manual receiving and counting
* No barcode scanning
* Similar-looking drone components
* Supplier short-ships and over-ships
* Inventory discrepancies
* Separate UPS/FedEx shipping systems
* Limited reporting and traceability

## Problem Statement

Manual inventory and shipping processes increase the risk of receiving errors, inventory inaccuracies, misidentified parts, duplicate data entry, and limited shipment visibility.

## Goal Statement

Centralized multi-carrier shipping, supplier variance tracking, and ERP integration (John Deere may decide this).

{% stepper %}
{% step %}
## Phase 1: Standardize & Stabilize

* Standard receiving procedures
* Location management
* Cycle counts
* Supplier discrepancy log
* Inventory labeling standards
{% endstep %}

{% step %}
## Phase 2: WMS + Centralized Shipping

* Barcode receiving
* Inventory locations
* Put-away tracking
* Scanning
* Cycle counting
* Multi-carrier shipping platform
* Centralized tracking
* Export documentation management
{% endstep %}

{% step %}
## Phase 3: ERP Integration

Centralize purchasing, inventory, receiving, shipping, vendor management, analytics and reporting into a single enterprise platform.
{% endstep %}
{% endstepper %}

## Potential Software Options

| Category     | Software               | Typical Fit                   | Estimated Cost Range |
| ------------ | ---------------------- | ----------------------------- | -------------------- |
| WMS          | Fishbowl               | Mid-size inventory            | $595/mo (Advanced )  |
| WMS          | Cin7 Core              | Inventory and warehouse       | $349 – $999          |
| Shipping/TMS | 2Ship                  | Multi-carrier parcel shipping | \$$                  |
| Shipping/TMS | ProShip                | Enterprise shipping           | \$$$                 |
| ERP          | Microsoft Dynamics 365 | Enterprise integration        | \$$$-\$$\$$          |
| ERP          | NetSuite               | Cloud ERP                     | \$$$                 |
| ERP          | Acumatica              | Mid-market ERP                | \$$$                 |

## Expected Benefits

* 98%+ inventory accuracy target
* Reduced receiving errors
* Supplier performance visibility
* Reduced manual entry
* Centralized shipping analytics
* ERP readiness

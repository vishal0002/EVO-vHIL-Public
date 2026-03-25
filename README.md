# EVO vHIL — EV Powertrain Architecture & Validation Framework  
**by Vishal (vishal0002)**

This repository contains the architecture and system design for **EVO vHIL**, a virtual Hardware-in-the-Loop (vHIL) platform for validating high-voltage EV powertrains without reliance on physical hardware test benches.

---

## Overview

EVO vHIL enables full-stack validation of EV systems, including:

- Dual-pack battery architecture (84S HV + independent 4S LV)
- Production-intent BMS firmware (C / RTOS)
- Android Automotive VCU safety daemon
- Virtual CAN communication bridge
- SPI-based CCS fast charging integration (ISO 15118)

---

## Design Philosophy

EVO vHIL is built on a core principle:

> **The control system must remain operational under traction system failure.**

By decoupling the low-voltage (LV) control domain from the high-voltage (HV) traction system, the platform ensures:

- Continued execution of control logic during HV faults  
- Deterministic fault handling and logging  
- Controlled, graceful system shutdown  

---

## Scope & Disclosure

This repository documents the system at an architectural and interface level.

Certain subsystems — including LV energy management, safety control logic, and CCS charging control — are intentionally described in terms of externally observable guarantees rather than internal implementation.

This preserves proprietary design while ensuring that:

- Safety-critical behavior is explicit  
- System invariants are verifiable  
- Integration boundaries are clearly defined  

---

## Repository Scope

This repository contains:

- System architecture  
- Interface definitions  
- Validation approach  

It does **not** include:

- Firmware source code  
- Safety logic implementation  
- Hardware design details  

---

## Explore the Full Architecture

👉 [View the full white paper](https://evovhil.com/)

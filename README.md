# EVO vHIL — EV Powertrain Architecture & Validation Framework

This repository contains the architecture and system design for **EVO vHIL**, a virtual Hardware-in-the-Loop (vHIL) platform for validating high-voltage EV powertrains.

## Overview

EVO vHIL enables full-stack validation of EV systems including:

- Dual-pack battery architecture (84S HV + independent 4S LV)
- Production-intent BMS firmware (C / RTOS)
- Android Automotive VCU daemon
- Virtual CAN communication bridge
- SPI-based CCS fast charging integration (ISO 15118)

## Scope & Disclosure

This document describes the EVO architecture at a system and interface level.  
Certain subsystems — including LV energy management and CCS charging control — are intentionally documented using externally observable guarantees rather than internal implementation details.

This approach preserves proprietary design elements while ensuring that all safety-critical behaviors and system-level invariants are clearly defined.

## Note

This repository contains architecture-level documentation only.  
Implementation details, control logic, and system tuning are intentionally omitted.

## Explore the Full Architecture

👉 [View the white paper](./index.md)
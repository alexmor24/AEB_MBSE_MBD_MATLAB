# 1. Scope and Assumptions  
Automatic Emergency Braking (AEB) System  
MBSE & Model-Based Design Project

---

## 1.1 Purpose

The purpose of this document is to define the scope and assumptions of the
Automatic Emergency Braking (AEB) system developed in this project.

This project aims to demonstrate a complete Model-Based Systems Engineering
(MBSE) and Model-Based Design (MBD) workflow, from system definition and
requirements to control modeling and verification through simulation using
MATLAB and Simulink.

---

## 1.2 System Overview

The AEB system is an advanced driver assistance function designed to
automatically apply braking in order to avoid or mitigate rear-end collisions
with a vehicle ahead.

The system monitors the driving environment, evaluates collision risk, warns
the driver when necessary, and autonomously applies braking if the driver does
not react in time.

---

## 1.3 System Scope

The scope of the AEB system in this project is intentionally limited to allow
clear focus on requirements engineering, system behavior modeling, and
simulation-based verification.

### In Scope
- Longitudinal vehicle motion only
- Straight-line driving scenarios
- Single lead vehicle directly ahead of the ego vehicle
- Forward collision warning (FCW)
- Partial and full autonomous braking
- Driver brake override
- Closed-loop simulation with a simplified vehicle dynamics model

### Out of Scope
- Lateral vehicle control (steering, lane keeping)
- Multiple objects or cut-in scenarios
- Pedestrian or cyclist detection
- Detailed sensor physics (radar or camera modeling)
- Road friction variations (e.g., wet or icy roads)
- Interaction with other ADAS functions (ACC, LKA, etc.)

---

## 1.4 Operational Concept

The AEB system operates under the following high-level concept:

1. The system continuously monitors the relative distance and relative velocity
   between the ego vehicle and a lead vehicle.
2. The system calculates a collision risk metric based on Time-To-Collision (TTC).
3. If the collision risk exceeds predefined thresholds:
   - A visual or audible warning is issued to the driver.
   - Autonomous braking is applied if the driver does not react.
4. The driver may override autonomous braking by applying the brake pedal.

---

## 1.5 Assumptions

The following assumptions are made to simplify modeling and simulation while
preserving realistic system behavior.

### Environment Assumptions
- The road is flat and straight.
- Road surface is dry with constant friction.
- Visibility conditions are ideal.

### Sensor and Perception Assumptions
- The lead vehicle is always correctly detected and classified.
- Relative distance and relative velocity measurements are available without noise.
- Sensor latency is neglected.

### Vehicle Dynamics Assumptions
- Vehicle mass is constant.
- Brake system response is instantaneous.
- Longitudinal dynamics are modeled using a simplified point-mass model.

### Driver Assumptions
- The driver is attentive but may react late.
- Driver braking input overrides autonomous braking.

---

## 1.6 Constraints

- The system is intended for simulation and demonstration purposes only.
- No compliance with production-level safety standards is claimed.
- Parameter values are representative but not tied to a specific vehicle platform.

---

## 1.7 Document Status

This document represents the initial scope definition for the AEB MBSE/MBD
project and may be updated as system requirements and architecture are refined.

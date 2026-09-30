# Smart-museum-Artifact-conservation
SV&amp;V lab5 Smart-museum-Artifact-conservation system


# Smart Museum Artifact Conservation System

## Overview

This repository contains the requirements and operation schemas for a Smart Museum Artifact Conservation System.

The system monitors environmental conditions and protects valuable historical artifacts by controlling temperature, humidity, light exposure, vibration, chamber door status, artifact condition, and power availability.

## Tasks

### Task 1 — Identify Operations

The system operations were extracted from the conservation chamber scenario.

A total of 22 operations were identified.

Examples include:

- Perform System Self-Check
- Record Artifact Information
- Load Environmental Profile
- Monitor Environmental Conditions
- Correct Temperature
- Verify Temperature Recovery
- Correct Humidity
- Verify Humidity Recovery
- Activate Protection Measures
- Generate Operator Alert
- Verify Safe Conditions
- Perform Safe Shutdown

### Task 2 — Complete Operation Schema

Each operation is documented using:

- Operation ID
- Operation Name
- Trigger
- Preconditions
- Inputs
- Processing
- Outputs
- Postconditions
- Exceptions

## Repository Structure

```text
Smart-Museum-Artifact-Conservation/
│
├── README.md
│
├── Operations/
│   └── Artifact_Conservation_Operations.md
│
└── Schemas/
    └── Operation_Schema.md

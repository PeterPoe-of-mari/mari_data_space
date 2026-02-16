---
name: "P2: Action Observer (LLM)"
about: "Observation of data actions and normalization into event JSON"
title: "[P2] Action Observer: Deterministic Core + Optional LLM Plugin"
labels: ["p2","events","observer","index-prep"]
---

# [P2] Action Observer  
## Deterministic Core + Optional LLM Plugin

### Goal

Design and implementation of the **Action Observer** between:

Demolition Engine → Order Engine → Index Writer

The Action Observer documents what data **does**.

It:
- does not modify Values
- does not modify Order metadata
- does not write Index entries
- does not apply norms

It produces normalized **Observation Events**.

### Components

1. **Observer Core (deterministic)**
2. **Optional LLM Plugin (extended pattern recognition)**

The core is rule-based and append-only.

---
name: "P3: Mari Index Writer"
about: "Experience-driven writer of the Mari Index"
title: "[P3] Mari Index Writer: Experience-Based Memory Committer"
labels: ["p3","index","llm","core"]
---

# [P3] Mari Index Writer  
## Experience-Based Memory Committer

---

## Goal

The **Mari Index Writer** is one of the two equal LLM core programs within the Mari Data Space.

Its mission:

> Translate observations into historicized memory entries.

It writes the Mari Index in an append-only manner and is the **only program with commit rights to the Index Store**.

---

## Role in the System

Demolition Engine  
→ Order Engine  
→ Action Observer  
→ **Index Writer**  
→ Index Store  

The Writer collaborates with the **Index Interpreter**, but receives no commit instructions from it.

---

## Inputs

1. **Observation Events** (from the Action Observer)  
2. **Interpreter Memory Bundles** (experience context for the current action)

Memory Bundles may contain:
- relevant Value IDs / Index IDs
- dominant primitives
- reference candidates (`ref`)
- stability/repetition indicators
- confidence values

These provide context — not commands.

---

## Core Principle

Observation Event  
+ Experience Context (Interpreter)  
→ Primitive Hypothesis (LLM)  
→ Marker Enrichment  
→ Append-only Index Entry  

Index format:

<IndexID> : <ValueRef> <PRIMITIVE> <ValueRef?> | <Marker*>

---

## Properties

- Append-only
- Primitive whitelist enforced
- Marker whitelist enforced
- No free-text fields
- No normative statements
- Mandatory LLM versioning

---

## Learning Mechanism

Quality emerges through:

- Repetition (`*`)
- Stabilization (`#`)
- Referencing (`ref`)
- Deviation (`!`)
- Aggregation (`⊕`)
- Hierarchical superordination (Überordnung)

The Writer historicizes hypotheses.  
Corrections occur only through new entries.

---

## Interface (Minimal)

process_events(events, memory_bundle) -> List[IndexEntry]

class IndexEntry:
    index_id: str
    value_refs: list
    primitive: str
    markers: dict
    created_at: datetime

---

## Acceptance Criteria

- [ ] Only the Writer can commit to the Index
- [ ] Append-only behavior enforced
- [ ] Memory Bundle context is considered
- [ ] Primitive and Marker whitelists enforced
- [ ] No free text in the Index
- [ ] Replayable via (events + memory + model version)

---

## Strategic Significance

The Writer makes experience persistent.

It writes memory —  
not as absolute truth,  
but as historicized hypothesis.

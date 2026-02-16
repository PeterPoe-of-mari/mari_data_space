---
name: "P4: Mari Index Interpreter"
about: "Equal twin of the Index Writer: memory reader and projection builder"
title: "[P4] Mari Index Interpreter: Projection & Experience Companion"
labels: ["p4","index","llm","core","projections"]
---

# [P4] Mari Index Interpreter  
## Projection & Experience Companion

---

## Goal

The **Mari Index Interpreter** is the second equal LLM core program alongside the Index Writer.

Guiding idea:

> The Writer writes memory.  
> The Interpreter lives within it.

The Interpreter operates independently of the Writer and is primarily responsible for:

- Projections
- Memory aggregation
- Context construction
- Providing raw projection data to the Communicator

---

## Role in the System

### Memory Path
→ Index Writer → Index Store

### Usage Path
User Request  
→ Communicator  
→ **Index Interpreter**  
→ Projection Artifact  
→ Communicator  

The Interpreter can operate independently of the Writer at any time.

---

## Core Responsibilities

### 1) Projection Builder

Generates structured **Projection Artifacts** from:

- Value Store (read-only)
- Order Layer (read-only)
- Index Store (read-only)

It collects relevant memory signals for:
- Answers
- Explanations
- Views
- Planning

---

### 2) Experience Context Provider

During ongoing indexing operations, it produces:

**Memory Bundles** for the Writer:

- dominant primitives
- repetition patterns
- reference candidates
- stability indicators
- confidence levels

These bundles provide context — not commit instructions.

---

### 3) Optional: Interpretation Hints (append-only)

The Interpreter may write structured hints:

- suggest_ref
- suggest_marker
- suggest_delay_aggregation
- suggest_hierarchy (hierarchical superordination)

Hints are optional and non-binding.

---

## Projection Artifact Schema (Minimal)

{
  "projection_id": "P-...",
  "value_ids": [...],
  "index_ids": [...],
  "dominant_primitives": [...],
  "signals": [...],
  "confidence": 0.82,
  "version": {"model": "...", "prompt": "..."}
}

No normative statements.  
No Index mutations.

---

## Properties

- Fully read-only on Value/Order/Index
- Operable independently of the Writer
- LLM-native interpretation of the Index language
- Versioned and replayable

---

## Acceptance Criteria

- [ ] Can operate without the Writer
- [ ] Projection Artifacts are structured and versioned
- [ ] Memory Bundles available for Writer
- [ ] No direct Index mutation
- [ ] Supports hierarchical superordination in projections

---

## Strategic Significance

The Interpreter makes memory usable.

It aggregates experience for projections  
and provides context for new memory entries.

Two equal programs.  
One shared memory space.

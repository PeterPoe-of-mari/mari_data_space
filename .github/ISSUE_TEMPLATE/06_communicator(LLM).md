---
name: "P5: Mari Communicator"
about: "Normative LLM layer: user interaction, law integration, controlled output"
title: "[P5] Mari Communicator: Normative Interface & Decision Layer"
labels: ["p5","llm","interface","code-of-law","projections"]
---

# [P5] Mari Communicator  
## Normative Interface & Decision Layer

---

## Goal

The **Mari Communicator** is the third LLM core program in the Mari Data Space.

It acts as the interface between:

- Humans / APIs / external systems  
and  
- the internal memory space (Value, Order, Index)

Guiding idea:

> The Communicator does not decide about memory.  
> It decides about usage.

---

## Role in the System

### Memory Formation
Demolition → Order → Observer → Index Writer

### Projection
User → Communicator → Index Interpreter → Projection Artifact → Communicator

### Normative Application
Communicator → Code of Law → Final Response / Action

---

## Core Responsibilities

### 1) Intent Parsing

- Analyze user requests
- Classify intent:
  - answer
  - explain
  - view
  - plan
  - execute (optional)
- Extract scope parameters

---

### 2) Request Projection

The Communicator sends structured requests to the **Index Interpreter**.

Input:
- Intent
- Scope
- Constraints

Output:
- Projection Artifact (structured raw data)

---

### 3) Code of Law Application (Normative Layer)

The Communicator is the only LLM module that interacts with the **Code of Law**.

It validates:

- Access restrictions
- Roles / permissions
- Data protection classes
- Allowed actions
- Compliance rules

The Code of Law acts as:
- Filter
- Validator
- Decision logic

The Communicator may:
- Deny responses
- Anonymize data
- Block actions
- Provide compliance explanations

---

### 4) Response Generation

Transforms the Projection Artifact into:

- Structured API response
- UI view
- Explanatory answer
- Action instruction

This is the only layer where free natural language generation is permitted.

---

## Inputs

- User Request
- Projection Artifact (from Interpreter)
- Code of Law
- Role/context information

---

## Outputs

- Final User Response
- Optional System Action
- Audit Log (documented normative decision)

---

## Guardrails

The Communicator may:

- Make normative statements
- Take decisions
- Deny access
- Generate free text

The Communicator may not:

- Write to the Index
- Mutate Values
- Modify Order metadata
- Define new primitives

---

## Interface (Minimal)

handle_request(user_input) -> Response

class Response:
    content: str
    structured_data: dict | None
    decision_log: dict
    confidence: float
    version: {"model": "...", "prompt": "..."}

---

## Acceptance Criteria

- [ ] Code of Law integration mandatory
- [ ] Access control enforced
- [ ] No direct Index mutation
- [ ] Projection Artifact treated as read-only
- [ ] Audit log for normative decisions
- [ ] Model + prompt versioning

---

## Strategic Significance

The Communicator is the normative surface of the system.

Writer writes memory.  
Interpreter makes memory usable.  
Communicator decides what may be spoken or executed.

Memory remains pure.  
Norms remain explicit.

# Mari Data Space

This repository describes the **Mari Data Space**: the layered architecture and formal information levels
through which classical information systems (ERP, administration, production, documents) can be transformed
into a shared, AI-centered semantic space — without requiring the source systems to be unified.

**Core Idea:** Interoperability is not an interface problem, but a property of a shared,
open, machine-native structural layering.

The Mari Data Space strictly separates:

1. **Value Store** – raw, atomic values (append-only)
2. **Mari Index Language** – machine-native memory (append-only; separate repository)
3. **Code of Law** – normative rules of the human domain (project-specific, explicit)
4. **Order Layer (Order Metadata)** – human-readable origin/structure (optional, coexisting)
5. **Projections** – context-dependent views/responses (derivable, ephemeral)

This repository contains the **structural specification** of the Mari Data Space.
Reference implementations belong in a separate repository (`mari-engine`).

---

## Quick Start

- Architecture Overview: `01_Architecture/01_Layer_Model.md`
- Value Store: `01_Architecture/03_Value_Format.md`
- Order Layer: `01_Architecture/04_Order_File_Schema.md`
- Code of Law: `01_Architecture/05_Code_of_Law_Schema.md`
- Projections: `01_Architecture/06_Projection_Contract.md`

---

## Prioritized Development Issues (Program Components)

See: `.github/ISSUE_TEMPLATE/`.

---

## License

Specification & Documentation: **CC BY 4.0** (see `LICENSE.md`).  
Implementation code belongs in `mari-engine` and is licensed separately.

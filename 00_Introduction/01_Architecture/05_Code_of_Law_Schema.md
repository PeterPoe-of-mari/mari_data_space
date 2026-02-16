# Code of Law (Schema)

The Code of Law represents the **normative layer** of the human domain.
It defines rights, obligations, prohibitions, validation rules, and justification requirements.

## Minimal Schema (YAML)
```yaml
version: 0.1
scope: "erp_demo"
rules:
  - id: GB-001
    title: "Allergen labeling must be present"
    applies_to:
      entity: "Article"
    condition: "Article.allergen_list == null OR Article.allergen_list == ''"
    severity: "high"
    action: "raise_question"
    rationale: "Food labeling regulation"
```

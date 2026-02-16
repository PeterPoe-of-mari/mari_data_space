# Order File (Schema)

Order metadata describes **where** a Value originates and **how** it is structured within a source system.
It defines **no meaning** and **no norms**.

A Value can have 0..n Order Files (multiple systems/views may coexist).

## Minimal Schema (JSON)
```json
{
  "value_id": "V-...",
  "source_system": "erp_demo",
  "source_type": "table_cell",
  "path": {
    "table": "Article",
    "row_key": "article_id=1001",
    "column": "description"
  },
  "relations": {
    "foreign_keys": [
      {"from": "Article.supplier_id", "to": "Supplier.id", "type": "fk"}
    ]
  },
  "observed_at": "2026-02-15T10:00:00Z"
}
```

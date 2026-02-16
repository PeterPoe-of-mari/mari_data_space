# Value Format (Specification)

A **Value** is a raw, atomic fact (e.g., a table cell, JSON leaf node).

## Minimal JSON Record
```json
{
  "value_id": "V-01HZY...",
  "payload": "Gouda Cheese 48%",
  "payload_type": "string",
  "created_at": "2026-02-15T10:00:00Z"
}
```

Origin/order information does not belong in the Value itself, 
but in separate Order Files.

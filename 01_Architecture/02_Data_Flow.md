# Data Flow (from Source System to Mari)

1. Extraction → atomic values
2. Storage → Value Store (append-only)
3. Order → 0..n order files per value
4. Observation → actions/events (Insert/Update/Delete/Import)
5. Indexing → index entries (Mari Index Language) for events
6. Projection → response to user queries (Index + Order + Code of Law)

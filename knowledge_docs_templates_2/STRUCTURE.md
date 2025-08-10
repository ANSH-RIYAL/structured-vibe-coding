# STRUCTURE

## Directory Layout (Immutable Skeleton)
```
Auto-Graph/
├── src/
│   ├── parser/
│   ├── analyzer/
│   ├── llm_integration/
│   ├── graph_builder/
│   ├── export/
│   ├── visualization/
│   ├── agent_detection/
│   ├── models/
│   ├── utils/
│   └── web/
├── examples/
├── graph/
├── cache/
└── logs/
```

## Layer Responsibilities
- **/parser**: AST/symbol parsing.
- **/analyzer**: Pipeline coordination.
- **/llm_integration**: Single LLM client, prompts, retries, caching.
- **/graph_builder**: HLD/LLD construction and metadata.
- **/export**: Multi-format export.
- **/visualization**: Graph visualizer helpers.
- **/agent_detection**: Pattern-based detection; no ML.
- **/web**: Flask app, endpoints, static/templates.
- **/models**: Pydantic/dataclasses for requests/responses/graph.
- **/utils**: File IO, logging.

## Immutable Interface Contracts
- **JSON shape**: `{ success, data, error }`.
- **Endpoints**:
  - POST `/api/analysis/upload` (multipart)
  - GET  `/api/analysis/<id>/status`
  - GET  `/api/analysis/<id>/result`
  - GET  `/api/analysis/<id>/export?format=...`
- **Status fields**: `analysis_id, status, progress, stage, estimated_completion`.
- **Export formats**: `json,yaml,csv,dot,html,mermaid`.

## Golden Artifacts
- Location: `examples/sample_graphs/`.
- Purpose: Manual debug baseline; compare node/edge counts and metadata keys.
- Tolerance: counts within ±5% unless otherwise specified.


# REALITY_CHECKS

## Canonical Payloads
- Request: multipart upload with `analysis_options.include_ai_detection` and `export_formats`.
- Status: `{ success, data: { analysis_id, status, progress, stage, estimated_completion }, error }`.
- Result: graph object with `metadata, nodes[], edges[]` and simple `statistics`.

## Golden Samples
- Location: `examples/sample_graphs/`.
- Check: total_nodes, total_edges, hld_nodes, lld_nodes within ±5% of golden.
- Action: If outside tolerance, run Minimal Debug Ritual and note in Decision Log.

## Edge Cases (Short List)
- Invalid upload (empty/corrupted zip) → 400 with helpful error.
- LLM unavailable → AST-only partial results; set `stage: "fallback_ast"`.
- Very large codebase → degrade to file-level summary; keep UI responsive.

## Debug-First Checks
- Prefer manual checks and logs during development.
- Formal tests can come later; keep payloads and golden samples up to date.


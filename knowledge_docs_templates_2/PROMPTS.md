# PROMPTS

## Canonical System Prompts

### Cursor (Backend)
- **Goal**: Implement or edit code in `src/` to satisfy endpoint and pipeline requirements.
- **Respect**: Invariants in `FOUNDATION.md` and contracts in `STRUCTURE.md`.
- **Do Not**: Rename endpoints/dirs, introduce DB/auth/WebSockets/queues, change JSON schema.
- **Outputs**: Edits only; keep code readable; include imports; preserve existing style.
- **Fallback**: If LLM unavailable, ensure AST-only path works and set `stage` accordingly.

### Replit (Frontend)
- **Goal**: Single-page upload → progress → results → export UI.
- **Respect**: Endpoint paths and JSON schema.
- **Do Not**: Add frameworks or auth; keep plain HTML/CSS/JS.
- **Outputs**: Accessible UI; graceful errors; no renames of IDs/paths.

### ChatGPT (Docs/Prompts)
- **Goal**: Keep docs skimmable; update Decision Log when choices change.
- **Respect**: Invariants; avoid proposing out-of-scope tech.
- **Outputs**: Minimal edits with clear bullets; no large rewrites.

## Prompt Variables
- `codebase_path`, `analysis_id`, `model_name`, `budget_tokens`, `cache_key`, `failure_policy`.

## Anti-Patterns (Avoid)
- Renaming endpoints or directories.
- Adding authentication/databases/WebSockets/queues.
- Changing `{ success, data, error }` response shape.
- Long-running chains that ignore cost ceilings.


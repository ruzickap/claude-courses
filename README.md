# Claude Courses Notes

## Environment Setup

Dependencies are declared in `pyproject.toml` and pinned in `uv.lock`. One
command creates the `.venv` at the **workspace root** (next to `.vscode/`) and
installs everything. VS Code then auto-selects it for all notebooks — no kernel
prompt.

```bash
# Run from the workspace root (claude-courses/)
uv sync
```

Open any `*.ipynb` — VS Code picks up `.venv` automatically via
`.vscode/settings.json` (`python.defaultInterpreterPath`) and the recommended
Python + Jupyter extensions in `.vscode/extensions.json`.

### Notes

- Keep secrets in `.env` (for example `ANTHROPIC_API_KEY`), not in notebook
  cells.
- Prefer managing dependencies outside notebooks for reproducibility.

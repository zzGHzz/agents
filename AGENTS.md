# Repository Guidelines

## Project Structure & Module Organization
- Root contains one agent per file (`*.md`) using lowercase kebab-case (e.g., `backend-architect.md`).
- `.github/` holds community docs and templates; `examples/` contains usage/examples (e.g., `examples/tdd-usage.md`).
- There is no application code, package manifest, or build system in this repository.

## Build, Test, and Development Commands
- No build step is required; this is a Markdown-only repo.
- Optional local checks (use if available):
  - `markdownlint '**/*.md'` — lint Markdown formatting.
  - `rg 'TODO|FIXME' -n` — surface unresolved notes.
  - `prettier -w "**/*.md"` — format Markdown consistently.

## Coding Style & Naming Conventions
- Filenames: lowercase kebab-case with `.md` extension.
- Headings: use Title Case for `#`/`##`; keep hierarchy shallow and logical.
- Bullets: `-` for lists; keep items concise; prefer one idea per line.
- Code blocks: fenced with language (e.g., ```bash, ```json) when relevant.
- Writing: clear, actionable, and current; aim for <120 characters per line.

## Testing Guidelines
- Validate links and anchors in changed files; preview Markdown locally before submitting.
- Verify shell commands in examples run as written (use minimal, copy-pastable snippets).
- For new agents, include: purpose, capabilities, model selection, usage examples, and safety considerations.
- When adding an agent, link it from `README.md` in the appropriate category table.

## Commit & Pull Request Guidelines
- Prefer Conventional Commits:
  - `feat(agent): add ui-visual-validator`
  - `docs(readme): update model distribution`
  - `chore: tidy formatting across agents`
- PRs should include: clear description, scope of change, linked issue, and before/after snippets if applicable.
- Keep PRs focused and small; avoid drive-by unrelated edits.

## Security & Content Quality
- Do not include secrets, credentials, or sensitive data in examples.
- Cite sources when including standards or external guidance; respect licensing.
- Ensure examples are safe, non-destructive, and production-minded.

## Adding a New Agent (Checklist)
- Create `new-agent-name.md` with consistent sections and model.
- Provide 2–4 concrete usage examples.
- Update `README.md` tables with the new agent and description.

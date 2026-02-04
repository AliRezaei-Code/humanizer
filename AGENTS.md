# AGENTS.md

This file guides agentic coding assistants working in this repository.
The repo is a Claude Code skill implemented entirely in Markdown.

## Repository overview
- Primary artifact: `SKILL.md` (YAML frontmatter + skill prompt).
- Human-facing docs: `README.md` (install, usage, summary table).
- Guidance: `WARP.md` (how this repo works).

## Commands (build/lint/test)
There are no build, lint, typecheck, or test scripts in this repo.
No `package.json`, `Makefile`, or CI configs are present.

Single-test execution:
- Not applicable (no automated tests in this repository).

If you add tooling later, update this section with exact commands.

## Manual validation checklist
Use these checks instead of build/test until tooling is added:
- `SKILL.md` YAML frontmatter is valid and correctly delimited by `---`.
- `SKILL.md` and `README.md` stay consistent on version and content changes.
- Numbered pattern lists remain stable unless intentionally renumbered.
- Markdown tables render correctly (alignment and pipes intact).
- No curly quotes or emoji are introduced in text that should be plain ASCII.

## Source of truth and file responsibilities
- `SKILL.md` is the canonical skill definition and must be updated first.
- `README.md` is a summary and should reflect `SKILL.md` changes.
- `WARP.md` documents repo usage; update if workflow changes.

When changing behavior/content, update `SKILL.md` first, then sync `README.md`.

## Versioning rules
- `SKILL.md` has a `version:` field in YAML frontmatter.
- `README.md` has a "Version History" section.
- If you bump the version, update both files in the same change.

## YAML frontmatter rules (SKILL.md)
- Keep the opening and closing `---` lines intact.
- Use two-space indentation for nested fields (e.g., `allowed-tools`).
- Keep keys in a stable, readable order (name, version, description, allowed-tools).
- Do not add non-ASCII characters in YAML unless already present.

## Markdown style guidelines
Follow the style of the file you are editing:
- `README.md` uses standard Title Case headings for top-level sections.
- `SKILL.md` uses uppercase section headers and numbered subsections.

General Markdown rules:
- Use straight quotes (") rather than curly quotes.
- Avoid emoji in documentation unless an example explicitly requires it.
- Keep lists tight and avoid excessive bolding.
- Use fenced code blocks with a language tag when possible.
- Preserve existing line breaks in long examples unless rewriting the example.

## Content and writing conventions
- Avoid chatbot artifacts ("I hope this helps", "Let me know").
- Prefer concrete facts over vague claims in examples.
- Keep headings sentence case unless the file already uses another style.
- Do not add promotional or hype language to examples.

## Editing patterns and tables
- Keep the 1-24 pattern numbering stable across files.
- If a pattern is added/removed, update every place it appears.
- In `README.md`, keep the pattern table in sync with `SKILL.md`.
- If you change a pattern example, update both before/after blocks.

## Allowed tools (Claude Code skill metadata)
- The `allowed-tools` list in `SKILL.md` is part of the skill contract.
- If you change allowed tools, explain why in the version history.

## Common tasks and tips
- Installing the skill locally:
  - `mkdir -p ~/.claude/skills`
  - `git clone https://github.com/blader/humanizer.git ~/.claude/skills/humanizer`
- Updating only the skill file:
  - `mkdir -p ~/.claude/skills/humanizer`
  - `cp SKILL.md ~/.claude/skills/humanizer/`
- Running in Claude Code:
  - Invoke `/humanizer` and paste input text.

## Consistency checks when editing
- If you edit `SKILL.md`, scan `README.md` for mismatches.
- If you edit `README.md`, confirm it reflects the current skill behavior.
- If you edit `WARP.md`, ensure it matches the repo layout.

## Cursor or Copilot rules
- No `.cursor/rules/` or `.cursorrules` files found.
- No `.github/copilot-instructions.md` found.

## Scope and safety
- This repo is Markdown-only; avoid adding code unless requested.
- Keep changes minimal and focused on the requested behavior.
- Do not introduce new dependencies or tooling without explicit request.

## Quick reference
- Canonical content: `SKILL.md`
- Summary and install docs: `README.md`
- Repo guidance: `WARP.md`

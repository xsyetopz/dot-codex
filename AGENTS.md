# AGENTS.md

## Shared worktree

- Preserve untracked files, unrelated modifications, and pre-staged paths.
- Treat unclear ownership as user-owned.
- Stage or commit only the explicitly requested slice.
- Before staging or committing, verify the index with `git diff --cached --name-only`.
- Do not use `git restore`, `git restore --staged`, `git reset`, `git checkout --`, `git clean`, or broad `rm` on user-owned state.

## Repository scope

- Read broadly when needed for behavior, parity, ownership, or risk.
- Write only files covered by the current explicit request.
- Modifying READMEs, docs, tools, configs, or assets requires explicit request or repository proof.
- Preserve legacy parity unless the user explicitly asks for redesign.

## Tools

- Use `rg` for search.
- Use `rtk` when available.
- Reuse existing helpers, shims, scripts, and conventions when repository evidence supports them.

## Evidence

- Repository evidence outranks convention.
- Missing evidence is `UNKNOWN: Cannot verify.`
- Builds and tests are evidence, not proof of correctness.
- Report blocked or skipped validation as uncertainty.

## Output

- Answer first.
- Use semantic Markdown: backticks for files, commands, states; tables for mappings; fenced blocks for exact formats.
- Keep output short and technical.

Mutation reports must end exactly with:

```text
CHANGED:
    <files modified, created, or deleted>
CHECKED:
    <validation performed>
BLOCKED:
    <unverified behavior or assumptions>
```

@/Users/krystian/.codex/RTK.md

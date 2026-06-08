# AGENTS.md

Role: Repository-local rules for Codex agents in this worktree. These rules define local scope, parity, staging, AND reuse expectations.

# Personality
Terse engineering communication. No filler.

# Goal
Keep repository changes literal, narrow, reusable, AND verifiable.

# Success criteria
- Parity work is treated as parity, NOT redesign.
- Test helpers AND compatibility shims have one shared owner when project structure supports it.
- Staged paths match the requested commit slice.
- Validation gaps are reported as uncertainty.

# Constraints
- Prefer `rg` AND `rg --files`.
- For parity commits, stage only requested parity source, parity tests, directly required project/build references, AND matched source deletions.
- Do NOT include docs, tools, scripts, plans, formatting churn, OR unrelated config in a parity commit unless the user explicitly includes them.
- Before creating a duplicate helper, shim, fixture, utility, project, abstraction, generated file, OR support file, search for an existing owner. Reuse, link, move, OR extend that owner when the repository structure supports it.
- Prefer linked/shared compile items for cross-project test compatibility helpers when available.
- Treat untracked files AND unrelated modifications as user-owned.
- Before committing, verify `git diff --cached --name-only` contains only the intended slice.
- Passing builds/tests are evidence, NOT proof of parity OR user acceptance.

# Output
For mutation tasks, final reports end exactly with:

```text
changed: <files modified, created, OR deleted>
checked: <commands, files, systems, OR tests evaluated>
uncertain: <unverified behavior, missing evidence, OR assumptions>
```

@~/.codex/RTK.md

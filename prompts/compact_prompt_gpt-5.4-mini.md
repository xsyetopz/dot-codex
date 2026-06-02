1. Task
Compress the conversation history into a strict, mechanical state summary for a GPT-5.4-mini session.

2. Critical rule
Preserve explicit user constraints, boundaries, and corrections exactly. Do not soften, summarize away, or reinterpret them.

3. Exact step order
1. Extract user constraints, boundaries, and corrections.
2. Extract files explicitly mutated, created, deleted, or replaced.
3. Extract outcomes mechanically verified by commands, files, tests, tools, runtime observation, or direct source checks.
4. Extract pending tasks as literal directives.
5. Extract unknowns, assumptions, and blocked items.
6. Remove filler, apologies, rationalizations, intent-verbs, psychological explanations, advice, and proposals.
7. Output only the required ledger.

4. Edge cases or clarification behavior
- If a claimed completion lacks evidence, place it under `Unknowns / blocked items`.
- If a user correction contains literal wording, keep the literal wording.
- If a status is not explicitly established, do not invent it.
- If a future task is not explicitly requested, do not add it.

5. Output format
Return exactly these sections:
- User constraints
- Mutated files
- Verified outcomes
- Pending directives
- Unknowns / blocked items

After `Unknowns / blocked items`, output nothing further.

6. One correct example
Input: `Are you skipping part of the requested parity by using "minimal" as objective?`
Output under `User constraints`: `"Are you skipping part of the requested parity by using "minimal" as objective?" => Do not mark or present partial parity as complete.`

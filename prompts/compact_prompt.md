Compress the conversation into a strict mechanical state summary.

Preserve:
- Explicit user constraints, corrections, and boundaries using the user's literal words where important.
- Current objective.
- Completed actions.
- Files modified, created, deleted, or inspected.
- Commands/tests/checks run and their outcomes.
- Verified facts.
- Unknowns, assumptions, and unresolved risks.
- Pending tasks as literal directives, not suggestions.

Remove:
- Apologies.
- Conversational filler.
- Rationalizations.
- Intent verbs such as "tried", "wanted", "aimed", "decided", or "prioritized".
- Coaching, advice, proposals, and next steps unless explicitly requested by the user.
- Claims of completion without evidence.

Format:
Objective:
<literal active task>

User constraints:
- <constraint>

State:
- <fact>

Files:
- changed: <file or none>
- inspected: <file or none>

Verification:
- <command/check>: <outcome>

Pending:
- <literal directive or none>

Unknown:
- <unknown or none>

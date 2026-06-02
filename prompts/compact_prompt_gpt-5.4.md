<task>
Compress the conversation history into a strict, mechanical state summary for a GPT-5.4 session.
</task>

<output_contract>
Return exactly these sections, in this order:
1. User constraints
2. Mutated files
3. Verified outcomes
4. Pending directives
5. Unknowns / blocked items
After section 5, output nothing further.
</output_contract>

<grounding_rules>
- Preserve explicit user constraints, boundaries, and corrections exactly, using the user's literal words where they matter.
- List only files that were explicitly mutated, created, deleted, or replaced.
- List only outcomes that were mechanically verified by commands, files, tests, tools, runtime observation, or direct source checks.
- Preserve pending tasks as literal directives.
- Separate verified facts, direct inferences, assumptions, unknowns, and blocked items.
</grounding_rules>

<verbosity_controls>
- Use a cold, factual ledger.
- Strip conversational filler, apologies, rationalizations, intent-verbs, and psychological explanations.
- Do not explain why mistakes happened unless the conversation contains a verified mechanical cause.
</verbosity_controls>

<verification_loop>
Before finalizing:
- Check that no user correction has been softened or paraphrased into a weaker rule.
- Check that no completion, verification, or file mutation is claimed without evidence.
- Check that no proposal, advice, next step, or implementation plan was added.
</verification_loop>

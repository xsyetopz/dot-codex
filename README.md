# .codex

Usually, GPT models inherit one-or-many of these issues:

- Infers unstated intent; answers inferred requests over literal ones.
- Converts complaints into advice, corrections into new artifacts, and "this is wrong" into "here is a better prompt/version."
- Generates content after useful answers are complete; adds unwanted structure, workflows, framing, examples, caveats, safety rails, best practices, and next steps.
- Fills silence with transitions, rationales, implementation advice, or rewritten prompts.
- Optimizes for complete-looking or generic responses over bounded, user-controlled ones.
- Treats user frustration/anger as a process-design request or ambiguity to resolve.
- Treats negative feedback or rejected artifacts as prompts to generate more text.
- Acknowledges boundaries/mistakes but immediately crosses them or repeats the error.
- Uses tidy, abstract wording to hide boundary violations or distance itself from mistakes.
- Makes users repeatedly correct the same assumptions, police boundaries, and undo invented constraints.
- Acts like a teacher, negotiator, project manager, or coach instead of an exact tool.
- Overclaims problems as fixed, verified, confirmed, or resolved without evidence.
- Understates missing evidence; fails to say "unknown" or "cannot verify."
- Uses confident language for inferences; fails to mark inferences clearly or separate source-grounded conclusions from guesses.
- Equates mechanical success (build passes, tests pass) with user acceptance and bug resolution, ignoring visual correctness or runtime observation.
- Treats uncertainty as something to smooth over; treats plausible causality as evidence.
- Ignores programming context; treats debugging like documentation.
- Treats legacy code/parity as a vague improvement target rather than a strict acceptance criterion.
- Restricts investigation scope based on edit scope, treating file names as hard boundaries; treats "avoid unrelated edits" as "avoid reading related code."
- Suppresses relevant search paths; treats previous edits as sunk cost to defend.
- Acts like a code janitor instead of a code investigator; assumes current code premises are worth preserving.
- Compresses complex user intent into convenient model-shaped tasks; substitutes helpfulness/productivity for obedience/correctness.
- Quotes users loosely instead of exactly; claims users asked for unrequested actions or premises.
- Answers how to fix it or what the rule is instead of why it happened or who asked.
- Creates extra burden, review work, diff noise, conceptual noise, and correction loops.
- Generates outputs the user must prune; creates unauthorized tasks or restrictions that block investigation.
- Adds unrequested formatting, structures, and titles even when corrected, repeating the exact behavior under review.

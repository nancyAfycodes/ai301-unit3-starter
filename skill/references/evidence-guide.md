# Evidence guide: where evidence lives in a plan package

## Diagnosis
Where it lives: The plan's section describing the root cause (may be titled "Root Cause," "Problem," "Analysis," etc.), compared against the issue's reproduced evidence.

What good looks like: The plan identifies the same root cause shown in the repro evidence. 
The cause is stated at the level of mechanism: "X causes Y" not "Y is broken."

## Scope
Where it lives: The section describing what will and won't change (may be titled "Scope," "Changes," "What I'll Do," etc.).

What good looks like: The plan limits changes to the minimum needed. No extra refactoring or feature scope creep.

## Executability
Where it lives: The section with step-by-step instructions (may be titled "Implementation Steps," "How to Fix It," "Changes," etc.).

What good looks like: Steps are specific enough for someone to follow: file names, line numbers, or exact locations.

## Test plan
Where it lives: The section showing how to verify the fix works (may be titled "Testing," "Verification," "How to Test," "Expected Results," etc.).

What good looks like: Shows how to verify the fix—includes a test command or observation, and states what success looks like.

## Honesty
Where it lives: Any section documenting unknowns, risks, or limitations (may be titled "Unknowns," "Risks," "Caveats," "Notes," etc.).

What good looks like: Plan acknowledges what it doesn't know; doesn't hide difficult or uncertain parts.

## Comms
Where it lives: The plan comment posted on the GitHub issue.

What good looks like: Language is clear, specific, and professional. Matches the repo's contribution style.
# Rubric: is this plan ready to post and build from


## Checks

| Check | Evidence | Pass condition | Weight |
|---|---|---|---|
| Diagnosis matches evidence | Plan's stated cause + repro report's conclusion | Plan correctly names the same root cause shown in the repro evidence (8-space indent causing code block parsing) | required |
| Scope is bounded | Plan's scope/change section | Plan describes only the minimum changes needed to fix the root cause; no scope creep or extra refactoring | required |
| Fix targets cause, not symptom | Plan's fix steps + repro evidence | Plan addresses the root cause, not just a workaround or surface-level fix | required |
| Steps are executable | Plan's implementation steps | Steps are numbered, specific, and a stranger could execute them without re-reading the issue | required |
| Test plan is concrete | Plan's testing/verification section | Plan specifies the exact command to run and what success looks like (e.g., "test passes with output X"), not vague ("it works") | required |
| No hidden unknowns | Plan text | Plan acknowledges uncertainties or what it doesn't know; doesn't hide or hand-wave difficult parts | preferred |

## Verdict rule

Accept if: All required checks pass.
Reject if: Any required check fails.
Unclear: Treat as fail and reject.
Preferred checks never change the verdict.
# Rubric: is this plan ready to post and build from


## Checks

| Check | Evidence | Pass condition | Weight |
|---|---|---|---|
| Diagnosis matches evidence | Plan's stated cause compared to reproduced evidence | Plan correctly names the same root cause shown in the repro evidence on the issue thread | required |
| Scope is bounded | Plan's scope/change section | Plan describes only the minimum changes needed to fix the root cause; no scope creep or extra refactoring | required |
| Fix targets cause, not symptom | Plan's fix steps + repro evidence | Plan addresses the root cause, not just a workaround or surface-level fix | required |
| Steps are executable | Plan's implementation steps | Steps describe concrete actions that someone could follow; not vague or missing key details | required |
| Test command specified | Plan's testing/verification section | Plan includes the exact test command with flags and test node ID (e.g., `pytest tests/unit/test_foo.py::TestClass::test_method -v`) | required |
| Expected output stated | Plan's testing/verification section | Plan names the specific expected output or behavior after the fix (e.g., "test passes with PASSED [100%]"), not generic language like "it works" | required |
| Professional tone | Plan comment text | Language is specific and clear, matches the repo's contribution style | required |
| No excessive emoji | Plan comment text | Emoji use is minimal or absent | preferred |
| No hidden unknowns | Plan text | Plan acknowledges uncertainties or what it doesn't know; doesn't hide or hand-wave difficult parts | preferred |

## Verdict rule

Accept if: All required checks pass.
Reject if: Any required check fails.
Unclear: Treat as fail and reject.
Preferred checks never change the verdict.
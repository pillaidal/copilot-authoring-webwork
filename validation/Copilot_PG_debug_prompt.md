# Copilot Prompt: Debug a WeBWorK PG Problem

Attach `WeBWorK_PG_Copilot_Instructions.md`, the affected `.pg` file, and paste the WeBWorK error.

Use this prompt:

```text
Read and follow the attached WeBWorK PG authoring instructions.

Diagnose this problem as a production WeBWorK PG file. Do not patch only the reported line. Audit the whole file for related failures.

Perform this review in order:
1. PG syntax and loaded macros.
2. Variables defined before use.
3. PGML syntax and interpolation.
4. Answer evaluators and appropriate tolerances.
5. RadioButtons exact answer/choice matches.
6. Randomization edge cases and degenerate values.
7. Independent recalculation of every graded mathematical answer.
8. Consistency between displayed rounded data and the answer key.
9. ANS(...) registration for each input.
10. Applicable mathematical invariants.

ERROR FROM WEBWORK:
[paste error here]

Return:
- the root cause;
- any additional issues discovered;
- the corrected complete PG file;
- a short list of checks I should run in WeBWorK.
```

# Start Here: Creating WeBWorK Problems with Microsoft Copilot

This toolkit lets an instructor or teaching assistant start a fresh Copilot conversation and create new WeBWorK PG problems without needing access to the conversations used to develop the toolkit.

The resources incorporate lessons from the migration and modernization of STAT 1060, STAT 2060, and STAT 2080 problems, together with new problem development and testing for upper-level Statistics.

## Files to provide to Copilot

When starting a new WeBWorK authoring conversation, upload these three files:

1. `WeBWorK_PG_Copilot_Instructions.md`
2. `filelist.txt` 
3. `pg_macro_index.txt`

Optional but useful:

4. `WeBWorK_PG_Authoring_Guide.docx`
5. One existing `.pg` example similar to the problem you want to create

### Why provide `filelist.txt`?

`filelist.txt` is an inventory of the static reference copy of the PG installation corresponding to the current Dalhousie WeBWorK environment.

Copilot may use the inventory to discover native PG macros, parsers, contexts, graphing tools, mathematical utilities, examples, and libraries that could be useful for your problem.

The current static PG reference is available at:

https://www.mathstat.dal.ca/downloads/copilot-for-webwork/pg2.20/

You normally do **not** need to upload the complete PG source tree. If Copilot discovers a specialized macro whose API it needs to inspect, retrieve that individual file, supporting library, or example from the static PG reference and provide it to Copilot.

The static PG reference is authoring documentation only. It is not used by the production WeBWorK server.

## Start the conversation

After uploading the files, tell Copilot:

> Read and follow the attached WeBWorK PG authoring instructions throughout this conversation. Use the supplied PG file inventory to identify native WeBWorK capabilities when useful. Create a complete PG file ready for testing from the problem idea below.

## Quick-start prompt

Copy this prompt and fill in whatever you know. You may omit fields that are not relevant.

```text
Read and follow the attached WeBWorK PG authoring instructions throughout this conversation.

Use filelist.txt to discover native PG functionality when the requested problem may benefit from a specialized parser, context, graphing tool, answer evaluator, or other macro. Do not invent an undocumented specialized API. If a promising macro is found but its usage is unclear, tell me which file from the static PG reference you need me to provide.

COURSE:

TOPIC:

LEARNING OBJECTIVE:
What should the student demonstrate?

PROBLEM IDEA:
Describe it informally. I do not need to know PG or Perl syntax.

DIFFICULTY:
introductory / intermediate / advanced

QUESTION STYLE:
numerical / symbolic / multiple choice / multiple select / graphical / multipart

RANDOMIZATION:
What should vary between students, if known?

CONSTRAINTS:
Notation, methods, values, rounding, units, course conventions, or other requirements.

OUTPUT:
Create a complete `.pg` file ready for testing in WeBWorK.

Before finalizing:
- derive answers from the displayed randomized values;
- check invalid or degenerate random cases;
- verify answer evaluators and tolerances;
- verify every RadioButtons correct answer exactly matches a listed choice;
- verify mathematical identities and invariants;
- verify all ANS(...) registrations;
- sanity-check multiple randomized branches;
- use native PG capabilities when appropriate;
- do not use deprecated macros for new problems;
- do not use R/Rserve unless I explicitly request it and there is a compelling reason;
- briefly list important assumptions after the code.
```

## Example: Mathematics

```text
Read and follow the attached WeBWorK PG authoring instructions.

Course: first-year calculus
Topic: chain rule
Learning objective: differentiate a composite function containing two nested layers.
Problem idea: students should differentiate a function like (a+bx^2)^n and evaluate the derivative at a clean point.
Difficulty: intermediate
Question style: multipart symbolic/numerical
Randomization: coefficients and exponent should vary, but arithmetic should remain manageable.
Constraints: mathematically equivalent symbolic answers must be accepted. No external services.
Output: complete .pg file ready for testing.
```

## Example: Statistics

```text
Read and follow the attached WeBWorK PG authoring instructions.

Course: STAT 2080
Topic: matched-pairs t inference
Learning objective: recognize pairing and perform inference on within-subject differences.
Problem idea: before-and-after measurements.
Difficulty: intermediate
Question style: multipart
Randomization: randomized displayed data.
Constraints: define D = After - Before. Include hypotheses, D-bar, sD, SE, df, t statistic, confidence interval, decision, and interpretation. Calculate answers from displayed data.
Output: complete .pg file ready for testing.
```

## When Copilot generates the file

AI-generated PG must be tested before it is assigned to students.

1. Save the source as a `.pg` file.
2. Test it in the appropriate WeBWorK course.
3. Generate and inspect several randomized versions.
4. Test correct answers and representative incorrect answers.
5. Check mathematical/statistical correctness independently.
6. Check notation, units, tables, graphics, and rounding.
7. Check hardcopy/PDF rendering if the course uses hardcopy.

A generated problem becomes production-ready only after successful local testing.

## If WeBWorK reports an error

Provide Copilot with the complete PG file and the exact error or warning.

```text
Use the attached WeBWorK PG authoring standards.

Diagnose this as a production WeBWorK problem. Do not patch only the reported line. Review the whole file for related issues and return the corrected complete PG file.

ERROR FROM WEBWORK:
[paste the exact error here]
```

If the error involves a specialized macro or supporting PG class, Copilot should use `filelist.txt` to identify the relevant local PG source and ask you to provide that specific reference file if necessary.

## If the problem runs but the answer appears wrong

```text
Audit this PG problem independently. Recalculate every graded answer from the values shown to students, verify all mathematical identities and randomization constraints, check rounding and sign conventions, and list any discrepancies before returning corrected code.
```

## Important note about native PG capabilities

The Dalhousie PG installation contains substantially more functionality than the small set of macros commonly seen in introductory examples. Native facilities include specialized answer parsers, mathematical contexts, tables, statistical functions, 2D and 3D graphing, interactive graphing, units, matrices and vectors, proof-oriented interactions, differential-equation tools, and discrete-mathematics utilities.

Copilot should prefer an appropriate native PG facility when it is known and locally supported rather than recreating the feature manually.

`filelist.txt` exists so that less-common capabilities can be discovered when needed.

## Important note about R / Rserve

R support exists in the WeBWorK environment, but live R/Rserve usage is strongly discouraged for ordinary problem authoring.

Do **not** explicitly request R merely because the problem is statistical. Describe the statistical task instead and allow Copilot to use native PG, MathObjects, and WeBWorK graphing/statistics facilities.

Native PG should be preferred for routine calculations, randomization, data generation, simulations of modest complexity, and graphics whenever reasonably practical.

If a problem genuinely appears to require live R execution, the dependency should be identified explicitly and discussed with the WeBWorK administrator.

## Problem brief for instructors assigning development to a TA

```text
WEBWORK PROBLEM BRIEF

Course:
Topic:
Learning outcome:

Student should be able to:

Problem idea/context:

Expected solution method:

Methods students should not use, if any:

Randomized or fixed:

Desired difficulty:

Answer type:
[ ] Numerical
[ ] Symbolic
[ ] Multiple choice
[ ] Multiple select
[ ] Graphical
[ ] Multipart

Desired scaffolding:

Notation conventions:

Rounding conventions:

Units:

Other requirements:
```

## Recommended workflow

**Idea -> learning objective -> capability discovery -> mathematical design -> randomization constraints -> PG generation -> WeBWorK testing -> error/debug loop -> random-seed QA -> instructor approval -> publish**

The instructor or TA does not need to know PG syntax to begin. A clear learning objective and problem idea are enough for a useful first draft.

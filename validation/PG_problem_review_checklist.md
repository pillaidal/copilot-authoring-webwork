# PG Problem Review Checklist

## Mathematical design
- [ ] Learning objective is explicit.
- [ ] Randomization is generated from valid mathematical structure.
- [ ] No zero denominators, invalid domains, unintended repeated roots, zero variance, or ambiguous cases.
- [ ] Sign/difference conventions are explicit and consistent.

## Student display
- [ ] Students see every value required to solve the problem.
- [ ] Units and notation are clear.
- [ ] Display rounding matches what the answer key uses.
- [ ] Tables render correctly for unequal/dynamic sizes.

## Answer evaluation
- [ ] Correct MathObjects/context is used.
- [ ] Exact numerical answers use zero tolerance when appropriate.
- [ ] Rounded answers use a deliberate absolute tolerance.
- [ ] Symbolic equivalents are accepted where appropriate.
- [ ] Every RadioButtons correct answer exactly matches a listed choice.
- [ ] Multiple-select answers use an appropriate modern parser.
- [ ] Every student input is registered with ANS(...).

## Statistical checks when applicable
- [ ] P-values lie in [0,1].
- [ ] Confidence interval lower < upper.
- [ ] Correlation lies in [-1,1].
- [ ] One-way ANOVA SS and df decompositions hold.
- [ ] Two-way ANOVA SS and df decompositions hold.
- [ ] Regression SST = SSR + SSE and R-squared identities agree.
- [ ] Wilcoxon ties receive average ranks and variance is tie-corrected when required.
- [ ] Wording uses fail-to-reject rather than accept-H0.

## Randomization QA
- [ ] Several seeds/branches were tested.
- [ ] Conditional branches all define needed variables.
- [ ] No duplicate or nonsensical multiple-choice choices arise.
- [ ] No decision rests accidentally on a rounding boundary.

## Publication
- [ ] HTML rendering checked.
- [ ] Hardcopy/PDF checked if used in the course.
- [ ] File has a clear DESCRIPTION and metadata.
- [ ] Instructor has tested correct and common incorrect answers.

# WeBWorK PG Copilot Instructions

## Purpose

You are helping university instructors and teaching assistants create, review, debug, and improve WeBWorK PG problems for Mathematics and Statistics courses.

When the user gives a problem idea, turn it into a complete `.pg` file ready for testing in the local WeBWorK environment. Do not stop at pseudocode unless explicitly requested.

A generated PG file is **not production-ready until it has been tested successfully in the local WeBWorK installation across appropriate randomized versions**.

## Local PG reference

The author may provide `filelist.txt`, an inventory of the static reference copy of the PG installation used by the current Dalhousie WeBWorK environment.

Current static PG reference root:

https://www.mathstat.dal.ca/downloads/copilot-for-webwork/pg2.20/

Use this reference for capability discovery and version-specific implementation guidance.

The static source tree is reference material only. The production WeBWorK server does not depend on it.

## Capability-discovery rule

Before implementing specialized functionality manually:

1. Start from the mathematical or statistical learning objective.
2. Check whether an established native PG capability in this document matches the need.
3. If not, search the supplied `filelist.txt` for likely macros, contexts, parsers, utilities, tutorials, or supporting libraries.
4. Prefer files under locations such as:
   - `macros/parsers/`
   - `macros/contexts/`
   - `macros/math/`
   - `macros/graph/`
   - `macros/ui/`
   - `tutorial/`
5. If a promising specialized macro is identified but its API is unclear, do **not invent syntax**. Ask the user to provide the relevant local macro, POD documentation, sample problem, or supporting library from the static PG snapshot.
6. Prefer locally confirmed capabilities over assumptions derived from examples for other PG versions.
7. Do not use files under `macros/deprecated/` for newly authored problems.
8. If no specialized facility is required, use the simplest reliable PG/MathObjects implementation.

Valid Perl syntax is not automatically valid inside WeBWorK's restricted PG execution environment. Avoid assuming that arbitrary Perl operations are permitted. If a safe-compartment error occurs, redesign using supported PG constructs rather than trying to bypass the restriction.

## Core authoring principles

1. The displayed problem, mathematical model, derived quantities, and answer evaluators must share one source of truth.
2. Derive answers from randomized inputs. Do not independently hard-code derived answers.
3. If students calculate from rounded displayed data, normally round first and derive graded answers from those displayed values.
4. Randomize from the mathematical structure desired. Prefer generating valid solutions, parameters, or model characteristics first and deriving coefficients/data from them.
5. Explicitly define sign conventions such as `B-A`, `After-Before`, or `x2-x1`, and use them consistently.
6. Use MathObjects evaluators so mathematically equivalent answers are accepted when appropriate.
7. Use deliberate tolerances: zero for exact integer/count answers and absolute tolerances matched to requested rounding for numerical answers.
8. Define dynamic RadioButtons answer strings once and reuse the exact strings in the available choices.
9. Prefer native PG, MathObjects, PGML, parsers, contexts, and graphing facilities over unnecessary custom code or external computation.
10. Perform mathematical, statistical, and randomized consistency checks before finalizing.
11. Test several randomized versions in the actual WeBWorK installation before publication.

## Preferred baseline file structure

```perl
## DESCRIPTION
## ...
## ENDDESCRIPTION

## DBsubject(...)
## DBchapter(...)
## Level(...)

DOCUMENT();

loadMacros(
    "PGstandard.pl",
    "MathObjects.pl",
    "PGML.pl",
    "PGcourse.pl"
);

Context("Numeric");

# 1. Randomized parameters
# 2. Derived quantities
# 3. Answer evaluators
# 4. Choice / interaction objects
# 5. Tables / graphs / display structures

BEGIN_PGML
...
END_PGML

ANS(...);

ENDDOCUMENT();
```

Load additional macros only when needed.

## Native PG capabilities known to be available

The installed PG environment contains many native facilities. Use these as starting points and consult `filelist.txt` for additional capabilities.

### Core authoring

- `PGstandard.pl`
- `MathObjects.pl`
- `PGML.pl`
- `PGcourse.pl`

### Choices and structured responses

- `parserRadioButtons.pl` for single-choice radio questions.
- `parserCheckboxList.pl` for select-all-that-apply questions.
- `parserPopUp.pl` for dropdown selections.
- `parserMultiAnswer.pl` for coordinated multi-answer questions.
- `parserRadioMultiAnswer.pl` for radio selections combined with multiple answers.
- `parserOneOf.pl` for specialized one-of answer handling.
- `parserMultipleChoice.pl` and related parser facilities may be available for specialized choice designs; inspect local documentation before use.

### Tables and presentation

- `niceTables.pl` for `DataTable` and structured displays.
- `quickMatrixEntry.pl` for specialized matrix-entry interfaces; inspect the local API before use.
- `scaffold.pl` exists for structured/scaffolded problem designs; inspect local documentation before adopting it.

### Statistics

- `PGstatisticsmacros.pl` provides native statistical utility functions.
- `PGnauStats.pl` provides additional statistics functionality.
- `PGstatisticsGraphMacros.pl` provides native statistical graph functionality.

Prefer native PG for routine statistics calculations, datasets, and graphics when reasonably practical.

### Native 2D graphing

`PGgraphmacros.pl` provides WWPlot-based functions, points, labels, and graph images.

A locally validated PG 2.20 pattern for plotting a function is:

```perl
$graph = init_graph(
    $xmin,
    $ymin,
    $xmax,
    $ymax,
    axes => [0,0],
    grid => [6,5],
    size => [620,380]
);

$f = sub {
    my $x = shift;
    return ...;
};

$fun = new Fun($f,$graph);
$fun->color('blue');
$fun->weight(3);
$fun->steps(150);
```

Important local behavior: `new Fun($f,$graph)` installs the function in the graph and initializes its domain from the graph. Do not add the same function to the graph a second time.

To restrict the plotted function domain:

```perl
$fun->domain($left,$right);
```

Add a filled point with:

```perl
$graph->stamps(
    closed_circle($x,$y,'blue')
);
```

Add an open-circle marker with:

```perl
$graph->stamps(
    open_circle($x,$y,'red')
);
```

Add a label with the locally established `Label` pattern:

```perl
$graph->lb(
    new Label(
        $x,
        $y,
        'Label',
        'blue',
        'left'
    )
);
```

Display a WWPlot graph with:

```perl
[@ image(
    insertGraph($graph),
    width=>620,
    height=>380
) @]*
```

For `init_graph`, `grid => [xdiv,ydiv]` specifies numbers of grid divisions, not coordinate step sizes.

Do not invent undocumented WWPlot method calls. In particular, do not assume that a standalone PG macro is also a method on the graph object.

### Interactive graphing and advanced graphics

Known graph-related facilities include:

- `parserGraphTool.pl`
- `PGstatisticsGraphMacros.pl`
- `plots.pl`
- `PGtikz.pl`
- `plotly3D.pl`
- `VectorField2D.pl`
- LiveGraphics 2D/3D-related macros

These are specialized facilities. Inspect their local source, POD, or examples before generating a problem that depends on their API.

### Algebra, equations, inequalities, and sets

Potentially relevant native facilities include:

- `parserSolutionFor.pl`
- `parserLinearInequality.pl`
- `parserLinearRelation.pl`
- `parserImplicitEquation.pl`
- `parserRoot.pl`
- `contextInequalities.pl`
- `contextInequalitySetBuilder.pl`
- `contextFiniteSolutionSets.pl`
- `contextPolynomialFactors.pl`
- `contextRationalFunction.pl`
- `contextRestrictedDomains.pl`

Prefer a suitable native parser/context to manual string comparison when the requested mathematical object has an established representation.

### Functions and calculus

Potentially relevant facilities include:

- `parserFunction.pl`
- `parserFunctionPrime.pl`
- `parserFormulaUpToConstant.pl`
- `parserDifferenceQuotient.pl`
- `parserPrime.pl`
- `PGdiffeqmacros.pl`
- `specialTrigValues.pl`

Use symbolic MathObjects evaluation for mathematically equivalent formulas whenever appropriate.

### Units and applied numerical answers

- `contextUnits.pl`
- `parserNumberWithUnits.pl`
- `parserFormulaWithUnits.pl`
- `MatrixUnits.pl`

Prefer native unit-aware evaluation rather than manually comparing answer strings containing units.

### Linear algebra and vectors

Known facilities include:

- `contextMatrixExtras.pl`
- `contextLimitedVector.pl`
- `PGmatrixmacros.pl`
- `PGmorematrixmacros.pl`
- `MatrixCheckers.pl`
- `VectorListCheckers.pl`
- `MatrixReduce.pl`
- `MatrixUnimodular.pl`
- `SystemsOfLinearEquationsProblemPCC.pl`
- `SolveLinearEquationPCC.pl`

Inspect the specialized local API or example before producing nontrivial matrix interactions.

### Proof and classification interactions

- `draggableProof.pl`
- `draggableSubsets.pl`

These can support richer interactive mathematics. Inspect local documentation/examples before use.

### Discrete mathematics and optimization

Known specialized facilities include:

- `PGnauGraphtheory.pl`
- `PGnauGraphCatalog.pl`
- `PGnauScheduling.pl`
- `PGnauBinpacking.pl`
- `LinearProgramming.pl`
- `tableau.pl`

Use only after inspecting the relevant local macro/example.

### Additional numerical and algebra utilities

Examples include:

- `PGnumericalmacros.pl`
- `PGpolynomialmacros.pl`
- `algebraMacros.pl`
- `interpMacros.pl`
- `fixedPrecision.pl`

Consult local documentation when these match the requested learning objective.

## Deprecated functionality

Do not use macros under:

```text
macros/deprecated/
```

for newly authored problems.

Internet examples may use deprecated WeBWorK macros. Prefer a modern facility confirmed by the local PG inventory.

## External computational services

### R / Rserve

`RserveClient.pl` exists in the PG installation, but live R/Rserve is strongly discouraged for ordinary problem authoring.

Do not choose R merely because the course is Statistics.

Prefer native PG/Perl/MathObjects for:

- routine statistical calculations;
- randomization;
- dataset generation;
- standard regression/ANOVA calculations;
- modest simulations;
- native statistical and mathematical graphics.

If the instructor explicitly requests R or a task genuinely appears to require live R execution:

1. Explain the dependency clearly.
2. Determine whether native PG can reasonably accomplish the learning objective first.
3. Treat live Rserve as an exceptional facility requiring administrator awareness/review.
4. Do not generate unnecessarily large simulations or HPC-like workloads.

### Sage

`sage.pl` exists but should not be used for new problems without explicit administrator approval and confirmation that the external service is configured and appropriate.

## Workflow: idea to PG

Before writing the final source, establish:

1. Learning objective.
2. Mathematical/statistical object being assessed.
3. Desired student reasoning workflow.
4. Appropriate native PG capability or parser.
5. Randomized inputs.
6. Constraints guaranteeing valid randomized versions.
7. Displayed quantities and rounding.
8. Derived correct answers.
9. Appropriate answer evaluator.
10. Relevant mathematical invariants.
11. Edge cases and safe-compartment concerns.
12. Local functionality requiring validation.

Then produce the complete `.pg` file.

## Constructive randomization

Do not choose arbitrary coefficients and hope they produce a pedagogically useful problem. Generate the mathematical structure first.

Example: a quadratic with guaranteed integer roots.

```perl
$r1 = non_zero_random(-6,6,1);
$r2 = non_zero_random(-6,6,1);
$b  = -($r1+$r2);
$c  = $r1*$r2;
```

Use the same principle for systems, derivatives, integrals, probability tables, dose-response models, regression examples, ANOVA designs, matrices, and other randomized questions.

## Prevent degenerate cases

Check for:

- zero or near-zero denominators;
- invalid logarithm or radical arguments;
- repeated roots when distinct roots are intended;
- zero variance;
- unintended singular matrices;
- duplicate/equivalent answer choices;
- impossible probabilities or counts;
- accidental ambiguity;
- empty arrays;
- boundary decisions caused by rounding;
- ties inconsistent with the intended statistical method;
- conditionally defined variables missing from some random branches.

## Displayed values and rounding

When students calculate from displayed values, normally round those values first and derive the answer afterward.

```perl
$x = sprintf("%.2f",$x) + 0;
# Calculate graded quantities from this displayed value.
```

Avoid hidden-precision answer keys when students only have rounded data unless the problem explicitly provides sufficient precision.

## Numerical evaluators

Exact integer/count answers:

```perl
$ans = Real($answer)->cmp(
    tolType   => 'absolute',
    tolerance => 0
);
```

Answers rounded to two decimal places commonly use:

```perl
$ans = Real($answer)->cmp(
    tolType   => 'absolute',
    tolerance => 0.005
);
```

Answers rounded to three decimal places commonly use `0.0005`.

Choose tolerance from the pedagogical precision requirement, not arbitrarily.

## RadioButtons

Define the correct string once and reuse the exact value:

```perl
$correct = "The samples are independent.";

$radio = RadioButtons(
    [
        $correct,
        "The samples are paired.",
        "The observations must be identical."
    ],
    $correct,
    labels => "ABC",
    displayLabels => 1
);
```

For dynamic questions, define every possible answer string first and assign the correct-answer variable to one of those exact strings.

The correct answer must textually match one of the available button values.

## Multiple-selection questions

Prefer `CheckboxList` for select-all-that-apply questions.

Use it when genuinely assessing a set of simultaneously correct statements rather than replacing several unrelated single-choice questions merely for compactness.

## PGML house style

Use PGML for problem prose and mathematics.

Inline mathematics:

```text
[`x^2+y^2=1`]
```

Display mathematics:

```text
[`
t
=
\frac{\bar X-\mu_0}{SE}.
`]
```

Answer box:

```text
[_________]{$ans}
```

Radio buttons:

```text
[_]{$radio}
```

Use headings and multipart structure that follow the student's reasoning process.

## Tables

Prefer `DataTable` from `niceTables.pl` for raw data, summaries, ANOVA tables, survival tables, calibration data, and other structured displays.

Generate table rows programmatically and deliberately format displayed numerical precision.

## Multipart design

Organize parts in the order a disciplined solution proceeds.

Statistics example:

```text
study design
-> hypotheses/model
-> summaries
-> standard error/model quantities
-> statistic/estimate
-> uncertainty
-> interpretation
```

Mathematics example:

```text
recognize structure
-> choose method
-> execute
-> verify
-> interpret/domain/check
```

Do not split questions merely for length. Each part should assess or scaffold a meaningful step.

## Statistical language standards

- Say **fail to reject the null hypothesis**, not **accept the null hypothesis**.
- A P-value is not the probability that the null hypothesis is true.
- A confidence level is a long-run property of the interval procedure.
- Statistical significance is not automatically practical or biological importance.
- Association or an adjusted regression model does not by itself establish causation.
- For one-way ANOVA, the alternative means not all population means are equal, not that every pair differs.
- Examine interaction before interpreting marginal main effects when interaction is important.
- For Wilcoxon rank-sum tests, formulate hypotheses appropriately for the method rather than automatically describing them as tests of population means.
- If tied ranks are used in a normal approximation, use an appropriate tie correction.
- In risk assessment, distinguish observed zero events from exact zero population risk.
- Distinguish risk ratio, odds ratio, and hazard ratio; they are not interchangeable.
- Distinguish model-derived benchmark/effective doses from guaranteed biological or regulatory thresholds.

## Useful statistical consistency checks

### Independent pooled two-sample t

```text
sp^2 = ((n1-1)s1^2 + (n2-1)s2^2)/(n1+n2-2)
SE = sp*sqrt(1/n1+1/n2)
df = n1+n2-2
```

### Matched pairs

Define the direction first, for example `D = After - Before`.

```text
t = Dbar/(sD/sqrt(n))
df = n-1
```

### Permutation tests

For a two-sided statistic:

```text
p = count(|T_perm| >= |T_obs|) / total allocations
```

### One-way ANOVA

```text
SST = SSTreatment + SSE
dfTreatment + dfError = dfTotal
F = MSTreatment/MSE
```

### Two-way ANOVA

```text
SSA + SSB + SSAB + SSE = SST
dfA + dfB + dfAB + dfE = dfTotal
```

### Regression

```text
SST = SSR + SSE
R^2 = SSR/SST = 1-SSE/SST
b1 = SSxy/SSxx
b0 = ybar-b1*xbar
```

### Logistic dose response

```text
logit(p) = beta0 + beta1*x
p = exp(eta)/(1+exp(eta))
ED_p = [log(p/(1-p))-beta0]/beta1
```

### Risk measures

```text
RD = R_exposed - R_reference
RR = R_exposed/R_reference
odds = p/(1-p)
OR = odds_exposed/odds_reference
```

### Kaplan-Meier

```text
S_hat(t) = product over event times of (1-d_i/n_i)
```

Censoring changes later risk sets but does not itself represent an event.

### Cox proportional hazards

```text
h(t|X) = h0(t)*exp(beta'X)
HR = exp(beta*DeltaX)
```

A hazard ratio is not the same quantity as a cumulative risk ratio.

## Mathematics authoring patterns

These principles apply equally to Mathematics courses.

### Algebra

Generate coefficients from desired roots/solutions when clean structure matters. Enforce domain restrictions for rational/logarithmic/radical expressions.

### Functions and precalculus

Generate compositions, inverses, domains, and ranges from valid structures. Use specialized contexts where appropriate.

### Calculus

Choose randomized functions that exercise the intended rule rather than accidental algebraic complexity. Generate tangent-line points and substitution structures constructively. Check domains.

### Linear algebra

Generate systems from known solutions and matrices from intended rank/determinant properties. Prevent randomization from changing the intended case.

### Probability

Generate internally consistent count/probability structures. Enforce nonnegative probabilities and required totals.

## Invariants and sanity checks

Before finalizing, verify all applicable identities and bounds, such as:

- `0 <= p <= 1`;
- confidence-interval lower endpoint < upper endpoint;
- `-1 <= r <= 1`;
- ANOVA SS and df decompositions;
- regression `SST = SSR + SSE`;
- permutation extreme count between zero and total allocations;
- generated roots satisfy the generated polynomial;
- matrix determinant/rank matches the intended case;
- effective-dose calculations reproduce the requested fitted probability;
- survival estimates stay in `[0,1]` and do not increase after events.

## Random-seed testing

A randomized problem is not complete because one rendering works.

Inspect several versions and every conditional branch. Look for invalid domains, degeneracies, duplicate choices, rounding-boundary decisions, malformed tables/graphs, and different answer logic across branches.

## Debugging workflow

When given a WeBWorK error, audit the whole file in this order:

1. PG syntax and loaded macros.
2. Variables defined before use.
3. PGML syntax and interpolation.
4. Answer objects and tolerances.
5. RadioButtons exact answer/choice matches.
6. Specialized macro API validity for the local PG version.
7. Safe-compartment restrictions.
8. Randomization edge cases.
9. Independent recalculation of every graded answer.
10. Displayed-data versus answer-key consistency.
11. `ANS(...)` registration for every input.
12. Mathematical/statistical invariants.

If a specialized macro or library causes an error and its local API is not known, use `filelist.txt` to identify the relevant source/reference file and ask the instructor to provide that specific file rather than guessing repeatedly.

## Common failures to avoid

- Hard-coded derived answers drifting from randomized data.
- Hidden full-precision answers when students calculate from rounded displayed data.
- RadioButtons correct strings that do not exactly match a button value.
- Inventing an API for a macro merely because its filename suggests a capability.
- Assuming arbitrary valid Perl is allowed by the PG safe compartment.
- External files or legacy course-specific dependencies that are unavailable.
- Wrong sign conventions.
- Incorrect treatment of statistical ties.
- Incorrect statistical language such as "accept H0" or "the P-value is the probability H0 is true."
- Treating statistical association as proof of causation.
- Treating a model-derived low risk as exact zero risk.

## Final output expectations

For a creation request:

1. Return a complete `.pg` source ready for testing.
2. Use native PG capabilities appropriately.
3. Briefly summarize the design and randomization after the code.
4. State any specialized macro/API assumptions that still require local testing.
5. Do not require the instructor to reconstruct missing fragments.

For a review/debug request:

1. Identify the root cause.
2. Check for related issues elsewhere in the file.
3. Correct the code.
4. Return the complete corrected file when requested.
5. Explain the correction concisely.
6. Preserve the instructor's mathematical intent unless it is incorrect or ambiguous.

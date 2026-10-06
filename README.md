# WeBWorK PG Authoring Knowledge for Copilot

This repository contains public reference material intended to help Microsoft Copilot author, review, debug, and migrate WeBWorK problems written in the PG language.

The target production environment is **WeBWorK PG 2.20**.

## Purpose

Use these resources together with the official WeBWorK PG source repository:

https://github.com/openwebwork/pg

The official PG repository is the authoritative source for PG implementation, macros, functions, contexts, parsers, answer evaluators, and version history.

This repository provides additional authoring guidance, searchable macro information, file inventories, and other material useful when creating or converting WeBWorK problems.

## Important Resources

### START_HERE_WITH_COPILOT.md

Starting point for Copilot.

Read this first when using the repository as a WeBWorK authoring knowledge source.

### WeBWorK_PG_Copilot_Instructions.md

Guidance for producing reliable WeBWorK PG problems.

It contains authoring conventions, validation guidance, compatibility considerations, and recommendations for generating maintainable PG code.

### pg_macro_index.txt

Searchable index of WeBWorK PG macros and associated documentation.

Use this file when identifying an appropriate macro or PG facility for a particular authoring requirement.

Before implementing functionality manually, search this index and the official PG repository to determine whether PG already provides an established solution.

### filelist.txt

Inventory of files from the WeBWorK PG source tree.

Use this resource to determine whether a macro, module, or other PG file exists and to help locate relevant implementation or documentation.

## PG Version

The production target for this knowledge repository is:

**PG 2.20**

The official openwebwork/pg GitHub repository may default to a newer version.

When version compatibility matters:

1. Look for the `PG-2.20` tag or historical source information.
2. Do not assume that functionality in the current `main` branch or PG 2.21 existed in PG 2.20.
3. Prefer confirmed PG 2.20-compatible facilities.
4. If exact PG-2.20-tag evidence is unavailable, authoritative historical evidence predating PG 2.20 may be used, but the strength of that evidence should be stated accurately.

## Authoring Principles

When creating new PG problems:

- Prefer established PG functionality over custom implementations.
- Do not invent macro names, functions, contexts, options, parsers, or answer evaluators.
- Search the official PG repository and relevant documentation before implementing specialized functionality manually.
- Consult authoritative Open Problem Library examples when useful.
- Treat old OPL examples as evidence of usage, not automatically as current best practice.
- Prefer modern PG 2.20 authoring patterns when available.
- Use MathObjects and current parser-based answer mechanisms when appropriate.
- Design randomization so every generated problem is valid and pedagogically meaningful.
- Preserve the learning objective when converting problems from systems such as LON-CAPA.
- Do not reproduce platform-specific machinery when PG provides a simpler native implementation.
- Do not expose correct answers or solution details in student-visible content unless explicitly requested.
- Never claim generated PG has been tested on a WeBWorK server unless an actual test result has been supplied.

## Finding Information

For a specific authoring task:

1. Check the guidance in this repository.
2. Search `pg_macro_index.txt` for relevant PG macros or facilities.
3. Consult `filelist.txt` when locating PG source components.
4. Verify important details against the official `openwebwork/pg` repository.
5. Look for authoritative Open Problem Library examples when an established usage pattern would help.
6. Prefer standard PG functionality over bespoke code.

Examples of authoring tasks include:

- numerical answers and tolerances
- tables and layouts
- radio buttons and checkboxes
- dropdown menus
- multipart and dependent answers
- units
- graphing
- statistical distributions
- randomized datasets
- matrices and vectors
- custom grading
- accessibility
- CAPA/LON-CAPA migration

## Accuracy

If the available sources do not establish a PG feature or syntax reliably, do not guess.

State what could not be verified and either use a verified alternative or identify what requires testing on the local WeBWorK installation.

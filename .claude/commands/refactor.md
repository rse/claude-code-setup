---
argument-hint: "[results]"
description: "Refactor Existing Source Code"
---

<execute>
@~/.claude/commands/meta/prolog.md
</execute>

<command>
Refactor Existing Source Code
</command>

<role>
You role is an expert-level developer.
</role>

<objective>
*Refactor* existing code the following way: $ARGUMENTS.
</objective>

For this, strictly follow the following <plan/>:

<plan>
1. <task id="STEP 1: reason about the refactoring">
   Figure out what the requested refactoring is about.
   </task>

2. <task id="STEP 2: check existing code base">
   Check the existing source files for all code which is related to the
   requested refactoring.
   </task>

3. <task id="STEP 3: check existing architecture">
   Check the architecture of the existing code base to understand the
   overall structures and dynamics.
   </task>

4. <task id="STEP 4: refactor the existing code">
   Refactor the existing code the requested way by still closely
   aligning to the existing architecture and the existing code base.
   </task>

5. <task id="STEP 5: ensure cleanness of code base">
   Lint the entire code base to ensure that everything is still sane.
   </task>
</plan>


---
argument-hint: "[results]"
description: "Craft Source Code From Scratch"
---

<execute>
@~/.claude/commands/meta/prolog.md
</execute>

<command>
Craft Source Code From Scratch
</command>

<role>
Your role is an expert-level developer
</role>

<objective>
From scratch *craft new code* for: $ARGUMENTS.
</objective>

For this, strictly follow the following <plan/>:

<plan>
1. <task id="STEP 1: reason about the functionality">
   Figure out what the requested new functionality is about.
   </task>

2. <task id="STEP 2: check existing code base">
   Check the existing source files for all code which is related to the
   requested new functionality.
   </task>

3. <task id="STEP 3: check existing architecture">
   Check the architecture of the existing code base to understand the
   overall structures and dynamics.
   </task>

4. <task id="STEP 4: craft the new code">
   Craft the new code for the requested functionality by closely
   aligning to the existing architecture and the existing code base.
   </task>

5. <task id="STEP 5: ensure cleanness of code base">
   Lint the entire code base to ensure that everything is still sane.
   </task>
</plan>


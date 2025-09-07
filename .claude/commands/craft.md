---
argument-hint: "[results]"
description: "Craft Code From Scratch"
---

<execute>
@~/.claude/commands/meta/prolog.md
</execute>

<command>Craft Code From Scratch</command>
<role>Your role is an expert-level developer</role>
<objective>From scratch *craft new code* for: $ARGUMENTS</objective>.

For this, strictly follow the following <plan/>:

<plan>
1. <step>**STEP 1: reason about the functionality**</step>:
   Figure out what the requested new functionality is about.

2. <step>**STEP 2: check existing code base**</step>:
   Check the existing source files for all code which is related to the
   requested new functionality.

3. <step>**STEP 3: check existing architecture**</step>:
   Check the architecture of the existing code base to understand the
   overall structures and dynamics.

4. <step>**STEP 4: craft the new code**</step>:
   Craft the new code for the requested functionality by closely
   aligning to the existing architecture and the existing code base.

5. <step>**STEP 5: ensure cleanness of code base**</step>:
   Lint the entire code base to ensure that everything is still sane.
</plan>


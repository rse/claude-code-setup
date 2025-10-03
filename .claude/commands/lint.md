---
argument-hint: "[code refrence hint]"
description: "Lint Source Code"
---

<execute>
@~/.claude/commands/meta/prolog.md
</execute>

<command>
Lint Source Code
</command>

<role>
Your role is an expert-level developer.
</role>

<objective>
*Analyze* the code of $ARGUMENTS
for *potential problems*.
</objective>

Plan
----

Closely follow the following *<plan/>* of distinct *<task/>*,
in the given chronological order:

<plan>
1.  <task id="PREPARATION">           Find and read all the related source code files.</task>
2.  <task id="A01 - FORMATTING">      Check for inconsistently formatted code and badly vertically aligned code on sub-sequent lines.</task>
3.  <task id="A02 - COMPREHENSION">   Check for bad readability, bad maintainability, or bad self-documentation on identifiers.</task>
4.  <task id="A03 - CLEANLINESS">     Check for unclean code and inconsistent code.</task>
5.  <task id="A04 - SPELLING">        Check for typos, spelling errors, or incorrect grammar in identifiers, string literals and comments.</task>
6.  <task id="A05 - COMPLEXITY">      Check for extremely long functions of over 100 lines, and deeply nested code constructs of over 10 levels.</task>
7.  <task id="A06 - REDUNDANCY">      Check for redundancies through duplications of identical code or nearly identical code.</task>
8.  <task id="A07 - PATTERNS">        Check for broken design patterns, broken conventions, or broken best practices.</task>
9.  <task id="A08 - COMPLICATENESS">  Check for complicated or cumbersome code constructs.</task>
10. <task id="A09 - CONCISENESS">     Check for non-concise or redundant code.</task>
11. <task id="A10 - SMELLS">          Check for unnecessary type casts, problematic value coercens, surprising void() and risky eval() constructs.</task>
12. <task id="A11 - TYPING">          Check for broken "maximum type safety with minimum type annotations" rule.</task>
13. <task id="A12 - ERROR-HANDLING">  Check for missing, incorrect or inconsistent error handling or error preventions.</task>
14. <task id="A13 - MEMORY-LEAK">     Check for memory leaks and inconsistent resource allocation/deallocation pairs.</task>
15. <task id="A14 - CONCURRENCY">     Check for concurrency or parallelism race conditions.</task>
16. <task id="A15 - PERFORMANCE">     Check for bad performance and inefficiency issues.</task>
17. <task id="A16 - SECURITY">        Check for potential vulnerabilities, typical security issues, and missing essential validations.</task>
18. <task id="A17 - ARCHITECTURE">    Check for architecture, design, or modularity concerns.</task>
19. <task id="A18 - LOGIC">           Check for wrong and inconsistent domain logic.</task>
20. <task id="SUMMARY">               Give a summary of all accepted and rejected code changes.</task>
</plan>

Procedure
---------

*Analyze* the code of $ARGUMENTS for *potential problems*.
For each *potential problem* you detect, propose a corresponding
*complete code change set*. Keep all changes as *surgical and small* as possible.

In case of no code change proposal at all for an entire <task/>,
display this with the following output <template/>, where the
`**AX - XXX**: Check for [...]` is a reference to the
current <task/> you analyzed:

<template>
**AX - XXX**: Check for [...]

&#x26AA; **RESULT**: No issues found, no changes necessary.

</template>

Before any code change, provide a *brief explanation*
*what* the *problem* is and *how* the proposed *solution* fixes it.
Emphasize important keywords in your explanation texts and
use the following <template/> for those outputs, where the
`**AX - XXX**: Check for [...]` is a reference to the
current <task/> you are analyzing:

<template>
**AX - XXX**: Check for [...]

&#x1F7E0; **PROBLEM**: [...]

&#x1F535; **SOLUTION**: [...]

</template>

At the end, do not give any more explanations, except for
a summary of all accepted and reject code
changes. For this, according to the original <task/> ordering,
use the following output <template/>, where
`&#x1F7E0; **AX - XXX**: N issues` is used for <task/>
with N issues and `&#x1F535; **AX - XXX**: no issues`
for <task/> without any issues:

<template>
**SUMMARY**:

&#x1F7E0; **AX - XXX**: N issues

&#x26AA; **AX - XXX**: no issues

[...]
</template>


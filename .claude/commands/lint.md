---
argument-hint: "[code refrence hint]"
description: "Lint Source Code"
---

<execute>
@~/.claude/commands/meta/prolog.md
</execute>

<command>Lint Source Code</command>
<role>Your role is an expert-level developer.</role>
<objective>*Analyze* the code of $ARGUMENTS for *potential problems*.</objective>

Plan
----

Closely follow the following *<plan/>* of distinct *<task/>*,
in the given chronological order:

<plan>
1.  <task>**PREPARATION**:          Find and read all the related source code files.</task>
2.  <task>**A01 - FORMATTING**:     Check for inconsistently formatted code or incorrect naming.</task>
3.  <task>**A02 - COMPREHENSION**:  Check for readability, maintainability, and self-documentation via identifiers.</task>
4.  <task>**A03 - CLEANESS**:       Check for unclean or inconsistent code.</task>
5.  <task>**A04 - SMELLS**:         Check for code duplications, extremely long functions, and deeply nested constructs.</task>
6.  <task>**A05 - PATTERNS**:       Check for design pattern, convention and best practice conflicts.</task>
7.  <task>**A06 - COMPLICATENESS**: Check for complicated or cumbersome language constructs.</task>
8.  <task>**A07 - CONCISENESS**:    Check for non-concise or redundant code.</task>
9.  <task>**A08 - TYPING**:         Check for maximum type safety with minimum type annotations.</task>
10. <task>**A09 - ERROR-HANDLING**: Check for missing or incorrect error handling or error preventions.</task>
11. <task>**A10 - MEMORY-LEAK**:    Check for memory leaks.</task>
12. <task>**A11 - CONCURRENCY**:    Check for concurrency or parallelism race conditions.</task>
13. <task>**A12 - PERFORMANCE**:    Check for performance and efficiency issues.</task>
14. <task>**A13 - SECURITY**:       Check for potential vulnerabilities or security issues.</task>
15. <task>**A14 - ARCHITECTURE**:   Check for architecture, design and modularity concerns.</task>
16. <task>**A15 - LOGIC**:          Check for domain logic and runtime processing issues.</task>
17. <task>**SUMMARY**:              Give a summary of all accepted and rejected code changes.</task>
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


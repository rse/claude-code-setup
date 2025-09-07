---
argument-hint: "[code refrence hint]"
description: "Lint Code"
---

Your role is an expert-level developer.
*Analyze* the code of $ARGUMENTS for *potential problems*.

Plan
----

Closely follow the following *plan* of distinct *aspects*,
in the given chronological order:

1.  **PREPARATION**:          Find and read all the related source code files.
2.  **A01 - FORMATTING**:     Check for inconsistently formatted code or incorrect naming.
3.  **A02 - COMPREHENSION**:  Check for readability, maintainability, and self-documentation.
4.  **A03 - CLEANESS**:       Check for unclean or inconsistent code.
5.  **A04 - SMELLS**:         Check for code duplications, extremely long functions, and deeply nested constructs.
6.  **A05 - PATTERNS**:       Check for design pattern, convention and best practice conflicts.
7.  **A06 - COMPLICATENESS**: Check for complicated or cumbersome language constructs.
8.  **A07 - CONCISENESS**:    Check for non-concise or redundant code.
9.  **A08 - TYPING**:         Check for maximum type safety with minimum type annotations.
10. **A09 - ERROR-HANDLING**: Check for missing or incorrect error handling or error preventions.
11. **A10 - MEMORY-LEAK**:    Check for memory leaks.
12. **A11 - CONCURRENCY**:    Check for concurrency or parallelism race conditions.
13. **A12 - PERFORMANCE**:    Check for performance and efficiency issues.
14. **A13 - SECURITY**:       Check for potential vulnerabilities or security issues.
15. **A14 - ARCHITECTURE**:   Check for architecture, design and modularity concerns.
16. **A15 - LOGIC**:          Check for domain logic and runtime processing issues.
17. **SUMMARY**:              Give a summary of all accepted and rejected code changes.

Procedure
---------

*Analyze* the code of $ARGUMENTS for *potential problems*.
For each *potential problem* you detect, propose a corresponding
*complete code change set*. Keep all changes as *surgical and small* as possible.

In case of no code change proposal at all for an entire aspect,
display this with the following output <template/>, where the
`**AX - XXX**: Check for [...]` is a reference to the
current aspect you analyzed:

<template>
**AX - XXX**: Check for [...]

&#x26AA; **RESULT**: No issues found, no changes necessary.
</template>

Before any code change, provide a *brief explanation*
*what* the *problem* is and *how* the proposed *solution* fixes it.
Emphasize important keywords in your explanation texts and
use the following <template/> for those outputs, where the
`**AX - XXX**: Check for [...]` is a reference to the
current aspect you are analyzing:

<template>
**AX - XXX**: Check for [...]

&#x1F7E0; **PROBLEM**: [...]

&#x1F535; **SOLUTION**: [...]
</template>

At the end, do not give any more explanations, except for
a summary of all accepted and reject code
changes. For this, according to the original aspect ordering,
use the following output <template/>, where
`&#x1F7E0; **AX - XXX**: N issues` is used for aspects
with N issues and `&#x1F535; **AX - XXX**: no issues`
for aspects without any issues:

<template>
**SUMMARY**:

&#x1F7E0; **AX - XXX**: N issues

&#x26AA; **AX - XXX**: no issues

[...]
</template>


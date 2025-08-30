---
argument-hint: "[code refrence hint]"
description: "Lint Code"
---

*Analyze* the code of $ARGUMENTS for *potential problems*.

Plan
----

Closely follow the following plan of distinct aspects,
in the given chronological order:

1.  [ ] **Preparation**:         Find and read all the related source code files.
2.  [ ] **A1 - FORMATTING**:     Check for inconsistently formatted code or incorrect naming.
3.  [ ] **A2 - CLEANESS**:       Check for unclean or inconsistent code.
4.  [ ] **A3 - COMPLICATENESS**: Check for complicated or cumbersome language constructs.
5.  [ ] **A4 - CONCISENESS**:    Check for non-concise or redundant code.
6.  [ ] **A5 - ERROR-HANDLING**: Check for missing or incorrect error handling or error preventions.
7.  [ ] **A6 - MEMORY-LEAK**:    Check for memory leaks.
8.  [ ] **A7 - CONCURRENCY**:    Check for concurrency or parallelism race conditions.
9.  [ ] **A8 - PERFORMANCE**:    Check for performance issues.
10. [ ] **A9 - SECURITY**:       Check for security issues.
11. [ ] **A10 - ARCHITECTURE**:  Check for architecture concerns and design pattern improvements.
12. [ ] **A11 - LOGIC**:         Check for domain logic and runtime processing issues.
13. [ ] **Summary**:             Give a summary of all accepted and rejected code changes.

Procedure
---------

*Analyze* the code of $ARGUMENTS for *potential problems*.
For each *potential problem* you detect, propose a corresponding
*complete code change set*. Keep all changes as *surgical and small* as possible.

In case of no code change proposal at all for an entire aspect,
display this with the following output template, where the
`**AX - XXX**: Check for [...]` is a reference to the
current aspect you analyzed:

```
**AX - XXX**: Check for [...]

&#x26AA; **RESULT**: No issues found, no changes necessary.
```

Before any code change, provide a *brief explanation*
*what* the *problem* is and *how* the proposed *solution* fixes it.
Emphasize important keywords in your explanation texts and
use the following template for those outputs, where the
`**AX - XXX**: Check for [...]` is a reference to the
current aspect you are analyzing:

```
**AX - XXX**: Check for [...]

&#x1F7E0; **PROBLEM**: [...]

&#x1F535; **SOLUTION**: [...]
```

At the end, do not give any more explanations, except for
a summary of all accepted and reject code
changes. For this, according to the original aspect ordering,
use the following output template, where
`&#x1F7E0; **AX - XXX**: N issues` is used for aspects
with N issues and `&#x1F535; **AX - XXX**: no issues`
for aspects without any issues:

```
**SUMMARY**:

&#x1F7E0; **AX - XXX**: N issues

&#x26AA; **AX - XXX**: no issues

[...]
```

Prohibitions
------------

Do not factor out code into own functions.
Do not use braces arround single statement blocks in "if" and "while" constructs.
Do not insist on early "return" in "if" block if "else" block exists.
Do not remove any whitespaces in the code formatting.
Do not show just partial code changes.

Commandments
------------

Always be very *pendantic* on style.
Always use *concise* and *type-safe* code.
Always use *precise* and *surgical* code changes.
Always propose *entire, complete, and necessary code change sets* for each solution.

Always place a blank line before a comment line, but not when it is the first line of a block or an end of line comment.
Always keep code and comment formatting exactly as in the existing code.
Always use regular comments `/* ... */` instead of end-of-line comments `//`.
Always use parenthesis around arrow function parameters, even for a single parameter.
Always make a line break before the keywords "else", "catch", and "finally".
Always try to vertically align similar operators on consecutive, similar lines.
Always place spaces after opening and before closing parenthesis and braces.


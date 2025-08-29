---
description: Lint Code
---

**Analyze** the code of $ARGUMENTS for **potential problems**.

Plan
----

Closely follow the following plan of distinct aspects:

1.  [ ] **A1 - FORMATTING**:     Check for inconsistently formatted code or incorrect naming.
2.  [ ] **A2 - CLEANESS**:       Check for unclean or inconsistent code.
3.  [ ] **A3 - COMPLICATENESS**: Check for complicated or cumbersome language constructs.
4.  [ ] **A4 - CONCISENESS**:    Check for non-concise or redundant code.
5.  [ ] **A5 - ERROR-HANDLING**: Check for missing or incorrect error handling or error preventions.
6.  [ ] **A6 - MEMORY-LEAK**:    Check for memory leaks.
7.  [ ] **A7 - CONCURRENCY**:    Check for concurrency or parallelism race conditions.
8.  [ ] **A8 - PERFORMANCE**:    Check for performance issues.
9.  [ ] **A9 - SECURITY**:       Check for security issues.
10. [ ] **A10 - ARCHITECTURE**:  Check for architecture concerns and design pattern improvements.
11. [ ] **A11 - LOGIC**:         Check for domain logic and runtime processing issues.

Procedure
---------

Try to **fix each potential problem** by proposing a corresponding **code change**.

Keep all code changes as **surgical and small** as possible.

Before each code change proposal, provide a **brief explanation**
what the problem is and how the proposed solution fixes it.
Emphasize important keywords in your explanation texts and
use the following template for your output:

```
&#x1F7E0; **PROBLEM**: [...]

&#x1F535; **SOLUTION**: [...]
```

Prohibitions
------------

Do not factor out code into own functions.
Do not use braces arround single statement blocks in "if" and "while" constructs.
Do not insist on early "return" in "if" block if "else" block exists.
Do not remove any whitespaces in the code formatting.

Commandments
------------

Always be very *pendantic* on style.
Always use *concise* and *type-safe* code.
Always use *precise* and *surgical* code changes.
Always propose *complete changes* for a single problem.

Always place a blank line before a comment line, but not when it is the first line of a block.
Always keep code and comment formatting exactly as in the existing code.
Always use parenthesis around arrow function parameters, even for a single parameter.
Always make a line break before the keywords "else", "catch", and "finally".
Always try to vertically align similar operators on consecutive, similar lines.
Always place spaces after opening and before closing parenthesis and braces.


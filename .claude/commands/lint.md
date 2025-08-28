---
description: Lint Code
---

**Analyze** the code of $ARGUMENTS for **potential problems**.
Closely follow the following plan of distinct aspects:

1.  **A1 - FORMATTING**:     Check for inconsistently formatted code or incorrect naming.
2.  **A2 - CLEANESS**:       Check for unclean or inconsistent code.
3.  **A3 - COMPLICATENESS**: Check for complicated or cumbersome language constructs.
4.  **A4 - CONCISENESS**:    Check for non-concise or redundant code.
5.  **A5 - ERROR-HANDLING**: Check for missing or incorrect error handling or error preventions.
6.  **A6 - MEMORY-LEAK**:    Check for memory leaks.
7.  **A7 - CONCURRENCY**:    Check for concurrency or parallelism race conditions.
8.  **A8 - PERFORMANCE**:    Check for performance issues.
9.  **A9 - SECURITY**:       Check for security issues.
10. **A10 - LOGIC**:         Check for domain logic and runtime processing issues.
11. **A11 - ARCHITECTURE**:  Check for architecture concerns and design pattern improvements.

Try to **fix each potential problem** by proposing a corresponding **code change**.
Keep all code changes as **surgical and small** as possible.
Before each code change proposal, provide a **brief explanation**
**WHAT** the problem is and **WHY** the proposed change fixes it.

Do not factor out code into own functions.
Do not use braces arround single statement blocks in "if" and "while" constructs.
Do not insist on early "return" in "if" block if "else" block exists.
Do not remove any whitespaces in the code formatting.
Always use concise and type-safe code.
Always use precise and surgical code changes.
Always place a blank line before a comment line, but not when it is the first line of a block.
Always keep code and comment formatting exactly as in the existing code.
Always use parenthesis around arrow function parameters, even for a single parameter.


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
*Analyze* the code of $ARGUMENTS for *potential problems*.
</objective>

Plan
----

Closely follow the following *<plan/>* of distinct *<task/>*,
in the given chronological order:

<plan>
1.  <task id="PREPARATION">
    Find and read all the corresponding source code files.
    </task>

2.  <task id="A01 - FORMATTING">
    Check for inconsistently formatted code and badly vertically
    aligned code on sub-sequent lines.

    For vertical alignment, prefer to align on operators. For
    continuous code blocks (those without any blank lines at all),
    ensure that they always start with a blank line and a comment
    (usually just a single-line one).
    </task>

3.  <task id="A02 - COMPREHENSION">
    Check for bad readability, bad maintainability, or bad
    self-documentation on identifiers.

    For identifiers, prefer single-letter ones for short loops and
    accept that identifier length correlates to the identifier
    scope, i.e., longer identifiers are acceptable for larger
    scopes. For all indentifers, prefer camel-case. For classes and
    interfaces, prefer first letter to be upper-case. For parameters
    and variables, prefer first letter to be lower-case.
    </task>

4.  <task id="A03 - CLEANLINESS">
    Check for unclean code and inconsistent code.

    For unclean code, especially detect out-dated code construct
    patterns. For inconsistent code, especially detect code
    variations for equal intentions.
    </task>

5.  <task id="A04 - SPELLING">
    Check for typos, spelling errors, or incorrect grammar in
    identifiers, string literals and comments.

    Especially, for comments ensure English language only and
    prefer short very brief one-line descriptions.
    </task>

6.  <task id="A05 - COMPLEXITY">
    Check for extremely long functions, and deeply nested code
    constructs.

    Especially, for functions prefer fewer then 100 lines, and for
    nested constructs prefer fewer than 10 nesting levels.
    </task>

7.  <task id="A06 - REDUNDANCY">
    Check for redundancies through duplications of identical code or
    nearly identical code.

    For redundant code of more than 3 lines, suggest factoring it out
    into a utility function, but position it before its calls as close
    as possible.
    </task>

8.  <task id="A07 - PATTERNS">
    Check for broken design patterns, broken conventions, or broken
    best practices.

    For design patterns, especially check for broken OOP and FP aspects.
    For conventions, especially check for broken TypeScript/JavaScript
    conventions. For best practices, especially check for not leveraging
    ECMAScript APIs or using obsolete ECMAScript APIs.
    </task>

9.  <task id="A08 - COMPLICATENESS">
    Check for complicated or cumbersome code constructs.

    Especially, check for unnecessary difficult code constructs
    for which simpler solutions exist.
    </task>

10. <task id="A09 - CONCISENESS">
    Check for non-concise and boilerplate-based code.

    Especially, check for unnecessary long code constructs for
    which shorter solutions exist, and check for unnecessary
    technical/infrastructural code with too less domain-specific
    aspects.
    </task>

11. <task id="A10 - SMELLS">
    Check for code smells.

    Especially, check for unnecessary type casts, problematic value
    coercions, surprising void() and risky eval() constructs.
    </task>

12. <task id="A11 - TYPING">
    Check for broken "maximum type safety with minimum type
    annotations" rule.

    Especially, ensure that no implicit "any" type exists and that types
    are primarily used on function parameters. For all other cases,
    ensure that a maximum type inference is used.
    </task>

13. <task id="A12 - ERROR-HANDLING">
    Check for missing, incorrect or inconsistent error handling or
    error preventions.

    Surround code blocks with try/catch-clauses only if really
    necessary to not clutter the code too much with error handling. For
    asynchronous code, prefer .catch() instead of try/catch.
    </task>

14. <task id="A13 - MEMORY-LEAK">
    Check for memory leaks and inconsistent resource
    allocation/deallocation pairs.

    Especially, ensure that for each allocation there is a corresponding
    deallocation and that deallocations happen in the exact opposite
    order of the allocations.
    </task>

15. <task id="A14 - CONCURRENCY">
    Check for concurrency or parallelism race conditions.

    Especially, check for potential problems of code which runs
    asynchronously from timeout/interval or I/O driven callbacks.
    </task>

16. <task id="A15 - PERFORMANCE">
    Check for bad performance and inefficiency issues.

    Especially, check for code constructs with a high (i.e., not
    constant/O(1), or linear/O(n) complexity) in its execution time
    and/or memory consumption.
    </task>

17. <task id="A16 - SECURITY">
    Check for potential vulnerabilities, typical security issues,
    and missing essential validations.

    Especially, check for edge cases in value ranges.
    </task>

18. <task id="A17 - ARCHITECTURE">
    Check for architecture, design, or modularity concerns.

    For architecture, ensure that patterns like Layer, Slice, Hub
    & Spoke, and Pipes & Filters are used correctly. For design,
    ensure that patterns like Singleton, Proxy, Adapter, Class, and
    Interface are used correctly.
    </task>

19. <task id="A18 - LOGIC">
    Check for wrong and inconsistent domain logic.

    Especially, try to detect implausible edge cases in the domain
    logic.
    </task>

20. <task id="A19 - FLOW">
    Check for wrong control or data flow.

    Especially, try to detect control flows where corner cases are not covered,
    and data flows with inconsistent value unit processing.
    </task>

21. <task id="SUMMARY">
    Give a summary of all accepted and rejected code changes.
    </task>
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


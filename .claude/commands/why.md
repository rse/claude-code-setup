---
argument-hint: "[issue]"
description: "Five-Whys Root-Cause Analysis"
---

Apply the Five-Whys root-cause analysis technique to investigate the following issue:

$ARGUMENTS

For this, iteratively ask "why" to drill down from symptoms to the root-cause. 
This helps to identify the fundamental reason behind a problem rather than just
addressing surface-level symptoms.

To apply the method, follow the following plan:

1. Start with the problem statement.
2. Check sources for initial hints on the problem.
3. Perform the analysis iteration cycle:
   a. Ask "Why did this happen?" and document the answer.
   b. For each answer, ask "Why did this happen?" again.
   c. Continue for at least 5 iterations or until root-cause is found.
4. Validate the root-cause by working backwards the causality chain.
5. Propose solutions that address and solve the root-cause.

Notice the following points:

- Don't stop at symptoms, keep digging for systemic issues.
- Multiple root-causes may exist -- explore different branches.
- Document each "Why" for future reference.
- Consider both technical, domain-specific, process-related or organizational causes.
- The magic is NOT in exactly 5 "Why" -- you can stop when you already reached the root-cause.
- For the proposed solutions, optionally directly propose corresponding code changes.

Example:

```
**Problem Statement**: Application crashes on startup.
**WHY 1**: Database connection fails.
**WHY 2**: Connection string is invalid.
**WHY 3**: Environment variable not set.
**WHY 4**: Deployment script missing environment setup.
**WHY 5**: Documentation didn't specify environment requirements.
**Root Cause**: Missing deployment documentation.
**Validation (Working Backwards)**: [...]
**Proposed Solution**: [...]
```


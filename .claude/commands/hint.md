---
argument-hint: "[question]"
description: "Give Essential Hints"
---

Be an expert-level pair-programming partner and
give essential hints on the following question or issue:

$ARGUMENTS

Always answer very briefly and very concise.
Always show concise and type-safe code only.
Always show precise and surgical code changes only.
Always emphasize essential keywords in your hints.
Always format code as such in your hints.

If possible, tell me about the cruxes (essential background
information I should not overlook) of the hints.

If possible, tell me about alternatives in
case your hints cannot be followed by me.

If possible, give one to three URLs of essential sources
where further information can be found.

Never propose direct changes to the existing code.

For your answer use the following outout <template/>:

<template>
**REQUEST**:
$ARGUMENTS

**HINTS**:
- [...]
- [...]
- [...]

**CRUXES**:
- [...]
- [...]
- [...]

**ALTERNATIVES**:
- [...]
- [...]
- [...]

**SEE ALSO**:
- [...]
- [...]
- [...]
</template>


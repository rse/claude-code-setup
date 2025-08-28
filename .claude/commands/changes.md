---
description: ChangeLog Entries
---

You are an assistant helping to complete *ChangeLog* entries,
based on the underling Git commit messages.

PLAN
----

Follow the following plan:

1. Locating and reading `CHANGELOG.md` file.
2. Reading corresponding Git commit log information.
3. Completing `CHANGELOG.md` file.

EXECUTION
---------

The *ChangeLog* file `CHANGELOG.md` contains sections
with headers in the style `N.M.K (YYYY-MM-DD)`.
It is located in the current directory or one of the parent directories.

Please complete the entries in the first (most recent) section only,
by summarizing the corresponding (most recent) Git commits.

Ignore the current Git index and stash.
Just use the Git commits.

For finding the corresponding Git commits, use the `N.M.K`
from the second header in the *ChangeLog* file as
the corresponding Git tag and then check all commits
between `HEAD` and this tag.

Instead of the chronological commit order, group the *ChangeLog* entries
by the following prefixes and use the given prefix order:

- `IMPROVEMENT`
- `BUGFIX`
- `UPDATE`
- `CLEANUP`


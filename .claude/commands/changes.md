---
description: ChangeLog Entries
---

You are an assistant, helping to complete and consolidate
*ChangeLog* entries, based on underling Git commit messages.

PLAN
----

Follow the following plan:

1. Locate and read existing `CHANGELOG.md` file.
2. Read corresponding Git commit log messages.
3. Complete entries in `CHANGELOG.md` file.
4. Consolidate entries in `CHANGELOG.md` file.
5. Sort entries in `CHANGELOG.md` file.

EXECUTION
---------

The *ChangeLog* file `CHANGELOG.md` contains sections
with headers in the style `N.M.K (YYYY-MM-DD)`.
It is located in the current directory or one of the parent directories.

Please complete, consolidate and sort the entries in the first (most recent)
section only, by summarizing the corresponding (most recent) Git commits only.

Ignore the current Git index and Git stash and use the Git commits only.

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

Perform the entry consolidation per prefix group only.


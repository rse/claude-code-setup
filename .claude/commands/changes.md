---
description: ChangeLog Entries
---

You are an assistant, helping to complete, consolidate
and sort *ChangeLog* entries, based on underling Git commit messages.

PLAN
----

Follow the following plan:

1. Locate and read existing `CHANGELOG.md` file.
2. Read corresponding Git commit log messages.
3. Complete *ChangeLog* entries.
4. Consolidate *ChangeLog* entries.
5. Sort *ChangeLog* entries.
6. Write modified *ChangeLog* entries to `CHANGELOG.md` file.

EXECUTION
---------

Execute the plan as following:

1. Locate and read existing `CHANGELOG.md` file:
   The *ChangeLog* file `CHANGELOG.md` contains sections
   with headers in the style `N.M.K (YYYY-MM-DD)`.
   The `CHANGELOG.md` file is located in the current directory
   or one of the parent directories.

2. Read corresponding Git commit log messages:
   Ignore the current Git index and Git stash and use the Git commits only.
   For finding the corresponding Git commits, use the `N.M.K`
   from the second header in the *ChangeLog* file as
   the corresponding Git tag and then check all commits
   between `HEAD` and this tag.

3. Complete *ChangeLog* entries
   (without immediately modifying `CHANGELOG.md` file):
   Complete the entries in the first (most recent) section only,
   by adding the corresponding (most recent) Git commits only.
   Per Git commit, reduce the Git commit messages to a single
   short sentence.

4. Consolidate *ChangeLog* entries
   (without immediately modifying `CHANGELOG.md` file):
   Consolidate the entries in the first (most recent) section only,
   by summarizing and merging closely related entries.
   Perform the entry consolidation per prefix group only.

5. Sort *ChangeLog* entries
   (without immediately modifying `CHANGELOG.md` file):
   Please sort the entries in the first (most recent) section only.
   Instead of the chronological commit order, group the entries
   by the following prefixes and their given prefix order:

    - `IMPROVEMENT`
    - `BUGFIX`
    - `UPDATE`
    - `CLEANUP`

6. Write modified *ChangeLog* entries to `CHANGELOG.md` file:
   Finally, update the `CHANGELOG.md` file with the
   completed, consolidated and sorted entries.


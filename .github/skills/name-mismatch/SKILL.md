---
name: catalog-helper
description: Use when the user asks to register or document a new S3 Tables dataset in the data catalog.
---

# S3 Tables catalog entry (broken: name does not match directory)

This skill will not load. The directory is `name-mismatch/`, but the frontmatter
`name` is `catalog-helper`. VS Code requires the `name` to match the parent
directory name exactly, and when it does not, the skill is dropped silently with
no error in the chat.

To fix: rename either the directory or the `name` field so they match.

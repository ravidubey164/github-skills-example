---
name: myorg/s3-table-entry
description: Use when the user asks to register or document a new S3 Tables dataset in the data catalog.
---

# S3 Tables catalog entry (broken: illegal characters in name)

This skill will not load. The `name` field contains a slash (`myorg/s3-table-entry`).
VS Code only allows lowercase letters, numbers, and hyphens in the `name`. Slashes,
colons, dots, and namespace prefixes cause the skill to fail to load, again with no
error message. Plugin command prefixes are added automatically; you never write them
into `name` yourself.

To fix: set `name: s3-table-entry` and let the directory name match it.

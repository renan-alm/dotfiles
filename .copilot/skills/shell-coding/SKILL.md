---
name: shell-coding
description: Guidance for writing and debugging shell scripts (Bash/Zsh). Use this when asked to create or fix shell scripts, automate tasks, or manage system configurations via shell commands.
---
# Shell Coding Skill and Rules

## Overall rules

Always start with `set -euo pipefail` - Exit on errors (`-e`), undefined variables (`-u`), and pipeline failures (`-o pipefail`) to catch bugs early.

Quote all variables - Use `"$var"` instead of `$var` to prevent word splitting and glob expansion issues with spaces or special characters.

Use `[[ ]]` instead of `[ ]` - Double brackets provide safer string comparisons, support regex, and avoid pitfalls with empty variables.

## Input validation

Check that required arguments exist and commands are available before proceeding (e.g., `command -v jq >/dev/null || { echo "jq required"; exit 1; }`).

## Function creations

Organize code into functions with descriptive names to improve readability and maintainability.


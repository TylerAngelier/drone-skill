---
name: drone-skill
description: Operate the installed Drone CI command line client to inspect or manage builds, repositories, secrets, logs, cron jobs, templates, users, and local pipeline execution. Use when Codex needs to run `drone` commands, discover exact CLI syntax with `--help`, troubleshoot Drone CLI usage, or cross-reference the official Drone CLI docs while working against a Drone server.
---

# Drone CLI

## Overview

Use the installed `drone` binary as the source of truth for syntax and available flags. Use the official Drone docs as a secondary reference for examples, command families, and expected behavior.

## Workflow

1. Verify the CLI before planning work.
   - Run `command -v drone`.
   - Run `drone --version`.
   - If the docs and local help disagree, follow local help for executable syntax.

2. Verify connection settings before remote operations.
   - Check `DRONE_SERVER` and `DRONE_TOKEN`.
   - If either is missing, ask the user for the value or explain which exports they need.
   - Read `references/auth-and-discovery.md` for the minimal setup and discovery flow.

3. Discover the exact command shape from the installed binary.
   - Start with `drone --help`.
   - Drill into `drone <group> --help` and `drone <group> <subcommand> --help`.
   - Prefer live help over memory before running state-changing commands.
   - Common examples: `drone build info --help`, `drone repo update --help`, `drone secret add --help`, `drone exec --help`.

4. Load reference material only when needed.
   - Read `references/command-map.md` for the top-level command map and common subcommands.
   - Read `references/docs-index.md` for the official documentation tree and source links.

5. Execute carefully and report clearly.
   - Treat `secret rm`, `repo disable`, `repo update`, `build stop`, `template rm`, and `log purge` as mutating operations.
   - Confirm the target repo, build number, secret name, or template name from help or existing output before execution.
   - Report the exact command you ran and any environment assumptions.

## Command Patterns

- Treat `build`, `repo`, `secret`, `template`, `cron`, `user`, `server`, `queue`, `orgsecret`, and `autoscale` as grouped commands with subcommands.
- Treat `exec`, `encrypt`, `lint`, `sign`, `jsonnet`, and `starlark` as direct utilities.
- Treat `log` as a grouped command with log-specific subcommands.
- Inspect `drone <group> --help` instead of guessing subcommands or flags.

## References

- `references/auth-and-discovery.md` for authentication and command discovery.
- `references/command-map.md` for the observed command map from the installed CLI.
- `references/docs-index.md` for official docs URLs and GitHub source paths.

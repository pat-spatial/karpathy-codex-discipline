# Karpathy Codex Discipline

A small Codex skill that adapts the Karpathy-inspired `CLAUDE.md` coding-agent discipline to a Codex workflow.

The goal is not to add a giant prompt pack. It is to make one useful behavior easy to invoke:

```text
Use Karpathy skill: keep this surgical, state assumptions, define success criteria, and verify.
```

## What It Does

This skill pushes Codex toward five behaviors:

- Think before coding.
- Prefer the simplest viable change.
- Keep diffs surgical.
- Work from explicit success criteria.
- Verify before claiming completion.

It also translates those ideas into Codex-specific mechanics:

- read relevant code before editing;
- use `rg` first for search;
- use `apply_patch` for manual edits;
- preserve dirty worktrees;
- request sandbox escalation only when needed;
- report checks, skipped checks, and residual risk clearly.

## Why This Exists

The original `andrej-karpathy-skills` project became popular because it targets common coding-agent failure modes: silent assumptions, overengineering, broad unrelated edits, and unverified "done" claims.

Codex already has strong coding-agent discipline in many environments. This skill is therefore best understood as a triggerable emphasis layer: use it when the task is ambiguous, risky, refactor-prone, or likely to invite speculative cleanup.

## Install

Copy the skill folder into your Codex skills directory:

```bash
mkdir -p ~/.codex/skills/karpathy-codex-discipline
cp skills/karpathy-codex-discipline/SKILL.md ~/.codex/skills/karpathy-codex-discipline/SKILL.md
```

Then invoke it in a Codex task:

```text
Use Karpathy skill and fix this bug. Keep the change surgical, state assumptions, define success criteria, and verify.
```

## When To Use It

Use it for:

- bug fixes with ambiguous reproduction steps;
- refactors where scope creep is likely;
- PR review follow-up;
- high-risk edits in a dirty worktree;
- tasks where verification matters more than speed.

Skip it for tiny one-command requests.

## Attribution

Inspired by the Karpathy/Claude Code guideline pattern popularized by:

- https://github.com/multica-ai/andrej-karpathy-skills
- https://github.com/forrestchang/andrej-karpathy-skills

This repository is an independent Codex adaptation, not an official Andrej Karpathy, Claude, Anthropic, OpenAI, or Multica project.

## License

MIT


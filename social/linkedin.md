# LinkedIn Draft

I asked Codex to critically review the popular Karpathy-inspired `CLAUDE.md` coding-agent discipline and adapt it for Codex.

The useful part was not copying the prompt over verbatim. Codex compared the idea against its own existing prompt discipline, identified the overlap, removed redundant instructions, and kept the pieces that make sense as a Codex-native workflow.

The result is a small skill, not a giant prompt pack: a triggerable behavior layer for moments when coding agents tend to drift.

Invocation:

```text
Use Karpathy skill: keep this surgical, state assumptions, define success criteria, and verify.
```

The skill focuses Codex on five habits:

- think before coding;
- choose the simplest viable change;
- keep diffs surgical;
- work from explicit success criteria;
- verify before claiming completion.

It is also tuned for Codex-specific workflow details: `rg`-first code discovery, `apply_patch` edits, dirty worktree protection, sandbox approval discipline, and concise reporting of checks and residual risk.

My main takeaway: in a well-instructed Codex environment, this does not unlock a new capability. It acts more like a deliberate mode switch. Use it when the task is ambiguous, refactor-prone, or verification-sensitive.

Repo: https://github.com/pat-spatial/karpathy-codex-discipline

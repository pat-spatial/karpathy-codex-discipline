# LinkedIn Draft

I adapted the popular Karpathy-inspired `CLAUDE.md` coding-agent discipline into a small Codex skill.

The point is not a larger prompt pack. It is the opposite: a short, triggerable behavior layer for moments when coding agents tend to drift.

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

I also adapted it for Codex-specific workflow details: `rg`-first code discovery, `apply_patch` edits, dirty worktree protection, sandbox approval discipline, and concise reporting of checks and residual risk.

My main takeaway: in a well-instructed Codex environment, this does not unlock a new capability. It acts more like a deliberate mode switch. Use it when the task is ambiguous, refactor-prone, or verification-sensitive.

Repo: [add GitHub URL]


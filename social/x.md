# X Draft

I asked Codex to critically review the Karpathy-inspired `CLAUDE.md` coding-agent discipline and adapt it for Codex.

The useful move was not copying it verbatim. Codex removed redundant instructions, kept the intent, and made it consistent with Codex workflows.

Invocation:

```text
Use Karpathy skill: keep this surgical, state assumptions, define success criteria, and verify.
```

It is not a giant prompt pack. It is a small mode switch for Codex: think first, keep diffs tight, avoid speculative cleanup, and verify before saying done.

Repo: https://github.com/pat-spatial/karpathy-codex-discipline

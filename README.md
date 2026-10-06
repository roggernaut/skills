# skills

Agent skills I use to keep output from reading or looking AI-generated. They follow the standard `SKILL.md` format, so they work in Codex, ChatGPT, Claude and other agents that load skills.

- [deslop-writing](deslop-writing/SKILL.md): the recognized tells of LLM prose (vocabulary, sentence shapes, tone, transitions, formatting), the fix for each and a revision pass.
- [deslop-design](deslop-design/SKILL.md): the visual tells of AI-built pages (left-border callouts, icon-in-a-box grids, eyebrows, gradient headlines, purple defaults), graded fixes from simple to complex and a review pass.

Each `SKILL.md` is a short workflow with hard defaults. The full pattern catalogue lives in `references/patterns.md` and is read on demand.

Run both on anything public-facing. Copy tells and design tells usually show up together.

## Install

```bash
git clone https://github.com/roggernaut/skills.git
```

Then copy the skill folders into your agent's skills directory:

- Codex: `~/.codex/skills/`
- Claude Code: `~/.claude/skills/` (personal) or `.claude/skills/` in a project

```bash
cp -R skills/deslop-writing skills/deslop-design ~/.codex/skills/
```

ChatGPT and Claude.ai: zip a skill folder and upload it as a skill.

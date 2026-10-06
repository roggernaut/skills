# skills

Claude skills I use to keep output from reading or looking AI-generated.

- [ai-writing-clean](ai-writing-clean/SKILL.md): the recognized tells of LLM prose (vocabulary, sentence shapes, tone, transitions, formatting), the fix for each, and a revision pass.
- [ai-design-clean](ai-design-clean/SKILL.md): the visual tells of AI-built pages (left-border callouts, icon-in-a-box grids, eyebrows, gradient headlines, purple defaults), graded fixes from simple to complex, and a review pass.

Run both on anything public-facing. Copy tells and design tells usually show up together.

## Install

Claude Code: copy a folder into `~/.claude/skills/` (personal) or `.claude/skills/` in a project.

```bash
git clone https://github.com/roggernaut/skills.git
cp -R skills/ai-writing-clean skills/ai-design-clean ~/.claude/skills/
```

Claude.ai / desktop: zip a skill folder and upload it under Settings → Capabilities → Skills.

# Install -- Claude Code

## Quick install

```bash
# 1. Copy cognitive protocol to Claude's config
cp cognitive-protocol.md ~/.claude/motivation-audit.md

# 2. Add reference in CLAUDE.md
echo '@~/.claude/motivation-audit.md' >> ~/.claude/CLAUDE.md
```

## What gets loaded where

| File | Destination | Purpose |
|---|---|---|
| `cognitive-protocol.md` | `~/.claude/motivation-audit.md` | Always-on core rules (~30 lines) |
| `SKILL.md` | `~/.claude/skills/motivation-audit/SKILL.md` | Full reference (loaded on demand) |
| `anti-patterns.md` | `~/.claude/skills/motivation-audit/anti-patterns.md` | Detailed anti-pattern guide |
| `examples.md` | `~/.claude/skills/motivation-audit/examples.md` | Before/after reference |

## Full install (with skill files)

```bash
# 1. Core rules
cp cognitive-protocol.md ~/.claude/motivation-audit.md

# 2. Skill files
mkdir -p ~/.claude/skills/motivation-audit
cp SKILL.md ~/.claude/skills/motivation-audit/
cp anti-patterns.md ~/.claude/skills/motivation-audit/
cp examples.md ~/.claude/skills/motivation-audit/

# 3. Register in CLAUDE.md
echo '@~/.claude/motivation-audit.md' >> ~/.claude/CLAUDE.md
```

## Verify

Ask Claude Code: "What are the motivation-audit cognitive rules you're following?" It should list the five sections from `cognitive-protocol.md`: audit motivation before analyzing, detect motivation contamination, calibrate don't paralyze, the altruism test, output self-check.

## Stacking with other cognitive bases

Motivation Audit loads FIRST -- before frame-auditing, before first-principles. It audits the driver of reasoning, not the reasoning itself. If `~/.claude/frame-auditing.md` or `~/.claude/first-principles.md` are already referenced in `CLAUDE.md`, place `motivation-audit.md` BEFORE them.

Recommended loading order in `CLAUDE.md`:
```
@~/.claude/motivation-audit.md
@~/.claude/frame-auditing.md
@~/.claude/first-principles.md
```

## Uninstall

```bash
rm ~/.claude/motivation-audit.md
rm -rf ~/.claude/skills/motivation-audit
# Remove the @~/.claude/motivation-audit.md line from ~/.claude/CLAUDE.md
```

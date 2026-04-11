# Install -- Claude Code

> **Recommended**: Run `./install.sh` from the repo root for automated installation with dual-mode support (@ reference + inline fallback).
> The manual steps below are for reference or troubleshooting.

## Quick install

```bash
# 1. Inject core rules into CLAUDE.md (direct content injection — works on all versions)
cat cognitive-protocol.md >> ~/.claude/CLAUDE.md
```

## What gets loaded where

| File | Destination | Purpose |
|---|---|---|
| `cognitive-protocol.md` | `~/.claude/CLAUDE.md` (appended) | Always-on core rules (~30 lines) |
| `SKILL.md` | `~/.claude/skills/motivation-audit/SKILL.md` | Full reference (loaded on demand) |
| `anti-patterns.md` | `~/.claude/skills/motivation-audit/anti-patterns.md` | Detailed anti-pattern guide |
| `examples.md` | `~/.claude/skills/motivation-audit/examples.md` | Before/after reference |

## Full install (with skill files)

```bash
# 1. Core rules (inject directly into CLAUDE.md)
cat cognitive-protocol.md >> ~/.claude/CLAUDE.md

# 2. Skill files
mkdir -p ~/.claude/skills/motivation-audit
cp SKILL.md ~/.claude/skills/motivation-audit/
cp anti-patterns.md ~/.claude/skills/motivation-audit/
cp examples.md ~/.claude/skills/motivation-audit/

# 3. (Core rules already injected in step 1)
```

## Verify

Ask Claude Code: "What are the motivation-audit cognitive rules you're following?" It should list the five sections from `cognitive-protocol.md`: audit motivation before analyzing, detect motivation contamination, calibrate don't paralyze, the altruism test, output self-check.

## Stacking with other cognitive bases

Motivation Audit loads FIRST -- before frame-auditing, before first-principles. It audits the driver of reasoning, not the reasoning itself. If Frame Auditing or First Principles is already injected into `CLAUDE.md`, inject Motivation Audit content BEFORE them.

Recommended injection order in `CLAUDE.md`:
```
(Motivation Audit content)
(Frame Auditing content)
(First Principles content)
```

## Uninstall

```bash
# Remove the Motivation Audit section from ~/.claude/CLAUDE.md (search for "# Motivation Audit -- Cognitive Protocol" header)
rm -rf ~/.claude/skills/motivation-audit
```

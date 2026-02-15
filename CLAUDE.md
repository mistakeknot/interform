# interform

Design patterns and visual quality for Claude Code — distinctive, production-grade interfaces.

## Overview

1 skill, 0 agents, 0 commands, 0 hooks. Companion plugin for Clavain.

## Quick Commands

```bash
python3 -c "import json; json.load(open('.claude-plugin/plugin.json'))"  # Manifest check
ls skills/*/SKILL.md | wc -l  # Should be 1
```

## Design Decisions (Do Not Re-Ask)

- Anti-AI-slop aesthetic — bold, intentional design over generic templates
- Covers web, TUI, native, and print mediums
- Extracted from Clavain — domain-specific design skill, not core engineering

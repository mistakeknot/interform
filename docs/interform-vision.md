# interform — Vision and Philosophy

**Version:** 0.1.0
**Last updated:** 2026-02-28

## What interform Is

interform is the design standards layer for Claude Code. It provides a single skill — `distinctive-design` — that guides generation of production-grade interfaces across web, TUI, native, and print mediums. The skill encodes concrete aesthetic judgment: specific font choices to avoid, layout patterns that signal laziness, and the kind of intentionality that separates designed output from generated output.

interform is a companion to Clavain. Where Clavain handles engineering workflow and OS-level behavior, interform handles the visual dimension of what agents produce. They share the same host but different concerns — neither duplicates the other.

## Why This Exists

AI-generated interfaces have a recognizable aesthetic: Inter font, purple-to-blue gradients, card grids, hollow icons, symmetrical layouts. This aesthetic signals that no human made a choice — the model took the path of least resistance. interform exists because the visual quality of generated artifacts is a form of documentation quality, and documentation quality is a product interface. Slop output is a trust signal. Distinctive output is evidence of craft.

## Design Principles

1. **The aesthetic standards are the product.** Without opinionated defaults on typography, color, spatial composition, and medium-appropriate detail, interform is just a prompt wrapper. The opinions are not configurable noise — they are the deliverable.

2. **Medium specificity over generic rules.** Web, TUI, native, and print each have different constraints and different failure modes. A TUI skill applied to a print layout produces bad output. Guidance is concrete and medium-aware, not abstract and portable.

3. **Bold intentionality over intensity.** Maximalism and minimalism both produce distinctive work. Generic work comes from indecision, not from choosing a quiet register. The skill enforces commitment to a direction, not any particular direction.

4. **Strong defaults, explicit overrides.** interform ships with strong defaults (avoid Inter, avoid purple gradients, avoid card grids) that any session can override with a deliberate rationale. The defaults do the heavy lifting; overrides are documented, not silent.

5. **Documentation is a visual artifact.** The visual quality of what agents produce reflects on the platform that produced it. interform treats every generated interface — including rendered docs, TUI outputs, and web previews — as part of the product surface.

## Scope

**Does:**
- Provide the `distinctive-design` skill for web, TUI, native, and print interface generation
- Encode specific, actionable anti-patterns (named fonts, named color clichés, layout defaults to avoid)
- Guide aesthetic direction before code generation begins — tone, medium, differentiation
- Apply to any interface Claude Code generates in a session where the skill is active

**Does not:**
- Enforce design rules via hooks or automated checks (that requires tooling interform does not ship)
- Cover data modeling, API design, or backend architecture
- Replace human design review — it raises the floor, not the ceiling
- Duplicate Clavain's engineering workflow guidance

## Direction

- Expand medium-specific guidance as concrete examples accumulate — the skill grows stronger with real output artifacts feeding back into its guidelines
- Add a `docs/examples/` directory with before/after comparisons demonstrating anti-slop enforcement in practice
- Remain a single-skill plugin; complexity budget stays low — depth in the one skill beats breadth across many

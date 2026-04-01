# TH B UI Skill

TH B UI Skill is a reusable skill for generating enterprise admin UI prototypes.

It helps AI produce interfaces that feel structured, restrained, and operational by encoding page patterns, interface semantics, and UI specification rules. The focus is on design language and page structure rather than any single technical implementation.

## Highlights

- Enterprise-style list, detail, form, drawer, and dashboard patterns
- Clear rules for color usage, button hierarchy, forms, tables, and states
- Reusable prompts for prototype text, Figma prompts, and frontend code
- Skill-marketplace-friendly structure with `SKILL.md` and `agents/openai.yaml`
- GitHub-friendly repository layout for sharing and versioning

## Quick Start

Reference the skill directly in your prompt:

```text
Use $th-b-ui-skill to design a desktop enterprise prototype with compact spacing, neutral surfaces, clear button hierarchy, and stable table behavior.
```

For better results, also provide:

- page type
- key sections
- major fields
- table columns
- primary and secondary actions
- whether you want prototype text, a Figma prompt, or frontend code

## Example Prompts

```text
Use $th-b-ui-skill to design a desktop admin list page for resource management. Keep the page structured with a filter panel, action area, data table, status tags, and pagination.
```

```text
Use $th-b-ui-skill to create an approval form prototype with grouped sections, compact controls, clear validation, and a fixed footer action area.
```

```text
Use $th-b-ui-skill to generate a Figma-ready prompt for a detail page with a status header, summary card, related tabs, and an operation log.
```

```text
Use $th-b-ui-skill to produce enterprise-style frontend code with neutral surfaces, compact forms, clear action hierarchy, and explicit loading, empty, and error states.
```

## What This Skill Covers

This skill guides AI to generate:

- list pages with filter panel, action area, data table, and pagination
- detail pages with status header, summary blocks, and related tabs
- create and edit forms with grouped sections and clear action hierarchy
- drawer-based quick workflows
- dashboard-style operational pages
- Figma-ready interface prompts
- enterprise-style HTML, Vue, or React prototype code

## Design Principles

This skill prefers:

- neutral, low-noise surfaces
- one accent color
- compact density
- clear action hierarchy
- stable enterprise page layouts
- explicit loading, empty, and error states

This skill avoids:

- decorative marketing layouts
- flashy gradients
- oversized hero sections
- overly playful UI patterns

## Repository Structure

```text
th-b-ui-skill/
├── SKILL.md
├── README.md
├── HUMAN_GUIDE.md
├── agents/
│   └── openai.yaml
└── references/
    ├── internal-mapping.md
    ├── page-patterns.md
    ├── publishing-kit.md
    └── ui-spec.md
```

### Main Files

- `SKILL.md`
  The core skill definition and main rule set.

- `agents/openai.yaml`
  Display metadata and default prompt for platforms that support skill manifests.

- `HUMAN_GUIDE.md`
  A human-readable usage guide for teammates and collaborators.

### Reference Files

- `references/page-patterns.md`
  Reusable page archetypes such as list, detail, form, drawer, and dashboard pages.

- `references/internal-mapping.md`
  Naming semantics and component-family style mappings.

- `references/ui-spec.md`
  More explicit rules for color, buttons, forms, tables, spacing, and interactions.

- `references/publishing-kit.md`
  Publishing copy, short descriptions, and example prompts.

## Using This Repository

This repository can be used in several ways:

1. As a local skill folder inside a Codex-compatible skills directory
2. As a GitHub-backed source for a skills marketplace
3. As a reusable enterprise UI prompt specification for design and frontend teams

## Best Fit Scenarios

- generating a management list page
- designing a detail page with tabs and status
- creating a configuration or approval form
- building a quick-create drawer workflow
- drafting an operational dashboard
- generating enterprise-style frontend prototypes

## Publishing Notes

This repository is structured to work well with skill marketplaces and GitHub-based distribution. The skill is presented as a reusable enterprise UI specification layer rather than a product-specific technical dependency.

If your platform reads skill metadata, the main entry points are:

- `SKILL.md`
- `agents/openai.yaml`

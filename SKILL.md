---
name: th-b-ui-skill
description: Generate product prototypes that visually and structurally match an internal enterprise component system through reusable UI rules, naming semantics, and page patterns. Use when Codex needs to create UI mockups, wireframes, Figma drafts, HTML, or frontend code that should feel like an internal admin platform, especially for list pages, detail pages, search forms, dialogs, drawers, tables, tabs, and dashboard-style operational interfaces.
---

# TH B UI Skill

Generate prototypes that feel like a mature internal business system rather than a generic consumer app.

Treat this skill as a design-rules layer. Reproduce the structure, density, hierarchy, naming habits, and component selection patterns of the internal system, but do not depend on private registries, internal URLs, or unpublished component APIs unless the user explicitly provides them in the current task.

## Workflow

Follow this sequence:

1. Identify the page type.
2. Infer the dominant component pattern.
3. Apply the layout and density rules in this skill.
4. Generate the prototype in the requested format.
5. Briefly self-check that the result still feels like an internal enterprise UI.

If requirements are incomplete, infer the most likely enterprise pattern instead of blocking:

- List page: search area, action area, data table, pagination
- Detail page: summary header, sectioned information blocks, related records
- Create or edit page: form sections, sticky actions, validation hints
- Dialog workflow: compact form, clear primary action, explicit cancel path
- Dashboard: restrained cards, summary metrics, filters, supporting table or chart

## Naming Semantics

When the user wants the prototype to feel close to the internal system, organize the UI using these naming semantics even if the final output uses generic components:

- `Base*`: foundational components, especially layout, form, table, drawer, modal, tabs, pagination, select, date picker, tag, and card patterns
- `Business*`: domain-aware components, especially specialized selectors and packaged workflows
- `Standard*` or configuration-driven blocks: generated or highly standardized admin sections such as search forms, tables, button groups, and bottom action bars

Use this mental model:

- Reach for `Base*` when you need a foundational container or interaction primitive.
- Reach for `Business*` when the page benefits from a domain-aware selector or ready-made domain block.
- Reach for `Standard*` when the page should feel strongly standardized, repetitive, or configuration-driven.

Common internal-feeling examples:

- a base layout container for overall page framing
- a base form container for filter panels and edit sections
- a base data table for record-centric main content
- a side drawer for lightweight create and edit flows
- a modal dialog for confirmation and short tasks
- tab containers for entity subdomains
- pagination controls for bottom table navigation
- status tags or indicators for lifecycle state
- business-aware date range, organization, category, resource, or object selectors when a plain input would feel too generic
- standard search forms, standardized tables, button groups, and fixed bottom action bars as shorthand patterns for repeatable enterprise sections

If the user does not need literal internal names in the output, preserve the pattern and translate it to generic labels such as "filter form", "business selector", "data table", "bottom action bar", and "status indicator".

## Layout Rules

Prefer calm, structured, rectangular layouts.

- Use a clear top-to-bottom hierarchy.
- Group controls into containers with obvious boundaries.
- Prefer card, panel, table, form, tab, drawer, and modal patterns over freeform compositions.
- Use consistent horizontal alignment.
- Keep content widths practical for desktop admin work.
- Reserve visual emphasis for the primary action and key status information.
- Avoid decorative hero sections, marketing-style banners, oversized illustrations, and playful landing-page patterns.

For list pages, default to this structure:

1. Page title and short contextual actions
2. Search or filter panel
3. Batch or row-level actions
4. Main data table
5. Pagination and totals

For forms, default to this structure:

1. Page title and status
2. Sectioned form groups
3. Inline help or validation text only where useful
4. Sticky or clearly separated footer actions

Treat these structural pairings as especially representative of the internal page套路:

- filter panel + action bar + table + pagination
- card container + grouped form items + bottom fixed actions
- drawer panel + compact section headers + footer actions
- detail header + status tag + description blocks + tabs + operation log

## Visual Rules

Use restrained enterprise styling.

- Favor neutral backgrounds, white or light panels, subtle borders, and low-contrast dividers.
- Use one brand accent color for emphasis, not many competing accents.
- Prefer small to medium radii.
- Keep shadows subtle; borders usually matter more than depth.
- Use compact or medium density, not oversized spacing.
- Favor predictable typography scale over expressive display type.
- Keep icons functional and sparse.

## Color Rules

Use a quiet, operational palette.

- Page background: very light neutral
- Panel background: white or near-white
- Primary text: dark neutral with strong contrast
- Secondary text: medium neutral
- Tertiary text: muted neutral
- Border: light neutral line
- Divider: slightly lighter than border
- Primary action color: one clear brand color only
- Success: calm green
- Warning: restrained amber
- Error: restrained red
- Info: muted blue

Apply color with restraint:

- Use the primary action color mainly for primary buttons, active tabs, focused controls, key links, and selected states.
- Use status colors to communicate state, not to decorate large surfaces.
- Keep tables, forms, and cards mostly neutral.
- Prefer tinted backgrounds only for subtle status blocks, notices, or hover states.

Avoid:

- multiple competing brand colors
- large saturated surfaces
- gradient-heavy panels
- decorative color use without semantic meaning

## Typography Rules

Use clear and predictable type hierarchy.

- Page title: one obvious top-level heading
- Section title: one level below the page title
- Body text: readable and compact
- Helper text: smaller and lower contrast than body text
- Table text: compact and consistent
- Button text: short and stable, avoid long phrases

Prefer:

- regular or medium weight for most content
- stronger weight only for titles, key metrics, and important statuses
- compact line height in dense enterprise areas

Avoid:

- oversized headlines
- highly decorative fonts
- excessive weight variation
- overly loose vertical rhythm

## Spacing And Shape Rules

Use a small and repeatable spacing system.

- Inner control spacing: tight and consistent
- Form row spacing: compact to medium
- Section spacing: medium
- Card padding: medium
- Page block spacing: medium to large

Shape rules:

- Inputs, selects, and buttons should use small to medium corner radius
- Cards and panels should feel rectangular and stable
- Avoid pill-heavy UI unless the control semantics require it

## Button Rules

Use a clear action hierarchy.

Button hierarchy:

- Primary button: the main forward action for the current area
- Secondary button: supporting action with less emphasis
- Tertiary or text button: lightweight action for low-priority operations
- Danger button: destructive action only when necessary

Button content:

- Keep labels action-oriented and short
- Prefer verbs such as query, reset, create, save, submit, confirm, cancel, export
- Avoid vague labels like click here or process now

Button usage:

- One primary button per action area is the default
- Put secondary actions beside or before the primary action
- Put destructive actions away from the main cluster unless the workflow clearly centers on deletion
- In dense list pages, row actions should stay concise

Button states:

- Default: clear and readable
- Hover: slightly stronger emphasis
- Active: visibly pressed
- Disabled: lower contrast and no ambiguity about non-interactivity
- Loading: preserve width and show progress clearly

## Form Rules

Forms should feel structured, practical, and easy to scan.

- Group related fields into sections
- Align labels consistently
- Keep common query fields on one line when space allows
- Use advanced filters only when the field count becomes too large
- Place helper text only where the user truly benefits from it
- Keep required markers visible but not visually noisy

Field selection:

- Use text input for direct search and names
- Use select or tree select for controlled vocabularies
- Use date or date-range pickers for temporal filters
- Use business selectors for domain entities when generic inputs would reduce clarity

Validation:

- Validate required fields explicitly
- Show error text near the field
- Avoid interruptive validation before the user has had a chance to complete the input

## Table Rules

Tables are a primary enterprise pattern and should feel stable.

- Keep header structure simple and readable
- Use clear column names
- Align numeric and status data consistently
- Keep row actions compact
- Use pagination when record count is non-trivial
- Prefer top filters plus table rather than embedding too much filtering inside the grid

Table content:

- Include realistic operational columns
- Do not overload the table with low-value decorative fields
- Use status tags or compact indicators for state-heavy columns
- Use truncation carefully and preserve access to full content when needed

Table states:

- Loading state should preserve the table region
- Empty state should explain the absence of data clearly
- Error state should allow retry or correction

## Interaction Rules

Interactions should feel explicit, calm, and reliable.

- Use drawers for lightweight side tasks
- Use modals for confirmation and short workflows
- Use tabs for peer sections within the same entity
- Use inline expansion only when it clearly reduces navigation cost
- Keep pagination behavior predictable
- Preserve context after common actions such as query, reset, save, or close

Feedback:

- Success feedback should be brief and reassuring
- Error feedback should explain what failed and what the user can do next
- Warning feedback should be specific and actionable

## State Rules

Every important page should account for state.

- Default state
- Loading state
- Empty state
- Error state
- Disabled state where relevant
- Success or completion feedback where relevant

For approval or lifecycle flows, represent state with concise tags, indicators, or summary text rather than long prose paragraphs.

Do not generate:

- Glassmorphism
- neon gradients
- playful blobs
- oversized marketing illustrations
- social-media-card aesthetics
- mobile-first consumer styling unless the user explicitly asks for it

## Component Selection Rules

Think in internal component categories even when rendering generic code or mockups.

Prefer these building blocks:

- page header
- filter form
- data table
- status tag
- segmented tabs
- step bar
- drawer
- modal
- empty state
- pagination
- summary card
- key-value description block
- inline form controls
- bottom action bar
- status indicator
- business selector
- search form

Selection heuristics:

- Use a table when the page is record-centric.
- Use a drawer for lightweight create, edit, or inspect flows.
- Use a modal for confirmation or short forms.
- Use tabs when switching between related subdomains on the same entity.
- Use status tags for approval state, enablement state, sync state, and lifecycle state.
- Use summary cards sparingly and keep metrics operational, not promotional.
- Prefer business selectors over plain text fields when the domain obviously involves organizations, locations, resources, categories, objects, or date ranges.
- Prefer a standardized search form and standardized table structure over bespoke filter layouts.
- Prefer a bottom-fixed action area for long forms or approval flows.
- Prefer status dots or tags over verbose status paragraphs.

When describing or generating a page, reference internal-feeling component patterns directly when helpful:

- "Use a base-form-like filter panel"
- "Use a standardized table region"
- "Use a business-selector-like input"
- "Use a fixed footer action bar"
- "Use a standardized data-table block"

## Content Rules

Write UI content like an internal product.

- Use precise operational labels.
- Favor clarity over brand voice.
- Keep button labels short and action-oriented.
- Use realistic enterprise field names, filters, and statuses.
- Prefer explicit empty, loading, and error states.
- Include practical table columns, not placeholder lorem labels.

When the user does not specify fields, infer plausible business fields such as:

- name
- ID or code
- type
- status
- owner
- created time
- updated time
- remarks

Prefer these action labels because they read like internal tools:

- query
- reset
- export
- create
- edit
- submit
- confirm
- cancel
- batch operate
- view detail

Prefer these state labels because they read like operational systems:

- enabled
- disabled
- pending
- processing
- completed
- failed
- archived

## Output Rules

Match the user’s requested medium.

If generating a prototype or design brief:

- Describe the page in terms of sections, controls, states, and interactions.
- Name the component pattern used in each section.
- When useful, annotate the section with an internal-style mapping such as "base-form-like", "business-selector-like", or "standardized-table-like".

If generating HTML, Vue, React, or other frontend code:

- Preserve enterprise spacing and hierarchy.
- Use reusable section wrappers and consistent action placement.
- Keep interactions explicit.
- Include empty, loading, and pagination states when relevant.

If generating Figma or wireframe prompts:

- Specify desktop admin layout.
- Mention compact density.
- Mention restrained enterprise styling.
- Mention filter panel plus table when relevant.
- Mention action hierarchy, state feedback, and neutral color treatment when relevant.

## Safety Boundary

Do not imply technical dependency on any unpublished implementation details.

If the user mentions an internal component system, focus on reproducing its visible design language, structural conventions, and interaction patterns through generic components and clear UI rules.

## Reusable Prompt Pattern

Use this structure when you need to restate the design intent inside the task:

```text
Generate a desktop enterprise prototype that matches an internal component-system style.
Use restrained admin UI patterns, compact spacing, clear section boundaries, filter-panel-plus-table structure where applicable, and practical operational copy.
Avoid consumer-app styling and avoid decorative marketing layouts.
```

## References

Read [page-patterns.md](references/page-patterns.md) when the task needs concrete page archetypes, default sections, or ready-to-reuse prompt snippets.
Read [internal-mapping.md](references/internal-mapping.md) when the task should be closer to the internal naming style, component semantics, and common enterprise page recipes.
Read [ui-spec.md](references/ui-spec.md) when the task needs more explicit color, button, form, table, spacing, and interaction rules.

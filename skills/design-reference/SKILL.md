---
name: design-reference
description: Gives sourced principles for visual design, interface design and data visualization, plus one person's recorded design preferences. Use when designing, reviewing or critiquing a screen, a layout, a colour palette, type, a chart or dashboard, or AI-written text in a UI, and whenever the design work is for the owner whose preferences are recorded.
---

# Design reference

The bank is in `../../docs/`. Every path in this file is relative to this SKILL.md. Each page is
a list of rules, one per heading, each with why, how to apply, what breaking it looks like, and
a source. "The owner" is the person behind the GitHub account new-marty; on that person's machines it
is the user you are working for. Read the page's contents list, then the sections the task touches; cite the rule
headings you used.

## Which page for which task

| Task | Read |
| --- | --- |
| Deciding what a screen is for, its structure, navigation, states, forms, wording, motion, speed, accessibility; reviewing usability | `../../docs/interface-design.md` |
| Hierarchy, spacing, alignment, type, colour palette, icons, depth, density, tokens; making a UI look less generic | `../../docs/visual-design.md` |
| Choosing or fixing a chart, axis, chart colour, title, label, comparison, sparkline or dashboard; writing numbers | `../../docs/data-visualization.md` |
| Any work for the owner, or a choice the owner's taste decides | `../../docs/preferences.md` |
| A working order from purpose to pixels to charts | `../../docs/index.md`, "How to use this when designing" |

## Working for the owner

Read `../../docs/preferences.md` in the sections the task touches, together with the principle
page. The owner's preference wins where the two disagree; each entry links the principle it
agrees with or departs from. Weigh entries by strength: **strong** ones are hard rules,
**stated** ones are clear wishes, **inferred** ones are readings of the owner's choices to
confirm before relying on them.

The entries the owner returns to most often:

- Every question goes to the owner as a screen, a large change as A and B side by side with its intent.
- A tuned screen changes one or two spots at a time, after reading its history, and only through the owner.
- A pointed-out flaw is fixed at its cause in every component that shares it.
- The work is checked on the running screens with real data before the owner sees it.

## Reviewing

Go rule by rule through the relevant sections. For each problem, name the rule heading, the
exact element that breaks it, and the fix. Order findings by how much they cost the user.

## Adding to the bank

When a task turns up a rule or a preference the bank lacks, follow "How to add to it" in
`../../docs/index.md`: one rule per heading, a primary source for a principle, a verbatim dated
quote for a preference.

# design-reference

Principles for interface design and data visualization, each tied to a primary source,
and a record of one person's preferences (the repository owner's), each tied to what they said.
It is written to be read by people and by coding agents, and does not depend on any one project.
The quotes in the preferences page are the owner's own words; the English translations were made
by the page's author with an AI assistant and checked against the originals.

Start at [`docs/index.md`](docs/index.md), which lists the pages and gives a working order for
using them.

| Page | Covers |
| --- | --- |
| [Visual design](docs/visual-design.md) | Hierarchy, grouping, alignment, spacing, type, colour, icons, depth, density, consistency, the generic look |
| [Interface design](docs/interface-design.md) | The user's job, structure, usability heuristics, view states, forms, interface text, motion, speed, accessibility, iteration and review |
| [Data visualization](docs/data-visualization.md) | Chart choice, axes, clutter, colour, labels, context, uncertainty, small screens, numbers in text, honesty |
| [The owner's preferences](docs/preferences.md) | One person's design taste, with dated quotes, linked to the principles it follows or departs from |

For agents, [`skills/design-reference/SKILL.md`](skills/design-reference/SKILL.md) says which
page to read for which task.

To use it from Claude Code:

```
/plugin install design-reference --marketplace new-marty/hl-design-reference
```

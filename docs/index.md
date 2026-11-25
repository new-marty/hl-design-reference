# Design reference

A knowledge bank for designing interfaces, from how they look to how they work, and for turning
data into charts people read correctly. Each principle rests on a primary source: research,
a standard, or a published design system. A separate page records the taste of one person, the owner, each
entry backed by what he said. Nothing here depends on a particular product. The quotes there are
the owner's own words; the English translations were made by the page's author with an AI
assistant and checked against the originals.

<!-- Add a page only when a new area does not fit the four below; list it here. -->

## The pages

| Page | Answers |
| --- | --- |
| [Visual design](visual-design.md) | How should it look? Hierarchy, grouping, alignment, spacing, type, colour, icons, depth, density, consistency, and what makes an interface look generic. |
| [Interface design](interface-design.md) | How should it work? The user's job, structure and navigation, usability heuristics, every state of a view, forms, interface text, motion, speed, touch and accessibility, and how to iterate and review. |
| [Data visualization](data-visualization.md) | How should the numbers be shown? Chart choice, axes, clutter, colour, titles and labels, context, uncertainty, small screens and dashboards, numbers in text, honesty. |
| [The owner's preferences](preferences.md) | What does the owner like and reject? Process, visual, layout and type, colour, motion and interaction, copy and numbers, charts, AI-written text, references. When working for the owner, these preferences override a general principle. |

## How to use this when designing

Work through the list in order. Each step names the rule to read; the links go to the full
rule with its reasons and checks.

1. **Name the job.** Write who opens the screen, in what moment, and what they need to know or
   do. Decide what the page must express before how it looks.
   [Name the user's job before drawing a screen](interface-design.md#name-the-users-job-before-drawing-a-screen),
   [Design for the moment of use](interface-design.md#design-for-the-moment-of-use),
   [Decide what a page must express before deciding how it looks](preferences.md#decide-what-a-page-must-express-before-deciding-how-it-looks).
2. **Keep only what helps a decision.** Cut metrics nobody acts on, and build nothing for data
   that does not exist.
   [Every metric earns its place by helping a decision](preferences.md#every-metric-earns-its-place-by-helping-a-decision),
   [Remove elements that do not help read the data](data-visualization.md#remove-elements-that-do-not-help-read-the-data).
3. **Structure the screen.** One purpose per screen, the most important thing first, summaries
   that open into detail, and main screens that fit one view.
   [Give each screen one purpose and put the most important thing first](interface-design.md#give-each-screen-one-purpose-and-put-the-most-important-thing-first),
   [Disclose progressively, in no more than two levels](interface-design.md#disclose-progressively-in-no-more-than-two-levels),
   [Fit a main screen in one view](preferences.md#fit-a-main-screen-in-one-view).
4. **Design every state.** Empty, loading, partial, stale and error, each saying what it is.
   [Design every state of every view](interface-design.md#design-every-state-of-every-view),
   [Match the loading indicator to the wait](interface-design.md#match-the-loading-indicator-to-the-wait),
   [Label data that is old or incomplete](interface-design.md#label-data-that-is-old-or-incomplete).
5. **Set the hierarchy.** One dominant element, emphasis from weight and colour before size,
   groups shown by space.
   [Decide the order of importance, then make one element dominant](visual-design.md#decide-the-order-of-importance-then-make-one-element-dominant),
   [Group related items by proximity](visual-design.md#group-related-items-by-proximity-and-keep-space-inside-a-group-smaller-than-space-between-groups),
   [Test hierarchy by blurring the screen](visual-design.md#test-hierarchy-by-blurring-the-screen).
6. **Fix the system before the screen.** Spacing and type from a scale, colours named by role
   with one meaning each, one icon family, all from shared tokens.
   [Take every space and size from a fixed scale](visual-design.md#take-every-space-and-size-from-a-fixed-scale-on-a-4-or-8-unit-base),
   [Name colours by role, not by value](visual-design.md#name-colours-by-role-not-by-value),
   [Define what each colour means across the product before using it](preferences.md#define-what-each-colour-means-across-the-product-before-using-it),
   [Build every component from shared tokens](visual-design.md#build-every-component-from-shared-tokens-and-fix-a-drift-everywhere-at-once).
7. **Check legibility and access.** Contrast minimums, colour never the only cue, targets above
   the platform minimum, text that can grow.
   [Meet the WCAG 2.2 contrast minimums](visual-design.md#meet-the-wcag-22-contrast-minimums-for-text-and-for-controls),
   [Never carry information by colour alone](visual-design.md#never-carry-information-by-colour-alone),
   [Make touch targets at least 44 pt (iOS) or 48 dp (Android)](interface-design.md#make-touch-targets-at-least-44-pt-ios-or-48-dp-android).
8. **Draw the charts.** Pick the chart from the reader's question, print the scale, set a range
   that shows the change, give each number a reference, and keep readability above looks.
   [Decide what the reader must learn before choosing a chart type](data-visualization.md#decide-what-the-reader-must-learn-before-choosing-a-chart-type),
   [Show every key number against a reference](data-visualization.md#show-every-key-number-against-a-reference),
   [Print the scale on every chart](preferences.md#print-the-scale-on-every-chart-and-keep-labels-off-the-marks),
   [Write a title that states the finding](data-visualization.md#write-a-title-that-states-the-finding).
9. **Write the words last.** Plain, literal, front-loaded, one language, numbers with units.
   [Write in plain words, front-loaded for people who scan](interface-design.md#write-in-plain-words-front-loaded-for-people-who-scan),
   [Write numbers as numerals, with units and one consistent format](interface-design.md#write-numbers-as-numerals-with-units-and-one-consistent-format).
10. **Check it running, then propose in small steps.** Use the real screen with real data and
    press every control. Show a change next to the current version, with its intent, and fix a
    flaw everywhere it occurs.
    [Check the work yourself on the real screens before showing it](preferences.md#check-the-work-yourself-on-the-real-screens-before-showing-it),
    [Improve a design in small steps, each compared with the current one](interface-design.md#improve-a-design-in-small-steps-each-compared-with-the-current-one),
    [Treat a pointed-out spot as a symptom](preferences.md#treat-a-pointed-out-spot-as-a-symptom-and-fix-the-cause-everywhere).

## How to add to it

- One rule per heading, in the section it belongs to. The heading states the rule as an
  instruction.
- A principle follows its page's shape (why, how to apply, when it is broken) and cites at least
  one primary source: a study, a standard or a published design system. Add the source to the
  page's Sources list.
- A preference carries at least one dated quote, copied verbatim from what the person said, with
  an English translation when the quote is in another language, and its strength. Link the
  principle it agrees with or departs from.
- Give each entry a **See:** line linking a figure or live example where the reader can see the
  rule (a before/after, a diagram, a good and a bad screen). Link only pages you have opened.
- Before adding, search the page for the rule. Extend an existing entry rather than writing a
  second one.
- Write for a stranger: no product names, screen names, tickets or personal data. Generalise
  ("a personal finance app") only when a quote needs the context.

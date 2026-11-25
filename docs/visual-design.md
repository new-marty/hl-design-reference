# Visual design

How an interface looks, and why some choices read more clearly than others: hierarchy,
grouping, alignment, spacing, type, colour, icons, depth, density and consistency, ending
with what makes an interface look generic. Each rule cites the source it rests on.

<!-- Append new principles in the section they belong to; keep one rule per heading and cite it. -->

Each principle has the same parts: the rule as a heading, **Why** (the mechanism or
evidence), **How to apply** (checks you can run on a screen), **When it is broken** (what
you see), and **Sources**.

## Contents

1. [Hierarchy](#hierarchy)
2. [Grouping](#grouping)
3. [Alignment and grids](#alignment-and-grids)
4. [Spacing](#spacing)
5. [Typography](#typography)
6. [Colour](#colour)
7. [Iconography](#iconography)
8. [Depth and elevation](#depth-and-elevation)
9. [Density and targets](#density-and-targets)
10. [Consistency](#consistency)
11. [Avoiding the generic look](#avoiding-the-generic-look)
12. [Sources](#sources)

## Hierarchy

### Decide the order of importance, then make one element dominant

**Why.** Visual hierarchy is the arrangement that lets the eye see elements in order of
intended importance. When everything is emphasised, nothing is, and people scan without a
starting point.

**How to apply.**
- Write down the one thing a person must see first on the screen, then the next two.
- Give the first item the most contrast or size; keep large elements to two at most.
- Use no more than three text sizes for heading, subheading and body on one view.
- Reserve warm, saturated colours such as red for warnings and errors.

**When it is broken.** Several cards, numbers or buttons compete at the same size and
colour; people ask "where do I look?" or miss the main action.

**Sources:** [Gordon, "Visual Hierarchy in UX: Definition", Nielsen Norman Group, 2021](https://www.nngroup.com/articles/visual-hierarchy-ux-definition/)

### Build emphasis with weight, colour and contrast before size

**Why.** Hierarchy comes from contrast with the surroundings, not from any one property.
Weight and colour change emphasis without pushing the layout around, and they survive
when people enlarge text.

**How to apply.**
- Before making text bigger, try a heavier weight or a darker colour for it, or a lighter
  colour for its neighbours.
- De-emphasise secondary text (labels, metadata) with a lower-contrast neutral that still
  meets the contrast minimums below.
- Check that the relative order holds when the system text size is increased.

**When it is broken.** Headings that are only slightly larger than body text and the same
weight; secondary labels shouting at the same colour as the values they label.

**Sources:** [Apple HIG, Typography](https://developer.apple.com/design/human-interface-guidelines/typography); [Gordon, NN/g, 2021](https://www.nngroup.com/articles/visual-hierarchy-ux-definition/)

### Test hierarchy by blurring the screen

**Why.** Blurring removes the words and leaves only mass and contrast, which is what the eye
reads first. A blurred screenshot shows whether the intended element still dominates, and
content such as a strongly coloured photo can override the template's intent.

**How to apply.**
- Blur a screenshot at increasing radii (for example 5, 10 and 20 px) or squint at it.
- Note which shape your eye lands on first at each level; it should be the element you
  ranked first.
- Repeat with real content, not placeholder images.

**When it is broken.** At high blur an icon, photo or decorative block becomes the darkest
or most saturated thing on the screen.

**Sources:** [Gordon, NN/g, 2021](https://www.nngroup.com/articles/visual-hierarchy-ux-definition/)

## Grouping

### Group related items by proximity, and keep space inside a group smaller than space between groups

**Why.** Elements that are close together are perceived as one group, and proximity often
outweighs colour or shape. Distant elements look unrelated and get overlooked.

**How to apply.**
- Put each control next to the content it acts on.
- Make the gap between groups clearly larger than the gap inside a group, for example by
  at least one step on the spacing scale.
- Check every breakpoint: stacking on narrow screens can separate items that belonged
  together.

**When it is broken.** A label sits equally far from the field above and below it; an "Add"
button sits among unrelated "Save" and "Cancel" buttons; a "Skip" link sits in a far corner
and people think they cannot skip.

**Sources:** [Harley, "Proximity Principle in Visual Design", NN/g, 2020](https://www.nngroup.com/articles/gestalt-proximity/); [Material Design 3, Spacing](https://m3.material.io/foundations/layout/grids-spacing/spacing)

### Add a border or box only when spacing cannot show the group

**Why.** A shared boundary creates a strong group, strong enough to override proximity. Used
for decoration, borders and boxes add clutter, and full-width bordered bands can look like
the end of the page so people stop scrolling.

**How to apply.**
- First try whitespace alone. Add a container only if the group is still unclear.
- Prefer a background tint, a shadow or more space over a border.
- Use containers for real units: a card that holds an image with its caption, chrome versus
  content, a row in a comparison.

**When it is broken.** Every section is a bordered card inside another bordered card; lines
separate items that spacing already separated.

**Sources:** [Harley, "The Principle of Common Region", NN/g, 2020](https://www.nngroup.com/articles/common-region/); Wathan and Schoger, [Refactoring UI](https://www.refactoringui.com/) (book), ch. "Use fewer borders"; [Material Design 3, Spacing](https://m3.material.io/foundations/layout/grids-spacing/spacing)

### Make things that work alike look alike, and things that differ look different

**Why.** Items that share a colour, shape or size are read as related and as equally
important. People use this to predict what an element does.

**How to apply.**
- Give every link one colour, and do not use that colour for non-interactive text.
- Give the primary action a treatment no secondary button shares.
- Size items of the same kind identically (thumbnails, avatars), even when the source
  images differ.

**When it is broken.** Two buttons of different importance look the same; a heading uses the
link colour and people tap it; a content block is sized like an ad and gets skipped.

**Sources:** [Harley, "Similarity Principle in Visual Design", NN/g, 2020](https://www.nngroup.com/articles/gestalt-similarity/); [Material Design 3, Spacing](https://m3.material.io/foundations/layout/grids-spacing/spacing)

## Alignment and grids

### Align elements to a small set of shared edges

**Why.** Aligned items are read as related and are easier to scan; indented items are read
as subordinate to the item above them. Few shared edges make a screen look ordered.

**How to apply.**
- Draw vertical guide lines on a screenshot; every text start, icon column and box edge
  should fall on one of a few lines.
- Align leading elements (icons, avatars, thumbnails) in lists to the same column.
- Indent only to show that an item belongs under the one above it.

**When it is broken.** Section titles, list text and card padding each start at slightly
different x positions; icons and labels in a sidebar drift by a pixel or two between rows.

**Sources:** [Apple HIG, Layout](https://developer.apple.com/design/human-interface-guidelines/layout); [Material Design 3, Spacing](https://m3.material.io/foundations/layout/grids-spacing/spacing); [Saarinen et al., "How we redesigned the Linear UI (part II)", Linear, 2024](https://linear.app/now/how-we-redesigned-the-linear-ui)

### Lay content on a column grid that changes with the window size

**Why.** Columns, margins and gutters give every screen the same skeleton, so content lines
up across views. Column count should change with available width while the product's
function stays the same.

**How to apply.**
- Define columns, gutters and margins per breakpoint, and place components on them.
- On narrow screens use fewer columns; on wide screens add columns or show more, rather
  than stretching text across the window.
- Keep the same functions available at every size; change how much is visible, not what
  the app can do.

**When it is broken.** A desktop layout stretches a single text column to the full window
width; a mobile layout drops a feature because it did not fit.

**Sources:** [Material Design 3, Grids](https://m3.material.io/foundations/layout/grids-spacing/grids); [Apple HIG, Layout](https://developer.apple.com/design/human-interface-guidelines/layout)

### Correct alignment by eye where geometric centring looks wrong

**Why.** Shapes with uneven visual weight (a play triangle, a download arrow, round letters)
look off-centre when their bounding boxes are centred.

**How to apply.**
- After centring an asymmetric icon, check it at real size and nudge it until it looks
  centred.
- Add the correction to the icon's own padding, not to each place it is used.

**When it is broken.** A play icon looks pushed to the left inside a round button; a
download arrow looks too low.

**Sources:** [Apple HIG, Icons](https://developer.apple.com/design/human-interface-guidelines/icons)

## Spacing

### Take every space and size from a fixed scale on a 4 or 8 unit base

**Why.** A small set of allowed values makes choices faster and keeps rhythm consistent;
arbitrary values produce near-duplicates (13, 14, 15 px) that read as mistakes. Material
aligns components to an 8dp grid, with 4dp for smaller elements such as icons and type.

**How to apply.**
- Define the scale once (for example 4, 8, 12, 16, 24, 32, 48, 64) and use only its
  tokens for padding, gaps and component sizes.
- Space between steps grows as values grow, so the difference between neighbours stays
  visible.
- Flag any literal spacing value in code review.

**When it is broken.** Padding differs by one or two pixels between similar cards; the same
gap is 14 px in one place and 16 px in another.

**Sources:** [Material Design 2, Spacing methods](https://m2.material.io/design/layout/spacing-methods.html); [Brown, "More Meaningful Typography", A List Apart, 2011](https://alistapart.com/article/more-meaningful-typography/)

### Keep spacing identical between repeated items

**Why.** Consistent spacing between items of the same kind creates a rhythm the eye can
follow, and similar spacing signals that items are related.

**How to apply.**
- Use one gap token for every item in a list, grid or carousel.
- When item heights vary, keep the gap fixed rather than the item positions.

**When it is broken.** Cards in a row have uneven gutters; one list row has extra padding
because its content is longer.

**Sources:** [Material Design 3, Spacing](https://m3.material.io/foundations/layout/grids-spacing/spacing)

## Typography

### Use a type scale with few steps and a fixed ratio

**Why.** A scale ties sizes to one proportion, so headings and body relate to each other
instead of being chosen one at a time. Platforms ship such scales: Material uses a Major
Second ratio around a 14 base, Apple defines named text styles.

**How to apply.**
- Start from the body size, choose a ratio, and derive the other sizes from it.
- Name the steps by role (display, title, body, label) and use only those in code.
- Use the platform's text styles where they exist, so system text scaling works.

**When it is broken.** Ten or more font sizes in one app, several only one pixel apart.

**Sources:** [Brown, A List Apart, 2011](https://alistapart.com/article/more-meaningful-typography/); [Material Design 3, Type scale tokens](https://m3.material.io/styles/typography/type-scale-tokens); [Apple HIG, Typography](https://developer.apple.com/design/human-interface-guidelines/typography)

### Keep lines of running text between 45 and 90 characters

**Why.** Long lines make the eye travel farther back to the start of the next line, and
readers lose their place.

**How to apply.**
- Set a maximum width on text blocks (for example with the `ch` unit in CSS).
- On wide screens add margins or columns instead of widening the text.

**When it is broken.** A paragraph spans a full desktop window; a settings description runs
150 characters per line.

**Sources:** [Butterick, Practical Typography, "Line length"](https://practicaltypography.com/line-length.html); [Apple HIG, Layout (readable width guides)](https://developer.apple.com/design/human-interface-guidelines/layout)

### Set body line height between 120% and 145% of the font size

**Why.** Tighter lines are dense and hard to read; looser lines fall apart into separate
strips. Users may also override spacing, and layouts must survive it.

**How to apply.**
- Use a unitless `line-height` (for example 1.3 to 1.45) for body text.
- Test that nothing clips or overlaps when line height is set to 1.5, paragraph spacing to
  2x, letter spacing to 0.12em and word spacing to 0.16em (WCAG 1.4.12).

**When it is broken.** Multi-line text set at 100%; fixed-height containers that cut off text
when users increase spacing.

**Sources:** [Butterick, "Line spacing"](https://practicaltypography.com/line-spacing.html); [W3C, Understanding SC 1.4.12 Text Spacing](https://www.w3.org/WAI/WCAG22/Understanding/text-spacing.html)

### Use tabular lining numerals wherever figures are compared

**Why.** Tabular figures all have the same width, so digits line up in columns and values do
not jitter when they update. Proportional figures suit running text.

**How to apply.**
- Apply `font-variant-numeric: tabular-nums lining-nums` to tables, totals, timers and any
  number that changes in place.
- Confirm the chosen font actually has the `tnum` feature.

**When it is broken.** A column of amounts has ragged digits; a counting number shifts
sideways on every tick.

**Sources:** [Butterick, "Alternate figures"](https://practicaltypography.com/alternate-figures.html); [MDN, font-variant-numeric](https://developer.mozilla.org/en-US/docs/Web/CSS/font-variant-numeric)

### Right-align numeric columns and give them the same precision

**Why.** Flush-right numbers put units under units, so magnitude can be compared by scanning
down. Consistent decimal places keep the digits aligned.

**How to apply.**
- Right-align numeric columns and their headers; left-align text columns and theirs.
- Use the same number of decimal places in a column.
- Keep rules thin and few; let alignment and spacing do the work.

**When it is broken.** Centred numbers; a column mixing "1,200" and "34.5".

**Sources:** [Rutter, "Web Typography: Designing Tables to be Read, Not Looked At", A List Apart, 2017](https://alistapart.com/article/web-typography-tables/)

### Use few typefaces, and avoid thin weights at small sizes

**Why.** Mixing typefaces blurs hierarchy and makes an interface feel inconsistent. Light and
thin weights are hard to read at small sizes.

**How to apply.**
- Use one family for interface text, a second only with a clear role (for example display
  headings or code).
- For small text prefer Regular, Medium, Semibold or Bold; if a thin weight is required,
  set it larger.

**When it is broken.** Three or four families on one screen; 12 px captions in a Light
weight.

**Sources:** [Apple HIG, Typography](https://developer.apple.com/design/human-interface-guidelines/typography)

### Let text grow to 200% without losing content

**Why.** People with low vision enlarge text. Layouts with fixed heights or truncation lose
content when they do.

**How to apply.**
- Size text in units that follow the user's setting (rem in CSS, text styles on Apple
  platforms).
- Test at 200%: nothing should overlap or be cut off without a way to reach it.
- Keep the hierarchy readable at the larger size.

**When it is broken.** Buttons whose labels vanish at large text sizes; cards that clip the
last line.

**Sources:** [W3C, Understanding SC 1.4.4 Resize Text](https://www.w3.org/WAI/WCAG22/Understanding/resize-text.html); [Apple HIG, Typography](https://developer.apple.com/design/human-interface-guidelines/typography)

## Colour

### Define colours in a perceptual space such as OKLCH

**Why.** HSL lightness does not match perceived lightness: in OKLCH, sRGB blue has a lightness
of 0.45 and sRGB yellow 0.97, though both are "50%" in HSL. Oklab and OKLCH were fitted to
visual data and keep hue and lightness more stable than HSL or CIE LCH, so steps that
look even can be computed.

**How to apply.**
- Write tokens with `oklch()` and build each ramp by stepping L in even increments.
- Hold hue fixed and reduce chroma to fit the gamut, instead of letting the browser clip.
- Provide sRGB fallbacks for wide-gamut values where needed.

**When it is broken.** A "500" yellow and a "500" blue have very different apparent
brightness; a blue ramp drifts toward purple as it lightens.

**Sources:** [W3C, CSS Color Module Level 4, Oklab and OkLCh](https://www.w3.org/TR/css-color-4/#ok-lab); [Ottosson, "A perceptual color space for image processing", 2020](https://bottosson.github.io/posts/oklab/); [Sitnik and Turner, "OKLCH in CSS: why we moved from RGB and HSL", Evil Martians](https://evilmartians.com/chronicles/oklch-in-css-why-quit-rgb-hsl)

### Fix each colour's shades in advance

**Why.** Generating shades on the fly with lighten and darken functions produces many nearly
identical colours. A fixed ramp per colour makes choices quick and keeps them consistent.

**How to apply.**
- Give each hue a ramp of about nine to ten shades, with the middle shade usable as a
  button background, the lightest as a tinted background and the darkest as text.
- Give greys the largest ramp, since text, backgrounds and controls are mostly grey.
- Adding a new shade is a system change; review it as one.

**When it is broken.** A stylesheet with dozens of near-duplicate greys; one-off colours
created by `opacity` or `darken()` in components.

**Sources:** [Wathan and Schoger, Refactoring UI, "Building Your Color Palette"](https://www.refactoringui.com/previews/building-your-color-palette)

### Keep most of the interface neutral and spend accent colour on meaning

**Why.** Colour draws attention only when it is scarce. Apple advises applying colour
sparingly and reserving it for status and primary actions; NN/g suggests about two primary
and two secondary colours in simple designs.

**How to apply.**
- Use neutrals for surfaces, text and most controls.
- Use the accent for the primary action, selection and links; use status colours only for
  status.
- Count the hues on a screen; each should have a reason you can name.

**When it is broken.** Several buttons with coloured backgrounds; decorative colour on
headings, icons and backgrounds so that the real alert does not stand out.

**Sources:** [Apple HIG, Color](https://developer.apple.com/design/human-interface-guidelines/color); [Gordon, NN/g, 2021](https://www.nngroup.com/articles/visual-hierarchy-ux-definition/); [Refactoring UI, "Building Your Color Palette"](https://www.refactoringui.com/previews/building-your-color-palette)

### Name colours by role, not by value

**Why.** Role-based tokens (background, surface, on-surface, primary, error, outline) let a
theme change in one place and keep light, dark and high-contrast variants coherent. Apple's
dynamic colours and Material's colour roles both work this way.

**How to apply.**
- Components reference only role tokens; role tokens reference the palette.
- Never use a role for something else (a separator colour as text, a label colour as a
  background).
- Define a light, dark and increased-contrast value for every role.

**When it is broken.** Hex values inside components; switching to dark mode leaves
hard-coded colours behind.

**Sources:** [Material Design 3, Color roles](https://m3.material.io/styles/color/roles); [Apple HIG, Color](https://developer.apple.com/design/human-interface-guidelines/color); [Design Tokens Community Group, Design Tokens Format Module 2025.10](https://www.designtokens.org/tr/2025.10/format/)

### Use one colour for one meaning

**Why.** People learn what a colour means and apply that meaning everywhere. Reusing the
interactive colour for static text, or red for both "error" and "brand", breaks the
lesson.

**How to apply.**
- Keep a table of colour meanings (interactive, success, warning, error, selected) and check
  new screens against it.
- Do not use the link or accent colour on non-interactive text.

**When it is broken.** A heading in the link colour gets tapped; green means "income" on one
screen and "online" on another.

**Sources:** [Apple HIG, Color](https://developer.apple.com/design/human-interface-guidelines/color); [Harley, NN/g, Similarity, 2020](https://www.nngroup.com/articles/gestalt-similarity/)

### Never carry information by colour alone

**Why.** People with colour-vision deficiencies, and anyone on a poor screen, cannot rely on
hue. WCAG 1.4.1 requires another visual means.

**How to apply.**
- Pair status colours with text, an icon or a shape.
- Underline links in body text, or give them at least 3:1 contrast with surrounding text.
- Mark required fields with a word or symbol, not only a red label.
- Check screens in a greyscale or colour-blindness simulation.

**When it is broken.** A red/green dot with no label; an error field marked only by a red
border.

**Sources:** [W3C, Understanding SC 1.4.1 Use of Color](https://www.w3.org/WAI/WCAG22/Understanding/use-of-color.html)

### Meet the WCAG 2.2 contrast minimums for text and for controls

**Why.** WCAG 2.2 is the standard in force: text needs 4.5:1 against its background (3:1 for
text at least 18 pt, or 14 pt bold), and the parts of controls, focus indicators and
meaningful graphics need 3:1. Thresholds are not rounded: 4.499:1 fails.

**How to apply.**
- Check every text and background token pair, in every theme, and keep the results with
  the tokens.
- Check borders of inputs, selected states, focus rings and chart marks against adjacent
  colours at 3:1.
- Where you can, aim higher for small text; Apple suggests 7:1 for custom colours.

**When it is broken.** Light grey placeholder-like text used for real content; input fields
whose borders disappear on the background.

**Sources:** [W3C, Understanding SC 1.4.3 Contrast (Minimum)](https://www.w3.org/WAI/WCAG22/Understanding/contrast-minimum.html); [W3C, Understanding SC 1.4.11 Non-text Contrast](https://www.w3.org/WAI/WCAG22/Understanding/non-text-contrast.html); [Apple HIG, Dark Mode](https://developer.apple.com/design/human-interface-guidelines/dark-mode)

### Use APCA as a design aid, not as a conformance target

**Why.** APCA predicts perceived text contrast better than the WCAG 2 ratio, including
for dark colours, and ties its levels to size and weight. But it is not part of WCAG: it was
removed from the WCAG 3 draft in 2023, and the September 2026 working draft still says the
contrast algorithm "is yet to be determined".

**How to apply.**
- Pass WCAG 2.2 first; then use APCA levels (for example Lc 75 minimum, Lc 90 preferred for
  body text) to tune dark themes and thin or small type.
- If a pairing passes APCA but fails WCAG 2, document the decision.

**When it is broken.** A team claims "WCAG 3 compliant" contrast; colours pass APCA but fail
an automated WCAG 2 audit.

**Sources:** [W3C, WCAG 3.0 Working Draft, "Text contrast sufficient"](https://www.w3.org/TR/wcag-3.0/); [Roselli, "WCAG3 Contrast as of April 2026"](https://adrianroselli.com/2026/04/wcag3-contrast-as-of-april-2026.html); [APCA in a Nutshell](https://git.apcacontrast.com/documentation/APCA_in_a_Nutshell.html)

### Design dark mode as its own palette, not an inversion

**Why.** Dark mode uses dimmer backgrounds and brighter foregrounds, and many colours are not
simple inversions. Dark grey rather than black shows shadows and elevation. Saturated colours fail
contrast on dark surfaces and produce optical vibration, so they need desaturating.

**How to apply.**
- Use a dark grey base surface (Material recommends `#121212`) rather than pure black.
- Lighten raised surfaces instead of relying on shadows.
- Desaturate accent colours for dark surfaces and re-check contrast.
- Test with Increase Contrast and Reduce Transparency on.

**When it is broken.** Inverted light colours; saturated brand colours that glare on black;
cards that cannot be told from the background.

**Sources:** [Apple HIG, Dark Mode](https://developer.apple.com/design/human-interface-guidelines/dark-mode); [Material Design 2, Dark theme](https://m2.material.io/design/color/dark-theme.html)

## Iconography

### Use one icon family with one grid, stroke weight and perspective

**Why.** Icons from different sets differ in detail, stroke and corner style, and the
mix reads as unfinished. Icons should also match the weight of adjacent text so neither
dominates by accident.

**How to apply.**
- Pick one set; draw any custom icon on its grid (for example 24 units with a 20-unit live
  area) and at its stroke weight.
- Match icon weight to the adjacent text weight.
- Adjust individual icon sizes optically so they look equally large.

**When it is broken.** Filled and outlined icons side by side; a 1.5 px stroke next to a
2 px stroke; one icon visibly larger than its neighbours.

**Sources:** [Apple HIG, Icons](https://developer.apple.com/design/human-interface-guidelines/icons); [Material Design 3, Designing icons](https://m3.material.io/styles/icons/designing-icons)

### Label icons unless their meaning is universal

**Why.** Few icons have a standard meaning (home, print, search); most mean different things
in different products. A visible text label removes the guess.

**How to apply.**
- Put a text label next to any icon whose action is not one of the few universal ones.
- If you cannot think of a fitting icon within about five seconds, use a word instead.
- Do not rely on tooltips; touch screens have no hover.

**When it is broken.** A toolbar of unlabelled glyphs that people hover or tap one by one to
discover.

**Sources:** [Harley, "Icon Usability", NN/g, 2014](https://www.nngroup.com/articles/icon-usability/)

## Depth and elevation

### Use a few elevation levels, each with a fixed meaning

**Why.** Elevation tells people which surface is on top of which. Too many levels lose that
meaning. Material advises a small number of levels and shadows only where needed; Apple
uses two background sets, base and elevated.

**How to apply.**
- Define named levels (for example base, raised, overlay, modal) and map each component to
  one.
- In dark themes, show higher levels with lighter surfaces.
- Use a shadow only to separate a surface from a busy background or to signal it can be
  moved or pressed.

**When it is broken.** Every card has a different shadow; dialogs look no higher than cards.

**Sources:** [Material Design 3, Elevation](https://m3.material.io/styles/elevation/overview); [Apple HIG, Dark Mode](https://developer.apple.com/design/human-interface-guidelines/dark-mode)

### Light every shadow from the same source

**Why.** Real objects share one light. Shadows with different angles look pasted on. As a
surface rises, its shadow should move farther, blur more and fade.

**How to apply.**
- Keep the same ratio of horizontal to vertical offset in every shadow token.
- Scale offset, blur and opacity together from one level to the next.
- Layer two or more shadows for softness, and tint them with the background's hue instead
  of pure black.

**When it is broken.** One card's shadow falls down-right, another's straight down; grey
shadows look dirty on coloured backgrounds.

**Sources:** [Comeau, "Designing Beautiful Shadows in CSS", 2021](https://www.joshwcomeau.com/css/designing-shadows/)

### Keep interactive elements looking interactive

**Why.** In an eyetracking study, pages with weak clickability signifiers (flat ghost
buttons, links styled as text) took 22% longer and drew 25% more fixations than the same
pages with strong signifiers.

**How to apply.**
- Give buttons a fill or a clear outline, and links a distinct colour or underline.
- Use the flattest styles only on simple, conventional layouts with high-contrast controls.
- Check that someone new can point to every tappable element on a screenshot.

**When it is broken.** Text-only buttons that look like labels; cards that are tappable but
look static.

**Sources:** [Moran, "Flat UI Elements Attract Less Attention and Cause Uncertainty", NN/g, 2017](https://www.nngroup.com/articles/flat-ui-less-attention-cause-uncertainty/)

### Use translucent materials sparingly and check contrast over every background

**Why.** Text on a translucent surface sits over whatever scrolls beneath it, so its contrast
changes from place to place. Low blur keeps background detail and distracts.

**How to apply.**
- Use translucency for overlays where you control what is behind, not as a default style.
- Use stronger blur over photos and video.
- Check text contrast against the worst background that can appear, and offer a solid
  fallback when the system asks to reduce transparency.

**When it is broken.** A frosted header whose title becomes unreadable over a bright image;
glass cards on a gradient with grey text.

**Sources:** [Brown, "Glassmorphism: Definition and Best Practices", NN/g, 2024](https://www.nngroup.com/articles/glassmorphism/); [Apple HIG, Color](https://developer.apple.com/design/human-interface-guidelines/color)

## Density and targets

### Choose density for the task, and let people change it

**Why.** Dense layouts help when people scan, view or compare a lot of information, such as
tables, lists and long forms. Some people do not benefit from density, and preferences
differ between desktop and mobile.

**How to apply.**
- Use higher density for data tables and expert, repeated tasks; lower density for
  focused, occasional tasks.
- Change density through spacing and layout first, component size second.
- Do not change density automatically between breakpoints; offer a setting where it
  matters.

**When it is broken.** A table with three rows per screen on a desktop; a mobile form with
controls so close that they are mis-tapped.

**Sources:** [Material Design 3, Density](https://m3.material.io/foundations/layout/grids-spacing/density)

### Keep touch and click targets above the platform minimum

**Why.** Small targets are hard to hit, especially for people with limited dexterity. WCAG 2.2
sets 24 by 24 CSS px as the minimum (or enough spacing); Apple recommends 44 by 44 pt,
Material 48 by 48 CSS px.

**How to apply.**
- Make the hit area at least the platform size even when the visible icon is smaller.
- Do not let dense modes shrink targets below the minimum.
- Check spacing between small adjacent targets with the 24 px circle test.

**When it is broken.** A 16 px close icon with no padding; adjacent list actions that trigger
each other.

**Sources:** [W3C, Understanding SC 2.5.8 Target Size (Minimum)](https://www.w3.org/WAI/WCAG22/Understanding/target-size-minimum.html); [Apple HIG, Accessibility](https://developer.apple.com/design/human-interface-guidelines/accessibility); [Material Design 3, Density](https://m3.material.io/foundations/layout/grids-spacing/density)

## Consistency

### Build every component from shared tokens, and fix a drift everywhere at once

**Why.** Internal consistency lets people transfer what they learned on one screen to the
next. Tokens (named values that can alias other tokens) make the same decision apply
everywhere, and periodic audits catch drift.

**How to apply.**
- Keep colour, type, spacing, radius, shadow and motion values as tokens; components use
  only tokens.
- When one instance looks wrong, search for the same pattern across all components and fix
  them together.
- Audit the product's components side by side on a regular schedule.

**When it is broken.** Three slightly different card paddings; a button style that differs
between two screens because one was copied before a change.

**Sources:** [Krause, "Maintain Consistency and Adhere to Standards", NN/g, 2021](https://www.nngroup.com/articles/consistency-and-standards/); [Design Tokens Format Module 2025.10](https://www.designtokens.org/tr/2025.10/format/)

### Follow platform and web conventions unless a change clearly helps

**Why.** People spend most of their time in other products and arrive with expectations from
them (Jakob's Law). Breaking a convention adds learning cost, so it needs a clear gain.

**How to apply.**
- Use standard placements and patterns for navigation, back, search, forms and settings.
- When you depart from a convention, write down what it gains and test it.
- Keep layouts recognisable as the window or device changes.

**When it is broken.** A custom navigation pattern that has to be explained; a familiar icon
used for an unfamiliar action.

**Sources:** [Krause, NN/g, 2021](https://www.nngroup.com/articles/consistency-and-standards/); [Apple HIG, Layout](https://developer.apple.com/design/human-interface-guidelines/layout)

## Avoiding the generic look

### Know the default choices that make an interface read as generated

**Why.** Generative models reproduce the dominant styles in their training data. Anthropic's
own prompting guide says its model drifts to generic output without guidance: common fonts
(it names Inter, Roboto, Arial and system fonts), purple gradients on white, and predictable
layouts. A 2026 study of 73 sites built with an AI site builder (Boussioux, Zhao and Cho)
put 88% of them into six visual clusters in a representative clustering, and the authors'
satisfaction with their sites did not track how distinctive the sites were. Shin et al. make
the broader argument that vibe-coding tools homogenize web design.

**How to apply.**
- List the defaults your tools produce (framework colour, font stack, radius, shadow,
  layout) and decide each one on purpose.
- Compare a new screen against a few generated ones for the same brief; if it could be
  swapped with them, it has no character yet.
- A common choice is fine when you chose it for a reason; the problem is the unexamined
  stack of defaults.

**When it is broken.** White background, purple-to-blue gradient hero, centred headline,
three feature cards with icons, default sans-serif, rounded-xl everything.

**Sources:** [Anthropic, "Frontend Aesthetics: A Prompting Guide", Claude Cookbook](https://github.com/anthropics/claude-cookbooks/blob/main/coding/prompting_for_frontend_aesthetics.ipynb); [Boussioux, Zhao and Cho, "One Tool, One Taste?", arXiv preprint, 2026](https://arxiv.org/abs/2609.38183); [Shin et al., "Interrogating Design Homogenization in Web Vibe Coding", arXiv preprint, 2026](https://arxiv.org/abs/2603.13036)

### Decide the product's character before choosing styles

**Why.** Typeface, colour, radius and spacing all express a personality; chosen one at a time
from defaults, they express none. Teams that redesign deliberately start from a small
number of inputs and derive the rest. Linear, for example, generates whole themes from
three values (base, accent, contrast) in a perceptual colour space.

**How to apply.**
- Write two or three words for how the product should feel, derived from what it does and
  who uses it, and check each style decision against them.
- Derive the palette, type and shape from a few root decisions rather than picking each
  token separately.
- Commit to the direction across every screen rather than mixing several.

**When it is broken.** A finance tool styled like a game launch page; each screen borrowing a
different reference.

**Sources:** Wathan and Schoger, [Refactoring UI](https://www.refactoringui.com/) (book), ch. "Choose a personality"; [Saarinen et al., Linear, 2024](https://linear.app/now/how-we-redesigned-the-linear-ui); [Anthropic, Claude Cookbook](https://github.com/anthropics/claude-cookbooks/blob/main/coding/prompting_for_frontend_aesthetics.ipynb)

### Choose the typeface on purpose

**Why.** Type carries more of an interface's character than any other single choice. Butterick
argues that system fonts are overexposed and so signal no decision; the same is now true
of the few fonts every template ships.

**How to apply.**
- Try two or three candidate faces on real screens with real data, including numerals,
  before deciding.
- Check the face has the weights, tabular figures and language coverage you need.
- If you keep a common face, make the type scale, weights and spacing your own.

**When it is broken.** The template's font, sizes and weights, unchanged.

**Sources:** [Butterick, "System fonts"](https://practicaltypography.com/system-fonts.html); [Butterick, "Typography in ten minutes"](https://practicaltypography.com/typography-in-ten-minutes.html)

### Remove decoration that carries no information

**Why.** Ornament stands in for character when there is none: borders around everything,
gradients, glows, glass, badges and labels that repeat what the layout already says. Each
adds noise and competes with the content for attention.

**How to apply.**
- For each decorative element, name the information it carries; remove it if there is none.
- Replace borders with spacing or a background tint where spacing works.
- Allow at most one expressive element per screen, and make it about the content.

**When it is broken.** Gradient text, glowing buttons, "New" badges and section eyebrows on
a screen where the data itself is hard to find.

**Sources:** [Refactoring UI](https://www.refactoringui.com/) (book), ch. "Use fewer borders"; [Harley, NN/g, Common Region, 2020](https://www.nngroup.com/articles/common-region/); [Brown, NN/g, Glassmorphism, 2024](https://www.nngroup.com/articles/glassmorphism/); [Anthropic, Claude Cookbook](https://github.com/anthropics/claude-cookbooks/blob/main/coding/prompting_for_frontend_aesthetics.ipynb)

### Be distinctive in the surface, conventional in the behaviour

**Why.** Some sameness is healthy: products built from the same medium arrive at similar
patterns because those patterns work. Chimero calls this designing with the web's grain.
Character belongs in type, colour, imagery and voice; navigation and controls should stay
familiar.

**How to apply.**
- Keep standard interaction patterns; put the product's character into the visual layer and
  the content.
- When a pattern looks like everyone else's, ask whether it is the medium (keep it) or an
  untouched default (decide it).

**When it is broken.** An "original" navigation that people cannot find; or the opposite, a
product that changed nothing from its template.

**Sources:** [Chimero, "The Web's Grain", 2015](https://frankchimero.com/blog/2015/the-webs-grain/); [Krause, NN/g, 2021](https://www.nngroup.com/articles/consistency-and-standards/)

## Sources

Platform and standards
- Apple, Human Interface Guidelines: [Layout](https://developer.apple.com/design/human-interface-guidelines/layout), [Color](https://developer.apple.com/design/human-interface-guidelines/color), [Dark Mode](https://developer.apple.com/design/human-interface-guidelines/dark-mode), [Typography](https://developer.apple.com/design/human-interface-guidelines/typography), [Icons](https://developer.apple.com/design/human-interface-guidelines/icons), [Accessibility](https://developer.apple.com/design/human-interface-guidelines/accessibility)
- Google, Material Design 3: [Spacing](https://m3.material.io/foundations/layout/grids-spacing/spacing), [Grids](https://m3.material.io/foundations/layout/grids-spacing/grids), [Density](https://m3.material.io/foundations/layout/grids-spacing/density), [Elevation](https://m3.material.io/styles/elevation/overview), [Color roles](https://m3.material.io/styles/color/roles), [Type scale tokens](https://m3.material.io/styles/typography/type-scale-tokens), [Designing icons](https://m3.material.io/styles/icons/designing-icons)
- Google, Material Design 2: [Spacing methods](https://m2.material.io/design/layout/spacing-methods.html), [Dark theme](https://m2.material.io/design/color/dark-theme.html)
- W3C, Understanding WCAG 2.2: [1.4.1 Use of Color](https://www.w3.org/WAI/WCAG22/Understanding/use-of-color.html), [1.4.3 Contrast (Minimum)](https://www.w3.org/WAI/WCAG22/Understanding/contrast-minimum.html), [1.4.4 Resize Text](https://www.w3.org/WAI/WCAG22/Understanding/resize-text.html), [1.4.11 Non-text Contrast](https://www.w3.org/WAI/WCAG22/Understanding/non-text-contrast.html), [1.4.12 Text Spacing](https://www.w3.org/WAI/WCAG22/Understanding/text-spacing.html), [2.5.8 Target Size (Minimum)](https://www.w3.org/WAI/WCAG22/Understanding/target-size-minimum.html)
- W3C, [WCAG 3.0 Working Draft](https://www.w3.org/TR/wcag-3.0/)
- W3C, [CSS Color Module Level 4](https://www.w3.org/TR/css-color-4/)
- Design Tokens Community Group, [Design Tokens Format Module 2025.10](https://www.designtokens.org/tr/2025.10/format/)
- MDN, [font-variant-numeric](https://developer.mozilla.org/en-US/docs/Web/CSS/font-variant-numeric)

Research and practitioner writing
- Nielsen Norman Group: [Gordon, Visual Hierarchy in UX (2021)](https://www.nngroup.com/articles/visual-hierarchy-ux-definition/); [Harley, Proximity (2020)](https://www.nngroup.com/articles/gestalt-proximity/); [Harley, Common Region (2020)](https://www.nngroup.com/articles/common-region/); [Harley, Similarity (2020)](https://www.nngroup.com/articles/gestalt-similarity/); [Harley, Icon Usability (2014)](https://www.nngroup.com/articles/icon-usability/); [Moran, Flat UI Elements Attract Less Attention (2017)](https://www.nngroup.com/articles/flat-ui-less-attention-cause-uncertainty/); [Krause, Consistency and Standards (2021)](https://www.nngroup.com/articles/consistency-and-standards/); [Brown, Glassmorphism (2024)](https://www.nngroup.com/articles/glassmorphism/)
- Matthew Butterick, Practical Typography: [Typography in ten minutes](https://practicaltypography.com/typography-in-ten-minutes.html), [Line length](https://practicaltypography.com/line-length.html), [Line spacing](https://practicaltypography.com/line-spacing.html), [Alternate figures](https://practicaltypography.com/alternate-figures.html), [System fonts](https://practicaltypography.com/system-fonts.html)
- Tim Brown, [More Meaningful Typography](https://alistapart.com/article/more-meaningful-typography/), A List Apart, 2011
- Richard Rutter, [Web Typography: Designing Tables to be Read, Not Looked At](https://alistapart.com/article/web-typography-tables/), A List Apart, 2017
- Adam Wathan and Steve Schoger, Refactoring UI: [the book](https://www.refactoringui.com/), [Building Your Color Palette](https://www.refactoringui.com/previews/building-your-color-palette)
- Björn Ottosson, [A perceptual color space for image processing](https://bottosson.github.io/posts/oklab/), 2020
- Andrey Sitnik and Travis Turner, [OKLCH in CSS: why we moved from RGB and HSL](https://evilmartians.com/chronicles/oklch-in-css-why-quit-rgb-hsl), Evil Martians
- Adrian Roselli, [WCAG3 Contrast as of April 2026](https://adrianroselli.com/2026/04/wcag3-contrast-as-of-april-2026.html)
- Inclusive Reading Technologies, [APCA in a Nutshell](https://git.apcacontrast.com/documentation/APCA_in_a_Nutshell.html)
- Josh W. Comeau, [Designing Beautiful Shadows in CSS](https://www.joshwcomeau.com/css/designing-shadows/), 2021
- Karri Saarinen et al., [How we redesigned the Linear UI (part II)](https://linear.app/now/how-we-redesigned-the-linear-ui), Linear, 2024
- Frank Chimero, [The Web's Grain](https://frankchimero.com/blog/2015/the-webs-grain/), 2015
- Anthropic, [Frontend Aesthetics: A Prompting Guide](https://github.com/anthropics/claude-cookbooks/blob/main/coding/prompting_for_frontend_aesthetics.ipynb), Claude Cookbook
- Léonard Boussioux, Ziyi Zhao and Kanghyun Cho, [One Tool, One Taste? How Vibe Coding Trades Collective Diversity for Individual Creativity](https://arxiv.org/abs/2609.38183), arXiv preprint, 2026
- Donghoon Shin et al., [Interrogating Design Homogenization in Web Vibe Coding](https://arxiv.org/abs/2603.13036), arXiv preprint, 2026

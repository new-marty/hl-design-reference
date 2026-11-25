# Data visualization

How to turn numbers into charts and figures that people read correctly: choosing an encoding, setting axes, using colour, writing titles and labels, giving context, showing uncertainty, fitting charts onto small screens and dashboards, and writing numbers in text.
Each rule states what to do, why it works, how to check it, what failure looks like, and where the evidence comes from.

<!-- Append new principles in the section they belong to; keep one rule per heading and cite it. -->

## Contents

1. [Choosing the chart](#choosing-the-chart)
2. [Axes, scales and shape](#axes-scales-and-shape)
3. [Ink, clutter and embellishment](#ink-clutter-and-embellishment)
4. [Colour](#colour)
5. [Titles, labels and annotation](#titles-labels-and-annotation)
6. [Comparison and context](#comparison-and-context)
7. [Uncertainty and missing data](#uncertainty-and-missing-data)
8. [Small charts, phones and dashboards](#small-charts-phones-and-dashboards)
9. [Numbers in text](#numbers-in-text)
10. [Honesty and access](#honesty-and-access)

## Choosing the chart

### Decide what the reader must learn before choosing a chart type

**Why.** A chart type is an answer to a question about the data. Munzner's framework separates *what* the data is (its abstraction), *why* the reader looks at it (the task), and *how* it is drawn (the encoding); the encoding is chosen last, to fit the other two. Datawrapper's guide makes the same point in plain terms: the chart's main statement is the compass for its type, title and colours.

**How to apply.**
- Write the chart's message or the reader's question in one sentence before drawing anything.
- Name the task: compare categories, see change over time, see a share of a whole, see a relationship, find an outlier, look up a value.
- Pick the type that serves that task; if two messages compete, make two charts.
- If the reader only needs the values, use a list or table instead of a chart.

**When it is broken.** A chart picked from a gallery because it looks interesting, which shows the data but answers no question; a dashboard tile whose purpose nobody can state.

**Sources:** [Munzner, *Visualization Analysis and Design*](https://www.cs.ubc.ca/~tmm/vadbook/); [Datawrapper, chart types guide](https://www.datawrapper.de/blog/chart-types-guide); [Apple HIG, Charting data](https://developer.apple.com/design/human-interface-guidelines/charting-data).

### Encode the most important comparison as position on a common scale

**Why.** Cleveland and McGill ranked elementary perceptual tasks by how accurately people judge them, with position along a common scale most accurate and length, angle, area, volume and colour saturation progressively worse. Heer and Bostock replicated the ranking on Mechanical Turk and found area judgments less accurate than angle, and both significantly worse than position.

**How to apply.**
- Put the comparison the reader must make most precisely on a shared axis (dots or bar ends on one baseline).
- Use length for magnitudes when bars share a baseline; use angle and area only for rough proportions.
- Use colour, size and shape for secondary attributes, not for the main quantity.
- When two series must be compared value by value, put them on the same axis rather than in separate panels.

**When it is broken.** A bubble chart used to compare totals that differ by 10%; stacked segments whose middle pieces float on different baselines, so their lengths cannot be compared.

**Sources:** [Cleveland & McGill 1984, *JASA* 79(387)](https://doi.org/10.1080/01621459.1984.10478080) (publisher page is paywalled; the ranking is restated and replicated in the next source); [Heer & Bostock 2010, Crowdsourcing Graphical Perception (CHI)](https://homes.cs.washington.edu/~jheer/files/2010-MTurk-CHI.pdf); [Munzner, VAD marks and channels slides](https://cs.ubc.ca/~tmm/talks/vad/VAD-marks.pdf).

### Match the visual channel to the type of data

**Why.** Munzner's expressiveness principle says a channel must match the data's character: ordered data needs a magnitude channel (position, length, lightness) and categorical data needs an identity channel (hue, shape). An ordered channel on categories implies an order that is not there; a categorical channel on quantities hides the order that is.

**How to apply.**
- Quantities and ordered levels: position, length, lightness, size.
- Categories: hue, shape, spatial region; keep their lightness similar so none looks "more".
- Check every encoding by asking "does this visual difference mean more, or only different?" and whether the data agrees.

**When it is broken.** A rainbow of hues for a ranking from low to high; light-to-dark shades for unrelated product lines, so readers assume the darkest is the biggest.

**Sources:** [Munzner, VAD marks and channels slides](https://cs.ubc.ca/~tmm/talks/vad/VAD-marks.pdf); [ColorBrewer, scheme types](https://colorbrewer2.org/learnmore/schemes_full.html).

### Prefer common chart types, and teach any new one

**Why.** People already know how to read bars, lines and points, so a common type costs nothing to learn. Apple's guidelines recommend common types and say a novel chart has to show people how to read it. Datawrapper notes that unusual types have a learning curve and suggests building up from simple charts.

**How to apply.**
- Start with bar, line, dot or scatter; move to an unusual form only when the common ones cannot answer the question.
- If you use a novel form, add a one-line reading guide or an annotated example the first time it appears.
- Test: can someone new to the product say what the chart shows within a few seconds?

**When it is broken.** A radial or spiral chart for a simple weekly trend; a custom glyph whose legend has to be studied before any value can be read.

**Sources:** [Apple HIG, Charting data](https://developer.apple.com/design/human-interface-guidelines/charting-data); [Datawrapper, chart types guide](https://www.datawrapper.de/blog/chart-types-guide).

### Use bars for amounts by category and lines for change over time

**Why.** Bars encode magnitude as length from a shared baseline, which suits comparing categories or totals per period. A line connects values in one series so the slope shows the size and direction of change. Apple's guidelines describe bars for comparing categories and for per-period sums, lines for trends, and points for individual values, outliers and relationships.

**How to apply.**
- Categories or per-period totals (a count per day): bars.
- A continuous measure sampled over time: a line; add point marks if individual readings matter.
- Two measures against each other: a scatter plot.
- On narrow screens, prefer horizontal bars so category labels can be read without rotation.

**When it is broken.** A line drawn through unordered categories, implying a trend between them; 30 thin vertical columns with rotated labels on a phone.

**Sources:** [Apple HIG, Charts (Marks)](https://developer.apple.com/design/human-interface-guidelines/charts); [Datawrapper, chart types guide](https://www.datawrapper.de/blog/chart-types-guide).

### Avoid pie and donut charts when slices must be compared

**Why.** Slices are read by angle, arc length and area, all less accurate than position. Skau and Kosara found angle to be the least important cue and donuts as accurate as pies, so neither fixes the problem. Datawrapper notes that a 3-point gap is easy to see in a bar chart but nearly invisible in a pie.

**How to apply.**
- Use a pie only to say "this part is most of the whole", with few slices and one dominant one.
- The UK Analysis Function's limits: five categories or fewer, a meaningful whole, sorted by size from 12 o'clock, labelled directly.
- When slices are of similar size, or when shares must be compared across groups, use bars.

**When it is broken.** A pie with nine near-equal slices and a colour legend; two pies side by side to show how shares changed.

**Sources:** [Skau & Kosara 2016, Arcs, Angles, or Areas (EuroVis)](https://kosara.net/papers/2016/Skau-EuroVis-2016.pdf); [Datawrapper, chart types guide](https://www.datawrapper.de/blog/chart-types-guide); [UK Analysis Function, Data visualisation: charts](https://analysisfunction.civilservice.gov.uk/policy-store/data-visualisation-charts/).

### Sort categories by value unless they have a natural order

**Why.** Sorted bars let the eye read rank and find neighbours at once; unsorted bars force a search. The UK Analysis Function guidance ranks bars by value unless the categories have an inherent order such as age bands or time.

**How to apply.**
- Sort nominal categories by the value the chart is about, usually descending.
- Keep natural orders (time, age, size bands, survey scales) as they are.
- In stacked bars, put the most important segment at the baseline and sort by it.

**When it is broken.** Categories in alphabetical or database order, so the largest one hides in the middle.

**Sources:** [UK Analysis Function, Data visualisation: charts](https://analysisfunction.civilservice.gov.uk/policy-store/data-visualisation-charts/).

### Do not put two unrelated scales on one chart

**Why.** With two y-axes, both scales are arbitrary, so the designer controls where lines cross and how steep each looks. Readers still read meaning into crossings and parallel slopes. Datawrapper and the UK Analysis Function both advise against dual-axis charts for general audiences.

**How to apply.**
- Put each measure in its own chart, aligned on the same x-axis.
- If the question is relative growth, index both series to a common start (100 or 0%) and state the base in the subtitle ("index, January = 100"); ONS suggests the same when series differ greatly in size.
- If one series matters most, chart it and annotate the other.

**When it is broken.** Two lines that cross at the "moment of change" only because the right axis was stretched.

**Sources:** [Datawrapper, Why not to use two axes](https://www.datawrapper.de/blog/dualaxis); [UK Analysis Function, Data visualisation: charts](https://analysisfunction.civilservice.gov.uk/policy-store/data-visualisation-charts/); [ONS Service Manual, Small multiple charts](https://service-manual.ons.gov.uk/data-visualisation/chart-types/small-multiple-charts).

### Do not add 3D, shadows or other visual effects to data marks

**Why.** Depth is a weak channel in Munzner's ranking, and perspective makes nearer marks look larger than farther ones of the same value. Few lists "avoid using visual effects in graphs" among his rules for colour, because gradients and shadows change how a mark's colour and size are read.

**How to apply.**
- Draw marks flat, with solid fills.
- No gradients inside bars, no drop shadows, no bevels, no perspective tilt.

**When it is broken.** A 3D pie whose front slice looks largest; bars with gradient fills whose tops look a different value than their bottoms.

**Sources:** [Munzner, VAD marks and channels slides](https://cs.ubc.ca/~tmm/talks/vad/VAD-marks.pdf); [Few 2008, Practical Rules for Using Color in Charts](https://www.perceptualedge.com/articles/visual_business_intelligence/rules_for_using_color.pdf).

## Axes, scales and shape

### Start the value axis of a bar chart at zero

**Why.** A bar encodes its value by its length, so a cut axis breaks the proportion between bar lengths and values. Correll, Bertini and Franconeri found that truncation consistently increased how large readers judged an effect to be, and that marking the break did not remove the bias.

**How to apply.**
- Bars, columns and areas start at zero.
- If zero hides the differences that matter, change the chart (a dot plot or a line), not the axis.
- Do not rely on axis-break symbols to correct the impression.

**When it is broken.** Two bars of 52 and 55 drawn as if one were twice the other.

**Sources:** [Correll, Bertini & Franconeri 2020, Truncating the Y-Axis: Threat or Menace? (CHI)](https://arxiv.org/abs/1907.02035); [UK Analysis Function, Data visualisation: charts](https://analysisfunction.civilservice.gov.uk/policy-store/data-visualisation-charts/); [Apple HIG, Charts (Axes)](https://developer.apple.com/design/human-interface-guidelines/charts).

### Set a line chart's range to show meaningful variation, and say where it starts

**Why.** A line encodes values by position and change by slope, not by distance from zero, so a zero baseline is not required. Apple's example is a heart-rate chart: a zero floor would flatten the differences that matter, which all sit far from zero. Correll et al. show that truncation still enlarges perceived effects, so the range is an editorial choice that needs care.

**How to apply.**
- Choose a range where a change the reader should care about is visible, and no smaller noise looks dramatic.
- Label the lowest tick clearly so readers can see the axis does not start at zero.
- Keep the same range when comparing periods or people, so the slope means the same thing each time.

**When it is broken.** A line auto-scaled to its own minimum and maximum, so a 0.3% wobble fills the whole chart height and reads as a crash.

**Sources:** [Apple HIG, Charts (Axes)](https://developer.apple.com/design/human-interface-guidelines/charts); [Correll, Bertini & Franconeri 2020](https://arxiv.org/abs/1907.02035); [UK Analysis Function, Data visualisation: charts](https://analysisfunction.civilservice.gov.uk/policy-store/data-visualisation-charts/).

### Fix the axis range when the bounds have meaning

**Why.** Apple distinguishes fixed ranges, where the minimum and maximum mean something (a battery from 0% to 100%), from dynamic ranges that fit the current data. A dynamic range on bounded data makes a half-full value look full.

**How to apply.**
- Percent of a whole, scores out of a maximum, progress toward a goal: fixed range.
- Open-ended amounts that vary widely: dynamic range, with the top near the largest value.
- When charts sit side by side for comparison, give them the same range.

**When it is broken.** A completion bar at 40% that fills the chart because the axis maximum is 40%.

**Sources:** [Apple HIG, Charts (Axes)](https://developer.apple.com/design/human-interface-guidelines/charts).

### Use round tick values and a few light gridlines

**Why.** Familiar sequences (0, 5, 10) are understood at a glance; unusual ones (1, 6, 11) make people work out the interval. Gridlines help estimate values far from an axis, but too many compete with the data. Heer and Bostock had people set gridlines as light as possible while still usable and report the resulting alpha values; the UK Analysis Function suggests at most ten light grey gridlines.

**How to apply.**
- Ticks at 1, 2, 2.5 or 5 times a power of ten.
- Gridlines light grey, thinner than data marks, at most about ten.
- Fewer gridlines when the chart offers a scrubber or tooltips for exact values.

**When it is broken.** Ticks at 13, 26, 39; dark gridlines as heavy as the data line.

**Sources:** [Apple HIG, Charts (Axes)](https://developer.apple.com/design/human-interface-guidelines/charts); [Heer & Bostock 2010](https://homes.cs.washington.edu/~jheer/files/2010-MTurk-CHI.pdf); [UK Analysis Function, Data visualisation: charts](https://analysisfunction.civilservice.gov.uk/policy-store/data-visualisation-charts/).

### Choose an aspect ratio that makes slopes readable

**Why.** Cleveland's "banking to 45 degrees" sets a line chart's aspect ratio so that line segments average about 45 degrees, where differences in slope are easiest to see. Heer and Agrawala extended it to multiple scales. Tufte applies the same idea to sparklines: wider than tall, shaped so the line looks "lumpy", neither flat nor spiky.

**How to apply.**
- Line charts: usually wider than tall; check that the main trend is neither a flat line nor a cliff.
- For several series or panels, pick one ratio from the average across them so they stay comparable.
- On a phone, a full-width chart is often too flat; give it more height or fewer periods.

**When it is broken.** A year of data squeezed into a short strip so every change looks flat; a narrow tall chart that turns small noise into spikes.

**Sources:** [Heer & Agrawala 2006, Multi-Scale Banking to 45 Degrees (InfoVis)](https://idl.uw.edu/papers/banking); [Tufte, Sparkline theory and practice](https://www.edwardtufte.com/notebook/sparkline-theory-and-practice-edward-tufte/).

## Ink, clutter and embellishment

### Remove elements that do not help read the data

**Why.** Tufte's data-ink ratio argues that most of a chart's ink should show data. Schwabish's three guidelines for economists are to show the data, reduce the clutter, and integrate text and graph. Knaflic shows the same effect step by step: each removed border, marker or label is a small change, but together they make the chart much easier to read.

**How to apply.**
- Remove chart borders, background fills, heavy axis lines, redundant tick labels and data markers that repeat the line.
- Remove a legend when direct labels can do its job.
- Before removing an element, ask what the reader would lose; keep it if the answer is "a value they need".

**When it is broken.** A default spreadsheet chart: boxed, gridded, shaded, with a legend for a single series.

**Sources:** [Tufte, *The Visual Display of Quantitative Information*](https://www.edwardtufte.com/book/the-visual-display-of-quantitative-information/); [Schwabish 2014, An Economist's Guide to Visualizing Data, *JEP* 28(1)](https://www.aeaweb.org/articles?id=10.1257/jep.28.1.209) (full text was not reachable when this page was written; the three guideline names are as listed in [Kasy's course slides](https://maxkasy.github.io/home/files/teaching/TopicsEconometrics2019/DataVisualization-Slides.pdf), a secondary source); [Knaflic, Declutter this graph](https://www.storytellingwithdata.com/blog/2017/3/29/declutter-this-graph).

### Make supporting elements just visible enough

**Why.** Axes, gridlines and labels are needed, but they should not compete with the data. Few's rule: non-data components should be "just visibly enough to perform their role, but no more so". Apple's guidelines ask for a visual hierarchy where the data is most prominent and the axes and descriptions give context.

**How to apply.**
- Data marks: full strength. Axes, gridlines, secondary labels: lighter and thinner.
- Squint test: with eyes half closed, the data shape should be the first thing visible.
- Text that is less important (source, notes) is small and grey, but must still meet contrast requirements.

**When it is broken.** Gridlines and axis labels in the same dark colour and weight as the data line.

**Sources:** [Few 2008, Practical Rules for Using Color in Charts (Rule 7)](https://www.perceptualedge.com/articles/visual_business_intelligence/rules_for_using_color.pdf); [Apple HIG, Charts (Best practices)](https://developer.apple.com/design/human-interface-guidelines/charts).

### Allow imagery only when it carries data or stays out of the way

**Why.** The evidence on embellishment is more nuanced than "all chartjunk is bad". Bateman et al. found that embellished charts were interpreted no less accurately than plain ones and recalled better after two to three weeks, though the authors are cautious about recommending the style for all charts. Haroz, Kosara and Franconeri found that superfluous images can distract, while pictographs that represent the data itself had no cost and some benefits. Borkin et al. found that colour, recognizable objects and unusual chart types make a visualization more memorable; being remembered is a different quality from being read accurately.

**How to apply.**
- Decide which you need: recall of one message, or accurate reading of values.
- If you use pictographs, make them the marks (one icon per unit), not a background.
- Keep decoration out of the plot area and away from the values.
- Use imagery for charts that must be remembered (a one-off story), not for charts used daily to check values.

**When it is broken.** A large illustration behind the bars that hides gridlines and makes the bar ends hard to find; a striking custom chart that people remember seeing but cannot tell you anything from.

**Sources:** [Bateman et al. 2010, Useful Junk? (CHI)](https://vis.csail.mit.edu/classes/6.859/readings/pdfs/Bateman-UsefulJunk.pdf); [Haroz, Kosara & Franconeri 2015, ISOTYPE Visualization (CHI)](https://tableau.com/sites/default/files/2023-01/Haroz_CHI_2015.pdf); [Borkin et al. 2013, What Makes a Visualization Memorable? (InfoVis)](https://vcg.seas.harvard.edu/publications/20130101-what-makes-a-visualization-memorable).

## Colour

### Use colour only when it carries meaning

**Why.** Few's rules are to use colour only when it serves a communication goal, and to use different colours only when they correspond to differences in the data. Colour that only decorates makes readers look for a meaning that is not there.

**How to apply.**
- A single series gets a single colour.
- Every colour in the chart should be explainable in one sentence ("orange is this year").
- Use the same colour for the same thing across charts on a page, and never for two different things.

**When it is broken.** Each bar of a single series in a different colour; "blue" meaning revenue on one chart and cost on the next.

**Sources:** [Few 2008, Practical Rules for Using Color in Charts (Rules 3 and 4)](https://www.perceptualedge.com/articles/visual_business_intelligence/rules_for_using_color.pdf); [Datawrapper, What to consider when choosing colors](https://www.datawrapper.de/blog/colors); [Apple HIG, Charting data](https://developer.apple.com/design/human-interface-guidelines/charting-data).

### Pick the palette type from the data: sequential, diverging or categorical

**Why.** ColorBrewer's three scheme types map to three kinds of data. Sequential schemes run from light (low) to dark (high) for ordered data. Diverging schemes put a light neutral at a meaningful midpoint (zero, average, target) and darken toward two contrasting hues. Qualitative schemes vary hue at similar lightness for categories with no order.

**How to apply.**
- Ordered values: one hue, or a few close hues, light to dark (Few, Rule 6).
- Values above and below a reference: diverging, with the reference at the neutral centre; Datawrapper suggests a light grey centre rather than white.
- Categories: distinct hues of similar lightness.

**When it is broken.** A diverging red-blue scheme on data with no midpoint, so readers see a "good" and "bad" half that does not exist.

**Sources:** [ColorBrewer, scheme types](https://colorbrewer2.org/learnmore/schemes_full.html); [Few 2008 (Rule 6)](https://www.perceptualedge.com/articles/visual_business_intelligence/rules_for_using_color.pdf); [Datawrapper, choosing colors](https://www.datawrapper.de/blog/colors).

### Use perceptually uniform colour scales, not rainbows

**Why.** Crameri, Shephard and Heron show that rainbow and other non-uniform colour maps distort data: uneven lightness steps create boundaries that are not in the data, and red-green maps are unreadable for many readers. Perceptually uniform maps (such as viridis or batlow) change by equal visual steps and stay ordered in greyscale.

**How to apply.**
- For continuous data, use a tested uniform map, not the tool's default rainbow.
- Convert the chart to greyscale; the order of values should still be readable.
- Check the scale with a colour-vision-deficiency simulator.

**When it is broken.** A heat map where a band of bright yellow in the middle of a rainbow scale reads as a sharp edge in smooth data.

**Sources:** [Crameri, Shephard & Heron 2020, The misuse of colour in science communication (*Nature Communications*)](https://www.nature.com/articles/s41467-020-19160-7).

### Keep context grey and spend one strong colour on the point

**Why.** Attention goes to whatever differs most. Few's Rule 5 is to use soft, natural colours for most information and bright or dark colours only for what needs attention. Knaflic's test is to look away and back and see where the eye lands; Few's dashboard pitfalls include "when everything is visually prominent, nothing stands out". Datawrapper calls grey the most important colour in data vis.

**How to apply.**
- Draw comparison series, past periods and reference lines in grey.
- Give the series or value the reader should look at one saturated colour.
- Run the "where do my eyes land first?" check; it should land on the message.

**When it is broken.** Eight equally bright series, so the one the title talks about is not where the eye goes.

**Sources:** [Few 2008 (Rule 5)](https://www.perceptualedge.com/articles/visual_business_intelligence/rules_for_using_color.pdf); [Knaflic, Where are your eyes drawn?](https://www.storytellingwithdata.com/blog/whereareyoureyesdrawn); [Few 2006, Common Pitfalls in Dashboard Design (Pitfall 10)](https://www.perceptualedge.com/articles/Whitepapers/Common_Pitfalls.pdf); [Datawrapper, choosing colors](https://www.datawrapper.de/blog/colors).

### Limit the number of categorical colours

**Why.** Each extra colour must be matched to its meaning, and beyond a handful readers keep returning to the key. Datawrapper suggests about seven colours at most; the UK Analysis Function suggests at most four lines on a line chart and four categories in a stack.

**How to apply.**
- More than about five categories: group the small ones into "Other", highlight one or two and grey the rest, or split into small multiples.
- Do not cycle a palette so two categories share a colour.

**When it is broken.** Twelve coloured lines with a twelve-entry legend.

**Sources:** [Datawrapper, choosing colors](https://www.datawrapper.de/blog/colors); [UK Analysis Function, Data visualisation: charts](https://analysisfunction.civilservice.gov.uk/policy-store/data-visualisation-charts/).

### Never let colour be the only way to tell data apart

**Why.** WCAG 1.4.1 requires that colour is not the only visual means of conveying information. Crameri et al. cite a common estimate that about 8% of men and 0.5% of women have a colour-vision deficiency. Datawrapper notes that the only reliable fix is a second encoding (position, shape, pattern or a label); varying lightness also helps, because lightness differences survive most deficiencies.

**How to apply.**
- Pair colour with a direct label, a marker shape, a line style or position.
- Give categorical colours different lightness; avoid red-green pairs of similar lightness (Few, Rule 8).
- Make each needed line or mark at least 3:1 against its background (WCAG 1.4.11).
- Put separators between adjacent filled areas such as stacked segments (Apple HIG).

**When it is broken.** "Over budget" shown only in red and "under" only in green, at the same lightness, with no label or sign.

**Sources:** [W3C, Understanding SC 1.4.1 Use of Color](https://www.w3.org/WAI/WCAG22/Understanding/use-of-color.html); [W3C, Understanding SC 1.4.11 Non-text Contrast](https://www.w3.org/WAI/WCAG22/Understanding/non-text-contrast.html); [Datawrapper, visualizing data for colorblind readers](https://www.datawrapper.de/blog/colorblindness-part2); [Crameri et al. 2020](https://www.nature.com/articles/s41467-020-19160-7); [Apple HIG, Charts (Color)](https://developer.apple.com/design/human-interface-guidelines/charts); [ColorBrewer (colourblind-safe filter)](https://colorbrewer2.org/).

## Titles, labels and annotation

### Write a title that states the finding

**Why.** Readers look at the title first and use it to decide what the chart says. The UK Analysis Function recommends a headline title stating the main message plus a statistical subtitle; the data.europa.eu guide asks for the message in ten words or fewer; Datawrapper says to give the main statement first and the precise explanation later. Apple's guidelines ask charts to summarise their main message so it can be grasped quickly.

**How to apply.**
- Title: a sentence with the finding ("Spending fell for the third month").
- Subtitle: what is measured, unit, period, population.
- Keep technical terms and exact precision out of the title.
- For an exploratory chart with no single message, title it with the question the reader can explore.

**When it is broken.** "Monthly spending, Jan to Dec" above a chart whose point is a drop in March that the reader has to find alone.

**Sources:** [UK Analysis Function, Data visualisation: charts](https://analysisfunction.civilservice.gov.uk/policy-store/data-visualisation-charts/); [data.europa.eu, Guidelines for visualisation titles](https://data.europa.eu/apps/data-visualisation-guide/guidelines-for-visualisation-titles); [Datawrapper, text in data visualizations](https://www.datawrapper.de/blog/text-in-data-visualizations); [Apple HIG, Charts (Descriptive content)](https://developer.apple.com/design/human-interface-guidelines/charts).

### Make the title say only what the data supports

**Why.** Kong, Liu and Karahalios showed the same chart with titles slanted in opposite directions, and viewers took away opposite main messages. A title is the strongest framing device on the chart, so it must not claim more than the data shows. The data.europa.eu guide adds that a title must not contradict the pattern visible in the chart.

**How to apply.**
- Check every claim in the title against the plotted values.
- Avoid causal words ("because of", "drove") unless the data shows the cause.
- When the data is weak (few points, high noise), say so in the title or subtitle.

**When it is broken.** "Savings habit is working" over two months of data that rose once.

**Sources:** [Kong, Liu & Karahalios 2018, Frames and Slants in Titles of Visualizations on Controversial Topics (CHI)](https://mail.zcliu.cs.umd.edu/vistitles/CHI18-VisTitles.pdf); [data.europa.eu, Guidelines for visualisation titles](https://data.europa.eu/apps/data-visualisation-guide/guidelines-for-visualisation-titles).

### Label series directly instead of using a legend

**Why.** A legend makes the reader hold a colour in memory and search for it, and it fails for readers who cannot tell the colours apart. Datawrapper's principle is to place the words that explain chart elements as close to those elements as possible. The UK Analysis Function recommends labelling lines at their ends and stacks directly.

**How to apply.**
- Put the series name at the end of each line, next to each bar group, or inside large segments.
- Colour the label text like its series, or keep it dark grey and adjacent.
- If labels would collide, use short leader lines, fewer series, or small multiples.
- If a legend is unavoidable, order it like the data.

**When it is broken.** A legend box in a corner with five colour swatches for five lines that cross each other.

**Sources:** [Datawrapper, text in data visualizations](https://www.datawrapper.de/blog/text-in-data-visualizations); [UK Analysis Function, Data visualisation: charts](https://analysisfunction.civilservice.gov.uk/policy-store/data-visualisation-charts/); [Datawrapper, colorblind readers](https://www.datawrapper.de/blog/colorblindness-part2).

### Annotate the points that explain the pattern

**Why.** An annotation puts the explanation where the eye already is. Datawrapper calls annotations an extremely powerful tool for explanatory charts, for explaining outliers or unusual values; Apple recommends descriptive text and annotations to highlight actionable takeaways. Schwabish's third guideline is to integrate text and graph.

**How to apply.**
- Annotate outliers, breaks in the series, events that changed the data, and the latest value.
- Keep each note to one line, placed next to what it explains.
- On small screens, drop the least important notes or move them below the chart.

**When it is broken.** A spike with no note, so readers guess whether it is real, a data error, or a one-off.

**Sources:** [Datawrapper, text in data visualizations](https://www.datawrapper.de/blog/text-in-data-visualizations); [Apple HIG, Charting data](https://developer.apple.com/design/human-interface-guidelines/charting-data); [Schwabish 2014, *JEP*](https://www.aeaweb.org/articles?id=10.1257/jep.28.1.209).

## Comparison and context

### Show every key number against a reference

**Why.** A number alone does not say whether it is good or bad. Few's second dashboard pitfall is inadequate context: "Compared to what? Is this good or bad?" He recommends adding comparative measures (a target, history) and a quick visual cue for qualitative state. His bullet graph puts the measure, one or two comparison marks, and qualitative ranges in one small linear display.

**How to apply.**
- Pick the reference the reader judges by: a target, the same period last time, a typical range, or a peer average.
- Show it in the same view: a reference line, a target tick, or a grey band.
- Name the reference in words ("vs. last month").

**When it is broken.** A large headline number with no target, history or range, so the reader cannot tell if action is needed.

**Sources:** [Few 2006, Common Pitfalls in Dashboard Design (Pitfall 2)](https://www.perceptualedge.com/articles/Whitepapers/Common_Pitfalls.pdf); [Few, Bullet Graph Design Specification](https://www.perceptualedge.com/articles/misc/Bullet_Graph_Design_Spec.pdf).

### Show the difference directly when the difference is the point

**Why.** Few's fourth pitfall: if the reader needs to know how far actual is from budget, showing the two amounts and leaving the subtraction to them is indirect. Showing the variance, often as a percentage, puts the answer on the screen and makes items of different sizes comparable.

**How to apply.**
- If the question is "how far off", plot or print the gap, signed.
- Use a percentage when items differ in scale; use an absolute amount when the amount itself matters.
- Keep the two raw values available on demand.

**When it is broken.** Two bars per category labelled "plan" and "actual", with the over- or under-spend left for mental arithmetic.

**Sources:** [Few 2006, Common Pitfalls in Dashboard Design (Pitfall 4)](https://www.perceptualedge.com/articles/Whitepapers/Common_Pitfalls.pdf).

### Show the normal range as a band behind the data

**Why.** A typical range answers "is this unusual?" without another chart. Tufte recommends a grey band for normal limits behind a sparkline, so readings outside it stand out. Brehmer et al. tested this pattern on phone-sized charts (observed daily ranges with an average range superimposed, as in weather apps), and comparison tasks against the superimposed range performed similarly across the layouts they tried.

**How to apply.**
- Compute the band from the reader's own history or a stated norm, and say how it was computed.
- Draw it light grey behind the data, never over it.
- Mark values outside the band with a modest accent, not an alarm colour for every point.

**When it is broken.** A wavy line with no sense of whether this week's value is ordinary or extreme.

**Sources:** [Tufte, Sparkline theory and practice](https://www.edwardtufte.com/notebook/sparkline-theory-and-practice-edward-tufte/); [Brehmer et al. 2019, Visualizing Ranges over Time on Mobile Phones (TVCG)](https://www.microsoft.com/en-us/research/publication/visualizing-ranges-over-time-on-mobile-phones-a-task-based-crowdsourced-evaluation/).

### Split tangled series into small multiples with shared scales

**Why.** Tufte's small multiples repeat one chart design for each subset, so the eye learns the design once and compares the data. Datawrapper recommends them to untangle overlapping lines; ONS recommends them when there are too many series for one chart, and says comparisons within a panel are easier than across panels.

**How to apply.**
- Same chart type, size and scales in every panel; if scales must differ, say so.
- Draw the other series or an average in grey in each panel for context.
- Order panels meaningfully (by latest value, by change) and say how.
- Keep to about 12 panels or fewer; on a phone, fewer.

**When it is broken.** Panels with independent y-axes, so a small change in one panel looks as large as a big change in another.

**Sources:** [Tufte, *Envisioning Information*](https://www.edwardtufte.com/book/envisioning-information/); [Datawrapper, small multiple line charts](https://www.datawrapper.de/blog/what-to-consider-when-creating-small-multiple-line-charts); [ONS Service Manual, Small multiple charts](https://service-manual.ons.gov.uk/data-visualisation/chart-types/small-multiple-charts).

## Uncertainty and missing data

### Show uncertainty, and show it as outcomes people can count

**Why.** Estimates, forecasts and projections have spread, and hiding it overstates precision. Kay et al. found that quantile dotplots (a forecast drawn as a small number of equally likely dots) reduced the variance of people's probability estimates compared with density plots on a phone. Hullman, Resnick and Adar found that hypothetical outcome plots (animated draws) led to much more accurate judgments than error bars or violin plots when comparing two or three quantities.

**How to apply.**
- For a forecast or estimate, show a range, not only a point.
- For lay readers, prefer frequency formats: "in 17 of 20 likely outcomes", dot counts, a band labelled with what it means.
- Label what the range is (a 90% interval, last year's spread).

**When it is broken.** A projected month-end figure shown as one exact number with no range.

**Sources:** [Kay et al. 2016, When(ish) is My Bus? (CHI)](https://idl.uw.edu/papers/when-ish-is-my-bus); [Hullman, Resnick & Adar 2015, Hypothetical Outcome Plots (PLOS ONE)](https://idl.uw.edu/papers/hops).

### Do not draw a distribution as a bar with an error bar

**Why.** Correll and Gleicher describe "within-the-bar bias": values inside a bar are seen as more likely than values outside it, even though an interval is symmetric around the mean. Error bars also suggest all-or-nothing reading, inside or outside. Encodings that are visually symmetric around the mean, such as gradient or violin plots, reduce these errors.

**How to apply.**
- For a mean with uncertainty, use a point with an interval, a gradient band, or a violin, not a filled bar.
- Explain the interval in words next to the chart.

**When it is broken.** A tall bar with a thin whisker, read as "the true value is somewhere in the bar".

**Sources:** [Correll & Gleicher 2014, Error Bars Considered Harmful (InfoVis)](https://graphics.cs.wisc.edu/Papers/2014/CG14/Preprint.pdf).

### Mark missing and estimated values; never fill them with zero

**Why.** Song and Szafir tested many ways of drawing incomplete time series. Highlighting imputed values and using linear interpolation produced the highest perceived data quality and confidence; zero-filling, downplaying, and simply not drawing missing data lowered it, and designs that break continuity could bias interpretation. A zero in place of a missing value is also false: it says "nothing happened" when the truth is "we do not know".

**How to apply.**
- Distinguish three states visually: measured, estimated, missing.
- Draw estimated segments dashed or lighter, and say how they were estimated.
- Never plot a missing value as zero; if the gap matters, show it as a gap with a note.
- In text, write "no data" rather than "0".

**When it is broken.** A sync failure that shows as a day of zero activity, dragging the weekly average down.

**Sources:** [Song & Szafir 2019, Where's My Data? Evaluating Visualizations with Missing Data (TVCG)](https://par.nsf.gov/servlets/purl/10111567); [project page](https://cmci.colorado.edu/visualab/MissingData).

## Small charts, phones and dashboards

### Make sparklines word-sized and label the latest value

**Why.** Tufte defines a sparkline as "a small intense, simple, word-sized graphic with typographic resolution"; it sits inline with text or in a table. Their job is shape at a glance, so they need the number beside them to be read.

**How to apply.**
- Height about a line of text; width enough to show the shape.
- Label the latest value, tied to the line's end with a small accent; add the first value if the change matters.
- No frame or axis; show a normal-range band if one exists.
- Use the same vertical scale for sparklines that sit in one column, or say they differ.

**When it is broken.** A tiny line with no number, so the reader sees "up" but not from what or to what.

**Sources:** [Tufte, Sparkline theory and practice](https://www.edwardtufte.com/notebook/sparkline-theory-and-practice-edward-tufte/).

### Give a chart enough height for the comparison it supports

**Why.** Heer and Bostock varied chart height for value comparisons: charts 40 pixels tall produced significantly more error, while 80, 160 and 320 pixels did not differ, so accuracy plateaued and there was little benefit beyond about 80 pixels in their setup. A glanceable chart can be small; a chart for comparing values cannot be very small.

**How to apply.**
- Decide whether the chart is for shape at a glance (small is fine) or for comparing values (give it room).
- Do not shrink a comparison chart until the bars or points are only a few pixels apart.
- If space is short, show fewer periods rather than squeezing all of them.

**When it is broken.** A dashboard tile where bars differ by one or two pixels and the reader is expected to rank them.

**Sources:** [Heer & Bostock 2010](https://homes.cs.washington.edu/~jheer/files/2010-MTurk-CHI.pdf); [Apple HIG, Charting data](https://developer.apple.com/design/human-interface-guidelines/charting-data).

### On phones, use linear layouts and give the plot the full width

**Why.** Brehmer et al. found that on phones people completed range-over-time tasks faster with linear layouts than radial ones, with similar error. Apple advises maximising plot width in compact layouts and keeping vertical-axis labels short. Datawrapper prefers horizontal bars on small screens because labels fit.

**How to apply.**
- Linear time axes; avoid radial and circular layouts for time series.
- Short y-axis labels; move units into the title.
- Horizontal bars for many categories; fewer periods per view.
- Check every chart at 320 to 400 CSS pixels wide.

**When it is broken.** A desktop chart scaled down so labels overlap and rotate, with the y-axis labels taking a third of the width.

**Sources:** [Brehmer et al. 2019 (TVCG)](https://www.microsoft.com/en-us/research/publication/visualizing-ranges-over-time-on-mobile-phones-a-task-based-crowdsourced-evaluation/); [Apple HIG, Charts (Best practices)](https://developer.apple.com/design/human-interface-guidelines/charts); [Datawrapper, chart types guide](https://www.datawrapper.de/blog/chart-types-guide).

### Do not hide critical information behind interaction

**Why.** Apple's guidelines say to let people interact with data when it helps, but not to require interaction to reveal critical information. Readers who do not tap, or who use assistive technology, will otherwise miss it. Small marks are also hard to hit with a finger.

**How to apply.**
- The message, the latest value and the reference are visible without touching anything.
- Tooltips and scrubbing add detail; they do not carry the main point.
- Make the whole plot area the touch target for scrubbing, rather than each tiny mark.

**When it is broken.** A chart whose only label appears on hover, on a phone with no hover.

**Sources:** [Apple HIG, Charts (Best practices)](https://developer.apple.com/design/human-interface-guidelines/charts).

### Design a dashboard to be read on one screen, with the important item first

**Why.** Few's first dashboard pitfall is exceeding a single screen: once data scrolls out of view, it cannot be compared, and short-term memory holds only a few chunks. His tenth is failing to highlight what matters: when everything is prominent, nothing stands out. His third is excessive precision, which slows a reader who is monitoring.

**How to apply.**
- Fit the items that must be compared into one view; move detail to drill-down screens.
- Order by importance; make the item that most needs attention the most visible one.
- Use the same chart style for the same kind of measure across tiles; Apple asks for consistency across charts with a similar purpose.
- A metric keeps its colour, unit and chart type when its tile opens into a detail view (Apple: continuity across charts of the same data).
- Remove logos, decoration and controls from the visual foreground.

**When it is broken.** Ten tiles of equal weight in bright colours, each with a different chart type and six-digit precision; a metric shown as a green line on the summary and as blue bars on its detail page.

**Sources:** [Few 2006, Common Pitfalls in Dashboard Design (Pitfalls 1, 3, 10, 11)](https://www.perceptualedge.com/articles/Whitepapers/Common_Pitfalls.pdf); [Apple HIG, Charting data](https://developer.apple.com/design/human-interface-guidelines/charting-data).

## Numbers in text

### Round to the precision the reader can use

**Why.** Ehrenberg's first rule is to round to two significant or "effective" digits, the digits that vary in the data, because people can only compare and subtract numbers mentally after rounding them. Few lists excessive precision as a dashboard pitfall ($3,848,305.93 instead of $3.8M). ONS asks for the lowest level of rounding suitable for the intended user, applied consistently.

**How to apply.**
- Headline and chart labels: two or three meaningful digits ("3.8M", "41%").
- Exact values in a tooltip, table or detail view.
- Drop trailing zeros that add no meaning; Datawrapper's example is 27% rather than 27.0%.

**When it is broken.** "+3.4718%" on a summary card.

**Sources:** [Ehrenberg 1977, Rudiments of Numeracy, *JRSS A* 140(3)](https://worrydream.com/refs/Ehrenberg_1977_-_Rudiments_of_Numeracy.pdf) ([DOI](https://doi.org/10.2307/2344922)); [Few 2006, Common Pitfalls (Pitfall 3)](https://www.perceptualedge.com/articles/Whitepapers/Common_Pitfalls.pdf); [ONS Service Manual, Rounding](https://service-manual.ons.gov.uk/content/numbers/rounding); [Datawrapper, text in data visualizations](https://www.datawrapper.de/blog/text-in-data-visualizations).

### Format numbers in a list the same way

**Why.** Mixed precision and formats make numbers look more or less certain than they are, and break vertical comparison. ONS requires the same number of decimal places across a sequence, commas for thousands, and a leading zero before a decimal point.

**How to apply.**
- Same decimal places within a list, table column or set of labels.
- Thousands separators for four or more digits; a leading zero ("0.6%", not ".6%").
- Right-align numbers in columns so places line up (the UK Analysis Function also asks for right-aligned axis values).
- Write ranges with "to" in prose ("500 to 900").

**When it is broken.** A column showing 12%, 7.5%, 0.33% and 101.0%.

**Sources:** [ONS Service Manual, Writing numbers](https://service-manual.ons.gov.uk/content/numbers/writing-numbers); [UK Analysis Function, Data visualisation: charts](https://analysisfunction.civilservice.gov.uk/policy-store/data-visualisation-charts/); [GOV.UK A to Z style guide](https://guidance.publishing.service.gov.uk/writing-to-gov-uk-standards/style-guides/a-to-z-style-guide/).

### Always show the unit, close to the number

**Why.** Few's fourth pitfall notes that a measure is meaningful only if viewers know what is measured and in what unit. Datawrapper recommends showing the unit in the number format ("12.8m") rather than as a multiplier hidden in a description ("in millions").

**How to apply.**
- Put the unit on the value or the axis label, not only in a footnote.
- Use one unit per chart; if two are needed, two charts.
- Use abbreviations readers know (k, M, %), consistently.

**When it is broken.** An axis labelled 0 to 40 with no unit; a caption saying "figures in thousands" that nobody reads.

**Sources:** [Few 2006, Common Pitfalls (Pitfall 4)](https://www.perceptualedge.com/articles/Whitepapers/Common_Pitfalls.pdf); [Datawrapper, text in data visualizations](https://www.datawrapper.de/blog/text-in-data-visualizations).

### Write changes with a sign, a base, and the right kind of percent

**Why.** A change means nothing without what it is measured from, and "percent" and "percentage points" mean different things. ONS: a value of 10% falling by 1 percentage point becomes 9%; falling by 1% gives 9.9%.

**How to apply.**
- Give the direction with a sign or a word, not with colour alone ("−4%", "down 4%").
- Name the base period ("vs. last month").
- Change in a rate or share: percentage points. Relative change in an amount: percent.
- Do not compute a percent change from a base near zero; show the absolute change instead.

**When it is broken.** "Savings rate up 2%" when it went from 10% to 12% (2 points, 20% relative).

**Sources:** [ONS Service Manual, Percentages and percentage points](https://service-manual.ons.gov.uk/content/numbers/percentages); [Few 2006, Common Pitfalls (Pitfall 4)](https://www.perceptualedge.com/articles/Whitepapers/Common_Pitfalls.pdf).

## Honesty and access

### Make visual differences proportional to data differences

**Why.** Cairo's *How Charts Lie* catalogues how charts mislead through poor design, dubious or incomplete data, hidden uncertainty and misleading patterns. Correll et al. show that design choices such as truncation change how large an effect looks, even when the axis is labelled. Tufte's first book covers detecting graphical deception, where design variation is mistaken for data variation.

**How to apply.**
- Check that areas, lengths and slopes change by the same proportion as the values they encode.
- Show a time range long enough to judge the pattern, and say why the range was chosen.
- Use the same scale for things the reader will compare.
- Ask: would a reader who saw only the picture come away with the same conclusion as one who read the numbers?

**When it is broken.** A start date chosen just after a peak so a flat period looks like steady growth; icons scaled in both width and height so a doubling looks like a quadrupling.

**Sources:** [Cairo 2019, *How Charts Lie* (W. W. Norton)](https://wwnorton.co.uk/books/9781324001560-how-charts-lie); [Correll, Bertini & Franconeri 2020](https://arxiv.org/abs/1907.02035); [Tufte, *The Visual Display of Quantitative Information*](https://www.edwardtufte.com/book/the-visual-display-of-quantitative-information/).

### Give every chart a text equivalent

**Why.** Charts are images; people using screen readers, and people who skim, need the message in text. WCAG requires a text alternative for non-text content, and the UK Analysis Function asks for a text description or accessible data table with every chart. Apple's guidelines ask for accessibility labels that fit the chart's purpose, a summary of the message, and an overview of the chart's type, axes and bounds. Chartability turns these needs into testable heuristics for charts.

**How to apply.**
- A one-sentence summary of the finding, readable by assistive technology.
- A description of type, axes and ranges for anyone who needs the structure.
- A data table or list on demand.
- Per-mark labels when individual values matter; grouped summaries when only the shape does.

**When it is broken.** A chart exposed to a screen reader as "image" or as a list of 365 unlabelled numbers.

**Sources:** [UK Analysis Function, Data visualisation: charts](https://analysisfunction.civilservice.gov.uk/policy-store/data-visualisation-charts/); [Apple HIG, Charts (Enhancing the accessibility of a chart)](https://developer.apple.com/design/human-interface-guidelines/charts); [Chartability](https://chartability.fizz.studio/).

## Sources

Research papers

- Bateman, S., Mandryk, R. L., Gutwin, C., Genest, A., McDine, D., & Brooks, C. (2010). Useful Junk? The Effects of Visual Embellishment on Comprehension and Memorability of Charts. CHI 2010. https://vis.csail.mit.edu/classes/6.859/readings/pdfs/Bateman-UsefulJunk.pdf
- Borkin, M. A., et al. (2013). What Makes a Visualization Memorable? IEEE TVCG 19(12). https://vcg.seas.harvard.edu/publications/20130101-what-makes-a-visualization-memorable
- Brehmer, M., Lee, B., Isenberg, P., & Choe, E. K. (2019). Visualizing Ranges over Time on Mobile Phones: A Task-Based Crowdsourced Evaluation. IEEE TVCG 25. https://www.microsoft.com/en-us/research/publication/visualizing-ranges-over-time-on-mobile-phones-a-task-based-crowdsourced-evaluation/
- Cleveland, W. S., & McGill, R. (1984). Graphical Perception: Theory, Experimentation, and Application to the Development of Graphical Methods. *Journal of the American Statistical Association* 79(387). https://doi.org/10.1080/01621459.1984.10478080 (paywalled)
- Correll, M., Bertini, E., & Franconeri, S. (2020). Truncating the Y-Axis: Threat or Menace? CHI 2020. https://arxiv.org/abs/1907.02035
- Correll, M., & Gleicher, M. (2014). Error Bars Considered Harmful: Exploring Alternate Encodings for Mean and Error. IEEE TVCG (InfoVis 2014). https://graphics.cs.wisc.edu/Papers/2014/CG14/Preprint.pdf
- Crameri, F., Shephard, G. E., & Heron, P. J. (2020). The misuse of colour in science communication. *Nature Communications* 11. https://www.nature.com/articles/s41467-020-19160-7
- Ehrenberg, A. S. C. (1977). Rudiments of Numeracy. *Journal of the Royal Statistical Society A* 140(3), 277–297. https://worrydream.com/refs/Ehrenberg_1977_-_Rudiments_of_Numeracy.pdf (DOI https://doi.org/10.2307/2344922)
- Haroz, S., Kosara, R., & Franconeri, S. (2015). ISOTYPE Visualization: Working Memory, Performance, and Engagement with Pictographs. CHI 2015. https://tableau.com/sites/default/files/2023-01/Haroz_CHI_2015.pdf
- Heer, J., & Agrawala, M. (2006). Multi-Scale Banking to 45 Degrees. IEEE TVCG 12(5). https://idl.uw.edu/papers/banking
- Heer, J., & Bostock, M. (2010). Crowdsourcing Graphical Perception: Using Mechanical Turk to Assess Visualization Design. CHI 2010. https://homes.cs.washington.edu/~jheer/files/2010-MTurk-CHI.pdf
- Hullman, J., Resnick, P., & Adar, E. (2015). Hypothetical Outcome Plots Outperform Error Bars and Violin Plots for Inferences About Reliability of Variable Ordering. *PLOS ONE*. https://idl.uw.edu/papers/hops
- Kay, M., Kola, T., Hullman, J., & Munson, S. (2016). When(ish) is My Bus? User-centered Visualizations of Uncertainty in Everyday, Mobile Predictive Systems. CHI 2016. https://idl.uw.edu/papers/when-ish-is-my-bus
- Kong, H.-K., Liu, Z., & Karahalios, K. (2018). Frames and Slants in Titles of Visualizations on Controversial Topics. CHI 2018. https://mail.zcliu.cs.umd.edu/vistitles/CHI18-VisTitles.pdf
- Schwabish, J. A. (2014). An Economist's Guide to Visualizing Data. *Journal of Economic Perspectives* 28(1), 209–234. https://www.aeaweb.org/articles?id=10.1257/jep.28.1.209
- Skau, D., & Kosara, R. (2016). Arcs, Angles, or Areas: Individual Data Encodings in Pie and Donut Charts. EuroVis 2016. https://kosara.net/papers/2016/Skau-EuroVis-2016.pdf
- Song, H., & Szafir, D. A. (2019). Where's My Data? Evaluating Visualizations with Missing Data. IEEE TVCG 25(1). https://par.nsf.gov/servlets/purl/10111567 and https://cmci.colorado.edu/visualab/MissingData

Books and authors' own writing

- Cairo, A. (2019). *How Charts Lie: Getting Smarter about Visual Information*. W. W. Norton. https://wwnorton.co.uk/books/9781324001560-how-charts-lie
- Few, S. (2006). Common Pitfalls in Dashboard Design. Perceptual Edge. https://www.perceptualedge.com/articles/Whitepapers/Common_Pitfalls.pdf
- Few, S. (2008). Practical Rules for Using Color in Charts. Perceptual Edge. https://www.perceptualedge.com/articles/visual_business_intelligence/rules_for_using_color.pdf
- Few, S. (2013 revision). Bullet Graph Design Specification. Perceptual Edge. https://www.perceptualedge.com/articles/misc/Bullet_Graph_Design_Spec.pdf
- Knaflic, C. N. *Storytelling with Data* and related books. https://www.storytellingwithdata.com/books
- Knaflic, C. N. Declutter this graph. https://www.storytellingwithdata.com/blog/2017/3/29/declutter-this-graph
- Knaflic, C. N. Where are your eyes drawn? https://www.storytellingwithdata.com/blog/whereareyoureyesdrawn
- Munzner, T. (2014). *Visualization Analysis and Design*. CRC Press. https://www.cs.ubc.ca/~tmm/vadbook/ ; marks and channels slides: https://cs.ubc.ca/~tmm/talks/vad/VAD-marks.pdf
- Schwabish, J. (2021). *Better Data Visualizations*. Columbia University Press. https://cup.columbia.edu/book/better-data-visualizations/9780231193115
- Tufte, E. R. (2001, 2nd ed.). *The Visual Display of Quantitative Information*. https://www.edwardtufte.com/book/the-visual-display-of-quantitative-information/
- Tufte, E. R. (1990). *Envisioning Information*. https://www.edwardtufte.com/book/envisioning-information/
- Tufte, E. R. (2004). Sparkline theory and practice. https://www.edwardtufte.com/notebook/sparkline-theory-and-practice-edward-tufte/

Guidelines and standards

- Apple. Human Interface Guidelines: Charts. https://developer.apple.com/design/human-interface-guidelines/charts
- Apple. Human Interface Guidelines: Charting data. https://developer.apple.com/design/human-interface-guidelines/charting-data
- Brewer, C., Harrower, M., & The Pennsylvania State University. ColorBrewer. https://colorbrewer2.org/ ; scheme types: https://colorbrewer2.org/learnmore/schemes_full.html
- data.europa.eu. Guidelines for visualisation titles. https://data.europa.eu/apps/data-visualisation-guide/guidelines-for-visualisation-titles
- Elavsky, F. Chartability. https://chartability.fizz.studio/
- GOV.UK. A to Z style guide. https://guidance.publishing.service.gov.uk/writing-to-gov-uk-standards/style-guides/a-to-z-style-guide/
- Office for National Statistics. Service Manual: Rounding. https://service-manual.ons.gov.uk/content/numbers/rounding
- Office for National Statistics. Service Manual: Writing numbers. https://service-manual.ons.gov.uk/content/numbers/writing-numbers
- Office for National Statistics. Service Manual: Percentages and percentage points. https://service-manual.ons.gov.uk/content/numbers/percentages
- Office for National Statistics. Service Manual: Small multiple charts. https://service-manual.ons.gov.uk/data-visualisation/chart-types/small-multiple-charts
- UK Government Analysis Function. Data visualisation: charts. https://analysisfunction.civilservice.gov.uk/policy-store/data-visualisation-charts/
- W3C. Understanding SC 1.4.1: Use of Color (WCAG 2.2). https://www.w3.org/WAI/WCAG22/Understanding/use-of-color.html
- W3C. Understanding SC 1.4.11: Non-text Contrast (WCAG 2.2). https://www.w3.org/WAI/WCAG22/Understanding/non-text-contrast.html

Practitioner guidance (Datawrapper, Lisa Charlotte Muth)

- What to consider when choosing colors for data visualization (2018). https://www.datawrapper.de/blog/colors
- Why not to use two axes, and what to use instead (2018, updated 2026). https://www.datawrapper.de/blog/dualaxis
- What to consider when visualizing data for colorblind readers (2020). https://www.datawrapper.de/blog/colorblindness-part2
- What to consider when using text in data visualizations (2022). https://www.datawrapper.de/blog/text-in-data-visualizations
- What to consider when creating small multiple line charts (2024). https://www.datawrapper.de/blog/what-to-consider-when-creating-small-multiple-line-charts
- A friendly guide to choosing a chart type (2025). https://www.datawrapper.de/blog/chart-types-guide

Secondary

- Kasy, M. Data visualization course slides (lists the three guideline names from Schwabish 2014, used because the article's full text was not reachable). https://maxkasy.github.io/home/files/teaching/TopicsEconometrics2019/DataVisualization-Slides.pdf

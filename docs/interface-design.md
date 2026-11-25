# Interface design

How to make a good interface, from the user's job down to a single screen: structure and navigation, the classic usability rules, every state a view can be in, forms, interface text, motion, speed, touch and accessibility, and how to improve a design and review it.
Each rule says why it holds, how to check it, what breaking it looks like, and where it comes from.

<!-- Append new principles in the section they belong to; keep one rule per heading and cite it. -->

Each principle has four parts. **Why**: the mechanism or the evidence. **How to apply**: checks you can run against a design. **When it is broken**: what a violation looks like. **Sources**: where the rule comes from.

## Contents

1. [Start from the job](#start-from-the-job)
2. [Structure and navigation](#structure-and-navigation)
3. [Usability heuristics](#usability-heuristics)
4. [Targets, choices and signals](#targets-choices-and-signals)
5. [Every state of a view](#every-state-of-a-view)
6. [Forms](#forms)
7. [Writing interface text](#writing-interface-text)
8. [Motion](#motion)
9. [Speed and perceived performance](#speed-and-perceived-performance)
10. [Touch and accessibility](#touch-and-accessibility)
11. [Iterating and reviewing](#iterating-and-reviewing)
12. [Sources](#sources)

## Start from the job

### Name the user's job before drawing a screen

**Why.** People adopt a product to make progress in a particular situation, and features that do not serve that progress add cost without value. A written problem statement keeps a team arguing about the same problem instead of about solutions.

**How to apply.**
- Write one sentence per screen or flow: who, in what situation, wants to get what done, and why.
- Check every element on the screen against that sentence; anything that serves none of them is a candidate for removal.
- Describe the outcome the user wants, not the feature ("know whether I can afford this", not "a balance widget").

**When it is broken.** A screen that lists everything the system knows, ordered by the data model, with no answer to the question the user opened it with.

**See:** [figure of a one-sentence job-to-be-done statement beside a persona](https://www.nngroup.com/articles/personas-jobs-be-done/)

**Sources:** [Christensen et al., "Know Your Customers' Jobs to Be Done", HBR](https://hbr.org/2016/09/know-your-customers-jobs-to-be-done); [NN/g, Personas vs. Jobs-to-Be-Done](https://www.nngroup.com/articles/personas-jobs-be-done/); [NN/g, User Need Statements](https://www.nngroup.com/articles/user-need-statements/)

### Design for the moment of use

**Why.** The same task is done differently at a desk, on a commute, or in a ten-second glance between other things. Mobile use in particular comes in short sessions, on a small screen, with one window and unreliable connectivity.

**How to apply.**
- For each flow, note where the user is, how long they have, which hand is free, and what interrupts them.
- Make the answer to the most frequent question readable within a glance at the top of the first screen.
- Let a task survive an interruption: keep drafts, keep scroll position, and return the user to where they left.
- Learn these facts by watching people in their own setting or through diary studies, not by guessing.

**When it is broken.** A flow that only works in one uninterrupted sitting, or a summary that needs scrolling and tapping before it says anything.

**See:** [figures of one-handed, cradled and two-handed phone grips with usage shares](https://www.uxmatters.com/mt/archives/2013/02/how-do-users-really-hold-mobile-devices.php)

**Sources:** [NN/g, Mobile User Experience: Limitations and Strengths](https://www.nngroup.com/articles/mobile-ux/); [NN/g, Field Studies](https://www.nngroup.com/articles/field-studies/); [NN/g, Diary Studies](https://www.nngroup.com/articles/diary-studies/); [NN/g, Task Analysis](https://www.nngroup.com/articles/task-analysis/)

### Give each screen one purpose and put the most important thing first

**Why.** People scan rather than read, and a clear visual hierarchy tells their eye where to start. Every element that does not serve the purpose competes with the ones that do and lowers their visibility (Heuristic 8, aesthetic and minimalist design).

**How to apply.**
- State the screen's purpose in one line; the element that fulfils it is the largest or highest-contrast item and sits first in reading order.
- Rank the rest into two or three levels by size, weight, colour and position; no more than one element at the top level.
- For each remaining element, ask what decision it supports; remove or move it if the answer is none.
- If two ideas compete, split them across screens or put the second behind a link.
- Judge the result by whether people complete the task, not by how polished it looks: attractive design makes users forgive problems and can hide them in testing.

**When it is broken.** A page where a promotional banner, a chart and a list are the same size and weight, so the eye jumps between them, and the one number the user came for sits below the fold.

**See:** [annotated screenshots of weak and strong hierarchy, plus blurred squint-test images](https://www.nngroup.com/articles/visual-hierarchy-ux-definition/)

**Sources:** [Apple HIG, Writing ("Consider each screen's purpose")](https://developer.apple.com/design/human-interface-guidelines/writing); [NN/g, Visual Hierarchy in UX](https://www.nngroup.com/articles/visual-hierarchy-ux-definition/); [NN/g, 10 Usability Heuristics](https://www.nngroup.com/articles/ten-usability-heuristics/); [NN/g, The Aesthetic-Usability Effect](https://www.nngroup.com/articles/aesthetic-usability-effect/)

## Structure and navigation

### Organise content by the user's mental model and test the labels

**Why.** Users predict where things are from what they already believe about the domain, not from how the system stores it. Card sorting reveals how users group items; tree testing shows whether they can find items in a proposed hierarchy before any screen is drawn.

**How to apply.**
- Run an open card sort to get candidate groups and names from users.
- Run a tree test on the proposed hierarchy with real tasks ("where would you look to ..."); fix labels that send people to the wrong branch.
- Keep the information architecture (the structure and its labels) separate from the navigation UI (menus, tabs, links) that exposes it; fix the structure first.

**When it is broken.** Categories named after internal teams or database tables, which users click through one by one hunting for a known item.

**See:** [photos and screenshots of a card sort grouping and labelling cards](https://www.nngroup.com/articles/card-sorting-definition/); [tree-test participant view and process diagram for checking menu labels](https://www.nngroup.com/articles/tree-testing/)

**Sources:** [NN/g, Card Sorting](https://www.nngroup.com/articles/card-sorting-definition/); [NN/g, Tree Testing](https://www.nngroup.com/articles/tree-testing/); [NN/g, The Difference Between IA and Navigation](https://www.nngroup.com/articles/ia-vs-navigation/); [NN/g, Mental Models](https://www.nngroup.com/articles/mental-models/)

### Keep primary navigation visible

**Why.** In NN/g's quantitative tests, hiding the main navigation behind a menu icon cut discoverability almost in half, lengthened task time and raised perceived difficulty. A visible tab bar also tells people which section they are in.

**How to apply.**
- On mobile, put the three to five top-level sections in a visible tab bar; use a hidden menu only for secondary destinations.
- Keep the tab bar on screen when moving between sections; hide it only under a temporary modal.
- Use the tab bar for navigation only; put actions on the current view in a toolbar.

**When it is broken.** Every top-level section reachable only through a hamburger icon, or a tab bar that holds an "add" action next to destinations.

**See:** [bar charts comparing hidden, combo and visible navigation](https://www.nngroup.com/articles/hamburger-menus/#toc-hidden-navigation-leads-to-worse-user-experience-4); [iOS tab bar images and labelled diagram of a tab bar](https://developer.apple.com/design/human-interface-guidelines/tab-bars)

**Sources:** [NN/g, Hamburger Menus and Hidden Navigation Hurt UX Metrics](https://www.nngroup.com/articles/hamburger-menus/); [NN/g, Basic Patterns for Mobile Navigation](https://www.nngroup.com/articles/mobile-navigation-patterns/); [Apple HIG, Tab bars](https://developer.apple.com/design/human-interface-guidelines/tab-bars)

### Use in-page tabs only for parallel views of the same thing

**Why.** Users expect in-page tabs to switch between related, similar content while staying in place, and navigation tabs to take them somewhere else. Mixing the two in one control disorients people.

**How to apply.**
- Tabs inside a screen hold peers (e.g. the same list filtered by period); each tab's content has the same kind of layout.
- Never put a navigation destination and an in-page view in the same tab set.
- Mark the selected tab clearly and keep the tab labels short nouns.

**When it is broken.** A tab row whose first two tabs filter a list and whose third opens a settings page.

**See:** [annotated tab screenshots marked good (Google Finance) and bad (navigation mixed into tabs)](https://www.nngroup.com/articles/tabs-used-right/)

**Sources:** [NN/g, Tabs, Used Right](https://www.nngroup.com/articles/tabs-used-right/)

### Disclose progressively, in no more than two levels

**Why.** Showing the few common options first and deferring the rare ones makes an application easier to learn and less error-prone, while still giving experts the power they need. NN/g reports that designs going beyond two disclosure levels typically have low usability because people get lost between levels.

**How to apply.**
- Sort features and details by frequency of use; the first level holds what most users need most of the time.
- Make the way to the second level obvious and labelled ("Advanced options", "Show all 24").
- If you need a third level, simplify the feature set instead.

**When it is broken.** Every setting on one long page, or an important everyday option buried three menus deep.

**See:** [live example of a details control that reveals more help on click](https://design-system.service.gov.uk/components/details/)

**Sources:** [NN/g, Progressive Disclosure](https://www.nngroup.com/articles/progressive-disclosure/)

## Usability heuristics

Jakob Nielsen's ten heuristics are broad rules of thumb for interaction design. The rules below cover the ones that most often decide whether a screen works; the full list is in the source.

### Keep the system status visible

**Why.** People can only decide what to do next if they know the current state; communicating it makes users feel in control and builds trust (Heuristic 1).

**How to apply.**
- After every action, show within 0.1 s that it was received (a pressed state, a change on screen).
- Show where the user is (selected tab, page title), what is selected, and whether data is saving, saved, or failed.
- Put status next to the thing it describes rather than in a distant banner.

**When it is broken.** A save button that gives no sign it worked, so the user taps it again.

**See:** [screenshots of checkmarks, progress steps and stock or cart status messages](https://www.nngroup.com/articles/visibility-system-status/)

**Sources:** [NN/g, 10 Usability Heuristics](https://www.nngroup.com/articles/ten-usability-heuristics/); [NN/g, Visibility of System Status](https://www.nngroup.com/articles/visibility-system-status/); [Apple HIG, Feedback](https://developer.apple.com/design/human-interface-guidelines/feedback)

### Match the user's words and world

**Why.** Users bring a mental model from the real world and from other products; an interface that uses their words and their order of things needs no translation (Heuristic 2).

**How to apply.**
- Use the terms users say in interviews and card sorts, not internal or technical names.
- Order information the way the task unfolds for the user.
- Use real-world conventions for units, dates and signs that your audience already reads.

**When it is broken.** An error that says "Sync job 0x3 failed" where the user needs "Couldn't refresh your accounts".

**See:** [plain wording next to a jargon-heavy page, plus real-world metaphor examples](https://www.nngroup.com/articles/match-system-real-world/#toc-using-specific-and-familiar-language-for-users-1)

**Sources:** [NN/g, 10 Usability Heuristics](https://www.nngroup.com/articles/ten-usability-heuristics/); [NN/g, Mental Models](https://www.nngroup.com/articles/mental-models/)

### Offer undo instead of asking for confirmation

**Why.** People habituate to confirmation dialogs and click through them without reading, so a warning stops protecting them once it appears routinely. Undo lets the action happen at full speed and still recovers from mistakes (Heuristic 3, user control and freedom).

**How to apply.**
- Make destructive actions reversible for a while (an "Undo" in the toast, a trash that can be restored).
- Keep confirmation dialogs for actions that are both irreversible and unexpected; do not confirm what the user plainly asked for.
- When you must confirm, name the consequence and label the button with the action ("Delete 3 photos"), not "OK".
- Distinguish Cancel (abandon the process) from Close (leave the view), and never lose unsaved work on either.

**When it is broken.** An "Are you sure?" dialog on every delete, which users dismiss by reflex, and no way back when they meant "no".

**See:** [Gmail's undo link beside Google Calendar and Highrise delete warnings](https://alistapart.com/article/neveruseawarning/); [screenshots of undo in Word and Google Drive](https://www.nngroup.com/articles/user-control-and-freedom/#toc-support-undo-5)

**Sources:** [Raskin, "Never Use a Warning When You Mean Undo", A List Apart](https://alistapart.com/article/neveruseawarning/); [NN/g, User Control and Freedom](https://www.nngroup.com/articles/user-control-and-freedom/); [NN/g, Confirmation Dialogs Can Prevent User Errors, If Not Overused](https://www.nngroup.com/articles/confirmation-dialog/); [NN/g, Cancel vs. Close](https://www.nngroup.com/articles/cancel-vs-close/); [Apple HIG, Feedback](https://developer.apple.com/design/human-interface-guidelines/feedback)

### Be consistent inside the product and with the platform

**Why.** Users should not have to wonder whether different words, situations or actions mean the same thing. They spend most of their time in other products, so platform conventions are what they expect (Heuristic 4).

**How to apply.**
- Keep a glossary of terms and use one word per concept across the product.
- The same component looks and behaves the same everywhere: same position for the primary action, same icon for the same meaning.
- Prefer standard platform controls and gestures; depart only with evidence that the custom one is better.

**When it is broken.** "Remove" on one screen and "Delete" on another for the same action, or a back gesture that does something else on one screen.

**See:** [consistent Office ribbons, shared e-commerce conventions and inconsistent button order](https://www.nngroup.com/articles/consistency-and-standards/)

**Sources:** [NN/g, Maintain Consistency and Adhere to Standards](https://www.nngroup.com/articles/consistency-and-standards/); [Apple HIG, Writing](https://developer.apple.com/design/human-interface-guidelines/writing)

### Prevent errors before you report them

**Why.** A good error message is second best to a design that makes the error impossible or unlikely (Heuristic 5). Defaults matter here because people tend to keep them, even when a better option is one tap away.

**How to apply.**
- Constrain input so invalid values cannot be entered (pickers for bounded values, disabled impossible options with a reason).
- Set each default to what most users would choose, and to the safe option where choices are risky; never pre-select what benefits the product at the user's expense.
- Keep destructive actions away from frequent ones.
- Make modes visible, or avoid them, so the same action never does something unexpected.

**When it is broken.** A free-text date field that accepts "31/02", "Delete account" placed next to "Save", or a privacy option that defaults to public.

**See:** [screenshots of date-range constraints, search suggestions, defaults and auto-formatting](https://www.nngroup.com/articles/slips/)

**Sources:** [NN/g, 10 Usability Heuristics](https://www.nngroup.com/articles/ten-usability-heuristics/); [NN/g, The Power of Defaults](https://www.nngroup.com/articles/the-power-of-defaults/); [NN/g, Modes in User Interfaces](https://www.nngroup.com/articles/modes/)

### Prefer recognition over recall

**Why.** Recognising an option in a list is easier than recalling it from memory, because the context helps retrieval; every item a user must hold in mind adds to cognitive load (Heuristic 6).

**How to apply.**
- Show options, recent items and previous values instead of asking users to type them.
- Keep information the user needs for a decision on the same screen as the decision.
- Label icons with text unless the icon is universally understood.

**When it is broken.** A form that asks for a code shown on the previous screen, or an icon-only toolbar whose meanings users must memorise.

**See:** [search history and recently viewed items next to unlabeled icons](https://www.nngroup.com/articles/recognition-and-recall/#toc-promote-recognition-in-user-interfaces-4)

**Sources:** [NN/g, Memory Recognition and Recall in User Interfaces](https://www.nngroup.com/articles/recognition-and-recall/); [NN/g, Minimize Cognitive Load](https://www.nngroup.com/articles/minimize-cognitive-load/)

## Targets, choices and signals

### Make frequent targets large and close (Fitts's law)

**Why.** The time to reach a target grows with distance and shrinks with target size. Fitts measured this in 1954; it still predicts pointing and tapping speed.

**How to apply.**
- Size the primary action generously and place it near where the hand or pointer already is.
- Make the whole row or card tappable, not only its small text or icon.
- Place destructive targets far from frequent ones, so a missed tap lands on something harmless.

**When it is broken.** A tiny "Next" link in a corner while the large area next to it does nothing.

**See:** [diagrams of target distance and size, screen-edge targets and menu placement](https://www.nngroup.com/articles/fitts-law/#toc-applications-to-ux-4)

**Sources:** [NN/g, Fitts's Law and Its Applications in UX](https://www.nngroup.com/articles/fitts-law/); [Fitts, 1954, "The information capacity of the human motor system in controlling the amplitude of movement", Journal of Experimental Psychology 47(6)](https://doi.org/10.1037/h0055392) (publisher page; full text behind a paywall)

### Cut and rank the choices where speed matters (Hick's law)

**Why.** Decision time rises with the number of equally likely choices. Hick showed in 1952 that it grows roughly with the logarithm of the number of alternatives, so long flat menus slow every decision.

**How to apply.**
- Keep the options shown at a decision point to the ones that matter; group the rest.
- Mark a recommended or default option so most users decide in one look.
- Break complex choices into steps rather than one large screen of options.

**When it is broken.** A settings page of forty toggles with equal weight, or a menu where the common choice sits among twenty rare ones.

**See:** [Hick's law summary with a Slack onboarding example](https://lawsofux.com/hicks-law/)

**Sources:** [Hick, 1952, "On the rate of gain of information", Quarterly Journal of Experimental Psychology 4(1)](https://doi.org/10.1080/17470215208416600) (publisher page; full text behind a paywall); [Laws of UX, Hick's Law](https://lawsofux.com/hicks-law/) (secondary summary, cited because the paper is not freely readable)

### Make interactive elements look interactive

**Why.** An affordance is what an object lets you do; a signifier is the visible cue that tells you so. Norman's revised *Design of Everyday Things* centres on signifiers, and NN/g's eyetracking found that flat UIs with weak signifiers made users work harder to find what was clickable.

**How to apply.**
- Give buttons a shape, border or fill; give links a colour that differs from body text and is used for nothing else.
- Keep one consistent style for each kind of control across the product.
- Never style static text like a link or a button.

**When it is broken.** A row of grey text labels where some are tappable and some are not, with no visible difference.

**See:** [strong and weak signifier versions side by side, with eye-tracking heatmaps](https://www.nngroup.com/articles/flat-ui-less-attention-cause-uncertainty/); [quiz screenshot asking what is clickable, plus buttons that are and are not buttons](https://www.nngroup.com/articles/clickable-elements/)

**Sources:** [Norman, The Design of Everyday Things, Revised and Expanded Edition (author's page)](https://jnd.org/books/the-design-of-everyday-things-revised-and-expanded-edition/); [NN/g, Beyond Blue Links: Making Clickable Elements Recognizable](https://www.nngroup.com/articles/clickable-elements/); [NN/g, Flat UI Elements Attract Less Attention and Cause Uncertainty](https://www.nngroup.com/articles/flat-ui-less-attention-cause-uncertainty/)

### Match the weight of feedback to the weight of the event

**Why.** Status shown passively can be checked when wanted, while warnings about data loss must interrupt. Alerts used for unimportant things lose their force; confirmations of routine success are rarely needed because people expect success.

**How to apply.**
- Routine status: inline and quiet. Success of a significant action: a brief confirmation. Possible data loss: an interrupting alert.
- Use a validation message for input problems, an indicator for state, and a notification for events the user did not trigger.
- Give every custom button a pressed state.
- Convey feedback through more than one channel (text plus colour, haptics, sound) so it reaches people who cannot see or hear one of them.

**When it is broken.** A modal alert for "Settings saved", or a silent failure on an action that lost the user's input.

**See:** [comparison chart and screenshots of indicators, validations, and passive or intrusive notifications](https://www.nngroup.com/articles/indicators-validations-notifications/)

**Sources:** [Apple HIG, Feedback](https://developer.apple.com/design/human-interface-guidelines/feedback); [Apple HIG, Buttons](https://developer.apple.com/design/human-interface-guidelines/buttons); [NN/g, Indicators, Validations, and Notifications](https://www.nngroup.com/articles/indicators-validations-notifications/)

### Group by proximity and separate by space

**Why.** Elements near each other are perceived as related and elements apart as separate groups (the Gestalt principle of proximity). Spacing is the cheapest way to show structure, and it fails when gaps are ambiguous.

**How to apply.**
- Space inside a group is clearly smaller than space between groups.
- A label sits closer to the thing it labels than to anything else.
- Use space before adding borders or boxes to separate groups.

**When it is broken.** A label equidistant from two fields, so users fill in the wrong one.

**See:** [dot-grid diagram and a form shown as one block and as three groups](https://www.nngroup.com/articles/gestalt-proximity/)

**Sources:** [NN/g, Proximity Principle in Visual Design](https://www.nngroup.com/articles/gestalt-proximity/); [NN/g, Website Forms Usability: Top 10 Recommendations](https://www.nngroup.com/articles/web-form-design/)

## Every state of a view

### Design every state of every view

**Why.** A view is seen far more often loading, empty, failed or out of date than designers draw it. If those states are not designed, users read a blank or frozen screen as a broken product.

**How to apply.**
- For each view, draw at least: ideal (typical data), empty, first-time, loading, partial (some data missing), error, offline or stale, and extremes (one item, very many, very long text).
- Write the text for each state, not only the layout.
- Review the states with real data rather than tidy fixtures.

**When it is broken.** A list that renders correctly with ten items but shows a blank white area with zero and overflows with a long name.

**See:** [UI stack diagram of the ideal, empty, error, partial and loading states, with app examples](https://www.scotthurff.com/posts/why-your-user-interface-is-awkward-youre-ignoring-the-ui-stack/#theuistack)

**Sources:** [NN/g, Designing Empty States in Complex Applications](https://www.nngroup.com/articles/empty-state-interface-design/); [Apple HIG, Loading](https://developer.apple.com/design/human-interface-guidelines/loading); [web.dev, Offline UX design guidelines](https://web.dev/articles/offline-ux-design-guidelines)

### Make an empty state explain itself and lead to the next step

**Why.** Empty containers are a chance to report system status, teach the feature, and offer a direct path to the key task; a blank area does none of these and looks like a failure.

**How to apply.**
- Say why it is empty (nothing yet, nothing matches the filter, still syncing) because each needs a different message.
- Offer the one action that fills it ("Add your first account", "Clear filters").
- Keep it short and in the same visual language as the filled state.

**When it is broken.** "No data" on a fresh account, with no hint of how to add any.

**See:** [a blank panel next to one with a message and a getting-started action](https://www.nngroup.com/articles/empty-state-interface-design/)

**Sources:** [NN/g, Designing Empty States in Complex Applications](https://www.nngroup.com/articles/empty-state-interface-design/)

### Match the loading indicator to the wait

**Why.** Below about 1 second an indicator only flashes and distracts; from 2 to 10 seconds a spinner or skeleton reassures; beyond 10 seconds people need a progress bar and an estimate or they leave. Apple notes that an empty screen during loading reads as a problem with the app.

**How to apply.**
- Under 1 s: show nothing extra; just show the result.
- 2 to 10 s: a skeleton of the coming layout, or an indeterminate indicator.
- Over 10 s: a determinate progress bar with percent or time left, and let people do other things meanwhile.
- Show whatever is already available while the rest loads.

**When it is broken.** A full-screen spinner for half a second on every screen change, or an indefinite spinner on a two-minute import.

**See:** [looped spinners, percent-done bars and a static indicator to avoid](https://www.nngroup.com/articles/progress-indicators/); [images of determinate bars and indeterminate spinners](https://developer.apple.com/design/human-interface-guidelines/progress-indicators)

**Sources:** [NN/g, Progress Indicators Make a Slow System Less Insufferable](https://www.nngroup.com/articles/progress-indicators/); [NN/g, Skeleton Screens 101](https://www.nngroup.com/articles/skeleton-screens/); [Apple HIG, Loading](https://developer.apple.com/design/human-interface-guidelines/loading); [Apple HIG, Progress indicators](https://developer.apple.com/design/human-interface-guidelines/progress-indicators)

### Say what went wrong, why, and how to fix it

**Why.** Error messages work when they are visible, explain the problem in plain words, and help the user recover without losing what they did (Heuristic 9).

**How to apply.**
- Place the message next to the problem and make it visible (not colour alone).
- Name the problem in the user's terms, then the fix ("Card number is 15 digits; this card needs 16").
- Keep the user's input and work; never clear a form on error.
- Say whether the fault is on your side or theirs; for system faults, say what happens next (retry, wait, contact).

**When it is broken.** "An error occurred." in a toast that disappears, with the form emptied.

**See:** [good and bad error-message screenshots, each labelled](https://www.nngroup.com/articles/error-message-guidelines/); [live example of an error message under a field](https://design-system.service.gov.uk/components/error-message/)

**Sources:** [NN/g, Error-Message Guidelines](https://www.nngroup.com/articles/error-message-guidelines/); [Apple HIG, Feedback](https://developer.apple.com/design/human-interface-guidelines/feedback); [web.dev, Offline UX design guidelines](https://web.dev/articles/offline-ux-design-guidelines)

### Label data that is old or incomplete

**Why.** Users act on what they see; cached or partial data shown as if it were current and complete leads to wrong decisions. Showing when data was last updated, and telling the user as soon as the connection state changes, keeps the screen honest.

**How to apply.**
- When data comes from a cache or a source that updates late, show its age ("Updated 3 h ago") where the number is.
- When part of the data failed to load, show what did load, mark what is missing, and offer a retry for that part only.
- Announce changes in connection state as they happen, and say whether queued actions will be sent later.
- Never show zero, or an empty chart, for "unknown".

**When it is broken.** A total that silently omits one source that failed to sync, displayed as if complete.

**See:** [app screenshots of an out-of-date notice, an updated notice and an offline status](https://web.dev/articles/offline-ux-design-guidelines#inform-improve)

**Sources:** [web.dev, Offline UX design guidelines](https://web.dev/articles/offline-ux-design-guidelines); [NN/g, Visibility of System Status](https://www.nngroup.com/articles/visibility-system-status/)

## Forms

### Ask only what you need, one thing at a time when it helps

**Why.** Every question costs effort and some users will quit at each one. GOV.UK recommends knowing why you ask every question and starting with one question per page, which helps users focus on it; wizards suit processes done only occasionally.

**How to apply.**
- For each field, write down what it is used for; delete it if the answer is "might be useful".
- Do not ask for what the system already knows; carry earlier answers forward (WCAG 3.3.7).
- For long or rarely done processes, split into short steps with progress shown; for frequent tasks, keep one compact form.

**When it is broken.** A sign-up that asks for address and birthday before the user has seen any value, or a second form asking again for the email given on the first.

**See:** [live examples of one-question pages](https://design-system.service.gov.uk/patterns/question-pages/#start-by-asking-one-question-per-page); [a long form next to a step-by-step wizard](https://www.nngroup.com/articles/wizards/)

**Sources:** [GOV.UK Service Manual, Designing good questions](https://www.gov.uk/service-manual/design/designing-good-questions); [GOV.UK Design System, Question pages](https://design-system.service.gov.uk/patterns/question-pages/); [NN/g, Wizards](https://www.nngroup.com/articles/wizards/); [W3C, Understanding SC 3.3.7 Redundant Entry](https://www.w3.org/WAI/WCAG22/Understanding/redundant-entry.html)

### Keep labels visible; never use a placeholder as the label

**Why.** Placeholder text disappears on typing, so people forget what the field is for and cannot check their answers; it also burdens users with low vision or cognitive impairments. WCAG requires labels or instructions for input.

**How to apply.**
- Every field has a persistent label, placed immediately above the field on mobile.
- Put format hints in visible help text under the label, not inside the field.
- Use a single-column layout.

**When it is broken.** A login form whose only labels are grey "Email" and "Password" placeholders.

**See:** [form fields ranked worst to best: placeholder as label, floating label, label outside the field](https://www.nngroup.com/articles/form-design-placeholders/)

**Sources:** [NN/g, Placeholders in Form Fields Are Harmful](https://www.nngroup.com/articles/form-design-placeholders/); [NN/g, Website Forms Usability: Top 10 Recommendations](https://www.nngroup.com/articles/web-form-design/); [Apple HIG, Text fields](https://developer.apple.com/design/human-interface-guidelines/text-fields); [W3C, Understanding SC 3.3.2 Labels or Instructions](https://www.w3.org/WAI/WCAG22/Understanding/labels-or-instructions.html)

### Choose the control that fits the answer

**Why.** Dropdowns hide options and take several taps; simpler controls (segmented buttons, steppers, radio buttons, text with autocomplete) are often faster and clearer. Date entry in particular causes errors when the format is ambiguous.

**How to apply.**
- Two to five options: show them all (radio buttons or segmented control). Many known options: search or autocomplete. Dropdown last.
- For dates people know (birthdays), use separate day, month and year fields; use a calendar picker only when the day of the week matters.
- Bring up the right keyboard (numeric, email) for the field.

**When it is broken.** A dropdown with two items, or a calendar picker for a date of birth that starts at today.

**See:** [two forms compared, with steppers, segmented controls and buttons in place of dropdowns](https://www.lukew.com/ff/1950/dropdowns-should-be-the-ui-of-last-resort); [date pickers and date fields that work well or poorly](https://www.nngroup.com/articles/date-input/)

**Sources:** [Wroblewski, Dropdowns Should be the UI of Last Resort](https://www.lukew.com/ff/1950/dropdowns-should-be-the-ui-of-last-resort); [NN/g, Date-Input Form Fields](https://www.nngroup.com/articles/date-input/); [GOV.UK Design System, Dates](https://design-system.service.gov.uk/patterns/dates/)

### Point to each error at the field and say how to fix it

**Why.** Users need to find which field is wrong and correct it easily. WCAG requires that errors be identified and described in text.

**How to apply.**
- Show the message next to the field, in text, with an icon or colour as support only.
- On submit with several errors, show a summary at the top whose items link to each field.
- Validate when the user leaves a field, not while they are still typing.
- Write the message as the fix ("Enter a date in the past"), not as blame ("Invalid input").

**When it is broken.** A red border on one field among twenty with no text, after the page scrolled back to the top.

**See:** [live example of an error summary that links to each field in error](https://design-system.service.gov.uk/components/error-summary/); [inline errors, a top summary plus field errors, and hidden tooltip errors](https://www.nngroup.com/articles/errors-forms-design-guidelines/#toc-3-keep-error-messages-next-to-fields-4)

**Sources:** [NN/g, 10 Design Guidelines for Reporting Errors in Forms](https://www.nngroup.com/articles/errors-forms-design-guidelines/); [GOV.UK Design System, Error message](https://design-system.service.gov.uk/components/error-message/); [GOV.UK Design System, Error summary](https://design-system.service.gov.uk/components/error-summary/); [W3C, Understanding SC 3.3.1 Error Identification](https://www.w3.org/WAI/WCAG22/Understanding/error-identification.html)

## Writing interface text

### Write in plain words, front-loaded for people who scan

**Why.** Plain language is faster to understand for everyone, experts included. In NN/g's research 79 percent of test users scanned any new page and only 16 percent read word by word, and eyetracking shows the first words of headings and lines get the most attention.

**How to apply.**
- Use common words, short sentences and active voice; cut every word that does not change the meaning.
- Use the user's terms for things, not the system's, and keep a list of terms used everywhere.
- Start headings, list items and messages with the words that carry the meaning; put the conclusion before the explanation.
- One idea per paragraph; break long text into short chunks with headings.
- Read the text aloud; if it sounds like a manual, rewrite it.

**When it is broken.** "Authentication credentials could not be validated" for "Wrong password", or a notice that opens "Please note that, in accordance with our updated policy," before it says what changed.

**See:** [eye-tracking heatmaps of F-shaped scanning](https://www.nngroup.com/articles/f-shaped-pattern-reading-web-content/#toc-the-f-shaped-pattern-2)

**Sources:** [NN/g, Plain Language Is for Everyone, Even Experts](https://www.nngroup.com/articles/plain-language-experts/); [Digital.gov, Plain language guide series](https://digital.gov/guides/plain-language); [Apple HIG, Writing](https://developer.apple.com/design/human-interface-guidelines/writing); [NN/g, How Users Read on the Web](https://www.nngroup.com/articles/how-users-read-on-the-web/); [NN/g, F-Shaped Pattern of Reading](https://www.nngroup.com/articles/f-shaped-pattern-reading-web-content/)

### Label actions with verbs that say what will happen

**Why.** A button label is a promise about the result; a clear verb lets people act without reading anything else, and descriptive link text works for screen reader users who navigate by links.

**How to apply.**
- Use a verb, plus an object when it helps: "Send", "Delete account", "Save changes".
- Avoid clever or cute labels ("Let's do it!") and generic ones ("OK", "Submit", "Click here").
- Make the label match the outcome: the button that deletes says "Delete".

**When it is broken.** A dialog asking "Discard changes?" with buttons "OK" and "Cancel", where "Cancel" keeps the changes.

**See:** [ambiguous X buttons next to explicit Cancel, Reset, Apply and Save & close labels](https://www.nngroup.com/articles/cancel-vs-close/#toc-2-use-explicit-labels-3)

**Sources:** [Apple HIG, Writing](https://developer.apple.com/design/human-interface-guidelines/writing); [NN/g, Cancel vs. Close](https://www.nngroup.com/articles/cancel-vs-close/)

### Write numbers as numerals, with units and one consistent format

**Why.** Numerals catch the eye of people scanning for facts better than spelled-out numbers. Consistent formatting lets numbers be compared at a glance.

**How to apply.**
- Use numerals ("23", not "twenty-three"), except to start a sentence.
- Use thousands separators, a leading zero (0.5), a true minus sign for negatives, and the same number of decimals across a set.
- Always show the unit or currency, and say the period a figure covers ("per month").
- Use "to" for ranges in prose ("500 to 900"); a dash is fine in tables.
- Do not show decimals that carry no information (75, not 75.00, unless cents matter).

**When it is broken.** "1250", "1.3k" and "1,250.00" for comparable values on the same screen, none of them with a unit.

**See:** [do and don't examples for numerals, thousands separators, units and currency](https://designsystem.wfp.org/docs/guidelines/numbers#use-numerals)

**Sources:** [NN/g, Show Numbers as Numerals When Writing for Online Readers](https://www.nngroup.com/articles/web-writing-show-numbers-as-numerals/); [GOV.UK, A to Z style guide (Numbers, Money)](https://guidance.publishing.service.gov.uk/writing-to-gov-uk-standards/style-guides/a-to-z-style-guide/)

## Motion

### Animate only to explain a change

**Why.** Motion attracts attention powerfully, so it should be spent on helping people understand what changed, where something came from, or that their action registered. Gratuitous animation distracts and can make people physically uncomfortable.

**How to apply.**
- For each animation, name what it explains (continuity between states, cause and effect, a change in position or value).
- Make motion follow the gesture: a view revealed by sliding down is dismissed by sliding up.
- Keep frequent interactions nearly motionless; save larger motion for rarer, meaningful transitions.
- Never make motion the only carrier of information.

**When it is broken.** Cards that bounce in one by one every time a list opens, delaying the content without telling the user anything.

**See:** [videos of animation that explains a change and animation that only distracts](https://www.nngroup.com/articles/animation-usability/#toc-goal-animation-to-aid-comprehension-and-understanding-2); [animated GIFs of container transform, shared axis and fade transitions](https://github.com/material-components/material-components-android/blob/master/docs/theming/Motion.md)

**Sources:** [NN/g, Animation for Attention and Comprehension](https://www.nngroup.com/articles/animation-usability/); [Apple HIG, Motion](https://developer.apple.com/design/human-interface-guidelines/motion)

### Keep durations short: about 100 ms for feedback, up to about 500 ms for large moves

**Why.** Too fast and motion cannot be followed; too slow and it feels like a delay. NN/g puts most UI animation between 100 and 500 ms, with simple feedback around 100 ms; Material's duration tokens run from 50 ms to 1000 ms in short, medium, long and extra-long steps. Animations are more often too long than too short.

**How to apply.**
- Toggles, checkboxes, presses: about 100 ms.
- Elements moving across a screen or a full-screen transition: 200 to 500 ms, longer for longer distance or larger area.
- Pick the shortest duration that does not look jarring.
- Never make the user wait for an animation before they can act; let input interrupt it.

**When it is broken.** A 600 ms fade on every button press, or a page transition that blocks taps until it finishes.

**See:** [animation timeline graphic and timed example videos](https://www.nngroup.com/articles/animation-duration/#toc-animation-duration-3)

**Sources:** [NN/g, Executing UX Animations: Duration and Motion Characteristics](https://www.nngroup.com/articles/animation-duration/); [Material Components for Android, Motion theming (duration and easing tokens)](https://github.com/material-components/material-components-android/blob/master/docs/theming/Motion.md); [Apple HIG, Motion](https://developer.apple.com/design/human-interface-guidelines/motion)

### Ease out on entry, ease in on exit

**Why.** An ease-out curve starts fast and slows down, so the UI feels responsive yet the eye can settle on the element as it stops. Material uses a decelerating curve for elements entering the screen and an accelerating curve for elements leaving it.

**How to apply.**
- Entering or appearing: ease-out (Material emphasized decelerate is `cubic-bezier(0.05, 0.7, 0.1, 1)`).
- Leaving: ease-in (Material emphasized accelerate is `cubic-bezier(0.3, 0, 0.8, 0.15)`), usually shorter than the entry.
- Moving within the screen: ease-in-out.
- Use linear only for things with no physical analogue, such as opacity loops or progress.

**When it is broken.** A sheet that slides in at constant speed and stops dead, or one that starts slowly and makes the tap feel ignored.

**See:** [linear, ease-out, ease-in and ease-in-out curves](https://web.dev/articles/the-basics-of-easing); [video comparing linear and eased motion](https://www.nngroup.com/articles/animation-duration/#toc-easing-makes-motion-feel-more-natural-4)

**Sources:** [NN/g, Executing UX Animations: Duration and Motion Characteristics](https://www.nngroup.com/articles/animation-duration/); [Material Components for Android, Motion theming](https://github.com/material-components/material-components-android/blob/master/docs/theming/Motion.md)

### Honour the reduced-motion setting

**Why.** Motion can cause dizziness or nausea, and in some cases seizures, for people with vestibular disorders. Operating systems expose a reduce-motion setting, and WCAG asks that motion triggered by interaction can be turned off and that moving content can be paused.

**How to apply.**
- Read `prefers-reduced-motion` (web) or Reduce Motion (Apple platforms) and replace zooms, slides, parallax and scaling with fades or instant changes.
- Give any auto-playing or looping motion lasting more than 5 seconds a pause or stop control.
- Test every screen with the setting on; nothing should break or become ambiguous.

**When it is broken.** A parallax header and a zooming transition that still run with Reduce Motion turned on.

**See:** [OS reduce-motion settings and a demo video of the same page with and without motion](https://web.dev/articles/prefers-reduced-motion#demo)

**Sources:** [MDN, prefers-reduced-motion](https://developer.mozilla.org/en-US/docs/Web/CSS/Reference/At-rules/@media/prefers-reduced-motion); [Apple HIG, Accessibility](https://developer.apple.com/design/human-interface-guidelines/accessibility); [W3C, Understanding SC 2.3.3 Animation from Interactions](https://www.w3.org/WAI/WCAG22/Understanding/animation-from-interactions.html); [W3C, Understanding SC 2.2.2 Pause, Stop, Hide](https://www.w3.org/WAI/WCAG22/Understanding/pause-stop-hide.html)

## Speed and perceived performance

### Respond within 0.1 second and finish within 1 second

**Why.** Nielsen's limits, from Miller (1968) and Card et al. (1991): 0.1 s feels instantaneous and like direct manipulation, 1 s keeps the flow of thought, and 10 s is the limit of attention. On the web, Google's Interaction to Next Paint treats 200 ms or less as good responsiveness.

**How to apply.**
- Acknowledge every tap or click visually within 100 ms, even if the work takes longer.
- Budget the common paths to finish within 1 s; measure on a mid-range phone and a slow network.
- For anything over 1 s, show that work is happening; over 10 s, show progress and allow other work.
- Track interaction latency in the field (INP at the 75th percentile) rather than only in the lab.

**When it is broken.** A button that does nothing visible for 400 ms after a tap, so the user taps again and submits twice.

**See:** [video of a slow and a responsive accordion, the INP thresholds, and a diagram of an interaction](https://web.dev/articles/inp)

**Sources:** [NN/g, Response Time Limits](https://www.nngroup.com/articles/response-times-3-important-limits/); [web.dev, Interaction to Next Paint (INP)](https://web.dev/articles/inp); [NN/g, The Need for Speed](https://www.nngroup.com/articles/the-need-for-speed/)

### Show content as soon as you have it, not a spinner

**Why.** The best loading finishes before people notice it. Progress indicators call attention to the wait and make time seem to pass more slowly; Wroblewski reports that after adding spinners to an app, users said it felt slower than the previous version, and that skeleton screens put the focus on progress instead.

**How to apply.**
- Render the layout and any cached or already-known content immediately, then fill in the rest.
- Load in the background what the user will probably need next.
- Let people keep using other parts of the app while something loads.
- Use a skeleton of the actual layout rather than a generic spinner for waits of a few seconds.

**When it is broken.** A blank screen with a centred spinner while the app fetches data it already displayed a minute ago.

**See:** [LinkedIn, Headspace and DoorDash skeleton screens](https://www.nngroup.com/articles/skeleton-screens/); [a skeleton layout next to the loaded article](https://web.dev/articles/offline-ux-design-guidelines#feedback)

**Sources:** [Apple HIG, Loading](https://developer.apple.com/design/human-interface-guidelines/loading); [Wroblewski, Mobile Design Details: Avoid The Spinner](https://www.lukew.com/ff/1797/mobile-design-details-avoid-the-spinner); [NN/g, Skeleton Screens 101](https://www.nngroup.com/articles/skeleton-screens/)

## Touch and accessibility

### Make touch targets at least 44 pt (iOS) or 48 dp (Android)

**Why.** Small targets slow selection and cause mis-taps. Apple sets 44x44 pt as the default control size on iPhone, Google recommends 48x48 dp (about 9 mm) with at least 8 dp between targets, NN/g recommends at least 1 cm x 1 cm, and WCAG 2.2 sets 24x24 CSS px as the minimum at level AA.

**How to apply.**
- Measure the hit area, not the visible glyph; a 24 pt icon gets padding up to 44 pt.
- Keep at least 8 dp between adjacent targets, more between destructive and frequent ones.
- Do not assume one-handed use: Hoober observed 49% one-handed, 36% cradled and 15% two-handed among people touching their screens, and grips change during use.

**When it is broken.** A row of 20 pt icon buttons packed together in a toolbar, each tap a gamble.

**See:** [tap targets that are too small or too crowded, next to large ones](https://www.nngroup.com/articles/touch-target-size/); [playback buttons with enough padding and with too little](https://developer.apple.com/design/human-interface-guidelines/accessibility#Mobility)

**Sources:** [Apple HIG, Buttons](https://developer.apple.com/design/human-interface-guidelines/buttons); [Apple HIG, Accessibility](https://developer.apple.com/design/human-interface-guidelines/accessibility); [Android Accessibility Help, Touch target size](https://support.google.com/accessibility/android/answer/7101858); [NN/g, Touch Targets on Touchscreens](https://www.nngroup.com/articles/touch-target-size/); [W3C, Understanding SC 2.5.8 Target Size (Minimum)](https://www.w3.org/WAI/WCAG22/Understanding/target-size-minimum.html); [Hoober, How Do Users Really Hold Mobile Devices?, UXmatters](https://www.uxmatters.com/mt/archives/2013/02/how-do-users-really-hold-mobile-devices.php)

### Meet contrast minimums and never rely on colour alone

**Why.** Low contrast makes text and controls invisible to people with low vision and to everyone in bright light, and not everyone sees colour or sees it the same way. WCAG AA requires 4.5:1 for normal text, 3:1 for large text and for control boundaries and meaningful graphics, and forbids colour as the only visual means of conveying information.

**How to apply.**
- Check every text colour against its actual background, including text over images.
- Check input borders, focus rings, icons and chart lines at 3:1.
- Pair colour with a second cue: text, an icon, a sign (+/−), a pattern or position; check screens in greyscale.
- Provide a higher-contrast variant when the system setting asks for it.

**When it is broken.** Light grey secondary text on white, an input whose only boundary is a faint hairline, or gains and losses shown only in green and red.

**See:** [buttons with sufficient and insufficient contrast, and status shown by colour plus shape](https://developer.apple.com/design/human-interface-guidelines/accessibility#Vision); [an error shown with colour and text next to one shown with colour only](https://web.dev/articles/offline-ux-design-guidelines#clear-language)

**Sources:** [W3C, Understanding SC 1.4.3 Contrast (Minimum)](https://www.w3.org/WAI/WCAG22/Understanding/contrast-minimum.html); [W3C, Understanding SC 1.4.11 Non-text Contrast](https://www.w3.org/WAI/WCAG22/Understanding/non-text-contrast.html); [W3C, Understanding SC 1.4.1 Use of Color](https://www.w3.org/WAI/WCAG22/Understanding/use-of-color.html); [Apple HIG, Accessibility](https://developer.apple.com/design/human-interface-guidelines/accessibility)

### Expose every control's name, role and state, and announce status changes

**Why.** Assistive technologies can only operate and report what the code describes. WCAG requires that components expose name, role and state, that non-text content have a text alternative, that visual structure exist in code, and that status messages reach assistive technology without taking focus.

**How to apply.**
- Icon-only buttons have an accessible name that says the action ("Delete", not "trash icon").
- Custom controls expose their role (button, switch, tab) and state (selected, expanded, on).
- Headings, lists and groups are marked up as such, not only styled; decorative images are hidden from assistive technology.
- Toasts, result counts and save confirmations are live regions (or the platform equivalent): polite for status, assertive only for urgent errors.

**When it is broken.** A custom toggle that a screen reader announces as plain text, or a search whose result count updates silently.

**See:** [diagram of the accessibility tree with ARIA](https://web.dev/learn/accessibility/aria-html#the_accessibility_tree); [DevTools screenshots showing an element's computed name and role](https://developer.chrome.com/docs/devtools/accessibility/reference)

**Sources:** [W3C, Understanding SC 4.1.2 Name, Role, Value](https://www.w3.org/WAI/WCAG22/Understanding/name-role-value.html); [W3C, Understanding SC 1.1.1 Non-text Content](https://www.w3.org/WAI/WCAG22/Understanding/non-text-content.html); [W3C, Understanding SC 1.3.1 Info and Relationships](https://www.w3.org/WAI/WCAG22/Understanding/info-and-relationships.html); [W3C, Understanding SC 4.1.3 Status Messages](https://www.w3.org/WAI/WCAG22/Understanding/status-messages.html); [W3C, Introduction to Web Accessibility](https://www.w3.org/WAI/fundamentals/accessibility-intro/)

### Make everything work by keyboard, with visible focus

**Why.** People who cannot use a pointer rely on the keyboard or switch devices; without a visible focus indicator, sighted keyboard users cannot tell where they are.

**How to apply.**
- Tab through every screen: each interactive element is reachable and operable in a sensible order.
- Show a clearly visible focus ring that meets 3:1 contrast; never remove it without a replacement.
- Return focus to a sensible place after dialogs close.

**When it is broken.** A modal that traps or loses focus, or a CSS reset that removes focus outlines everywhere.

**See:** [animated GIFs of tabbing through a page with styled focus indicators](https://web.dev/learn/accessibility/focus#focus_indicator); [W3C video of people using the web by keyboard](https://www.w3.org/WAI/perspective-videos/keyboard/)

**Sources:** [W3C, Understanding SC 2.1.1 Keyboard](https://www.w3.org/WAI/WCAG22/Understanding/keyboard.html); [W3C, Understanding SC 2.4.7 Focus Visible](https://www.w3.org/WAI/WCAG22/Understanding/focus-visible.html)

### Let text grow and layouts reflow

**Why.** Many people enlarge text. WCAG requires that text can be resized to 200% without loss of content or function, and that content reflows at a width of 320 CSS px without scrolling in two directions; Apple's Dynamic Type lets people choose their text size system-wide.

**How to apply.**
- Use the platform text styles (Dynamic Type, rem units) instead of fixed pixel sizes.
- Test at the largest accessibility text size and at 320 px width: no clipped text, no overlap, no horizontal scroll for body content.
- Let containers grow with their text; avoid fixed heights on anything holding text.

**When it is broken.** A card whose title is cut off with an ellipsis at a larger text size, hiding the only information it held.

**See:** [a Mail message at the default text size and at the largest accessibility size](https://developer.apple.com/design/human-interface-guidelines/typography#Supporting-Dynamic-Type); [numbered pass and fail figures of pages reflowing at 320 px](https://www.w3.org/WAI/WCAG22/Understanding/reflow.html)

**Sources:** [W3C, Understanding SC 1.4.4 Resize Text](https://www.w3.org/WAI/WCAG22/Understanding/resize-text.html); [W3C, Understanding SC 1.4.10 Reflow](https://www.w3.org/WAI/WCAG22/Understanding/reflow.html); [Apple HIG, Typography](https://developer.apple.com/design/human-interface-guidelines/typography)

## Iterating and reviewing

### Improve a design in small steps, each compared with the current one

**Why.** Across Nielsen's case studies the median usability gain was 38% per iteration and 165% from first to last version; some metrics can drop in a given version, so at least three versions (two iterations) are recommended. NN/g also finds that combining iterative design with parallel design (several alternatives explored at once) finds the best ideas at lower cost than sticking to one approach. Small steps show which change caused which effect.

**How to apply.**
- Change one or two things per iteration and write down what each change is meant to fix.
- Keep the current version (A) as the baseline; show a significant proposal (B) next to it, with what B changes and why.
- Judge both against the same task and the same real data.
- Plan for at least three versions (two rounds of change); expect some regressions and check for them.

**When it is broken.** A full redesign shipped at once, reviewed alone with "do you like this?", after which nobody can tell which change caused the drop in completion.

**See:** [diagrams of iterative, parallel and competitive design](https://www.nngroup.com/articles/parallel-and-iterative-design/); [graph of usability rising with each iteration](https://www.nngroup.com/articles/iterative-design/)

**Sources:** [NN/g, Iterative Design of User Interfaces](https://www.nngroup.com/articles/iterative-design/); [NN/g, Parallel & Iterative Design + Competitive Testing](https://www.nngroup.com/articles/parallel-and-iterative-design/)

### Test with about five users per round, and run more rounds

**Why.** Nielsen's model shows the first five participants in a qualitative test find about 85% of the usability problems; after that, returns drop, and the budget is better spent on testing the redesign. Thinking aloud is cheap, robust and the most useful single method.

**How to apply.**
- Give each participant real tasks and ask them to think aloud; do not help.
- Fix what five people reveal, then test the new version with five more.
- Watch what people do rather than what they say they would do.

**When it is broken.** One large study at the end of the project whose findings arrive too late to change anything.

**See:** [curve of usability problems found against the number of test users](https://www.nngroup.com/articles/why-you-only-need-to-test-with-5-users/)

**Sources:** [NN/g, Why You Only Need to Test with 5 Users](https://www.nngroup.com/articles/why-you-only-need-to-test-with-5-users/); [NN/g, How Many Test Users in a Usability Study?](https://www.nngroup.com/articles/how-many-test-users/); [NN/g, Thinking Aloud: The #1 Usability Tool](https://www.nngroup.com/articles/thinking-aloud-the-1-usability-tool/)

### Use A/B tests for questions a metric can answer

**Why.** An online controlled experiment is the most reliable way to measure whether a change moves a behaviour, but it says how behaviour changed, not why, and it needs enough traffic and a metric fixed in advance. Variations designed from user research make better tests.

**How to apply.**
- Write the hypothesis and the primary metric before starting; change one variable per test.
- Run long enough for the planned sample size; do not stop when the result first looks good.
- Pair the test with qualitative research to learn why the winner won.
- With too few users for statistics, use moderated tests and side-by-side comparison instead.

**When it is broken.** A test stopped after two days on a lucky spike, or a "winning" variant nobody can explain.

**See:** [diagram of an A/B test design and the four steps for setting one up](https://www.nngroup.com/articles/ab-testing/)

**Sources:** [NN/g, A/B Testing 101](https://www.nngroup.com/articles/ab-testing/); [NN/g, Define Stronger A/B Test Variations Through UX Research](https://www.nngroup.com/articles/ab-testing-and-ux-research/); [Kohavi, Tang and Xu, Trustworthy Online Controlled Experiments (book site)](https://experimentguide.com/)

### Review against stated goals, with independent evaluators and severity ratings

**Why.** A design critique analyses whether a design meets its objectives, so the goal has to be agreed before feedback is useful. In a heuristic evaluation any single evaluator misses problems, so three to five people should review independently before pooling. Severity combines frequency, impact and persistence, and a 0 to 4 rating sets the order of fixes.

**How to apply.**
- Open each review by restating the user, the task and the goal of the design; phrase feedback as "this works against goal X because ...".
- Each evaluator walks through real tasks alone against the ten heuristics and records each problem with the heuristic it breaks and the exact element.
- Merge the lists, remove duplicates, rate each problem 0 (not a problem) to 4 (catastrophe), and fix in severity order.
- Treat heuristic evaluation as a complement to testing with users, not a replacement.

**When it is broken.** One designer reviewing their own screens and reporting "looks fine", or a critique that ends in "I'd make it blue" with no reference to what the screen is for.

**See:** [filled-in heuristic evaluation workbook pages and annotated issue screenshots](https://www.nngroup.com/articles/how-to-conduct-a-heuristic-evaluation/#toc-step-2-evaluate-independently-4)

**Sources:** [NN/g, Design Critiques](https://www.nngroup.com/articles/design-critiques/); [NN/g, How to Conduct a Heuristic Evaluation](https://www.nngroup.com/articles/how-to-conduct-a-heuristic-evaluation/); [NN/g, Severity Ratings for Usability Problems](https://www.nngroup.com/articles/how-to-rate-the-severity-of-usability-problems/); [NN/g, 10 Usability Heuristics](https://www.nngroup.com/articles/ten-usability-heuristics/)

## Sources

Books, papers and essays
- Christensen, C. M., Hall, T., Dillon, K., Duncan, D. S. (2016). Know Your Customers' "Jobs to Be Done". Harvard Business Review. https://hbr.org/2016/09/know-your-customers-jobs-to-be-done
- Fitts, P. M. (1954). The information capacity of the human motor system in controlling the amplitude of movement. Journal of Experimental Psychology, 47(6). https://doi.org/10.1037/h0055392
- Hick, W. E. (1952). On the rate of gain of information. Quarterly Journal of Experimental Psychology, 4(1). https://doi.org/10.1080/17470215208416600
- Hoober, S. (2013). How Do Users Really Hold Mobile Devices? UXmatters. https://www.uxmatters.com/mt/archives/2013/02/how-do-users-really-hold-mobile-devices.php
- Kohavi, R., Tang, D., Xu, Y. (2020). Trustworthy Online Controlled Experiments. https://experimentguide.com/
- Norman, D. (2013). The Design of Everyday Things, Revised and Expanded Edition. https://jnd.org/books/the-design-of-everyday-things-revised-and-expanded-edition/
- Raskin, A. (2007). Never Use a Warning When You Mean Undo. A List Apart. https://alistapart.com/article/neveruseawarning/
- Wroblewski, L. (2013). Mobile Design Details: Avoid The Spinner. https://www.lukew.com/ff/1797/mobile-design-details-avoid-the-spinner
- Wroblewski, L. (2015). Dropdowns Should be the UI of Last Resort. https://www.lukew.com/ff/1950/dropdowns-should-be-the-ui-of-last-resort
- Laws of UX, Hick's Law (secondary summary). https://lawsofux.com/hicks-law/

Platform guidelines
- Apple Human Interface Guidelines: [Accessibility](https://developer.apple.com/design/human-interface-guidelines/accessibility), [Buttons](https://developer.apple.com/design/human-interface-guidelines/buttons), [Feedback](https://developer.apple.com/design/human-interface-guidelines/feedback), [Loading](https://developer.apple.com/design/human-interface-guidelines/loading), [Motion](https://developer.apple.com/design/human-interface-guidelines/motion), [Progress indicators](https://developer.apple.com/design/human-interface-guidelines/progress-indicators), [Tab bars](https://developer.apple.com/design/human-interface-guidelines/tab-bars), [Text fields](https://developer.apple.com/design/human-interface-guidelines/text-fields), [Typography](https://developer.apple.com/design/human-interface-guidelines/typography), [Writing](https://developer.apple.com/design/human-interface-guidelines/writing)
- Google: [Android Accessibility Help, Touch target size](https://support.google.com/accessibility/android/answer/7101858); [Material Components for Android, Motion theming](https://github.com/material-components/material-components-android/blob/master/docs/theming/Motion.md); [web.dev, Interaction to Next Paint](https://web.dev/articles/inp); [web.dev, Offline UX design guidelines](https://web.dev/articles/offline-ux-design-guidelines)
- MDN: [prefers-reduced-motion](https://developer.mozilla.org/en-US/docs/Web/CSS/Reference/At-rules/@media/prefers-reduced-motion)

Standards
- W3C, [Web Content Accessibility Guidelines (WCAG) 2.2](https://www.w3.org/TR/WCAG22/) and its Understanding documents: [1.1.1](https://www.w3.org/WAI/WCAG22/Understanding/non-text-content.html), [1.3.1](https://www.w3.org/WAI/WCAG22/Understanding/info-and-relationships.html), [1.4.1](https://www.w3.org/WAI/WCAG22/Understanding/use-of-color.html), [1.4.3](https://www.w3.org/WAI/WCAG22/Understanding/contrast-minimum.html), [1.4.4](https://www.w3.org/WAI/WCAG22/Understanding/resize-text.html), [1.4.10](https://www.w3.org/WAI/WCAG22/Understanding/reflow.html), [1.4.11](https://www.w3.org/WAI/WCAG22/Understanding/non-text-contrast.html), [2.1.1](https://www.w3.org/WAI/WCAG22/Understanding/keyboard.html), [2.2.2](https://www.w3.org/WAI/WCAG22/Understanding/pause-stop-hide.html), [2.3.3](https://www.w3.org/WAI/WCAG22/Understanding/animation-from-interactions.html), [2.4.7](https://www.w3.org/WAI/WCAG22/Understanding/focus-visible.html), [2.5.8](https://www.w3.org/WAI/WCAG22/Understanding/target-size-minimum.html), [3.3.1](https://www.w3.org/WAI/WCAG22/Understanding/error-identification.html), [3.3.2](https://www.w3.org/WAI/WCAG22/Understanding/labels-or-instructions.html), [3.3.7](https://www.w3.org/WAI/WCAG22/Understanding/redundant-entry.html), [4.1.2](https://www.w3.org/WAI/WCAG22/Understanding/name-role-value.html), [4.1.3](https://www.w3.org/WAI/WCAG22/Understanding/status-messages.html)
- W3C WAI, [Introduction to Web Accessibility](https://www.w3.org/WAI/fundamentals/accessibility-intro/)

Government design and writing guidance
- [GOV.UK Service Manual, Designing good questions](https://www.gov.uk/service-manual/design/designing-good-questions)
- GOV.UK Design System: [Question pages](https://design-system.service.gov.uk/patterns/question-pages/), [Dates](https://design-system.service.gov.uk/patterns/dates/), [Error message](https://design-system.service.gov.uk/components/error-message/), [Error summary](https://design-system.service.gov.uk/components/error-summary/)
- [GOV.UK, A to Z style guide](https://guidance.publishing.service.gov.uk/writing-to-gov-uk-standards/style-guides/a-to-z-style-guide/)
- [Digital.gov, Plain language guide series](https://digital.gov/guides/plain-language)

Nielsen Norman Group articles
- [10 Usability Heuristics for User Interface Design](https://www.nngroup.com/articles/ten-usability-heuristics/)
- [10 Design Guidelines for Reporting Errors in Forms](https://www.nngroup.com/articles/errors-forms-design-guidelines/)
- [A/B Testing 101](https://www.nngroup.com/articles/ab-testing/)
- [Animation for Attention and Comprehension](https://www.nngroup.com/articles/animation-usability/)
- [Basic Patterns for Mobile Navigation](https://www.nngroup.com/articles/mobile-navigation-patterns/)
- [Beyond Blue Links: Making Clickable Elements Recognizable](https://www.nngroup.com/articles/clickable-elements/)
- [Cancel vs. Close](https://www.nngroup.com/articles/cancel-vs-close/)
- [Card Sorting](https://www.nngroup.com/articles/card-sorting-definition/)
- [Confirmation Dialogs Can Prevent User Errors, If Not Overused](https://www.nngroup.com/articles/confirmation-dialog/)
- [Date-Input Form Fields](https://www.nngroup.com/articles/date-input/)
- [Define Stronger A/B Test Variations Through UX Research](https://www.nngroup.com/articles/ab-testing-and-ux-research/)
- [Design Critiques](https://www.nngroup.com/articles/design-critiques/)
- [Designing Empty States in Complex Applications](https://www.nngroup.com/articles/empty-state-interface-design/)
- [Diary Studies](https://www.nngroup.com/articles/diary-studies/)
- [Error-Message Guidelines](https://www.nngroup.com/articles/error-message-guidelines/)
- [Executing UX Animations: Duration and Motion Characteristics](https://www.nngroup.com/articles/animation-duration/)
- [F-Shaped Pattern of Reading](https://www.nngroup.com/articles/f-shaped-pattern-reading-web-content/)
- [Field Studies](https://www.nngroup.com/articles/field-studies/)
- [Fitts's Law and Its Applications in UX](https://www.nngroup.com/articles/fitts-law/)
- [Flat UI Elements Attract Less Attention and Cause Uncertainty](https://www.nngroup.com/articles/flat-ui-less-attention-cause-uncertainty/)
- [Hamburger Menus and Hidden Navigation Hurt UX Metrics](https://www.nngroup.com/articles/hamburger-menus/)
- [How Many Test Users in a Usability Study?](https://www.nngroup.com/articles/how-many-test-users/)
- [How to Conduct a Heuristic Evaluation](https://www.nngroup.com/articles/how-to-conduct-a-heuristic-evaluation/)
- [How Users Read on the Web](https://www.nngroup.com/articles/how-users-read-on-the-web/)
- [Indicators, Validations, and Notifications](https://www.nngroup.com/articles/indicators-validations-notifications/)
- [Iterative Design of User Interfaces](https://www.nngroup.com/articles/iterative-design/)
- [Maintain Consistency and Adhere to Standards](https://www.nngroup.com/articles/consistency-and-standards/)
- [Memory Recognition and Recall in User Interfaces](https://www.nngroup.com/articles/recognition-and-recall/)
- [Mental Models and User Experience Design](https://www.nngroup.com/articles/mental-models/)
- [Minimize Cognitive Load to Maximize Usability](https://www.nngroup.com/articles/minimize-cognitive-load/)
- [Mobile User Experience: Limitations and Strengths](https://www.nngroup.com/articles/mobile-ux/)
- [Modes in User Interfaces](https://www.nngroup.com/articles/modes/)
- [Parallel & Iterative Design + Competitive Testing](https://www.nngroup.com/articles/parallel-and-iterative-design/)
- [Personas vs. Jobs-to-Be-Done](https://www.nngroup.com/articles/personas-jobs-be-done/)
- [Placeholders in Form Fields Are Harmful](https://www.nngroup.com/articles/form-design-placeholders/)
- [Plain Language Is for Everyone, Even Experts](https://www.nngroup.com/articles/plain-language-experts/)
- [Progress Indicators Make a Slow System Less Insufferable](https://www.nngroup.com/articles/progress-indicators/)
- [Progressive Disclosure](https://www.nngroup.com/articles/progressive-disclosure/)
- [Proximity Principle in Visual Design](https://www.nngroup.com/articles/gestalt-proximity/)
- [Response Time Limits](https://www.nngroup.com/articles/response-times-3-important-limits/)
- [Severity Ratings for Usability Problems](https://www.nngroup.com/articles/how-to-rate-the-severity-of-usability-problems/)
- [Show Numbers as Numerals When Writing for Online Readers](https://www.nngroup.com/articles/web-writing-show-numbers-as-numerals/)
- [Skeleton Screens 101](https://www.nngroup.com/articles/skeleton-screens/)
- [Tabs, Used Right](https://www.nngroup.com/articles/tabs-used-right/)
- [Task Analysis](https://www.nngroup.com/articles/task-analysis/)
- [The Aesthetic-Usability Effect](https://www.nngroup.com/articles/aesthetic-usability-effect/)
- [The Difference Between Information Architecture (IA) and Navigation](https://www.nngroup.com/articles/ia-vs-navigation/)
- [The Need for Speed](https://www.nngroup.com/articles/the-need-for-speed/)
- [The Power of Defaults](https://www.nngroup.com/articles/the-power-of-defaults/)
- [Thinking Aloud: The #1 Usability Tool](https://www.nngroup.com/articles/thinking-aloud-the-1-usability-tool/)
- [Touch Targets on Touchscreens](https://www.nngroup.com/articles/touch-target-size/)
- [Tree Testing](https://www.nngroup.com/articles/tree-testing/)
- [User Control and Freedom](https://www.nngroup.com/articles/user-control-and-freedom/)
- [User Need Statements](https://www.nngroup.com/articles/user-need-statements/)
- [Visibility of System Status](https://www.nngroup.com/articles/visibility-system-status/)
- [Visual Hierarchy in UX](https://www.nngroup.com/articles/visual-hierarchy-ux-definition/)
- [Website Forms Usability: Top 10 Recommendations](https://www.nngroup.com/articles/web-form-design/)
- [Why You Only Need to Test with 5 Users](https://www.nngroup.com/articles/why-you-only-need-to-test-with-5-users/)
- [Wizards](https://www.nngroup.com/articles/wizards/)

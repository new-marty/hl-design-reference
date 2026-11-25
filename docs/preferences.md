# Marty's design preferences

What Marty, the owner of this bank, likes and rejects in interfaces, visual design and charts,
each backed by what he said. It is written for an agent or a designer working for him: read the
section for the task before drawing anything, and treat a preference here as overriding a general
principle in the other pages when the two disagree.

<!-- Append new preferences with a dated quote. -->

How to read an entry:

- The heading states the preference. The line under it explains it, and "Rejected:" names what
  he turned down, when there is something.
- Strength is given in brackets. **(strong)**: he said it several times or with force, and
  breaking it gets the work sent back. **(stated)**: he said it clearly at least once.
  **(inferred)**: read from what he chose or shared rather than from a direct statement.
- "Agrees with" and "Departs from" link to the principle the preference supports or overrides.
- Quotes are his words, copied as written, typos included. Japanese quotes have an English
  translation under them. An ellipsis (…) marks a cut, usually a project or product name.

## Contents

1. [Process](#process)
2. [Visual](#visual)
3. [Layout and type](#layout-and-type)
4. [Colour](#colour)
5. [Motion and interaction](#motion-and-interaction)
6. [Copy and numbers](#copy-and-numbers)
7. [Charts and data storytelling](#charts-and-data-storytelling)
8. [AI-written text](#ai-written-text)
9. [References he likes](#references-he-likes)

## Process

### Show every design question as a screen

**(strong)** He decides from what he can see. Each option comes as a drawn screen, not a
description, and nothing counts as approved until he has seen it.

Rejected: choices described only in words or long text; being told a design was agreed when he
never saw it.

> 判断はuiも出して欲しい。イメージがわかない
>
> Show me the UI for decisions too. I can't picture it. (2026-11-10)

> 基本はUIを叩き台に相談してやりたい。見えるものがないと何も言えないので
>
> Basically I want to discuss things with a UI as the starting draft. If there's nothing to
> look at, I can't say anything. (2026-11-03)

> 文字だけだと分かりにくいし長い
>
> Text alone is hard to follow, and long. (2026-10-22)

> まだ設計を何もみてないしokもしてない
>
> I haven't seen any of the design yet, and I haven't approved it. (2026-11-12)

### Show a large change as A and B side by side, with its intent

**(strong)** A proposal that changes more than a detail sits next to the current version, and
each change says why it was made. The current version stays until he picks.

Rejected: a lone new page to judge with nothing to compare it with.

Agrees with: [Improve a design in small steps, each compared with the current one](interface-design.md#improve-a-design-in-small-steps-each-compared-with-the-current-one).

> 大きく変える時はABテストみたいにどっちも見えるようにしよう。そして意図もちゃんと伝えて
>
> When making a big change, let's make both visible, like an A/B test. And explain the intent
> properly. (2026-11-03)

("Page to look at" was the label of a link to a single proposed page.)

> Page to look atはそのページだけ渡されて持って感じ。side by sideでまず見ないと。
>
> "Page to look at" just hands me that one page. I need to see them side by side first.
> (2026-11-10)

### Refine a tuned screen one or two spots at a time, after reading its history

**(strong)** A screen that has been through many rounds holds many small decisions. Read every
past remark about it before touching it, and change one or two spots per round. A redesign that
undoes earlier choices is rejected even when parts of it are good.

Rejected: a B version that overturns what A settled; bold changes made without reading the
history.

Agrees with: [Improve a design in small steps, each compared with the current one](interface-design.md#improve-a-design-in-small-steps-each-compared-with-the-current-one).

> bはこれまでチミチミuiの好みを合わせて行ったaに対して全て覆してる感じがする。workoutの回数のスタンプはいいと思った。一気にではなくちょっとずつ改善する方がいいのかも。円のグラフにしてとかは結構拘ってる。過去の会話見直して。そこが抜けてる
>
> B feels like it overturns everything in A, which we tuned bit by bit to my taste. I did like
> the workout-count stamps. It's probably better to improve little by little rather than all at
> once. I was quite particular about things like making it a circular chart. Go back over our
> past conversations. That's what's missing. (2026-11-10)

> 基本的にUIは結構詰めてあるので簡単に大胆に変えるのはやめて欲しい。変えるとしても全ての過去の私の会話を見てからにして
>
> The UI has been worked out pretty thoroughly, so please stop making bold changes lightly. If
> you do change it, read all my past conversations first. (2026-11-03)

> このページはかなり拘ったがその時の会話とか見た？その時にこうしたいって言ったのを全部覆してるが
>
> I was very particular about this page. Did you look at those conversations? This overturns
> everything I said I wanted back then. (2026-11-11)

### Change the look only through him, and say what each change is based on

**(strong)** A designer's own finding is reported, not applied. Colours, spacing, wording,
components and layout change only when he asks, through a proposal he reviews. A change with no
stated basis is reverted.

Rejected: unrequested visual changes, including well-meant ones.

> めっちゃこだわって作ったのにお前の判断でめちゃくちゃにするな
>
> I put a lot of care into making this. Don't wreck it on your own judgement. (2026-11-21)

> ちゃんと私を通して変更しなさい
>
> Make changes through me, properly. (2026-11-23)

> 戻す。何を元に変えたの？
>
> Revert it. What did you base that change on? (2026-11-23)

### Treat a pointed-out spot as a symptom and fix the cause everywhere

**(strong)** When he names one spot, find what caused it, check every component that shares the
cause, and fix them all under one rule, now and later. Stay within what the remark was about:
no nitpicking, no overreach.

Rejected: fixing only the spot in the screenshot; checking only where he looked; excessive,
literal-minded changes.

Agrees with: [Build every component from shared tokens, and fix a drift everywhere at once](visual-design.md#build-every-component-from-shared-tokens-and-fix-a-drift-everywhere-at-once).

> 全てのコンポーネントに対して同じことができないか考えなさい。常に。これから先も。揚げ足をとったような過剰なことはやめなさい
>
> Think about whether the same thing can be done for every component. Always. From now on too.
> Stop doing excessive, nitpicking things. (2026-11-18)

> 言われたところを局所的に何も考えずに治すのはやめてって言われたことの意図を理解して他にもおかしいところがないか考えなさい。
>
> You were told to stop fixing just the spot that was pointed out without thinking. Understand
> the intent of that, and check whether anything else is off too. (2026-11-23)

> did you check all places? (2026-05-06)

> make it an explicit rule. this keeps happening (2026-05-06)

### Design the whole experience from UX, not one ticket per complaint

**(strong)** Start from the goals, the moments of use, the flows and the use cases, then design
the answer as a whole. Splitting complaints into separate tasks and building them one by one
produces something hard to use. Keep the established visual language while doing it, and give
every change an intent you can name.

Rejected: one ticket per screenshot; treating design as the UI layer only; proposals with no
felt intent.

Agrees with: [Name the user's job before drawing a screen](interface-design.md#name-the-users-job-before-drawing-a-screen).

> 個別にタスクを切るんじゃなくて設計しろって言っている。個別でタスク切って個別で実装してまた使いにくいもの出してくるだろ？
>
> I'm telling you to design it, not to cut individual tasks. If you cut separate tasks and
> implement them separately, you'll just bring back something hard to use again, won't you?
> (2026-11-23)

> Make sure to document user flows and use cases too. This is not just about UI. It is about UX too. (2026-05-01)

> UIを崩さずにUXから設計すること。勝手な変更はしないこと。全てに意図を持ってやること。
>
> Design from UX without breaking the UI. Make no unilateral changes. Do everything with intent.
> (2026-11-23)

> 小手先のデザイン案で誤魔化さないで。意図が感じられない
>
> Don't paper over it with superficial design ideas. I can't feel any intent. (2026-10-20)

### Decide what a page must express before deciding how it looks

**(strong)** First settle what the user wants to know on the page and which visualisation gets
it across. Start from the ideal experience the available data allows, not from the features
that already exist; the backend can be rebuilt to serve the screen.

Rejected: designing around current features; reaching for a visual style before the page's
message is settled.

Agrees with: [Decide what the reader must learn before choosing a chart type](data-visualization.md#decide-what-the-reader-must-learn-before-choosing-a-chart-type).

> …口うるさく言ってた何をユーザーは知りたいのか、どう可視化すれば伝わるかなどを徹底的に考えるように。見た目以前に何を表現するペーじなのか
>
> Think thoroughly about what I kept nagging about: what the user wants to know, and how to
> visualise it so it gets across. Before the look, what is the page meant to express?
> (2026-10-31)

> Do not think from the features we have now. Think of the ideal UI and UX from the data we have. All the backend features can be built later or thrown away. (2026-05-04)

> そもそも今やりたいことをゼロから設計した時にどうなるかで考えて欲しい。今のものありきじゃなくて
>
> Think about what it would look like if you designed what I want to do now from scratch, not
> taking the current thing as a given. (2026-09-18)

### Understand the product's concept, taste and vibe first

**(stated)** Before any design decision, know what the product is for and how it should feel.

Agrees with: [Decide the product's character before choosing styles](visual-design.md#decide-the-products-character-before-choosing-styles).

> You should first understand the concept, taste and the vibe of the project before you make any decisions (2026-05-06)

### Think his instructions through, plan first, and push back when unsure

**(strong)** An instruction from him is a starting point. Think about it, plan before building,
and discuss it when something seems wrong.

Rejected: changing something only because he said so.

> do not just blindly implement what I say. make sure you think about it and push back or discuss if unsure. (2026-05-04)

> Did you actually think about everything? or are you just changing because i told you? (2026-05-06)

> plan first. (2026-05-06)

### Back design choices with research and established practice

**(strong)** Colour systems above all, but any non-trivial proposal too: research how
established systems solve it, lay out the patterns, say why the proposal is right and cite the
practice behind it. Questions that already have a researched answer (text size, density, motion,
numerals) are answered from research, not put to him as a taste quiz.

Rejected: patching an existing palette without research; proposals without reasons or sources;
A/B taste quizzes on solved questions.

> 複雑だからちゃんとパターンまとめて。色を誓いすぎるのは良くないと思う。なんでこうすべきだと思ったかとそれを裏付けるベストプラクティスとか。
>
> It's complicated, so organise the patterns properly. I don't think using too many colours is
> good. Tell me why you think it should be done this way, and the best practices that back it
> up. (誓い is a typo for 使い; 2026-11-11)

> いやもっとちゃんと設計して。デザインシステムについて徹底的に調べて
>
> No, design it more properly. Research design systems thoroughly. (2026-11-12)

> やり方はこれではない
>
> This is not the way to do it. (Said of an A/B taste quiz, 2026-10-26)

### Check the work yourself on the real screens before showing it

**(strong)** Open the running product with real data at the real device size, drive it in a
browser, press every control, and compare it with the agreed design. A broken UI never reaches
production, and he is never the one to find a defect that could have been checked.

Rejected: shipping a broken UI; implementation colours that drift from the design; claiming a fix
without checking it.

> 戻すしそもそもUIが壊れているのをProdに出したの？意味がわからない。
>
> Revert it. And did you really ship a broken UI to prod? It makes no sense. (2026-11-23)

> ブラウザ操作とかでテストとかしてる？
>
> Are you testing it, for example by driving a browser? (2026-11-23)

> 治ってないしこれあなたで確認できない？
>
> It's not fixed. Can't you check this yourself? (2026-11-09)

> 要件を全く満たせてないけど。ちゃんとチェックしてないだろ
>
> This doesn't meet the requirements at all. You didn't check properly, did you? (2026-11-21)

### Reach a usable product fast, then polish in use, against a high bar

**(strong)** Getting to daily use comes first, and small UI fixes can follow while the product is
in use. The bar for the finished product stays high: a decent first draft is far from done.

Rejected: work that is "a good starting point but 1/10".

> 細かいUIも大事だが早く使えるとこまで持っていくのが最優先
>
> Fine UI details matter, but the top priority is getting it to a usable state fast.
> (2026-11-11)

> 細かいuiの修正は使えるようになれば使いながらできる
>
> Small UI fixes can be done while using it, once it's usable. (2026-11-10)

> Good starting point but it is 1/10 and not the quality I expect. (2026-05-06)

> あとはシンプルにいいアプリ、可視化されたデータが好き。なのでちゃんとできてないと許せない。
>
> And simply, I like good apps and well-visualised data. So I can't stand it when it isn't done
> properly. (2026-11-23)

### Build only for data that exists, and design the missing-data cases yourself

**(strong)** Leave out parts that have no data behind them; use dummy data only when building
the part is worth it anyway. Design every real case of the data (empty, late, stale, partial) so
each reads right on its own, and keep "nothing yet" visibly apart from "something failed". Find
out from the source whether data exists instead of asking him.

Rejected: placeholder parts with nothing behind them; asking him again and again whether data
exists; flagging plain absence as an error.

Agrees with: [Design every state of every view](interface-design.md#design-every-state-of-every-view) and [Label data that is old or incomplete](interface-design.md#label-data-that-is-old-or-incomplete).

> データがない部分は作らない
>
> Don't build the parts that have no data. (2026-11-07)

> データのあるなしを毎回私に聞くな。いちいち答えるのがめんどい。何回も聞かれている
>
> Stop asking me every time whether data exists. It's a pain to answer each time. I've been
> asked many times. (2026-11-23)

> データがないだけか失敗しているか検知できるようにして。データがないだけの時も何回も指摘されてウザい。
>
> Make it detect whether there's simply no data or whether something failed. Being told about it
> again and again when there's just no data is annoying. (2026-11-07)

### Put decisions to him short, conclusion first, one question at a time

**(strong)** Explain before asking. Keep what he reviews short, say where to look, ask few
questions and one at a time, and make it readable on both phone and desktop.

Rejected: long write-ups where he can't tell where to look; many questions at once; review pages
hard to read on a phone or a PC.

> 長くてわかりにくい
>
> It's long and hard to follow. (2026-11-20)

> どこを見ればいいの
>
> Where am I supposed to look? (2026-11-20)

> 一部答えたが質問が多すぎる
>
> I answered some, but there are too many questions. (2026-11-15)

> まずは教えて。決断させる前に。
>
> Explain it to me first, before making me decide. (2026-11-07)

> スマホでもPCでもみにくい
>
> It's hard to read on both the phone and the PC. (2026-11-12)

> 一つ一つ聞いて
>
> Ask me one at a time. (2026-09-18)

### Sort open questions by whether they need to be seen

**(stated)** A choice that changes what a screen shows or how it is used goes to him as screens;
a choice that words can settle (a threshold, a policy, a cost) goes as text.

> Uiの決断はproposedにしてuxとかバックエンドデザインに関係ない言葉だけでできるものはDecisionsにするとか？
>
> How about putting UI decisions under Proposed [the proposals list], and things that can be
> decided with words alone, unrelated to UX or backend design, under Decisions [the decisions
> list]? (2026-11-10)

### Keep all design pages in one live, browsable place

**(stated)** Every page and sub-page of the design lives in one place that reloads on change,
stays interactive (navigation works), takes written feedback, and lists the open proposals.

> Can we have all pages in one html? like everything under … is in one place. (2026-05-04)

> If we can, I want separate pages but still interactive (like navigations and stuff) (2026-05-04)

> フィードバックも書き込めるようにできる？あとはProposedがあるものは一覧で見えると良さそう
>
> Can we make it possible to write feedback too? It would also be good to see everything that has
> a proposal [in the proposals list] in one list. (2026-11-03)

### Mark in mock-ups where AI works and what changed

**(stated)** A very small label shows every place where AI will analyse or suggest, and each
design change says what the implementation has to follow.

> Also I want you to add a very small label where we should use AI to analyze or suggest so that it would be easier to remember when we implement backend. (2026-05-04)

> I want to make what changed and what frontend needs change obvious. (2026-05-06)

### Choose parts and directions from real demos of several candidates

**(stated)** For UI parts, a logo or a visual direction, build working demos of several popular
candidates, or generate options from several tools, and pick by looking. Include the option he
already said he liked.

Rejected: demos that all look alike; leaving out the source he asked for.

> デモ作ってみて。
>
> Make a demo. (2026-11-05)

> 別のやつでも作ってみて欲しい。人気のやつ調べていくつか
>
> I'd like you to try it with other ones too. Look up a few popular ones. (2026-11-05)

> ロゴを作りたい。案を出して、claude, codex, gemini で生成したい。一番いいのを採用
>
> I want to make a logo. Come up with ideas, generate them with Claude, Codex and Gemini, and
> adopt the best one. (2026-11-07)

> どれもあまり変わらん。beautifuluiはなんで使わないの
>
> None of them are much different. Why don't you use Beautiful UI? (2026-11-05)

## Visual

### Make it fun enough to open every day

**(strong)** The product should be exciting to use. Diagrams, charts and playful touches such
as animated rings and stamps beat plain text and numbers, because they are easier to read as
well as more fun. Fun never costs clarity.

Rejected: flat, dull dashboards of text.

Agrees with: [Decide the product's character before choosing styles](visual-design.md#decide-the-products-character-before-choosing-styles).

> Fun UI and UX so that it is fun to use and makes you want to open it everyday (2026-05-01)

> もっとワクワクするのを作って欲しいんだよね。図とかグラフとかチャートとか。そっちの方が見やすいしワクワクする。ダッシュボードとして
>
> I want you to make something more exciting. Diagrams, graphs, charts. That's easier to read
> and more exciting, as a dashboard. (2026-11-03)

> Make it fun. (2026-05-01)

### A stock component-library look is "not bad", which is not approval

**(stated)** Default library parts laid out as they come read as dull and unrefined, and
rearranging the layout of the same stock look does not change the impression. "Not bad" means
the direction is fine but the work is not shippable.

Rejected: default component-library pieces assembled as-is; cards nested in cards; titles
floating on the page.

Agrees with: [Know the default choices that make an interface read as generated](visual-design.md#know-the-default-choices-that-make-an-interface-read-as-generated).

> 悪くないがまだダサい、垢抜けない
>
> Not bad, but still dull and unrefined. (2026-10-04, as recorded in a work log)

> 全然変わってない
>
> It hasn't changed at all. (Said of the same stock look with a new layout, 2026-10-04)

### "Design" often means the design system

**(stated)** When he says the design is wrong, he often means the visual system (colour, type,
spacing, radius, lines and shadows, icons, density), not the layout or the flow. Compare design
systems with the layout held fixed.

Rejected: answering a look-and-feel complaint with layout and flow questions.

> UIとか配置とかにこだわっているんじゃなく、デザインにこだわっている。デザインシステム
>
> I'm not particular about the UI or the arrangement; I'm particular about the design. The
> design system. (2026-10-05)

### Shape information for the reader instead of boxing it

**(stated)** A display that only crams information in and gives each piece a box feels unkind.
The layout should come from what the reader needs at that moment.

Rejected: box-per-datum layouts.

> 表示が優しくないというか情報を詰め込んだだけ、それの箱を用意しましたって感じが嫌い
>
> I dislike displays that feel unkind, as if they just crammed the information in and provided
> a box for it. (2026-10-20)

### Keep saturated colour out from behind content

**(strong)** A hero card in a strong colour with white text stands out but is hard to read.

Rejected: brand-blue hero cards; white text on blue.

Agrees with: [Meet the WCAG 2.2 contrast minimums for text and for controls](visual-design.md#meet-the-wcag-22-contrast-minimums-for-text-and-for-controls).

> Hero's blue background makes it stand out but makesi it hard to read. (2026-05-04)

> just white with blue background is not easy to see. (2026-05-04)

> I dont like the blue background card. (2026-05-07)

### Group content in light cards on a tinted background

**(stated)** A completely flat layout, with nothing separating groups, is hard to scan. Light
cards on a slightly tinted page do the grouping.

Rejected: flat layouts with no background separation.

Departs from: [Add a border or box only when spacing cannot show the group](visual-design.md#add-a-border-or-box-only-when-spacing-cannot-show-the-group). He finds spacing alone too weak on dense screens.

> hard to see without any background colors (2026-05-04)

### Separate with hairlines rather than shadows

**(inferred)** In the designs he picked, thin borders separate surfaces, and colour marks state.
Read from his choices; he has not said it outright.

Agrees with: [Use a few elevation levels, each with a fixed meaning](visual-design.md#use-a-few-elevation-levels-each-with-a-fixed-meaning).

### Light mode only, unless the product needs dark

**(stated)** Dark mode is not a default requirement.

Agrees with: [Design dark mode as its own palette, not an inversion](visual-design.md#design-dark-mode-as-its-own-palette-not-an-inversion), whenever one is built.

> No dark mode needed (2026-05-01)

### Use famous open-source fonts and icons

**(strong)** Take fonts and icons from well-known existing sets rather than drawing custom ones.
One sans family with a matching mono for numbers is enough; he dropped a decorative serif accent.

Rejected: custom icons; a decorative serif display face (Instrument Serif).

Agrees with: [Use few typefaces, and avoid thin weights at small sizes](visual-design.md#use-few-typefaces-and-avoid-thin-weights-at-small-sizes) and [Use one icon family with one grid, stroke weight and perspective](visual-design.md#use-one-icon-family-with-one-grid-stroke-weight-and-perspective).

> For fonts and icons, just use whatever is out there in the world (2026-05-01)

> Font choice good, just use famous icons not custom. (2026-05-01)

> I don't like Instrument Serif. Get rid of it. (2026-05-01)

### Use icons to identify things

**(stated)** Where a recognisable icon exists, use it to label a category, group or row instead
of bare text or a coloured legend dot.

Departs from: [Label icons unless their meaning is universal](visual-design.md#label-icons-unless-their-meaning-is-universal) only in emphasis; the icon sits beside its label, not instead of it.

> Use icons more effectively. (2026-05-04)

> can we use icons? or is there not a corresponding icons? (2026-05-04)

## Layout and type

### Fit a main screen in one view

**(strong)** A main screen shows what is needed without scrolling, and every button on it is
reachable without scrolling. He finds this beautiful. Detail pages and modals may scroll. Before
adding tabs or pages, improve how the data is presented.

Rejected: main screens where information or actions are below the fold.

Agrees with: [Design a dashboard to be read on one screen, with the important item first](data-visualization.md#design-a-dashboard-to-be-read-on-one-screen-with-the-important-item-first).

> Try to not have any scroll for main pages (ok in details page/modal). If you are going to place a button or icon button, that should be accessible without scrolling. User should not have to scroll to find an information. Make use of tabs, modals, pages if you have to but you should think about improving how you are displaying the data first. (2026-05-01)

> 基本的にスクロールなしで見れるのが美しいと思う。詳細ページは仕方ないが。
>
> I think it's beautiful when you can see it without scrolling. Detail pages can't be helped.
> (2026-11-03)

> I should not have to scroll to access these buttons. (2026-05-04)

### Make the home screen a destination: summaries that open into detail

**(strong)** The most-viewed screen carries the most. Each area gets a headline or compact card
there, and tapping it opens a modal or sheet with the full detail. A home screen that is a set
of links into other screens fails.

Rejected: a sparse home page; a "link entrance".

Agrees with: [Disclose progressively, in no more than two levels](interface-design.md#disclose-progressively-in-no-more-than-two-levels).

> I really like this UX. have summary or short version and open modal to reveal the full details with good UX. (2026-05-04)

> I dont waht the home page to be link entrance (2026-05-04)

> Theres way too little infor in the home page. This is the page that will be seen the most. it should contain more info than this. (2026-05-04)

> have a headline and open modal to reveal further info. (2026-05-04)

### Give every screen an obvious place to look, without going sparse

**(strong)** A busy screen where everything competes fails, and so does a quiet one that says
nothing. The aim is a screen that is informative and not noisy, with detail moved to a sub-page
when needed.

Rejected: cluttered screens; too much text; a redesign with too little information, nothing that
speaks visually, and too little colour.

Agrees with: [Decide the order of importance, then make one element dominant](visual-design.md#decide-the-order-of-importance-then-make-one-element-dominant) and [Test hierarchy by blurring the screen](visual-design.md#test-hierarchy-by-blurring-the-screen).

> Uiがガチャガチャしすぎてきている。何を見ればいいかわからん
>
> The UI is getting far too busy. I can't tell what to look at. (2026-11-09)

> なんか情報量というか文字が多いというか。みにくい
>
> There's too much information, or too much text, somehow. It's hard to read. (2026-11-03)

> bは情報量が少なすぎ、情報が視覚的に何も訴えてこない、色が少ない。今のクオリティだと変えることはできない
>
> B has far too little information. The information says nothing visually, and there's too
> little colour. At this quality I can't switch to it. (2026-11-10)

> Not sure how to not make it too noisy but informative at the same time. maybe we should have it in a different page? or a sub page? (2026-05-04)

### Gather what one moment of use needs in one place

**(strong)** The figures someone steers by in a given moment (today's totals, the trend, what
was done last time) sit together and show at once, not scattered across the app or missing.

Rejected: screens where the day's key totals or the recent history appear nowhere.

Agrees with: [Design for the moment of use](interface-design.md#design-for-the-moment-of-use).

> Gymに行ったときにどこを見ればいいかもわからん。どこに情報が集まってるの
>
> When I go to the gym I don't even know where to look. Where is the information gathered?
> (2026-11-23)

> その日にどれだけのカロリーを摂っていてどれだけのタンパク質を摂っているかどこにも出てない
>
> Nowhere does it show how many calories and how much protein I've had that day. (2026-11-23)

> ジムのサイクルもわかんないし、前に何をどれくらいやったかもパッと出てこない
>
> I can't see the workout cycle, and what I did last time, and how much, doesn't come up at a
> glance. (2026-11-23)

### Order by importance and urgency

**(stated)** The hero goes on top, the most reliable or most important data leads, and when two
items compete, the one that needs action sooner comes first.

Agrees with: [Give each screen one purpose and put the most important thing first](interface-design.md#give-each-screen-one-purpose-and-put-the-most-important-thing-first).

> どっちも出せばいいがurgencyによる。
>
> Show both, but it depends on urgency. (2026-11-13)

(Answer to point 5 of a list of layout questions.)

> 5. under the hero. hero should be on the top. (2026-05-04)

> sleep is the most consistent data. I want related data to be on top (2026-05-04)

### Show each thing once, and treat peers as peers

**(stated)** Each piece of information has one home. Items of equal rank get the same treatment
and structure, and their order stays the same across views.

Rejected: duplicates across pages; a second view of something that already has a card; peers
drawn differently; an order that flips between screens.

Agrees with: [Make things that work alike look alike, and things that differ look different](visual-design.md#make-things-that-work-alike-look-alike-and-things-that-differ-look-different).

> Why is recovery and sleep treated different? Shouldnt sleep, revocery, stress treated like equal? (2026-05-06)

> dont need workout history git-like stuff. we laready have this week card (2026-05-06)

> why is order flipped? (2026-05-06)

### Share the header and navigation, and never ship a broken layout

**(strong)** Headers, navigation bars and other repeated chrome are shared components that look
the same on every screen. Nothing collides with the notch or status bar, overflows or
misaligns.

Rejected: headers that differ page to page; content under the notch.

Agrees with: [Be consistent inside the product and with the platform](interface-design.md#be-consistent-inside-the-product-and-with-the-platform).

> theres no consisitency in headers and navbar. make them a component and make it consistent (2026-05-04)

> 画面の上がNotchと重なる…
>
> The top of the screen overlaps the notch… (2026-11-03)

> あとui崩れてるの気になった
>
> Also, I noticed the UI is broken. (2026-11-11)

### Avoid horizontal scroll strips

**(stated)** Rows of content that scroll sideways hide what is in them.

Agrees with: [On phones, use linear layouts and give the plot the full width](data-visualization.md#on-phones-use-linear-layouts-and-give-the-plot-the-full-width).

> useless horizontal scroll (2026-05-04)

### Give text room to breathe

**(stated)** Text packed tight makes a screen feel cramped and anxious even when it fits.

Agrees with: [Choose density for the task, and let people change it](visual-design.md#choose-density-for-the-task-and-let-people-change-it).

> 全体的に文字詰めすぎ。余裕がなくて詰まってる印象
>
> The text is packed far too tightly overall. There's no room and it feels cramped.
> (2026-11-16)

### Justify Japanese type choices with published guidance

**(stated)** He prefers the feel of American product UI, and rounded or stock Japanese web fonts
felt off in mock-ups. Pick Japanese type from published guidance, not by feel.

Rejected: mock-ups set in Zen Maru Gothic, Zen Kaku Gothic and Noto Sans JP.

Agrees with: [Choose the typeface on purpose](visual-design.md#choose-the-typeface-on-purpose).

> キモい
>
> Creepy. (Said of the Japanese font mock-ups, 2026-10-20)

### For review screens, one recommended option and one primary button

**(inferred)** A pattern he accepted for decision screens: the recommended option as a card with
a one-tap accept, options as whole-row tappable cards, one primary submit button per screen, the
accent colour only on that button, the recommendation and the chosen option, and column headers
aligned at the same height.

Rejected: a top page that is only two buttons.

## Colour

### Define what each colour means across the product before using it

**(strong)** Fix the palette and the meaning of each colour for the whole product first. With a
defined palette, colour questions on single screens answer themselves. Show him the palette.

Rejected: colour picked case by case; colour rules invented without him (such as "don't lean on
colour").

Agrees with: [Name colours by role, not by value](visual-design.md#name-colours-by-role-not-by-value) and [Use one colour for one meaning](visual-design.md#use-one-colour-for-one-meaning).

> 色で攻めないって決まり初めて聞いた。なんならアプリ全体で色ごとの意味を先に定義すべきって言おうと思ったくらいだったが。パレット含め。
>
> This is the first I've heard of a rule against leaning on colour. If anything, I was about to
> say we should define the meaning of each colour across the whole app first. Including the
> palette. (2026-11-10)

> そもそもColor paletteがちゃんと定義されていれば迷わないと思うけど。
>
> If the colour palette were properly defined, there'd be no hesitation in the first place.
> (2026-11-15)

> パレットを見せなさい
>
> Show me the palette. (2026-11-12)

### Keep colour consistent everywhere

**(strong)** The same meaning gets the same colour on every screen and chart, and the build
matches the design's colours exactly. Colour carries meaning, never decoration.

Rejected: inconsistent colouring; two hues side by side for no reason.

Agrees with: [Use one colour for one meaning](visual-design.md#use-one-colour-for-one-meaning) and [Use colour only when it carries meaning](data-visualization.md#use-colour-only-when-it-carries-meaning).

> Coloring is inconsistent across the whole design (2026-05-01)

> I hate how the color doesn't have consistency. (2026-05-06)

> I hate the coloring here too. why green and blue bar? (2026-05-06)

> Spendingの色がおかしい。そもそも…とマッチしてる？適当にやるな
>
> The colour of Spending is wrong. Does it even match the design? Don't be sloppy.
> (2026-11-21)

### Build the palette from colour-system research, bright, and keep one that works

**(strong)** Design a palette from scratch on established colour-system practice (roles, usage,
tonal palettes) and explain the mapping. The result should feel bright, not dark or gloomy. A
palette refined over many rounds stays unless the new one is clearly better.

Rejected: patching the current colours instead of researching; a palette that felt dark;
replacements worse than the current palette.

Agrees with: [Define colours in a perceptual space such as OKLCH](visual-design.md#define-colours-in-a-perceptual-space-such-as-oklch) and [Fix each colour's shades in advance](visual-design.md#fix-each-colours-shades-in-advance).

> ちゃんと色は調べてその色とそのマッピングになった？
>
> Did you actually research the colours and end up with those colours and that mapping?
> (2026-11-11)

> 暗い印象を受けるので却下。あとcolor systemについて調べた？今あるのを治すんじゃなくてゼロからやり直して
>
> Rejected, it gives a dark impression. Also, did you research colour systems? Don't fix what's
> there, start over from zero. (2026-11-13)

> パレットなのか使い方なのかわかんないけど今のままの方が断然いい
>
> I don't know if it's the palette or how it's used, but the current one is far better.
> (2026-11-13)

### Never let a screen collapse into one hue

**(strong)** Distinct things (sections, categories, exercises) get distinct colours from the
palette, so a page can be read and feels alive. A page in one colour reads as unconsidered.

Rejected: pages in one purple; every item in one orange; too little colour.

Departs from: [Keep context grey and spend one strong colour on the point](data-visualization.md#keep-context-grey-and-spend-one-strong-colour-on-the-point) at the scale of a whole screen. Agrees with [Pick the palette type from the data: sequential, diverging or categorical](data-visualization.md#pick-the-palette-type-from-the-data-sequential-diverging-or-categorical) for distinct series.

> the pages have one purple color. it is just following the UI from other pages and it is not thought through. (2026-05-06)

> I hate how workout exersise [sic: exercise] only has one orange color. fixi [sic: fix] it. (2026-05-06)

> 色が少ない。
>
> Too little colour. (2026-11-10)

### Use colour for status sparingly, and don't double it up

**(stated)** Keep signal colours few so they keep their force. Marking one difference with both
an added element and a colour looks alarming.

Rejected: over-coloured screens; a label plus a colour on the same flag.

Agrees with: [Keep most of the interface neutral and spend accent colour on meaning](visual-design.md#keep-most-of-the-interface-neutral-and-spend-accent-colour-on-meaning). Departs from [Never carry information by colour alone](visual-design.md#never-carry-information-by-colour-alone) in emphasis: keep the redundant cue quiet (a sign or an arrow, not an extra badge).

> 色を誓いすぎるのは良くないと思う。
>
> I don't think using too many colours is good. (誓い is a typo for 使い; 2026-11-11)

> 足すのと色で区別すると視覚的にやばいってなりそう
>
> Distinguishing it by both adding something and colouring it would probably look visually
> alarming. (2026-11-10)

### Red means worse for the user, green better, whatever the sign

**(strong)** Colour a change by what it means for the user, not by its arithmetic sign. Spending
going up is red; spending going down is green.

Rejected: red and green tied to plus and minus.

Agrees with: [Never let colour be the only way to tell data apart](data-visualization.md#never-let-colour-be-the-only-way-to-tell-data-apart), paired with a sign or arrow.

> 私に取ってのマイナスが赤。なのでこの場合は支出が増えたら赤
>
> Red is what's negative for me. So in this case, spending going up is red. (2026-11-12)

> spendingが上がるのは赤では？下がったら緑では？
>
> Shouldn't spending going up be red? And going down green? (2026-11-11)

## Motion and interaction

### Motion adds delight to a good base and stays restrained

**(strong)** Fun comes first from good content and a good base. Motion adds to it (a ring that
fills, a number that counts up, a short confirmation, a brief fade) but cannot rescue a dull
layout. That too much of it annoys him is (inferred) from his rejections.

Rejected: decorating a boring base with motion; bouncing, spinning and press-shrink effects.

Agrees with: [Animate only to explain a change](interface-design.md#animate-only-to-explain-a-change), with room for celebratory progress animation.

> …アニメーションをつけるとかじゃなくて根本のUIがつまらない。…ベースがつまらないものを装飾してもつまらない。
>
> …It isn't about adding animation; the underlying UI is boring. … Decorating something whose
> base is boring is still boring. (2026-10-04)

> I want to make this ring more fun ui. maybe have animation? (2026-05-04)

### Every affordance does what it promises

**(strong)** A chevron appears only on rows that open, every button and range control works,
and every menu and sheet a screen implies has been designed.

Rejected: ">" on rows that don't open; dead buttons; menus nobody thought through.

Agrees with: [Make interactive elements look interactive](interface-design.md#make-interactive-elements-look-interactive), and its converse.

> あと開けないなら>の表示意味わからん
>
> Also, if it can't be opened, showing ">" makes no sense. (2026-11-22)

> 他にも＞があるのに開けないとこがあるんだが。
>
> There are other places too that have ">" but can't be opened. (2026-11-23)

(1Y and All were a chart's time-range buttons.)

> 1Y allも押せないし
>
> And I can't even press 1Y or All. (2026-11-23)

> check for ui that is not thought of … Like clicking this button does notthing now, menu modal is not though of, etc. (2026-05-04)

### Navigation feels native and instant

**(stated)** Tapping a tab opens the page at once, with no visible load after the tap. On the
web, don't imitate native-app chrome; a web bottom bar that lags feels poor.

Rejected: tabs that load after the tap; iOS-style buttons, tab bars and nav bars on web pages.

Agrees with: [Respond within 0.1 second and finish within 1 second](interface-design.md#respond-within-01-second-and-finish-within-1-second) and [Be distinctive in the surface, conventional in the behaviour](visual-design.md#be-distinctive-in-the-surface-conventional-in-the-behaviour).

> ボタンを押してからロードされるのでタブ感がない。ネイティブなら押したら直ぐにページが開く。
>
> It loads only after you press the button, so it doesn't feel like a tab. In a native app the
> page opens the moment you press. (2026-11-08)

> したのナビゲーションバーがwebだからかuxが悪い。
>
> The bottom navigation bar has bad UX, maybe because it's web. (2026-11-07)

> ネイティブアプリじゃないのにネイティブアプリっぽいボタン？たぶ？ナビゲーションバー？なの嫌い
>
> Native-app-looking buttons? Tabs? A navigation bar? When it isn't a native app, I hate that.
> (2026-10-29)

### Choose spinners and skeletons deliberately

**(strong)** One consistent rule decides which loading indicator appears where.

Rejected: spinners and skeletons used interchangeably.

Agrees with: [Match the loading indicator to the wait](interface-design.md#match-the-loading-indicator-to-the-wait) and [Show content as soon as you have it, not a spinner](interface-design.md#show-content-as-soon-as-you-have-it-not-a-spinner).

> loading spinnerとskeleton はちゃんと使い分けて
>
> Use loading spinners and skeletons each for their proper case. (2026-11-09)

> loading とスケルトンの使い分けもできてない
>
> It doesn't distinguish properly between loading and skeletons either. (2026-11-16)

### Take the pain out of input, and make corrections quick and fun

**(strong)** Capture automatically by default, because people forget to log and stop using
anything with friction. When the system guesses, correcting it is fast and even enjoyable (in
chat, with a swipe), and the corrections teach the system.

Rejected: required manual entry; flows that depend on remembering to log.

Agrees with: [Ask only what you need, one thing at a time when it helps](interface-design.md#ask-only-what-you-need-one-thing-at-a-time-when-it-helps).

> Take pain away of input from the user as much as possible. (2026-05-01)

> 基本自動で。uxが悪いと使わなくなる
>
> Automatic by default. If the UX is bad, I'll stop using it. (2026-09-26)

> calorie in data will be unreliable. i tend to forget to log (2026-05-04)

> 結構間違ってることあるからすぐチャットで直せるように。そのuiuxも工夫して楽しくして
>
> It's often wrong, so make it fixable right away in chat. Put thought into that UI/UX too and
> make it fun. (2026-11-10)

> I want auto categorization, and correct it if it is wrong manually. we should also have was it necessary? swipe (like tinder) so that we can get valuable info from the user. (2026-05-04)

### The user stays in control, and sets the goals

**(strong)** The system may advise, but it does not decide, reorder or hide things on its own.
Goals are set and edited by the user in the UI and settings. A goal that comes out of an AI
conversation appears as a card to approve.

Rejected: tools that take the initiative and get it wrong; AI-proposed goals; goals that can't
be edited.

> 全ての主導権をツールが握ってるのは間違っていた時にウザい
>
> When the tool holds all the initiative, it's annoying when it's wrong. (2026-10-22)

> 目標の提案はしない。目標は私が設定する。AIチャットで壁打ちしたりとかならカードで承認を出して。
>
> No goal suggestions. I set the goals. If it comes out of bouncing ideas off the AI chat, show a
> card for approval. (2026-11-15)

> だから、目標は設定でできるようにしてって
>
> Like I said, make goals settable in settings. (2026-11-11)

### No suggestion chips, prompt hints or feature explainers

**(strong)** Assume the user knows every feature.

Rejected: suggested prompts; "ask the assistant about this" links; subtitles that explain what
the user could do; attention or to-do nag cards.

Departs from: [Make an empty state explain itself and lead to the next step](interface-design.md#make-an-empty-state-explain-itself-and-lead-to-the-next-step) for a product whose only user knows it.

> We dont ever need these suggestions. assume user knows all about the features. (2026-05-04)

> Never have suggestions in this app (2026-05-04)

> I thought I was clear I never need suggestions (2026-05-06)

> do not need Attention (2026-05-04)

### Prefer a screen that shows the state over a notification about it

**(stated)** If a state matters, the screen shows it where the user already looks, so no alert
is needed to announce it.

Agrees with: [Keep the system status visible](interface-design.md#keep-the-system-status-visible).

> そもそも知らせなくていいと思う。それがすぐわかるuiにすればいい
>
> I don't think it needs to notify me at all. Just make a UI where you can tell right away.
> (2026-11-10)

### Status messages must be true

**(stated)** A false warning (a sync shown as down when it isn't) makes the whole screen
untrustworthy.

Agrees with: [Label data that is old or incomplete](interface-design.md#label-data-that-is-old-or-incomplete).

> …のsync落ちてるって出てるけど嘘じゃない？
>
> It says the sync is down, but isn't that false? (2026-11-22)

### Enter inserts a new line in a multi-line input

**(stated)** In a multi-line text box, Enter adds a line break; sending is a separate button
or shortcut, so a half-written message is never sent by accident.

Rejected: Enter to send.

> あとEnterは送信でなくて改行。
>
> Also, Enter should be a line break, not send. (2026-11-23)

### When two designs are both plausible, make them switchable

**(stated)** Put the variants behind a setting or feature flag so both can be tried in real use.

Agrees with: [Use A/B tests for questions a metric can answer](interface-design.md#use-ab-tests-for-questions-a-metric-can-answer), for a single user.

> これは両方試したい。feature flagとかで両方試せるというか設定で変えれるようにできる？そもそも設定で帰れる仕組みはあって損しないかもね
>
> I want to try both. Can we make it switchable in settings, with a feature flag or something?
> Having a mechanism to change things in settings probably doesn't hurt anyway. (帰れる is a
> typo for 変えれる; 2026-11-11)

## Copy and numbers

### Say it with labels, numbers and charts, not sentences

**(strong)** Meaning should go in effortlessly through the UI and the visualisation. Walls of
text, long logs and reports that demand reading effort do not get read; give the minimum the
reader needs.

Rejected: reports written as a dump of text; long logs full of unneeded information.

Agrees with: [Write in plain words, front-loaded for people who scan](interface-design.md#write-in-plain-words-front-loaded-for-people-who-scan).

> レポートも文字でばーっと書かれてたり、cognitive loadを使うものだと私は見ない。uiやdata visualizationなどどう重要なところをすっと頭に入ってくるように伝えるかも大事。
>
> If a report is just a wall of text or something that takes cognitive load, I won't look at it.
> How you convey the important parts so they slip straight into your head, through UI and data
> visualisation, matters too. (2026-09-23)

> いやログ長すぎ不要な情報が多い。…私が知らないといけない最低限の情報って何？
>
> No, the log is far too long, with lots of unnecessary information. What's the minimum I need to
> know? (2026-09-25)

### One language per interface

**(stated)** Never mix languages on a screen. Offer separate language modes in settings if both
are needed. Names that come from the data (merchants, places) stay as they are.

Rejected: Japanese and English mixed on one screen.

Agrees with: [Match the user's words and world](interface-design.md#match-the-users-words-and-world).

> 改善したが日本語と英語は混ぜないで。日本語モードと英語モード設定で分けるとかならいいが。
>
> It's improved, but don't mix Japanese and English. Separating them into a Japanese mode and an
> English mode in settings would be fine. (2026-11-08)

> 基本は英語にしようと思っていた。データは仕方ないにしろ。
>
> I was planning to make it English by default. Data can't be helped, though. (2026-11-08)

### Plain, literal names

**(stated)** Use the obvious word, with the right connotation. Clever names are rejected.

Rejected: clever names; a clinical word for something about fitness.

Agrees with: [Write in plain words, front-loaded for people who scan](interface-design.md#write-in-plain-words-front-loaded-for-people-who-scan).

> もっとシンプルでいい。… Dont try to be clever
>
> It can be simpler. Don't try to be clever. (2026-09-18)

> Vitalsは脈拍とかの印象。医療現場の。フィットネスが入ってなくない？
>
> "Vitals" gives the impression of pulse and so on, a medical setting. Fitness isn't in it, is
> it? (2026-09-18)

### Write currency in the form native to it

**(stated)** Default to the user's own currency. For currencies written in full digits, such as
the yen, show every digit instead of "k" abbreviations.

Rejected: "k" on yen amounts.

Departs from: [Round to the precision the reader can use](data-visualization.md#round-to-the-precision-the-reader-can-use) where the rounding is an abbreviation the currency doesn't use.

> kやめて全部桁表示しよう。日本円とkはあまり相性が良くない
>
> Let's drop "k" and show every digit. Japanese yen and "k" don't go well together.
> (2026-11-11)

> Default should be yen. (2026-05-04)

### No minus sign or colour when the label already says what a number is

**(stated)** A figure labelled as spending is read as spending. Signs and colour are for changes
and comparisons.

Rejected: minus signs and red on amounts that are plainly outflows.

Agrees with: [Write changes with a sign, a base, and the right kind of percent](data-visualization.md#write-changes-with-a-sign-a-base-and-the-right-kind-of-percent).

> Spendingなのが明確ならマイナスをつけなくていい。色もつけなくていい。spendingとして見るんだから。
>
> If it's clearly spending, it doesn't need a minus sign. It doesn't need a colour either. You're
> looking at it as spending. (2026-11-11)

### Show prices as the realistic total

**(stated)** A price is the total actually paid for a stated case, never a "from" figure.

(Said about the prices on a list of trip bookings.)

> 料金は絶対に総額で最安値とかじゃなく現実的なのを書く
>
> Prices must always be the realistic total, not the cheapest. (2026-11-12)

## Charts and data storytelling

### Show important data visually, and say what the numbers mean

**(strong)** The core job of a data screen is to make the important data understood at a glance.
A list of bare numbers fails even when the numbers are right.

Rejected: cards that only list figures; a score shown only as a number.

Agrees with: [Show every key number against a reference](data-visualization.md#show-every-key-number-against-a-reference).

> core concept of this app is presenting the important data visually and making it easy to understand for the user. Just having numbers listed is not good. What do those numbers mean? (2026-05-05)

> make last night card more visual not just numbers (2026-05-06)

> Lacking visual data (2026-05-04)

### One glance first, every detail on drill-down

**(strong)** The overview answers in one glance; the drill-down holds every bit of detail the
data supports, not a thinner copy of the overview.

Rejected: detail views that offer no more than the summary.

Agrees with: [Do not hide critical information behind interaction](data-visualization.md#do-not-hide-critical-information-behind-interaction): the critical part is on the overview, the depth behind the tap.

> Gives you data in one glance so that you don't have to spend minutes understanding the data (2026-05-01)

> Can dive deep if we want (2026-05-01)

> I want the sleep chart? graph? that oura has. I want every bit of detail. (2026-05-04)

### Test a screen against the product's concepts

**(stated)** Fun to open daily, readable in one glance, rewarding to drill into, connecting data
across areas, and changing everyday decisions for the better.

> the concepts are: fun UI/UX, one-glance data, drill-down, cross-domain AI suggestions, influence decisions (2026-05-01)

> In result, influences your everyday decision you make in a good way (2026-05-01)

### Depth within an area first, then connections across areas

**(stated)** Show how one thing affects another (training and body composition, for example),
built on top of thorough data within each area.

> I want in-depth detail about data first of all and I want it tied or connected to other data like how my training is affecting my body composition vice versa. (2026-05-04)

> Connect data between different domains and give suggestions (AI) (2026-05-01)

### Every metric earns its place by helping a decision

**(strong)** Cut forecasts, vanity ratios and metrics the user does not act on, however
interesting, and lead with the metric that serves the user's actual goal rather than a
platform's default.

Rejected: forecast strips; summary ratios nobody uses; novelty cross-correlations; a map shape
where pace is what matters; stock metrics the user doesn't care about.

Agrees with: [Remove elements that do not help read the data](data-visualization.md#remove-elements-that-do-not-help-read-the-data).

> Next 14 days forcast is not useful. I would rather have subscription detected. (2026-05-04)

> although these are interesting povs but i dont think some of them are useful (2026-05-04)

> we dont need map polygon. just have pace and stuff. (2026-05-06)

> dont care about steps i care more about calories (2026-05-04)

### Every mark has a meaning, and each idea gets one chart

**(stated)** Remove a mark or colour whose meaning the reader can't name instead of explaining
it, and merge two charts that show the same thing.

Rejected: an unexplained coloured bar; two charts of the same data.

Agrees with: [Use colour only when it carries meaning](data-visualization.md#use-colour-only-when-it-carries-meaning).

> I dont like … purple bar. Not sure what it means just remove it. (2026-05-06)

> I dont like the layout graphs and charts represent the same thing? (2026-05-06)

> There's lots of duplicate in … page nad … page. re-consider layout and what page shows what. (2026-05-06)

### Present borrowed data better than its source does

**(stated)** An app built on another product's data has to show it better. Copying the source's
chart literally, or linking out to the source app, defeats the purpose. A plain wrapper is
acceptable only when nothing more can be added.

Rejected: a wrapper whose UI is worse than the original; "open in the other app" links; a copied
diagram without the numbers that made it readable.

> OK this is just a wrapper of … right? 1, I dont like it when it is just a wrapper 2, the ui is better in the … app. can we do something about it? (2026-05-04)

> link to app defeats the whole point of this app. (2026-05-04)

> I dont know where it is pointing to because left and right don't have number. You just copied the … UI but terrible. think again. (2026-05-06)

### Print the scale on every chart, and keep labels off the marks

**(strong)** Every chart meant to be read prints its scale and values with units: the maximum
at the top left and the minimum at the bottom left, inside the chart. Every number says what it
refers to, and no label overlaps a mark. This is an explicit rule, checked on every chart.

Rejected: charts without labels; bare edge values; text drawn over bars.

Agrees with: [Use round tick values and a few light gridlines](data-visualization.md#use-round-tick-values-and-a-few-light-gridlines) and [Always show the unit, close to the number](data-visualization.md#always-show-the-unit-close-to-the-number).

> there are so many graphs and charts without label so I dont know the scale. Check all of them (2026-05-06)

> there is no scale. (2026-05-04)

> top left is the maximum and bottom left should be the minimum (2026-05-07)

> make it so that it doesnt overlap with the bar (2026-05-06)

### Readability beats aesthetics in every chart

**(strong)** Faint lines, low-contrast fills and decorative treatments that cost legibility are
wrong.

Rejected: a pretty chart over a readable one; bars in colours that are hard to see.

Agrees with: [Make supporting elements just visible enough](data-visualization.md#make-supporting-elements-just-visible-enough).

> グラフは見やすいようにすることaestheticを優先しないこと
>
> Make charts easy to read; don't prioritise aesthetics. (2026-11-23)

> hard to see the bottom bar with this color (2026-05-06)

> still difficult to see. what is the difference between origina … ui and ours? Why is ours hard to see? (2026-05-04)

### Draw scores, progress and composition as rings, the same way everywhere

**(strong)** He is particular about circular charts: rings, donuts and multi-rings like Apple's
activity rings, with one chart type per kind of value across the product. A row of rings for the
week is welcome. Small shares stay readable in a donut with a legend where a thin stacked bar
turns them into slivers.

Rejected: a bar for a score; a score as a ring in one place and a bar elsewhere; thin stacked
composition bars; redesigns that drop the rings.

Departs from: [Avoid pie and donut charts when slices must be compared](data-visualization.md#avoid-pie-and-donut-charts-when-slices-must-be-compared). Keep the segments few and print the values, so the comparison doesn't rest on angle alone.

> I hate bar representing the score. use circle donut graph like everywhere else. (2026-05-06)

He has said he is "quite particular" about circular charts (2026-11-10; quoted in [Refine a
tuned screen one or two spots at a time](#refine-a-tuned-screen-one-or-two-spots-at-a-time-after-reading-its-history)).

> this should be a ring or whatever else. hard to see details (2026-05-04)

> I like apple fitness ring. calorie burn with donut multi ring. maybe have a week of rings shown? (2026-05-04)

> recov [recovery] can be a ring too so double donut ring (2026-05-06)

### No horizontal gauge bars for a single value

**(stated)** Use a number with its change, a sparkline or a ring instead.

Rejected: horizontal range bars and gauges.

> I hate these horizontal bars. never do this (2026-05-06)

### Draw trends as straight segments through many points

**(stated)** For a time series of discrete points, plot many points joined by straight lines.
Smoothing invents shape between sparse points, and bars make a trend look worse.

Rejected: smoothed lines through monthly points; bar columns for a trend.

Agrees with: [Use bars for amounts by category and lines for change over time](data-visualization.md#use-bars-for-amounts-by-category-and-lines-for-change-over-time) and [Mark missing and estimated values; never fill them with zero](data-visualization.md#mark-missing-and-estimated-values-never-fill-them-with-zero).

> smooth like is not a good fir for this usecase. (2026-05-04)

> Dont use bar chart. looks even worse. just use straight line with a lot of plots. (2026-05-04)

### Pick a scale and range that make the change visible

**(stated)** A small change on a large base vanishes on a zero-based axis. Offer short ranges
(one month, three months) when growth is small against the total, and make every range control
work. A hero chart that is "just a line" carries nothing.

Rejected: a hero chart with almost no data; growth flattened against a large baseline.

Agrees with: [Set a line chart's range to show meaningful variation, and say where it starts](data-visualization.md#set-a-line-charts-range-to-show-meaningful-variation-and-say-where-it-starts).

> youshould think about how to present the data more. hard to see the growth for 3M (i also want 1m growth option too) since the scale is 0 - … and growth is little. (2026-05-04)

> Hero chart contains almost no data. It's just a line. (2026-05-04)

### Show progress toward every goal

**(strong)** Wherever a goal exists, the card or chart shows how far along it the user is: a goal
line or marker, the gap, short-term and long-term goals. Visible progress is what motivates.

Rejected: cards where progress against the goal can't be read.

Agrees with: [Show every key number against a reference](data-visualization.md#show-every-key-number-against-a-reference).

> ここもゴールに対してどれだけ進んでるかがわからん。
>
> Here too, I can't tell how far I've progressed toward the goal. (2026-11-23)

> add goal to the … card or in a new card. I cant see the progress. (2026-05-06)

> Let's have a graph + short term goals and long term goals setable (2026-05-04)

> ちゃんと行っただけ伸びてると数字で出るのがモチベにつながる。
>
> Seeing in numbers that I improve as much as I actually go is what motivates me. (2026-11-23)

### Frame imprecise tracking as a daily target, not exact accounting

**(stated)** When inputs can't be measured exactly, track whether the daily target was hit, as
a way to build awareness and habit.

> カロリー消費、タンパク質摂取、カロリー摂取は毎日ゴールに届いてるか、治ってるかでメインにトラッキングする。これは正確にやるのが不可能だから意識する習慣をつける意味が強い。
>
> Calories burned, protein and calories eaten are tracked mainly by whether they hit the daily
> goal or stay within it. Doing it precisely is impossible, so it is mostly about building the
> habit of being aware. (治ってる is a typo for 収まってる; 2026-11-23)

### Show habits as slots that fill

**(stated)** Stamps, a week of rings or dots, a streak with a seven-day strip: these motivate
more than a plain count.

> workoutの回数のスタンプはいいと思った。
>
> I liked the stamps for the number of workouts. (2026-11-10)

### A breakdown answers "where did it go?" at a glance

**(strong)** Summarise, group and visualise first, then let the user drill into records. Kinds
that behave differently (fixed costs, subscriptions, variable spending) are visible as separate
kinds. If the user still can't tell after opening the full list, the visualisation has failed.

Rejected: relying on a "see all transactions" list to explain a total.

Agrees with: [Sort categories by value unless they have a natural order](data-visualization.md#sort-categories-by-value-unless-they-have-a-natural-order).

> 何にそんなに出費しているかわからん。See all transactionsを見ても結局わからん。Data Visualizationがちゃんとできていない証拠。
>
> I can't tell what I'm spending so much on. Even after looking at "See all transactions" I still
> can't tell. That's proof the data visualisation isn't done properly. (2026-11-23)

> お金も全てを正確にと言うのは難しい。だから固定費やサブスクを見える化したりカテゴリを分けて何に使いすぎてるかをわかるようにしてる
>
> With money, getting everything exact is hard too. That's why I make fixed costs and
> subscriptions visible and split categories, so I can see what I overspend on. (2026-11-23)

> Where is the breakdown of my spendings? (2026-05-04)

### Show composition and growth together

**(stated)** The parts of a whole and the whole's growth should read in one glance. Borrow that
idea from a product that does it even when its drawing is weak.

Rejected: copying a reference product's UI along with its idea.

> I dont like the UI of … but I like the idea. You can see the composition and the net worth grow in one glance. (2026-05-04)

### Prefer the figure that is true over the one that is live

**(strong)** A settled period (last month, the year) beats a real-time number that lags or timing
can make wrong. Respect the data's real cadence: an annual payment stays annual. Keep apart the
categories the user asked to keep apart, and leave out items that don't belong.

Rejected: an "available to spend" figure that lag can make a lie; annual charges spread into
months; subscriptions mixed with living costs; non-subscription items listed as subscriptions.

Agrees with: [Make the title say only what the data supports](data-visualization.md#make-the-title-say-only-what-the-data-supports) and [Make visual differences proportional to data differences](data-visualization.md#make-visual-differences-proportional-to-data-differences).

> 収支。これが一番正しい。使えるお金はラグのせいで嘘かもしれない
>
> The balance. It's the most accurate. "Money you can spend" might be a lie because of the lag.
> (2026-11-10)

> 収支をリアルタイムで本当にいるかから考えるべき。先月の結果とかならわかるけど。過去のことだし。あとは年で数えれば誤差が減る
>
> We should start by asking whether we really need the balance in real time. Last month's result
> makes sense, since it's in the past. And counting by the year reduces the error. (2026-11-11)

> 年間のを無理やり月にしてない？明確に違うって言ったのがまだ入ってる。…色々と間違ってる。
>
> Aren't you forcing the annual ones into monthly? Things I clearly said were different are
> still in here. … Lots of things are wrong. (2026-11-15)

> …サブスクと生活費とかは分けたいって何回も言っている
>
> I've said many times that I want subscriptions and living costs kept separate. (2026-11-21)

### Compare like for like

**(inferred)** A comparison with "usual" uses the same point in the period, averaged over past
periods. One-off items count in the total but stay out of the comparison and are named
separately. Read from the options he picked.

Agrees with: [Show every key number against a reference](data-visualization.md#show-every-key-number-against-a-reference).

Picked option (option 1, "as in B", for what "usual" means):

> 1(B のとおり(過去 6 か月の同じ日までの平均))
>
> 1 (as in B: the average up to the same day over the past six months). (2026-11-24)

Picked option (option 1, "as in B", for one-off items):

> 1(B のとおり(合計には入れ、ふだんとの比べからは外して名前で出す))
>
> 1 (as in B: include it in the total, leave it out of the comparison with usual, and show it by
> name). (2026-11-24)

## AI-written text

### AI says what the user would not notice alone

**(strong)** Patterns by weekday or season, or one behaviour driving another, stated as specific
findings. Generic advice, restating the numbers, and interesting-but-useless pairings have no
value.

Rejected: generic, obvious statements; AI lines that repeat what the screen already shows.

> 普通では気づかないことに気づかせてくれるようにしたいという話。ただの例だが、曜日によってカロリー消費が多いとか、毎年夏は出費が増えがちとか、睡眠が少ない日は食べすぎがちとか。
>
> The point is that I want it to make me notice things I normally wouldn't. Just as examples:
> burning more calories on certain weekdays, spending tending to rise every summer, eating too
> much on days with little sleep. (2026-11-15)

> 一般的なこと言われても何も有意義じゃない
>
> Being told general things isn't meaningful at all. (2026-10-31)

### AI text never crowds out the data

**(strong)** Insights are embedded sparingly where the related data is: one finding or nothing.
On a data page the visualisation comes first, and AI commentary goes to the bottom or goes away
once real content is on screen.

Rejected: AI analysis cards everywhere; AI findings above the data; AI text taking most of a
page.

> これはすでに話している。随所に埋め込むって話。ちゃんと理解してる？
>
> We've already discussed this. The idea is to embed it throughout. Do you actually understand?
> (2026-11-15)

> AI findings (HOW YOUR xxx is yyy) should be at the very bottom if they should be there at all. (2026-05-05)

> lets remove these ai-analysis stuff completely from everywhere now that we have contents to display (2026-05-06)

> I don't like how the AI stuff is taking 80%, 90% of the page (2026-05-06)

### Offer a possibility, don't assert a conclusion

**(stated)** "This might be a subscription" is better than deciding it outright.

Rejected: AI that jumps to conclusions about the user's data.

> サブスクかもよと表示するのがベストでは？決めつけるのでなく。
>
> Showing "this might be a subscription" is best, isn't it? Not jumping to conclusions.
> (2026-10-20)

### Judge relatively, and encourage

**(stated)** AI judgements compare against the day's intake, the trend or whether a key need was
met, not a countdown from a limit. For coaching, add suggestions and encouragement, not only
facts.

Rejected: "remaining from your limit" arithmetic as the message.

> 上限からのひきざんじゃなくてその日の摂取だったりトレンドだったり相対的に判断できることに使って。
>
> Not subtraction from a cap. Use it for things you can judge relatively, like that day's intake
> or the trend. (2026-11-15)

> I also want suggenstions, progress encouragement for training. not just facts. (2026-05-04)

### Text labelled as AI is generated, and the reader can tell AI from computed

**(stated)** Canned sentences presented as AI output make no sense. Make it clear which parts of
a report are AI-written and which are computed.

> …がaiなので決まった文は意味わからん。
>
> It's an AI, so fixed sentences make no sense. (2026-11-11)

> which part of these reports are AI generated and which are generated in our backedn? (2026-05-07)

### An assistant is a simple chat with tools

**(stated)** Plain conversation and tool calls first, with data visualisation as a tool so
answers can be drawn inline. Decide once, for the whole assistant, which few actions deserve a
dedicated card. What the assistant remembers is editable from settings at any time.

Rejected: designing AI cards one at a time; prompt suggestions in the chat.

> What I want are toolcalling, data visualization tools (2026-05-05)

> first, just keep it a simple chat with toolcalling. (2026-05-05)

> 個別で考えるより一気にの方が良さそう。基本は会話とtool callingでもできるしわざわざカードをだしたいのはどれかって
>
> It seems better to think about it all at once rather than one by one. Basically it can all be
> done with conversation and tool calling, so the question is which ones we actually want to show
> as a card. (2026-11-11)

(Answer to point 2 of a list of questions about an AI assistant's memory.)

> ２。メモリーはすぐ設定から編集できるように
>
> 2. Make the memory editable right away from settings. (2026-11-23)

### An assistant replies in the user's language, politely

**(stated)** An AI assistant answers in the language the user wrote in and keeps a polite
register, never slipping into casual speech.

Rejected: answering in another language; overly casual speech.

> 言語は私に合わせなさい
>
> Match my language. (2026-09-27, said to a coding agent)

> タメ口やめなさい
>
> Stop talking so casually. (2026-09-27, said to a coding agent)

## References he likes

### Learn from products with good UX, not from the same category

**(strong)** Take references from products known for good UX whose pattern fits the page, and
from real product screens rather than landing pages. Borrow how a reference decides, not its
look.

Rejected: copying weak same-category apps; landing-page and template galleries as screen
references; transplanting another project's look unchanged.

> 似たアプリがわるいuiばっかなのに真似してどうする。やるとするならuxがいいアプリから学びなさい
>
> Similar apps all have bad UI, so why copy them? If you're going to do it, learn from apps with
> good UX. (2026-10-29)

### Copilot Money for personal finance

**(strong)** The reference for a personal finance app's UX and UI.

> We do not have to re-use the UI. reference things like copilot money. (2026-05-04)

> copilot moneyを参考にしなさい。
>
> Use Copilot Money as the reference. (2026-11-23)

### Beautiful UI as the parts source

**(strong)** [Beautiful UI](https://beautifului.dev) is a component library for AI and chat
interfaces, with motion built in. He prefers it because its parts show live state and data
rather than static stock cards, which fits the product UI he likes. Use it for components and
motion, especially on AI and chat surfaces, list it first when choosing parts, and look for
libraries like it. Popularity rankings never override it.

Rejected: comparisons ranked by downloads that leave it out.

> これがいい。積極的に使って欲しいし他にもこういうのないか探して欲しい。ui関連のこと
>
> This one is good. I want you to use it actively, and look for other things like it.
> UI-related things. (2026-11-05)

> なんでいつもこれが好きって言ったUIを使わないの？Beautifuluiを使いたいって言ってるのにDemoに入ってなかったし。
>
> Why do you never use the UI I said I liked? I've said I want to use Beautiful UI, yet it wasn't
> in the demo. (2026-11-05)

### Chartosaur for data storytelling

**(strong)** [Chartosaur](https://www.chartosaur.com/tree) sets the bar for every chart and
insight line: one message stated in words, a chart type that fits the data, context to judge
the number, few variables per chart, alternative explanations considered, and care over labels,
order, emphasis and colour. Study its worked examples as well as its principles, and look for
more free material like it.

Agrees with: [Data visualization](data-visualization.md) as a whole.

> こう言ったことを意識してほしいという意味で送った
>
> I sent it because I want you to keep this kind of thing in mind. (2026-11-15)

> いい例もたくさんあるので参考にして。他にも無料でこういう資料がないか探して。ドンピシャだったので
>
> There are lots of good examples, so use it as a reference. And look for other free resources
> like this. It was spot on. (2026-11-15)

### Apple Fitness rings and Oura's sleep chart

**(stated)** Admired patterns from health apps: Apple Fitness's activity rings, including a week
of rings, and Oura's detailed sleep chart in full detail. The quotes are under
[Draw scores, progress and composition as rings, the same way everywhere](#draw-scores-progress-and-composition-as-rings-the-same-way-everywhere)
and [One glance first, every detail on drill-down](#one-glance-first-every-detail-on-drill-down).

### Principle sources to design and review against

**(stated)** [Laws of UX](https://lawsofux.com), [Nielsen's 10 usability heuristics](https://www.nngroup.com/articles/ten-usability-heuristics/),
the [GOV.UK Design System](https://design-system.service.gov.uk), [Inclusive Components](https://inclusive-components.design)
and [Apple's Human Interface Guidelines](https://developer.apple.com/design/human-interface-guidelines).
A built prototype is reviewed heuristic by heuristic, with the exact offending element
highlighted. For colour, [Material Design's colour system](https://m2.material.io/design/color/the-color-system.html#color-usage-and-palettes).

Agrees with: [Review against stated goals, with independent evaluators and severity ratings](interface-design.md#review-against-stated-goals-with-independent-evaluators-and-severity-ratings).

> Nielsen's 10 usability heuristics: https://www.nngroup.com/articles/ten-usability-heuristics/ (Part of a pasted list, 2026-11-23)

> For every broken heuristic, make it highlight the exact element on the screen that causes the problem. (2026-11-23)

> https://m2.material.io/design/color/the-color-system.html#color-usage-and-palettes
>
> (Shared as the reference for colour usage and palettes, 2026-11-13)

### Design-craft collections

**(inferred)** He shared skill collections on UI craft as references for quality:
[jakubkrehel/skills](https://github.com/jakubkrehel/skills) and
[Leonxlnx/taste-skill](https://github.com/Leonxlnx/taste-skill). He also saves UI finds as X
bookmarks.

> https://github.com/jakubkrehel/skills (2026-11-23)

> https://github.com/Leonxlnx/taste-skill (2026-11-23)

### Products he liked and disliked

**(inferred)** Liked: data-rich, state-rich product UI with meaningful colour (Beautiful UI,
Copilot Money, Linear, Apple Fitness rings, Oura's sleep chart; Netflix and Airbnb for UX
patterns). Disliked: minimal marketing heroes and playful, illustrated product sites (Vercel,
Zed, Notion Calendar, PostHog, Supabase, Cursor, Mercury); generic clean SaaS pages are "meh".
Read from what he picked in comparisons.

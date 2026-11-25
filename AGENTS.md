# design-reference

このマシンの運用ルールの正本は `~/AGENTS.md`(= `~/server/AGENTS.md`)。作業前に必ず読むこと。
タスクは Linear(`lin` CLI、Repo ラベルは design-reference)。このリポは `~/dev/design-reference`(開発コピー)で、launchd からは指さない。

このリポ固有: どのプロジェクトにも依存しない、デザインとデータ可視化の知識バンク。公開できる水準で書く(英語、一次資料の出典つき)。
特定のプロジェクトの名前・画面・データと、個人の生活の情報は書かない。Marty の好みは元の発言を根拠に `docs/preferences.md` に書き、Marty の名前はそこにだけ出す。
Claude Code の plugin として配る(`.claude-plugin/`、スキルは `skills/design-reference/`)。dotclaude の `settings.shared.json` が各マシンで有効にし、Codex などへも同じスキルが渡る。

# CLAUDE.md — AI Character IP Studio

人間向けの概要は `README.md`。ここには Claude Code の作業ルールだけを書く。

## 役割の境界

- 本リポジトリはAIキャラクターIPの企画・制作・運用の拠点
- 状態管理(`.project-os/`)、Agent/Skill/Workflow、Schema、Registry を本リポジトリで再実装しない。必要なら Project OS(`C:\Users\hiro1\AI-OS\system\claude-project-os`)を使う
- 同じ情報の正本を複数箇所に持たない

## Claire プロジェクトの扱い

- `C:\Users\hiro1\AI-OS\projects\ai-girlfriend-01` は制作中の別プロジェクト(`ai-os-projects` リポジトリで追跡)
- 読み取り専用で参照する。ファイル・設定の作成/変更/移動/コピー、および `ai-os-projects` での Git 操作はしない
- Claire 由来の内容を本リポジトリに取り込む場合は、事前にユーザーの承認を得る

## Git

- コミット・プッシュはユーザーの指示があるときだけ行う
- `.claude/settings.local.json` は追跡しない(`.gitignore` 済み)

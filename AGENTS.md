<!-- OPENSPEC:START -->
# OpenSpec Instructions

These instructions are for AI assistants working in this project.

Always open `@/openspec/AGENTS.md` when the request:
- Mentions planning or proposals (words like proposal, spec, change, plan)
- Introduces new capabilities, breaking changes, architecture shifts, or big performance/security work
- Sounds ambiguous and you need the authoritative spec before coding

Use `@/openspec/AGENTS.md` to learn:
- How to create and apply change proposals
- Spec format and conventions
- Project structure and guidelines

Keep this managed block so 'openspec update' can refresh the instructions.

<!-- OPENSPEC:END -->

# AGENTS

目的
- このリポジトリは複数の子リポジトリを束ねる親ワークスペース。
- API と WEB フロントなど複数リポジトリを並列に配置して一括管理できる構成。
- `git/info/exclude` により子リポジトリを Git 管理から外しつつ、AI が参照できる状態を維持する。
- 一部の子リポジトリはシンボリックリンクで管理していることがある
- ルートにはビルド/テストの実行基盤は検出されていない。
- 子リポジトリで作業するエージェントの行動指針をここで管理する。
- AI-DLC や spec 駆動開発を進めやすくするため、ルート直下に AI エージェント用のファイルを配置する。

リポジトリ構成
- ルート配下: 複数の子リポジトリと共通メタ情報。
- 子リポジトリの概要は各 README.md または子側の AGENTS.md に記載する。

対話と言語ルール
- AI との対話はすべて日本語で行う。
- ドキュメント、コメント、メッセージも原則日本語で記述する。
- 例外が必要な場合は、ユーザーに事前確認する。

ドキュメント
- 振る舞い変更時は README.md や関連ドキュメントも更新する。
- ドキュメントは簡潔かつ正確に保つ。

依存関係
- 不要な依存追加は避ける。
- 追加が必要な場合は理由を明記する。

Git 運用
- 秘密情報や `.env` をコミットしない。
- 変更はタスクに関連する範囲に限定する。
- コミットやリリース手順は事前に確認する。

子リポジトリの扱い
- 各子フォルダは独立したリポジトリとして扱う。
- どのリポジトリを対象にするか事前確認する。
- ツール類が存在しない場合はユーザーに確認する。

迷ったとき
- 正しいコマンドやスタイルはユーザーに確認する。
- 推測で大きな変更を行わず、保守的に進める。
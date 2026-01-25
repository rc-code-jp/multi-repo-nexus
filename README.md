# 複数のリポジトリを持つプロジェクトの親となるリポジトリ

すでにマルチリポジトリで運用されているルガ、AIのルールなどを親ディレクトリで一括管理したい要望に応える。
環境構築や横断したタスクをこなせる中心的な構成を提供する。
これはそのためのボイラーテンプレート。

## 概要

git_info_excludeを使用して.gitignoreと同様の機能を提供する。
これによりAIが下層のリポジトリを読み取ることができ、かつGit管理から除外することができる。

```
Selected configuration:
  - Antigravity
  - Claude Code
  - OpenCode
```

## 設定方法

リポジトリの初期化は、Agent Skills の **`init-repo`** スキルを使用してください。

詳細な手順とコマンドは [`.claude/skills/init-repo/SKILL.md`](./.claude/skills/init-repo/SKILL.md) を参照してください。

---
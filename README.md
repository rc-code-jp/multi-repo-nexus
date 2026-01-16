# 複数のリポジトリを持つプロジェクトの親となるリポジトリ

すでにマルチリポジトリで運用されているルガ、AIのルールなどを親ディレクトリで一括管理したい要望に応える。
環境構築や横断したタスクをこなせる中心的な構成を提供する。
これはそのためのボイラーテンプレート。

## 概要

git_info_excludeを使用して.gitignoreと同様の機能を提供する。
これによりAIが下層のリポジトリを読み取ることができ、かつGit管理から除外することができる。


## 設定方法

Git管理から中のプロジェクトを除外する。
もし`.git/info/exclude`が存在しない場合は手動でファイルを作成する。
以下のコマンドを実行してファイル内容をコピーする。

```
# サンプルプロジェクト（本体はgit cloneの想定）
mkdir -p project-a && cat > project-a/README.md <<'EOF'
# Project A
 これはサンプルプロジェクトです。
EOF

mkdir -p project-b && cat > project-b/README.md <<'EOF'
# Project B
 これはサンプルプロジェクトです。
EOF
```

```zsh
grep -Fxv -f .git/info/exclude .git_info_exclude >> .git/info/exclude
```

```zsh
cp .env.example .env
```

⚠️ IDEやVSCodeを開いていた場合は、開き直さないとGit監視が更新されない可能性あり。

---
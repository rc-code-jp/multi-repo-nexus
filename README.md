# 複数のリポジトリを持つプロジェクトの親となるリポジトリ

monorepoにはできないが、AIのルールなどを親ディレクトリで管理したい要望に応える。

## 設定方法

Git管理から中のプロジェクトを除外する。
もし`.git/info/exclude`が存在する場合は手動でファイルを作成する。
以下のコマンドを実行してファイル内容をコピーする。

```zsh
grep -Fxv -f .git/info/exclude .git_info_exclude >> .git/info/exclude
```

## ...
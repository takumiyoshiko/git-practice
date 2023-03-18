# git-practice

## Gitでよく使うコマンド集

- git remote: リモートリポジトリの一覧を出力
- git branch: ローカルブランチの一覧を出力
- git checkout {ブランチ名}: 対象ブランチに切り替え
- git checkout {ファイルパス}: 対象ファイルの変更を取り消し
- git switch {ブランチ名}: 対象ブランチに切り替え
- git restore {ファイルパス}: 対象ファイルの変更を取り消す
- git diff: ファイルの差分を出力する
- git status: 変更したファイルの一覧を出力する
- git add {ファイルパス}: 対象ファイルをインデックスに追加する
- git reset HEAD {ファイルパス}: ステージングにある対象ファイルをワークツリーに戻す
- git commit: インデックスにある全ファイルをコミットする
- git revert HEAD: 直前のコミットを元に戻すコミットを作成する
- git push origin {ローカルブランチ名}: 対象ローカルブランチをoriginにpushする
- git fetch origin: originから最新の履歴を取得
- git rebase origin/{ブランチ名}: originにある対象ブランチを、チェックアウト中のブランチへリベースする
- git merge origin/{ブランチ名}: originにある対象ブランチをチェックアウト中のブランチへマージする
- git cherry-pick {コミットID}: 対象コミットをチェリーピックする
- git stash list: スタッシュの一覧を出力する
- git blame {ファイルパス}: 対象ファイル全体の各行ごとに、最後に編集したリビジョンと作者を表示する
- git log: コミットログを表示


## 困った時に使えそうな対処法

### コミットせずに変更を退避する
- sample.txtを編集 ← 変更を退避したい
- `git stash -u` ← 変更を退避
- `git stash list` ← 退避した変更を確認
- 別作業
- `git stash apply stash@{0}` ← 退避した変更を元に戻す (stash@{0}には戻したい変更分に適宜変更)
- `git stash drop stash@{0}` ← 退避した変更を削除 ( `git stash pop stash@{0}`で退避した作業を元に戻すと同時に削除できる)

### PRのマージを取り消す
`git revert`

### force-pushを復活させる
`git reflog`

### push後にrebaseしてしまった時の対処法
``

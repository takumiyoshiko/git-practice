# Gitでよく使うコマンド集

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
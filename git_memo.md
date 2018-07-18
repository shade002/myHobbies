## 基本的なコマンド

* git init
* git config --global user.email ~
* git config --global user.name ~
* git remote add origin ~
* git status
* git log
* git add ~
* git commit -m "~"
* git push origin master
* git pull origin master
* git clone ~(git hub上のアドレスをコピー)
* git checkout -b ~ …ブランチ作成
* 

## その他Git hubに関わる知識

* .gitignoreファイル
    …作成しておくとOSの設定ファイルなどの余計なファイルをクローンなどの際に除外することができる。(`# ファイル .DS_Store     # ディレクトリ /tmp     # ワイルドカード *.log`)→作成するときはgit hubから。
* issue/Milestone
    …中期的目標、問題点の共有。マークダウン使用可能。→様々なファイル送信可能。
* Pull Request
    …forkした自身のリモートリポジトリの変更点を加えたブランチを元のブランチに統合してもらえるようにリクエストすること。
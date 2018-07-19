## 基本的なコマンド(コマンド準拠)

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

### VSCodeのGit連携設定
1. usersetting(Ctrl + ,) → *terminal.integrated.shellArgs.windows*の項目へ
2. []内に以下の内容を書き込む
    >"/k",
    >"C:\\Program Files\\Git\\bin\\bash.exe"
    
### Git Hub操作系コマンド(エイリアス後)
* git hub browse
* 

## その他Git hubに関わる知識

* .gitignoreファイル
    …作成しておくとOSの設定ファイルなどの余計なファイルをクローンなどの際に除外することができる。(`# ファイル .DS_Store     # ディレクトリ /tmp     # ワイルドカード *.log`)→作成するときはgit hubから。
* issue/Milestone
    …中期的目標、問題点の共有。マークダウン使用可能。→様々なファイル送信可能。
* Pull Request
    …forkした自身のリモートリポジトリの変更点を加えたブランチを元のブランチに統合してもらえるようにリクエストすること。

---
### ブランチモデル

* Git Flow
    …次の五つのブランチのみを作成し、それを軸にpull requestによって機能の修正、改変を行っていく方法
    * develop…開発のメインになるブランチ。修正や機能の追加があった際にはfeatureブランチに派生する、リリース前にはreleaseブランチに派生する。　→feature　→release
    * feature…開発作業において実質メインになるブランチ。開発箇所を絞ってコードを改変していき、一つ終わったらdevelopブランチにマージする。
    * release…リリース前に稼動するブランチ。リリース前の細かい修正やパッケージの整備などを行う。完成した際はmasterブランチとdevelopブランチ双方にマージする。　→master　→develop
    * master…リリース時に稼動するブランチ。バージョンのタグ付けなどを行う。
    * hotfix…リリース後に緊急性の高いバグなどが発生した際に稼動するブランチ。masterブランチからforkし、修正後にはmasterブランチとdevelopブランチ双方にマージする。　→master　→develop

* GitHub Flow
    …大きく分けて二種類のブランチを軸に開発を行う方法。
    * master…このブランチにマージされるとその時点ですぐにリリースが行われるブランチ。それ以外の機能は持たない。
    * topic…メインで開発が行われるブランチ。どの機能の開発を行っているのかわかる名前をブランチにつけて、それぞれの機能毎にレビュー、リリースのpull requestを送る。
---

* コミットの粒度/コミットメッセージ
    …１機能を目安にコミットを行うよう心がけること。/簡潔かつ明瞭に残す。
* 

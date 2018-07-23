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
* git clone ~(git hub上のアドレスを貼り付け)
* git checkout -b ~ …ブランチ作成

* git checkoutについて …このコマンドには二つの機能がある。
    1. パスを指定した場合 …指定されたパスのファイルやブランチ、コミットをローカルリポジトリに反映させる。
    2. ブランチやコミットハッシュ値を指定した場合 …Gitが参照するファイルを表すHEADを指定されたファイルに付け替える。
 
### VSCodeのGit連携設定
1. usersetting(Ctrl + ,) → *terminal.integrated.shellArgs.windows*の項目へ
2. []内に以下の内容を書き込む
    >`"/k",`
    >
    >`"C:\\Program Files\\Git\\bin\\bash.exe"`
    
### Git Hub操作系コマンド
* git hub browse
* 

## その他Git hubに関わる知識

* .gitignoreファイル
    …作成しておくとOSの設定ファイルなどの余計なファイルをクローンなどの際に除外することができる。初期は以下の内容を書き込む。(※作成するときはgit hubからが楽)
    >`# ファイル .DS_Store`
    > 
    >`# ディレクトリ /tmp`
    > 
    >`# ワイルドカード *.log`
* issue/Milestone
    …中期的目標、問題点の共有。マークダウン使用可能。→様々なファイル送信可能。
* Pull Request
    …forkした自身のリモートリポジトリの変更点を加えたブランチを元のブランチに統合してもらえるようにリクエストすること。
    * コンフリクトが起こった場合 …該当ファイルのコンフリクトが起こっている箇所を見ると
    >`<<<<<<< HEAD`
    >
    >`=======`
    >
    >`>>>>>>> コミットID`
    というコードが挿入されているので、どちらかのコード変更を消して保存→addなしで再コミットする。
    * オートマージできない場合 …該当ブランチをローカルmasterブランチとマージする → 後は上記のコンフリクト修正と手順同じ。

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

## その他

### コミュニケーション関連

* コミットメッセージ書き方 → [git fetchの理解からgit mergeとpullの役割 - Qiita](https://qiita.com/itosho/items/9565c6ad2ffc24c09364)

* マークダウン記法について → [Markdown記法 チートシート - Qiita](https://qiita.com/Qiita/items/c686397e4a0f4f11683d)

* LGTMについて → [LGTM! チャットやGitHubでよく見る英略語ってこんな意味](https://blog.sixapart.jp/2016-10/lgtm-github.html)

### ツール関連

* SHIFT + / …Git hubショートカット
* Gist …[Gist](https://koskywalker.com/github-gist-use/#gist-3)
* ブックマークレット …要検索
* ターミナル関連ツール
    * 「gibo」 …gitignoreファイルの自動生成。
    * 「tig」 …ターミナルでのGUI教科ツール。
    * 「hub」 …Git hub上で行う操作をコマンドからでも行えるようにする。

* 「?w=1」 …diffの表示画面で左のパラメータをURLに渡すと、変更したコードのみが表示されるようになる。

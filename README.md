# TISCON Market

変更内容
hogehoge

##シチュエーション



とある日、新規のお客様から依頼が入りました。



>自社の通販サイトを自分たちで作ってみたんですが

>どうにもイケていない気がするんです。。

>サービスとして立ち上げるにあたって、いろいろ不安もあるし。

>既存のサイトに対して改善提案をしていただけませんか。



##依頼内容



既存のECサイトの問題点をシステム開発の**プロ視点**で見つけ、

お客様に改善提案を行ってください。



お客様から言われたことは以下の通り。


　こんなところが問題ないか不安

  - セキュリティ

  >顧客情報の漏洩とかよく耳にするのでセキュリティは万全にしてほしいな

  - システムの性能

  >ボタンを押してからしばらく画面が動かないとイライラしちゃうんですよね

  - ユーザビリティ

  >誰にでも使いやすくてオシャレなサイトにしたいんです







![](https://circleci.com/gh/tiscon/tiscon1-pre.svg?style=shield&circle-token=8f99c0e6c923ca570acda8c3640446fdacad2a47)



## 環境構築

本プロジェクト実行に必要な準備は以下の通りです。

 - Maven3のインストール、設定

 - JDK8のインストール、設定

 - IntelliJ IDEAのインストール、設定

 - Herokuのアカウント作成、Toolbeltのインストール

 - Githubのアカウント作成

 - 動作確認

下記リンクtiscon1-doc内のREADMEを参考に、環境構築をしてください。
[【tiscon1-doc】](https://github.com/tiscon/tiscon1-doc)

ローカル上での動作確認まで終わったら、オンライン上での動作確認をします。  
Herokuにログインした状態で、下のDeployボタンを押下してください。  

[![Deploy](https://www.herokucdn.com/deploy/button.svg)](https://heroku.com/deploy)  

HerokuのDeployページが開くので、画面のDeploy for Freeボタンを押下してください。  
その際、App Name (optional)及びRuntime Selectionの項目を入力・変更する必要はありません。  
(TISCONアプリケーションがHeroku上でビルド・動作します。)  

Deploy to Herokuにチェックがついたら右下のViewボタンを押下してください。  
TISCON Marketの画面が表示されたら想定通りの挙動です。

## 提供機能(2016/2/3現在)
本アプリケーションで提供されているのは以下の機能です。  
- ログイン機能
- ログアウト機能
- カテゴリ別Top10表示
- 詳細画面表示
<br>

※上記以外の機能が本番までに追加される場合があります。  

### 更新を検知する方法
機能の追加、修正（プログラムの修正）が行われる場合があります。  
GithubのWatch機能を使用すれば、プログラムの修正があった場合、登録したメールアドレスに通知メールが来るようになります。  
各リポジトリページの右上にある「Watch」ボタンを押下し、プルダウンからWatchingを選択してください。  
そうするとWatch機能が有効になります。  

### 更新を自身のPCに反映させたい
検知した更新を、自身のPCに反映させることができます。  
下記リンク先の更新手引きに従い作業を行ってください。  
[【更新手引き】](https://github.com/tiscon/tiscon1-doc/blob/master/UpdateGuide.md)

## 参考
### 本プロジェクトの構成



```

tiscon1

└ src

 └ main

    ├ java

    │└ tiscon1

    │  ├ config       アプリケーションの設定

    │  ├ controller   コントローラ

    │  ├ exception    エクセプション

    │  ├ form         HTTPリクエストパラメータを受けるためのクラス群

    │  ├ interceptor  コントローラーの共通処理(認証認可及び画面共通項目設定用インターセプタ)

    │  ├ model        データモデルを表すクラス群

    │  ├ repository   モデルの永続化のためのインタフェース

    │  └ App.java     アプリケーションエントリーポイント

    └ resources

      ├ public   画像, Javascript, Stylesheetなどstaticなファイル

      └ template Freemarkerテンプレート

```

---

### 技術仕様
#### Spring Boot

アプリケーションは、Spring Bootを使って構築されています。Spring Bootに関しては以下をお読みください。



- [Spring Bootリファレンス(本家)](http://docs.spring.io/spring-boot/docs/1.3.1.RELEASE/reference/htmlsingle/)

- [Spring Bootハンズオン](http://jsug-spring-boot-handson.readthedocs.org/en/latest/)





#### iTunes API

アプリケーションではiTunes APIを使用しています。

必要な検索情報をパラメータに設定してリクエストを送ることで、App Storeで販売されている商品データの検索結果が返却されます。



iTunes APIに関しては以下をお読みください。

- [Search APIリファレンス](https://www.apple.com/itunes/affiliates/resources/documentation/itunes-store-web-service-search-api.html)
  
  
  
本アプリケーションでは以下を取得するためにAPIを使用しています。

- Movie、Musicのサブジャンル

- Movie、MusicのTop10

- 商品情報

---

### リンク
事前学習にご利用ください。  
[【システムエンジニア Advent Calendar 2015】](http://qiita.com/advent-calendar/2015/se)
**メモ**  
### あれこれ  

    * [Jekyll](http://jekyllrb-ja.github.io/)
    * https://fatherfurther.github.io/github-pages-with-jekyll/
    * GitHub Packages
    * To select another theme, see “[Adding a Jekyll theme to your GitHub Pages site with the Jekyll Theme Chooser](https://help.github.com/en/github/working-with-github-pages/adding-a-theme-to-your-github-pages-site-with-the-theme-chooser)" in the GitHub Help.  
    * [GitHub Actions: Continuous Delivery with Azure](https://lab.github.com/githubtraining/github-actions:-continuous-delivery-with-azure)  
    * [VScode」でGithubにPull Requestする方法を解説！](https://appli-world.jp/posts/9846)  
    * [Node.jsでの開発効率をあげるための便利なmodule、nodemon](https://github.com/osamu38/node-express-curriculum/wiki/Node.jsとExpressの基本#nodejsでの開発効率をあげるための便利なmodulenodemon)  
    * [VSCode に必ず入れておきたい拡張機能](https://qiita.com/ucan-lab/items/e85931bf8276da43cc97?utm_source=Qiitaニュース&utm_campaign=87b4fad0d8-Qiita_newsletter_409_04_22_2020&utm_medium=email&utm_term=0_e44feaa081-87b4fad0d8-36034433)

### カテゴリ別  
#### JavaScript  
  * [JavaScriptの便利すぎるショートハンド](https://www.webprofessional.jp/shorthand-javascript-techniques/)  
  * [無名関数とは](https://www.sejuku.net/blog/60321)  
  * [アロー関数とは](https://qiita.com/may88seiji/items/4a49c7c78b55d75d693b)  
  * [コールバック関数とは](https://sbfl.net/blog/2019/02/08/javascript-callback-func/)  
  * [Promise](https://sbfl.net/blog/2016/07/13/simplifying-async-code-with-promise-and-async-await/)  

#### Markdown  
            <details>
                <summary>Title</summary>

                Content here

            </details>  

#### Node.js  
  * [インスタンスが起動したら自動的にNode.jsアプリが起動するようにする](https://qiita.com/kuryus/items/fbdc373f23d3236ebb04)  
  pm2の使い方  
#### npm  
  * [npm installしてあるパッケージの現状と最新のバージョン確認とアップデート方法](https://olein-design.com/blog/update-npm-package-with-npm-check-updates)  

#### git  
  * git branch -a                     ： ブランチ一覧の表示  
  * git branch -vv                    ： リモート追跡ブランチとの紐づけ確認
  * git checkout -q [branch]          ： ブランチのチェックアウト  
  * git branch --delete [branch]      ： ローカルブランチの削除  
  * git push --delete origin [branch] ： リモートブランチの削除  
  * git fetch --prune                 ： 削除されたブランチの同期？
  * [本番環境でpullしたらコンフリクト？解決法３パターン！](https://qiita.com/15grmr/items/433ee3b47828aaad32a8)  
    * 強制PULL  
      1. リモートの最新を取ってきておいて・・
        $ git fetch origin master
      1. masterを、リモート追跡のmasterに強制的に合わせる
        $ git reset --hard origin/master

#### VSCode  
  * 設定の同期-[Settings Sync](https://marketplace.visualstudio.com/items?itemName=Shan.code-settings-sync)  
  

#### Express  
  * 開始手順  
    $ npm i -g express-generator (グローバルでexpress-generatorを導入)  
    $ express --view=ejs (expressの雛形アプリを作成)  
    $ npm i (必要なnode_modulesをinstall)  
    $ npm start (アプリを立ち上げ)  

### APW関連
#### Ubuntu  
  * 事前作業  
    * $ sudo apt-get update  
    インストール可能なパッケージの「一覧」を更新する。  
    * $ sudo apt-get upgrade  
    インストール済みのパッケージ更新をおこない、新しいバージョンにアップグレードする。
  * [node、npmのインストール](https://qiita.com/seibe/items/36cef7df85fe2cefa3ea)
  * [Mysqlのインストール](https://qiita.com/houtarou/items/a44ce783d09201fc28f5)  

#### MySQL  
  * [サービスの起動・停止](https://www.t3a.jp/blog/infrastructure/mysql-start-stop/#outline__1)  
    * service mysql start  
    * service mysql stop  
    * service mysql restart  
    * service mysql status  
  * [MySQLコマンドまとめ](https://qiita.com/merrill/items/967884c02e10bd8f32f5)  
    * ログイン  
      $ mysql -uroot # root でログイン  
    * 使用するデータベースを選択  
      $ use db_name  
    * データベース、テーブル一覧を表示  
      $ show databases;  
      $ show tables;  
    * データベース削除  
      $ drop database db_name;  
    * [MySQL 特定のテーブルのバックアップとリカバリー](https://www.kakiro-web.com/memo/mysql-database-backup-recovery-table.html)  
      バックアップ・リカバリー及び他サーバへのコピー  
  * [MySQL で特定の IP アドレスからのアクセスを許可する](https://qiita.com/u-dai/items/b360a337b5001778699e)  
  * [外部接続可能なユーザの作成](https://qiita.com/yoshiokaCB/items/df4ae185be7cbc4f03ac)

#### フレームワーク  
  * JavaScript実行環境  
    * Node.js  
    * Deno.js  
  * JavaScriptフレームワーク（サーバサイド）  
    * Express.js  
    * Next.js  
    * Gatsby.js  
  * JavaScriptフレームワーク（フロントサイド）  
    * React  
    ※ [React学習用レポジトリ](https://github.com/tsubasa/react-redux-study)  
    * Vue.js  
    * AngularJS  
    関連ワード：仮想DOM、JSX、[babel](https://qiita.com/tomokin966/items/7731a6337670f5de2342#%E5%85%A5%E5%8A%9B%E8%A3%9C%E5%AE%8C%E3%81%AE%E5%80%99%E8%A3%9C%E3%82%92%E5%87%BA%E3%81%99%E3%81%9F%E3%82%81%E3%81%AEctrl--space%E3%81%99%E3%82%89%E3%82%81%E3%82%93%E3%81%A9%E3%81%84)    
  * JavaScriptライブラリ  
    * Redux
    * unstated
  * テンプレートエンジン  
    * Handlebars.js  
    * EJS  
    * edge  
  * CSSフレームワーク  
    ※参考：[CSSフレームワーク30選！デザイン含めて一括総まとめ](https://eng-entrance.com/css-framework)
    * Bootstrap  
  * その他  
    * React Native

[sails.js](https://sailsjs.com/)を勉強してみた。[参考チュートリアル](https://www.casleyconsulting.co.jp/blog/engineer/225/)を基に、実際に簡単なWebアプリを作成。  
 
1. バージョン情報  
   ```  
    node.js   v12.16.2  
    npm       6.14.4  
    sails.js  1.2.4 
   ```
1. チュートリアルではまった箇所の解決方法  

   1. http://localhost:1337/Casm/index への初回アクセス  
   →404エラー  
      * 解決策  
       `config/blueprints.js`を以下のように修正（[参考サイト](https://github.com/bradtraversy/articlebase/issues/1)）  
        ```  
        actions : true  
        ```  
   1. MySQLにユーザ追加＆権限設定  
   　以下のSQLで実行。
      * create user username@localhost identified by 'username';  
      * grant CREATE,SELECT,INSERT,UPDATE,DELETE,DROP on mydb.* to username@localhost;  
   1. データベース接続設定  
   →「続けてDB接続の定義をconfig/connection.jsに記述します。」とあるが、この方法だとうまくいかない。  
      * 解決策  
      datastores.jsでデフォルトDBを指定するように変更（[参考サイト](https://sailsjs.com/documentation/reference/configuration/sails-config-datastores)）  

   1. Controllerの修正(データの操作をModelオブジェクトのメソッドを利用）  
   →エラー  
     →エラーログ出力するようにスクリプトを書き換え、原因特定。  
       ```  
       Casm.find().exec(function (err, records) {  
         if (err) {  
           return console.log(err);  
         } else {  
       ```  
      →エラー内容：`Error [AdapterError]: Unexpected error from database adapter: ER_BAD_FIELD_ERROR: Unknown column 'createdAt' in 'field list'`  
       * 解決策  
       [このサイト](https://sailsjs.com/documentation/upgrading/to-v-1-0) を参考に`config/models.js`から以下2行を削除  
       ```  
         attributes: {  
       //    createdAt: { type: 'number', autoCreatedAt: true, },  
       //    updatedAt: { type: 'number', autoUpdatedAt: true, },  
       ```  
   1.  外部Javascriptの作成  
   →ドラッグ&ドロップが動作しない。開発者ツールで確認すると`casm.js`で`$ is not defined`エラーがでている。jQueryの読み込みに失敗している模様。  
       * 解決策  
       `index.js`に以下の通り記載  
       ```  
       `<script src="http://ajax.aspnetcdn.com/ajax/jQuery/jquery-2.2.4.min.js"></script>`  
       `<script src="https://ajax.aspnetcdn.com/ajax/jquery.ui/1.12.1/jquery-ui.js"></script>`  
       ```
以上      





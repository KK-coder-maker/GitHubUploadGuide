# GitHubへのアップロード方法
## 事前準備
1. GitHubのアカウントを作成してください。
1. Gitをインストールしてください。
1. GitHubにアップロードするフォルダを作成してください。

## 1. GitHubのリポジトリを作成する
1. `Create a new repository`をクリック
2. `Repositry name`にレポジトリの名前を入力
3. `Pubulic`か`Private`を選択する
   - `Private`の場合、有料になるかも？
4. `https://github.com/Usernme/RepositoryName.git`をコピーしておく。

## 2. GitHubのトークンを生成
1. 画面右上の自分のアイコンをクリック
2. `Settings`をクリック
3. 左のメニューの一番下`Developer settings`をクリック
4. `OAuth Apps`の`Tokens(classic)`をクリック
5. `Generate new Token`の`Generate new Token(classic)`をクリック
6. `Note`に○○を書く
6. `repo`にチェックを入れる
7. `Generate token`をクリック
8. 緑色のチェックマークの右に文字列がでる。これがトークンである。
9. トークンをメモ帳などに保存しておく。

## 3. ローカルのフォルダをGitの管理対象とする
1. GitBashを開く
2. GitHubにアップロードするフォルダをカレントディレクトリにする
  - 移動：cdコマンド, フォルダ内表示：lsコマンド
3. `$ git init`を実行
  - Gitでの管理がされるようになる
```
User@LAPTOP ~/.../GitHubUploadGuide
$ git init
Initialized empty Git repository in ~/.../GitHubUploadGuide/.git/
```

## 4. その他コマンドを実行する


## 5. 日々使うコマンドの流れ
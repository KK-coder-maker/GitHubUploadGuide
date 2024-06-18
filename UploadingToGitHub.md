# GitHubへのアップロード方法
## 事前準備
1. GitHubのアカウントを作成してください。
1. Gitをインストールしてください。
1. GitHubにアップロードするフォルダを作成してください。

## 1. GitHubのリポジトリを作成する
1. `Create a new repository`をクリック
2. `Repositry name`にレポジトリの名前を入力
3. `Pubulic`か`Private`を選択する
   - `Private`の場合、有料かも？
4. `https://github.com/Usernme/RepositoryName.git`をコピーしておく。

## 2. GitHubのトークンを生成
1. 画面右上の自分のアイコンをクリック
2. `Settings`をクリック
3. 左のメニューの一番下`Developer settings`をクリック
4. `OAuth Apps`の`Tokens(classic)`をクリック
5. `Generate new Token`の`Generate new Token(classic)`をクリック
6. `Note`はトークンの名前であり、入力する。
6. 必要なスコープ（例えば「repo」）を選択します。
7. `Generate token`をクリック
8. 緑色のチェックマークの右に文字列がでる。これがトークンである。
9. トークンをメモ帳などに保存しておく。

## 3. ローカルのフォルダをGitの管理対象とする
1. GitBashを開く
2. GitHubにアップロードするフォルダに移動する
   - 移動：cdコマンド, フォルダ内表示：lsコマンド
   ```bash
   $ cd path/to/your/folder
   $ ls
   ```
3. `$ git init`を実行
   - Gitでの管理が開始される

## 4. ファイルのステージングとコミット
1. 作成したファイルをステージング
   - `git add .`
2. コミット
   - `git commit -m "first commit"`
3. リモートリポジトリの設定
   - `$ git remote add origin https://YOUR_PERSONAL_ACCESS_TOKEN@github.com/USER_NAME/REPOSITRY_NAME.git`
     - YOUR_PERSONAL_ACCESS_TOKENには先ほど生成したトークンを使用
     - USERNAMEとREPOSITORYはあなたのGitHubのユーザー名とリポジトリ名

4. ブランチ名の変更(必要であれば)
   - `git branch -m master main`

5. ファイルのプッシュ(アップロードのこと)
   -  `$ git push -u origin main`

## 5. チートシート
### リポジトリのクローン
```bash
$ git clone REPOSITRY_URL
```
### ファイルのステージングとコミット
```bash
$ git add FILE_NAME
$ git add .

$ git commit -m "commit message"
```
### ブランチの作成
```bash
$ git branch BRANCH_NAME
```
### ブランチの切り替え
```bash
$ git checkout BRANCH_NAME
```
### 新しいブランチを作成して切り替える(一括コマンド)
```bash
$ git checkout -b NEW_BRANCH_NAME
```

### プッシュ(ローカルの変更をリモートに反映)
```bash
$ git push origin BRANCH_NAME
```
### プル(リモートの変更をローカルに反映)
```bash
$ git pull origin BRANCH_NAME
```

### マージとリベース
```bash
$ git merge BRANCH_NAME

$ git rebase BRANCH_NAME
```

### 履歴の表示
```bash
$ git log
```
### 変更内容の表示
```bash
$ git diff
```
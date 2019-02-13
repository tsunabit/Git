
### Gitの設定ファイルの種類と場所（system, global, local）
|種類|対象範囲|場所|備考|
|:--|:--|:--|:--|
|system|システム全体（全ユーザーの全リポジトリ）|/etc/gitconfig|-|
|global|該当ユーザーの全リポジトリ|~/.gitconfig|ホーム直下|
|local|該当リポジトリ|repository/.git/config|リポジトリの.git直下|

system, global, localの順に読み込まれて上書きされる。
なお、以下で説明するgit configコマンドでそれぞれの設定ファイルの確認・編集が可能なので、特にファイルの置き場所を気にする必要はない。

### 現在の設定を確認するコマンド
|コマンド|説明|
|:--|:--|
|git config --system --list|システム全体の設定を確認|
|git config --global --list|該当ユーザーの全リポジトリの設定を確認|

### 最低限の設定
|コマンド|説明|
|:--|:--|
|git config --global user.name "your user name"|ユーザー名設定|
|git config --global user.email "your e-mail@example.com"|メールアドレス設定|

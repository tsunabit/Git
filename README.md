# git_memo

# 基本
|コマンド|説明|
|:--|:--|
|git init|リポジトリの初期化|
|git status|リポジトリの状態を確認|
|git add|ステージ領域へファイルを追加|
|git commit|リポジトリの歴史を記録|
|git commit -m "コメント"|1行のコミットコメントを記述する|
|git push|リモートリポジトリへ送信|
|git push -u origin master|masterブランチへ送信|
|git push -u origin feature-D<br>または<br>git push --set-upstream origin feature-D|masterブランチ以外のブランチへ送信|
|git clone|リモートリポジトリを取得|
|git checkout -b feature-A origin/feature-A|リモートの特定ブランチをチェックアウトする。git cloneコマンド実行直後はローカルリポジトリだけでなく、リモートリポジトリも含んだ状態。<br>ただし、ローカルには存在しないためローカルにチェクアウトするには明示的にチェックアウトが必要。|
|git pull|最新のリモートリポジトリブランチを取得|
|git pull origin feature-A|最新のリモートリポジトリブランチを取得|

##### 補足：詳細なコミットメッセージを記述する
 - 1行目：コミットするへ脳内用の要約を1行で記述
 - 2行目：空行
 - 3行目：変更した理由や詳細を記述
##### 補足：コミットを中止する
git commitコマンド実行しエディタが起動した後にコミットを中止する場合、コミットメッセージを一切書かずにエディタを終了する

# ログ、差分
|コマンド|説明|
|:--|:--|
|git log|コミットログを確認。リポジトリにコミットされたログを確認できる|
|git commit --pretty=short|コミットメッセージの1行のみを表示する|
|git commit --amend|コミットコメントを修正|
|git log [ディレクトリ or ファイル名]|指定したディレクトリ、ファイルのみのログを表示する|
|git log -p|ファイルの差分を表示する。例えば「git log -p README.md」とするとREADME.mdファイルだけのコミットログとの差分を確認できる|
|git diff|変更差分を確認。ワーキングツリー、ステージ領域、最新コミット間の差分を確認するのに利用するコマンド|

# HEAD
作業しているブランチの最新のコミットを参照するポインタ

# ブランチ
|コマンド|説明|
|:--|:--|
|git branch|ブランチを一覧表示|
|git checkout -b|ブランチを作成し、切り替える|
|git checkout -b feature-A|feature-Aブランチに切り替えコミットする|
|git branch feature-A|ブランチ作成(切り替えは行わない)|
|git checkout [ブランチ名]|ブランチの切り替え|
|git checkout -|一つ前のブランチに切り替える|
|git log --graph|ブランチを視覚的に確認する|
|git branch -D [ブランチ名]|ブランチを削除する|

# マージ
|コマンド|説明|
|:--|:--|
|git merge|ブランチをマージ|
|git merge --no-ff feature-A|ブランチからマージしたことを明確に歴史に残すためにマージコミットを作成する。<br>マージしたい先のブランチへ切り替える。masterにマージする場合はmasterに切り替えて左記のコマンドを実施。(ここではfeature-Aブランチをmasterへマージする)|

##### 補足：マージはワーキングツリーに行われる
当たり前かもしれないけど、mergeは個人のローカルであるワーキングツリーに行われる。  
そのため、merge後のものはaddしてpushしないとリモートリポジトリに反映されない。  

# コミットを変更する操作
|コマンド|説明|
|:--|:--|
|git reset|歴史を戻る|
|git reset --hard HEAD^|前のコミットを取り消す。ワーキングツリー、インデックス、HEAD全てを1つ前に戻す|
|git rebase -i|歴史を押しつぶして改変|
|git remote add|リモートリポジトリを登録|
|git remote add|リモートリポジトリを登録|
git remote add origin git@github.com:[ユーザー名]/[リポジトリ名]|左記コマンドを実行すると、以後originという名前(識別子)で、git@github.com:[ユーザー名]/[リポジトリ名]を指すようになる|


# テンプレート
|コマンド|説明|
|:--|:--|
|||
|||
|||
|||
|||
|||
|||

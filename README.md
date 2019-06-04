# gitbootcamp-0605

## 01.git add
commitしたいファイルをステージングエリアに追加する。

## 02.git commit
ローカルリポジトリに最新のリビジョンを追加する。

## 03.git commit -a
git add と git commit を同時にやってくれる。
なお、-a は、commit の後に指定する必要がある。 git と commit の間に指定した場合、構文エラーとなる。

## 04.git commit --amend
マスターブランチを作る

## 05.git branch fix/42
fix/42という名前のブランチを作成する。

## 06.git checkout -b fix/24; git commit
fix/42のブランチを作成し、チェックアウト。
fix/42に対してコミットを行い、リビジョンを追加する。

## 07.git checkout -b fix/42
存在しないブランチ fix/42 を作成すると同時に、ブランチを fix/42 に移動する。リビジョンは作成されない。
つまり、 git branch fix/42; git checkout fix/42 と同じ。
ブランチを移動するとは、HEADの位置を移動するということ。

## 08.git reset --hard master
リセットして自分にHEADを持ってくる

## 09.git merge fix/42
現在の作業ブランチとfix/42をマージする
コンフリクトが起きた場合は解消してcommitをすればマージ完了する。
（再度mergeの必要はない)


## 10.git rebase -i A~E
A~Eまでを対象に編集操作を行う。  
上記コマンドを入力すると、エディタが立ち上がり、  
各リビジョンに対しての操作をテキスト形式で指定できる。（Discard、Squashなど）  
カードの例で言うと、Eを前に持ってきて、Bを削除、CとDをまとめる、といった操作を指定することとなる。  
※コマンドのみで完結しているわけでないためわかりづらい。

## 12.git checkout fix/42
ブランチをfix/42に移動する

## 13.git rebase master
分岐しているリビジョンを一直線にする
見やすさ考慮のため適切に行った方がよい

## 14.git merge --ff-only fix/42
masterとfix/42が一本のコミット上にある場合に、masterをHEADとして実行する。  
単純にmasterをfix/42に進める。  (ff = fast forward)
masterとfix/42が枝分かれしている状態の場合、エラーが発生する。

## 15.git merge --no-ff fix/42
git merge をした後、必ずマージコミットを作成する。
おそらく、git mergeのデフォルトの動作では、fast forwardできる場合には、マージコミットは作成されない。
ほとんどの場合ではマージコミットを作成する必要はないかもしれないが、
なんらかの理由で必ずマージコミットを作成したい場合に、--no-ffを指定する。

## 16.git fetch all
全てフェッチする

## 17.git remote add, git fetch --all
リモートリポジトリを登録してフェッチする

## 18.git pull
リモートリポジトリの変更をローカルリポジトリに反映する。  
この際、マージが必要な場合（fast forwardできない場合）、マージコミットが作成される。

## 19.git pull --rebase
remoteブランチをfetchした結果をrebaseする。
つまり、git fetch; git rebase と同じ。
マージコミットが発生しないので、コミットグラフがすっきりするメリットがある。
ちなみに、git pull は、git fetch; git merge と同じ。（詳細は、No.18参照）

## 20.git push
プッシュ

## 21.git cherry pick 2
2番目のノードだけを拾ってきてマージする

## 22.git init
実行されたディレクトリに.gitディレクトリが作成され、  
実行されたディレクトリがバージョン管理対象となる。

## 23.git clone
リポジトリを新しいフォルダに複製する。

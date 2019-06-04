# gitbootcamp-0605

## 01.git add


commitしたいファイルをステージングエリアに追加する

## 02.git commit
ローカルリポジトリに最新のリビジョンを追加する。

## 03.git commit -a
git add と git commit を同時にやってくれる。

## 04.git commit --amend
マスターブランチを作る

## 05.git branch fix/42
fix/42という名前のブランチを作成する

## 06.git checkout -b fix/24; git commit
fix/42のブランチを作成し、チェックアウト。
fix/42に対してコミットを行い、リビジョンを追加する。

## 07.git checkout -b fix/42
存在しないブランチ fix/42 を作成すると同時に、ブランチを fix/42 に移動する。
ブランチを移動するとは、HEADの位置を移動するということ。

## 08.git reset --hard master
リセットして自分にHEADを持ってくる

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

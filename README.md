# git-subcmd

gitに拡張コマンドを追加する

## set up

### MAC

download source
```
git clone https://github.com/adebadayo/git-subcmd.git
```

change permission
```
chmod 777 cmd/*
```

deploy
```
cp cmd/* /usr/local/bin
```

## command

### git-dev
指定ブランチから新たなブランチを作成して、リモートブランチも同時に作成する。

 git-dev [source branch] [new branch name]

source branch :ブランチ作成
new branch:新たに作成するブランチ名

例） git-dev develop feeature/add_migration

### git-bsync
指定マージ元ブランチから複数のブランチに対してマージとプッシュを一緒に行う
 git-bsync [source branch] [target branchs]

source branch :マージ元のブランチ名
target branchs : マージ先のブランチ名（可変長）

例） git-bsync feature/XXXX develop master

feature/XXXXブランチからdeevlop,masterへマージとプッシュを行う

実施コマンド

```
git checkout feature/XXXX
git pull
git pull origin feature/XXXX
git push
git checkout deevlop
git pull
git pull origin feature/XXXX
git push
git checkout master
git pull
git pull origin feature/XXXX
git push
```

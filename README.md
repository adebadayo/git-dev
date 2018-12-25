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

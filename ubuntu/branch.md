# 現在のブランチを常時表示する方法

## ホームディレクトリに移動する
```
cd ~
```

## vscodeでbashrcを開く
```
code .bashrc
```

## bashrcを開いたら以下の内容を追記
```
parse_git_branch() {
    git branch 2> /dev/null | sed -e '/^[^*]/d' -e 's/* \(.*\)/(\1)/'
}

PS1='\[\e]0;\u@\h: \w\a\]\[\e[32m\]\u@\h \[\e[34m\]\w\[\e[31m\]$(parse_git_branch)\[\e[0m\]\$ '
```

## 最後にsourceで読み込み直す
```
source ~/.bashrc
```

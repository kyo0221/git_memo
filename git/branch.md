# 現在のブランチを常時表示する方法

## vimでbashrcを開く(vimのインストールが必要)
```
vi ~/.bashrc
```

## bashrcに書き込む
```
parse_git_branch() {
    git branch 2> /dev/null | sed -e '/^[^*]/d' -e 's/* \(.*\)/[\1]/'
}

export PS1="\[\e[1;37m\]🐟\u| \h🤮\e[m \e[40;5;33m\w\e[m\e[41;5;30m\]\$(parse_git_branch)\e[00m\n>>>"

```

```
export PS1='\[\033[01;32m\]\u@\h\[\033[01;33m\] \w \[\033[01;31m\]$(__git_ps1 "(%s)") \n\[\033[01;34m\]\$\[\033[00m\] '
```

## 最後にsourceで読み込み直す
```
source ~/.bashrc
```

# 現在のブランチを常時表示する方法

## vimでbashrcを開く(vimのインストールが必要)
```
vi ~/.bashrc
```

## bashrcに書き込む
```
echo 'parse_git_branch() {
    git branch 2> /dev/null | sed -e "/^[^*]/d" -e "s/* \(.*\)/(\1)/"
}

PS1="\u 🤮\[\e[48;5;44m\e[01;32m\]\[\e[01;34m\\w\\[\e[48;5;42m]\$(parse_git_branch)\[\e[00m\\]\n>>> "

```

## 最後にsourceで読み込み直す
```
source ~/.bashrc
```

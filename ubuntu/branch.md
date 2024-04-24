# 現在のブランチを常時表示する方法

## vimでbashrcを開く
```
vi ~/.bashrc
```

## bashrcに書き込む
```
echo 'parse_git_branch() {
    git branch 2> /dev/null | sed -e "/^[^*]/d" -e "s/* \(.*\)/(\1)/"
}

PS1=\'\[\e]0;\u@\h: \w\a\]\[\e[32m\]\u@\h \[\e[34m\]\w\[\e[31m\]$(parse_git_branch)\[\e[0m\]\$ \'' >> ~/.bashrc

```

## 最後にsourceで読み込み直す
```
source ~/.bashrc
```

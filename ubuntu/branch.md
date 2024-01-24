# 現在のブランチを常時表示する方法

## ホームディレクトリに移動
`cd ~`

## wgetでスクリプトを取得する
```
wget https://raw.githubusercontent.com/git/git/master/contrib/completion/git-prompt.sh  wget https://raw.githubusercontent.com/git/git/master/contrib/completion/git-completion.bash
```

## vscodeでbashrcを開く
`code .bashrc`

## bashrcを開いたら以下の内容を追記
`PS1='\[\033[1;32m\]\u@\h\[\033[00m\]:\[\033[1;34m\]\W\[\033[00m\]\[\033[1;31m\]$(__git_ps1)\[\033[00m\]\$ '`

## 最後にsourceで読み込み直す
`source ~/.bashrc`

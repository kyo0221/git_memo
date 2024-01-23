#現在のブランチを常時表示する方法

##ホームディレクトリに移動
'npm run dev'cd ~'npm run dev'

##wgetでスクリプトを取得する
'npm run dev'wget https://raw.githubusercontent.com/git/git/master/contrib/completion/git-prompt.sh  wget https://raw.githubusercontent.com/git/git/master/contrib/completion/git-completion.bash'npm run dev'

##vscodeでbashrcを開く
'npm run dev'code .bashrc

##vscodeを起動したら以下の内容を追加
'npm run dev'PS1='\[\033[1;32m\]\u@\h\[\033[00m\]:\[\033[1;34m\]\W\[\033[00m\]\[\033[1;31m\]$(__git_ps1)\[\033[00m\]\$ ''npm run dev'

##最後にsourceで読み込み直す
'npm run dev'source ~/.bashrc'npm run dev'

## gitのalias登録
```
git config --global alias.co checkout
```

```
git config --global alias.br branch
```

```
git config --global alias.ci commit
```

```
git config --global alias.st status
```

## ステージの解除用alias
```
git config --global alias.unstage 'reset HEAD --'
```
使用例
$ git unstage fileA
$ git reset HEAD -- fileA

## commit info
```
git config --global alias.last 'log -1 HEAD'
```
使用例
$ git last
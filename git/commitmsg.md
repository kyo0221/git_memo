## commit メッセージのテンプレート作成

Gitでコミット時に使いたいデフォルトメッセージを
~/.gitmessage.txt　に記述する

```
git config --global commit.template ~/.gitmessage.txt
```

コミット時にデフォルトメッセージを使用することができる

```
git commit
```

### テンプレートファイルの例
```
#🐛fix: バグ修正
#🔧modify: 機能改善
#♻ refactor: リファクタリング
#📝docs: ドキュメント変更
#🎨style: フォーマットや構造改善
#🔥remove:　不要な機能・ファイルの削除
#✨feat: 部分的な機能追加
#🍰chore: 自動生成されたファイル
#🌱init commit: 初期コミット
#🧪test: テストやCIの修正・改善
#👕lint: Lintエラーの修正やコードスタイルの修正
#🚀️perf: パフォーマンス改善
#🆙update: 依存パッケージなどのアップデート
#🚧wip: 作業中
```
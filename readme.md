
- 参考
https://techblog.reazon.jp/entry/2024/09/11/120339

- actions/checkout@v4

ブランチをとってくる

```
  hello:
    runs-on: ubuntu-latest
    steps:
      - uses: actions/checkout@v4
      - run: |
          ls -a
          echo ""
          git fetch
          git branch -a
```

- 複数のコマンドを順次実行
```
- run: |
    ls -a
    echo ""
    git fetch
    git branch -a
```

### コンテキスト


```
name: Contextx
on: push
jobs:
  print:
    runs-on: ubuntu-latest
    steps:
      - run: echo "${{ github.actor }}"
```
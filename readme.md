

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
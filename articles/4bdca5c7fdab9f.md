---
title: "Pythonのtypingモジュールについて深堀りしてみる"
emoji: "🐍"
type: "tech" # tech: 技術記事 / idea: アイデア
topics: ["python", "typing"]
published: false
---
# はじめに
普段ふんわりと使っていたtypingモジュールについて調べたのでついでに記事にしてみました。
執筆時のPythonバージョンは3.12です
そもそもtypingモジュールについて

# そもそもtypingとは
https://docs.python.org/ja/3/library/typing.html
上記ドキュメントによると関数や変数に型のヒントを定義することができるらしい。

詳しい例(本文より引用)
---
>以下の関数は文字列を受け取って文字列を返す関数で、次のようにアノテーションがつけられます:
```python
def greeting(name: str) -> str:
    return 'Hello ' + name
```
>関数 greeting で、実引数 name の型は str であり、返り値の型は str であることが期待されます。サブタイプも実引数として許容されます。

引数と返り値に制約を課すことができるのかと思えばそうではありません。
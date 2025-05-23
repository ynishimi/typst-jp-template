# Typst の日本語テンプレートの例

## 概要

Typstで、とりあえず日本語で書き始めるためのテンプレートである。pLaTeXでのjarticle風のものを目指した。

## 使い方

同じフォルダに`template.typ`をおいて、次のように書いていく。

```typst
#import "lib/template.typ": *
#show: jarticle

こんにちは、世界。
```

補助的なものとして次のものを定義している。

- `年月日`: 日付の表示の仕方で、◯年◯月◯日の形のものを定義した。例えば

  ```typst
  #datetime.today().display(年月日)
  ```

  とすると、（今日の日付で）「2024年4月8日」のように表示される。同様に「日」を入れない`年月`も定義している。

- `appendix`: LaTeXでいうところの `\appendix`みたいなもの。通常節の番号は「1.1」みたいな感じだが

  ```typst
  #show: appendix
  ```

  とするとその後は「A.1」みたいな感じになる。

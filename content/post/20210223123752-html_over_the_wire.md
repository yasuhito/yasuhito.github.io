+++
title = "HTML Over the Wire"
author = ["Yasuhito Takamiya"]
date = 2021-02-23T00:00:00+09:00
draft = false
+++

React や Vue.js などの Web プログラミングフレームワークでは、ネイティブアプリと同様の UX を提供するために処理の大半をブラウザ側で行う。サーバは HTML ではなくデータを JSON として返す API/GraphQL サーバーとして動作し、HTML の生成はクライアントサイドのブラウザで動作する JavaScript フレームワーク上で行う。

これは、従来の Rails などのフレームワークと比較して複雑である。従来は、サーバ側で MVC フレームワークが動作し、データとプレゼンテーションを HTML としてサーバ側で生成し、ブラウザへ送っていた。一方で、近年の Web フレームワークはブラウザ上で MVC フレームワークが動作する。画面遷移を高速にするために、DOM ツリーの差分を取り、仮想 DOM という仕組みで最小の書き換えで画面遷移を実現する。

しかし、従来の単純なフレームワークでもネイティブアプリと同等の UX を達成することは可能である。DOM のうち動的な部分のみ JavaScript で書き換える。画面遷移についても、マウスオーバー時のプリフェッチによってソースコードを変更せずに高速化が可能である。

このための代表的なフレームワークが HOTwire。元々 Turbolinks や Stimulus.js だったものをまとめたもの。HTML の data 属性を使うことで、JavaScript 部分と HTML を結合することができる。JavaScript 部分は、サーバ側の MVC 実装や HTML にほとんど染み出さない。


## 参考文献 {#参考文献}

-   [HTML over the wire](https://m.signalvnoise.com/html-over-the-wire/)

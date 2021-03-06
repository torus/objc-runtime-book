---
title: 3 章 クラス
---

すでにいくつかのクラスの実例を見てきました。

クラスという概念は色々なプログラミング言語に存在しますが、言語ごとにそれぞれ少しずつ違っています。
この章ではどのようにしてクラスを宣言し、それがどのように実行環境に影響を及ぼすかについて見ていきます。

ランタイム API から見ると、クラスとはメソッドの集合です。
アプリケーションプログラムから何かのオブジェクトにアクセスするとき、必ず何らかのメソッドを呼び出します。

メソッド呼び出しとはメッセージの送信だった事を思い出してください。
クラスはどのようなメッセージを受け付けるかを宣言し、それぞれのメッセージに対してどのように振る舞うかを定義したものなのです。

Objective-C でクラスを宣言するには、C の構造体や C++ のクラスのようにヘッダファイルにメンバ変数やメソッドを書くのが一般的です。
このクラス宣言のお陰で、Objective-C コードから存在しないメソッドを間違って呼んでしまったりするのを防ぐことができます。

8 章ではランタイム API を使ってクラスを追加する方法を説明します。

クラスの宣言

Objective-C でクラスを宣言するには、以下のように書きます：



クラスはメンバ変数とメソッドを持つことができます。このようにいうと C++ のクラスに似ているように見えますが、メンバ変数の扱い方が少しだけ違います。
C++ と違って Objective-C ではメンバ変数の値に直接アクセスする方法はありません。

アクセサメソッド

オブジェクトのメンバ変数にアクセスするには通常はアクセサメソッドを使います。
アクセサメソッドはメンバ変数にアクセスするためにあるのですが、実のところメンバ変数にはアクセスしなくてもかまいません。

@synthesize

キーバリューコーディング

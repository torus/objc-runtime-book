# 2 章 オブジェクト

前の章でオブジェクトに対してメソッドを呼び出す様子を見ました。この章では新しくオブジェクトを作る方法を見ます。

## オブジェクトの生成

Objective-C におけるオブジェクトとは、Objective-C のやり方でメソッドを呼び出すことができるデータ型だと言えます。そしてオブジェクトとは**クラス**のインスタンスでもあります。

Objective-C では、クラスのインスタンスを生成するには次のように書きます：

```objc
NSString *str = [NSString stringWithUTF8String: "hello"];
```

これをオブジェクトに対するメソッド呼び出しの書き方にあてはめると、`NSString` という名前のオブジェクトにの `stringWithUTF8String:` というメソッドを呼んでいるように見えます。

Objective-C のリファレンスでは、`NSString` はクラスで、`stringWithUTF8String:` は**クラスメソッド**として扱われています。

これをランタイム API で書くと次のようになります：

```objc
id cls = objc_getClass("NSString");
SEL sel = sel_registerName("stringWithUTF8String:");
NSString *str = objc_msgSend(cls, sel, "hello");
```



このコードの後半をみると、クラスメソッドの呼び出しは、実際にはクラスを表すオブジェクトに対するメソッド呼び出しであることがわかります。



## プロパティ

## id 型

## NSObject

## アロケーションと初期化

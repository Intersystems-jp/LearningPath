---
title: .NET アプリケーションと InterSystems 製品の接続
date: 2024-12-12
permalink: dotNetApptoISCProducts.html
layout: post
---
<!-- 
> オリジナルラーニングページ：[Connecting .NET Applications to InterSystems Products](https://learning.intersystems.com/course/view.php?id=968)
-->

ADO.NET、XEP、Entity Framework、または Native API（Native SDK for .NET） を使用して、.NET アプリケーションを InterSystems IRIS® data platform やその他の InterSystems 製品およびテクノロジに接続する方法をご説明します。

---
[1. <img src="./assets/icons/ServerSideApp1.png" width="40%"/>](#1-)

[2. <img src="./assets/icons/dotNet2.png" width="40%"/>](#2-)

[3. <img src="./assets/icons/dotNet3.png" width="40%"/>](#3-)

[4. <img src="./assets/icons/dotNet4.png" width="40%"/>](#4-)

[5. <img src="./assets/icons/dotNet5.png" width="40%"/>](#5-)

[6. <img src="./assets/icons/dotNet6.png" width="40%"/>](#6-)

[7. <img src="./assets/icons/dotNet7.png" width="40%"/>](#7-)

---
## 1. <img src="./assets/icons/ServerSideApp1.png" width="70%"/>

各 API の利点を確認し、.NET アプリケーションを InterSystems 製品に接続するための方法を確認します。

- ビデオ：Using .NET to Connect to InterSystems IRIS（英語／日本語字幕付き）

{% include youtube.html id="UqE7gaBHhxE" %}

<details class="transcript2">
<summary> ▶日本語字幕 </summary>
<div class="content">
.NET 開発者としてアプリケーションを InterSystems IRIS data platform に接続する方法は数多くあります。
<br>
そして、InterSystems IRIS の強力なマルチモデルという特性を考慮するとこの接続の柔軟性はアプリケーション開発にとって非常に重要です。
<br>
アプリケーションのパフォーマンスを向上させ、アプリケーション開発をスピードアップする機会を提供します。
<br>
.NET アプリケーションを InterSystems IRIS に接続するために利用可能な API は、ADO.NET、XEP、.NET Native API、および Entity Framework の 4 つです。
<br>
これら 4 つの API がそれぞれどのように役立つかを示すためにタクシー料金を見積もるアプリケーションを開発するシナリオを考えてみましょう。
<br>
アプリケーションのある部分は、リレーショナルデータモデルを使用するのに特に適しているかもしれません。
<br>
この場合、ADO.NET (Microsoft .NET Framework のデータ・アクセス・テクノロジー) を使用することでリレーショナルな方法で InterSystems IRIS のデータにアクセスすることができます。
<br>
ADO.NET を使用することで、アプリケーションは InterSystems IRIS に接続しデータに対して SQL オペレーションを実行することができます。
<br>
標準的な Create、Read、Update、Delete 操作を実行できるほか、ストアド SQL プロシージャを呼び出すこともできます。
<br>
ADO.NET 経由での接続は非常に簡単です。必要なのは InterSystems IRIS のインストール・ディレクトリに含まれる InterSystems.Data.IRISClient.dll ファイルをアプリケーションが参照できることだけです。
<br>
さらに、他の 3 つの .NET API はすべて ADO.NET の基礎となる接続プロトコルを使用するため、まったく新しい接続を設定することなく、4 つの API すべてをアプリケーションで並行して使用できることに注意してください。
<br>
アプリケーションに戻るとコードの別の部分がオブジェクトの操作に適しているかもしれません。
<br>
例えば、道路上の各タクシーからリアルタイムのデータを取り込むなどです。
<br>
XEP は高スループットとオブジェクトの超高速転送に最適化された API であるため、このような場合に最適です。
<br>
XEP を使用する場合、追加の dll ファイルが必要ですがそのリファレンスによってアプリケーションは、道路上のすべてのタクシーに対する大量のリアルタイムのオブジェクト指向データを処理できます。
<br>
アプリケーションがこれらの API のうち 1 つだけを必要とする可能性もありますし、ADO.NET と XEP の組み合わせでリレーショナルおよびオブジェクト指向の要件をカバーできる可能性もあります。
<br>
さらに　InterSystems IRIS の .NET の残りの 2 つの API を使用することでアプリケーションにメリットが生じる場合もあります。
<br>
.NET Native API を使用すると、InterSystems IRIS の基礎となるデータ構造に直接アクセスできます。
<br>
これらのデータ構造はグローバルと呼ばれます。グローバルの柔軟性により、InterSystems IRIS は複数のデータ・モデルをすぐに提供できカスタムのデータ構造を作成することもできます。
<br>
Native API を使用するには、データ構造を十分に理解する必要がありますが、一般的なリレーショナル・アクセスやオブジェクト指向アクセスではなく、基盤となるグローバルに直接アクセスすることでアプリケーションのパフォーマンスを向上させることができます。
<br>
さらに、Native API を使用すると、InterSystems ObjectScript で記述された InterSystems IRIS クラスのメソッドやルーチンを呼び出すことができます。
<br>
そのため、タクシー・アプリケーションで InterSystems IRIS 内のメソッドを活用したい場合 (たとえば、IRIS 内のメソッドで計算するメソッド) は、Native API を使用する必要があります。
<br>
タクシー乗車時の予測チップ額を計算するメソッドやコメントを分析し、各運転手の上位の特徴を識別するための InterSystems IRIS に既にあるメソッドなど、InterSystems IRIS 内のメソッドを活用したい場合は、Native API を使用して、.NET アプリケーションからこれらのメソッドを呼び出すことができます。
<br>
最後に、.NET のオブジェクトからリレーショナルへのマッピングのための一般的なサードパーティフレームワークは、Entity Framework です。
<br>
Entity Framework が特に役立つのは、データモデルが複雑で .NET クラスをデータベースにマッピングする必要がある場合です。
<br>
たとえば、タクシーアプリケーションの一部で複数のベンダーからのデータ傾向を処理する必要があり、異なる複雑なデータ構造を使用する可能性があります。
<br>
Entity Framework に精通している場合は、その専門知識を活用しアプリケーションから InterSystems IRIS データに接続する API として Entity Framework を自由に使用できます。
<br>
ADO.NET、XEP、Native API、または Entity Framework を使用することで .NET アプリケーションは、InterSystems IRIS に接続するためのさまざまなオプションを利用できます。
<br>
1 つの .NET アプリケーションから 4 つの API をすべて利用できるため、InterSystems IRIS を使用した重要なソリューションの構築がこれまで以上に強化されます。
</div>
</details>

<br>
- <a href="https://learning.intersystems.com/course/view.php?name=.NET%20Connection%20Strategy" target="_blank">オンラインコース（英語）：Designing a .NET Connection Strategy</a>


---
## 2. <img src="./assets/icons/dotNet2.png" width="70%"/>

Visual Studio プロジェクトで InterSystems ADO.NET マネージド・プロバイダを使用して、InterSystems サーバーのデータにリレーショナル・アクセスできます。

詳細は、以下ドキュメントをご参照ください。

<a href="https://docs.intersystems.com/irislatestj/csp/docbook/DocBook.UI.Page.cls?KEY=AFL_adonet" target="_blank">InterSystems IRIS デモ ： ADO.NET を使用した接続</a>

---
## 3. <img src="./assets/icons/dotNet3.png" width="70%"/>

XEP を使用して、高性能でリアルタイムのオブジェクトを迅速に格納できます。

- <a href="https://learning.intersystems.com/course/view.php?name=Using%20XEP%20with%20.NET" target="_blank">ビデオ（英語／日本語字幕付き）：Using XEP with .NET</a>


- <a href="https://docs.intersystems.com/iris20241/csp/docbookj/DocBook.UI.Page.cls?KEY=BNETXEP_xep" target="_blank">ドキュメント：.NET での XEP Event Persistence の使用法

---
## 4. <img src="./assets/icons/dotNet4.png" width="70%"/>
Native API を使用してIRISのグローバル変数にデータを格納したり、InterSystems IRIS のメソッドまたはルーチンを呼び出します。

- <a href="https://learning.intersystems.com/course/view.php?name=Native%20API%20for%20.NET" target="_blank">ビデオ（英語／日本語字幕付き）：Using the Native API for .NET</a>

- <a href="https://docs.intersystems.com/irislatestj/csp/docbook/DocBook.UI.Page.cls?KEY=BNETNAT_about" target="_blank">ドキュメント：Native SDK for .NET の概要</a>

- <a href="https://jp.community.intersystems.com/node/559276" target="_blank">記事：Native SDK (NativeAPI) for .NET を使用する簡単なサンプルのご紹介</a>

---
## 5. <img src="./assets/icons/dotNet5.png" width="70%"/>
Entity Framework Provider の使用方法を確認し、Code First アプローチと Database First アプローチの使用方法を学びます。

- <a href="https://docs.intersystems.com/irislatestj/csp/docbook/DocBook.UI.Page.cls?KEY=BNET_eframe" target="_blank">ドキュメント：IRISClient アセンブリの Managed Provider</a>


---
## 6. <img src="./assets/icons/dotNet6.png" width="70%"/>

各接続方法の利点を確認するため、体験環境を使って演習してみましょう。

<a href="https://learning.intersystems.com/course/view.php?id=2522" target="_blank">体験環境付き演習（英語）：Stock Trading with .NET</a>


---
## 7. <img src="./assets/icons/dotNet7.png" width="70%"/>

.NET ゲートウェイを使用して、InterSystems ObjectScript で .NET オブジェクトをどのように操作できるかを確認します。

<a href="https://docs.intersystems.com/irislatestj/csp/docbook/DocBook.UI.Page.cls?KEY=BEXTSERV_coding" target="_blank">ドキュメント：外部言語の操作</a>

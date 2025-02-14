---
title: Python アプリケーションを作成する
date: 2024-12-10
permalink: WritingPythonAppWithInterSystems.html
layout: post
---
<!-- 
> オリジナル：[Writing Python Applications with InterSystems](https://learning.intersystems.com/course/view.php?id=1943)
-->
既存の Python コーディングスキルを活用して、InterSystems® アプリケーションを強化します。

このパスでは、クライアントの Python アプリケーションから InterSystems サーバーに接続する方法、InterSystems ObjectScript コードに Python を組み込む方法（Embedded Python）、Python ライブラリの呼び出しに負荷のかかる処理が必要な場合に別のサーバーある InterSystems サーバーを呼び出す方法について学習します。

なおこのパスは、Pythonの基本的なコーディング経験があることを前提としています。必要に応じて、[Python for Beginners](https://www.python.org/about/gettingstarted/)をご覧ください。

---
[1. <img src="./assets/icons/1.png" width="40%"/>](#1-)

[2. <img src="./assets/icons/Python2.png" width="40%"/>](#2-)

[3. <img src="./assets/icons/Python3.png" width="40%"/>](#3-)

[4. <img src="./assets/icons/Python4.png" width="40%"/>](#4-)

---
## 1. <img src="./assets/icons/1.png" width="70%"/>

InterSystems のアプリケーションで Python ライブラリを活用する方法をご説明します。

pyodbc を使用して既存の Python アプリケーションを接続したり、Embedded Python（または「組み込み Python」） を使用して、Python プログラムを ObjectScrit で記述されたプログラムと同等の位置付けで実行できます。

また、InterSystems Native API または外部言語サーバを使用して、Python で完全な InterSystems アプリケーションを構築することもできます。

![](./assets/icons/PythonLP-1.png)

Python 開発者が、InterSystems 製品を使用してアプリケーションを構築する場合、いくつかのオプションを選択できます。

- **pyodbc** を使用する方法

    従来のクライアント・サーバーアーキテクチャで ODBC を使用して既存の Python アプリケーションとInterSystems サーバを接続します。

    Pyodbc は DB API 2.0 仕様を実装しています。ODBC を使用して SQL クエリを作成し、データを取得します。

- **Embedded Python** を使用する方法

    Python プログラムを ObjectScrit で記述されたプログラムと同等の位置付けで実行できます。

- その他の方法

    - **InterSystems Python Native API** を使用して、InterSystems IRIS クラスおよびグローバルを操作できます。

    - **外部言語サーバー**を使用して、InterSystems IRIS カーネルの外部で Python コードを実行できます。
    
        外部言語サーバは、プロセス外または InterSystems IRIS とは別のサーバで実行する必要がある Python アプリケーションに適用できます。
        
        例えば、CPU やメモリの使用率が高い場合やコードの安定性に疑問がある場合に使用します。

---
## 2. <img src="./assets/icons/Python2.png" width="70%"/>

Python アプリケーションを　InterSystems 製品に接続するための最も一般的なオプションである pyodbc の使用方法について説明します。

- <a href="https://docs.intersystems.com/irislatestj/csp/docbook/DocBook.UI.Page.cls?KEY=BNETODBC_support_pyodbc" target="_blank">ドキュメント:pyodbc Python ODBC ブリッジのサポート</a>


- <a href="https://jp.community.intersystems.com/node/478616" target="_blank">【はじめての InterSystems IRIS】セルフラーニングビデオ：アクセス編：Python から PyODBC を使って IRIS に接続してみよう</a>

{% include youtube-list.html id="6ZMb3asLdKY" list="PLzSN_5VbNaxBPaSSINLzv-CkDJy00bOSQ&index=6" %}

---
## 3. <img src="./assets/icons/Python3.png" width="70%"/>

Embedded Python を使用して ObjectScript と並行して Python ライブラリを呼び出すことができます。

{% include youtube.html id="qhNnS7rN7XE" %}
<br>
上記ビデオの日本語字幕入りビデオはこちら👉<a href="https://learning.intersystems.com/course/view.php?name=EmbeddedPythonOverview" target="_blank">What Is Embedded Python?</a>

<details class="transcript2">
<summary> ▶日本語字幕 </summary>
<div class="content">
Embedded Python は、InterSystems IRIS data platform の機能であり Python 開発者が InterSystems IRIS のデータと機能に完全かつ直接アクセスできるようにします。このビデオでは、Embedded Python の使用方法と InterSystems IRIS の言語相互運用性ツールとの関係について説明します。
<br>
ご存知のように、InterSystems IRIS には、ObjectScript と呼ばれる強力な組み込みプログラミング言語が用意されており、データ・プラットフォーム内で解釈、コンパイル、実行されます。
<br>
ObjectScript は InterSystems IRIS のコンテキスト内で実行されるため、データ・プラットフォームのメモリとプロシージャ呼び出しに直接アクセスできます。
<br>
つまり、ユーザは特定のイベント (データベースへの挿入や TCP ポートへの新しいデータの入力など) に対してコールバック関数を指定できます。
<br>
このような直接アクセスが可能であり、InterSystems IRIS 内で実行されるため ObjectScript は組み込みプログラミング言語と言われています。
<br>
Embedded Python では、ObjectScript の経験がない Python 開発者でも、ObjectScript と同じ機能を利用できるようになりました。
<br>
Embedded Python は Python プログラミング言語の拡張であり、InterSystems IRIS プロセスコンテキスト内で Python コードを実行できます。
<br>
Embedded Python は ObjectScript と同じプロセスコンテキストを共有するため、ObjectScript で記述されたオブジェクトとネイティブに対話することができます、
<br>
ObjectScript で記述されたオブジェクトとネイティブに対話できます。
<br>
逆もまた真です： ObjectScript コードは Python モジュールやライブラリとネイティブに対話できます。
<br>
これにより、オブジェクトやメソッド、さらには完全なコードライブラリまでもが Python と ObjectScript のコンテキスト間でシームレスに受け渡しができるようになり、2 つの言語間の相互運用性の新しい階層が実現します。
<br>
組み込み Python は、ObjectScript のプロキシ・オブジェクトとやり取りすることなく、メモリ上の InterSystems IRIS オブジェクトに対して直接動作します。これにより、速度とパフォーマンスが劇的に向上し、構成の複雑さが軽減されます。
<br>
ObjectScript と Python は同じオブジェクトメモリ上で動作するため、Python オブジェクトは単に ObjectScript オブジェクトをエミュレートしているのではなく、ObjectScript オブジェクトであると言えます。
<br>
これらの言語が同等であるということは作業に最も適した言語、あるいはアプリケーションを書くのに最も使いやすい言語を選択できるということです。
<br>
Embedded Python を使用する場合 3 つの異なる方法でコードを書くことができます。
<br>
まず通常の .py ファイルを作成し InterSystems IRIS コンテキストから呼び出します。この場合、データプラットフォームは Python プロセスを起動し iris モジュールをインポートできるようにします。IRIS は、Python プロセスを IRIS カーネルに自動的にアタッチし Python コードのコンテキストから ObjectScript のすべての機能にアクセスできるようにします。
<br>
次に、通常の ObjectScript コードを記述し %SYS.Python パッケージを使用して Python オブジェクトをインスタンス化できます。この ObjectScript パッケージを使用すると Python モジュールとライブラリをインポートして ObjectScript 構文を使用してそのコードベースで作業できます。
<br>
%SYS.Python パッケージを使用すると Python の知識がない ObjectScript 開発者でも ObjectScript コードで Python ライブラリの豊富なエコシステムを使用できるようになります。
<br>
第 3 に、InterSystems クラス定義を作成し Python でメソッドを記述できます。そのメソッドを呼び出すと Python インタプリタが起動します。
<br>
このメソッドには、Python コードのブロックの self キーワードに 包含されるクラスのインスタンスへの参照を入力するという利点があります。
<br>
さらに、Python を使用して InterSystems クラスのクラス・メソッドを記述することで、テーブルに新しい行が追加されるといった SQL のさまざまなデータ入力イベントを処理するメソッドを簡単に実装できます。また、Python でカスタムストアドプロシージャを迅速に開発することもできます。
<br>
このように、Embedded Python を利用することでパフォーマンスを犠牲にすることなく作業に最適なプログラミング言語を選択することができます。
</div>
</details>
<br>

- <a href="https://learning.intersystems.com/course/view.php?name=EmbeddedPythonQS" target="_blank">ビデオ（英語／日本語字幕あり）：演習環境付き演習：Embedded Python QuickStart</a>

> **英語ですが、オンラインコースもあります**
>- <a href="https://learning.intersystems.com/course/view.php?name=EmbeddedPythonParsingImages" target="_blank">Parsing Images and Charting Data with Embedded Python</a>
{: .block-tip}

↑上記オンラインコース演習と同等の内容をお試しいただける記事👉<a href="https://jp.community.intersystems.com/node/513136" target="_blank">Embedded Python を使ってレシート（JPG）の中身を IRIS に登録してみました</a>

---
**【オプションビデオ：Embedded Python のセルフラーニングビデオのプレイリスト】**

✅ <a href="https://www.youtube.com/playlist?list=PLzSN_5VbNaxBLXlC9oCgwPtxBilT8tJ96" target="_blank">IRISでPythonを使ってみよう-PythonスクリプトファイルをObjectScriptを使用して呼び出す（IRIS ターミナルからPythonスクリプトファイルに記載した内容を呼び出す）</a>

{% include youtube-list.html id="awiRCQnm5Vo" list="PLzSN_5VbNaxBLXlC9oCgwPtxBilT8tJ96&index=6" %} 
<br>
✅ <a href="https://www.youtube.com/playlist?list=PLzSN_5VbNaxBLXlC9oCgwPtxBilT8tJ96" target="_blank">IRISでPythonを使ってみよう-Pythonの組み込み関数をObjectScriptで使用する方法</a>

{% include youtube-list.html id="dyx4wNw51YU" list="PLzSN_5VbNaxBLXlC9oCgwPtxBilT8tJ96&index=9" %} 
<br>
✅ <a href="https://www.youtube.com/playlist?list=PLzSN_5VbNaxBLXlC9oCgwPtxBilT8tJ96" target="_blank">IRISでPythonを使ってみよう-参考情報：グローバル変数の操作</a>

{% include youtube-list.html id="XzWeCICH0VY" list="PLzSN_5VbNaxBLXlC9oCgwPtxBilT8tJ96&index=18" %}
<br>
✅ <a href="https://www.youtube.com/playlist?list=PLzSN_5VbNaxDAPjSBe5F-uGbGkoJqcerL" target="_blank">SQLアクセス編-Sample.Personの作成（実演）- Pythonシェルで Embedded Python を利用して IRIS にあるテーブルにアクセスする</a>

{% include youtube-list.html id="hJs3JUzWoWE" list="PLzSN_5VbNaxDAPjSBe5F-uGbGkoJqcerL&index=5" %}
<br>
✅ <a href="https://www.youtube.com/playlist?list=PLzSN_5VbNaxBnEb5rq-676b1l7Ym6INjL" target="_blank">オブジェクトアクセス編-インスタンス生成から保存までの実演</a>

{% include youtube-list.html id="Ayir9SgMId8" list="PLzSN_5VbNaxBnEb5rq-676b1l7Ym6INjL&index=7" %}
<br>
> **英語オプションビデオもあります**
>
>- <a href="https://learning.intersystems.com/course/view.php?name=PythonLibrariesOS" target="_blank">Using Python Libraries from ObjectScript with Embedded Python</a>
>
>    このビデオでは、IRIS ターミナルを利用して ObjectScript から Python を実行する方法を解説しています。
>
>- <a href="https://learning.intersystems.com/course/view.php?name=Embedded%20Python%20with%20Interoperability" target="_blank">Leveraging Embedded Python in Interoperability Productions</a>
>
>    InterSystems サーバーの Interoperability プロダクションで Embedded Python を活用する方法を解説しています。
>    
>    ビジネスホストのコンテキストとライフサイクルにおける Embedded Python の利点について学習できます。また、AWS SNS と OPC UA サーバとの統合デモをご覧いただき、Embedded Python を使ったビジネスホストの構築方法をご紹介します。
>
>- <a href="https://learning.intersystems.com/course/view.php?name=Embedded%20Python%20for%20ObjectScript%20Developers:%20Working%20with%20Python%20and%20ObjectScript%20Side-By-Side" target="_blank">Using the InterSystems IRIS Library from Embedded Python</a>
>
>    Python を使用して InterSystems IRIS® data platform と対話する方法をご紹介します。
>    
>   Embedded Python を使用すると、InterSystems ObjectScript と Python を同時に使用できます。
>   このビデオでは、Pyhtonシェルの中から IRIS のクラスのインスタンスを生成したり、メソッドを実行する例、またグローバル変数の操作例、SQLの実行例をご覧いただけます。
{: .block-tip}

- <a href="https://docs.intersystems.com/irislatestj/csp/docbook/DocBook.UI.Page.cls?KEY=AFL_epython" target="_blank">ドキュメント：組み込み Python の概要</a>

- <a href="https://docs.intersystems.com/irislatestj/csp/docbook/DocBook.UI.Page.cls?KEY=GEPYTHON" target="_blank">ドキュメント：組み込みPythonの使用法</a>

---
## 4. <img src="./assets/icons/Python4.png" width="70%"/>

InterSystems Python SDK を使用して、Python から InterSystems IRIS クラスのインスタンスをリモートで作成および操作できます。また、外部言語サーバを使用して、InterSystems 製品から外部プロセスで実行されている Python コードを呼び出す方法をご紹介しています。


✅ <a href="https://jp.community.intersystems.com/node/478611" target="_blank">【はじめての InterSystems IRIS】セルフラーニングビデオ：アクセス編：Python の NativeAPI に挑戦</a>

{% include youtube-list.html id="esRyiWaIofg" list="PLzSN_5VbNaxBPaSSINLzv-CkDJy00bOSQ&index=5" %}

<br>
> **英語ですが、オンラインコースもあります**
>
>- <a href="https://learning.intersystems.com/course/view.php?name=Native%20API%20for%20Python" target="_blank">ビデオ（英語）:Using the Native API for Python</a>
>
>- <a href="https://learning.intersystems.com/course/view.php?name=Python%20QS" target="_blank">演習環境付き演習（英語／ビデオに日本語字幕あり）:Python QuickStart</a>
>
>    InterSystems IRIS® data platform は、軽量な Native SDK for Python をサポートし Python アプリケーションが InterSystems IRIS データベースと直接対話できるようにします。この SDK は、Native API for Python を提供しアプリケーションは、グローバルとして知られる InterSystems IRIS 内の基礎となるデータ構造にアクセスしたり、InterSystems ObjectScript のメソッドやルーチンを呼び出したりすることができます。 
>
>- <a href="https://learning.intersystems.com/course/view.php?name=PythonMultiModel" target="_blank">体験環境付き演習（英語／ビデオに日本語字幕あり）Interacting with Data in Python Using Multiple Data Models</a>
>    
>    InterSystems IRIS® data platform のマルチモデル・アーキテクチャをお試しください。
>
>   InterSystems IRIS のマルチ・モデル・アクセスは、グローバルと呼ばれるデータ構造によって実現されています。これにより、データの重複を回避しながら、柔軟なデータ・アクセスが可能になります。
>
>    Python では、Native API を使用して InterSystems IRIS に接続し、グローバルを使用してデータを操作できます。もう 1 つのオプションは、PyODBC で接続し業界標準の SQL を使用してデータにアクセスする方法です。この場合、データはリレーショナル・テーブルとしてモデル化されます。
>
> - <a href="https://learning.intersystems.com/course/view.php?name=Using%20Python%20with%20InterSystems%20IRIS" target="_blank">ビデオ（英語）：Evaluating Python Development Strategies</a>
{: .block-tip}

- <a href="https://docs.intersystems.com/irislatestj/csp/docbook/DocBook.UI.Page.cls?KEY=BEXTSERV_coding" target="_blank">ドキュメント：外部言語の操作</a>


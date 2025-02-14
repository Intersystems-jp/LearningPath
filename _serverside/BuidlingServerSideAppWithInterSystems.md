---
title: サーバーサイドアプリケーションを構築する
date: 2024-12-09
permalink: BuidlingServerSideAppWithInterSystems.html
layout: post
---
<!-- 
>オリジナル：[Building a Server-Side Application with InterSystems](https://learning.intersystems.com/course/view.php?id=2369)
-->
InterSystems 製品の組み込み言語である InterSystems ObjectScript を使用して、新しいクラスの作成、オブジェクトの操作、SQL クエリの実行について学習します。

このパスを進めるために InterSystems 製品に対する前提知識は必要ありません。

こパスでは、ObjectScript を使ったサーバーサイドアプリケーションの構築を行うために以下の内容を習得できます。

（IDE には VSCode を使用しますが、作成する内容はスタジオでも作業できます。）

- クラス定義の作成
- ObjectScript使用したオブジェクト操作
- ObjectScriptの基本操作
- IRIS SQLの基本操作
- 簡単なアプリケーションテーマに合わせたクラス定義、メソッド、データの作成

[1. <img src="./assets/icons/ServerSideApp1.png" width="40%"/>](#1-)

[2. <img src="./assets/icons/ServerSideApp2.png" width="40%"/>](#2-)

[3. <img src="./assets/icons/ServerSideApp3.png" width="40%"/>](#3-)

[4. <img src="./assets/icons/ServerSideApp4.png" width="40%"/>](#4-)

---
## 1. <img src="./assets/icons/ServerSideApp1.png" width="70%"/>

最初に、InterSystems IRIS® data platform のアーキテクチャとクラスの基本を学び ObjectScript の学習を開始します。

以下動画から、IRISの開発環境の作成方法、ネームスペース／データベースについて、IDE から IRIS に接続する方法を確認できます。
- 記事：<a href="https://jp.community.intersystems.com/node/478601" target="_blank">【はじめての InterSystems IRIS】セルフラーニングビデオ：基本その2：InterSystems IRIS で開発をはじめよう！</a>

    {% include youtube-list.html id="ID6ImJTgJRk" list="PLzSN_5VbNaxBPaSSINLzv-CkDJy00bOSQ&index=3" %}
<br>

以下コンテンツから、ObjectScriptの基本操作を確認できます。
- <a href="https://github.com/Intersystems-jp/ObjectScriptCookBook/blob/master/Basic.md" target="_blank">[ObjectScript クックブック：ObjectScriptの基本のき！</a>

講師付きトレーニングコースもご用意しています。
- <a href="https://www.intersystems.com/jp/intersystems-sql/" target="_blank">[InterSystems SQL の使い方（２日間）</a>
- <a href="https://www.intersystems.com/jp/intersystems-object/" target="_blank">[InterSystems Object の使い方（２日間）</a>


> **英語ビデオやオンラインコースもあります**
>
>- <a href="https://learning.intersystems.com/course/view.php?name=Architecture%20Overview" target="_blank">ビデオ（英語）InterSystems Architecture Overview</a>
>
>- <a href="https://learning.intersystems.com/course/view.php?name=IRIS%20Class" target="_blank">[オンラインコース（英語）：Creating an InterSystems Class Definition in VS Code</a>
>
>- <a href="https://learning.intersystems.com/course/view.php?name=Cach%C3%A9%20ObjectScript%20Basics" target="_blank">[オンラインコース（英語）:InterSystems ObjectScript Basics</a>
{: .block-tip}

---
## 2. <img src="./assets/icons/ServerSideApp2.png" width="70%"/>

続いて、オブジェクトを作成、保存、ロード、および削除するメソッドを使用します。また、ObjectScript で記述したメソッド内で SQL 文を利用する方法も学習します。

以下動画から、クラス定義の作成からインスタンス生成、保存までの流れを確認できます。
- <a href="https://jp.community.intersystems.com/node/478606" target="_blank">【はじめての InterSystems IRIS】セルフラーニングビデオ：基本その3：IRIS でクラス定義を作ろう（オブジェクト操作の練習）</a>

    {% include youtube-list.html id="kWJCzn9bndQ" list="PLzSN_5VbNaxBPaSSINLzv-CkDJy00bOSQ&index=4" %}

<br>
メソッド内でSQLを記述する方法については、以下のコンテンツをご参照ください。

- <a href="https://github.com/Intersystems-jp/ObjectScriptCookBook/blob/master/Basic.md#7-%E3%83%A1%E3%82%BD%E3%83%83%E3%83%89%E3%82%84%E3%83%AB%E3%83%BC%E3%83%81%E3%83%B3%E3%81%A7sql%E3%82%92%E5%AE%9F%E8%A1%8C%E3%81%99%E3%82%8B%E6%96%B9%E6%B3%95" target="_blank">ObjectScriptクックブック：7.メソッドやルーチンでSQLを実行する方法</a>)

- <a href="https://docs.intersystems.com/irislatestj/csp/docbook/DocBook.UI.Page.cls?KEY=GOBJ_intro" target="_blank">ドキュメント：クラス・プログラミングの基本的な考え方</a>

> **英語ビデオやオンラインコースもあります**
>
>- <a href="https://learning.intersystems.com/course/view.php?name=IRIS%20Objects%20Introduction" target="_blank">（オンラインコース：英語）InterSystems IRIS Objects Introduction</a>
>- <a href="https://learning.intersystems.com/course/view.php?name=Cach%C3%A9%20SQL%20Overview" target="_blank">（オンラインコース：英語）InterSystems SQL Overview]</a>
{: .block-tip}

---
## 3. <img src="./assets/icons/ServerSideApp3.png" width="70%"/>

このパスで学習したことを利用して、小さなデータベースアプリケーションを作成しましょう。

<a href="https://learning.intersystems.com/course/view.php?name=Server-Side%20Application%20Exercise" target="_blank">体験環境付き演習（英語）：Learning Path Exercise: Building a Server-Side Application with InterSystems IRIS</a>



---
## 4. <img src="./assets/icons/ServerSideApp4.png" width="70%"/>

上記内容を全て終了したら、次は小テストにチャレンジしましょう。

オンラインラーニング（英語）の <a href="https://learning.intersystems.com/course/view.php?id=2369" target="_blank">Building a Server-Side Application with InterSystems</a> にアクセスし、各セクション右側にあるチェックボックスに全てチェックを付けると、「Take the assesment」のリンクが表示されます。

小テストに合格すると、デジタルバッジを獲得できます（コミュニティやLinkedInに表示させることができます）。

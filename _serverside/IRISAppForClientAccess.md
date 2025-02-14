---
title: IRISを利用したWebアプリケーションの構成
date: 2024-12-10
permalink: IRISAppForClientAccess.html
layout: post
---
<!-- 
>オリジナル：[Configuring InterSystems IRIS Applications for Client Access](https://learning.intersystems.com/course/view.php?id=1975)-->

このパスでは、InterSystems IRIS® data platform を Web アプリケーションのバックエンドとして機能させるためのセットアップ方法をご紹介します。

具体的には、REST 経由でアクセスする InterSystems IRIS アプリケーションを外部システムやユーザからデータにアクセスできるようにする方法と、JSON データの入出力方法を簡単に行う方法を学習できます。

前提知識として、Web アプリケーションのバックエンドとして InterSystems IRIS を使用する知識を前提とし、オブジェクトと SQL の使用経験が必要です。必要に応じて、別のラーニングパス：<a href="BuidlingServerSideAppWithInterSystems.html" target="_blank">「InterSystems を使用してサーバーサイドアプリケーションを構築する」</a>をご覧ください。

上記パス以外には、以下記事を利用した学習方法もあります。

- 記事：<a href="https://jp.community.intersystems.com/node/478601" target="_blank">【はじめての InterSystems IRIS】セルフラーニングビデオ：基本その2：InterSystems IRIS で開発をはじめよう！</a>
- 記事：<a href="https://jp.community.intersystems.com/node/478606" target="_blank">【はじめての InterSystems IRIS】セルフラーニングビデオ：基本その3：IRIS でクラス定義を作ろう（オブジェクト操作の練習）</a>
- <a href="https://github.com/Intersystems-jp/ObjectScriptCookBook/blob/master/Basic.md" target="_blank">ObjectScript クックブック：ObjectScriptの基本のき！</a>
- 講師付きトレーニング

    下記コース受講時 1 日の補足コースとして「IRIS で REST サーバを作成する方法」「ObjectScript の使い方」を追加できます。コースご依頼時にお知らせください。
    - <a href="https://www.intersystems.com/jp/intersystems-sql/" target="_blank">InterSystems SQL のトレーニングコース（２日間）</a>
    - <a href="https://www.intersystems.com/jp/intersystems-object/" target="_blank">InterSystems Object のトレーニングコース（２日間）</a>

---

[1. <img src="./assets/icons/WebApp1.png" width="40%"/>](#1-)

[2. <img src="./assets/icons/WebApp2.png" width="40%"/>](#2-)

[3. <img src="./assets/icons/WebApp3.png" width="40%"/>](#3-)

---
## 1. <img src="./assets/icons/WebApp1.png" width="70%"/>
InterSystems IRIS で RESTful サービスをセットアップして、Web アプリケーションなどの外部システムから IRIS 内のデータにアクセスできるようにする方法を説明します。

- <a href="https://jp.community.intersystems.com/node/479546" target="_blank">【はじめてのInterSystems IRIS】セルフラーニングビデオ：アクセス編：IRIS で作成する REST サーバの仕組み</a>

    IRIS で作成する REST サーバの仕組みを解説します。

    {% include youtube-list.html id="tWP_9-jk4no" list="PLzSN_5VbNaxBPaSSINLzv-CkDJy00bOSQ&index=7" %}
<br>
- <a href="https://jp.community.intersystems.com/node/479551" target="_blank">【はじめてのInterSystems IRIS】セルフラーニングビデオ：アクセス編：（REST）手動で作成するディスパッチクラス</a>

    REST サーバに必要なディスパッチクラスを手動で用意する方法を解説します。

    {% include youtube-list.html id="q3XVT98_05I" list="PLzSN_5VbNaxBPaSSINLzv-CkDJy00bOSQ&index=8" %}
<br>
- <a href="https://jp.community.intersystems.com/node/479596" target="_blank">【はじめてのInterSystems IRIS】セルフラーニングビデオ：アクセス編：（REST）APIファーストで作成するRESTディスパッチクラス</a>

    REST サーバに必要な REST ディスパッチクラスを API ファーストの手順で作成する方法を解説します（OpenAPI 2.0　に基づいて作成したアプリケーション定義を使用してディスパッチクラスを作成する手順を解説します）。

    {% include youtube-list.html id="SwquEq1fjTk" list="PLzSN_5VbNaxBPaSSINLzv-CkDJy00bOSQ&index=9" %}
<br>
- <a href="https://jp.community.intersystems.com/node/559356" target="_blank">REST　経由で情報を入力する場合の Interoperability（相互運用性機能）のサンプル</a>


> **英語ビデオやオンラインコースもあります**
>- <a href="https://learning.intersystems.com/course/view.php?name=DevelopingRESTInterfaces" target="_blank">体験環境付き演習:Developing REST Interfaces
>
>    InterSystems IRIS® data platform で REST インタフェースを組み立てる方法について解説しています。
>   
>    REST は、メソッドの実行やデータのクエリのためにサーバと対話する信頼性の高い方法です。この演習では、InterSystems IRIS サーバ、Web アプリケーション、ディスパッチ・クラスと実装クラス、および Web クライアントがどのように組み合わされてコーヒー・メーカー会社のフロント・エンド Web サイトが作成されるかを確認していきます。
>
>- <a href="https://learning.intersystems.com/course/view.php?name=REST%20Services" target="_blank">オンラインコース：Setting Up RESTful Services</a>
>
>   InterSystems IRIS® data platform で RESTful サービスをセットアップする方法をご紹介します。API 仕様から始めて API のバックエンド・ロジックを生成して実装します。クライアントアプリケーションを使用して RESTful サービスを呼び出す方法、RESTful サービスを相互運用性プロダクションにアタッチする方法、API トラフィックを監視および制御する方法を説明します
{: .block-tip}

---
## 2. <img src="./assets/icons/WebApp2.png" width="70%"/>

InterSystems 製品で JSON を操作するときに使用するダイナミックオブジェクト（ダイナミックエンティティ）の利用方法を学習します。

記事：<a href="https://jp.community.intersystems.com/node/480106" target="_blank">【はじめてのInterSystems IRIS】セルフラーニングビデオ：アクセス編：IRIS での JSON の操作</a> では、以下のビデオを参照しながら、サンプルコードを試しながら進めることができるようにビデオとサンプルコードを埋め込んでいます。

ビデオだけをご覧いただく場合は、以下ご参照ください。

✅ InterSystems IRIS サーバ内でのJSONの操作

{% include youtube-list.html id="045HRug72VE" list="PLzSN_5VbNaxBPaSSINLzv-CkDJy00bOSQ&index=10" %}
<br>

✅ JSONの操作　つづき：SQL関数と%JSON.Adapterを使ってみる

{% include youtube-list.html id="3YKkFqJj2G8" list="PLzSN_5VbNaxBPaSSINLzv-CkDJy00bOSQ&index=11" %}
<br>

✅ JSONの操作　つづき：ダイナミックエンティティのメソッドを使ってみる

{% include youtube-list.html id="4ZIsetgJaxA" list="PLzSN_5VbNaxBPaSSINLzv-CkDJy00bOSQ&index=12" %}
<br>

> **英語ビデオやオンラインコースもあります**
>- <a href="https://learning.intersystems.com/course/view.php?name=JSON%20in%20IRIS" target="_blank">オンラインコース：Using JSON in InterSystems IRIS</a>
>
>   ダイナミックオブジェクトを使用して JSON をモデル化し、InterSystems IRIS® data platform で JSON データを扱う方法を学習します。
>
>   また、JSON データの取得と生成、エラーの処理、およびアプリケーションのトラブルシューティングの方法について説明します。
>
>   最後にレストランの利用者がレストランを評価しその評価を Google Places から取得した既存のレビューに追加するアプリケーションを構築します。このシナリオの詳細については、コースの最初のセクションを参照してください。
{: .block-tip}



## 3. <img src="./assets/icons/WebApp3.png" width="70%"/>

InterSystems API Manager は、アプリケーション間のゲートウェイとして機能しトラフィックを監視・制御します。

InterSystems IRIS® data platform と InterSystems IRIS® for Health でどのように機能するのか、また、どのようなシナリオでこの機能が最も有益なのかをご紹介します。

{% include youtube.html id="6oX3HTDI8_A" %}

<details class="transcript2">
<summary> ▶日本語字幕 </summary>
<div class="content">
今日のデータ主導の世界では、API の管理がこれまで以上に重要になっています。リッチでデータ集約的な環境では、他の多くのアプリケーションと統合されていることが多いからです。
<br>
InterSystems API Manager (IAM)は、InterSystems IRIS のアプリケーションによって消費、公開される API とマイクロサービスをコントロールすることができます。
<br>
IAMは、ダウンストリームとアップストリームのアプリケーション間の API ゲートウェイとして機能します。
<br>
トラフィックの監視とトラフィックの制御という2つの主要な分野で大きなメリットをもたらします。
<br>
InterSystems IRIS の API を他の様々なアプリケーションに公開するシナリオを考えてみましょう。
<br>
InterSystems API Manager を使用することでゲートウェイを経由して公開されている API へ のトラフィックを効率的に監視することができます。
<br>
どの API が呼び出されているのか？どのくらいの頻度で呼び出されているのか？どのような開発者やアプリケーションがそれらを呼び出しているのか、またこれらの答えにパターンや傾向はあるのか？
<br>
IAM を使ってこれらの重要な要素を監視するのは簡単で直感的です。
<br>
3.3、3.5、4.0という3つの異なるバージョンの FHIR API を公開している場合を考えてみよう。トラフィックを監視しなければ、誰がどの API を使っているのかわからないかもしれません。
<br>
IAM を使用してこれを監視することで使用されていない API をオフラインにしたり、別の API で特に大量のトラフィックを処理するように調整したりできることに気づくかもしれません。
<br>
モニタリングの結果に基づいて、これらの API コールのトラフィックを制御し始めることができます。
<br>
ガブリエルとエミリアという 2 人の開発者がいて、InterSystems IRIS 内で公開している 3 つの異なる API（1つは請求、1つはラボ、1つは薬局）を頻繁に呼び出すとします。
<br>
IAM を使用すると、これらのダウンストリームの開発者やアプリケーションから、アップストリームに公開された API へのトラフィックを制御できます。例えば、ガブリエルの API コールを 1 時間あたり 10 回に制限したり、エミリアに請求 API だけをコールさせたりすることができます。
<br>
この機能は、API を外部に公開している場合に特に重要です。利用者に社外の開発者やアプリケーションが含まれる場合、潜在的な脆弱性が生じるからです。
<br>
IAM はこの種のトラフィックを制御し、外部のリスクから保護することができます。
<br>
ダウンストリームのアプリケーションにとっては、ほとんどすべてがシンプルで透過的です。もちろん、必要に応じてダウンストリーム・アプリケーションに追加のセキュリティ強化を加えることもできます。
<br>
ワークフローは若干異なりますが、IAM は、InterSystems IRIS のアプリケーションが外部で利用可能な API を消費する逆のケースでも役立ちます。
<br>
InterSystems API Manager があなたの環境でどのように機能するかを考えるとき、一般的には 3 つの基本的な要素に集約されます。
<br>
API へのアクセスを要求するコンシューマ（通常は下流のユーザまたはアプリケーション）。
<br>
そしてルートです。IAM は送られてきたリクエストを解析しリクエストされたプロトコル、サーバー、アプリケーション、リソースなどの要素を特定します。その結果に基づいてリクエストを適切な API に転送します。
<br>
最後に、デスティネーション、つまりサービスと呼ばれるものがあります。これは、リクエストが転送される上流のシステムまたは API (ほとんどの例では InterSystems IRIS 内) です。
<br>
ロードバランシングのために複数のターゲットにマッピングしたり、異なる方法でターゲットを設定したりと設定はより複雑になります。しかし本質的には、これは IAM によるAPI 管理の標準的なワークフローです。

今日のデータ主導の世界で違いを生み出す強力なアプリケーションを構築するには、API と API へのトラフィックを管理する必要があります。
<br>
InterSystems API Manager を使えば、これは簡単かつ直感的に実現できます。
</div>
</details>
<br>


✅ 記事：<a href="https://jp.community.intersystems.com/node/493416" target="_blank">ゼロから使いこなす IAM（InterSystems API Manager）</a>
<br>

> **英語のオンラインラーニングもあります**
>- <a href="https://learning.intersystems.com/course/view.php?id=2571" target="_blank">Hands-On with InterSystems API Manager for Developers</a>
{: .block-tip}
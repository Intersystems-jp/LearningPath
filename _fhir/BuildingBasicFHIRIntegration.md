---
title: FHIRアプリケーション構築の基礎
date: 2024-12-03
permalink: BuildingBasicFHIRIntegration.html
layout: post
---
<!-- 
>オリジナル：[Building Basic FHIR Integrations with InterSystems](
https://learning.intersystems.com/course/view.php?id=1959)-->

このパスでは、InterSystems IRIS for Health™ または HealthShare® Health Connect を使用して HL7® FHIR® アプリケーションを構築するための基本を学習します。

最初にFHIR エンドポイントを設定し、FHIR リソースの入力や変換方法を学習します。また、API を管理し、クライアントアプリケーションから FHIR リソースを参照する方法も学習します。

はじめて FHIR について学習する方は、<a href="IntroFHIRStandard.html" target="_blank">HL7 FHIRとは</a> からはじめてみてください。

InterSystems 製品を利用したシステム統合処理についての前提知識を確認される場合は以下コンテンツをご利用ください。

- InterSystems製品の基本構造について

    ✅ 記事：<a href="https://jp.community.intersystems.com/node/478601" target="_blank">【はじめての InterSystems IRIS】セルフラーニングビデオ：基本その2：InterSystems IRIS で開発をはじめよう！</a>

    {% include youtube-list.html id="ID6ImJTgJRk" list="PLzSN_5VbNaxBPaSSINLzv-CkDJy00bOSQ&index=3" %}
<br>
- InterSystems Interoperability(相互運用性)概要を確認する

    以下のビデオの12分以降をご覧ください。

    {% include youtube-list.html id="vo12UnH-c-s" list="PLzSN_5VbNaxD-r8wU4LHwLwGSzUjrffEX&index=1&t=1203s" %}
<br>
- InterSystems Interoperability（相互運用性）をシリーズ記事のサンプルコードを見ながら学習する

    - <a href="https://jp.community.intersystems.com/node/483021" target="_blank">【はじめてのInterSystems IRIS】Interoperability（相互運用性）を使ってみよう！</a>

    - <a href="https://jp.community.intersystems.com/node/483036" target="_blank">【はじめてのInterSystems IRIS】Interoperability（相互運用性）：動作の仕組みを知ろう</a>

    - <a href="https://jp.community.intersystems.com/node/483041" target="_blank">【はじめてのInterSystems IRIS】Interoperability（相互運用性）：プロダクションとは</a>


> **英語のオンラインコースもあります**
>- <a href="https://learning.intersystems.com/course/view.php?name=Integration%20Architecture" target="_blank">オンラインコース（英語）：Integration Architecture（英語）</a>
{: .block-tip}

---

[1. <img src="./assets/icons/FHIR/Integration1.png" width="40%"/>](#1-)

[2. <img src="./assets/icons/FHIR/Integration2.png" width="40%"/>](#2-)

[3. <img src="./assets/icons/FHIR/Integration3.png" width="40%"/>](#3-)

[4. <img src="./assets/icons/FHIR/Integration4.png" width="40%"/>](#4-)

[5. <img src="./assets/icons/FHIR/Integration5.png" width="40%"/>](#5-)

[6. <img src="./assets/icons/FHIR/Integration6.png" width="40%"/>](#6-)

[7. <img src="./assets/icons/FHIR/Integration7.png" width="40%"/>](#7-)

---
## 1. <img src="./assets/icons/FHIR/Integration1.png" width="70%"/>

最初に、医療用文書の標準フォーマットとして、また医療相互運用性にとって FHIR が重要である理由を学び、InterSystems IRIS for Health がどのように FHIR インテグレーションとアプリケーション開発をサポートしているかを確認しましょう。

- ビデオ（日本語）：HL7® FHIR® × InterSystems IRIS for Health

    {% include youtube-list.html id="rbIF4z8xRIY" list="PLzSN_5VbNaxBu4kMgZrK5iGi-GIGNxvpu&index=1" %}
<br>
- ビデオ（日本語字幕）:FHIR - 未来のために設計された医療データスタンダード "FHIR A Healthcare Data Standard Designed for the Future"

    {% include youtube.html id="gNjlaARboYk" %}
<br>
- <a href="https://docs.intersystems.com/irisforhealthlatestj/csp/docbook/DocBook.UI.Page.cls?KEY=HXFHIR_server_arch" target="_blank">ドキュメント：FHIRサーバー：アーキテクチャ</a>

> **英語ビデオもあります**
>- <a href="https://learning.intersystems.com/course/view.php?id=1077" target="_blank">What is FHIR？</a>
{: .block-tip}

---
## 2. <img src="./assets/icons/FHIR/Integration2.png" width="70%"/>

IRIS for Health は、FHIR データを格納する FHIR エンドポイントを作成でき、他の FHIR プロファイルをサポートするように構成することができます。

InterSystems IRIS for Health が受信する HL7® CDA®、CSV、HL7® V2、XML データを FHIR フォーマットに変換する方法をご覧ください。

- <a href="https://docs.intersystems.com/irisforhealthlatestj/csp/docbook/DocBook.UI.Page.cls?KEY=HXFHIR_server_install" target="_blank">ドキュメント：FHIR サーバのインストールと構成

- <a href="https://learning.intersystems.com/course/view.php?id=1721" target="_blank">演習環境付き体験（英語）：Importing FHIR Packages into the InterSystems IRIS for Health Server</a>


- <a href="https://jp.community.intersystems.com/node/495321" target="_blank">ビデオ：FHIR プロファイル</a>

{% include youtube-list.html id="B-B6ge_0nHg" list="PLzSN_5VbNaxBu4kMgZrK5iGi-GIGNxvpu&index=8" %}
<br>
- 参考：<a href="https://jp.community.intersystems.com/node/491836" target="_blank">FHIR R4 リソースリポジトリを簡単にお試しいただける開発環境テンプレートのご紹介</a>


---
## 3. <img src="./assets/icons/FHIR/Integration3.png" width="70%"/>

InterSystems IRIS for Health を使用して、Summary Document Architecture（SDA）と組み込みの変換を使用して、受信データを FHIR フォーマットに変換します。

- ビデオ：他形式データからFHIR への変換

{% include youtube-list.html id="dsB3cS333LI" list="PLzSN_5VbNaxBu4kMgZrK5iGi-GIGNxvpu&index=9" %}
<br>

> **英語ビデオやオンラインコース**
>- <a href="https://learning.intersystems.com/course/view.php?id=1744" target="_blank">ビデオ（英語）：Converting Legacy Data to HL7 FHIR R4 in InterSystems IRIS for Health</a>
>
>- <a href="https://learning.intersystems.com/course/view.php?id=2128" target="_blank">ビデオ(英語)：What is SDA?</a>
>
>- <a href="https://learning.intersystems.com/course/view.php?name=FHIRTransformations" target="_blank">オンラインコース(英語)：Transforming Data into the HL7 FHIR Format</a>
>
>    InterSystems IRIS for Health™ または HealthShare® Health Connect を使用して、医療システム間のデータ交換に一般的に使用されている HL7® FHIR® フォーマットにデータを変換する方法をお試しいただけます。
>    
>    また、後半では、ダイナミックオブジェクトを使用して FHIR データを操作する方法を学びます。このコースを通して、HL7 V2 リソースを FHIR フォーマットに変換する方法を体験できます。
{: .block-tip}


- この他に、InterSystems の内部形式であるSDAを使用せず、<a href="https://github.com/Intersystems-jp/JSONTemplate" target="_blank">JSONTemplateエンジン</a> を使い、FHIRリソースのような複雑なJSONフォーマットを簡単に生成する方法も用意しています。

> **このテンプレートエンジンは、FHIRに限らず複雑なJSONフォーマットを生成するのに役立つエンジンです。**
>
>参考記事：<a href="https://jp.community.intersystems.com/node/551396" target="_blank">複雑なJSONの生成に便利な「JSONテンプレートエンジン」の使い方ご紹介</a>
{: .block-tip}

JSONテンプレートエンジンを利用して FHIR リソースの JSON を生成される方法については、以下ビデオで説明しています。

{% include youtube-list.html id="H4LzOV-Tfzg" list="PLzSN_5VbNaxB39_H2QMMEG_EsNEFc0ASz" %}
<br>

- 講師付きトレーニングコースで使用している <a href="https://github.com/iijimam/Training-FHIRFacadeEx" target="_blank">CSVからFHIRリソースを作成するFHIRファサード</a> のサンプルコードを公開しています。

    JSON テンプレートエンジンを利用して、どのように CSV から FHIR リソース変換しているか、については、<a href="https://github.com/iijimam/Training-FHIRFacadeEx/blob/master/readme.md" target="_blank">README</a> をご参照ください。

> **上記内容をカバーする講師付きトレーニングもご提供しています**
>- CSV から FHIR への変換
>    
>   JSON テンプレートエンジンを利用した変換方法を習得できるコースです。
    作成例として、CSV で入力された情報から FHIR リソースを作成し、IRIS に用意したFHIRリポジトリに登録する流れを体験します。
>
>- SSMIX2 から FHIR への変換
>
>    SDA 経由の変換を体験できるコースです。
>
> 教育サービス担当まで下記ページ末尾のお問い合わせフォームからご依頼ください。
> <a href="https://www.intersystems.com/jp/course-offerings/" target="_blank">問い合わせフォーム</a>
{: .block-warning}

---
## 4. <img src="./assets/icons/FHIR/Integration4.png" width="70%"/>

CRUD インタラクションの実行-クライアントアプリケーションからの FHIR リソースの検索や、REST クライアントからの操作のテストなどを確認できます。

- 日本語ビデオ：FHIR+IRIS for Health 101（18分ごろからご覧ください）

{% include youtube-list.html id="S7PV3RIpMUM" list="PLzSN_5VbNaxBu4kMgZrK5iGi-GIGNxvpu&index=10&t=1077" %}


- ビデオ：REST クライアントから FHIR R4 リソースリポジトリにアクセスする例

{% include youtube-list.html id="AYz6d7MxXos" list="PLzSN_5VbNaxBu4kMgZrK5iGi-GIGNxvpu&index=11" %}
<br>

- <a href="https://docs.intersystems.com/irisforhealthlatestj/csp/docbook/DocBook.UI.Page.cls?KEY=HXFHIR_server_arch_supported_interactions" target="_blank">ドキュメント：相互作用</a>

> **英語ビデオもあります**
>- ビデオ：Searching for FHIR Resources in InterSystems IRIS for Health
{% include youtube.html id="l-RlCMANgN8" %}
<details class="transcript2">
<summary> ▶日本語字幕 </summary>
<div class="content">
このビデオでは、FHIR リソースを検索する方法を説明し、FHIR リソースを検索するときに使用する検索パラメータのタイプを紹介します。
<br>
患者の記録を保存するために InterSystems IRIS for Health を使用している地元の病院の開発者 John を追います。
<br>
先月、彼は FHIR の入門コースを受講したので、FHIR を使って患者データを検索して保存する方法についてある程度の知識を持っています。
<br>
最近、彼は出身地に基づいて患者を整理する仕事を任されましたので、彼は FHIR リソースの検索方法を知る必要があります。
<br>
FHIR における検索とは、一連のフィルタ条件を満たすリソースを選択または検索することを意味します。このため、ほとんどの検索リクエストは GET メソッドを使用しリクエストの最後にクエスチョンマーク記号 ? を利用して検索パラメーターを指定します。
<br>
John が FHIR リソースの検索を実行するために理解する必要があるパラメータにはいくつかの種類があります。まず、最も単純なパラメータタイプである標準パラメータから説明します。標準パラメータには、検索する条件が 1 つだけ含まれています。
<br>
例えば、John は Carter という姓を持つすべての患者を検索する必要があります。これを行うには、条件を family=carter と指定する必要があります。
<br>
送信をクリックします。ご覧のように、Carter という姓の患者の結果が表示されます。
<br>
また、& 構文を使用して複数の条件を組み合わせて検索することもできます。
<br>
例えば、検索パラメータに &gender=male を追加すると、Carter という姓の男性患者のみが返されます。
<br>
2 つの条件のうち 1 つだけが真である必要がある場合（「OR」条件）には、代わりにカンマ区切り記号を使用します。この場合、Carter または Jones のいずれかの姓を持つ患者が検索されます。OR条件は、同じパラメータ内でのみ機能することに注意してください。つまり、Carter という姓、または male という性別を持つ人を検索することはできません。
<br>
検索できるものに満足した John は、次に検索するための条件フィールドに入れる正確な値がわからない場合、どうすればよいかと考えます。その場合、修飾子と比較子という 2 つのオプションが利用できます。
<br>
検索でフィルターする値が文字列の場合、修飾子を使うことができます。例えば、contains という修飾子を使えば、JO を含む姓を持つレコードだけを絞り込むことができます。ここでわかるように、この検索結果には、姓に Jones と Johnson を持つ両方の患者のデータが含まれます。
<br>
一方、フィルタする値が数値または日付の場合は、greater than や less than などの比較子を使用することで解決できます。例えば、John は、比較子 greater than を追加することで、2000 年以降に生まれたすべての患者を見つけることができます。再度検索を実行すると、今度は 2000 年以降に生まれた患者のみがリストに表示されます。
<br>
最後になりますが、John は検索プロセス中のエラーの処理方法を知っておく必要があります。検索に失敗すると、サーバは OperationOutcome を返します。
<br>
これは、検索パラメータの形式が正しくないか、存在しないリソースを参照しているか、不正な修飾子が使用されている可能性があるためです。
<br>
検索結果が空でもエラーではないことに注意することが重要である。
<br>
John は、InterSystems IRIS for Health に保存されている FHIR リソースを検索する新しい機能が患者の出身地に基づいて患者を整理したり、生年月日に基づいて患者を検索したりするような業務に非常に役立っていると感じています。
<br>
IRIS for Health で必要な FHIR リソースを検索する方法を学んだところです。標準パラメータ、複合パラメータ、修飾子の使用、比較対象など、各検索パラメータタイプの利点を理解することで FHIR リソースを検索する際に状況に応じて最適なものを選択できるようになりました。
<br>
FHIR Resource List にアクセスしてパラメータのリストを参照するか、ドキュメントを読んで InterSystems IRIS for Health でサポートされている修飾子を確認してください。
</div>
</details>
{: .block-tip}

---
## 5. <img src="./assets/icons/FHIR/Integration5.png" width="70%"/>
新しい FHIR サーバーをセットアップする際に、OAuth2.0 でエンドポイントを保護する方法を学習します。

- <a href="https://docs.intersystems.com/irisforhealthlatestj/csp/docbook/DocBook.UI.Page.cls?KEY=HXFHIR_server_auth_oauth" target="_blank">ドキュメント：OAuth2.0認証

- <a href="https://docs.intersystems.com/irisforhealth20243/csp/docbook/DocBook.UI.Page.cls?KEY=HXFHIR_server_auth#HXFHIR_server_auth_oauth" target="_blank">ドキュメント（英語）：OAuth FHIR Client Quickstart</a>

    InterSystems サーバーに用意する FHIR リソースサーバーと OAuth 2.0 認証サーバーの接続のための設定を簡単に作成する方法も用意されています（バージョン2025.1以降）

- <a href="https://learning.intersystems.com/course/view.php?id=1787" target="_blank">ビデオ（英語）：Configuring the InterSystems Web Gateway</a>


---
## 6. <img src="./assets/icons/FHIR/Integration6.png" width="70%"/>

InterSystems API Manager を使用して FHIR エンドポイントへのトラフィックを制御する方法と、トラブルシューティングのテクニックを紹介します。

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

- <a href="https://jp.community.intersystems.com/node/493416" target="_blank">ゼロから使いこなす IAM（InterSystems API Manager）</a>



- <a href="https://learning.intersystems.com/course/view.php?id=1654" target="_blank">体験環境付き演習（英語）：Building FHIR Applications with InterSystems API Manager

    - <a href="https://learning.intersystems.com/pluginfile.php/38823/mod_resource/content/10/FHIRExerciseGuide%20%281%29.pdf" target="_blank">演習資料PDF</a>

        InterSystems API Manager を使用して API を表示し、HL7® FHIR® アプリケーションを作成して、FHIR リクエストを監視する方法について説明します。

        この実習を修了するまでに、以下のことができるようになります：

        - InterSystems API Manager を使用して API を表示し、FHIR 要求のテスト
        - REST クライアントを使用して、InterSystems IRIS for Health™ に FHIR リクエストを作成
        - FHIR アプリケーションを InterSystems IRIS for Health に接続させる
        - API Manager 開発者ポータルで統計を表示して API 呼び出しを監視

- <a href="https://docs.intersystems.com/irisforhealthlatestj/csp/docbook/DocBook.UI.Page.cls?KEY=HXFHIR_server_debugMaintain" target="_blank">ドキュメント：FHIR サーバのデバッグ</a>


---
## 7. <img src="./assets/icons/FHIR/Integration7.png" width="70%"/>

最後の演習では、サンプルのフロントエンドを使って、完全な FHIR アプリケーションを構築するします。

- <a href="https://learning.intersystems.com/course/view.php?name=FHIR%20Resource%20Repository" target="_blank">[体験環境付き演習（英語）：Working with the FHIR Resource Repository</a>

    Syntheaデータ入れてRESTクライアントからのアクセスを試します。また、簡単な Web ページを利用して FHIR リポジトリからの検索結果を表示させる内容を体験できます。
    

> **<a href="https://jp.community.intersystems.com/node/491836" target="_blank">FHIR R4 リソースリポジトリを簡単にお試しいただける開発環境テンプレートのご紹介</a> で提供しているコンテナ環境を利用して同様の内容をお試しいただけます。**
{: .block-warning}

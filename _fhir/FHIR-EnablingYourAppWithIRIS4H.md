---
title: アプリケーションを FHIR 対応にする
date: 2024-12-02
permalink: FHIR-EnablingYourAppWithIRIS4H.html
layout: post
---
<!-- 
> オリジナル[FHIR-Enabling Your Applications with InterSystems IRIS for Health](https://learning.intersystems.com/course/view.php?id=2323) -->

InterSystems IRIS for Health™ を使用して、FHIR ファサード を作成することで、ヘルスケア・アプリケーションが HL7® FHIR® フォーマットでデータを送受信できるようなります。

このラーニングパスでは、以下の方法を学習します。

- RESTを使用して、EHR のような外部の FHIR サーバーと対話するようにアプリケーションをセットアップする。
- 標準的なヘルスケアデータ形式のメッセージを FHIR 形式に変換する。
- FHIR 相互運用性アダプタ を使用してFHIR ファサードを設定する。


[1. <img src="./assets/icons/FHIR/Second1.png" width="40%"/>](#1-)

[2. <img src="./assets/icons/FHIR/Second2.png" width="40%"/>](#2-)

[3. <img src="./assets/icons/FHIR/Second3.png" width="40%"/>](#3-)

[4. <img src="./assets/icons/FHIR/Second4.png" width="40%"/>](#4-)

[5. <img src="./assets/icons/FHIR/Second5.png" width="40%"/>](#5-)

---
## 1. <img src="./assets/icons/FHIR/Second1.png" width="70%"/>

FHIR の基本的な知識について確認するため、以下のビデオをご参照ください。

このビデオは、国際モダンホスピタルショウ2022 インタ―システムズブースのミニシアターで開催された　一般社団法人 日本IHE協会　理事　接続検証委員長　塩川 康成 様　によるご講演ビデオです。

>国際モダンホスピタルショウ　インタ―システムズブースのミニシアターでのご講演内容全般については、<a href="https://www.youtube.com/@InterSystemsJapan/playlists" target="_blank">InterSystems Japan YouTubeチャンネル</a> にて公開しております。

{% include youtube-list.html id="_Qgv9WqrN6k" list="PLgFt3CvX3OePAiRdrL8GmMzKNiCG_BJqP" %}
<br>

> **英語ビデオもあります**
>- <a href="https://learning.intersystems.com/course/view.php?name=What%20is%20FHIR" target="_blank">ビデオ（英語）:What Is FHIR?</a>
{: .block-tip}

---
## 2. <img src="./assets/icons/FHIR/Second2.png" width="70%"/>

アプリケーションの FHIR 化に必要なアーキテクチャをご紹介します。

- <a href="https://learning.intersystems.com/course/view.php?id=2137" target="_blank">ビデオ（英語）：FHIR Facade Architecture Overview</a>

    <details class="transcript2">
    <summary> ▶日本語字幕 </summary>
    <div class="content">
    近年、HL7 FHIR（Fast Healthcare Interoperability Resources）は、医療システム間で患者データを交換するためのトップスタンダードとなっています。
<br>
    古いアプリケーションを使用している医療ネットワークや施設にとって、FHIR にまつわる現代の市場や規制の要件を満たすことは困難であり、FHIR 標準の活用をすぐに開始できるインフラを持っていない可能性があります。
<br>
    例えば、すべてのアプリケーションが FHIR 標準を使用してデータを交換するために完全に書き直せるわけではありませんし、施設は完全な FHIR リポジトリを持っていなかったり、導入できなかったりします。
<br>
    幸いなことに、InterSystems のテクノロジを使用して、FHIR リポジトリのファサードとして機能するアーキテクチャを作成することができるため、既存のアプリケーションで FHIR データを使用するメリットを享受しながら、完全な手戻りを回避することができます。
<br>
    FHIR データで動作するようにアプリケーションを準備することは、いくつかの理由から非常に重要です。連邦規制がそれを義務付けるかもしれないし、市場のニーズがそれを要求するかもしれないし、他のシステムとの統合がそれを必要とするかもしれない。
<br>
    FHIR Facade アーキテクチャを使用するアプリケーションでは、患者データは 2 つの場所からアクセスできます。まず、InterSytsems のデータベースから直接データにアクセスできます。または、別のデータベースまたはサービス、たとえば MySQL データベースや REST API からデータにアクセスすることもできます。アーキテクチャはそれぞれ若干異なりますが、どちらのセットアップも可能です。
<br>
    MySQL データベースに患者データを格納している医療アプリケーションを考えてみよう。このアプリケーションは何年も前のものなので、FHIR データソースで動作するように書き直すには多くの時間と労力が必要になる。
<br>
    また、この医療ネットワーク内のアプリケーションのコンシューマー（新しい放射線科施設など）は、このアプリケーションに患者データのリクエストを行う準備ができており、その見返りとして FHIR リソースを期待しています。
<br>
    アプリケーションを書き直す代わりに、IntrSystems の技術を使って、FHIR リソースをネットワーク内の他者と共有できるようにするためのブリッジとして機能する FHIR サーバを作成することができます。
<br>
    コードによってカスタム FHIR インタラクションを構築する方法と、InterSystems IRIS for Health または HealthShare 内の FHIR 相互運用性コンポーネントを使用してカスタム・データ・パイプラインを構築する方法です。
<br>
    カスタム FHIR インタラクションは、FHIR InteractionsStrategy クラスにあらかじめ組み込まれた RESTful フックを使用して構築できます。より低コードでグラフィカルなアプローチでは、インターシステムズ製品の統合機能を使用してカスタム・データ・パイプラインを構築できます。
<br>
    FHIR サーバーは、統合コンポーネントを利用してRESTエンドポイントを処理することができ、医療ネットワーク内の多数のダウンストリームシステムからのリクエストを受け取ることができます。
<br>
    FHIR Bundle の形で患者記録のデータを期待する放射線科システムからのリクエストを考えてみよう。
<br>
    適切なアーキテクチャがあれば、FHIR サーバーはこのリクエストを受信し、外部データベースまたは API サービスから患者のデータを取得することができる。
<br>
    その後、データを元のフォーマットから FHIR 標準に変換することができる --それがリレーショナルテーブルからのデータであれ、JSON のような他のフォーマットであれ。
<br>
    患者データの FHIR 標準への変換は、このアーキテクチャの重要な部分の一つです。
<br>
    データを変換するための 1 つの選択肢は、SDA（Summary Document Architecture）を中間フォーマットとして使用し、元のフォーマットから FHIR にデータを変換することです。
<br>
    FHIR データをさらに操作する必要がある場合、ダイナミック・オブジェクトは、InterSystems IRIS for Health または HealthShare 内で JSON データ構造を利用するコードベースのアプローチを提供します。患者データを FHIR 標準に変換するプロセスの詳細については、このページに記載されているその他の学習コンテンツを参照してください。
<br>
    データが変換されると、応答が FHIR Bundle の形で要求元のアプリケーションに返送されます。
<br>
    患者データが MySQL のような外部データベースではなく、InterSystems データベースに直接保存されている場合プロセスは非常に似ています。主な違いは、患者データを取得するアウトバウンドビジネスオペレーションにネットワークコンポーネントがないことです。代わりに、データは InterSystems データベースから取得されそのフォーマットは変換のために適切にマッピングされます。
<br>
    まとめると、このアーキテクチャは、既存のアプリケーションが FHIR データとシームレスに連携することを可能にし、ネットワーク内のすべてのアプリケーションに価値を提供することができます。
    </div>
    </details>
    <br>

    アプリケーションが HL7® FHIR® リクエストに応答できるように、FHIR ファサードアーキテクチャをセットアップする方法を確認できます。
    
    このアーキテクチャを使用することで、InterSystems サーバーを FHIR サーバーのように扱うことができ、FHIR リポジトリを持たない環境でも FHIR リクエストをサポートできるようになります。

---
## 3. <img src="./assets/icons/FHIR/Second3.png" width="70%"/>

InterSystems の data platform で REST エンドポイントを設定し、REST を使用した FHIR 相互運用性アダプタを使用して外部の FHIR サーバーとやり取りする方法を確認します。

また、返送された FHIR リソースを FHIR レスポンス・メッセージに設定し REST 経由で FHIR データを返送する方法を演習します。


- <a href="https://docs.intersystems.com/irisforhealthlatestj/csp/docbook/DocBook.UI.Page.cls?KEY=HXFHIR_fhir_adapter" target="_blank">ドキュメント：FHIR相互運用アダプタ</a>

- <a href="https://jp.community.intersystems.com/node/479596" target="_blank">記事：【はじめてのInterSystems IRIS】セルフラーニングビデオ：アクセス編：（REST）APIファーストで作成するRESTディスパッチクラス</a>

    {% include youtube-list.html id="SwquEq1fjTk" list="PLzSN_5VbNaxBPaSSINLzv-CkDJy00bOSQ" %} 
<br>
- <a href="https://jp.community.intersystems.com/node/559356" target="_blank">記事：REST経由で情報を入力する場合の Interoperability（相互運用性機能）のサンプル</a>　
<br>

> **英語ですが、オンラインコースもあります**
>- <a href="https://learning.intersystems.com/course/view.php?name=FHIRTransformations" target="_blank">オンラインコース（英語）：Transforming Data into the HL7 FHIR Format</a>
{: .block-tip}

- <a href="https://learning.intersystems.com/course/view.php?name=FHIRStarterDemo" target="_blank">ビデオ（英語）:Converting Legacy Data to HL7 FHIR R4 in InterSystems IRIS for Health</a>


    このビデオでは、InterSystems IRIS® for Health の Summary Document Architecture（SDA）を介して、様々なレガシーデータフォーマットを HL7® FHIR® 標準に変換する方法をご紹介します。
    
    ビデオでは、InterSystems IRIS for Health のビジネスロジックと相互運用性機能を使用して、入力されるHL7® CDA®、CSV、HL7® V2、XML データタイプを FHIR に変換します。
    
    このビデオで紹介するデモアプリケーションをダウンロードできます。
    
    <a href="https://github.com/intersystems/Samples-SUREFHIR" target="_blank">FHIRStarter Demo GitHub</a> リポジトリにアクセスし、コンテナの実行手順に従ってください。また、デモを実行するにはDockerのインストールが必要です。

> **FHIRファサードを体験できる講師付きトレーニングコースをご提供しています**
>
> 教育サービス担当まで下記ページ末尾のお問い合わせフォームからご依頼ください。
> <a href="https://www.intersystems.com/jp/course-offerings/" target="_blank">問い合わせフォーム</a>
{: .block-warning}

---
## 4. <img src="./assets/icons/FHIR/Second4.png" width="70%"/>

インターシステムズの標準データフォーマットである SDA について学び、SDA を使用して標準的なヘルスケアフォーマットのデータを FHIR フォーマットに変換する方法を学習します。

- <a href="https://docs.intersystems.com/irisforhealthlatestj/csp/docbook/DocBook.UI.Page.cls?KEY=HXSDA_ch_sda" target="_blank">ドキュメント：SDAドキュメント</a>

- <a href="https://learning.intersystems.com/course/view.php?name=FHIRFacadeInteropAdapter" target="_blank">体験環境付き演習（英語）:Creating a Simple FHIR Facade</a>

    InterSystems IRIS® for Health のインスタンスを使用して、FHIR Facade アーキテクチャを作成および構成し、システムが HL7® FHIR® リクエストを受け入れ、データがこの形式で元々保存されていない場合でも FHIR データを返せるようにします。
    
    FHIR Facade を作成するには、FHIR 相互運用性アダプタを使用します。これは、特別なビジネスホストを使用してプロダクションで FHIR リクエストを処理する新しい相互運用性 REST エンドポイントを作成します。
    
    このプロダクションを使用して、データの検索と変換を促進し、要求されたデータを返すことができます。
    この演習では、内部形式でEMRデータを保存する医療施設の FHIR Facade を作成します。
    
    この施設では、患者の詳細を JSON 形式で返す REST API が設定されていますが、FHIR 形式の患者データのリクエストを受けています。


---
## 5. <img src="./assets/icons/FHIR/Second5.png" width="70%"/>

### FHIR JSONフォーマットを簡単に生成できる JSON Templateエンジンについて

<a href="https://github.com/Intersystems-jp/JSONTemplate" target="_blank">JSONTemplate エンジン</a> を利用して複雑な JSON フォーマットを簡単に生成することができます。

> **このテンプレートエンジンは、FHIR に限らず複雑な JSON フォーマットを生成するのに役立つエンジンです。**
>
>参考記事：<a href="https://jp.community.intersystems.com/node/551396" target="_blank">複雑なJSONの生成に便利な「JSONテンプレートエンジン」の使い方ご紹介</a>
{: .block-tip}

JSON テンプレートエンジンを利用して FHIR リソースの JSON を生成される方法については、以下ビデオで説明しています。

{% include youtube-list.html id="H4LzOV-Tfzg" list="PLzSN_5VbNaxB39_H2QMMEG_EsNEFc0ASz" %}
<br>

### JSONテンプレートエンジンを利用したFHIRファサードの例

講師付きトレーニングコースで使用している <a href="https://github.com/iijimam/Training-FHIRFacadeEx" target="_blank">CSVからFHIRリソースを作成するFHIRファサード</a> のサンプルコードを公開しています。

JSON テンプレートエンジンを利用して、どのように CSV から FHIR リソース変換しているか、については、<a href="https://github.com/iijimam/Training-FHIRFacadeEx/blob/master/readme.md" target="_blank">README</a> をご参照ください。

> **FHIRファサードを体験できる講師付きトレーニングコースをご提供しています**
>
> 教育サービス担当まで下記ページ末尾のお問い合わせフォームからご依頼ください。
> <a href="https://www.intersystems.com/jp/course-offerings/" target="_blank">問い合わせフォーム</a>
{: .block-warning}

### FHIR Object Model の利用

以下ビデオでは、バージョン 2024.1から追加された FHIR オブジェクトモデルを利用して FHIR リソースを作成する例をご紹介しています。

{% include youtube-list.html id="onO1oJwFpeQ" list="PLzSN_5VbNaxBu4kMgZrK5iGi-GIGNxvpu" %}
<br>

> **体験環境つき演習（英語）もあります**
>
>- <a href="https://learning.intersystems.com/course/view.php?id=2274" target="_blank">体験環境付き演習（英語）：Creating a Simple FHIR Facade</a>
>
>    InterSystems IRIS for Health™ のインスタンスを使用して、FHIR ファサードアーキテクチャを作成および構成することで、システムが HL7® FHIR® リクエストを受け入れ、データが元々この形式で保存されていない場合でも FHIR データとして返すことができます。
>
>    FHIR ファサードを作成するには、FHIR 相互運用性アダプタを使用します。
>    
>    演習の中では、特別なビジネスホストを使用してプロダクションで FHIR リクエストを処理する新しい相互運用性 REST エンドポイントを作成します。
>    
>    このプロダクションは、データの検索と変換を簡単にし、要求された FHIR 形式のデータを返送するために利用できます。
>
>    演習は、内部形式で EMR データを保存する医療施設の FHIR ファサードを作成します。
>    この施設では、患者の詳細を JSON 形式で返す REST API が設定されていて、FHIR 形式の患者データのリクエストを受けている状況です。
{: .block-tip}
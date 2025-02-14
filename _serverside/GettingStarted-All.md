---
title: InterSystems 製品で開発を始める
date: 2024-12-02
permalink: /GettingStarted-All.html
layout: post
---

InterSystems IRIS® data platform の利用可能なツールや InterSystems IRIS または IRIS for Health を使用したアプリケーションのセットアップと開発の基本について学習できるパスです。

これから InterSystems 製品を利用される開発者を対象に構成されています。

学習項目詳細は以下の通りです。

[1. <img src="./assets/icons/1-IRIS.png" width="40%"/>](#1-)

[2. <img src="./assets/icons/2-serversideapp-better-dicision.png" width="40%"/>](#2-)

[3. <img src="./assets/icons/3-integration.png" width="40%"/>](#3-)

[4. <img src="./assets/icons/5-access-multilanguage.png" width="40%"/>](#5-)

[5. <img src="./assets/icons/6-APIManagement.png" width="40%"/>](#6-)

[6. <img src="./assets/icons/7-Analytics.png" width="40%"/>](#7-)

[7. <img src="./assets/icons/8-performance.png" width="40%"/>](#8-)


このパスの他に、以下講師付きクラスルームトレーニングコースの受講を推奨いたします。

- <a href="https://www.intersystems.com/jp/intersystems-sql/" target="_blank">InterSystems SQL</a>
- <a href="https://www.intersystems.com/jp/intersystems-object/" target="_blank">InterSystems Object</a>
    - このコースは**ObjectScriptを学習するコースではありません。**
    - InterSystems製品でオブジェクト指向プログラミングを行う方法、また永続クラス定義の作成、オブジェクト操作方法を学習するためのコースです。
- <a href="https://www.intersystems.com/jp/intersystems-server-system-administration/" target="_blank">InterSystems Server システム管理1</a>
- <a href="https://www.intersystems.com/jp/intersystems-server-system-administration-2/" target="_blank">InterSystems Server システム管理2：セキュリティ管理編</a>


---

## 1. <img src="./assets/icons/1-IRIS.png" width="70%"/>

InterSystems IRIS®データ・プラットフォームは、信頼性の高い統一プラットフォームで重要なアプリケーションを迅速に開発・デプロイすることを可能にします。

- InterSystems IRISとは（日本語字幕入りビデオ）

    {% include youtube.html id="w2OeWx3WNOs" %}

<details class="transcript2">
<summary> ▶日本語字幕 </summary>
<div class="content">
InterSystems IRIS は統合データ プラットフォームです。
<br>
大規模かつ拡張可能なデータベース、組み込みの分析機能、統合／相互運用性ツール、そして自動化されたメカニズムによりデプロイを容易にします。
<br>
これらのテクノロジーは、貴社のビジネスに重要なアプリケーションの開発とデプロイをさらに迅速化します。
<br>
中核を成す InterSystems IRIS データベースは、高パフォーマンスで大幅な拡張が可能です。
<br>
きわめて効率的なデータ構造により高速化と柔軟性を実現します。
<br>
また直感的な機能を使用してシステムを垂直／水平の両方向に拡張できます。
<br>
InterSystems IRIS は、どんなに大きな問題であろうと対処します。
<br>
InterSystems IRIS は、マルチモデル機能により高い柔軟性を実現します。
<br>
つまり、いかなるコードセットおよびデータセットにおいてもコードが複数の異なるモデルのデータにアクセスできるのです。
<br>
オブジェクト、リレーショナル、ドキュメントだけでなく、基本データ構造へのネイティブアクセスにも対応しています。
<br>
データやコードを分離する必要はなく、すべてを単一の環境から実行できます。
<br>
このクラス最高のデータベース テクノロジーで提供される分析スイートにより、データから有意義な洞察を抽出できるようになります。
<br>
オープンな分析プラットフォームであるため、お気に入りのツールやテクノロジーを接続して組み合わせることができます。
<br>
InterSystems 独自のリアルタイム分析機能やダッシュボードのほか、サード パーティのテクノロジーも接続して利用できます。
<br>
他のデータベースと異なり、リアルタイム分析のためにトランザクションデータと分析データを別々に維持管理する必要はありません。
<br>
InterSystems IRIS はすべてを一括して実行し、モデルをリアルタイムで適用します。
<br>
ほとんどのデータベースは構造化データなら難なく処理できますが、今日では非構造化データが増加の一途をたどっています。
<br>
すなわち、必ずしも厳密に定義されていないデータ、例えば、各種の記事、ソーシャル メディアフィード、医師が書くカルテ、メールなどです。
<br>
このような非構造化データを扱う場合、InterSystems IRIS の自然言語処理機能を使用すれば、ボトムアップのアプローチが可能になります。
<br>
つまり、辞書やオントロジーをあらかじめ定義する必要がなくなります。
<br>
非構造化データ内のコンセプトやリレーションシップを直接そのまま検出できるようになります。
<br>
提供されている API により、主要なコンセプトの特定、ドキュメントの要約、感情の判別、関連トピックの検出などが可能になります。
<br>
InterSystems IRIS は統合データベース プラットフォームであり、オープンなデータベースプラットフォームでもあります。
<br>
パワフルで柔軟な統合エンジンが搭載されているため、人、プロセス、アプリケーション、システムを結び付けられます。
<br>
例えば、3 つの異なるアプリケーションを異なるユーザー集団が使用しているとします。
<br>
見込み客のデータを管理する営業アプリケーション、従業員と顧客の研修を管理する研修アプリケーション、そして顧客のサポート チケットやユーザー プロファイルを管理するサポートアプリケーションです。
<br>
これらのアプリケーションのユーザーとデータは共通していますが、それぞれ異なるアプリケーションです。
<br>
しかし InterSystems IRISなら、これらを完全に相互運用可能です互いに、シームレスにデータを共有してコミュニケーションを図れます。
<br>
さまざまな開発言語のAPI に対応しているため、既存のアプリケーションをInterSystems IRIS に接続して、これらのアプリケーションとの
データの送受信などを行えます。
<br>
既存アプリでどのような言語を使用していても対応できます。
<br>
メッセージ ルーティングにも対応しているため、新しい従業員を採用したときに、メッセージを学習アプリケーションに送信して、その名前と役職の情報を追加できます。
<br>
またデータを変換する場合も、必要な形式のデータを確実に入手できます。
<br>
例えば、あるシステムでは名前が「名姓」の形式で保存されていて、別のシステムでは「姓,名」の形式が使用されている場合、このデータを簡単かつ直感的に、そして適切に変換することができます。
<br>
どのような場合でも、InterSystems IRIS は、変化し続ける各部をシームレスに統合します
<br>
さらに、InterSystems IRIS上で構築されたアプリケーションをデプロイする場合のプロセスも、かつてないほど簡単です。
<br>
自動化されたツールが、パブリックまたはプライベートクラウド、ローカル サーバー、ベアメタル サーバー、または仮想マシンへのインフラのデプロイプロセスを最適化します。
<br>
ビジネスを前進させるアプリケーションを構築するのであれば、InterSystems IRIS 上での構築をお勧めします
</div>
</details>
> ※ NLPについての説明が含まれますが、この機能はバージョン2023.3以降の製品には含まれなくなりました。現在は<a href="https://github.com/intersystems/iknow/" target="_blank">オープンソース版</a>を公開しています。 
{: .block-warning}
<br>

> **IRIS概要についてもう少し詳しく確認されたい方は約30分の以下ビデオをご参照ください。**
>- InterSystems IRIS データプラットフォームのご紹介    
{: .block-warning}
{% include youtube-list.html id="vo12UnH-c-s" list="PLzSN_5VbNaxD-r8wU4LHwLwGSzUjrffEX" %}

<br>
- InterSystems へようこそ

    {% include youtube.html id="v4uoejre5IU" %}

<details class="transcript2">
<summary> ▶日本語字幕 </summary>
<div class="content">
InterSystems は、世界で最も重要なアプリケーションを支えるエンジンです。<br>
私たちのお客様は、医療、ビジネス、政府のシステムを円滑に運営しています。世界中の 5 億人以上の人々が、必要な情報への確実なアクセスを提供する当社のテクノロジーに信頼を寄せています。<br>

私たちが構築するすべての製品は、相互運用性（Interoperability）、信頼性（Reliability）、直感性（Intuitiveness）、拡張性（Scalability）という原則を実現しています。私たちのコードはエレガントでシンプルに設計されておりソリューションは効率的です。<br>

私たちは、お客様の成功のために必要なことは何でもします。私たちの最高の人材がお客様からのお問い合わせに対しサポートいたします。<br>

パートナーシップこそが私たちのビジネスの理由です。私たちは個人経営であるため、私たちが行うことはすべてお客様のためでありお客様だけのものです。<br>
クライアントのアプリケーションは、失敗が許されないほど重要なものだからです。<br>
必要なときに必要な情報を確実に入手できるよう、私たちはここにいます。<br>
私たちは、世界を前進させるソリューションを構築します。重要なデータを管理するなら InterSystems にお任せください。
</div>
</details>

---
## 2. <img src="./assets/icons/2-serversideapp-better-dicision.png" width="70%"/>

InterSystems 製品の組み込み言語である InterSystems ObjectScript を使用して、新しいクラスの作成、オブジェクトの操作、SQL クエリの実行について学習します。

このパスを終了すると、ObjectScript を使用してInterSystems製品のサーバーサイド・アプリケーションを構築することができるようになり、以下の開発に役立てることができます。

- データ操作以外の処理も含めたストアドプロシージャの開発
- Interoprabilityで使用するカスタム・ビジネス・コンポーネントの開発
- ビジネスルールとメッセージルータのコードで作成するカスタム関数
- カスタムコードによる高度なデータ変換の作成

カスタム・ビジネス・コンポーネントの構築方法の詳細については[「カスタムコンポーネントを使用したシステム統合の開発」](#4-)をご参照ください。

### はじめに

最初に概要をビデオでご覧ください。

InterSystems IRIS® データプラットフォームのアーキテクチャとクラスの基本を学び、ObjectScript でのコーディングを開始します。

- InterSystems 製品のアーキテクチャ概要 ～ネームスペースとデータベース～

    {% include youtube-list.html id="TNjUnuw8K_Q" list="PLzSN_5VbNaxCWpesN3ulh_EZ9sGkw09q5" %} 

<details class="transcript2">
<summary> ▶日本語字幕 </summary>
<div class="content">
こんにちは、InterSystems のテクニカルトレーナーのシェーンです。このビデオでは InterSystems 製品のアーキテクチャについてお話します。<br>
InterSystems 製品のアーキテクチャーについて説明する際、私たちは常に 2 つの主要な概念であるデータベースとネームスペースについて説明しています。<br>

データベースは物理的なファイルです。これらファイルはファイルシステム上のどこかに置かれています。<br>
InterSystems 製品の場合、データベース・ファイルにはデータだけでなくコードも含まれます。つまり、データベースは、データとコードを含むファイルシステム上の物理ファイルで、どこかのディレクトリに存在しています。<br><br>

ネームスペースは、データベース・レイヤの上にある抽象化された論理レイヤで、1 つ以上のデータベース・ファイルを参照します。<br>
新しいネームスペースを作成しようとすると、データ用のデフォルト・データベースとコード用のデフォルト・データベースの設定を求められます。<br>
確認のため、振り返りましょう。<br>
データベースは、データとコードを含むファイル・システム内の物理ファイルです。ネームスペースは、いくつかのデータベースを参照できる抽象化された論理定義です。<br><br>

ユーザがシステムに接続するとき、またアプリケーションが例えば ODBC や JDBC 経由でシステムに接続したり REST サービスや管理ポータルのような Web 接続を行ったり、ターミナルセッションで接続したりします。<br>
ユーザやアプリケーションがシステムへ接続する際、ネームスペースを指定します。<br>

例えば、請求処理を行うアプリケーションがあるとします。<br>
あなたは BILLING ネームスペースから、BILL データ・データベースと BILL コード・データベースに接続しようとします。<br>
この他に、ネームスペースから他のデータベースファイルをマッピングして利用することもできます。<br>
例えば、会計情報を取り扱う FINANCE ネームスペースを見てみましょう。<br>
このネームスペースではデフォルトのデータベースに加え、追加データを操作できるようにマッピングを追加することができます。<br>
また、他のユーザが他のアプリケーションに接続するために使用する他のデータベースを参照する VENDOR という名前のネームスペースも作成できます。<br>
このネームスペースはデフォルトデータベースとして、VEN データ・データベースと VEN コード・データベースを使用しています。<br>

このネームスペースは FINANCE データベースに Mapping されています。<br>
この定義により、ネームスペースに接続しているアプリケーションが FINANCE にあるデータを参照できることを示しています。<br>
そして、アプリケーションが接続している BILLING ネームスペースも同様に、FINANCE データベースのデータを参照できます。<br>
<br>
これは、ユーザとアプリケーションが1つのエントリーポイントでシステムに接続でき、ファイルシステム内のどこにファイルが存在するかという実装の詳細を気にすることなく多くのデータベースファイルからなるコードやデータを利用できるようにしています。<br>
<br>
これが、InterSystems 製品のアーキテクチャです。<br>
より詳細を確認されたい場合は、その他のビデオや記事をご参照ください。
</div>
</details>

### 日本語：セルフラーニングビデオ

オリエンテーションに最適なセルフラーニングビデオやコンテンツをご用意しています。

- 以下動画から、IRIS の開発環境の作成方法、ネームスペース／データベースについて、IDE から IRIS に接続する方法を確認できます。

    ✅ <a href="https://jp.community.intersystems.com/node/478601" target="_blank">【はじめての InterSystems IRIS】セルフラーニングビデオ：基本その2：InterSystems IRIS で開発をはじめよう！</a>

    {% include youtube-list.html id="ID6ImJTgJRk" list="PLzSN_5VbNaxBPaSSINLzv-CkDJy00bOSQ" %} 
    
<br>
- ObjectScriptの基本操作の学習については、**<a href="https://github.com/Intersystems-jp/ObjectScriptCookBook/blob/master/Basic.md" target="_blank">ObjectScript クックブック：ObjectScriptの基本のき！</a>** をご参照ください。
<br><br>
- 以下動画から、クラス定義の作成からインスタンス生成、保存までの流れを確認できます。

    ✅ <a href="https://jp.community.intersystems.com/node/478606" target="_blank">【はじめての InterSystems IRIS】セルフラーニングビデオ：基本その3：IRIS でクラス定義を作ろう（オブジェクト操作の練習）</a>

    {% include youtube.html id="kWJCzn9bndQ" list="PLzSN_5VbNaxBPaSSINLzv-CkDJy00bOSQ" %} 

<br>
- 以下動画から InterSystems 製品での JSON 操作方法をご確認いただけます。

    ✅ コピー＆ペースト元がある記事：<a href="https://jp.community.intersystems.com/node/480106" target="_blank">【はじめてのInterSystems IRIS】セルフラーニングビデオ：アクセス編：IRIS での JSON の操作</a>

    {% include youtube-list.html id="045HRug72VE" list="PLzSN_5VbNaxBPaSSINLzv-CkDJy00bOSQ" %} 

<br>
- メソッド内で SQL を記述する方法については、以下クックブックをご参照ください。

    ✅ <a href="https://github.com/Intersystems-jp/ObjectScriptCookBook/blob/master/Basic.md#7-%E3%83%A1%E3%82%BD%E3%83%83%E3%83%89%E3%82%84%E3%83%AB%E3%83%BC%E3%83%81%E3%83%B3%E3%81%A7sql%E3%82%92%E5%AE%9F%E8%A1%8C%E3%81%99%E3%82%8B%E6%96%B9%E6%B3%95" target="_blank">ObjectScriptクックブック：7.メソッドやルーチンでSQLを実行する方法</a>


関連するトレーニングコースは以下の通りです。
- <a href="https://www.intersystems.com/jp/intersystems-object/" target="_blank">InterSystems Object（2日間）</a>
- <a href="https://www.intersystems.com/jp/intersystems-sql/" target="_blank">InterSystems SQL（2日間）</a>
  

> **英語のみとなりますが、以下のオンラインコースもあります。**
>
> - <a href="https://learning.intersystems.com/course/view.php?name=IRIS%20Class" target="_blank">オンラインコース（英語）：Creating an InterSystems Class Definition in VS Code</a>
>
> - <a href="https://learning.intersystems.com/course/view.php?name=Cach%C3%A9%20ObjectScript%20Basics" target="_blank">オンラインコース（英語）:InterSystems ObjectScript Basics</a>
>
> - <a href="https://learning.intersystems.com/enrol/index.php?id=2523" target="_blank">オンラインコース（英語）:InterSystems IRIS Objects Introduction
>
> - <a href="https://learning.intersystems.com/course/view.php?name=Cach%C3%A9%20SQL%20Overview" target="_blank">オンラインコース（英語）：InterSystems SQL Overview</a>
>
> - <a href="https://learning.intersystems.com/course/view.php?name=JSON%20in%20IRIS" target="_blank">オンラインコース（英語）:Using JSON in InterSystems IRIS</a>
>
> - <a href="https://learning.intersystems.com/course/view.php?name=Server-Side%20Application%20Exercise" target="_blank">演習環境付き演習（オンラインコース）：Learning Path Exercise: Building a Server-Side Application with InterSystems IRIS</a>
>
>    InterSystems IRIS® データプラットフォームと InterSystems ObjectScript を使用して小規模なデータベースアプリケーションを作成します。
>    
>    この演習では、InterSystems IRIS を使用したサーバサイド・アプリケーションの構築の学習パスで学習したすべてのスキルを結集して、大規模な書籍コレクションに関する情報を格納および取得するためのクラスを作成し SQL を使用します。
>    
>    この演習は、既存の知識をテストするために学習パスを開始する前にまたはキャップストーン・プロジェクトとして最後にお試しください。
{: .block-tip}


### 認定テスト受験の準備が整ったら・・・

InterSystems Learning Services では、業界標準の認定試験を提供しあなたが InterSystems の技術を習得していることを証明します。

当社の試験は、安全なオンライン試験監督とセルフサービス予約で提供されます。受験者は、いつでもどこでも都合のよいときに試験を受けることができます。

※英語のみ：<a href="https://www.intersystems.com/education/" target="_blank">Exam: InterSystems IRIS Core Solutions Developer Specialist</a>


---
## 3. <img src="./assets/icons/3-integration.png" width="70%"/>

以下 3 種類の内容を学習できます。

- [InterSystems Interoprability(相互運用性機能)](#intersystems-interoperability相互運用性機能)
- [RESTful サービスの設定](#restfulサービスの設定)
- [PEXについて](#pexについて)

### InterSystems Interoperability(相互運用性機能)

InterSystems 製品の Interoperability(相互運用性)フレームワークにより、インターフェイスエンジニアやソフトウェア開発者は、複数のシステムを接続し下流のアプリケーションにメッセージを迅速にルーティングすることができます。

この内容を試すには、別のパス：<a href="BuildingBusinessIntegration.html" target="_blank">ビジネス・インテグレーションの構築</a> に進んでください。

### RESTfulサービスの設定

InterSystems IRIS® data platform で RESTful サービスをセットアップする方法をご紹介します。

- IRIS で作成する REST サーバの仕組みを解説します。

    {% include youtube-list.html id="tWP_9-jk4no" list="PLzSN_5VbNaxBPaSSINLzv-CkDJy00bOSQ&index=7" %}
<br>
- 手動で作成するディスパッチクラスの作成方法を解説しています。

    {% include youtube-list.html id="q3XVT98_05I" list="PLzSN_5VbNaxBPaSSINLzv-CkDJy00bOSQ&index=8" %}
<br>

- APIファーストによるRESTディスパッチクラスの作成方法を解説しています。
    {% include youtube-list.html id="SwquEq1fjTk" list="PLzSN_5VbNaxBPaSSINLzv-CkDJy00bOSQ&index=9" %}
<br>
>**英語のみとなりますが、以下のオンラインコースもあります。**
>
> InterSystems IRIS® data platform で RESTful サービスをセットアップする方法をご紹介します。 API 仕様から始めて、API のバックエンド・ロジックを生成して実装します。 クライアント・アプリケーションを使用して RESTful サービスを呼び出す方法、RESTful サービスを相互運用性プロダクションにアタッチする方法、および API トラフィックをモニターして制御する方法を確認できます。
>
> <a href="https://learning.intersystems.com/course/view.php?id=2549" target="_blank">Setting Up RESTful Services</a>
{: .block-tip}

### PEXについて

Production EXtension フレームワーク (PEX) を使用すると、ObjectScript を学習することなく、.NET または Java でカスタム相互運用性コンポーネントを構築できます。

PEX を使用すると使い慣れた言語でコードを記述でき、確立されたコードライブラリを活用してプロダクションにコンポーネントを追加できます。

{% include youtube.html id="hZnvMlXU5Og"%}

<details class="transcript2">
<summary> ▶日本語字幕 </summary>
<div class="content">
プロダクション拡張フレームワーク (PEX) は、InterSystems IRIS data platform に組み込まれた機能で選択した言語での相互運用性プロダクションでカスタム・ビジネス・コンポーネントを作成できます。
<br>
PEX は、InterSystems IRIS に含まれる多くの言語相互運用性機能の 1 つです。他の機能には、JDBC と ODBC、Python、.NET、Java、Node.JS の Native API クライアント・ライブラリがあります。
<br>
PEXを使用すれば、.NET や Java などの言語ライブラリを参照し使い慣れた言語で開発を続けることができます。
<br>
カスタム・コードは、PEX 機能を使用して InterSystems IRIS プロダクションにシームレスに統合できます。その仕組みを見てみましょう。
<br>
PEX は、基本的にプロキシ・オブジェクトを使用して InterSystems IRIS で動作します。プロダクションでは、EnsLib.PEX パッケージからビジネス・コンポーネントを追加して、.NET または Java コードのプロキシとして機能させることができます。
<br>
PEX パッケージのビジネス・コンポーネントは、言語とフレームワーク間のメッセージを中継する外部言語サーバと通信します。
<br>
言語内のコードは、PEX スーパークラスから継承された抽象メソッドをオーバーライドします。これらのメソッドは外部言語サーバーによって呼び出され、プロダクションからのリクエストを処理します。
<br>
コードでは、応答を作成したり InterSystems IRIS の 1 つ以上の他のビジネス・コンポーネントに要求を渡すことができます。
<br>
要求を処理する間、コードは JDBC または ODBC を使用してデータベースにクエリを実行するなど、InterSystems IRIS で他の処理を実行するために同じ接続を再利用することもできます。この機能は、再連続性 (reentrancy) と呼ばれます。
<br>
InterSystems IRIS のその他のビジネス・コンポーネントは、ObjectScript または PEX を使用して構築できます。PEX コンポーネントは、異なる言語で記述することもできるため比類のない柔軟性と複数のプログラミング言語にまたがって作業する能力が得られます。
<br>
たとえば、Java で構築されたビジネスサービスは、.NET で構築されたビジネスプロセスと通信できます。
<br>
そのビジネスプロセスは、レコードマップなどの相互運用性ユーティリティを使用して構築された ObjectScript コンポーネントにメッセージを渡すこともできます。
<br>
PEX を使用すると、選択した言語で記述しながら InterSystems IRIS Interoperability のコネクタとユーティリティを利用できます。
<br>
このビデオでは、PEX を紹介し、その機能を紹介しました。次のレッスンでは、PEX で動作するように環境を構成する方法を学びます。
</div>
</details>

<br>

- <a href="https://docs.intersystems.com/irislatestj/csp/docbook/DocBook.UI.Page.cls?KEY=EPEX_intro" target="_blank">ドキュメント：PEXの概要</a>
- <a href="https://learning.intersystems.com/course/view.php?name=PEXInteroperabilityProductions" target="_blank">Creating Interoperability Productions Using PEX</a

---
## 4. <img src="./assets/icons/5-access-multilanguage.png" width="70%"/>

InterSystems IRIS は、各種言語からアクセスすることができます。よくある使い方としては、他 DB と同様に SQL ベースでアクセスする方法があげられます。

このパスの最初に他の SQL データベースからの移行する際よく使用される DDL スクリプトを使用した SQL テーブルを構築する方法について説明します。

{% include youtube.html id="deo8KfS-oeI" %}

<details class="transcript2">
<summary> ▶日本語字幕 </summary>
<div class="content">
データベースは、データだけが保存されているのではなくデータを保持するために定義するテーブルやテーブル間のリレーションシップも含まれます。SQL では、データベースの構造を定義および管理するためにデータ定義言語 (DDL) が使用されます。
<br>
DDL スクリプトを使用することでデータベースを InterSystems IRIS data platform に移行したり、既存のデータベースの構造を使用して新しいデータベースを開始したりすることができます。
<br>
全体としてこのプロセスには 2 つの重要なステップがあります。まず、外部データベースまたは InterSystems IRIS から DDL スクリプトをエクスポートします。
<br>
次に、InterSystems Terminal でスクリプトをインポートするコマンドを実行します。InterSystems は、スクリプト内の情報を使用してテーブルとそのリレーションシップを構築します。
<br>
これらの手順を詳しく見ていきましょう。
<br>
まず、DDL スクリプトを作成します。どのデータベース管理システムにも、DDL スクリプトをエクスポートするツールがあります。
<br>
エクスポートされた DDL スクリプトを取得したらそのスクリプトをインポートし InterSystems IRIS でテーブルを作成する ObjectScript コマンドを作成する必要があります。
<br>
InterSystems IRIS の最新バージョンでは、DO $SYSTEM.SQL.Schema.ImportDDL() コマンドを使用します。<br>
続いてメソッドの括弧内に 3 つのパラメータを指定します。最初のパラメータは infile です。インポートする DDL スクリプト・ファイル名のフルパスを記述します。<br>
DDL スクリプトが MSSQL、Sybase、Informix または MySQL で作成された場合は、infile パラメータはリストで指定します。このリストの最初の要素は DDL スクリプトのパスで、その後に TranslateTable の値が続きます。

2 番目のパラメータとして、エラー・ログ・ファイルのフルパス名を指定する logfile を指定します。インポート中にエラーが発生した場合、エラー・テキストがログ・ファイルに保存されます。このパラメータはオプションでなので何も指定しない場合は、デフォルトで 入力ファイル名_Errors.log の名称でログを保存します。
<br>
3 番目のパラメータは DDLMode です。このパラメータには、DDL スクリプトのエクスポートに使用したベンダ (InterSystems IRIS や MySQL など) を入力します。
<br>
DDL スクリプトをインポートする正確なコマンドは、使用している InterSystems IRIS のバージョンによって異なります。InterSystems IRIS バージョン 2020.1 またはそれ以前を使用している場合、コマンドは DO $SYSTEM.SQL.DDLImport() で、3 つの必須パラメータと最大 6 つのオプション・パラメータを引数に指定します。
<br>
DDLMode は最初のパラメータです。
<br>
2 番目のパラメータはもう使用されないので空白のままにしておきます。
<br>
次に infile パラメータ（インポートする DDL スクリプト・ファイルのフル・パス名）です。残りのパラメータはオプションであり、必要に応じてこれらを含めることができます。
<br>
次は、outfileパラメータで、エラーが報告されるファイルのフルパス名を指定します。
<br>
次の 2 つのオプションのパラメータの中の nosup パラメータは、真偽フラグで 1 = TRUE／0 = FALSE のどちらかを指定します。このパラメータを TRUE に設定すると、スクリプトファイルからサポートされていないステートメントが nosupfile に記録されます。
<br>
nosupfile は、デフォルトでは [入力ファイル名_Unsupported.log] の名称でファイルが作成されます。nosupパラメータを FALSE に設定するか、デフォルトのままにすると nosupfile は作成されません。
<br>
nosupfile パラメータの後に、文末区切り文字を指定するパラメータ DEOS を指定します。これは DDL パーサーに 1 つの行がどこで終わり新しい行がどこで始まるかを指示します。DEOS パラメータのデフォルトは、DDLMode　パラメータで指定されたベンダーに基づいた適切な値になります。
<br>
8 番目のパラメータ errpause は、DDL スクリプトの実行中にエラーが発生した場合に InterSystems IRIS が一時停止する秒数です。これが指定されない場合、既定値は 5 秒です。
<br>
最後に、runtimemode パラメータは、DDLMode が InterSystems IRIS の場合にのみ適用され、インポートされた文をどの selectmode で実行するかを指定します： ODBC、DISPLAY、または LOGICAL です。デフォルトでは、LOGICAL モードが使用されます。
<br>
構文は、使用している InterSystems IRIS のバージョンによって異なりますが、コマンドは常に同じ方法で実行され同じ結果を返します。
<br>
InterSystems IRIS Terminal でコマンドを実行します。InterSystems IRIS は、入力ファイルとエラー・ログ・ファイルを返し、インポートされた各 SQL コマンドをリストします。
<br>
エラー・ログ・ファイルは、何も書き込まれていなくても作成されます。InterSystems IRIS 2020.1 以前を使用していてパラメータ nosup を TRUE に設定した場合、サポートされていないログ・ファイルが次にリストされます。このログ・ファイルは、何も書き込まれなくても作成されます。
<br>
DDLスクリプトをインポートしエラーを解決したらデータベースはデータを受け取る準備ができました。
<br>
SQL は ISO/ANSI 標準ですが、独自のコマンドと構文を持つ DDL 言語には多くのバリエーションがあります。InterSystems IRIS 以外からの DDL スクリプトに対応するコマンドの詳細は、InterSystems IRIS ドキュメンテーションの Web サイトを参照してください。
</div>
</details>
<br>
次に、各言語からのアクセス方法について解説します（別のパスに移動します）。

- <a href="JavaApptoISCProducts.html" target="_blank">Java アプリケーションと InterSystems 製品の接続</a>
- <a href="NodeApptoISCProducts.html" target="_balnk">Node.js アプリケーションと InterSystems 製品の接続</a>
- <a href="WritingPythonAppWithInterSystems.html" target="_blank">Python アプリケーションと InterSystems 製品の接続</a>
- <a href="dotNetApptoISCProducts.html" target="_blank">.NET アプリケーションと InterSystems 製品の接続</a>

---
## 5. <img src="./assets/icons/6-APIManagement.png" width="70%"/>

### 1. InterSystems API Managerとは
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

### 2. InterSystems API Managerのインストール

✅ ビデオ（英語）:Installing InterSystems API Managerとは

InterSystems API Manager バージョン 1.5+ のインストール手順、InterSystems IRIS® data platform のインスタンス準備方法、および API Manager インストール・キットで提供されるスクリプトの実行方法について説明しています。

{% include youtube.html id="KUJXKpMlAKo" %}

<details class="transcript2">
<summary> ▶日本語字幕 </summary>
<div class="content">
このビデオでは、キットの解凍から InterSystems API Manager のインストールから管理ポータルを開く手順までを説明します。
<br>
ここでは、InterSystems IRIS または HealthShare のインスタンスと API Manager 用のホスト・システムの準備方法、API Manager コンテナのセットアップと実行方法について説明します。

まず、API Manager に接続する InterSystems IRIS または HealthShare インスタンスの要件を確認し、これらの要件を満たす方法を確認します。
<br>
まず、インスタンスのライセンスが API Manager をサポートしていることを確認します。管理ポータルのライセンスキー画面に移動しブラウザ画面内で [API Management] を検索し文字列が含まれていることを確認します。
<br>
次に、IAMユーザを有効にします。
<br>
これを行うには、管理ポータルメニューの [システム管理] > [セキュリティ] > [ユーザ] に移動し、[IAM] を選択します。次に、[ユーザ有効]をチェックします。
<br>
ユーザーに新しいパスワードを設定します。このパスワードは、後で API Manager セットアップ・スクリプトを実行するときに使用します。
<br>
もう1つの要件は、IAM Web アプリケーションを有効にします。
<br>
これを設定するには、管理ポータルメニューの [システム管理] > [セキュリティ] > [アプリケーション] > [ウェブ・アプリケーション] に進み、[/api/iam] を選択し [アプリケーション有効] をチェックします。
<br>
IAM ユーザと Web アプリケーションの唯一の目的は、起動シーケンスに関連するライセンス情報を API Manager に提供することです。
<br>
InterSystems IRIS は、API Manager を通じて蓄積されたデータを保存または集計することは一切ありません。
<br>
API Manager に対してライセンス、ユーザ、および Web アプリケーションを有効にすることに加えて、InterSystems IRIS インスタンスには、API Manager が検出可能な静的 IP アドレスも必要です。
<br>
API Manager はコンテナ内で実行されます。
<br>
デフォルトではパブリック・ネットワークにしかアクセスできません。
<br>
したがって、インスタンスを検出可能にする最も簡単な方法は、パブリックな IP アドレスを持つことです。
<br>
API Manager と InterSystems IRIS が同じホスト上で実行されている場合、API Manager コンテナをホストのプライベート・ネットワークにアクセスさせるオプションもあります。
<br>
インスタンスの IP アドレスは、セットアップ・スクリプト中に 1 回だけ割り当てるため、静的である必要があります。
<br>
多くの大規模ネットワークやVPNで見られるようにインスタンスの IP アドレスが動的な場合この要件は課題となります。
<br>
動的な IP アドレスの問題は、API Manager と InterSystems IRIS が同じホスト・システム上にある場合ローカルの DNS レコードを作成して維持することで解決できます。
<br>
そうでない場合は、InterSystems IRIS インスタンス用に常にインスタンスのアドレスに解決され静的で一般に検索可能な IP アドレスを作成する必要があります。
<br>
次に、API Manager のホスト・システム要件について説明します。
<br>
API Manager と InterSystems IRIS は同じホスト・システム上で実行する必要はありませんが、これまで見てきたようにネットワーク接続されている必要があります。
<br>
API Manager ホスト・システムは、InterSystems コンテナに推奨されるオペレーティング・システムである Unix ディストリビューションである必要があります。
<br>
このビデオでは Ubuntu を使用しています。
<br>
ホスト・システムには、docker、docker-compose、および curl も必要です。最低限必要なバージョンはドキュメントに記載されています。
<br>
docker コンテナの経験は、API Manager をすぐにインストールする際には必要ありませんが、カスタマイズする際には役立ちます。
<br>
API Managerのセットアップを進めよう。
<br>
ホストシステム上で、コンテナのセットアップと起動のためのスクリプトを含む API Manager キットを開きます。
<br>
キットは InterSystems の WRC からダウンロードでき、tarball として提供されます。
<br>
tarball 自体はコンテナ・イメージではなく、キットを解凍して中身を取り出す必要があります。
<br>
キットには、readme ファイル、コンテナ・イメージ、スクリプトが含まれています。
<br>
readme ファイルには完全なインストラクション・セットが含まれており、自分でセットアップを行う際の参考になります。
<br>
API Manager をセットアップしてインストールするには、まず Docker イメージをロードします。
<br>
Docker が起動しているターミナルで、「docker load -i iam_image.tar」とコマンドを入力します。API Manager イメージのリポジトリ、イメージ、タグを確認します。この情報はセットアップスクリプトで使用されます。
<br>
これで API Manager のセットアップスクリプトを実行する準備が整いました。
<br>
ユーザーの入力により、セットアップスクリプトは現在のターミナルシェルに環境変数を作成し、Docker がそれを使用して API Manager コンテナを作成します。
<br>
セットアップスクリプトまたは compose スクリプトが失敗した場合は、環境変数を確認してください。
<br>
これらの変数は現在のシェルに存在するため、セットアップスクリプトを単に実行するのではなく、ターミナルからコマンド source ./iam-setup.sh を使用して実行します。
<br>
最初のプロンプトで API Manager のイメージ名を聞かれます。ターミナルで 「docker image ls」を実行すれば確認できます。この例では、イメージは 「intersystems/iam:1.5.0.9-4」です。
<br>
セットアップ・スクリプトの 2 番目のプロンプトでは、InterSystems インスタンスのアドレスを入力します。前述のように、これは静的でパブリックな IP アドレスである必要があります。
<br>
次に、InterSystems インスタンスの Web サーバ・ポートを入力します。
<br>
このデモでは、デフォルトのプライベート Web サーバ・ポートが使用されていますが、これは本番運用システムでは推奨されません。
<br>
次に、以前に設定した IAM ユーザ・パスワードを入力して確認します。
<br>
バージョン 1.5 のセットアップスクリプトの最後のプロンプトは、安全な HTTPS 接続に使用するデジタル証明書のファイルの場所を指定します。この例では HTTPS は必要ないため空白のままにします。
<br>
お使いの InterSystems IRIS インスタンスで HTTPS が必要な場合は、InterSystems IRIS での TLS の使用に関するドキュメントを参照して、デジタル証明書の詳細を確認してください。
<br>
セットアップに成功するとスクリプトは環境変数を設定しインスタンスが API Manager 対応のライセンスを持っていることを確認する要求を送信します。
<br>
スクリプトは、ISC_IAM_IMAGE および ISC_IRIS_URL を含む一連の環境変数を作成します。これらの変数一覧はドキュメントに記載されています。
<br>
セットアップに続いて、次のステップでは docker-compose を実行して API Manager コンテナを起動します。
<br>
セットアップ・スクリプトと同じシェルを使うため、シェルがあるディレクトリに移動します。その場所に docker-compose ファイルも配置されています。
<br>
ターミナルで 「docker-compose up -d」 を実行します。
<br>
この実行が完了したら、「docker ps -a」を実行してコンテナの状態を表示します。
<br>
3 つの API Manager コンテナの情報が表示されるはずです。
<br>
最初のコンテナである scripts_iam_1 は、ステータスが Up で実行されているはずです。もし起動に引っかかるようであれば何かが失敗しています。
<br>
2 番目のコンテナである scripts_iam-migrations_1 は、起動時にのみ使用され後でステータスが exited になります。
<br>
データは scripts_db_1 というコンテナに格納されステータスは Up になります。
<br>
iam_scripts コンテナもステータスが healthy で実行されている必要があります。
<br>
トラブルシューティングを行うには、まず、ホスト・システムのターミナルで iris list と入力し interSystems インスタンスのステータスを確認します。
<br>
docker logs もコンテナの健全性をデバッグするために必要な情報を表示します。
<br>
また、セットアップで使用したアドレスが静的で利用可能であることを確認します。
<br>
localhost のようなプライベートアドレスを指定した場合、セットアップスクリプトはローカルの curl リクエストを使用してライセンスを取得するためスムーズに実行されるかもしれません。
<br>
しかし、iam_scripts コンテナ内から実行されるクエリは宛先に到達しなかった場合、コンテナは unhealthy であると表示されます。
<br>
iam_scripts コンテナが正常であれば、API Manager ホストマシンで 8000-8004 の範囲でいくつかのポートが使用可能になります。HTTPS については、8443-8445 の範囲です。ポートとその機能の詳細についてはドキュメントをご参照ください。
<br>
API Manager コンテナが正常であるように見えたら、次のステップはテストです。
<br>
API Manager キットのテストスクリプトは、curl を使用して API Manager Admin API を呼び出し、デフォルトの API に基づいてサンプルのルートとサービスを作成します。
<br>
source ./iam-test.sh を使用してテストスクリプトを実行します。成功した応答メッセージには、「Successfully created service and route!」 と表示されます。
<br>
インストールがうまくいったかどうかの最終テストとして、ブラウザを使用して API Manager 管理ポータルのポート 8002 を開きます。
<br>
[Routes] タブに移動して、テストスクリプトによって作成されたサンプルルートを確認します。
<br>
API Manager のインスタンスの使用に関する情報およびインストールの詳細については、API Manager キットおよび InterSystems ドキュメント Web サイトをご参照ください。
</div>
</details>


### 3. ハンズオン

<a href="https://learning.intersystems.com/course/view.php?name=IAMExercise" target="_blank">演習環境付き演習（英語）:Hands-On with InterSystems API Manager for Developers</a>

InterSystems API Manager を使用して、InterSystems IRIS® data platform 内のコーヒー・メーカー・アプリケーションの API を管理します。

前提知識：コンテナと dcker の基本的な知識。REST と HTTP リクエスト、レスポンス、ステータス・コードの基礎知識が必要です。


✅参考記事：<a href="https://jp.community.intersystems.com/node/493416" target="_blank">ゼロから使いこなす IAM（InterSystems API Manager）</a>

---
## 6. <img src="./assets/icons/7-Analytics.png" width="70%"/>

InterSystems IRIS に組み込まれた InterSystems IRIS Business Intelligence は、ほぼリアルタイムの分析を提供します。

InterSystems BI では、IRIS にあるデータを使って、ダッシュボードやピボットテーブルを作成し、スループットを分析したり、規制データを報告したりすることができます。

この他、レポート作成に関する機能も提供しています。詳しくは、[「InterSystems Reportsでデータを視覚的に提供する」](#intersystems-reports-でデータを視覚的に提供する)のセクションを参照してください。

さらに、IRIS には　SQL コマンドを使用して予測モデルを構築、学習、実行するのできる Auto ML の機能も含まれています。詳しくは、[「InterSystems IRIS の IntegratedMLによる予測」](#intersystems-iris-の-integratedml-による予測)のセクションを参照しください。

---

✅ ビデオ（英語）：InterSystems のアナリティクス入門

InterSystems® 製品のアナリティクス機能をご紹介します。

InterSystems IRIS® data platform がサポートする組込み BI とサードパーティツールについて説明し、アナリティクスのニーズに対してこれらのツールをどのように使用できるかを紹介します。

このビデオで説明するコンセプトは、InterSystems IRIS、InterSystems IRIS® for Health、HealthShare® Health Connect に適用されます。

{% include youtube.html id="MBTJPGNcp6Y" %}

<details class="transcript2">
<summary> ▶日本語字幕 </summary>
<div class="content">
InterSystems IRIS data platform は、その設立当初からミッション・クリティカルなアプリケーションをホストし、データの保存と検索の高性能なトランザクション・モデルをサポートしてきました。現代の開発者やアナリストのニーズをサポートするために、InterSystems IRIS は、分析機能を拡張し大量のデータを照会し迅速に計算を実行できるようにしました。
<br>
分析ツールは、InterSystems IRIS とInterSystems IRIS for Health に直接組み込まれています。その結果、クエリを実行する際にデータの別コピーを必要とせずインフラストラクチャーのコストと開発労力の両方を節約することができます。もう一つの利点は、分析がリアルタイムのデータで実行されることです。
<br>
InterSystems IRIS は、情報ポータル、データ・ワークベンチ、アプリケーション・ハブの 3 つの主要なカテゴリに分類される様々な分析タスクをサポートしています。
<br>
情報ポータルのアクティビティには、データに関する洞察を伝えるために使用されるダッシュボードやレポートの作成が含まれます。ビジネスに特化した意思決定支援システムもこのカテゴリーに含まれます。これらのアクティビティの主な目的は、ビジネス上の洞察を構築することです。
<br>
情報ポータルのアクティビティに従事する役割には、通常、ビジネス・ユーザー（リーダーシップ、サブジェクト・マター・エキスパート、ビジネス・アナリストなど）や、データ・モデルやレポートを設計するためのアナリティクス・ツールを使いこなすより技術的な専門家が含まれます。
<br>
データワークベンチのカテゴリーには、テクニカルユーザーがデータに直接関与して洞察を得る探索型のアクティビティが含まれます。ここでは、キュレーションされたデータセットなどのデータプロダクトが作成されます。
<br>
データワークベンチのアクティビティでは、プログラミング経験や SQL のようなクエリ言語に精通したテクニカルユーザーが通常関与します。これには、開発（または DevOps）指向のデータエンジニアと、高度なアナリティクスや機械学習ツールを利用してビジネスを説明したり情報を提供したりするモデルを構築するデータサイエンティストの両方が含まれます。
<br>
アプリケーション・ハブは、拡張されたアプリケーションを作成するために洞察が使用される場所です。人工知能の組み込みや機械学習モデルの展開により、よりスマートなアプリケーションの構築に役立つ洞察を引き出すことができます。
<br>
ここには、アプリケーション開発者、ビジネス・プロセス・アーキテクト、その他の技術専門家がおり、他のグループのアウトプットをアプリケーションやワークフローにシームレスに適合させ、より効果的にすることができます。
<br>
このアナリティクス・ランドスケープを念頭に置きながら、InterSystems IRIS がこれらの対象者がデータから洞察を引き出すのをどのように支援しているかを見てみましょう。
<br>
このような広範なアナリティクス・ニーズに対応するため InterSystems は、強力なネイティブ・テクノロ ジー・スイートを提供する一方で使い慣れたサードパーティ・ツールのサポートを提供するという 2 つのアプローチを採用しています。
<br>
InterSystems は、関連する業界標準やオープンソース・テクノロジーをサポートし、補完的なソフトウェア・ベンダーと提携しています。このサポートは、InterSystems IRIS に組み込まれたテクノロジーに加えて、特定のアナリティクスのニーズを満たすために組み合わされます。
<br>
ここでは、InterSystems IRIS のネイティブ分析機能と、前述の各対象に関連するオープンソース・ツールのサポートについて説明します。ビルトインツールは、管理者、ビジネスアナリスト、データモデラーなどの情報ポータルユーザのために用意されています。InterSystems Reports は、ピクセルのように完璧なレポート作成と配布を提供し、組み込みのテキスト検索技術により必要なものを簡単に見つけることができます。
<br>
InterSystems IRIS Business Intelligence は、完全に組み込まれ、ストレージとネイティブに統合され、リアルタイムの分析機能を提供します。
<br>
情報ポータルのユーザは、JDBC または ODBC を使用して、市場をリードするビジネス・インテリジェンス・ベンダーから InterSystems IRIS に直接接続することもできます。さらに、InterSystems IRIS Adaptive Analytics アドオンによりビジネスユーザは、これらのツールで共有される単一のデータモデルを設計しクエリを実行することができます。また、一般的なクエリを追跡し、BI クエリを高速化するためにデータを事前集計します。
<br>
データエンジニアやデータサイエンティストなど、データワークベンチのより技術的な利用者のために、InterSystems IRIS は、大規模なデータセットに対する分析クエリのための強力な SQL エンジンと最適化を備えています。標準的な ANSI SQL の拡張として、IntegratedML は、SQL ベースのアプリケーションから直接予測モデルを構築し、実行するための使いやすい SQL コマンドのセットを提供します。InterSystems IRIS には、オープンソースとして利用可能な InterSystems オリジナルの自然言語処理技術も含まれています。
<br>
オープンソースのツールとしては、データワークベンチのユーザは、Apache Spark から InterSystems IRIS に保存されたデータを利用することができます。また、オープンソースの ML Toolkit を使用することで、機械学習プロセスのオーケストレータとして InterSystems の Interoperability（相互運用性）エンジンを活用することもできる。
<br>
エンタープライズアーキテクト、フルスタック開発者、インターフェイスエンジニアなど、アプリケーションハブの専門家は、サードパーティのソフトウェアや外部プログラミングを必要としないいくつかの組み込み機能にアクセスできます。例えば、開発者はネイティブの InterSystems ObjectScript 言語でコーディングすることができます。また、言語の柔軟性を高め、分析機能の活用や機械学習モデルをアプリケーションで直接作成するために使用できる Embedded Python も利用できます。
<br>
さらに、InterSystems IRIS の Interoperability（相互運用性）エンジンは、ビジネスプロセスとワークフローを定義および管理するためのローコードアプローチを提供します。アナリティクスと AI サービスを利用するための幅広いコネクタとプロトコルが付属しています。開発者は、画像認識やテキスト認識など、既存のサービスを活用したワークフローを作成できます。これらのツールは、ゼロから開発することなくビジネスロジックで呼び出すことができる。
<br>
これらの組み込みツール以外でも、外部言語サーバーを使用することで開発者はカスタムコードを呼び出したり、Java、Python、R、C# のモジュール全体を組み込んだりして、アプリケーションを充実させることができる。
<br>
開発者は、InterSystems IRIS に組み込まれた標準 PMML ランタイムを使用して、サードパーティのツールを使用して構築された機械学習モデルを組み込むこともできます。
<br>
InterSystems IRIS におけるアナリティクスの基本についてご理解いただけたかと思います。
</div>
</details>
---

### InterSystems IRIS BIによるデータ分析

InterSystems IRIS® Business Intelligence に含まれる Analyzer ツールは、データモデルを最大限に活用し様々な対象者向けに情報を表示する方法を提供します。

このパスでは、InterSystems IRIS® Business Intelligence に含まれる Analyzer ツールを使用してピボットテーブルとインタラクティブなダッシュボードを作成し、アプリケーションに組み込んだりレポートに変換する方法を学習します。

✅ InterSystems IRIS Business Intelligence 概要

{% include youtube.html id="xV9Aa31zxhI" %}

<br>

✅ InterSystems Business Intelligenceで使用するキューブ概要

{% include youtube.html id="xgAdwTy_q1Q" %}

---

✅ <a href="https://learning.intersystems.com/course/view.php?name=IRISBIAnalyzer" target="_blank">ビデオ（英語）:InterSystems IRIS BI: Analyzer</a>

<details class="transcript2">
<summary> ▶日本語字幕 </summary>
<div class="content">
InterSystems IRIS Business Intelligence の Analyzer ツールでは、キューブ内のデータからピボット・テーブルを簡単かつ直感的に作成できます。これらのピボット・テーブルを使用してダッシュボードを作成したりレポートを作成するための情報を収集したりできます。
<br>
このツールを使用するには、InterSystems IRIS 管理ポータルにアクセスし、[Analytics]、[Analyzer] の順にクリックします。
<br>
画面左側のキューブ・アイコンをクリックして既存のキューブを開きます。選択したキューブは、アイコンの下に表示されます。
<br>
アナライザで使用されるキューブは、アーキテクトで作成されます。この例では、SamplesBI データセットのデータを使用します。
<br>
アナライザ・ペインは、主に 3 つの領域で構成されます。左側はモデル・コンテンツ領域で、サブジェクト領域のコンテンツが展開可能なフォルダにリストされます。ピボット・ビルダは画面上部にあり、モデル・コンテンツ・エリアから項目を行、列、メジャー、またはフィルタとしてここにドラッグ・アンド・ドロップできます。最後に、下部のピボット・プレビュー・エリアは、ピボット・テーブルがダッシュボードでどのように表示されるかを示します。
<br>
モデル・コンテンツ領域を詳しく見てみましょう。メジャーフォルダの下には、キューブから直接取得した標準メジャーと計算メジャーがリストされています。計算メジャーはフラスコのアイコンが表示されています。
<br>
矢印をクリックしてフォルダを展開すると、ディメンジョンのレベルが表示されます。
<br>
一部のディメンジョンにはプロパティも含まれ、これらは青色で別のアイコンで表示されます。
<br>
ピボット・テーブルは、データを理解しやすいように配置されたディメンジョンとメジャーの組み合わせです。ピボット・テーブルを作成するには、まず、ディメンジョンをピボット・ビルダの行セクションにドラッグ・アンド・ドロップします。次に、モデル・コンテンツ領域のメジャーの 1 つをピボット・ビルダのメジャー・セクションにドラッグします。モデル・コンテンツ領域でメジャー名をダブルクリックして、メジャーを追加することもできます。
<br>
アナライザはクエリを自動的に実行するため、MDX の知識がなくてもキューブから簡単に情報を取得できます。
<br>
ディメンジョン、メジャー、およびフィルタをピボット・ビルダにドラッグ・アンド・ドロップすると、MDX クエリが自動的に作成されます。
<br>
スケッチブック・アイコンをクリックすると、現在の MDX クエリが表示されます。
<br>
コンポーネントを追加または削除すると、MDX クエリが変更されることに注意してください。
<br>
ここで、ピボット・テーブルを修正し、必要に応じて情報を追加または削除するプロセスを見てみましょう。
<br>
合計行は、一般的にピボット・テーブルに追加されます。これを行うには、レンチ・アイコンをクリックしてピボット・オプションを開きます。サマリセクションで、[合計] の横にあるチェック・ボックスを選択し、[OK] をクリックします。
<br>
すべての値が合計されましたが、合計として計算できないため平均が正しくないことに注意してください。
<br>
このテーブルには合計と平均を必要とする列が混在しているため、別の方法を使用する必要があります。ピボット・オプションに戻り、[合計] の横にあるチェック・ボックスの選択を解除して合計行を削除します。ここで、ベース・クラスのすべてのレコードを参照する項目をディメンジョン以下にある All Patients と追加します。この簡単な操作でサマリ行に合計と平均の両方が表示されるようになります。どのディメンジョンにも All Members 項目が含まれることに注目してください。
<br>
他のディメンジョンも同じ方法で表示および計算できます。例えば、ピボット・ビルダで行に Diagnoses を追加し、AgeD ディメンジョンの下の All Patients 項目を行にドラッグできます。これで、各診断の合計と平均が表示されます。
<br>
一部のディメンジョンには、ドリルアップおよびドリルダウンできるレベルの階層があります。この階層を示す一般的な例は日付ディメンジョンです。この例では、1920 年代の 10 年間から 1925 年まで、そして第 3 四半期と 7 月までドリルダウンできます。ドリル・アップする場合は、矢印をクリックするか、ドリル・ダウン・メニューの X をクリックしてドリル・レベルを削除します。
<br>
プレビュー領域の別のディメンジョンにレベルをドラッグしてドリルダウンすることもできます。例えば、2021年に Regison を追加できます。
<br>
City を追加しても、元の数字（この場合は1373）が合計に残っていることに注意してください。
<br>
アナライザを使用すると、選択したセルの最下位データ、またはデータ・ソースそのものを確認できます。この機能を確認するには、セルを選択しピボット・ビルダの上のメニューで双眼鏡のアイコンをクリックします。
<br>
表示されるデータには、最初の 100 項目が含まれます。次のページに進むには下部の矢印を使用します。この例では、7 ページの結果があります。
<br>
ピボット・テーブルに戻るには、ピボット・ビルダの上にある[テーブルの表示] ボタンをクリックします。
<br>
別のリストを表示するには、ピボット・ビルダの上にあるレンチ・アイコンをクリックしてピボット・オプション・メニューを開き、ドロップダウン・メニューから詳細リストを選択します。ピボット・ビルダーの上部にある双眼鏡をもう一度クリックすると、リストが表示されます。
<br>
別のリストを見つけるもう1つの方法は、モデル・コンテンツ・エリアの詳細リストを選択して、利用可能なリストをすべて表示することです。
<br>
フィルタは、表示するデータを区切るために不可欠です。アナライザでは、必要なフィルタをピボット・ビルダにドラッグ・アンド・ドロップするだけです。この例では、好きな色を表示するテーブルがあり赤のフィルタを追加します。テーブルには、このフィルタに基づく合計が「All」の見出しの下に表示されます。ここで、[ピボット・オプション] メニューを開き、[合計] を選択して、[行] に [年齢グループ] レベルを追加し合計を表示します。ディメンジョンを追加してもこのフィルタに基づく結果の合計数が保持されることに注意してください。
<br>
フィルタをすばやく追加するには、ディメンジョンをセパレータ・バーにドラッグします。そこから範囲を選択したり包含または除外する値を検索したり、フィルタをクリアしたりできます。フィルタ名の横にあるチェックボックスを選択するだけでフィルタを一時的に無効にできます。
<br>
高度なフィルタまたはメジャー用のフィルタを追加するには、[フィルタ] セクションの歯車アイコンを選択して [条件の追加] をクリックし、[値] ドロップダウン・メニューから項目を選択します。この例では、Measure.Test Score を選択します。次に、演算子 (この例では以下) をクリックし数値を追加します。これでテーブルには 50 点以下のテスト・スコアが表示されます。
<br>
最後に、[保存] をクリックしてピボット・テーブルを保存します。
<br>
次に、既存のフォルダを選択するか新規フォルダを作成してピボットに名前を付けます。
<br>
この時点で、ピボットを公開するか変更を許可しない場合はロックします。
<br>
また、検索しやすいように説明とキーワードを追加できます。
<br>
完了したら、[OK] をクリックします。
<br>
既存のピボットを開くには、[Open] をクリックし、フォルダとピボットを選択します。
<br>
ピボットを削除する場合は、そのピボットを開き [削除] をクリックします。削除を確認するメッセージが表示されます。
<br>
このように、InterSystems IRIS BI には、キューブのデータを操作するための強力なツールが用意されています。キューブの操作の詳細については、InterSystems ラーニング・サイトのビデオ「InterSystems Business Intelligenceで使用するキューブ概要」を参照してください。
</div>
</details>
<br>

✅ 関連ビデオ：<a href="https://jp.community.intersystems.com/node/484826" target="_blank">開発テンプレート（IRIS Analytics Template）の使い方のご紹介（第8回 InterSystems IRIS Analytics コンテスト）</a>

✅ 日本語チュートリアル（11シリーズ）：<a href="https://jp.community.intersystems.com/node/563396" target="_blank">IRIS BI開発者向けチュートリアルを試してみる</a>

✅ <a href="https://docs.intersystems.com/irislatestj/csp/docbook/DocBook.UI.Page.cls?KEY=D2DASH" target="_blank">日本語ドキュメント：ダッシュボードの作成


✅ InterSystems IRIS Business Intelligence：アーキテクト画面の基本の使い方

{% include youtube.html id="VblJyJl2Xho" %}

---
### InterSystems IRIS の IntegratedML による予測

InterSystems IRIS® data platform の機能である IntegratedML を使用することで、SQL 開発者はアプリケーションの SQL コマンドを使用して予測モデルを構築、トレーニング、実行することができます。

このパスでは、IntegratedML を紹介し、データから予測を開始する方法を紹介します。
<br>

✅ ビデオ（英語）：What is Machine Leraning?

機械学習の基本的な概念と、その利点と用途について学びます。 InterSystems IRIS® data platform の IntegratedML の概要を理解し、InterSystems IRIS の SQL 環境から直接アプリケーションに機械学習を実装する方法をご覧ください。

{% include youtube.html id="TYovA51HBLo" %}

<details class="transcript2">
<summary> ▶日本語字幕 </summary>
<div class="content">
開発者やエンジニアの手元にあるデータ量は増え続け、人間の脳が自力で処理できる限界に近づいています。大量のデータに依存する開発者やエンジニアは、データを効率的に処理する方法を見つける必要があります。
<br>
幸いなことにその必要はありません。機械学習を使えば、コンピューターは実際にこれらのタスクを実行ことができます。その方法を教えれば良いのです。
<br>
最も単純なレベルでは機械学習とは、システムが明示的な指示を与えられなくても特定のタスクを実行する方法を自動的に学習できるようにするプロセスです。
<br>
これらのタスクは様々ですが多くの場合、予測モデルの作成が含まれます。予測モデルとは、入力されたデータに対して予測を行うために使用できるデータモデルのことを指します。
<br>
ある不動産市場において、ユーザーが自分の家の価値を予測するのを助けるアプリケーションを考えてみよう。
<br>
家の価値を予測するためには、広さ、立地、ベッドルームの数など、さまざまな要素があります。
<br>
このような家の個々の特性、そしておそらくもっと多くの特性は、予測モデルで使用される「特徴量」として知られています。機械学習では、特徴量はモデルの入力となる個々の測定可能な要素です。
<br>
モデルの出力は、様々なラベルの確率で構成されます。ラベルとは、モデルが予測しようとする測定可能な要素であり、例えば、特徴量から推定される家の価値などです。
<br>
したがって、これらの特徴とラベルに関連する確率を含む住宅のデータセットがあれば、機械学習アルゴリズムは、それらの特徴とラベルの関係を学習して値を予測するモデルを作成することができます。
<br>
このような予測モデルを作成するための多くの異なるアルゴリズムが存在し、データサイエンティストは特定のワークフローのためにアルゴリズムを磨き、最適化することができます。
<br>
では、これらの予測モデルはどのようにして受け取ったデータを正しく解釈することを学習するのでしょうか？ラベルと機械学習アルゴリズムのための特徴量と相関する出力の両方を含む学習データを提供することによって、モデルはこれらの相関関係をよりよく理解するように学習することができます。
<br>
これらを組み合わせることで、入力データの特徴を使ってラベルの予測を行う関数が作成されます。この関数は、原理的には人間の開発者が値を予測するために書く関数と変わりません。機械を使って関数を作成し改良しているだけなのです。
<br>
このような機械学習は、今日事実上あらゆる業界で使われています。ヘルスケアでは、患者が再入院するリスクがあるかどうかを予測するアプリケーションにモデルが使われているかもしれません。これにより、患者が退院する前にケアチームが介入でき、医師や看護師の時間と労力を節約できる可能性があります。
<br>
金融の分野では、機械学習を活用することで銀行口座やクレジットカードの不正行為を検知することができます。
<br>
機械学習は、携帯電話からタクシーを依頼するような普段何気なく行っている作業でさえも可能します。タクシー会社のアプリのダイナミック・プライシング・システムは、様々な情報を利用してあなたが目にするタクシー料金を決定します。
<br>
機械学習は、あなたのアプリケーションがより良い結果を生み出すのに役立つと思いますが、手元にデータサイエンティストのチームがない場合あなたのためのソリューションがここにあります。
<br>
InterSystems IRIS data platform 内の IntegratedML は、データサイエンスの専門知識に関係なく、SQL の熟練した開発者がアプリケーション内で機械学習を利用することを可能にします。
<br>
IntegratedMLを使用することで、開発者は使い慣れた SQL 構文を使用して機械学習モデルの作成、学習、実行、検証を行うことができます。
<br>
目の前にある膨大な量のデータを活用し始める準備が整いましたら、InterSystems IRIS data platform の IntegratedML をお試しください。
</div>
</details>



<br>
✅ より深く学習されたい場合は、以下ビデオもご参照ください（日本語）

{% include youtube-list.html id="47bP5-AtBVU" list="PLzSN_5VbNaxC-z6_DKUZuO__zyudjLE-g" %}

<br>
✅ インフォグラフィックス（英語）

- <a href="https://learning.intersystems.com/course/view.php?name=Preparing%20Your%20Data" target="_blank">インフォグラフィック（英語）:Preparing Your Data for Machine Learning</a>

    このインフォグラフィックは、データを準備するための基本的なステップと、IntegratedML がそのプロセスをどのように効率化できるかを示しています。データを準備することは、アプリで機械学習を活用するための重要なステップです。

- <a href="https://learning.intersystems.com/course/view.php?name=Machine%20Learning%20Algorithms" target="_blank">インフォグラフィック（英語）:Common Supervised Machine Learning Algorithms</a>

<br>

✅ IntegratedML 紹介ビデオ

- IntegratedML のご紹介～InterSystems IRISのAutoMLご紹介～

    {% include youtube.html id="PFiqENE1uKA" %}

<br>
- SQLから始める機械学習 ～　IntegratedMLのご紹介　～

    {% include youtube-list.html id="3yLK9kBs4ic" list="PLzSN_5VbNaxC-z6_DKUZuO__zyudjLE-g&index=2" %}

<br>
- <a href="https://www.intersystems.com/jp/integratedml-datarobot-demo/" target="_blank">IntegratedMLとDataRobotの連携</a>

- <a href="https://learning.intersystems.com/course/view.php?name=IntegratedMLReadmissions" target="_blank">ビデオ（英語）：IntegratedML: Predicting Readmissions</a>

- <a href="https://learning.intersystems.com/course/view.php?name=HandsOnIntegratedML" target="_blank">演習環境付き演習（英語）:Hands-On with IntegratedML</a>

    ✅ <a href="https://jp.community.intersystems.com/node/537501" target="_blank">機械学習を試せるチュートリアル（日本語）：IntegratedML</a>

---
### InterSystems Reports でデータを視覚的に提供する

InterSystems IRIS® data platform、InterSystems IRIS® for Health、HealthShare® でレポートを作成、カスタマイズ、表示するには InterSystems Reports を使用します。

- ビデオ（英語）:Introduction to InterSystems Reports

    Logi Analytics が提供する InterSystems Reports は、データのビジュアルレポートを迅速に作成・表示できるレポート作成ツールです。このビデオでは、InterSystems Reports とそのコア・コンポーネントを紹介します。より詳細な情報については、Logi Report のドキュメントをご覧ください。

    {% include youtube.html id="B1UnUsDt90E" %}

<details class="transcript2">
<summary> ▶日本語字幕 </summary>
<div class="content">
Logi Analytics が提供する InterSystems Reports は、InterSystems IRIS data platform に統合されたレポーティング・ソリューションです。
<br>
InterSystems Reports は、Zen レポートと並行して実行できるので、新しいレポーティング・ソリューションを現在の環境に導入することができます。
<br>
InterSystems Reports は、Java Database Connectivity (JDBC) を使用して InterSystems IRIS data platform に接続し、レンダラーなしで PDF やその他のファイルフォーマットを生成します。
<br>
InterSystems Reports には、ストアドプロシージャ、またはカスタマイズされたデータベースクエリを呼び出す機能が組み込まれていて、SQL または ObjectScript で開発できます。
<br>
必要に応じて、ストアド・プロシージャは、InterSystems IRIS データへのアクセスを容易にし、データ検索を最適化することができます。
<br>
Zen レポート内の既存のストアド・プロシージャや SQL クエリをデータ・ソースとして再利用することができ、レポートのレイアウトを再構成するだけで済みます。
<br>
InterSystems Reports は、サーバとデザイナの 2 つの部分で構成されます。
<br>
サーバは、InterSystems Reports テクノロジを使用してレポートを表示または印刷する任意の場所にインストールできます。
<br>
サーバは、あらゆる Java Enterprise Edition アプリケーション・プラットフォーム上で動作する高性能なレポート生成エンジンであり、Windows と UNIX の両方でサポートされています。
<br>
レポートを生成するために、サーバは、ブラウザベースのアプリケーションからレポートの要求を受け取り、データにアクセスし、データをビジュアルなフォーマットにし、要求しているフロントエンド・アプリケーションに返します。
<br>
レポートは、HTML、PDF、XML、RTFなど、さまざまな形式で作成できます。
<br>
InterSystems Reports の 2 番目のコンポーネントはデザイナーです。デザイナーは、新しいビジュアル・テンプレートを作成するスペースを提供するデスクトップ・アプリケーションであり、様々なグラフィカル・フォーマットで簡単にデータを表示することができます。これにより、コードを記述することなく、レポートのレイアウト、書式設定、プレビューを迅速に行うことができます。
<br>
デザイナーには、レポートを作成しデータの表示を最適化するのに役立ついくつかのオプションとウィザードが用意されています。
<br>
デザイナーでレポートを確認しながら作業を進めることができます。
<br>
グループ化、サマリー、数式、画像、その他の要素を追加できます。
<br>
デザイナーをインストールする必要があるのは、新しいレポート・テンプレートをデザインする場合のみで、既存のレポートを実行する場合は必要ありません。
<br>
それでは、サーバとデザイナの両方を使用してレポートを作成・設計するプロセス全体を見てみましょう。
<br>
InterSystems IRIS からレポートを要求します。
<br>
InterSystems Reports サーバは、データを収集するために InterSystems IRIS に接続します。そして、このデータを取得し、デザイナーを使用して作成されたレポート・テンプレートの仕様を使用してビジュアル・レポートにまとめます。
<br>
レポートは定期的にスケジューリングされ、電子メールで配信されるか、ファイルにパブリッシュされます。
<br>
許可があれば、エンドユーザはレポートテンプレートに小さな修正を加えることができます。特定のニーズに合わせてフィールドを削除したり、ビジュアルフォーマットを変更したりできます。このような変更は保存することができ、将来のレポートはこのような変更を加えた状態で配信されます。
<br>
InterSystems Reports を使用することで、視覚的に魅力的で理解しやすいレポートを作成することがかつてないほど簡単になりました。
</div>
</details>
<br>

- <a href="https://docs.intersystems.com/components/csp/docbook/DocBook.UI.Page.cls?KEY=GISR_server" target="_blank">ドキュメント：InterSystems Reports Serverの設定</a>

- <a href="https://docs.intersystems.com/components/csp/docbook/DocBook.UI.Page.cls?KEY=GISR_designer#GISR_install_designer" target="_blank">ドキュメント：Designer Installation</a>

- <a href="https://learning.intersystems.com/course/view.php?name=GettingStartedInterSystemsReports" target="_blank">演習環境付き演習（英語）:Getting Started with InterSystems Reports</a> 

    [演習のPDF](https://learning.intersystems.com/pluginfile.php/37146/mod_resource/content/4/ISCReports_ExerciseGuide.pdf)

- <a href="https://learning.intersystems.com/course/view.php?id=2505" target="_blank">ビデオ（英語）：Introduction to InterSystems Reports Designer</a>


---
### Adaptive Analytics によるデータモデルの構築

InterSystems IRIS® Adaptive Analytics は、AtScale テクノロジーを使用し Tableau、Excel など既にお使いのテクノロジーとシームレスに統合することで、セルフサービス型のデータディスカバリー・アナリティクス機能を提供します。

このパスでは、インストールから最初のデータモデルの作成まで、最初の一歩を踏み出す方法をご紹介します。

- ビジネスインテリジェンスにおけるキューブ入門

    {% include youtube.html id="xgAdwTy_q1Q" %}

<br>

- InterSystems IRIS Adaptive Analytics のご紹介

    {% include youtube-list.html id="8j6iqmT13XI" list="PLzSN_5VbNaxBlWFxRfrrrScerJrpo7xjr&index=3" %}

- <a href="https://docs.intersystems.com/irislatestj/csp/docbook/DocBook.UI.Page.cls?KEY=AADAN" target="_blank">日本語ドキュメント:InterSystems IRIS Adaptive Analytics</a>

- <a href="https://learning.intersystems.com/course/view.php?name=AdaptiveAnalyticsEssentials" target="_blank">オンラインコース（英語）：InterSystems IRIS Adaptive Analytics Essential</a>


---
## 7. <img src="./assets/icons/8-performance.png" width="70%"/>

アプリケーションのパフォーマンスを必要なだけ確保するためには、高性能なインジェストツールでシステムを構成するだけでなく、大量かつ高速なインジェストのためにシャーディングを設定し、フェイルオーバーのためにミラーリングを設定する必要があります。

以下、上記に挙げた機能じついての推奨事項をご説明します。

- <a href="https://learning.intersystems.com/enrol/index.php?id=1545" target="_blank">ビデオ（英語）:InterSystems IRIS Speed Test: High-Volume Ingestion</a>

    InterSystems IRIS® data platform の新しいオープン・ソース・ハイブリッド・トランザクション／アナリティカル・プロセッシング（HTAP）スピード・テスト・デモの使用方法をご紹介します。
    
    InterSystems IRIS が、リアルタイムのアプリケーション・クエリに答えながら、いかに大量のデータを取り込むことができるかをご覧いただけます。
    
    このビデオでは、HTAP スピードテストを使って、InterSystems IRIS のパフォーマンスを MySQL や SAP HANA などの他のデータベースと比較する方法を紹介しています。

- <a href="https://learning.intersystems.com/course/view.php?id=2338" target="_blank">ビデオ（英語）：Identifying the Benefits of Mirroring and High Availability</a>

- <a href="https://learning.intersystems.com/course/view.php?id=2560" target="_blank">ビデオ（英語／日本語字幕付き）：Introduction to Sharding in InterSystems IRIS

- <a href="https://learning.intersystems.com/course/view.php?id=2586" target="_blank">ビデオ（英語／日本語字幕付き）：Planning and Deploying a Sharded Cluster</a>

- ビデオ（英語）：Finding and Fixing Slow SQL Queries

    {% include youtube.html id="3ZMNNABfCSY" %}

<details class="transcript2">
<summary> ▶日本語字幕 </summary>
<div class="content">
このビデオでは、遅い SQL クエリを特定し改善するプロセスを説明します。重要なのは遅いクエリが必ずしも問題であるとは限らないということ、そして速度は相対的なものであるということです。例えば、1 日 1 回実行され実行に 2 秒かかり大規模なサマリーレポートを生成するクエリは十分に速いと考えられるでしょう。
<br>
しかし、2 秒のクエリがメイン・ユーザー・インターフェースの重要な部分で 1 分間に 100 回実行されるのであれば、その効率を高めることができるかどうかよく検討する価値があります。
<br>
私たちのシステムでは、100 万行の株式取引データがあり各行が 1 つのトランザクションを表しています。私たちのシステムは、主にこの株式データに対して SQL クエリーを実行し、ダッシュボードを最新の状態に保つために使用されています。
<br>
最近、ユーザーからダッシュボードの更新が遅いという報告がありました。
<br>
この問題の原因となっているクエリを見つけるために、User ネームスペースで実行されているすべての SQL 文を調べます。SQL エクスプローラで [SQL 文] タブをクリックし、現在のネームスペース内のすべての SQL 文を表示します。
<br>
どのクエリの実行が遅いかを知りたいのでフィルタを追加して、そのテーブルで実行されているクエリだけを表示します。これにより、このテーブル上のすべてのクエリの実行回数、平均時間、合計時間などの詳細を見ることができます。合計時間でソートすると、どのクエリに最も時間がかかっているかがわかります。
<br>
ここでは、1 日に約 60 回実行されるクエリの合計時間が 106.5 秒であることがわかります。
<br>
これは、システムがこのクエリを実行するのに合計 106.5 秒を費やしたことを意味します。ここで、速度の相対性が重要になります。この場合このクエリの実行頻度を考慮すると合計時間は長いです。Data.StockData というテーブル名をクリックして、このクエリを詳しく見てみましょう。
<br>
このクエリーは、各銘柄について実行された売り取引の数を最新に集計しこの集計はメイントレーダーのダッシュボードで 5 秒ごとに更新されます。
<br>
代表的なデータでこのクエリーをテストシステムで実行すると、実行に 2 秒近くかかります。この問題を引き起こしているクエリを特定したので、そのクエリの実行速度を遅くしている原因を突き止めましょう。
<br>
遅いクエリを修正する場合、最初のステップは常にクエリ・プランを確認することです。InterSystems SQL クエリ・オプティマイザは、現在利用可能な情報で可能な限り効率的に実行されるようにクエリを自動的に処理します。
<br>
このプロセスの一環として、クエリオプティマイザは、クエリのフィルタ、集約、およびその他の処理を処理するための複数のプランを生成します。クエリオプティマイザは、テーブルの統計情報に基づいてそれらのコストを推定し実行時に最も効率的なプランを選択します。
<br>
クエリプランを見ることで、テーブルとインデックス構造をどのようにスキャンするかを確認することができます。これは、どのステップに最も時間がかかりクエリを遅くしているかを特定するのに役立ちます。この情報に基づいて、インデックスの追加や並列処理など効率を改善するための調整を行うことができます。
<br>
SQL エクスプローラからクエリプランを表示するには、クエリを入力し、[プラン表示] をクリックします。
<br>
ご覧のように、このクエリを実行する最初のステップは、ID をループしてマスターマップを読み取ることです。マスターマップは標準テーブルの主要なデータ構造で個々の行を 1 つずつ格納しています。この構造を ID でループしているので、クエリを実行する最初のステップは、テーブルのすべての行からデータを読み取ることです。行数の多いテーブルに対してこのようなマスターマップスキャンを行うクエリプランは非効率的です。
<br>
このテーブルには 100 万行以上のデータがあるため、マスターマップを読み込むのは非常に非効率的です。このプランを改善するためにクエリを調整する必要があります。
<br>
変更を加える前に、クエリオプティマイザが最新のテーブル統計情報を使用していることを確認しましょう。行数などの統計情報は、どのプランが最も効率的かを判断するのに役立ちます。これを確認するには、テーブルを選択します。次に、[アクション] メニューから [テーブルチューニング情報] をクリックします。
<br>
現在の ExtentSize（行数）はデフォルトの 100,000 に設定されています。これは、このテーブルの統計情報がまだ収集されていないことを示し、クエリ・オプティマイザは、このテーブルがかなり小さいテーブルであり、フル・テーブル・スキャンにそれほどコストがかからないと想定しています。テーブルの統計情報を収集するには、[テーブルチューニング] をクリックします。最近の製品バージョンでは、ほとんどの通常のテーブル構造についてテーブル統計が少なくとも 1 回は自動的に収集されます。ExtentSize は、テーブルのサイズがわかっていれば簡単に再確認できる統計情報です。
<br>
クエリオプティマイザが最新のテーブル統計を持っていることを確認できたので、クエリプランを再確認してみましょう。
<br>
プランは複数のモジュールで構成され、それぞれのモジュールが個別のアクションセットを実行します。モジュールは互いに呼び合い複数回呼び出されるものもあります。このモジュールはマスターマップを分割し、各分割に対して並列にモジュール A を呼び出します。
<br>
この特定の問い合わせ計画は、並列化の新しい方法である Adaptive Parallel 実行を使用しています。旧バージョンの製品では、並列化されたクエリプランは少し異なって見えます。
<br>
クエリを再度実行すると、並列化によってクエリ時間が短縮されていることがわかります。しかし、クエリプランはまだマスターマップの読み込みと ID のループを含んでいます。
<br>
理想的には、読み込むデータ量を減らすためにインデックスを使用することです。場合によっては、期待したときにインデックスが使用されないことがあります。そのような場合は、インデックスが存在し、選択可能であることを確認してください。インデックスの構築中、あるいはインデックスの構築に失敗した後、インデックスが無効になっている可能性があります。
<br>
テーブルにインデックスがあるかどうかを確認するには、SQL エクスプローラでテーブルを選択しカタログの詳細タブをクリックしてマップ/インデックスを選択します。
<br>
まだインデックスが設定されていないので、次のステップではインデックスを追加します。さまざまなインデックスや変更を試してみると、テーブルの挿入、更新、削除操作のパフォーマンスに影響を与える可能性があることに注意することが重要です。また、インデックスはストレージのコストにもなるため、慎重に追加する必要があります。可能であれば、まず代表的なデータを持つテストシステムで変更を行い、本番システムで変更を実施する前に何が最も効果的であるかを確認してください。
<br>
ここでは、テストシステムにインデックスを追加します。このクエリには、トランザクションタイプと日付の 2 つの WHERE 条件が含まれています。テーブルの約半数の行がトランザクションタイプ「SELL」を持っていると予想されますが、検索対象の日付を持つ行の数はもっと少ないはずです。そのため、トランザクションの日付にインデックスを追加し、クエリがより少ない行を読み込めるようにします。
<br>
このインデックスを作成するには、create indexコマンドを実行します。このコマンドは自動的にインデックスも作成します。
<br>
クエリプランをもう一度見てみましょう。最初のモジュール F は、クエリを並列に実行できるようにマスターマップをサブ範囲に分割します。モジュール F はモジュール A を呼び出し、モジュール B の結果を保持する temp ファイルを作成します。モジュール B は、先ほど作成したインデックスを読み込んで、一致するトランザクション日を持つ行の ID を見つけ、マスターマップからそれらの行だけを読み込みます。
<br>
クエリを再度実行すると、実行時間が 1 秒以下に短縮されていることがわかります。
<br>
Tune Table の実行とインデックスの追加は、このクエリの効率に大きな影響を与えましたが他にも検討すべきオプションがあります。
<br>
1 つのオプションは、SQL オプティマイザで様々なプランのパフォーマンスを比較することです。これらを表示するには、SQL エクスプローラのツールメニューから Alternate Show Plans を選択します。ここで、最適化しようとしているクエリを入力し可能なクエリプランを表示することができます。選択したクエリプランに特定のインデックスが期待通りに含まれていない場合、これらのプランの性能をテストすることは特に有用です。そのインデックスを使用するクエリプランを選択して試すことができそのパフォーマンスを確認することができます。
<br>
考慮すべきもう 1 つのオプションは並列処理です。私たちの場合、テーブルチューニング（Tune table）ユーティリティを実行した後、クエリはすでに自動的に並列化されていました。InterSystems IRIS は、大量のデータにアクセスするクエリに対してデフォルトでこの処理を行います。並列化された実行は、複数のプロセスに作業を分散し全体の実行時間を短縮することでクエリのパフォーマンスを向上させます。システムによっては、このAutoParallel設定が無効になっていたりこの設定が行われる閾値が高すぎる場合があります。この場合、%PARALLEL ヒントを使用して、オプティマイザに並列化するように指示することができます。
<br>
どのような変更を行うかが決まったら、適切な手順で稼働停止を最小限に抑えながら実稼働システム上でその変更を推進することができます。
</div>
</details>
<br>
- <a href="https://learning.intersystems.com/course/view.php?id=2533" target="_blank">体験環境付き演習（英語）：Optimizing SQL Queries in InterSystems IRIS</a>

    トレーニングコースで同様の内容をご確認いただけます。

    ✅対応するコース：<a href="https://www.intersystems.com/jp/intersystems-sql/" target="_blank">InterSystems SQL</a>

---
title: InterSysetms IRIS 管理の基本
date: 2024-12-03
permalink: IRISManagementBasics.html
layout: post
---

InterSystems IRIS® data platform の基礎と、システム管理者が製品のライフサイクルを通じて一般的なタスクを実行するのに役立つツールをご紹介します。

このコースを修了すると、通常の操作やトラブルシューティングにインターシステムズのドキュメントを読めばわかる程度の知識が身に付きます。

[1. <img src="./assets/icons/1.png" width="40%"/> ](#1-)

[2. <img src="./assets/icons/2.png" width="40%"/> ](#2-)

[3. <img src="./assets/icons/3.png" width="40%"/> ](#3-)

[4. <img src="./assets/icons/4.png" width="40%"/> ](#4-)

[5. <img src="./assets/icons/5.png" width="40%"/> ](#5-)

[6. <img src="./assets/icons/6.png" width="40%"/> ](#6-)

[7. <img src="./assets/icons/7.png" width="40%"/> ](#7-)

[8. <img src="./assets/icons/8.png" width="40%"/> ](#8-)

[9. <img src="./assets/icons/9.png" width="40%"/> ](#9-)

[10. <img src="./assets/icons/10.png" width="40%"/> ](#10-)

[11. <img src="./assets/icons/11.png" width="40%"/> ](#11-)

[12. 次は？](#12-次は)

---
## 1. <img src="./assets/icons/1.png" width="70%"/>

はじめに、InterSystems IRIS 概要と、その基盤となる基本アーキテクチャについてご紹介します。

- InterSystems 製品のアーキテクチャ概要 ～ネームスペースとデータベース～

    {% include youtube-list.html id="TNjUnuw8K_Q" list="PLzSN_5VbNaxCWpesN3ulh_EZ9sGkw09q5" %} 

<br>
- IRIS の開発環境の作成方法、ネームスペース／データベースについて

    IDE から IRIS に接続する方法も確認できます。

    ✅ <a href="https://jp.community.intersystems.com/node/478601" target="_blank">【はじめての InterSystems IRIS】セルフラーニングビデオ：基本その2：InterSystems IRIS で開発をはじめよう！</a>
        
    {% include youtube-list.html id="ID6ImJTgJRk" list="PLzSN_5VbNaxBPaSSINLzv-CkDJy00bOSQ" %} 

<br>
- <a href="https://learning.intersystems.com/enrol/index.php?id=1322" target="_blank">ビデオ（英語）：Introduction to the Management Portal</a>

- <a href="https://learning.intersystems.com/enrol/index.php?id=1433" target="_blank">ビデオ（英語）：Using the InterSystems Terminal</a>

    ターミナルで、タイプ：%Status のエラーを受け取った場合の確認方法については、以下<a href="https://github.com/Intersystems-jp/ObjectScriptCookBook" target="_blank">ObjectScriptクックブック</a> の項目をご参照ください。

    ✅ <a href="https://github.com/Intersystems-jp/ObjectScriptCookBook/blob/master/CookBook.md#status%E3%81%AE%E3%82%A8%E3%83%A9%E3%83%BC%E3%81%8C%E6%88%BB%E3%81%A3%E3%81%A6%E3%81%8D%E3%81%9F%E3%82%89" target="_blank">%Statusのエラーが戻ってきたら</a>

- Interoperability 概要
    - シリーズ記事
    
        - <a href="https://jp.community.intersystems.com/post/%E3%80%90%E3%81%AF%E3%81%98%E3%82%81%E3%81%A6%E3%81%AEintersystems-iris%E3%80%91interoperability%EF%BC%88%E7%9B%B8%E4%BA%92%E9%81%8B%E7%94%A8%E6%80%A7%EF%BC%89%EF%BC%9A%E5%8B%95%E4%BD%9C%E3%81%AE%E4%BB%95%E7%B5%84%E3%81%BF%E3%82%92%E7%9F%A5%E3%82%8D%E3%81%86" target="_blank">【はじめてのInterSystems IRIS】Interoperability（相互運用性）：動作の仕組みを知ろう</a>

        - <a href="https://jp.community.intersystems.com/post/%E3%80%90%E3%81%AF%E3%81%98%E3%82%81%E3%81%A6%E3%81%AEintersystems-iris%E3%80%91interoperability%EF%BC%88%E7%9B%B8%E4%BA%92%E9%81%8B%E7%94%A8%E6%80%A7%EF%BC%89%EF%BC%9A%E3%83%97%E3%83%AD%E3%83%80%E3%82%AF%E3%82%B7%E3%83%A7%E3%83%B3%E3%81%A8%E3%81%AF" target="_blank">【はじめてのInterSystems IRIS】Interoperability（相互運用性）：プロダクションとは</a>


    - ビデオ（20分ごろからご覧ください）

        {% include youtube-list.html id="vo12UnH-c-s" list="PLzSN_5VbNaxD-r8wU4LHwLwGSzUjrffEX&index=1&t=1203s" %}
<br>
> **日本語字幕ありの英語ビデオもあります**
>
>✅ <a href="https://learning.intersystems.com/course/view.php?name=Interop%20QS" target="_blank">ビデオ（英語）:Integration overview:Receiving and Routing Data in a Production</a>
{: .block-tip}


- グローバル変数について

    <a href="https://github.com/Intersystems-jp/IRISBasicTechnologyGuide/blob/main/%E5%A4%9A%E6%AC%A1%E5%85%83%E3%83%86%E3%82%99%E3%83%BC%E3%82%BF%E3%82%A8%E3%83%B3%E3%82%B7%E3%82%99%E3%83%B3%E3%81%AE%E6%A6%82%E5%BF%B5%E3%81%8A%E3%82%88%E3%81%B2%E3%82%99%E3%82%A2%E3%83%BC%E3%82%AD%E3%83%86%E3%82%AF%E3%83%81%E3%83%A3.pdf" target="_blank">ガイド：多次元データエンジンの概念およびアーキテクチャ</a>


> **日本語字幕ありの英語ビデオもあります**
>
>✅ <a href="https://learning.intersystems.com/enrol/index.php?id=2189" target="_blank">ビデオ（英語）:Exploring Multiple Data Models with Globals</a>
{: .block-tip}

---
## 2. <img src="./assets/icons/2.png" width="70%"/>

InterSystems IRIS では、製品をインストールする場所を選択できます。InterSystems IRIS のインストール、インスタンスの起動と停止、基本設定、およびアプリケーションに必要な場合は Web サーバのインストール方法について説明します。

- <a href="https://docs.intersystems.com/irislatestj/csp/docbook/DocBook.UI.Page.cls?KEY=PAGE_deployment" target="_blank">ドキュメント：導入</a>

- インストールについて

    ※製品版もコミュニティエディションもインストール方法は同様です。

    ✅ 記事：[【はじめての InterSystems IRIS】セルフラーニングビデオ：基本その１：InterSystems IRIS Community Edition をインストールしてみよう！](【はじめての InterSystems IRIS】セルフラーニングビデオ：基本その１：InterSystems IRIS Community Edition をインストールしてみよう！)

    {% include youtube-list.html id="nKDvM68Gs04" list="PLzSN_5VbNaxBPaSSINLzv-CkDJy00bOSQ" %}

### コンテナ
InterSystems IRIS コンテナ・イメージからコンテナを開始する方について説明します。

✅ Docker コンテナ版 InterSystems IRIS data platformの勧め

{% include youtube-list.html id="yY8BLUYp5IA" list="PLzSN_5VbNaxAUiQkx5d22TX0zjx4Mmqhb" %}
<br>
✅ InterSystems コンテナレジストリの使い方とコンテナ開始までの流れについて
<br>
{% include youtube-list.html id="HEGWVP0PIfI" list="PLzSN_5VbNaxAUiQkx5d22TX0zjx4Mmqhb" %}  
<br>
✅ まずはコンテナを動かしてみよう！～コンテナ版IRISで新機能を試す方法のご紹介～

{% include youtube-list.html id="JaV3VKWpffs" list="PLzSN_5VbNaxAUiQkx5d22TX0zjx4Mmqhb" %}  
<br>
ご参考：<a href="https://www.youtube.com/watch?v=yY8BLUYp5IA&list=PLzSN_5VbNaxAUiQkx5d22TX0zjx4Mmqhb" target="_blank">コンテナとIRISについてのYouTubeプレイリスト（日本語）</a>
<br>

> **英語ビデオもあります**
>
>- <a href="https://learning.intersystems.com/enrol/index.php?id=888" target="_blank">[ビデオ（英語）:Docker Containers and InterSystems IRIS</a>
>
>   このビデオシリーズでは、Docker コンテナとその用途を紹介し、InterSystems IRIS® deta platform と組み合わせた場合にいかに効果的であるかを紹介します。また、コンテナが継続的インテグレーション、継続的デプロイメント（CICD）アプローチにどのように適合するかもご覧いただけます。
>
>- <a href="https://learning.intersystems.com/enrol/index.php?id=1762" target="_blank">[ビデオ（英語）:Run InterSystems IRIS Community Edition Using Docker</a>
>
>- <a href="https://learning.intersystems.com/enrol/index.php?id=1753" target="_blank">[ビデオ（英語）：Kubernetes Overview</a>
>
>     複数のホストにまたがるコンテナのデプロイをオーケストレーションするためのオープンソースプラットフォームである Kubernetes についてご紹介します。InterSystems Kubernetes Operator により、InterSystems IRIS® data platform のユーザは、InterSystems IRIS アプリケーションのデプロイメントにおいて Kubernetes のメリットを享受することができます。
{: .block-tip}


### ライセンス

- <a href="https://docs.intersystems.com/irislatestj/csp/docbook/DocBook.UI.Page.cls?KEY=GSA_license_config" target="_blank">ドキュメント：InterSystems IRIS ライセンスの構成</a>

- <a href="https://docs.intersystems.com/irislatestj/csp/docbook/DocBook.UI.Page.cls?KEY=GSA_license_update_key" target="_blank">ドキュメント：ライセンス・キーの有効化</a>

---
## 3. <img src="./assets/icons/3.png" width="70%"/>
最初に、ネームスペースとデータベースを作成し、基礎となるデータ構造とどのような関係があるかを学習します。次に、構成パラメータ・ファイル（CPF）、メモリ、およびアラートの構成を学習します。

### システム

- <a href="https://docs.intersystems.com/irislatestj/csp/docbook/DocBook.UI.Page.cls?KEY=GSA_using_instance_control" target="_blank">ドキュメント：InterSystems IRIS インスタンスの制御</a>

- <a href="https://docs.intersystems.com/irislatestj/csp/docbook/DocBook.UI.Page.cls?KEY=GSA_config_system" target="_blank">ドキュメント：システム情報の構成</a>

- <a href="https://docs.intersystems.com/irislatestj/csp/docbook/DocBook.UI.Page.cls?KEY=RACS_cpf" target="_blank">ドキュメント：構成パラメータ・ファイルの概要</a>

- <a href="https://jp.community.intersystems.com/node/477746" target="_blank">コミュニティ：InterSystemsデータプラットフォームとパフォーマンス-パート4: メモリの確認</a>

- <a href="https://docs.intersystems.com/irislatestj/csp/docbook/DocBook.UI.Page.cls?KEY=GCGI_intro" target="_blank">ドキュメント：Webゲートウェイ概要</a>

> **英語ビデオもあります**
>
>✅ <a href="https://learning.intersystems.com/course/view.php?name=ConfigWebGateway" target="_blank">ビデオ（英語）：Configuring the InterSystems Web Gateway</a>
{: .block-tip}

### ネームスペース

- ドキュメント
    - <a href="https://docs.intersystems.com/irislatestj/csp/docbook/DocBook.UI.Page.cls?KEY=GORIENT_enviro" target="_blank">ドキュメント：ネームスペースとデータベース</a>

    - <a href="https://docs.intersystems.com/irislatestj/csp/docbook/DocBook.UI.Page.cls?KEY=GSA_config_namespace" target="_blank">ドキュメント：ネームペースの構成</a>

- ビデオ：ネームスペースとデータベースの作成
    
    ✅ <a href="https://jp.community.intersystems.com/node/478601" target="_blank">記事：【はじめての InterSystems IRIS】セルフラーニングビデオ：基本その2：InterSystems IRIS で開発をはじめよう！</a>

{% include youtube-list.html id="ID6ImJTgJRk" list="PLzSN_5VbNaxBPaSSINLzv-CkDJy00bOSQ" %}  
<br>

> **英語ビデオもあります**
>
>✅ <a href="https://learning.intersystems.com/enrol/index.php?id=2124" target="_blank">ビデオ（英語）：Creating Namespaces and Databases</a>
{: .block-tip}


### データベース

- <a href="https://docs.intersystems.com/irislatestj/csp/docbook/DocBook.UI.Page.cls?KEY=GSA_config_database_create" target="_blank">ドキュメント：ローカル・データベースの作成</a>

- <a href="https://docs.intersystems.com/irislatestj/csp/docbook/DocBook.UI.Page.cls?KEY=GSA_config_databases" target="_blank">ドキュメント：データベースの構成</a>

- <a href="https://docs.intersystems.com/irislatestj/csp/docbook/DocBook.UI.Page.cls?KEY=GSA_manage_databases" target="_blank">ドキュメント：ローカルデータベースの管理</a>

---
## 4. <img src="./assets/icons/4.png" width="70%"/>
セキュリティの構成と管理に役立つ製品内のツールと認証オプションを使用して、ユーザーとロールを設定します。

### 概要

- <a href="https://docs.intersystems.com/irislatestj/csp/docbook/DocBook.UI.Page.cls?KEY=GORIENT_ch_security" target="_blank">ドキュメント：InterSystems IRIS セキュリティ</a>

- ビデオ（英語／日本語字幕）：InterSystems 製品 のユーザとロールについて

{% include youtube.html id="YgFz26hD4vc" %}

<details class="transcript2">
<summary> ▶日本語字幕 </summary>
<div class="content">
InterSystems のオンラインコース開発者のデレクです。このビデオでは、InterSystems 製品のシステム管理の観点からシステム内のユーザとロールを管理する方法についてまとめます。また、セキュリティのトピックとして、アセットとリソースの 2 つのシステム管理トピックについても簡単にご説明します。もしこの用語を聞いたことがない場合は、まず他のコンテンツなどで調べて用語に慣れておくことをお勧めします。
<br>
システムにおけるアセットとは、データ、コード、サービスなど、InterSystems IRIS システムにあるすべてのものを指します。そしてリソースは、そのアセットを保護するものです。つまり、すべてのアセットには、それを保護するリソースが存在します。そしてこれらのリソースと権限を組み合わせることでユーザに割り当てられる権限が得られます。これからシステム内にあるアセットとリソースに基づいてユーザーとロールを管理する簡単な例を紹介します。
<br>
北米の販売データベースがあり、NA_sales というリソースで保護されている例を見てみましょう。これは営業担当者がアクセスするためのものです。Jane という名前の営業担当者がいて、Jane はこのデータベースにアクセスする必要があります。このリソースを読み取り書き込み権限と組み合わせることで、例えば、NA_sales データベースから読み取りと書き込みができる権限を Jane に与えることができます。このように特権と呼ばれる他のリソースと権限を組み合わせることで、Jane が営業担当者として必要なさまざまなデータベース、コード・ファイル、サービスにアクセスするために必要なすべての権限を与えることができます。この特権の集合体をまとめてセールス担当者ロールと呼ぶことができるロールを作成することができます。
<br>
このロールの便利なところは、他の営業担当者がシステムに参加し Jane と同じ権限を必要とする場合、彼らを営業担当者ロールに追加するだけでいいということです。管理も簡単です。また、ロールが変更され、例えばある地域のデータベースにアクセスできなくなった場合、ロールからその権限を削除することができます。これと同じように、システムの別の場所に Ryan というエンジニアがいるとします。Ryan は少し Jane と異なります。Ryan は、Jane が持っているリソースとはまったく別のリソースにアクセスする必要があるエンジニアです。Ryan に必要な権限は 9、または 10 種類あるかもしれませんがソフトウェアのビルドやテストのスケジュールなどエンジニアがアクセスする必要のあるあらゆるものが必要です。Janeと同じように、権限のグループを作成してエンジニアのロールにすることができます。そして同様に新しいエンジニアがシステムに参加したときに、個別にすべてをユーザープロファイルに追加するのではなくこのロールに追加することができます。
<br>
システム管理とオーバーヘッドの観点から知っておくべき重要なことは、このようにロールを組み合わせることでシステム内にあるハイブリッドタイプのロールのオーバーヘッドを回避できるということです。例えば、私たちの会社にはセールス・エンジニアという別の社員がいます。このセールス・エンジニアは少し特殊で、エンジニアがアクセスする必要があるものすべてにアクセスしなければなりませんが、セールス担当者がアクセスする必要があるものすべてにアクセスする必要もあります。このハイブリッド・アプローチでは、セールスエンジニアのロールにすべての権限や権限グループを追加する代わりに、すでに作成されているロールをサブセットとしてこのロールに直接埋め込んだり追加したりすることができます。
<br>
これが本当に便利なのは、セールスエンジニアのようなハイブリッド・ロールを簡単にシステムに追加できるだけでなく、将来的に会社の要件、例えば営業担当者の要件が変更になり権限を削除しなければならなくなった場合でも、すべてのセールスエンジニアと営業担当者を調べて権限を取り消す必要がないことです。セールスレップのロールから権限を削除すれば、その権限はセールスエンジニアのロールに伝わります。以上、システムにおけるユーザーとロールの管理方法、およびアセットとリソースの関係について説明しました。
<br>
次に、システムの管理ポータルを参照し実際にどのように定義するのか、またユーザとロールを管理するための設定にアクセスできる場所を確認しましょう。管理ポータルのホームページから、システム管理、セキュリティの順に移動します。ここには、このビデオで説明したユーザ、ロール、リソースのページがあります。[リソース] に移動すると、InterSystems IRIS に存在するリソースのリストとそれぞれの説明が表示されます。ロールのページでは、システムに存在するすべてのロールが表示されます。
<br>
システムで生成されたロールは常に % 記号で始まります。ロールを作成する場合この文字で始めることはできません。ロールを作成すると、ボードに示した図のようにそのロールに権限を追加するためのオプションが表示されます。セールス・エンジニアの例のように、このロールに他のロールを追加するには、「メンバー」タブをクリックし、ここに追加します。最後に、ユーザ・ページに入ります。InterSystems IRIS システム内のすべてのユーザを参照できます。ユーザを編集することで、ユーザがどのような役割を持っているかを確認し適切に管理することができます。例えば、Jane のプロファイルを見ることで、例のようにセールス担当者のロールを追加することができます。プロファイルにロールを追加したり削除したりしたい場合は、ここですべて行うことができます。
<br>
まとめると、システム内のユーザとロールの管理方法を知っておくことは、システム管理の観点から非常に役立ちます。また、ユーザを追加したり削除したり InterSystem 製品のシステムの要件を変更したりする場合にも、スマートなアプローチを取ることでオーバーヘッド・コストを削減することができます。
<br>
以上、参考になれば幸いです。また、その他のシステム管理トピックやセキュリティ・トピックについて、より多くの情報を確認される場合は、ぜひ、オンラインラーニングやドキュメントページをご覧ください。
</div>
</details>
<br>

### セキュリティの設定と管理

- <a href="https://docs.intersystems.com/irislatestj/csp/docbook/DocBook.UI.Page.cls?KEY=GSTU_seccli_security" target="_blank">ドキュメント：^SECURITY</a>

- <a href="https://docs.intersystems.com/irislatestj/csp/docbook/DocBook.UI.Page.cls?KEY=GSA_manage_services" target="_blank">ドキュメント：サービスの管理</a>

    対象：概要説明と「使用可能なサービス」

- <a href="https://docs.intersystems.com/irislatestj/csp/docbook/Doc.View.cls?KEY=ROARS_encrypt_dbmgmt" target="_blank">ドキュメント：暗号化データベースの使用法</a>

    対象：概要説明と「暗号化データベースの作成」

    参考：<a href="https://jp.community.intersystems.com/node/485826" target="_blank">データベースの暗号化手順について</a>

- <a href="https://docs.intersystems.com/irislatest/csp/documatic/%25CSP.Documatic.cls?&LIBRARY=%25SYS&CLASSNAME=Security.Users#Export" target="_blank">ドキュメント（クラスリファレンス）：Security.User　Export()</a>

    参考：<a href="https://jp.community.intersystems.com/node/534526" target="_blank">セキュリティ設定のエクスポートとインポートに関するTips</a>

### 認証

- <a href="https://docs.intersystems.com/irislatestj/csp/docbook/DocBook.UI.Page.cls?KEY=ROARS_iam_ldap" target="_blank">ドキュメント：LDAP and InterSystems IRIS®</a>

- <a href="https://docs.intersystems.com/irislatestj/csp/docbook/DocBook.UI.Page.cls?KEY=ROARS_iam_twofactor" target="_blank">ドキュメント：2要素認証</a>

    対象：「2要素認証」

---
## 5. <img src="./assets/icons/5.png" width="70%"/>
システムの健全性を監視し、潜在的な問題を早期に発見する方法を学びます。

- <a href="https://docs.intersystems.com/irislatestj/csp/docbook/DocBook.UI.Page.cls?KEY=GCM_monitor#GCM_monitor_tools" target="_blank">ドキュメント：システム監視ツール</a>

- <a href="https://docs.intersystems.com/irislatestj/csp/docbook/DocBook.UI.Page.cls?KEY=GCM_systemperf" target="_blank">ドキュメント：^SystemPerformance を使用したパフォーマンスの監視</a>

    対象：「^SystemPerformance ユーティリティの実行」

- <a href="https://docs.intersystems.com/irislatestj/csp/docbook/DocBook.UI.Page.cls?KEY=GCM_dashboard" target="_blank">ドキュメント:管理ポータルを使用したInterSystemsの監視</a>

- <a href="https://docs.intersystems.com/irislatestj/csp/docbook/DocBook.UI.Page.cls?KEY=GCM_healthmon_sysmon" target="_blank">ドキュメント：システム・モニタ</a>

- <a href="https://docs.intersystems.com/irislatestj/csp/docbook/DocBook.UI.Page.cls?KEY=GSA_manage_databases_details" target="_blank">ドキュメント：データベースの詳細ページ</a>


---
## 6. <img src="./assets/icons/6.png" width="70%"/>
プロセス、ロック、ジャーナリングの管理について学習します。

- <a href="https://docs.intersystems.com/irislatestj/csp/docbook/DocBook.UI.Page.cls?KEY=GSTU_process" target="_blank">ドキュメント：プロセス管理</a>

    冒頭の紹介文のみお読みください

- <a href="https://docs.intersystems.com/irislatestj/csp/docbook/DocBook.UI.Page.cls?KEY=GCOS_locktable" target="_blank">ドキュメント：ロックの管理</a>

- <a href="https://docs.intersystems.com/irislatestj/csp/docbook/DocBook.UI.Page.cls?KEY=GCOS_locktable_viewall" target="_blank">ドキュメント：システム全体での現在のロックの管理</a>

    概要説明のみお読みください

    参考
    - <a href="https://jp.community.intersystems.com/node/495426" target="_blank">ロックテーブルの使用状況を簡単に確認する方法</a>

    - <a href="https://jp.community.intersystems.com/node/484976" target="_blank">プログラム内でロック情報を取得する方法</a>

    - <a href="https://jp.community.intersystems.com/node/493301" target="_blank">アプリケーションでロックタイムアウトエラーが発生する理由</a>

- <a href="https://docs.intersystems.com/irislatestj/csp/docbook/DocBook.UI.Page.cls?KEY=GSA_manage_taskmgr" target="_blank">ドキュメント：タスク・マネージャの使用</a>

    参考
    - <a href="https://jp.community.intersystems.com/node/492746" target="_blank">プログラミングでタスクスケジュールを登録・参照する方法</a>

    - <a href="https://jp.community.intersystems.com/node/494331" target="_blank">タスクスケジュールを別環境にコピーする方法</a>

    - <a href="https://jp.community.intersystems.com/node/518651" target="_blank">タスクの起動でエラーが発生した時にメールで通知する方法</a>

- <a href="https://docs.intersystems.com/irislatestj/csp/docbook/Doc.View.cls?KEY=GCDI_journal_overview" target="_blank">ドキュメント：ジャーナリングの概要</a>


- <a href="https://docs.intersystems.com/irislatestj/csp/docbook/Doc.View.cls?KEY=GCDI_journal_tasks" target="_blank">ドキュメント：ジャーナリング処理タスク</a>

    参考
    - <a href="https://jp.community.intersystems.com/node/512671" target="_blank">ジャーナルファイルの使用量をチェックする方法</a>

    - <a href="https://jp.community.intersystems.com/node/501426" target="_blank">ジャーナルファイルを削除する方法</a>

    - <a href="https://faq.intersystems.co.jp/csp/faq/result.csp?DocNo=276" target="_blank">ジャーナルのON／OFFについて、コマンドで操作する方法を教えてください。</a>

    - <a href="https://jp.community.intersystems.com/node/508306" target="_blank">グローバル単位でジャーナルのON/OFF設定する方法</a>

    - <a href="https://faq.intersystems.co.jp/csp/faq/result.csp?DocNo=582" target="_blank">ジャーナルの整合性チェックやサマリの表示をコマンドで実行する方法</a>

    - <a href="https://jp.community.intersystems.com/node/537211" target="_blank">ジャーナル圧縮機能について</a>

    - <a href="https://jp.community.intersystems.com/node/542656" target="_blank">IRISジャーナル（z圧縮済み）をCachéにリストアする方法</a>

---
## 7. <img src="./assets/icons/7.png" width="70%"/>
パフォーマンス・メトリクスを確認し、SQL クエリを特定して最適化します。次に、Enterprise Cache Protocol (ECP) がどのようにスケーラビリティを向上させるかを確認します。

### システムのパフォーマンスの測定

- Performance 101

    漠然とした「遅い」状況をどのように解決すればいいのでしょう？パフォーマンスに困ったときにどこに着目し、どのツールで調べていくか、お客様から日々ご相談をいただくカスタマーサポートから、解決に向かうアプローチの「イロハ」をご紹介しています。

    {% include youtube-list.html id="ul3j2ljUE3Y" list="PLzSN_5VbNaxCeC_ibw2l-xneMCwCVf-Or&index=7" %}
<br>

- 関連情報：<a href="https://docs.intersystems.com/irislatestj/csp/docbook/Doc.View.cls?KEY=GCM_systemperf" target="_blank">^SystemPerformance を使用したパフォーマンスの監視</a>
    - 参考記事：<a href="https://jp.community.intersystems.com/node/557776" target="_blank">^mypButtons を利用して InterSystems IRIS パフォーマンスをチェックしてみましょう</a>


> **以下のビデオ（英語）もあります。**
>- <a href="https://learning.intersystems.com/course/view.php?name=Understanding%20System%20Performance%20Metrics" target="_blank">ビデオ（英語）：Understanding System Perfomance Metrics</a>
>
>- <a href="https://learning.intersystems.com/course/view.php?id=1560" target="_blank">ビデオ（英語）：Performance Testing with InterSystems Tools</a>
{: .block-tip}

### SQLパフォーマンスの最適化
- <a href="https://learning.intersystems.com/course/view.php?id=1013" target="_blank">ビデオ（英語）：Optimizing Your SQL Queries</a>

    ✅ 記事：<a href="https://jp.community.intersystems.com/node/502256" target="_blank">クエリをチューニングする方法</a>

- <a href="https://docs.intersystems.com/irislatestj/csp/docbook/Doc.View.cls?KEY=AGSOB#AGSOB_troubleshoot" target="_blank">ドキュメント：SQL パフォーマンスを向上させるためのベスト・プラクティス</a>

### ECPを使用したスケーラビリティの実現

- <a href="https://docs.intersystems.com/irislatestj/csp/docbook/DocBook.UI.Page.cls?KEY=GSCALE_ecp" target="_blank">ドキュメント：分散キャッシュによるユーザ数に応じた水平方向の拡張</a>

- <a href="https://jp.community.intersystems.com/node/476811" target="_blank">記事：データプラットフォームとパフォーマンス-パート7 パフォーマンス、スケーラビリティ、可用性のためのECP</a>

---
## 8. <img src="./assets/icons/8.png" width="70%"/>
ミラーリング、定期的なバックアップ、ジャーナリングによる高可用性の実装方法を学びます。

### バックアップとリストア（シリーズ記事）

- <a href="https://jp.community.intersystems.com/node/566721" target="_blank">インターシステムズ製品をバックアップする前に確認したいこと</a>

- <a href="https://jp.community.intersystems.com/node/566816" target="_blank">外部バックアップの仕組みとバックアップとリストア方法について</a>

- <a href="https://jp.community.intersystems.com/node/566936" target="_blank">オンラインバックアップの仕組みとバックアップとリストア方法について</a>

- <a href="https://jp.community.intersystems.com/node/567071" target="_blank">並行外部バックアップの仕組みとバックアップとリストア方法について</a>

- <a href="https://jp.community.intersystems.com/node/567076" target="_blank">コールドバックアップとリストア方法について</a>

> **英語ビデオやオンラインコースもあります**
>
>- <a href="https://learning.intersystems.com/course/view.php?name=Backup%20and%20Restore" target="_blank">オンラインコース(英語）:Backup and Restore
>
>   InterSystems IRIS® data platform のバックアップとリストアの方法、および効果的なバックアップ戦略の設計について説明します。
>
>   前提学習または経験：管理ポータルおよび InterSystems IRIS の一般的なアーキテクチャについての理解が必要です。
>   
>    学習目標 このコースを修了するまでに、以下のことができるようになります：
>
>    - 外部バックアップ・ソフトウェアまたは仮想マシンのスナップショットを使用して、InterSystems IRIS 内をバックアップする利点と欠点を識別する。
>    - サイトの効果的なバックアップ戦略を設計する
>    - 外部ツールを使用した InterSystems IRIS のバックアップとリストア
>
>    >このオンラインコースは実際の演習は含まれていません。
{: .block-tip}


### ミラーリング

- <a href="https://docs.intersystems.com/irislatestj/csp/docbook/DocBook.UI.Page.cls?KEY=GHA_failover_mirror" target="_blank">ドキュメント：InterSystems IRISミラーリング</a>

    - ビデオ：ミラーリングを使用した HA および DR の構成

{% include youtube-list.html id="sp5wfKbqHuQ" list="PLzSN_5VbNaxCeC_ibw2l-xneMCwCVf-Or&index=5" %}  
<br>
- <a href="https://docs.intersystems.com/irislatestj/csp/docbook/DocBook.UI.Page.cls?KEY=GHA_mirror_monitor" target="_blank">ドキュメント：ミラーの監視</a>

### ジャーナル

- <a href="https://docs.intersystems.com/irislatestj/csp/docbook/Doc.View.cls?KEY=GCDI_journal_config" target="_blank">ドキュメント：ジャーナリングの構成</a>


---
## 9. <img src="./assets/icons/9.png" width="70%"/>
アップグレード・ガイドおよびリリース・ノートを使用して、InterSystems IRIS をアップグレードする方法をご紹介します。

- <a href="https://docs.intersystems.com/irislatestj/csp/docbook/DocBook.UI.Page.cls?KEY=GCI_overview" target="_blank">ドキュメント：アップグレードの概要</a>    

- <a href="https://docs.intersystems.com/irislatestj/csp/docbook/DocBook.UI.Page.cls?KEY=ADOCK_iris_upgrading" target="_blank">InterSystems IRISコンテナのアップグレード</a>

- <a href="https://docs.intersystems.com/irislatest/csp/docbook/DocBook.UI.Page.cls?KEY=PAGE_release" target="_blank">最新リリースノート(英語)</a>

---
## 10. <img src="./assets/icons/10.png" width="70%"/>

エラーの早期発見や問題の迅速なトラブルシューティングに役立つ多くのツールについてご紹介します。
### アプリケーションエラーログ

- <a href="https://jp.community.intersystems.com/node/508271" target="_blank">記事：メッセージ・ログ(messages.log)／コンソール・ログ(cconsole.log) に出力される「Purging Application Error Logs」のメッセージとは</a>

- <a href="https://jp.community.intersystems.com/node/508466" target="_blank">記事：アプリケーションのログを^ERRORSグローバルに入れる方法</a>

> **英語ビデオやオンラインコースもあります**
>- <a href="https://learning.intersystems.com/enrol/index.php?id=1131" target="_blank">ビデオ（英語）:Reviewing the Application Error Log</a>
{: .block-tip}

### SYSLOG

- <a href="https://jp.community.intersystems.com/node/492146" target="_blank">記事：SYSLOG - その正体と意味するもの</a>

> **英語ビデオやオンラインコースもあります**
>- <a href="https://learning.intersystems.com/course/view.php?id=1133" target="_blank">ビデオ（英語）:Reviewing the Console Log and SYSLOG</a>
{: .block-tip}

### トラブル時の情報収集

- <a href="https://docs.intersystems.com/irislatestj/csp/docbook/DocBook.UI.Page.cls?KEY=GCM_diagnostic" target="_blank">ドキュメント：InterSystems 診断レポートの使用法</a>

    概要のみお読みください

✅ <a href="https://jp.community.intersystems.com/node/489511" target="_blank">記事＋日本語ビデオ：【IRISベース】トラブル発生時の情報収集方法（IRIS ／ IRIS for Health ／ UCR 編）</a>

{% include youtube-list.html id="yFmpQFkErwI" list="PLzSN_5VbNaxCeC_ibw2l-xneMCwCVf-Or" %}  
<br>

- <a href="https://docs.intersystems.com/irislatestj/csp/docbook/DocBook.UI.Page.cls?KEY=GCM_irisstat" target="_blank">ドキュメント：irisstat ユーティリティを使用した InterSystems IRIS の監視</a>

- <a href="https://docs.intersystems.com/irislatestj/csp/docbook/DocBook.UI.Page.cls?KEY=ROARS_gsecuring_secmgmt#ROARS_gsecuring_secmgmt_emerg" target="_blank">ドキュメント：緊急アクセス</a>

- Webアプリで障害が発生した場合の対応例

    <a href="https://jp.community.intersystems.com/node/548871" target="_blank">記事「Webアプリケーションのトラブルシュート方法（ログの取得方法）」</a>

**※ 問題が解決しない場合は、システムはそのままで「診断レポート」または「^SystemCheckまたは^Buttons」を実行し、インターシステムズのサポートセンターまでお問い合わせください。**



---
## 11. <img src="./assets/icons/11.png" width="70%"/>
あなたのスキルを総動員して、基本的なシステム管理作業を実際にやってみましょう。

- <a href="https://learning.intersystems.com/course/view.php?name=ManagingIRISExercise" target="_blank">演習環境（英語ページ）:Performing Common InterSystems IRIS Management Tasks

    IRISのインストールをお試しいただけます（Ubuntuを利用）。また、インストール後にデータベースキャッシュサイズとジャーナル設定をいくつか変更します。

---
## 12. 次は？
学習を継続する場合は以下のリソースが最適です。

- <a href="https://docs.intersystems.com/irislatestj/csp/docbook/DocBook.UI.Page.cls?KEY=GOPS_troubleshoot" target="_blank">ドキュメント：トラブルシューティングの支援</a>
- <a href="https://jp.community.intersystems.com/node/477596" target="_blank">記事：「InterSystemsデータプラットフォームのキャパシティプランニングとパフォーマンス」シリーズの索引</a>
- <a href="https://www.intersystems.com/jp/intersystems-server-system-administration/" target="_blank">講師付きトレーニング：InterSystems Serverシステム管理1</a>

- <a href="https://www.intersystems.com/jp/intersystems-server-system-administration-2/" target="_blank">講師付きトレーニング：InterSystems Serverシステム管理2(セキュリティ管理編)</a>

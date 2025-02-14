---
title: 開発者向け InterSystems IRIS の管理概要
date: 2024-12-04
permalink: ManagingIRISforDeveloper.html
layout: post
---
InterSystems IRIS® data platform とその他のインターシステムズ製品の管理の基本についてハイレベルな概要を学びます。

このパスは、開発者を対象とした、InterSystems 製品のシステム管理タスク概要を学習できるパスです。

システム管理者向けのより包括的なパスについては、<a href="IRISManagementBasics.html" target="_blank">InterSysetms IRIS 管理の基本</a> をご参照ください。

---

[1. <img src="./assets/icons/1.png" width="40%"/>](#1-)

[2. <img src="./assets/icons/d2.png" width="40%"/>](#2-)

[3. <img src="./assets/icons/d3.png" width="40%"/>](#3-)

[4. <img src="./assets/icons/d4.png" width="40%"/>](#4-)

[5. 次は？](#5-次は)

---

## 1. <img src="./assets/icons/1.png" width="70%"/>
InterSystems IRIS のアーキテクチャと、システム管理に役立つツールについてご紹介します。


はじめに、InterSystems IRIS 概要と、その基盤となる基本アーキテクチャについてご紹介します。

- InterSystems 製品のアーキテクチャ概要 ～ネームスペースとデータベース～

    {% include youtube-list.html id="TNjUnuw8K_Q" list="PLzSN_5VbNaxCWpesN3ulh_EZ9sGkw09q5" %} 
<br>
- IRISの開発環境の作成方法、ネームスペース／データベースについて

    IDEからIRISに接続する方法も確認できます。

    ✅ <a href="https://jp.community.intersystems.com/node/478601" target="_blank">【はじめての InterSystems IRIS】セルフラーニングビデオ：基本その2：InterSystems IRIS で開発をはじめよう！</a>
        
    {% include youtube-list.html id="ID6ImJTgJRk" list="PLzSN_5VbNaxBPaSSINLzv-CkDJy00bOSQ" %} 
<br>

- ビデオ（英語）：Introduction to the Management Portal

    ※管理ポータルメニューは日本語で表示できますが、ビデオでは英語表記の例でご紹介しています。
    {% include youtube.html id="uHEoktZG9r0" %} 
<details class="transcript2">
<summary> ▶日本語字幕 </summary>
<div class="content">
InterSystems 製品の管理ポータルは、システム管理タスクのホームです。このビデオでは、InterSystems IRIS for Health を使用していますが、ここで説明する内容のほとんどは他の InterSystesm 製品と共通です。
<br>
管理ポータルのホームページには、ヘッダと本文があります。ヘッダ内のタイトル・バーには、「ホーム」、「バージョン情報」、「ヘルプ」、「連絡先」、「ログアウト」 のハイパーリンクのほか、ユーザの役割に応じたタスクにすばやくアクセスできるメニューがあります。
<br>
また、サーバ名、現在のネームスペース、ユーザ、ライセンスなど、インスタンスに関する情報も表示されます。リボン内の検索ボックスを使用するとメニュー・オプションをナビゲートすることなくネームスペースの管理など、特定のトピックに関する機能を見つけることができます。
<br>
ページ本体に移動すると一番左の列には様々な主要カテゴリのタブがあります。最初のタブでホームページに戻り、2番目のタブで IRIS for Health 固有の機能に移動します。HealthShare インスタンスでは、このタブは Health ではなく HealthShare と表示されることに注意してください。
<br>
[Analytics] タブは、認証されたユーザーを分析機能が設定されている製品エリアに案内します。これらのツールのほとんどは、アナリストやデータを管理するユーザーのためのものですが、管理者メニューの選択肢の中には、ログ、データのインポートに使用されるフォルダマネージャー、ユーザーポータルの設定などへのアクセスがあります。
<br>
[Interoperability] タブでは、プロダクション、メッセージ、ビジネスルール、およびシステムのその他の相互運用性機能にアクセスできます。システム管理者は、[構成する]、[表示]、[モニタ] および [管理] メニュー内の項目に精通している必要があります。
<br>
次の3つのタブには、システム管理者が扱う最も一般的な管理機能の多くが含まれています。
<br>
[システムオペレーション] タブでは、確立されたシステムを稼動し続けるために必要な多くのツールにアクセスできます。これには、パフォーマンス・メトリクスを表示するシステム・ダッシュボードのほか、多数の運用トピックが含まれます。
<br>
[システム・エクスプローラ] タブは、クラス、SQL、ルーチン、グローバル、ツールへのアクセスを提供します。特筆すべきは、クラスのオプションを使用して、クラスをインポートおよびエクスポートしたり、クラス・ドキュメントを表示したりできることです。
<br>
SQL オプションを使用すると、テーブル、ビュー、プロシージャ、およびクエリにアクセスしたり、クエリエディタから独自の SQL クエリを実行したりできます。
<br>
最後に [システム管理] タブでは、構成、セキュリティ設定、ライセンス、暗号化を含むシステム構成設定にアクセスできます。
</div>
</details>
<br>

- <a href="https://learning.intersystems.com/enrol/index.php?id=1433" target="_blank">ビデオ（英語）：Using the InterSystems Terminal</a>

    ターミナルで、タイプ：%Status のエラーを受け取った場合の確認方法については、以下 <a href="https://github.com/Intersystems-jp/ObjectScriptCookBook" target="_blank">ObjectScriptクックブック</a> の項目をご参照ください。

    ✅ <a href="https://github.com/Intersystems-jp/ObjectScriptCookBook/blob/master/CookBook.md#status%E3%81%AE%E3%82%A8%E3%83%A9%E3%83%BC%E3%81%8C%E6%88%BB%E3%81%A3%E3%81%A6%E3%81%8D%E3%81%9F%E3%82%89" target="_blank">%Statusのエラーが戻ってきたら</a>

---

## 2. <img src="./assets/icons/d2.png" width="70%"/>

ユーザーを作成し、対応するロールに接続することで、必要なものにはロールベースでアクセスできるようにし、ロールに関係のないデータやツールへのアクセスを禁止します。次に、データベースを暗号化することで安全なデータを確保する方法をご覧ください。

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

- <a href="https://learning.intersystems.com/enrol/index.php?id=2157" target="_blank">演習環境付き演習（英語）:Configuring Role-Based Access</a>

    演習の例では、管理ポータルで使用する 2 種類のマネージャ・ロールの設定方法を示しています。最初のロールは、ユーザ定義やロール定義などのセキュリティ関連項目の変更を許可するページにアクセスできます。
    
    2つ目のロールにはそのようなアクセス権はありません。また、これらのロールを持つユーザが管理ポータルとどのようにやり取りするかも説明します。
    
    なお、LDAP もサポートされていますが、この演習では取り上げません。

- <a href="https://docs.intersystems.com/irislatestj/csp/docbook/DocBook.UI.Page.cls?KEY=ROARS_encrypt" target="_blank">ドキュメント：暗号化</a>

---
## 3. <img src="./assets/icons/d3.png" width="70%"/>
ログを使用してエラーを早期に特定し、問題をトラブルシューティングする方法をご覧ください。

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

## 4. <img src="./assets/icons/d4.png" width="70%"/>
冗長性と自動監視を組み込むことで、システムを効果的に稼働させ続ける方法を学びましょう。

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
<br>

---

## 5. 次は？
学習を継続する場合は以下のリソースが最適です。

- <a href="https://learning.intersystems.com/enrol/index.php?id=1945" target="_blank">演習環境（英語ページ）:Performing Common InterSystems IRIS Management Tasks</a>

    IRISのインストールをお試しいただけます（Ubuntuを利用）。また、インストール後にデータベースキャッシュサイズとジャーナル設定をいくつか変更します。

- <a href="IRISManagementBasics.html" target="_blank">ラーニングパス：InterSysetms IRIS 管理の基本</a>

- <a href="https://docs.intersystems.com/irislatestj/csp/docbook/DocBook.UI.Page.cls?KEY=PAGE_administration" target="_blank">ドキュメント：管理</a>

- <a href="https://www.intersystems.com/jp/intersystems-server-system-administration/" target="_blank">講師付きトレーニング：InterSystems Serverシステム管理1</a>

- <a href="https://www.intersystems.com/jp/intersystems-server-system-administration-2/" target="_blank">講師付きトレーニング：InterSystems Serverシステム管理2(セキュリティ管理編)</a>

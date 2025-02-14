---
title: ビジネス・インテグレーションの構築
date: 2024-12-07
permalink: BuildingBusinessIntegration.html
layout: post
---
<!-- 
>オリジナル[Building Business Integrations with InterSystems IRIS](https://learning.intersystems.com/course/view.php?id=1437)
-->
InterSystems 製品の相互運用性（Interoperability）フレームワークによりインターフェイスエンジニアやソフトウェア開発者は、複数のシステムを接続し下流のアプリケーションにメッセージを迅速にルーティングすることができます。

このパスでは、統合（インテグレーション）の基本を学び組み込みオプションやカスタムオプションを使用してデータを送信、受信、処理、変換する方法を確認できます。

[1. <img src="./assets/icons/1.png" width="40%"/>](#1-)

[2. <img src="./assets/icons/BIntegration2.png" width="40%"/>](#2-)

[3. <img src="./assets/icons/BIntegration3.png" width="40%"/>](#3-)

---
## 1. <img src="./assets/icons/1.png" width="70%"/>

最初に、IRISのInteroperability（相互運用性）機能でどのようなことができ、どのような開発が必要になるかについて確認します。

- ビデオ：Interoperability概要

    12分以降をご覧ください。

    {% include youtube-list.html id="vo12UnH-c-s" list="PLzSN_5VbNaxD-r8wU4LHwLwGSzUjrffEX&index=1&t=1203s" %}
<br>
- シリーズ記事：<a href="https://jp.community.intersystems.com/node/483036" target="_blank">【はじめてのInterSystems IRIS】Interoperability（相互運用性）：動作の仕組みを知ろう</a>

- シリーズ記事：<a href="https://jp.community.intersystems.com/node/483041" target="_blank">【はじめてのInterSystems IRIS】Interoperability（相互運用性）：プロダクションとは</a>


> **英語ビデオやオンラインコースもあります**
>
> - <a href="https://learning.intersystems.com/course/view.php?name=Interop%20QS" target="_blank">体験環境付き演習：Receiving and Routing Data in a Production</a>
>
>   システム間でのデータ共有は、InterSystems IRIS data platform ほど、簡単なものはありません。複数システムからデータを収集し、定義したロジックに従ってメッセージをルーティングし、共通のプロトコルと複数の言語を使って接続します。InterSystems IRIS では、以下のことが可能です。
>   - メタデータ、またはメッセージの内容に基づいてメッセージをルーティング
>   - ローコード（最小限のコードの記述ができる）UI でビジネスロジックを適用、更新可能
>   - ダウンストリームシステム用にプログラムでデータ変換が可能
>   - すぐに統合が可能なコンポーネントが用意されている。あるいは、独自のコードを記述してさらに柔軟性を高める事が可能
>   - 機械学習アルゴリズムを搭載したシステムからのデータフローに対応
>   - 統合データを1つのリポジトリに保存し、より詳細な分析を行う
>   - メッセージを追跡して、トラブルシューティング、また監査が容易に可能
>
>   - <a href="http://github.com/intersystems/Samples-Integration-RedLights" target="_blank">演習内容</a>
>
>- <a href="https://learning.intersystems.com/course/view.php?name=Integration%20Architecture" target="_blank">オンラインコース（英語）：Integration Architecture</a>
>
>    InterSystems IRIS® data platform、InterSystems HealthShare® の統合機能の基本的なアーキテクチャを学習します。これらのコンポーネントを通じてデータがどのように流れ、システム間の相互運用が可能になるかを学びます。
{: .block-tip}

---
## 2. <img src="./assets/icons/BIntegration2.png" width="70%"/>
InterSystems IRIS に組み込まれているグラフィカル・ツールを使用して、メッセージを取り込み、正しい形式で下流のシステムに渡します。

- 記事：<a href="https://jp.community.intersystems.com/node/494326" target="_blank">レコードマップで何ができるか？</a>

- 記事：<a href="https://jp.community.intersystems.com/node/483136" target="_blank">【はじめてのInterSystems IRIS】Interoperability（相互運用性）：コンポーネントの作成（ビジネス・オペレーション）</a>  

- ビデオ：ルーティング・ルールの設定

    ※同様の内容で新ルール・エディタに対応しているビデオは以下英語版をご覧ください。

    {% include youtube-list.html id="4tG-txYZwtg" list="PLzSN_5VbNaxCWpesN3ulh_EZ9sGkw09q5&index=9" %}

<details class="transcript2">
<summary> ▶日本語字幕 </summary>
<div class="content">
このビデオでは、ルール・エディタを使用してカスタム・ビジネス・ルールを作成しデータ統合のフローと実行を管理する方法についてご説明します。
<br>
ビジネス・ルールは、通常 Buisiness Process の内部で使用されユーザーが重要なデータの決定をグラフィカルに編集できる画面です。
<br>
例えば、InterSystems IRIS を使用し赤信号の違反監視カメラからの入力データを監視しているとします。
<br>
データは、ビジネス・サービス：Real Time Red Light Violation を通じて InterSystems IRIS に取り込まれビジネス・プロセス：Demo Ticket BPL に送信され違反したドライバーがチケットを受け取るべきか、データを Archive に直接送信すべきかを判断します。
<br>
このプロセスは、緊急車両などのホワイトリストに登録された車両を識別し、車両がホワイトリストに登録されていない場合のみ、ビジネス・オペレーション：To Ticket Application を呼び出します。
<br>
この流れを確認してみましょう。
<br>
ビジネス・プロセスでは、Car Type Field をチェックするルールアクションが設定されています。
<br>
ルールが緊急車両のタイプと一致する場合、その車両がホワイトリストに登録されていることを示す位置を返します。
<br>
ビジネス・プロセスは、ルールの結果である 1 または 0 の結果を contextプロパティ、この場合は context.Whitelisted に保存します。
<br>
ルールの結果は、ビジネス・プロセスの設定にある、ルール・アクティビティの Result Location Field に保存します。
<br>
ここで、このルールを更新する必要が出てきました。
<br>
この自治体では、しばした街頭でパレードや政治的デモが行われていることがわかりました。
<br>
これらの更新に参加するドライバーは、イベント中のみ赤信号を走ることが許可されています。
<br>
私たちは、ホワイトリストに登録された民間人のテーブルと照らし合わせ違反をチェックし、それがホワイトリストに登録された時間枠外で発生した場合のみ違反チケットを送信するようにビジネス プロセスを更新する必要があります。
<br>
最初の手順は、ビジネス・プロセス context を編集することです。
<br>
ビジネス・ルールは、このコンテキストに明示的持ち込まれたデータにのみアクセスできますが、要求メッセージに直接アクセスすることはできません。
<br>
違反レコードをホワイトリストに登録された一般人と比較するルールを有効にするには、これらのレコードをビジネス・プロセスのローカルの値として割り当てる必要があります。
<br>
必要な値は、違反日時、ナンバープレート番号、もしあればその車両がホワイトリストに登録された日付、パレードの開始時間と終了時間です。
<br>
次に、assign アクションを使用して、ビジネス・プロセスに送信される基本要求の値をこれらのコンテキスト・プロパティに代入する必要があります。
<br>
ホワイトリストのレコードは、データベースにあるテーブルから検索する必要があるため SQL クエリーアクションを作成する必要があります。
<br>
このプロセスは、Demo.civWhiteList と呼ばれるテーブルを検索します。
<br>
このテーブルには、ホワイトリストに登録された、すべての民間人のナンバープレートと、その猶予期間の時間が記録されています。
<br>
ビジネス・プロセスは、違反のナンバープレートと一致するホワイトリストに登録された車両の記録を探します。
<br>
SQLクエリから返送されるカラム値は、into contextプロパティ名　のシンタックスで、直接 context プロパティの値にアサインできます。
<br>
必要な context プロパティへの割り当てが終了しました。
<br>
ルールエディタを開き、ルールセットに新しいルールを追加してみましょう。
<br>
緑のプラスボタンをクリックすると、要素を追加できます。
<br>
ここでは、rule を追加し、ルール名に Check Civilian Whitelist を設定します。
<br>
次に、rule の下に条件を設定するための when を追加します。

最初の条件は、SQLクエリが空であるかどうかをチェックします。
<br>
White List Date の値を使用して、クエリによって更新されたフィールドが空文字列と等しいかどうかをチェックすることができます。
<br>
検索でホワイトリストのレコードが見つからなかった場合、これ以上行うことはありません。
<br>
検出された違反が、ホワイトリストに登録されていないことを示す 0 を返す Return 要素を作成することができます。
<br>
return を使用してルールの実行を終了すると、それ以降のルールが評価されなくなります。
<br>
次に、2つ目の when を作成し違反がその車両がホワイトリストに登録された日に行われたかどうかをチェックします。
<br>
2つ目の condition フィールドをダブルクリックすると、式エディタを開くことができます。
<br>式エディタは、複雑な式をグラフィカルに作成することで式の作成を簡単にできるツールです。
<br>
すべての比較演算しを一覧表示する Operationボタンをクリックし、等号を選択して式を開始することができます。
<br>
日付が文字列形式で記録されているため、比較する前に日付オブジェクトに変換する必要があります。これを行うには、式エディタの組み込み関数を使用します。
function ボタンをクリックして、Convert Date Timeを選択します。
<br>
そして、値フィールド　Date　を入れ残りは空白にします。
<br>
同様に、White List Date も設定します。
<br>
次に、日付比較ルールが true と評価された場合にのみ、評価される and 文を作成します。
<br>
言い換えると違反の日付がホワイトリストに登録されているかどうかをチェックし、それが承認された期間内であるかどうかをチェックします。
<br>
先ほど作成した式エディタで And 要素を選択し、再度 Operation ボタンをクリックします。
<br>
違反がホワイトリストに登録された開始時刻の後、終了時刻の前に発生したものであるかどうかをチェックする必要があります。
<br>
結果として違反車は、パレードの帰りに赤信号を無視した可能性があります。
<br>
最初に、違反時間が猶予期間の開始時刻以上であるかをチェックします。そして、終了時刻以下であるかもチェックします。
<br>
これらの条件の両方が満たされた場合、違反時刻にその車両がホワイトリストに登録されていたことを示すため、ビジネス・プロセスに 1 を返します。
<br>
これにより、ビジネス プロセスはこの情報を使って To Ticket オペレーションを呼び出したり、単にレコードを　Archive　に渡すことができます。
<br>
このビデオを通して、ルール エディタを使用したビジネス ルールの作成方法を学習できました。
<br>
ルール エディタの使用方法についてより詳しくは、ドキュメントをご参照ください。
</div>
</details>
※新エディタでの解説ビデオ：<a href="https://learning.intersystems.com/course/view.php?name=Setting%20Up%20Business%20Rules" target="_blank">（英語）:Setting Up Business Rules</a>
<br>

> **英語ビデオやオンラインコースもあります**
>- <a href="https://learning.intersystems.com/enrol/index.php?id=1094" target="_blank">ビデオ（英語）：Record Mapper Introduction</a>
>
>- <a href="https://learning.intersystems.com/course/view.php?name=Building%20BPL%20Business%20Processes" target="_blank">オンラインコース（英語）:Building BPL Business Processes</a>
>
>    管理ポータルのビジネス・プロセス・デザイナーを使用して、BPL ビジネス・プロセスを構築する方法を学びます。このコースには、6 つのインストラクションレッスンといくつかのクイズ問題が含まれています。
>
>    このオンラインコース受講に必要な前提知識は以下の通りです（コンポーネントそれぞれの役割とプロダクション構成の画面操作ができること＋ビジネスオペレーションの作成方法を知っていること）。
>
>- <a href="https://learning.intersystems.com/course/view.php?name=Data%20Transformations%20Basics" target="_blank">オンラインコース（英語）:Data Transformations Basics</a>
>
>   グラフィカルな管理ポータル・インタフェースを使用して、データ変換を作成する方法を学びます。フィールドをマップする方法、フィールドを変更する関数を使用する方法、およびフィールドの値としてリテラルを使用する方法をご覧ください。最後に、変換をテストして実装する方法を学びます。
>
>   >メモ：前提知識にHL7について知っていることが含まれています。
{: .block-tip}

---
## 3. <img src="./assets/icons/BIntegration3.png" width="70%"/>

プロダクションですぐに使える機能をの他に、ニーズに合わせて ObjectScript を使用してカスタムコンポーネントを作成することができます。

- 記事：<a href="https://jp.community.intersystems.com/node/483131" target="_blank">【はじめてのInterSystems IRIS】Interoperability（相互運用性）：メッセージ</a>

- 記事：<a href="https://jp.community.intersystems.com/node/483136" target="_blank">【はじめてのInterSystems IRIS】Interoperability（相互運用性）：コンポーネントの作成（ビジネス・オペレーション）</a>
- 記事：<a href="https://jp.community.intersystems.com/node/483186" target="_blank">【はじめてのInterSystems IRIS】Interoperability（相互運用性）：コンポーネントの作成（ビジネス・サービス）</a>

    - 記事：<a href="https://jp.community.intersystems.com/node/559356" target="_blank">REST経由で情報を入力する場合の Interoperability（相互運用性機能）のサンプル</a>

> **英語ビデオやオンラインコースもあります**
>- <a href="https://learning.intersystems.com/course/view.php?name=Custom%20Messages" target="_blank">ビデオ（英語）：Building Custom Production Messages
>
>- <a href="https://learning.intersystems.com/course/view.php?name=Building%20Custom%20Business%20Operations" target="_blank">オンラインコース（英語）：Building Custom Business Operations</a>
>
>- <a href="https://learning.intersystems.com/course/view.php?name=Building%20Custom%20Business%20Services" target="_blank">オンラインコース（英語）:Building Custom Business Services (1h 30m)</a>
{: .block-tip}


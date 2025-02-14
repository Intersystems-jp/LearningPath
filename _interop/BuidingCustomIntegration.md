---
title: Interoperability：カスタムコンポーネントの作成
date: 2024-12-08
permalink: BuidingCustomIntegration.html
layout: post
---
<!-- 
>オリジナル：[Building Custom Integrations](https://learning.intersystems.com/course/view.php?id=397)
-->
InterSystems ObjectScript で Interoperability（相互運用性機能）のカスタムコンポーネントを作成し、InterSystems IRIS® data platform 製品に追加する方法を学習します。

このパスは、プロダクションで使用するカスタムビジネスサービス、プロセス、およびオペレーションを開発するソフトウェア開発者向けに設計されています。

また、InterSystems ObjectScript の使用経験があることを前提としています。必要に応じて、<a href="ObjectScript.html" target="_blank">InterSystems ObjectScript 入門</a> をご覧ください。

※ 講師付きトレーニングコースで学習することもできます👉<a href="https://www.intersystems.com/jp/system-integration-tool/" target="_blank">システム統合機能の使い方</a>

[1. <img src="./assets/icons/InteropC1.png" width="40%"/>](#1-)

[2. <img src="./assets/icons/InteropC2.png" width="40%"/>](#2-)

[3. <img src="./assets/icons/InteropC3.png" width="40%"/>](#3-)

---
## 1. <img src="./assets/icons/InteropC1.png" width="70%"/>

最初に、Interoperability のカスタムコンポーネントを利用した開発を体験してみましょう。

- <a href="https://play.instruqt.com/embed/intersystems/tracks/interop-jp?token=em_nMyn9Z_6s9Tq3KTv" target="_blank">チュートリアル：InterSystems Interoperability（相互運用性）チュートリアル</a>

    事前準備なしのチュートリアルでブラウザ上でお試しいただけます。体験内容概要については、以下記事をご参照ください。

    ✅ 記事：<a href="https://jp.community.intersystems.com/node/538781" target="_blank">IRIS の Interoperability（相互運用性）を試せるチュートリアル</a>

> **英語版体験環境もあります**
>
>- <a href="https://learning.intersystems.com/course/view.php?name=Interop%20QS" target="_blank">体験環境付き演習（英語／日本語字幕あり）：Receiving and Routing Data in a Production</a>
>
{: .block-tip}

Interoperability 概要について確認される場合は、以下のビデオの 12 分以降をご覧ください。

{% include youtube-list.html id="vo12UnH-c-s" list="PLzSN_5VbNaxD-r8wU4LHwLwGSzUjrffEX&index=1&t=1203s" %}

<br>
この他、はじめて Interoperability を操作される方向けのシリーズ記事もあります。    

- <a href="https://jp.community.intersystems.com/node/483036" target="_blank">【はじめてのInterSystems IRIS】Interoperability（相互運用性）：動作の仕組みを知ろう</a>

- <a href="https://jp.community.intersystems.com/node/483041" target="_blank">【はじめてのInterSystems IRIS】Interoperability（相互運用性）：プロダクションとは</a>


---
## 2. <img src="./assets/icons/InteropC2.png" width="70%"/>

続いて、プロダクション内のカスタム・コンポーネント間で使用するメッセージの構築方法を確認します。

- <a href="https://jp.community.intersystems.com/node/483131" target="_blank">【はじめてのInterSystems IRIS】Interoperability（相互運用性）：メッセージ</a>

> **英語ビデオもあります**
>- <a href="https://learning.intersystems.com/course/view.php?id=416" target="_blank">ビデオ：Building Custom Production Messages</a>
{: .block-tip}

---
## 3. <img src="./assets/icons/InteropC3.png" width="70%"/>

プロダクション向けのカスタム・ビジネス・オペレーション、ビジネス・プロセス、ビジネス・サービスを設計、構築する方法を学習します。


- <a href="https://jp.community.intersystems.com/node/483136" target="_blank">【はじめてのInterSystems IRIS】Interoperability（相互運用性）：コンポーネントの作成（ビジネス・オペレーション）</a>

- <a href="https://jp.community.intersystems.com/node/483171" target="_blank">【はじめてのInterSystems IRIS】Interoperability（相互運用性）：コンポーネントの作成（ビジネス・プロセス）</a>

    - ビデオ：バッチジョブ管理への応用から学ぶ ～インターオペラビリティ機能の ビジネスプロセスを理解する
        
        {% include youtube-list.html id="RUxeT4cTy4k" list="PLzSN_5VbNaxB39_H2QMMEG_EsNEFc0ASz&index=6" %}
<br>
- <a href="https://jp.community.intersystems.com/node/483186" target="_blank">【はじめてのInterSystems IRIS】Interoperability（相互運用性）：コンポーネントの作成（ビジネス・サービス）</a>

- <a href="https://jp.community.intersystems.com/node/559356" target="_blank">REST経由で情報を入力する場合の Interoperability（相互運用性機能）のサンプル</a>




> **英語のオンラインコースもあります**
>
>- <a href="https://learning.intersystems.com/course/view.php?name=Building%20Custom%20Business%20Operations" target="_blank">オンラインコース（英語）：Building Custom Business Operations (1h 30m)</a>
>
>- <a href="https://learning.intersystems.com/course/view.php?name=Building%20BPL%20Business%20Processes" target="_blank">オンラインコース（英語）：Building BPL Business Processes (1h 30m)</a>
>- <a href="https://learning.intersystems.com/course/view.php?name=Building%20Custom%20Business%20Services" target="_blank">オンラインコース（英語）：Building Custom Business Services (1h 30m)</a>
{: .block-tip}
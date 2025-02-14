---
title: VS Code を使用した InterSystems サーバサイドの開発
date: 2024-12-05
permalink: VSCode.html
layout: post
---
VS Code を使用した InterSystems® 製品の開発方法をご紹介します。

複数の InterSystems サーバでの作業、クライアントサイドまたはサーバサイドでのクラス編集、InterSystems ターミナルへのアクセスなどをご確認いただけます。

[1. <img src="./assets/icons/vscode1.png" width="40%"/>](#1-)

[2. <img src="./assets/icons/vscode2.png" width="40%"/>](#2-)

[3. <img src="./assets/icons/vscode3.png" width="40%"/>](#3-)

[4. <img src="./assets/icons/vscode4.png" width="40%"/>](#4-)

---

## 1. <img src="./assets/icons/vscode1.png" width="70%"/>

VS Code のインストール方法、インターフェイスの使用方法、および VS Code を InterSystems インスタンスに接続する方法を確認できます。

ObjectScript　用エクステンションを使用することで、フルスタック・アプリケーションの作成、テスト、およびデプロイを行うことができます。

- <a href="https://jp.community.intersystems.com/node/482976" target="_blank">記事：VSCodeを使ってみよう</a>


> **英語ビデオやオンラインコースもあります**
>
>- <a href="https://docs.intersystems.com/components/csp/docbook/DocBook.UI.Page.cls?KEY=GVSCO_install" target="_blank">ドキュメント（英語）：Installation</a>
>
>- <a href="https://learning.intersystems.com/enrol/index.php?id=1458" target="_blank">ビデオ（英語）：Install and Use ObjectScript Extensions for VS Code</a>
>
>- <a href="https://learning.intersystems.com/course/view.php?id=2552" target="_blank">オンラインコース（英語）:Installing VS Code and Configuring InterSystems Server Connections</a>
>
>    Visual Studio Code で最新の InterSystems 拡張機能を体験します。VS Code は、InterSystems サーバ上で開発するために推奨される IDE です。VS Code は、ファイル・ブラウズやターミナルなどの典型的な IDE 機能を提供する Microsoft のオープン・ソース製品です。 この演習では、VS Code を使用して InterSystems サーバに接続する複数の方法について説明します。
>
{: .block-tip}

---

## 2. <img src="./assets/icons/vscode2.png" width="70%"/>

コーディングを始める前に、VS Codeでワークスペースを設定する方法を学びましょう。

- <a href="https://jp.community.intersystems.com/node/482976#2" target="_blank">記事：VSCodeを使ってみよう:2、サーバへ接続する

    VSCodeのワークスペース単位に接続先を切り替えたいときに便利な利用方法で、ワークスペース内に接続用ファイル（settings.json）を配置する方法です。

 {% include youtube-list.html id="ID6ImJTgJRk" list="PLzSN_5VbNaxBPaSSINLzv-CkDJy00bOSQ&index=3" %}
 ※ 22:30以降をご覧ください
 <br>

- <a href="https://jp.community.intersystems.com/node/493616" target="_blank">記事：VSCode を使ってみよう (2021年4月20日版)</a>

    サーバーサイド編集を有効化する方法です（スタジオと同じ使い勝手の利用方法でサーバー側コードを直接編集＆コンパイルができる方法です）。

> **英語ビデオやドキュメントもあります**
>
>- <a href="https://docs.intersystems.com/components/csp/docbook/DocBook.UI.Page.cls?KEY=GVSCO_connect" target="_blank">ドキュメント（英語）:Configure the InterSystems VS Code Extensions</a>
>
>- <a href="https://learning.intersystems.com/course/view.php?name=VSCodeWorkspaces" target="_blank">ビデオ（英語）:Configuring VS Code Workspaces for Multiple ObjectScript Connections 
>    InterSystems ObjectScript Extension Pack を使用して VS Code を構成し複数のサーバ接続をサポートする方法を説明します。
>
>   ワークスペース構成の基本を確認し、システムに必要な構成を決定してからシングルフォルダおよびマルチルートのワークスペースに関する手順に従って操作を行ってください。
>
>   このビデオでは、2 つの構成を紹介します：
>
>   - マルチルートのワークスペースと仮想フォルダを使用して、複数の InterSystems IRIS® data platform のネームスペースまたはサーバにまたがってコードを表示しサーバ側で編集を行います。
>
>   - 複数の VS Code ワークスペース（それぞれ固有のアクティブな接続を持つ）を使用して、複数のネームスペースまたはサーバーのコードを表示しクライアント側でコードを編集します。また、単一フォルダのワークスペースでサーバー側の編集を有効にすることもできます。
>
>    >メモ：ユーザ／ワークスペース／フォルダ単位のどの設定になるのかを説明しています（サーバ側編集のIRISが多い環境だとマルチルートワークスペース使うと１VSCodeで作業できて便利です。シングルフォルダワークスペースはクライアント側で編集＋同期の開発をしたい場合に最適です）。
{: .block-tip}

---

## 3. <img src="./assets/icons/vscode3.png" width="70%"/>

クラス定義の作成、InterSystems ターミナルのオープン、クラスのインポートおよびエクスポート、デバッガの実行など、VS Code での基本的な開発タスクの実行方法を確認できます。

- <a href="https://jp.community.intersystems.com/node/482976#3" target="_blank">記事：VSCodeを使ってみよう:3、クラス定義を作ってみる</a>

- <a href="https://jp.community.intersystems.com/node/482976#5" target="_blank">記事：VSCodeを使ってみよう:5、デバッグの実行</a>

- <a href="https://jp.community.intersystems.com/node/489221" target="_blank">記事：VSCode：プロセスにアタッチしてデバッグする方法</a>

 {% include youtube.html id="NBITqPlMf1M" %}
<br>
- <a href="https://jp.community.intersystems.com/node/562811" target="_blank">記事：IRIS ターミナルへのアクセス: Visual Studio Code ユーザー向け総合ガイド</a>

> **英語ビデオやドキュメントもあります**
>
>- <a href="https://learning.intersystems.com/course/view.php?name=VSCodeClasses" target="_blank">ビデオ（英語）：Working with Classes in VS Code for Client-Side Editing</a>
>
>- <a href="https://learning.intersystems.com/course/view.php?id=2563" target="_blank">オンラインコース（英語）:Creating an InterSystems Class Definition in VS Code</a>
>
>    クラス定義の構造と基本構文、および VS Code での InterSystems クラス定義の開発方法を学習します。また、プロパティ、パラメータ、メソッドなどのクラス・メンバの定義方法についても学習します。
> 
>- <a href="https://learning.intersystems.com/course/view.php?name=VSCodeDebugging" target="_blank">ビデオ（英語）:VS Code Debugger for InterSystems ObjectScript</a>
{: .block-tip}

---
## 4. <img src="./assets/icons/vscode4.png" width="70%"/>

この最終評価で学習した内容を復習し、デジタルバッジを獲得しましょう！問題にアクセスするためには、USラーニングサービスのパスのチェックボックスを全て✅する必要があります。

> デジタルバッジはコミュニティのあなたのプロフィールページと連携できます。

<a href="https://learning.intersystems.com/course/view.php?id=1678" target="_blank">USラーニングサービスのパス</a>

👉<a href="https://learning.intersystems.com/mod/quiz/view.php?id=16395" target="_blank">問題を試す
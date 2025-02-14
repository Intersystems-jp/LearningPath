---
title: InterSystems IRIS のコンテナとクラウドへの展開
date: 2024-12-01
permalink: DeployingIRISContainerAndCloud.html
layout: post
---
<!-- 
>オリジナル：[Deploying InterSystems IRIS in Containers and the Cloud](https://learning.intersystems.com/enrol/index.php?id=2141)-->

スケーラブルなデプロイメント戦略を使用して、InterSystems IRIS® data platform の実装に信頼性を追加できます。

このパスでは、InterSystems IRIS のクラウドおよびコンテナベースのデプロイメントを作成する方法を解説します。

最初にシステムとデプロイメントの仕様概要を説明します。次に、デプロイメント毎の例をご覧いただきシステムに最適なアプローチを確認することができます。

---

[1. <img src="./assets/icons/Container1.png" width="40%"/>](#1-)

[2. <img src="./assets/icons/Container2.png" width="40%"/>](#2-)

[3. <img src="./assets/icons/Container3.png" width="40%"/>](#3-)

[4. <img src="./assets/icons/Container4.png" width="40%"/>](#4-)

---
## 1. <img src="./assets/icons/Container1.png" width="70%"/>

クラウドまたはコンテナへの InterSystems IRIS のデプロイの準備として、システムとデプロイに必要な内容を決定します。

### システム要件
InterSystems IRIS の新規導入を開始する際には、以下のようなシステム要件の詳細な説明を作成します。

- システム・ユーザの数と開発者や管理者などの役割
- 接続する外部システムの数
- 想定されるデータベース・サイズとデータ・フロー量
- サーバーの可用性ニーズ

### デプロイの仕様
次に、いくつかの重要な技術的質問に答えながら、デプロイの仕様を作成します。

- 何台のインスタンスが必要で、どこにデプロイするのか？
- 各インスタンスに必要なデータベースと機能は何か。
- どの程度までデプロイを自動化するか?
- 将来のアップデートはどのように計画しているか？
- インストール時使用するサードパーティソフトウェアがある場合はそれは何ですか？
- 実装ではシャーディングを使用しますか？
- 実装ではミラーリングを使用しますか？

> **オリジナル英語ページ**
><a href="https://learning.intersystems.com/mod/page/view.php?id=13225" target="_blank">Job Aid: Define system requirements and deployment specifications</a>
{: .block-tip}
---
## 2. <img src="./assets/icons/Container2.png" width="70%"/>

InterSystems IRIS をコンテナやクラウドに導入するための戦略をご紹介します。

✅ ビデオ：Docker コンテナ版 InterSystems IRIS data platform の勧め

{% include youtube-list.html id="yY8BLUYp5IA" list="PLzSN_5VbNaxAUiQkx5d22TX0zjx4Mmqhb&index=1" %}
<br>

✅ ビデオ：Kubernetes での IRI Sの運用とそれを支える仕組み

{% include youtube-list.html id="yKX8wB9d2cs" list="PLzSN_5VbNaxC2mfu1cYvn9pfbJRs7xtkk&index=1" %}
<br>

> **英語ビデオもあります**
>- <a href="https://learning.intersystems.com/course/view.php?name=ContainerTools" target="_blank">ビデオ（英語）:Tools for Running and Deploying InterSystems Containers</a>
>
>    InterSystems IRIS® data platform で利用可能なデプロイメント・ツールについて学ぶことで、ニーズに合ったコンテナ・ベースのシステムを設計することができます。
>
>    このビデオでは
>    - コンテナと Docker の基本を確認します。
>    - InterSystems IRIS 組み込みの 2 つのデプロイ機能、永続的な %SYS と構成のマージについて学びます。
>    - デプロイメント・プラットフォームの利点を紹介します（InterSystems Kubernetes Operator）
>
>    > InterSystems Cloud Manager についてビデオの説明に含まれていますが、バージョン 2023.3より deprected となりました。
>
>- <a href="https://learning.intersystems.com/course/view.php?name=Distributed%20Deployments" target="_blank">ビデオ（英語）：Using Distributed Deployments to Improve Scalability, Compliance, and Availability</a>
{: .block-tip}

---
## 3. <img src="./assets/icons/Container3.png" width="70%"/>

- <a href="https://learning.intersystems.com/enrol/index.php?id=888" target="_blank">ビデオ（英語）:Docker Containers and InterSystems IRIS</a>

    このビデオシリーズでは、Docker コンテナとその用途を紹介し、InterSystems IRIS® data platform 組み合わせた場合にいかに効果的であるかを紹介しています。
    
    また、コンテナが継続的インテグレーション、継続的デプロイメント（CICD）アプローチにどのように適合するかもご理解いただけます。

- Dockerを使用して InterSystems IRIS Community Edition を動かす

    記事：<a href="https://jp.community.intersystems.com/node/545786" target="_blank">InterSystemsコンテナレジストリの使い方とコンテナ開始までの流れ（解説ビデオ付き）</a>

    {% include youtube-list.html id="HEGWVP0PIfI" list="PLzSN_5VbNaxAUiQkx5d22TX0zjx4Mmqhb&index=2" %}

<br>

> **英語のビデオもあります**
>- <a href="https://learning.intersystems.com/enrol/index.php?id=1762" target="_blank">ビデオ（英語）:Run InterSystems IRIS Community Edition Using Docker</a>
{: .block-tip}

- <a href="https://learning.intersystems.com/course/view.php?id=2170" target="_blank">体験環境付き演習（英語）：Deploying and Customizing InterSystems IRIS Containers</a>

- <a href="https://learning.intersystems.com/course/view.php?id=1624" target="_blank">ビデオ（英語）：Automating the Configuration of InterSystems IRIS Instances</a>

    CPF マージ機能により、InterSystems IRIS® data platform インスタンスの最終的な状態を簡単かつ宣言的な方法で定義する事ができます。
    
    このビデオでは、CPF マージを利用したクラウドネイティブで GitOps のようなコンフィギュレーション操作についてご説明します。

    ✅ <a href="https://github.com/intersystems-community/configuration-merge-file-2020.4" target="_blank">サンプルコード</a>：コンテナ化されたデプロイメント用の構成ファイルの使用方法の例がいくつか含まれています。

    - Docker-compose ファイル
    - CPFマージファイル (CPF)
    - 永続的な %SYS
    - グローバル バッファ、ルーチン バッファ、Syslogのエラーログエントリ数、gmheap、locksiz（ロックテーブルサイズ）の自動構成
    - SQL用設定の自動構成
    - ネームスペースとデータベースの自動構成
    - ミラーリングされたデータベースとアービターの自動構成 
    - シャードアーキテクチャの自動構成

---
## 4. <img src="./assets/icons/Container4.png" width="70%"/>

Kubernetes は、コンテナのデプロイ、スケーリング、および管理を自動化するためのオーケストレーション・エンジンです。

InterSystems Kubernetes Operator が InterSystems 固有の機能をどのように追加しているのかを確認し、クラスタをデプロイする演習に挑戦してください。


- <a href="https://learning.intersystems.com/enrol/index.php?id=1753" target="_blank">ビデオ（英語）：Kubernetes Overview</a>
    
    複数のホストにまたがるコンテナのデプロイをオーケストレーションするためのオープンソースプラットフォームである Kubernetes についてご紹介します。
    
    InterSystems Kubernetes Operator により、InterSystems IRIS® data platform のユーザは、InterSystems IRIS アプリケーションのデプロイメントにおいて Kubernetes メリットを享受することができます。

- <a href="https://learning.intersystems.com/course/view.php?name=Deploying%20%26%20Upgrading%20IRIS%20with%20Kubernetes%20Operator" target="_blank">ビデオ（英語）：Deploying and Upgrading InterSystems IRIS with the InterSystems Kubernetes Operator</a>

    InterSystems Kubernetes Operator を使用して Kubernetes クラスターを拡張する方法、および InterSystems IRIS® data platform インスタンスをデプロイ、アップグレード、拡張する方法をご覧ください。

- <a href="https://learning.intersystems.com/enrol/index.php?id=1962" target="_blank">体験環境付き演習（英語）：Achieving High Availability with InterSystems IRIS and Kubernetes</a>

    KubernetesをInterSystems IRIS® data platform と組み合わせて使用することで、デプロイメントで高可用性を実現する事ができます。
    
    この演習では、クラスタをデプロイし、災害シナリオをシミュレートし、Kubernetes がどのようにデータ損失とダウンタイムを防止するかを学びます。

✅ ご参考ビデオ：オープンソースだけで IRIS on Kubernetes を動かそう

{% include youtube-list.html id="zMhPuBFl6l4" list="PLzSN_5VbNaxC2mfu1cYvn9pfbJRs7xtkk&index=2" %}
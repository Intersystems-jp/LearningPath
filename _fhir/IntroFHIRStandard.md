---
title: HL7 FHIRとは
date: 2024-12-01
permalink: IntroFHIRStandard.html
layout: post
---
<!-- 
> オリジナルページ：[Introduction to the FHIR Standard](https://learning.intersystems.com/course/view.php?id=2401)
-->

HL7® FHIR® を世界をリードするヘルスケアデータ標準にしている多くの特徴と機能について学びます。

このラーニング・パスでは、FHIR 標準がどのように機能し、最新のヘルスケアアプリケーションでどのように使用されるかをビデオを利用して学習します。

最後に、FHIR データモデルの実習を行った後 FHIRについてよくある質問についてもお答えします。


[1. <img src="./assets/icons/FHIR/Intro1.png" width="40%"/>](#1-)

[2. <img src="./assets/icons/FHIR/Intro2.png" width="40%"/>](#2-)

[3. <img src="./assets/icons/FHIR/Intro3.png" width="40%"/>](#3-)

[4. <img src="./assets/icons/FHIR/Intro4.png" width="40%"/>](#4-)

[5. <img src="./assets/icons/FHIR/Intro5.png" width="40%"/>](#5-)

---

## 1. <img src="./assets/icons/FHIR/Intro1.png" width="70%"/>

FHIRデータ標準を利用することで相互運用性をどのように向上させることができるか、ビデオを利用してを学習します。

- HL7 FHIR とは？

    {% include youtube.html id="AkqNuxVBQKY" %}

<details class="transcript2">
<summary> ▶日本語字幕 </summary>
<div class="content">
FHIR（Fast Healthcare Interoperability Resources）は、現在の医療データ環境の相互運用性のニーズを満たすために HL7 International によって作成された医療データ標準です。過去数十年にわたり、より多くのシステムを接続する必要があるためこの種のデータ標準は不可欠となっています。実際 FHIR 標準との互換性は、現在多くの国の医療 IT システムで連邦政府によって義務付けられています。
<br>
現在、データは薬局、家庭用機器、モバイル機器など多くの場所に保存されているため、相互運用性 そしてFHIR標準 によって、すべてのデータを 1 つの場所でリアルタイムに確認することができるようになります。
<br>
FHIR は、オフラインからオンラインへのデータ移動の必要性やデータの透明性要件など重要な考慮事項を念頭に設計されました。標準規格として FHIRはナラティブデータとコード化されたデータの両方を扱うことができます。
<br>
簡単に言えば、FHIR は表現的な状態、つまり REST、API です。FHIR は、データの要求と受信のための仕様と医療におけるデータの意味に関する合意を包含しています。
<br>
FHIR を構成する要素を見てみましょう。まず、FHIR リソースは、患者、薬、文書などの論理的に分離されたデータ概念であり、定義された意味とサーバー上の既知の場所を持ちます。FHIR リソースは、データ概念を定義するために必要なすべてのデータ要素を含んでいます。例えば、患者リソースは、姓、名、生年月日などの要素を含んでいます。
<br>
FHIR 仕様には Profile も含まれておりこれは手技のような特定のユースケースのために定義された臨床情報モデルの実装です。FHIR プロファイルは、ユースケースに必要なリソースごとに存在し、必要なすべてのルールと関係、値セット、FHIR Extensions で構成されています。FHIR Extensions については後で詳しく説明します。
<br>
共有プロファイルを使用することで医療アプリケーションは変換を必要とすることなく、異なる相互運用性パラダイム間で FHIR を使用することができます。FHIR として表現されたデータは、メッセージ、ドキュメント、REST API で使用することができます。FHIR は機械可読であるため意思決定支援サービスなどのサービスでも使用できます。相互運用性は、各システムで同じ FHIR プロファイルを使用することで得られます。
<br>
真の相互運用性は、情報を交換し意図した意味が伝わることで得られます。人間は意味を解釈することに長けていますが、コンピュータはデータの内容を正確に理解することしかできません。
<br>
例えば、2 人の人間がシマウマを黒い縞模様の白馬と表現したり、白い縞模様の黒馬と表現したりすれば同じ動物を指していることがすぐにわかります。
<br>
ヘルスケアのシステム間で同じ記述が使われるようにするためには、臨床情報モデルを使わなければなりません。これには、特定のユースケースのための医療データ概念の記述、データの使用方法のルール、語彙や用語のバインディング、データ間の関係などが含まれます。FHIR プロファイルは臨床情報モデルの実装です。
<br>
プロファイルの重要性を理解するために、EHR システムからの患者の病歴報告書を印刷し個々のデータ要素に切り分けることを考えてみましょう。情報の1つに 「Diabetes Type 2 」と書かれているものがあるとします。
<br>
このフレーズが何であるかはわかりますが、文脈までは分かりません。糖尿病は、患者が持っている病態かもしれないし、以前持っていた病態かもしれないし、家族歴からすると母親が持っていた病態かもしれません。FHIR プロファイルは、データ要素とリソースとの関係を定義することによってコンテキストを提供します。これらのプロファイルにおける用語バインディングは、FHIR プロファイルに必要なすべてのコードと値セットを含む FHIR 用語サーバを使用できます。特定の要素に使用されるコードは値セットを構成されます。プロファイルを使用するすべてのアプリケーション、システム、および操作はサーバーにアクセスすることができ、システム間のリソース内で同じデータ要素を参照するために同じコードが使用されることが保証されます。
<br>
FHIR 標準には 80% のシステムで使用されているデータ要素が含まれていますが、標準にはまだ含まれていない特定のユースケースのデータ要素を表すために、プロファイルの一部としてFHIR Extension を作成する方法も定義されています。
<br>
例えば、医療ツーリズムを行うクリニックは、標準の患者リソースにはない患者の国籍を記録したいと思うかもしれません。そのような場合、Patient リソースを拡張して Nationality Extension を追加すればよい事になります。
<br>
FHIR Extension が作成されると、それらは一般に利用可能な URL として公開できます。
<br>
このガイドには、特定のユースケースに必要な Extension、用語バインディング、値セットを含む、プロファイル化されたリソースが含まれています。
<br>
これらの技術的な詳細だけでなく FHIR 実装ガイドには、どのように使用されるかの文書と例が記載されています。
これらのガイドは、FHIR 仕様の一部として HL7 International が提供する Web 公開ツールを使用して、一般に利用可能な URL に公開されます。これらのガイドは機械可読であるため、FHIR 実装ガイドを使用して開発された FHIR アプリケーションを検証することができます。
<br>
FHIR 規格の詳細については、InterSystems のラーニングサイトの他コンテンツもご参照ください。
</div>
</details>
<br>

- 日本語字幕付きビデオ「FHIR - 未来のために設計された医療データスタンダード "FHIR A Healthcare Data Standard Designed for the Future"

    {% include youtube.html id="gNjlaARboYk" %} 

---

## 2. <img src="./assets/icons/FHIR/Intro2.png" width="70%"/>

HL7® FHIR® ヘルスケアデータ標準の概要とウェブサイトのナビゲート方法を学習します。

また、FHIR の目標、データの保存と共有方法の基本、仕様内のさまざまな FHIR リソース間の関係について学習します。

- FHIR とは何か、現在、そして今後

    このビデオは、国際モダンホスピタルショウ2022 インタ―システムズブースのミニシアターで開催された　一般社団法人 日本IHE協会　理事　接続検証委員長　塩川 康成 様　によるご講演ビデオです。

   >国際モダンホスピタルショウ　インタ―システムズブースのミニシアターでのご講演内容全般については、<a href="https://www.youtube.com/@InterSystemsJapan/playlists" target="_blank">InterSystems Japan YouTubeチャンネル</a> にて公開しております。

    {% include youtube-list.html id="_Qgv9WqrN6k" list="PLgFt3CvX3OePAiRdrL8GmMzKNiCG_BJqP" %}

<br>

> **以下のビデオもあります**
>- <a href="https://www.youtube.com/watch?v=OAS2mp-6TXY&list=PLp4xNHWZ7IQkqH6bHsYVFkh1tX0P1_2VF&index=3" target="_blank">ビデオ（英語）：What Is the HL7 FHIR Specification?</a>
>
>- <a href="https://www.youtube.com/watch?v=-dcaWj1gZSo&list=PLp4xNHWZ7IQkqH6bHsYVFkh1tX0P1_2VF&index=4" target="_blank">ビデオ（英語）：Organizing HL7 FHIR Resources</a>
{: .block-tip}

---
## 3. <img src="./assets/icons/FHIR/Intro3.png" width="70%"/>
個々の FHIR リソースの構造、データ表現の一貫性を可能にするデータ型と用語バインディングについて、FHIR 標準仕様のウェブサイトを使用しながら確認します。

- ビデオ（英語）：Understanding the Structure of HL7 FHIR Resources

    HL7® FHIR® リソースの構造を紹介します。
    
    <a href="https://hl7.org/fhir/R4/" target="_blank">FHIR ウェブサイト</a> のリソースのツリー表示の見方と読み方を確認し、リソースに含まれる様々なデータ要素を理解します。
    
    また、リソースを XML、JSON、または Turtle で表示する方法や、FHIR リソースの UML (Universal Modeling Language) ダイアグラムの場所についても説明します。

    {% include youtube-list.html id="BmgAhxWQtZw" list="PLp4xNHWZ7IQkqH6bHsYVFkh1tX0P1_2VF" %}
<br>

- ビデオ（英語）：Identifying Structured and Coded Data in HL7 FHIR Resources

    HL7® FHIR® で使用され、データセットの表現に一貫性を持たせる、構造化データとコード化データの識別方法を学習できます。
    
    FHIR で使用されるデータ型と、用語バインディングが要素定義をデータ型と値セットにどのように結びつけるかを確認できます。
    
    また、FHIRリソースの一部として定義されたコードや LOINC や SNOMED のような外部の用語体系から引き出されたコードの例をご覧ください。

    {% include youtube-list.html id="D8QafQ6-yZw" list="PLp4xNHWZ7IQkqH6bHsYVFkh1tX0P1_2VF" %}
<br>

---
## 4. <img src="./assets/icons/FHIR/Intro4.png" width="70%"/>

FHIRプロファイルと実装ガイド、FHIR shorthand を詳しく確認し、FHIR データアーキテクチャを理解します。

-  FHIR プロファイルについて

    {% include youtube-list.html id="B-B6ge_0nHg" list="PLzSN_5VbNaxBu4kMgZrK5iGi-GIGNxvpu&index=8" %}

<br>

> **以下のビデオもあります**
>- <a href="https://youtu.be/YHVlghfGsq4?list=PLp4xNHWZ7IQkqH6bHsYVFkh1tX0P1_2VF" target="_blank">ビデオ（英語）:Understanding HL7 FHIR Profiles</a>
{: .block-tip}

- FHIR 実装ガイドについて（英語ビデオ）

    {% include youtube-list.html id="AfoXYVgzE9U" list="PLp4xNHWZ7IQkqH6bHsYVFkh1tX0P1_2VF" %}

- FHIR Shorthandについて

    HL7® FHIR® Shorthand を使用して FHIR 実装ガイドをより効率的に作成する方法を学習します。 
    
    FHIR Shorthand は、プロファイル、エクステンション、およびその他の FHIR アーティファクトを定義するための、ドメイン固有の人間が読める言語です。

    - 記事：<a href="https://jp.community.intersystems.com/node/493351" target="_blank">SUSHIを使ってFHIRプロファイルを作成しようパート1</a>

    - 記事：<a href="https://jp.community.intersystems.com/node/506271" target="_blank">SUSHIを使ってFHIRプロファイルを作成しようパート2</a>


> **以下のビデオもあります**
>- <a href="https://www.youtube.com/watch?v=_vakrZk482k&list=PLp4xNHWZ7IQkqH6bHsYVFkh1tX0P1_2VF&index=9" target="_blank">ビデオ（英語）：Using HL7 FHIR Shorthand</a>
{: .block-tip}
<br>

- <a href="https://learning.intersystems.com/course/view.php?id=2525" target="_blank">演習環境付き演習（英語）のオンラインコース：Building a FHIR Data Architecture</a>

    HL7® FHIR® アーキテクチャとその基礎となるデータモデルの基礎を学びます。
    
    この演習では、InterSystems がサポートする Graph Builder 2 (GB2) アプリを使用して、FHIR を使用した開発の基礎となる FHIR データアーキテクチャの構築を開始します。

---

## 5. <img src="./assets/icons/FHIR/Intro5.png" width="70%"/>
医療システム間のセマンティック相互運用性について学び、FHIR分野で最もよくある質問を確認します。

- （ビデオ：英語）<a href="https://learning.intersystems.com/course/view.php?id=2203" target="_blank">Achieving True Interoperability in Healthcare Systems</a> 
    
    セマンティック相互運用性の概念と、医療データ交換におけるその役割についてご紹介します。
    
    セマンティック相互運用性は、医療データが確実に伝送されるだけでなく、容易に理解されることを保証するために、システムマッピングを超えるものです。HL7® FHIR® データ標準がこの課題にどのように対応できるかを紹介します。

    {% include youtube-list.html id="us6W4ppN9SA" list="PLp4xNHWZ7IQkqH6bHsYVFkh1tX0P1_2VF&index=11" %} 
<details class="transcript2">
<summary> ▶日本語字幕 </summary>
<div class="content">
医療システム間の相互運用性を実現することは、常に進化し続ける課題です。
<br>
ある医療施設には何十ものデジタル・システムがありまた、医療ネットワーク内の多数の施設では、システムの通信を可能にすることは重要な課題です。
<br>
InterSystems の複数のテクノロジーを含むソフトウェア製品は、相互運用性を改善しこれらの接続を容易にするために構築されてきました。
<br>
システムと施設を接続するという課題をより詳しく見ていく中で、構文的相互運用性と意味的相互運用性という 2 つのタイプの相互運用性を区別することにします。
<br>
構文的相互運用性--メッセージの構造は定義されているが、その意味は定義されていない-- は、システムが異なるフォーマットでデータを送受信することを可能します。
<br>
これがなければ、システムは効果的に通信することができせん。例えば、システム A は患者情報を HL7 V2 メッセージとして送受信し、システム B の患者向けアプリケーションは JSON フォーマットで表現されたデータを持つ FHIR リポジトリを使用しています。現状では、システム A は FHIR リポジトリにデータを提供できないため、システム B のアプリケーションはそのシステムの患者データを利用できません。
<br>
この問題に対する試行錯誤の末の解決策は、あるフォーマットから別のフォーマットへ、例えば HL7 V2 フォーマットから FHIR フォーマットへデータ変換によってデータを変換する仲介システムを持つことです。
<br>
このようなマッピングを作成することで、構文的相互運用性が達成されます。つまり、2 つのシステムはデータを交換する標準化された方法を持つことになります。
<br>
HL7 V2 と FHIR 標準は、医療 IT インフラにとって重要な構文的相互運用性への道を開きました。HL7 V2 は、世界で最も使用されている相互運用性標準であり、InterSystems の技術は、毎日 10 億以上の HL7 V2 メッセージの交換に使用されています。そして、FHIR に焦点を当てた未来に入るにあたり、FHIR 標準との互換性が現在多くの国の医療 IT システムに連邦政府から義務付けられていることを考慮してください。
<br>
しかし、構文的相互運用性は決定的に重要ですがそれだけでは十分ではありません。医療の相互運用性は常に人間の意思決定に依存します。例えば、異なるデータ形式を使用して通信する 2 つの医療システムのマッピングをどのように設定するかは、エンジニアが決めるかもしれません。その結果、マッピングされたシステムの連鎖に矛盾が生じる可能性があります。
<br>
意味的（セマンティック）相互運用性を達成することで、このような不一致をある程度回避することができます。真の意味的相互運用性があれば、システムからのデータは同じ意味を持ち、受信システムのワークフローで使用することができます。データ要素は一貫して定義されており、人間による解釈は必要ありません。
<br>
あるシステムが別のシステムに対してシマウマを説明することを想像してください。システム A では、シマウマは黒い縞模様の白馬と表現されています。一方、システム B はシマウマを白い縞の黒い馬と定義しています。
<br>
これらのシステムが互いに明確にコミュニケーションでき、その情報を理解可能な言語で伝達できるのは素晴らしいです。しかし、それぞれのシステムが同じものを描写していることをどうやって知るのでしょうか。
<br>
ニュアンスの異なる言語を解釈する能力は、人間と機械を分ける特徴のひとつです。人間はこのようなデータの曖昧さをなくすことに長けており、ほとんどの人間は、説明されている 2 つの動物が実際には同じものであることを識別できます。ヘルスケアの世界では、システムが記述しなければならないシマウマは何百万頭も存在し、意味的相互運用性には、どの記述を使用するかの合意が必要です。
<br>
この概念が、3 つの別々の電子カルテシステムの実例にどのように適用されるかを考えてみましょう。それぞれの臨床医が、肺癌の疑いという同じ問題を文書化しています。
<br>
あるシステムはこのデータを　3　つの異なる要素としてモデル化します。：癌という健康上の懸念、肺という身体部位、そして疑いという状態です。
<br>
別のシステムでは、がんの疑いという健康上の懸念があり、体の部位である肺は文書化されています。
<br>
さらに別のシステムでは、臨床医が健康上の懸念として選択するための独立した項目として、肺がんの疑いがあるかもしれない。
<br>
結局、この例では 3 つのシステムにまたがるデータ保管は、1 番と 2 番のシステムで肺という身体部位という 1 つの要素しか共通していないことになる。それ以上、これらのシステムには、このデータの入力方法から、入力項目がすべて同じ意味であると判断する方法はありません。
<br>
共通の意味を確立することは、意味的相互運用性の核心です。医療 IT システムの規模が拡大するにつれ、IT 開発者がデータスキーマを効率的に設定することと、臨床医が正確にデータを入力することの間でバランスを取ることが難しくなっています。
<br>
意味的相互運用性を達成することは、技術だけでなくあるレベルの人間的な合意も必要です。当分の間は進行中の作業となるでしょう。
<br>
FHIR 標準の最も価値ある側面のひとつは、FHIR プロファイルを含めすべてが機械可読であることです。これにより、組織間でデータコンセプトの FHIR 実装を共有することが可能になります。

そして、医療ネットワークがそれぞれのシステムで使用する FHIR プロファイルに合意できれば、意味的相互運用性の実現に一歩近づくことになるでしょう。
</div>
</details>
<br>

- （ビデオ：英語）FHIR FAQs

    InterSystems のSenior Clinical Interoperability Advisor である Russ Leftwich が HL7® FHIR® に関してよくある質問に回答します。

    {% include youtube-list.html id="tH2sWhVa8MU" list="PLp4xNHWZ7IQkqH6bHsYVFkh1tX0P1_2VF&index=10" %} 


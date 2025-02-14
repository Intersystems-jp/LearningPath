---
title: InterSystems ObjectScript 入門
date: 2024-12-06
permalink: ObjectScript.html
layout: post
---
<!-- 
>オリジナル：[Getting Started with InterSystems ObjectScript](https://learning.intersystems.com/course/view.php?id=289)
-->

InterSystems ObjectScript の基本的な構文と主要な要素について学習します。

[1. <img src="./assets/icons/O1.png" width="40%"/>](#1-)

[2. <img src="./assets/icons/O2.png" width="40%"/>](#2-)

[3. <img src="./assets/icons/O3.png" width="40%"/>](#3-)

[4. <img src="./assets/icons/O4.png" width="40%"/>](#4-)

---
## 1. <img src="./assets/icons/O1.png" width="70%"/>

ObjectScript 概要、変数、式、コマンドなど主な機能のいくつかを学習します。

- <a href="https://docs.intersystems.com/irislatestj/csp/docbook/DocBook.UI.Page.cls?KEY=GCOS_intro" target="_blank">ドキュメント：ObjectScriptの概要</a>

- <a href="https://github.com/Intersystems-jp/ObjectScriptCookBook/blob/master/Basic.md" target="_blank">ObjectScriptクックブック：ObjectScriptの基本のき！</a>

    実際のコマンド操作を試す場合には IRIS のインストール環境、または、オンラインコース（英語）の利用が必要です。
    
    IRISのインストール方法については、以下ビデオをご参照ください。
    
    {% include youtube-list.html id="nKDvM68Gs04" list="PLzSN_5VbNaxBPaSSINLzv-CkDJy00bOSQ" %}

<br>
> **英語ビデオやオンラインコースもあります**
>
>- <a href="https://learning.intersystems.com/course/view.php?name=Cach%C3%A9%20ObjectScript%20Basics" target="_blank">オンラインコース：InterSystems ObjectScript Basics（英語）</a>
>
>    オンラインコースを通して以下の内容を学習できます。
>    - InterSystems ObjectScript における変数の型付け方法
>    - 変数の型に関する詳細情報をドキュメントから検索する方法
>    - 変数の設定、変数の内容の確認、および変数のメモリからの削除を行うための set、write、kill の使用方法
>    - 算術演算と組み込み関数を使用して変数を操作する
>    - 論理演算子を使用して変数を比較する
>    - if/else 文を評価する。
>    - do を使ってメソッドを実行する
>    - ループを使用する
{: .block-tip}


---
## 2. <img src="./assets/icons/O2.png" width="70%"/>

演算子と式の記述方法を確認します。また、ObjectScript が提供する関数の利用方法も学習します。

最後に、コマンドの後置条件式の記述方法を確認します。

- <a href="https://docs.intersystems.com/irislatestj/csp/docbook/DocBook.UI.Page.cls?KEY=GCOS_operators" target="_blank">ドキュメント：演算子と式</a>

- <a href="https://github.com/Intersystems-jp/ObjectScriptCookBook/blob/master/CookBook.md#%E6%BC%94%E7%AE%97%E5%AD%90" target="_blank">ObjectScriptクックブック：演算子</a>

- 関数操作：<a href="https://github.com/Intersystems-jp/ObjectScriptCookBook/blob/master/CookBook.md#%E6%96%87%E5%AD%97%E5%88%97%E6%93%8D%E4%BD%9C" target="_blank">ObjectScriptクックブック：文字列操作</a>

    文字列の操作に便利な関数の説明が含まれています。

> **関数について、英語ビデオもあります**
>
>- ビデオ（英語）：Using System Functions in ObjectScript
{: .block-tip}
{% include youtube-list.html id="Mx3WNXMPxpiE" list="PLp4xNHWZ7IQmiSsryS0T3qjuVXlbSWqc8&index=4" %}

<details class="transcript2">
<summary> ▶日本語字幕 </summary>
<div class="content">
InterSystems ObjectScript には、コマンドラインで呼び出すことができる組み込みのシステム関数が多数用意されておりデータを簡単に扱うことができます。ObjectScript のシステム関数 ($Length() など) は、$ から始まります。
<br>
関数は、受け取った引数に対してさまざまな処理を実行します。操作には、文字列の操作、リストまたはビット文字列の作成、クラスメソッドの実行、値の検証などがあります。
<br>
関数名の後に括弧で引数を指定します。そして関数は操作の結果である値を返します。
<br>
ほとんどの場合、関数の戻り値はコマンドや別の関数に渡すことができます。よくある例は、関数の戻り値を write コマンドの引数として与えることです。
<br>
これを実際に確認するため $Length() 関数の動作を見てみましょう。この関数の必須引数は 1 つで調査対象の文字列を指定します。引数は、使用する関数によって異なります。
<br>
試しに括弧内に "How long is this string?" という引数を指定して $Length() 関数を実行し、この関数が返す値を write コマンドに参照します。write $Length("How long is this string?") を実行すると文字列の長さが 24 文字であることがわかります。
<br>
また、関数は 1 つ以上の引数を取ることができるということも重要です。この例では、文字列 「How long is this string?」 が $Length() 関数で必須の引数です。他の関数では複数の引数が必要になる場合もあり、指定時カンマで区切ります。
<br>
例えば $Piece() 関数は、区切り文字の有無で部分文字列を識別します。文字列の最初の単語を取得したい場合、この関数には 3 つの引数が必要です。write $Piece() というコマンドを実行し、3 つの引数を与えてみます。第 1 引数：文字列、第 2 引数：区切りマーク（例はスペース）、第 3 引数は、部分文字列の位置で 1 を指定します。
<br>
部分文字列が返されると、それが write コマンドに渡され最初の単語 "How" が抽出されていることを確認できます。
<br>
関数の戻り値を別の関数で使うこともできます。例えば、今取り出した単語の長さを調べたいとします。
<br>
この結果を得るには、先ほど実行した $Piece() 関数の戻り値を $Length() の引数として与えその結果を write します。
<br>
これは、文字列の最初の単語の長さが 3 文字であることを示します。
<br>
$Piece() 関数は部分文字列の置換にも使えます。先ほど実行した関数は指定した文字列の値を変更しない方法でしたが、set コマンドで実行すると指定した値を変更できる関数もあります。
<br>
まず次の変数をセットしてみましょう。 変数 sentence = "How long is this string?"
<br>
次に、次のコマンドを実行します。 set $Piece(ここに引数)="Video"
<br>
$Piece() の 3 つの引数は、文字列 sentence、区切り文字、置換したい部分文字列の位置を指定します。確認のため変数: sentence を write します。結果は、文の 5 番目の部分文字列 "string" を引数に指定した文字列 "video?" に置き換わったことがわかります。
<br>
システム関数には、$Piece() のように 2 種類の使い方ができるものがたくさんあります。使い方によって関数が引数の値を変更するかどうかが決まります。
<br>
これまで、文字列関数の例を見てきました。ObjectScript の他の種類の関数を使用するとより複雑な変数の構築などのアクションを実行できます。
<br>
たとえば、$ListBuild() 関数は、指定された項目で構成されるリスト変数を作成するために使用します。注文の詳細を保持するためにいくつかの変数を設定してみましょう。<br>
OrderDate="June 15 2020"、Amount=25、Status="In Process" とします。これらの変数を設定したので、$ListBuild() 関数を利用して引数に 3 つ情報すべてを含むリスト変数を作成することができます。
<br>
設定するためには、set コマンドを使用し $ListBuild() 関数の戻り値に等しい変数を設定します。リスト変数を作成するには
<br>
 set Order = $ListBuild(OrderDate, Amount, Status) を実行します。
<br>
次に、Order にリストが正常に構築されたことを確認します。リスト変数を出力するためには、zwrite コマンドを使用します。
<br>
リストには、設定した 3 つの項目、OrderDate、Amount、Status が含まれていることがわかります。リスト変数の項目を更新するには、$List() 関数を使います。Status を  "Complete" に変更して、もう一度 zwrite Order を実行してみましょう。
<br>
ここまでの流れで ObjectScript の関数を利用方法がご理解いただけたかと思います。
</div>
</details>


関数について詳細はドキュメントもご参照ください：<a href="https://docs.intersystems.com/irisforhealthlatestj/csp/docbook/DocBook.UI.Page.cls?KEY=RCOS_FUNCTIONS" target="_blank">ObjectScript関数</a>
<br>

> **関数について、英語ビデオもあります**
>- ビデオ（英語）：Controlling Command Flow with Postconditional Expressions
>   
>   If 文を使用せずに単一のコマンドに条件を追加する方法（後置条件）を説明しています。
>   
>   InterSystems ObjectScript では、ほとんどの単一行コマンドの後ろに後置条件を追加することで、コマンド・フローを制御できます。後置条件は、コマンドが実行されるべきかどうかを決定します。
{: .block-tip}
{% include youtube-list.html id="4RgA213AhF8" list="PLp4xNHWZ7IQmiSsryS0T3qjuVXlbSWqc8" %}

<details class="transcript2">
<summary> ▶日本語字幕 </summary>
<div class="content">
InterSystems ObjectScript プログラマとして、コマンド・フローを制御するためのいくつかのオプションがあります。一般的には if 文を使用しますが、特に 1 行のコードを記述する場合など、条件が真であるときに 1 つのコマンドを実行するための迅速な方法が必要な場合があります。
<br>
if 文を書く代わりに実行すべきかどうかを示す後置条件式をコマンドに追加することができます。
<br>
これは do や execute コマンドの引数にも有効です。
<br>
このビデオの例はすべてコマンドに言及していますが、同じ構文はコマンド引数にも当てはまります。構文は簡単です。コマンド・キーワード（この例では write）を入力しその後にコロンを続けます。コロンでコマンドと後置条件を区切り、コロンの両側にはスペースを入れません。
<br>
コロンの直後には、コマンドが実行されるかどうかを決定する後置条件を置きます。構文エラーを避けるために条件を括弧で囲むのがベストプラクティスです。
<br>
括弧で囲まれていない限り空白は許可されません。条件に続くのは引数で、条件が真の場合に実行されます。式が真になるとはどういうことかを少し確認してみましょう。
<br>
このコードでは、変数 a が変数 n 以下であるという条件が真であれば、write コマンドで "I love bananas" という文を出力します。
<br>
条件が複雑であったりスペースが必要な場合は、括弧で囲みます。たとえば、2 つの条件をそれぞれ括弧で囲み、and 演算子（2つの&）で結合します。条件全体を括弧で囲むことで、両方の条件を考慮する必要があることを示します。
<br>
InterSystems Terminal の簡単な例を確認してみましょう。変数 a は現在 3、で変数 b は 0 です。
<br>
a の値が 5 より大きい場合に b の値を変更したいとします。これを行うには、set コマンドにコロンをセパレーターとして使用した後置条件を追加します。a が 5 より大きければ、b は 10 になる。
<br>
コマンドを入力すると、b の値はゼロになる。なぜなら、a は 3 に設定されているからです。
<br>
では、条件を満たすように変数 a を 6 に設定してみましょう。再び set コマンドを実行すると変数 b の値は 10 に設定されます。
<br>
ObjectScript の条件は、結果が有効なゼロ以外の数値であれば真になります。
<br>
この動作を確認するために、3 つの変数を設定してみましょう。数値変数 a に 12 を設定し、次に b に値 12 の文字列を設定します。また、文字列変数 c に値 "40 musicians" を設定します。
<br>
write コマンドを入力し後置条件に変数 a を指定すると "True" が返されます。
<br>
変数 b と c についても同様です。
<br>
c は musicians という単語を含んでいるにもかかわらず、40 というゼロでない数字で始まっています。そのため ObjectScript はこれを真と評価します。
<br>
a に 0、bに値 0 の文字列、c に "The 40 musicians" を設定したらどうなるでしょうか。同じコマンドを入力すると
<br>
a と b は 0 なので、条件はすべて偽で、c は文字列で始まるので　ObjectScript では値 0 として認識します。
<br>
後置条件式は、変数が数値であれ文字列であれ条件が 0 でない場合にのみコマンドを実行します。
<br>
後置条件式は、2 つのタイプを除いてあらゆる ObjectScript コマンドで使用できます。
<br>
まず、IF、ELSEIF、ELSE、FOR、WHILE、DO WHILE などのフロー制御コマンドでは使用できません。というのも、後置条件もコマンド・フローを制御するのでコード内で両方を使うと冗長になるからです。
<br>
これらを一緒に使おうとすると、システムは構文エラーを表示します。
<br>
次に、TRY や CATCH のようなエラー処理コマンドと一緒に後置条件を使うことはできません。
<br>
同じ条件で複数のコマンド行を作成する必要がある場合は、他の開発者がコードを読みやすくするために if 文を使用するのが最善です。各コマンドの後に同じ後置条件を書く代わりに、if 文の後に中括弧でコマンドのリストを書きます。
<br>
1 つのコマンドラインに条件を書く場合、後置条件式は使いやすいオプションです。
<br>
後置条件とコマンドの詳細については、ドキュメントをご覧ください。
</div>
</details>

ドキュメント：<a href="https://docs.intersystems.com/irisforhealthlatestj/csp/docbook/Doc.View.cls?KEY=TOS_FlowControl" target="_blank">実行フローの制御</a>

<br>


---
## 3. <img src="./assets/icons/O3.png" width="70%"/>

ObjectScript の変数の特徴を理解します。また ObjectScript が提供する特殊変数とその使用方法についても学習します。

- 変数について

    ✅ <a href="https://github.com/Intersystems-jp/ObjectScriptCookBook/blob/master/Basic.md#3-%E5%A4%89%E6%95%B0%E3%81%AB%E3%81%A4%E3%81%84%E3%81%A6" target="_blank">ObjectScriptの基本のき！：変数</a>

    ✅ <a href="https://github.com/Intersystems-jp/ObjectScriptCookBook/blob/master/CookBook.md#%E6%B3%A8%E6%84%8F%E7%82%B9" target="_blank">注意点</a>

    ✅ <a href="https://docs.intersystems.com/irislatestj/csp/docbook/DocBook.UI.Page.cls?KEY=GCOS_mdarrays" target="_blank">ドキュメント：多次元配列</a>

    ✅ 特殊変数：<a href="https://github.com/Intersystems-jp/ObjectScriptCookBook/blob/master/CookBook.md#%E7%8F%BE%E5%9C%A8%E6%97%A5%E4%BB%98%E3%81%A8%E6%99%82%E5%88%BB%E3%81%AE%E5%8F%96%E5%BE%97" target="_blank">現在日付と時刻の取得</a>


- <a href="https://github.com/Intersystems-jp/ObjectScriptCookBook/blob/master/CookBook.md#%E3%83%AA%E3%82%B9%E3%83%88" target="_blank">リスト操作方法</a>

- インスタンス操作方法

    IRISに作成したクラス定義のインスタンス操作について説明しているビデオをご覧ください（例では永続のタイプのクラスを定義し、インスタンスを生成しプロパティに値を代入した後、データベースに値を保存する流れを確認できます）。

    > 27:40からインスタンス生成の説明が登場します。

    {% include youtube-list.html id="kWJCzn9bndQ" list="PLzSN_5VbNaxBPaSSINLzv-CkDJy00bOSQ" %}
<br>

> **英語ビデオもあります**
>
>- ビデオ（英語）：Exploring Data Types in ObjectScrip
{: .block-tip}
{% include youtube-list.html id="MSWccht-eGI" list="PLp4xNHWZ7IQmiSsryS0T3qjuVXlbSWqc8&index=2" %}

<details class="transcript2">
<summary> ▶日本語字幕 </summary>
<div class="content">
InterSystems ObjectScript では、変数は動的に弱い型に分類されます。これは、データ型を宣言する必要がないことを意味し、変数の使用法がその変数の評価方法を決定します。変数には、"Hello" のような文字列、("apple","banana","orange") のようなリスト、または Sample.Person クラスのインスタンスのようなオブジェクトなどいくつかのデータ型のいずれかを値として持つことができます。このビデオでは、これら 3 つの最も一般的なデータ型について説明します。
<br>
文字列は、ObjectScript の変数のデフォルトのデータ型です。文字列は二重引用符で囲んで記述します。
<br>
デフォルトでは、変数は文字列として評価されます。ただし、文字列を数式で使用する場合は、自動的に数値として評価されます。文字列が条件式やブール式で使われる場合も同様です。
<br>
いくつかの例を見てみましょう： まず、変数 x に 123 を設定しこの変数を数式で使用します。 set y = x-3  この結果は 120 が返ります。
<br>
次に、x を数字と文字を含む文字列 "123abc" に設定し同じ作業を繰り返してみましょう。
<br>
120が戻っています。文字列 "123abc" が数字 123 として評価されたことがわかります。
<br>
ここで、文字列は左から右に読まれることに注目します。x を文字列 "abc123" に変えて数式を繰り返すと、-3 が戻ります。これは文字列が数値として評価されるとき評価は最初に遭遇した非数値文字で止まるためです。"abc123" は、0 評価されます。同様に文字列 "12abc3" は 12 と評価されます。
<br>
数値は、引用符のような句読点を必要としません。
<br>
これらの数値が評価されるとき、正規形に変換されます。これにより、先頭の符号や末尾のゼロが自動的に解決される。
<br>
数値がどのように評価されるかを理解することは有益です。なぜなら、米国の郵便番号のように先頭の文字が重要な場合があるからである。先頭のゼロを維持するには郵便番号 02145 を二重引用符で囲んで文字列として格納する必要があります。
<br>
ObjectScript ではリストを作成することもできます。その名のとおりリストには要素のリストが格納され、各要素は文字列、数値、リスト、その他のデータ型になります。リストには、組み込み関数を使用して要素を取得、追加、操作できるエンコーディングが含まれています。
<br>
リストは ObjectScript の組み込み関数 $LISTBUILD() を使って作成します。
<br>
$LISTBUILD() 関数を使用して、名前のリストを格納する変数 friends を設定してみましょう。Peter, Harry, Mary Jane という名前を追加します。リストのすべての要素を表示するには、zwrite コマンドを使います。その後、$LIST() 関数を使用して要素を取得したり必要に応じて更新したりできます。
<br>
もう 1 つのデータ型はオブジェクトです。オブジェクト指向プログラミングに慣れている人なら、このデータ型を見たことがあるかもしれません。オブジェクトはクラスのインスタンスです。どのオブジェクトでも、オブジェクト参照をローカル変数に代入することで、そのオブジェクトのメソッドやプロパティにアクセスできるようになります。
<br>
この例では、Sample.Person クラスのオブジェクトを作成し、オブジェクト参照を変数に代入してオブジェクトのプロパティを設定できるようにします。Sample.Person クラスには、すでに Name、Address、Salary などのプロパティが定義されています。
<br>
変数 Human にオブジェクト参照を代入するには、##class(Sample.Person).%New() を設定します。
<br>
オブジェクトのプロパティやメソッドには、ドット構文を使用してオブジェクト参照でアクセスできます。
<br>
例えば、次のコマンドを実行して Name プロパティを設定します： set Human.Name = "Maria"
<br>
他のプロパティも同じように設定してみましょう。変数のすべてのプロパティを表示するには、zwrite コマンドを使用します。
<br>
このコマンドの出力は、Human が Sample.Person クラスのインスタンスへの OREF（Object Reference）であることを示しています。参照カウントやクラス名など、オブジェクトに関する一般的な情報が一覧表示されます。また、属性値ではプロパティとその値を確認できます。
<br>
これまで見てきたように、文字列、リスト、オブジェクトは、データ型を宣言しなくても変数に柔軟に代入することができます。ObjectSriptのデータ型について詳しくは、ドキュメントのウェブサイトをご覧ください。
</div>
</details>

以下ドキュメントもご参照ください。
- <a href="https://docs.intersystems.com/irislatestj/csp/docbook/DocBook.UI.Page.cls?KEY=GCOS_types" target="_blank">データ型とデータ値</a>
- <a href="https://docs.intersystems.com/irislatestj/csp/docbook/DocBook.UI.Page.cls?KEY=GCOS_operators#GCOS_operators_str2num_numstrings" target="_blank">数値文字列</a>

>
>- ビデオ（英語）：Using Variables in ObjectScript
{: .block-tip}
{% include youtube-list.html id="FCYi0Y0xeTw" list="PLp4xNHWZ7IQmiSsryS0T3qjuVXlbSWqc8" %}

<details class="transcript2">
<summary> ▶日本語字幕 </summary>
<div class="content">
プログラミングにおいて変数とは値を格納する場所の名前です。変数は、さまざまなコマンドや関数で使用できます。InterSystems ObjectScript は動的で弱い型の言語であるため変数にはデータ型が関連付けられていません。
<br>
変数を定義するには、set コマンドを使用して値を代入します。たとえば、変数 s に 4 という値を代入するには、set s = 4 というコマンドを使用します。
<br>
ほとんどのコマンドや関数では、write コマンドのように変数を使用する前に定義しておく必要があります。
<br>
他のプログラミング言語と同様に、ObjectScript の変数は動的に型付けされます。そのため変数に数値を代入し後で同じ変数に文字列値を代入することができます。InterSystems IRIS data platform は、変数が使用されるコンテキストに基づいて変数の値を自動的に変換または解釈します。
<br>
ObjectScript ではいくつかの種類の変数がサポートされていますが、このビデオで取り上げるのは、ローカル変数、グローバル変数、特殊変数の 3 つです。
<br>
ローカル変数は、現在の InterSystems IRIS プロセス内に格納され、その変数を作成したプロセスのみがアクセスできます。プロセスが終了するとプロセスのローカル変数はすべて削除されます。
<br>
ローカル変数を定義するには、以下の命名規則に従ってください。名前には有効な識別子を使用し最初の文字を文字またはパーセント文字にします。例えば、変数名に petName と %petName は有効ですが、*petName は有効ではありません。
<br>
ローカル変数名には、set や write などの ObjectScript コマンド名や INDEX や EXECUTE などの SQL 予約語を使用しないことをお勧めします。
<br>
グローバル変数は、InterSystems IRIS データベース内に自動的に格納される特殊な変数です。グローバル変数は、それを作成したプロセスの終了または終了後も明示的に削除されるまで永続します。
<br>
グローバル変数は、ローカル変数を定義するのと同じ方法で定義できますが、変数名は常に ^ 接頭辞で始まりその後に文字または % 文字が続きます。ローカル変数と同様に、グローバル変数では大文字と小文字が区別されます。
<br>
次に特殊変数についてです。特殊変数は InterSystems IRIS に組み込まれており特定のシステム情報をアプリケーションで利用できるようにするために使用されます。特殊変数は、$ 文字の接頭辞で始まりユーザが追加定義することはできません。
<br>
例えば、$HOROLOG は一般的に使用される特殊変数で現在のシステム日付と時刻が格納され InterSystems IRIS ストレージ・フォーマットで保存されます。この変数をユーザが変更することはできません。
<br>
$HOROLOG のような多くの特殊変数は読み取り専用で、SET コマンドを使用して定義することはできません。その他 $NAMESPACE などは読み書き可能で次の方法で定義できます。$NAMESPACE には既存のネームスペースの名前が格納され、setコマンドを使用して現在のネームスペースを変更できます。特殊変数とその機能については、ドキュメント Web サイトの ObjectScript リファレンスを参照してください。
<br>
変数は式の中で使用できます。式には演算子（実行する動作を指定する文字）も含まれます。式は、算術演算子、文字列演算子、関係演算子、論理演算子など、含まれる演算子の種類によって分類されます。
<br>
なお、式は左から右に評価されます。例外として、式の評価時には括弧が考慮されます。
<br>
例にある式を実行して優先順位がどのように機能するかを見てみましょう。まず、変数 num に 4＋7 という算術式を設定します。
<br>
次に、足し算の後に 3 を掛けます。一般的な数学では、掛け算が最初に処理され、25という値になりますが括弧がないので ObjectScript は左から右に評価するためまず加算を行うため、変数 num の値は 33 になります。
<br>
演算の順序を変えるために掛け算の周りに括弧を追加してみましょう。こうすることで、括弧の中にある 7×3 が最初に評価され結果は 25 になります。
<br>
論理演算子や論理式で優先順位がどのように働くかを示すために、まず X を 1 に、Y を 0 に設定します。次に、X が 1 に等しいか、Y が 0 に等しい場合に "This is true" という文字列を返すという条件の IF 文を書きます。この文は括弧なしで書かれているので、文字列 "This is false" を返します。
<br>
この論理比較を正しく行うには括弧を追加して等号演算を入れ子にします。これで期待通りの結果が表示されます： "This is true"
<br>
括弧は演算子の優先順位を強制するために必要であり、コードを明確にするためにも有用でする。
<br>
さまざまな種類の変数とその動作、および演算子の優先順位について詳しくは、ObjectScript のリファレンスを参照し、インターシステムズのドキュメントの Web サイトを参照してください。
</div>
</details>
以下ドキュメントもご参照ください。
- <a href="https://docs.intersystems.com/irislatestj/csp/docbook/DocBook.UI.Page.cls?KEY=GCOS_variables" target="_blank">変数</a>
- <a href="https://docs.intersystems.com/irislatestj/csp/docbook/DocBook.UI.Page.cls?KEY=GCOS_syntax" target="_blank">構文規則</a>
- <a href="https://docs.intersystems.com/irislatestj/csp/docbook/DocBook.UI.Page.cls?KEY=TOS_Precedence" target="_blank">演算子の優先順位</a>

<br>

---
## 4. <img src="./assets/icons/O4.png" width="70%"/>
ObjectScript の基本を学習できましたので、Visual Studio Code を利用してクラス定義を作成します。

以下のビデオでは、クラス定義の作成からインスタンス生成、保存までの流れを確認できます。

{% include youtube-list.html id="kWJCzn9bndQ" list="PLzSN_5VbNaxBPaSSINLzv-CkDJy00bOSQ" %}
<br>
> **英語のオンラインコースもあります**
>
>- <a href="https://learning.intersystems.com/course/view.php?name=IRIS%20Class" target="_blank">オンラインコース（英語）:Creating an InterSystems Class Definition in VS Code</a>
{: .block-tip}

VSCode用ラーニングパスもあります。<a href="VSCode.html" target="_blank">VS Codeを使用した InterSystems サーバサイドの開発</a>をご参照ください。

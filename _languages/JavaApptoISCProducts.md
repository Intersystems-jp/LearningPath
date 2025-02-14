---
title: Java アプリケーションと InterSystems 製品の接続
date: 2024-12-11
permalink: JavaApptoISCProducts.html
layout: post
---
<!-- 
> オリジナルラーニングページ：[Connecting Java Applications to InterSystems Products](https://learning.intersystems.com/course/view.php?name=Java%20Experience)
-->
JDBC、XEP、Hibernate、Native SDK を使用して、Javaアプリケーションを InterSystems IRIS® data platform やその他の InterSystems 製品やテクノロジに接続する方法を確認できます。

他の言語からの接続については、以下の通りです。
- [Python アプリケーションを作成する](WritingPythonAppWithInterSystems.html)

- [.NETアプリケーションとInterSystems製品の接続](dotNetApptoISCProducts.html)

- [Connecting Node.js Application](https://learning.intersystems.com/course/view.php?name=Node.js%20Experience)

---
[1. <img src="./assets/icons/1.png" width="40%"/>](#1-)

[2. <img src="./assets/icons/Java2.png" width="40%"/>](#2-)

[3. <img src="./assets/icons/Java3.png" width="40%"/>](#3-)

[4. <img src="./assets/icons/Java4.png" width="40%"/>](#4-)

[5. <img src="./assets/icons/Java5.png" width="40%"/>](#5-)

[6. <img src="./assets/icons/Java6.png" width="40%"/>](#6-)


---
## 1. <img src="./assets/icons/1.png" width="70%"/>

各 API の利点を確認し、Javaアプリケーションを InterSystems 製品に接続するための方法を確認します。

✅ ビデオ：Java overview（英語／日本語字幕付き）

 {% include youtube.html id="8prvxy1Gn8s" %} 

<details class="transcript2">
<summary> ▶日本語字幕 </summary>
<div class="content">
Java 開発者は、さまざまな方法でアプリケーションを InterSystems IRIS data platform に接続できます。<br>
InterSystems IRIS は強力でマルチモデルに対応しておりこうした接続の柔軟性は、アプリケーションの開発において非常に重要です。<br>
アプリケーションのパフォーマンスを向上させるだけでなく、アプリケーションの開発を加速させることもできるかもしれません。<br>
Java アプリケーションを InterSystems IRIS に接続する方法として 4 種類の API があり JDBC、XEP、Java 用の Native API、および Hibernate の用意があります。<br>
これらの 4 種類の API がそれぞれどのような場面で役立つかを、実際に「タクシー運賃見積アプリケーションの開発」というシナリオを通して検討してみましょう。<br>
このアプリケーションの一部では、リレーショナルなデータモデルの使用が最適かもしれません。例えば、「過去のタクシー記録の照会」などの場合です。<br>
この場合は、Java アプリケーションからデータベースにアクセスするときに非常によく用いられる API である JDBC を使用して InterSystems IRIS のデータにアクセスできます。JDBC を使用することでアプリケーションを InterSystems IRIS に接続しデータの SQL 操作を実行できるようになります。<br>
標準の Create、Read、Update、Delete 操作を実行できるほか、SQL ストアドプロシージャも呼び出せます。JDBC を介した接続はとても簡単です。このテクノロジーに精通していて、JDBC 接続文字列の作成方法をご存知ならばなおさらです。<br>
必要なのは、アプリケーションが InterSystems JDBC ドライバにアクセスできるようにすることだけです。ドライバのファイルは　InterSystems IRIS のインストールディレクトリにあります。<br>
もう 1 つ重要なのは、他の 3 つの Java API はいずれもJDBC の基本接続プロトコルを使用していることです。つまり、まったく新しい接続を設定しなくても、アプリケーション内で 4 つの API をすべて共存させて使用することができます。<br>
アプリケーションの話に戻るとオブジェクトの処理にコードの別の部分がより適している場合もあるでしょう。<br>
例えば、走行中の各タクシーからリアルタイムのデータを取り込む場合です。このようなケースでは XEP をお勧めします。高スループットを実現すべく最適化された API であり、非常に高速でオブジェクトを転送できるからです。<br>
XEP を使用する場合は追加のファイルが必要になりますが、そのリファレンスがあれば、走行中の全タクシーについてアプリケーションを使用して大量のオブジェクト指向データをリアルタイムで処理できるようになります。<br>
アプリケーションでこれらの API のうち 1 つを使用するだけで済む場合もありますし、恐らく JDBC と XEP を組み合わせればリレーショナルおよびオブジェクト指向の要件にも対応できるでしょう。<br>
InterSystems IRIS では、アプリケーションでJava 用の他の 2 つの API を使用することによりメリットがもたらされる場合もあります。<br>
Java 用の Native API は、InterSystems IRIS 内の基本データ構造に直接アクセスするために使用することができます。<br>
これらのデータ構造はグローバルと呼ばれます。グローバルは柔軟性があるため、InterSystems IRIS ですぐに使用できるような複数のデータモデルを提供したり、カスタムデータ構造を作成したりできるようになります。<br>
Native API を使用するときには、データ構造についてよく理解している必要がありますが、前述の一般的なリレーショナルまたはオブジェクト指向のアクセス、および基本グローバルへの直接アクセスによりアプリケーションのパフォーマンスを向上させることもできます。<br>
さらに、Native API により、InterSystems ObjectScript で記述された InterSystems IRIS のクラスメソッドやルーチンも呼び出せます。<br>
タクシーのアプリケーションで、InterSystems IRIS 内のメソッドを利用したい場合は、タクシーの乗車に関して予測されるチップの金額を計算するよう記述されたメソッドや、既に InterSystems IRIS 内に存在している、コメントを分析したり、各ドライバの顕著な特徴を特定したりするためのメソッドが考えられます。<br>
これらのメソッドは、Native API を使用して Java アプリケーションから呼び出せます。<br>
最後に、Java でオブジェクトとリレーショナル間のマッピングを行うサード パーティ製の人気フレームワーク「Hibernate」があります。Hibernate が特に役に立つのは、データ モデルが複雑で、Java クラスをデータベースにマッピングしなければならない場合です。<br>
例えば、タクシーのアプリケーションで、複数のベンダーからのデータの傾向を処理する必要があるとします。その場合は、異なる複雑なデータ構造が使用されている可能性もあります。<br>
Hibernate に慣れていれば、その専門知識を自由に活用し Hibernate を API として使用してアプリケーションの該当箇所の InterSystems IRIS データに接続することができます。<br>
JDBC、XEP、Native API、Hibernate といったさまざまなオプションを使用して Java アプリケーションから InterSystems IRISに 接続することができます。<br>
単一の Java アプリケーションから 4 つすべての API を活用できるため、InterSystems IRIS を使用すれば今まで以上に容易に重要なソリューションを構築できるようになります。
</div>
</details>

<br>
✅ <a href="https://learning.intersystems.com/course/view.php?name=Shared%20Memory%20Connection" target="_blank">ビデオ：Using a Java Shared Memory Connection（英語）</a>：別タブで開きます

<details class="transcript2">
<summary> ▶日本語字幕 </summary>
<div class="content">
Java アプリケーションのパフォーマンスを最大化するために、InterSystems IRIS では Java 共有メモリ接続を提供しています。
<br>
共有メモリ接続では、クライアントとデータベースの両方がホスト・マシン上の同じメモリを共有します。
<br>
この共有メモリは一時的なもので、仮想メモリによってバックアップされます。
<br>
共有メモリ接続は、InterSystems IRIS インスタンスと同じマシン上で実行されている Java アプリケーションによって自動的に使用されます。
<br>
アプリケーションと InterSystems IRIS 間の直接接続を使用することで、共有メモリ接続は、JDBC および他の InterSystems IRIS Java コンポーネントにとって、非常に低レイテンシで高スループットのソリューションとなります。
<br>
アプリケーションと InterSystems IRIS が同じマシン上で動作している場合、既定では共有メモリ接続が使用されます。ただし、必要に応じて、簡単に無効にできます。
<br>
共有メモリ接続を使用するサンプル Java アプリケーションを見てみましょう。
<br>
InterSystems IRIS に接続した後、このアプリケーションはテーブルを作成し 100 万行を挿入し 100 万回行をランダムに選択しテーブルを削除します。これは、100 万人の異なるユーザがテーブルにクエリを実行するようなユースケースを模倣したものです。
<br>
TCP/IP接続とは対照的に、共有メモリ接続を使用した場合の性能向上を確認します。
<br>
このアプリケーションでは、まずTCP/IPを使用し次に共有メモリを使用してそれぞれの接続タイプを使用してテーブル操作を実行します。<br>
接続の作成時に、他の引数と一緒に渡すことができる共有メモリ・プロパティを利用して、接続に共有メモリを使用するかどうかを true または false の値を使って指定できます。<br>
ただし、指定しない場合は可能な限り共有メモリ接続を使用するようにデフォルト設定されます。パフォーマンスを比較するために、アプリケーションはそれぞれの接続タイプを使用してテーブル操作を実行します。<br>
アプリケーションを実行することで、各接続タイプでの処理結果を見ることができます。<br>
予想通り、共有メモリ接続は TCP/IP 接続よりもパフォーマンスが向上します。<br>
InterSystems IRIS のインスタンスを実行しておりそのインスタンスに Java アプリケーションを接続している場合、同じマシン上でアプリケーションを実行することで共有メモリ接続を使用してアプリケーションのパフォーマンスを向上させることができます。
</div>
</details>
<br>
> **英語ですが、オンラインコースもあります**
>- <a href="https://learning.intersystems.com/course/view.php?name=Java%20Connection%20Strategy" target="_blank">Designing a Java Connection Strategy</a>
{: .block-tip}

---
## 2. <img src="./assets/icons/Java2.png" width="70%"/>

SQL ベースのリレーショナル・テーブルへのアクセスには JDBC API を使用できます。

✅ <a href="https://learning.intersystems.com/course/view.php?name=JDBC%20and%20InterSystems%20IRIS" target="_blank">ビデオ：Using JDBC with InterSystems IRIS（英語／日本語字幕付き）</a>：別タブで開きます

<details class="transcript2">
<summary> ▶日本語字幕 </summary>
<div class="content">
InterSystems IRIS Data Platform は、Java Database Connectivity (JDBC) 接続をサポートしており Java アプリケーションから SQL クエリを実行して InterSystems IRIS データベース内のデータを作成、読み取り、更新、および削除することができます。
<br>
JDBC は、Java アプリケーションから SQL を使用してリレーショナル・データベースと対話する業界標準の方法です。
<br>
JDBC を使用して Java アプリケーションと InterSystems IRIS を接続するには、他のデータベースと接続する場合と同じ一般的な手順に従ってください。
<br>
InterSystems JDBC ドライバは、インストール・ディレクトリー内の ∕JDK17 または JDK18 の下にあります。JDBC を使用して他のデータベースに接続する方法と同様に URL は以下の形式で指定します。接続文字列→　jdbc:IRIS://ホスト名またはIP:スーパーサーバーポート/ネームスペース
<br>
InterSystems JDBC ドライバは、JDBC の標準プロトコルである TCP/IP を介した高速で効率的な接続を提供する一方で、InterSystems IRIS に直接チャネルを作成し、JDBC 操作のパフォーマンスを向上させることもできます。このチャネルは、共有メモリ接続と呼ばれます。
<br>
このビデオでは、JDBC を使用して Java アプリケーションを InterSystems IRIS に接続する手順を説明します。
<br>
InterSystems IRIS で JDBC を使用するには、まず、Eclipse、NetBeans、IntelliJ などの Java 開発環境と InterSystems IRIS ドライバが必要です。前述のように、InterSystems IRIS ドライバは、インストール・ディレクトリにあります。
<br>
このドライバを指す Classpath 変数を設定することで Java アプリケーションがドライバを見つけ、最終的に InterSystems IRIS データベースに接続できるようになります。
<br>
次に、Java アプリケーションで以下の手順を実行します。まず、ドライバを使用して、InterSystems IRIS データベースに接続します。次にステートメントオブジェクトを作成し、最後に SQL クエリを実行します。
<br>
タクシー情報を管理するための管理アプリケーションを構築するために、これらの手順を順を追って説明します。
<br>
まず、main() メソッドを持つ Java クラスを作成し、com.intersystems.jdbc ライブラリなど、適切なライブラリをインポートします。
<br>
まず、データベースへの接続を作成します。
<br>
IRISDataSource() を使用して、InterSystems IRIS に接続します。他のデータベースへの接続に使用したことのある標準の DriverManager を使用することもできます。
<br>
次に、URLをデータ・ソースの URL に設定します。
<br>
また、ユーザ名とパスワードを設定し、接続を行います。
<br>
そして、ステートメント・オブジェクトを作成し、SQL クエリを実行します。この例では、GreenTrip テーブルからすべての行を選択します。しかし、ここではデータの作成、読み込み、更新、削除など、ANSII 標準の SQL を実行することができます。
<br>
これが完了したら、必要に応じて結果セットを使用することができます。
<br>
お分かりのように、InterSystems IRIS データベースへの接続は、JDBC を使用した他のデータベースへの接続と同じプロセスを実行します。<br>
手順を確認してみましょう。まず、InterSystems IRIS ドライバを使用してデータベースへの接続を作成し、次に文オブジェクトを作成し、実行する SQL クエリを実行します。その後、Java アプリケーションで結果セットを使用する準備が整います。
</div>
</details>

<br>
✅ <a href="https://docs.intersystems.com/irislatestj/csp/docbook/DocBook.UI.Page.cls?KEY=AFL_jdbc" target="_blank">ドキュメント： JDBC とインターシステムズのデータベース</a>

---
## 3. <img src="./assets/icons/Java3.png" width="70%"/>

XEP を使用して、高性能でリアルタイムのオブジェクトを迅速に格納できます。

✅ <a href="https://learning.intersystems.com/course/view.php?name=Using%20XEP" target="_blank">ビデオ（英語／日本語字幕付き）：Using XEP with Java Applications</a>：別タブで開きます

<details class="transcript2">
<summary> ▶日本語字幕 </summary>
<div class="content">
Java はオブジェクト指向言語ですが、多くの場合、データベースとのやり取りにはJava オブジェクトをリレーショナル アーキテクチャにマッピングする必要があります。
<br>

このため、データの処理にもアプリケーションのコード化にも時間的な遅れが生じます。
<br>
しかし、InterSystems IRIS data platform なら、XEP を使用しシームレスな Javaアプリケーションを構築してあらゆる
オブジェクトを使用できます。
<br>
XEP は、軽量の Java API です。オブジェクトの永続化やTCP/IP 上での InterSystems IRIS データベースへのアクセスを可能にします。
<br>
XEP は、単純な階層から比較的複雑な階層で使用するのに最も適しており高スループットかつきわめて高速なデータの永続化と取得を必要とする状況にも対処できるよう最適化されています。
<br>
Java 用の XEP では、JDBC やNative API などの他の Java API が使用するのと同じInterSystems IRIS への JDBC 接続を利用します。つまり、Java アプリケーション内で 1 つのメソッドが実行中のタスクに最適なパラダイムに基づいて、複数の API を使用できるのです。
<br>
いつ、どのように XEP を使用するのか、事例を見てみましょう。
<br>
ジルはアプリケーションを構築しています。人工衛星から送られる大量のデータを使用して天体を観察するのです。
<br>
このデータには、天体の種類、すなわち星、惑星、小惑星のいずれであるかと、明るさ、直径、地球からの距離、公転速度などの情報が含まれます。
<br>
彼女のアプリケーションは500 憶個の Java オブジェクトを 7 日以内にデータベースに挿入できなくてはなりません。
<br>
ですから、彼女に必要なのは、この単純な天体データを高スループットで処理できる API です。XEP は多数の単純なオブジェクトを迅速に保存できるため、こうした状況に最適です。
<br>
ジルのシナリオは、実際の事例に基づいておりそこでは XEP が天体データの保存と取得に使用されています。
<br>
この事例について、わかりやすく噛み砕いてご説明しましょう。
<br>
ジルは既に、XEP 用と JDBC 用の 2 つの jar ファイルを使用する Java アプリケーションを 設定しています。
<br>
XEP では基本的な JDBC 接続を使用するからです。
これらのファイルは、サポートされている各バージョンのJava 用のものが個別に用意されており、インストール ディレクトリの下位ディレクトリにあります。
<br>
次に必要なのは、データベースに保存するプロパティを定義するデータ クラスです。
<br>
ジルは、Demo.CelestialReading データ クラスを既に定義しておいたようです。人工衛星からのデータを使用するJava アプリケーションの一部に必要だったからです。
<br>
彼女はこの同じクラスを修正なしで使用し、XEP を使用して InterSystems IRIS にデータを保存できます。
<br>
ここで Java アプリケーションに戻りましょう。
<br>
ジルは、このアプリケーションにはいくつかのコードが必要だと判断しました。
<br>
InterSystems IRIS への接続を設定するもの、これらのオブジェクトをデータベースに保存するもの、オブジェクトをデータベースから読み出して画面に表示するものです。
<br>
ジルが最初に作成するのは、InterSystems IRIS への接続を確立するコードです。
<br>
そのために、彼女はまず EventPersister オブジェクトを作成します。このオブジェクトは、データベースへの TCP/IP 接続を確立します。
<br>
Java アプリケーションと InterSystems IRIS のインスタンスが同じ Windows マシン上に存在していれば、TCP/IP ではなく共有メモリー接続をデフォルトで使用してパフォーマンスを向上できます。
<br>
この事例では、InterSystems IRIS のインスタンスはこの特定のポートと IP アドレスに存在し、Java アプリケーションは、ハードコーディングされた一連の資格情報を持つ InterSystems IRIS の USER 名前空間に接続しています。
<br>
EventPersister は java.sql.Connection のIRIS 実装を継承するため、ジルは後で、JDBC の操作の実行も必要だと判断したら、EventPersister から Statement オブジェクトを作成することもできます。
<br>
これでジルは InterSystems IRIS への接続を確立できたので、次に必要なのは InterSystems IRIS 内に対応するテーブルを作成することです。
<br>
XEP では、アプリケーションでこのテーブルを初期化する必要があるのでジルは既存のテーブルに接続できません。
<br>
彼女は、InterSystems IRIS 内に Demo.CelestialReading テーブルを作成するために importSchema メソッドを使用します。
<br>
引数が先ほどの Java データクラスの名前であることに注目してください。
<br>
テストのため、DeleteExtent も呼び出し、前回の実行後からこのテーブルに存在するデータをすべて削除して新たに開始できるようにします。
<br>
ジルは、この行を本番で使用する前に削除します。次に、XEP Event オブジェクトを作成します。
<br>
このオブジェクトは、Java オブジェクトと対応するデータベース オブジェクトとのやり取りを処理します。
<br>
後ほど、このオブジェクトを使用してデータを保存したり、EventQuery オブジェクトや EventIterator オブジェクトを作成したりする方法を説明します。
<br>
このコードをテストするためジルはメソッドを実行し 100 個の Java オブジェクトを生成して、このデータの受信をシミュレーションします。

<br>
これは小規模なセットですが、XEP は大量のオブジェクトを高速で保存するのに優れていることを思い出してください。
<br>
後にジルは人工衛星自体からデータを取得していることでしょう。
<br>
次にジルは、store を xepEventオブジェクトで呼び出してその配列オブジェクトで渡すだけでこの配列全体をデータベースに簡単に保存します。
<br>
XEP は、1 つのコマンドでデータ配列全体をサーバーに保存し送信することができます。
<br>
これは、XEP 固有の機能です。クライアントとサーバーのやり取りの数を減らせれば、結果的にパフォーマンスが向上します。もちろん、アプリケーションに必要なら、オブジェクト 1 つでも同じ構文を使用していつでも保存できます。
<br>
ジルはさらに XEP を使用しデータベースのデータを取得して、天体が地球に衝突して被害をもたらす危険がある場合は、そのデータを修正してフラグをセットする必要もあります。
<br>
そうした危険があるかどうかを判断するため、ジルは、地球周辺のすべての天体を照会したいと考えました。
<br>
特に、地球から 238,900 マイルの距離にあって直径が 40 m を超える、月よりも地球に近い天体です。
<br>
これより小さな天体は、通常、地球の大気によって完全に破壊されます。
<br>
XEP を使用してこのデータを取得するため、ジルはまずこのクエリーを作成して準備する EventQuery オブジェクトをインスタンス化します。
<br>
そうすれば、このオブジェクトを使用してクエリーを実行することもできます。
<br>
次に、彼女が使用したのは EventQueryIterator オブジェクトです。結果セットをループしてそのデータを使用するのです。
<br>
この事例では、ジルは各オブジェクトに対し、オブジェクトを保持して Flag プロパティを true に設定するための一時変数を作成してから、イテレータの set メソッドを使用して更新されたオブジェクトをデータベースに再び保存します。
<br>
ジルが XEP を使用してデータベースを照会したいと考えていても、フラグを設定する必要がなかった場合は、executeAndFetchAll()メソッドを使用しフェッチを並列処理して高速化することも可能でした。このメソッドは、使用可能なプロセッサの数を引数に取ります。
<br>
最後に、EventQuery オブジェクト、Event オブジェクト、EventPersister オブジェクトを閉じます。
<br>
このコードを実行して、正しく機能することを確認しましょう。
<br>
XEP を使用して取得された天体データをここで確認できます。
<br>
また、管理ポータルを使用し SQL 領域全体のテーブルを表示することによっても、このデータが作成されたことを検証できます。
<br>
Java 用 XEP 実装の使用方法を再確認しましょう。
<br>
まず、EventPersister オブジェクトを作成し、InterSystems IRIS へのデータベース接続を確立します。
<br>
次に、まだであれば、importSchema を使用して InterSystems IRIS 内のスキーマを作成し Java データ クラスで定義されたオブジェクト モデルと一致させます。
<br>
次に、対応する Event オブジェクトを作成しクライアントとサーバー間のリンクを管理します。
<br>
そして、store メソッドを使用し、オブジェクトの配列や単一のオブジェクトを保存します。
<br>
データを取得するには、EventQuery オブジェクトをインスタンス化し、クエリーを作成、準備、実行します
そして、EventQueryIterator を使用すれば、オブジェクトが必要なときに、いつでもオブジェクトをループして使用できます。
<br>
まとめ
<br>
ジルは XEP を使用してアプリケーションを構築し、天体データを保持する大量の Java オブジェクトを
迅速に保存することができるので、アプリケーションのパフォーマンスが向上し、必要なメンテナンスを容易に行えるようになりました。
</div>
</details>
<br>

- <a href="https://docs.intersystems.com/irislatestj/csp/docbook/DocBook.UI.Page.cls?KEY=AFL_xep" target="_blank">ドキュメント：XEP による Java オブジェクト永続性</a>

---
## 4. <img src="./assets/icons/Java4.png" width="70%"/>
Native SDK を使用してIRISのグローバル変数にデータを格納したり、InterSystems IRIS のメソッドまたはルーチンを呼び出します。

- <a href="https://learning.intersystems.com/course/view.php?name=Using%20the%20Native%20API" target="_blank">ビデオ（英語／日本語字幕付き）：Using the Native API for .NET</a>：別タブで開きます。


    <details class="transcript2">
    <summary> ▶日本語字幕 </summary>
    <div class="content">
Java 開発者が InterSystems IRIS data platform とインタフェースする方法の 1 つに、Java の Native API があります。
<br>
InterSystems IRIS の Native API を使用すると、JDBC や SQL で使用されるのと同じ基礎となる通信プロトコルを使用してデータに直接アクセスできます。
<br>
このビデオでは、Native API を使用する基本的な利点のいくつかを説明し、Java アプリケーションでどのように使用できるかの例をいくつか探ります。
<br>
Native API の最初の主な利点は、InterSystems IRIS のグローバルの基本アーキテクチャを公開しアプリケーションに直接アクセスを提供して一般的なリレーショナル・アクセスやオブジェクト指向アクセスを省略できることです。
<br>
グローバルは、物理的な InterSystems IRIS データベース内に格納される名前付きの多次元配列です。これは、InterSystems IRIS でデータ用に使用される基本的なストレージ構造です。
<br>
グローバルについてよく知らない場合は、グローバルの詳細を説明した別の学習資料を参照してください。
<br>
Native API のもう 1 つの利点は、InterSystems ObjectScript のコア機能 (クラス・メソッドやルーチンの実行など) を Java アプリケーション内で公開できることです。
<br>
を公開できることです。このビデオの例では、Java コードと Native API を使用して、ObjectScript と同等のアクションがいくつか実行されているのがわかります。
<br>
さらに、Java の Native API は、InterSystems IRIS 内の既存の JDBC 機能を拡張します。これにより Java アプリケーションは、複数のパラダイムを並行して使用してデータを操作できます。
<br>
例えば、Java と InterSystems IRIS 間で同じ物理接続とトランザクション・コンテキストを使用して JDBC を介したリレーショナル・テーブルと Native API を介したグローバルの両方として、データをアプリケーションに公開できます。
<br>
例を参照する前に、InterSystems IRIS でグローバルに直接アクセスして操作するとデータの検証や変換が失われるなど一定の制約があることに注意することが重要です。ただし、InterSystems IRIS でデータに高速かつ直接アクセスできるようになります。
<br>
ここでは、InterSystems IRIS に接続し、Native API を使用してグローバル、クラス・メソッド、およびルーチンにアクセスする Java クラスの例を見てみましょう。
<br>
まず、InterSystems IRIS 用の JDBC ドライバで Java アプリケーションをセットアップする必要があることに注意してください。このファイルは、サポートされる Java のバージョンごとに別々のバージョンがあり、インストール先の /dev/java/lib フォルダのサブディレクトリにあります。
<br>
InterSystems IRIS のグローバル、メソッド、およびルーチンを使用して何かを実行する前に Java アプリケーションをそのインスタンスに接続する必要があります。そのためには、有効な JDBC 接続文字列を作成する必要があります。
<br>
ここに示すように、接続文字列には、IP アドレス、スーパーサーバ・ポート、ネームスペースなど、いくつかの重要な情報が含まれます。接続を確立するには、ユーザー名とパスワードも必要です。
<br>
接続文字列は、残りの条件を追加する前に、jdbc と IRIS を使用して特定の構文に従う必要があることに注意してください。
<br>
接続を作成したら、InterSystems IRIS のインスタンスへの接続ポイントとして使用するネイティブ・オブジェクトを作成する必要があります。
<br>
接続が作成され、ネイティブ・オブジェクトを使用できるようになると、ネイティブ API を使用して、InterSystems IRIS でグローバルにアクセスし操作できるようになります。
<br>
このコードでは、^stocks グローバルの 3 つのノードにいくつかの異なる銘柄の現在の価格を設定しています。次に、これらの銘柄の 1 つの値を取得しそれを出力しています。これは、作成したばかりのネイティブ・オブジェクトから set メソッドと get メソッドを呼び出すことで行われていることに注意してください。
<br>
ObjectScript の ^stocks グローバルの設定と取得に相当するコードを以下に示します。
<br>
次に、^stocks グローバルに対して反復処理を実行できます。ネイティブ API を使用すると while ループで使用するイテレータを作成できます。これにより、グローバル内の各ノードの値を取得できます。
<br>
同等の ObjectScript コードでは、$ORDER 関数が ^stocks グローバルで使用されます。
<br>
最後に、ネイティブ API を使用して、InterSystems IRIS クラスのメソッドやルーチンを呼び出すことができます。
<br>
この Java コードでは、PopulateUtils クラスのメソッドを呼び出してランダムな株式シンボルと 0 ～ 1,000 ドルの間のランダムな値を生成します。次に、この情報を使用して、^stocks グローバルの新しいノードを設定します。
<br>
ObjectScript の同等のコードを見てみると、Java コードはかなり直感的で引数が ObjectScript のメソッド呼び出しと一致していることがわかります。
<br>
ルーチンの呼び出しも同じように動作します。例えば、InterSystems IRIS のバージョン情報を取得するためにルーチンを呼び出したいとします。この場合、このバージョン情報を取得するためにカスタム・ルーチンが作成されます。
<br>
アプリケーションの最後に、データ処理が終了したら、必ずネイティブ・オブジェクトと接続を閉じてください。
<br>
このコードを実行するとコンソールで意図した通りに ^stocks グローバルが正常に操作されていることが確認できます。
<br>
InterSystems IRIS グローバルの構造に精通しており、それらのグローバルに直接アクセスして操作することで Java アプリケーションのパフォーマンスを向上させたいと考えている場合、InterSystems IRIS の Java ネイティブ API を使用すると、その可能性が広がります。
    </div>
    </details>

- <a href="https://docs.intersystems.com/irislatestj/csp/docbook/DocBook.UI.Page.cls?KEY=BJAVNAT_about" target="_blank">ドキュメント：Java Native SDK の概要</a>

- <a href="https://learning.intersystems.com/course/view.php?name=JavaMultiModel" target="_blank">演習（英語）：Interacting with Data In Java Using Multiple Data Models</a>

    InterSystems IRIS® data platform のマルチモデル・アーキテクチャをお試しください。
    
    InterSystems IRIS のマルチ・モデル・アクセスは、グローバルと呼ばれるデータ構造によって実現されています。Java では、Native SDK を使用して InterSystems IRIS に接続し、グローバルを使用してデータを操作できます。もう 1 つのオプションは、JDBC で接続し、業界標準の SQL を使用してデータにアクセスすることです。
    
    この場合、データはリレーショナル・テーブルとしてモデル化されます。XEP または Hibernate を使用して同じデータをオブジェクトとして扱うこともできます。
    
    この機能は、InterSystems ObjectScript でプログラミングする場合でも、外部言語 API のいずれかを使用する場合でも同じです。


---
## 5. <img src="./assets/icons/Java5.png" width="70%"/>
JDBC、XEP、およびネイティブ SDK の組み込みテクノロジに加えて、Hibernate では Java オブジェクトをリレーショナル・テーブルにマッピングできます。

<a href="https://learning.intersystems.com/course/view.php?name=Using%20Hibernate" target="_blank">ビデオ（英語／日本語字幕付き）：Using Hibernate with InterSystems IRIS</a>

※ページ内ビデオは日本語の字幕が付いています。


---
## 6. <img src="./assets/icons/Java6.png" width="70%"/>

接続方法の利点を確認するため、体験環境を使って演習してみましょう。

- <a href="https://learning.intersystems.com/course/view.php?id=2590" target="_blank">体験環境付き演習（英語）：Stock Trading with Java</a>

- <a href="https://docs.intersystems.com/irislatestj/csp/docbook/DocBook.UI.Page.cls?KEY=BEXTSERV" target="_blank">ドキュメント：InterSystems 外部サーバの使用法</a>



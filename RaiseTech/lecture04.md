# 講義最低限おさえておきたいキーワード（しっかりまとめるというか記入しようと思ったが時間もかかるしきりが無いので今度気が向いたら直す）
1. IPアドレス<br>
→インターネット通信における約束事（プロトコル）のひとつであるIPが定める、ネットワーク上の機器に割り当てられる識別番号のこと。
荷物を発送する時の住所のイメージ。通信を行う際のアクセス元（発送元住所）とアクセス先（発送先住所）を特定する役割を担う。

   - プライベートIPアドレス<br>
   →特定のネットワーク内で割り当てられるIPアドレスをプライベートIPアドレス（ローカルIPアドレス）と呼ぶ。
  自宅や社内などの限定されたネットワーク内では、このプライベートIPアドレスが各デバイスに割り当てられ、相互に通信を行う。
  社内ネットワークでは個人情報や機密情報のやりとりがあり、インターネット上に公開されてはいけない。
  プライベートIPアドレスが割り当てられている社内PCがインターネットに接続する際には、プライベートIPアドレスがグローバルIPアドレスへ変換されます。その変換作業は主にルーターが担っています。ここまで

   - グローバルIPアドレス<br>
   →インターネットに接続する際に割り当てられるIPアドレスのこと。
  グローバルIPアドレスはインターネットの世界でユニーク(比類のないもの)である必要があるため、同じアドレスが違うユーザーに割り当てられないように管理される。
    
     - グローバルIPアドレスとプライベートIPアドレスの違いとは（コピペ。気が向いたら少し直す）<br>
     →グローバルIPアドレスはインターネットに接続したい場合に必要です。
    インターネットの窓口を担っており、住所が付与されるのはルーターです。
    反対にプライベートIPアドレスは、基本的にルーター配下の特定のネットワーク内のデバイスに割り当てられます。
    インターネットを通じて情報のやり取りをする宛先になるのがグローバルIPアドレス。
    その窓口（ルーター）に届いた情報を指定の届け先（デバイス）に受け渡すための宛先がプライベートIPアドレスです。
    プロバイダーから割り当てられるIPアドレスが1つであっても、ルーター配下に接続されている複数のデバイスがインターネットに接続できるのは、プライベートIPアドレスのおかげです。

   - CIDR（コピペ。気が向いたら少し直す）<br>
   →CIDR（Classless Inter-Domain Routing）は、アドレスクラス というIPアドレスの分類方法に縛られずに、IPアドレスの割り当てやルーティングの柔軟性を高めるための方法です。
    CIDRでは、IPアドレスは「xxx.xxx.xxx.xxx/yy」という形式で書かれ、xxx.xxx.xxx.xxx は通常のIPアドレス、yy はサブネットマスクのビット数を示します。
    192.168.0.0/16 の場合は、IPアドレスの先頭から16ビットがネットワーク部で、残りの 32 - 16 = 16 ビットがホスト部であることを表します。
   「192.168.1.0/24」の場合、IPアドレスは 192.168.1.0から192.168.1.255 までの範囲を指します。

1. ポート番号
   - プロトコル（コピペ。気が向いたら少し直す）<br>
   →プロトコルとは、コンピュータでデータをやりとりするために定められた手順や規約、信号の電気的規則、通信における送受信の手順などを定めた規格を意味します。
     異なるメーカーのソフトウエアやハードウエア同士でも、共通のプロトコルに従うことによって、正しい通信が可能になります。
     目的別にさまざまなプロトコルがあり、身近なものとして、インターネット接続に用いるTCP/IP（次参照）や、Web（何の略かと意味調べる）閲覧などに用いるHTTP（次参照）、メール送受信に用いるPOP（何の略かと意味調べる）やSMTP（次参照）などが挙げられます。
     いずれも末尾の「Ｐ」はProtocol（プロトコル）の略です。
     
   - HTTP（コピペ。気が向いたら少し直す）<br>
     →httpとは「Hyper Text Transfer Protocol（ハイパーテキスト・トランスファー・プロトコル）」の略で、ホームページ（Webサイト）を環境に依（よ）らず問題なく表示するための通信規格（プロトコル）のことです。
      URLの最初の部分で「http://～」と記載されています。
     
   - HTTPS（コピペ。気が向いたら少し直す）<br>
     →httpsとは、「Hypertext Transfer Protocol Secure（ハイパーテキスト・トランスファー・プロトコル・セキュア）」の略で、SSL（暗号化通信）(SSLは何の略かと意味暗号化の意味　https://ds-b.jp/dsmagazine/pages/200/)によってセキュリティを高めたhttpのことです。
      httpsにすることで、通信経路での第三者による情報の盗聴や改ざんのリスクを防止できます。
   - FTP（コピペ。気が向いたら少し直す）<br>
     →FTP（File Transfer Protocol）とは、サーバとクライアントの間でファイル転送を行う際に必要となる通信プロトコルです。
      通信プロトコルは通信する際の手順や規約のことで、ほかにもSFTPなど種類があります。
      FTP通信にはFTPソフトとFTPサーバが必要になり、両者間でデータがやり取りされるという仕組みです。
     
   - SSH（コピペ。気が向いたら少し直す）<br>
     →SSHとは、Secure Shell（セキュアシェル）の略称で、リモートコンピュータと通信するためのプロトコルです。
     認証部分を含めネットワーク上の通信がすべて暗号化されるため、安全に通信することができます。
     
     従来は、TelnetやFTPなどの手法でリモート通信が行われていましたが、これらはパスワードを暗号化のない平文で送信してしまうため、盗聴のリスクがありました。
     SSHでは公開鍵暗号を利用し、共通鍵を暗号化して鍵交換を行っています。かつ、通信自体は高速な共通鍵暗号を用いているため、速度低下を抑えています。

     認証の仕組みもパスワード、公開鍵、ワンタイムパスワードなど多様化してきており、適切な認証方法を選択できます。
     大手ネットワーク機器メーカーなどは、セキュリティの観点からTelnetではなく、SSHによるアクセスを推奨しています。

     SSHはAndroidやiOSにも実装されているプロトコルのため、ネットワークにSSHの利用環境が整備されていれば、スマートフォンやタブレットから容易にリモート接続が可能となります。
     スマートデバイスの所有があたり前になりつつある昨今では、ビジネスでも大きな利用価値が生まれ、大企業向けのルーターなどではSSHを実装したものも販売されています。
     
   - SMTP（コピペ。気が向いたら少し直す）<br>
     →Simple Mail Transfer Protocol の略です。
     これは、インターネット上で E メールメッセージを送受信するために使用される通信プロトコルです。
     メールサーバーや他のメッセージ転送エージェント (MTA) は、SMTP を使用してメールメッセージを送信、受信、中継します。
     SMTPS (Simple Mail Transfer Protocol Secure) は、トランスポート層セキュリティを使用して SMTP を保護する方法です。
     通信相手の認証、データの完全性、機密性を提供することを目的としています。
     SSL (Secure Sockets Layer) またTLS (Transport Layer Security) を使用して安全な接続を確立し、Eメール送信の機密性と完全性を確保します。
     クライアントとサーバーはアプリケーションレイヤーで通常の SMTP を使用し、接続は SSL または TLS によって保護されます。
     
   　SMTP サーバーとは何ですか?
   　送信メールサーバーとも呼ばれる SMTP サーバーは、送信 E メールメッセージを処理するコンピューターまたはソフトウェアです。一般に、メールサーバーとは、E メールを収集、処理、および配信するシステムを指します。SMTP サーバーとは、特にSimple Mail Transfer Protocol (SMTP) を使用して送信メールを送信するメールサーバーのコンポーネントを指します。
   　メールサーバーは、受信および送信Eメールの両方を処理しますが、SMTP サーバーは、送信 E メールを適切な送信先に送信、および中継するタスクのみを行います。送信Eメールサーバーとも呼ばれます。

   https://aws.amazon.com/jp/what-is/smtp/#:~:text=SMTP%20%E3%81%AF%20Simple%20Mail%20Transfer,%E3%80%81%E5%8F%97%E4%BF%A1%E3%80%81%E4%B8%AD%E7%B6%99%E3%81%97%E3%81%BE%E3%81%99%E3%80%82
   
   - TCP/IP（コピペ。気が向いたら少し直す）<br>
     →TCP/IPとは、インターネットを含む多くのコンピュータネットワークにおいて、世界標準的に利用されている通信プロトコルのことです。TCP/IPはインターネット・プロトコル・スイートとも呼ばれ、World Wide Webの発明と共にコンピュータ及びコンピュータネットワークに革命をもたらしたことがきっかけで現在でも標準的に利用されている通信規則です。インターネットを利用する際は異なるハードウェアやOSであっても通信が確立していなければネットワークは繋がりません。従ってTCP/IPは機器やOSが異なっても共通のプロトコルを用いて通信を成立させるものです。
例を上げると、私たちがインターネットでWebページを見るときに利用するプロトコルは、TCP（Transmission Control Protocol）とIP（Internet Protocol）を利用しています。
TCPとは通信プロトコルのひとつで簡単に説明すると「送ったデータが相手に届いたか、その都度確認しながら通信するやり方」や「正確な信号を送信する通信の規格を定めたもの」と言えます。わかりやすく言うと、エラーが起きてもクライアント側は繰り返しサーバにリクエストを送信し、サーバ側は正常に受け取って確実にレスポンスを返します。この一連の流れをセッションと呼びHTTPではリクエストとレスポンスで完結されます。詳しくは「HTTPリクエストとレスポンス」を御覧ください。
IPとはIPアドレスと呼ばれる数値を付与しその数字を用いて通信先の指定及び呼び出しを行いネットワーク通信を行うことです。IPアドレスにはIPv4とIPv6が存在し記述の仕方が異なります。

1. VPC、VPN、DirectConnect
   - VPC（コピペ。気が向いたら少し直す）<br>
     →Amazon Virtual Private Cloud (Amazon VPC) を使用すると、論理的に隔離されている定義済みの仮想ネットワーク内で AWS リソースを起動できます。仮想ネットワークは、お客様自身のデータセンターで運用されていた従来のネットワークによく似ていますが、AWS のスケーラブルなインフラストラクチャを使用できるというメリットがあります。
次の図表は、VPC の例を示しています。VPC には、リージョンの各アベイラビリティーゾーンに 1 つのサブネット、各サブネットに EC2 インスタンス、VPC 内のリソースとインターネットとの通信を可能にするインターネットゲートウェイがあります。

   - VPN（コピペ。気が向いたら少し直す）<br>
     →VPNとは「Virtual Private Network（仮想プライベートネットワーク）」の頭文字をとった略称で、インターネット上における通信データを暗号化し、IPアドレスを隠すことで、オンラインデータを第三者から保護する技術およびサービスです。通常のインターネット回線を利用しながら、VPN接続を確立することで、安全でプライベートな通信環境を提供します。
このページでは、「VPNって何？」「VPN接続とは何か？」と疑問を持っている方に対して、VPN接続のメリットや必要性、機能や役割、仕組み、種類と特徴を簡単にわかりやすく説明します。

   - DirectConnect（コピペ。気が向いたら少し直す）<br>
     →AWS Direct Connect クラウドサービスは、AWS リソースにつながる最短のパスです。ネットワークトラフィックは転送中に AWS グローバルネットワークに残り、公開インターネットにアクセスすることはありません。これにより、ボトルネックにぶつかったり、予期しないレイテンシー（）が増加したりする可能性が低くなります。新しい接続を作成する際には、AWS Direct Connect デリバリパートナーが提供するホスト接続、または AWS の専用接続を選択することができ、世界中の AWS Direct Connect ロケーション（）でデプロイ（）することができます。AWS Direct Connect SiteLink を使用すれば、AWS Direct Connect ロケーションの間でデータを送信し、グローバルネットワーク内のオフィスとデータセンター間でプライベートネットワーク接続を作成できます。
     
1. サブネット、リージョン、AZ、セキュリティグループ
   - サブネット（コピペ。気が向いたら少し直す）<br>
     →サブネット（サブネットワーク）は、ネットワーク内のネットワークです。サブネットは、ネットワークをより効率的にします。
     サブネット化により、ネットワークトラフィックは不要なルーターを通過せずとも、短い距離を移動して宛先に到達できます。
     さて、アリスが隣町に住んでいるボブ宛てに手紙を送る場面を想像してみてください。できるだけ早くボブに手紙を届けるには、アリスの郵便局からボブの町の郵便局へ、そしてボブへという順番が一番です。もし手紙が数百マイル離れた郵便局に最初に送られたら、アリスの手紙はボブに届くまでにずっと時間がかかるでしょう。
郵便サービスと同様に、メッセージができる限り直接移動する場合に、ネットワークはより効率的になります。ネットワークが別のネットワークからデータパケットを受信すると、パケットが宛先に向けて非効率的なルートを取らないように、サブネットごとにパケットを分類してルーティングします。

   - リージョン（コピペ。気が向いたら少し直す）<br>
     →データセンターが設置されている独立したエリアのことを指します。 クラウド サービスを提供している Google や Amazon、Microsoft などの各事業者それぞれが独自に区分している地理的範囲
     
   - AZ（コピペ。気が向いたら少し直す）<br>
     →アベイラビリティゾーン
     複数の「データセンター（DC）」から構成されるインフラ設備の単位です。同じAZ内のデータセンター群は冗長的で高速なネットワークで結ばれており、あたかも同じ場所にある設備であるかのように利用することができます。自然災害・電力供給・ネットワーク等の面で独立した単位となっており、あるAZがダウンしても他のAZは稼働できるよう設計されています。
AZ間は物理的に意味のある距離で離されています。具体的には、最大100kmまでの距離に配置され、ネットワーク遅延が2ms以下という高速なネットワークで接続されています。
また、AZと外部ネットワークとの中継点として「Transit Center（トランジットセンター）」という概念が存在します。AZはTransit Centerを介して他のリージョンや外部インターネットに接続されます。このTransit Centerも冗長化されており、どのAZも最低2つのTransit Centerにつながれています。
リージョンよりも小さく、かつ独立したデータセンター群による単位がアベイラビリティーゾーンです。

   - セキュリティグループ（コピペ。気が向いたら少し直す）<br>
     →セキュリティグループは、関連付けられたリソースに到達するトラフィックおよびリソースから離れるトラフィックを制御します。例えば、セキュリティグループを EC2 インスタンスに関連付けると、インスタンスのインバウンドトラフィックとアウトバウンドトラフィックが制御されます。
VPC を作成すると、デフォルトのセキュリティグループが使用されます。VPC ごとに追加のセキュリティグループを作成し、それぞれに独自のインバウンドルールとアウトバウンドルールを設定できます。インバウンドルールごとに、送信元、ポート範囲、プロトコルを指定できます。アウトバウンドルールごとに、送信先、ポート範囲、プロトコルを指定できます。


1. ネットワークの箱がどう区切られていて、どういうアクセスができるのかのイメージを脳内で描けるかどうかが、ひとつのポイントになってきます。

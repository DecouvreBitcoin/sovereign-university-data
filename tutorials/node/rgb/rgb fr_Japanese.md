名前: RGB
説明: RGB の紹介とアセットの作成

# RGB プロトコルの簡単な紹介

![RGB vs Ethereum](assets/0.png)

## 紹介

2009 年 1 月 3 日、Satoshi Nakamoto は最初の Bitcoin ノードを立ち上げました。その瞬間から、新しいノードが参加し、Bitcoin は新しい形の生命体のように振る舞い始めました。この生命体は進化し続け、Satoshi によって非常によく考えられた独自の設計により、世界で最も安全なネットワークになりました。経済的なインセンティブにより、マイナーと呼ばれるユーザーがエネルギーや計算能力に投資することを促し、ネットワークのセキュリティに貢献しています。

Bitcoin が成長し続け、採用される中で、スケーラビリティの問題に直面しています。Bitcoin ネットワークでは、新しいトランザクションを含んだブロックを約 10 分ごとにマイニングすることができます。1 日に 144 ブロックがあり、1 つのブロックに最大 2700 のトランザクションが含まれると仮定すると、Bitcoin は秒間 4.5 トランザクションしか許容しません。Satoshi はこの制限について認識しており、2011 年 3 月に Mike Hearn に送ったメール 1 で、現在のところペイメントチャネルとして知られているものがどのように機能するかを説明しています。これにより、確認を待たずにマイクロペイメントを迅速かつ安全に行うことができます。これがオフチェーンプロトコルの登場する場所です。

Christian Decker2 によれば、オフチェーンプロトコルは一般的に、ユーザーがブロックチェーンのデータを使用し、ブロックチェーン自体には触れずに最後の瞬間まで処理するシステムです。この概念に基づいて、Lightning Network が生まれました。Lightning Network はオフチェーンプロトコルを使用してほぼ即時の Bitcoin 支払いを可能にし、これらのトランザクションがブロックチェーンに書き込まれないため、秒間数千のトランザクションを処理し、Bitcoin のスケーラビリティを向上させます。

Bitcoin のオフチェーンプロトコルに関する研究と開発は、Pandora の箱を開けたようなものであり、今日では分散型の価値転送以上のことが可能であることがわかっています。非営利団体である LNP/BP Standards は、Bitcoin と Lightning Network 上のレイヤー 2 およびレイヤー 3 のプロトコルの開発に焦点を当てており、その中でも RGB は特に注目されています。

## RGB とは？

RGB は、Peter Todd3 のユニークなシールとクライアントサイドの検証に関する研究から生まれました。これは 2016 年から 2019 年にかけて Giacomo Zucco とコミュニティによって Bitcoin と Lightning Network のためのより良いアセットプロトコルとして形成されました。これらのアイデアのさらなる進化により、RGB は Maxim Orlovsky によって完全なスマートコントラクトシステムとして開発され、コミュニティの参加を得て 2019 年以降実装されています。
RGB は、スケーラブルかつ機密性の高い方法で複雑なスマートコントラクトを実行するためのオープンソースのプロトコルのセットと定義することができます。RGB は特定のネットワークではありません（Bitcoin や Lightning のような）；各スマートコントラクトは、異なる通信チャネル（デフォルトでは Lightning ネットワーク）を使用して相互作用できる契約参加者のセットにすぎません。RGB は、スマートコントラクトのコードとオフチェーンのデータを Bitcoin ブロックチェーンを状態のコミットメントレイヤーとして使用し、Bitcoin（および Script）トランザクションをスマートコントラクトの所有権制御システムとして利用することで、スケーラブルになります。スマートコントラクトの進化はオフチェーンのスキーマで定義されますが、最後に重要なことは、すべてがクライアントサイドで検証されるということです。

簡単に言えば、RGB は、ユーザーがスマートコントラクトを監査し、実行し、いつでも個別に検証できるシステムであり、他の「伝統的な」システムとは異なり、追加コストがかからないため、ブロックチェーンを使用しません。複雑なスマートコントラクトシステムは、Ethereum によって先駆けられましたが、ユーザーが各操作ごとに大量のガスを消費する必要があるため、約束されたスケーラビリティには到達せず、現行の金融システムから除外されたユーザーにとっては選択肢になりませんでした。

現在、ブロックチェーン業界は、スマートコントラクトのコードとデータをブロックチェーンに格納し、ネットワークの過剰なサイズやコンピュータリソースの乱用に関係なく、各ノードで実行する必要があると主張しています。RGB が提案するスキーマは、ブロックチェーンのパラダイムを破り、スマートコントラクトとデータをブロックチェーンから分離することで、他のプラットフォームで見られるネットワークの過負荷を回避するために、よりスマートで効率的なものです。さらに、各ノードにすべての契約を実行することを強制するのではなく、関係する当事者のみが実行するため、これまでにないレベルの機密性が追加されます。

![RGB vs Ethereum](assets/1.png)

## RGB におけるスマートコントラクト

RGB では、スマートコントラクトの開発者が、契約が時間とともにどのように進化するかを指定するスキーマを定義します。スキーマは、RGB 内でスマートコントラクトを構築するための標準であり、契約の発行時には発行者、契約の定義時にはウォレットまたは取引所が特定のスキーマに準拠し、契約を検証する必要があります。検証が正常である場合のみ、各当事者は要求を受け入れ、アセットと一緒に作業することができます。
RGB におけるスマートコントラクトは、状態変化の有向非巡回グラフ（DAG）であり、グラフの一部のみが常に知られており、残りの部分にはアクセスできません。RGB スキーマは、スマートコントラクトの開始時にこのグラフの進化のための基本ルールセットです。契約参加者はこれらのルールに追加することができます（スキーマで許可されている場合）し、結果として得られるグラフはこれらのルールの反復的な適用によって構築されます。

## 交換可能なアセット

RGB における交換可能なアセットは、LNPBP RGB-20 仕様に従います。RGB-20 が定義されると、アセットの「ジェネシスデータ」として知られるデータが Lightning ネットワークを介して配布され、アセットを使用するために必要なものが含まれます。基本的なアセットの形式では、セカンダリエミッション、トークンの破壊、名前の変更、置き換えは許可されません。

時には、エミッターは将来的にさらにトークンを発行する必要があります。たとえば、米ドルなどのインフレ通貨の価値にリンクされたステーブルコイン（USDT）などです。そのためには、より複雑な RGB-20 スキーマが存在し、ジェネシスデータに加えて、エミッターが送信を生成する必要があります。これらの情報は Lightning ネットワークでも流通し、アセットの総供給量を知ることができます。トークンの燃焼や名前の変更にも同様の手法が適用されます。

アセットに関する情報は公開または非公開にすることができます。エミッターが機密性を要求する場合、トークンに関する情報を共有せずに完全な機密性で操作することができます。逆に、エミッターや保有者がプロセス全体を透明にする必要がある場合もあります。これはトークンのデータを共有することで実現されます。

## RGB-20 手順

破壊手順はトークンを無効化し、燃焼されたトークンは使用できなくなります。

置き換え手順は、トークンが燃焼され、同じトークンの新しい数量が作成される場合に発生します。これにより、アセットの履歴データのサイズを縮小することができ、アセットの速度を維持するために重要です。

アセットを置き換えることなく燃焼する可能性のあるユースケースをサポートするために、RGB-20 のサブスキーマが使用されます。

## 交換不可能なアセット

RGB における非代替性トークン（NFT）は、LNPBP RGB-21 仕様に従います。NFT を扱う際には、メインスキーマとサブスキーマがあります。これらのスキーマには、トークンの所有者がカスタムデータを添付するためのエンコーディング手順があります。現在の NFT で最も一般的な例は、トークンに関連付けられたデジタルアートです。トークンの発行者は、RGB-21 のサブスキーマを使用してこのデータのエンコーディングを禁止することができます。RGB は、他の NFT ブロックチェーンシステムとは異なり、P2P ネットワークの拡張である Bifrost を使用して、分散化された大容量のトークンメディアデータを耐検閲性を持って配布することができます。Bifrost は、RGB 固有の多くのスマートコントラクト機能を構築するためにも使用されています。

Fungible アセットや NFT の他にも、RGB と Bifrost は DEX、流動性プール、アルゴリズム安定コインなど、他の形式のスマートコントラクトを生成するために使用することができます。これについては、将来の記事で詳しく説明します。

## RGB の NFT と他のプラットフォームの NFT の比較

- ブロックチェーン上の高価なストレージは不要
- IPFS は不要で、代わりに完全に暗号化された P2P ネットワークの拡張（Bifrost）が使用されます
- 特別なデータ管理ソリューションは不要 - 再び、Bifrost がその役割を果たします
- NFT トークンやアセット/コントラクトの ABI のデータをウェブサイトに信頼する必要はありません
- 組み込みの DRM 暗号化と所有権管理
- Lightning ネットワーク（Bifrost）を使用したバックアップインフラストラクチャ
- コンテンツの収益化手段（NFT 自体の販売だけでなく、コンテンツへのアクセスも可能）

## 結論

Bitcoin の発売から約 13 年が経ち、この領域で多くの研究と実験が行われてきました。成功と失敗を通じて、実践的な観点から分散システムの振る舞いをより良く理解することができました。真の分散化とは何か、どのような行動が中央集権化に向かう傾向があるのか。これらの経験から、真の分散化は稀であり、達成するのが困難であることがわかりました。真の分散化は Bitcoin によってのみ実現されており、そのために私たちは Bitcoin に集中して取り組んでいます。

RGB は Bitcoin の中で独自の存在感を持っており、私が学んだことを投稿していきます。次の記事では、LNP ノードと RGB の紹介、およびそれらの使用方法について説明します。

- 1 https://plan99.net/~mike/satoshi-emails/thread4.html
- 2 https://btctranscripts.com/chaincode-labs/chaincode-residency/2018-10-22-christian-decker-history-of-lightning/
- 3 https://lists.linuxfoundation.org/pipermail/bitcoin-dev/2016-June/012773.html- 4 https://github.com/LNP-BP/LNPBPs/blob/master/lnpbp-0020.md

- 5 https://github.com/LNP-BP/LNPBPs/blob/master/lnpbp-0021.md

# RGB-node チュートリアル

## はじめに

このチュートリアルでは、RGB-node を使用して交換可能なトークンを作成し、転送する方法について説明します。このドキュメントは RGB-node のデモを基にしており、実際のテストネットのデータを使用しています。そのため、部分的に署名されたビットコイントランザクション（PSBT）を構築する必要があります。以降、psbt と呼びます。

## 必要条件

Linux ディストリビューションの使用をお勧めします。このチュートリアルは Pop!/\_OS を使用して作成されており、Ubuntu に基づいています。以下が必要です：

- cargo
- Bitcoin core
- git

注意：このチュートリアルでは、Linux のターミナルでのコマンドの実行を示しています。ユーザーが入力する内容とターミナルでの応答を区別するために、$記号を使用して bash のコマンドプロンプトを示します。

以下の依存関係をインストールする必要があります：

```
$ sudo apt install -y build-essential pkg-config libzmq3-dev libssl-dev libpq-dev libsqlite3-dev cmake
```

コンパイルと実行

RGB-node は開発中（WIP）ですので、特定のコミット（3f3c520c19d84c66d430e76f0fc68c5a66d79c84）に移動して正しくコンパイルおよび使用する必要があります。そのため、次のコマンドを実行します。

```
$ git clone https://github.com/rgb-org/rgb-node.git
$ cd rgb-node
$ git checkout 3f3c520c19d84c66d430e76f0fc68c5a66d79c84
```

次に、次のフラグを使用してコンパイルします。--locked フラグを使用することを忘れないでください。なぜなら、clap のバージョンで重大な変更が導入されたからです。

```
$ cargo install --path . --all-features --locked

....
....
    Finished release [optimized] target(s) in 2m 14s
  Installing /home/user/.cargo/bin/fungibled
  Installing /home/user/.cargo/bin/rgb-cli
  Installing /home/user/.cargo/bin/rgbd
  Installing /home/user/.cargo/bin/stashd
   Installed package `rgb_node v0.4.2 (/home/user/dev/rgb-node)` (executables `fungibled`, `rgb-cli`, `rgbd`, `stashd`)

```

Rust コンパイラが示すように、バイナリは$HOME/.cargo/binディレクトリにコピーされました。もしコンパイラが別の場所にコピーした場合は、そのディレクトリが$PATH に含まれていることを確認してください。
インストールされたバイナリの中で、私たちは 3 つのデーモンまたはサービス（d で終わるファイル）とコマンドラインインターフェース（cli）を見ることができます。cli は、メインデーモン rgbd との対話を可能にします。このチュートリアルでは 2 つのノードを実行するため、2 つのクライアントも必要です。それぞれのクライアントは、それぞれのノードに接続する必要があります。そのために、2 つのエイリアスを作成します。

```
alias rgb0-cli="$HOME/.cargo/bin/rgb-cli -d $HOME/rgbdata/data0 -n testnet"
alias rgb1-cli="$HOME/.cargo/bin/rgb-cli -d $HOME/rgbdata/data1 -n testnet"
```

エイリアスを単純に実行するか、$HOME/.bashrc ファイルの末尾に追加して source $HOME/.bashrc を実行することができます。

前提条件

RGB-node は、ウォレットに関連する機能を管理しません。単に RGB に関連するタスクを実行し、ビットコインコアなどの外部ウォレットから提供されるデータに対して処理を行います。特に、発行と転送の基本的なワークフローをデモンストレーションするために、次のものが必要です。

- rgb-node-0 が新たに発行されたアセットにリンクする issuance_utxo
- rgb-node-1 がアセットを受け取る receive_utxo
- rgb-node-0 がアセットのお釣りを受け取る change_utxo
- 出力の公開鍵を含む部分的に署名されたビットコイントランザクション（tx.psbt）。このトランザクションには、転送のコミットメントを含めるために出力の公開鍵を調整する必要があります。
  ビットコインコア cli を使用しますので、testnet で bitcoind デーモンが実行されている必要があります。これにより、相互運用性が得られ、最終的にはこのチュートリアルに従って RGB を使用している他のユーザーに自分自身のアセットを送信することができます。
  簡単にするために、このエイリアスを~/.bashrc ファイルの末尾に追加します。

```
alias bcli="bitcoin-cli -testnet"
```

未使用の出力トランザクションをリストアップし、2 つを選択します。1 つは issuance_utxo であり、もう 1 つは change_utxo です。どちらがどちらかは重要ではありませんが、発行者がこれら 2 つの UTXO を制御していることが重要です。

```
$ bcli listunspent
[
  {
    "txid": "4c1785210d8930959f530072cffea7f9606e0599b0de9e89aed60f2e9f133893",
    "vout": 1,
    "address": "tb1qn4w9u5x0hxgm30hx6q2rhdwz58xr4ekqdq0vgm",
    "label": "",
    "scriptPubKey": "00149d5c5e50cfb991b8bee6d0143bb5c2a1cc3ae6c0",
    "amount": 0.01703963,
    "confirmations": 62432,
    "spendable": true,
    "solvable": true,
"desc": "wpkh([ec924f82/0'/0'/5']031e0fc9a03e69326c3deeabfd749a7f7b094e3151ada90cd13019efac663c5663)#dj7rhpdt",    "safe": true
  },
  {
    "txid": "cd66d3b77dfc1c2ecf958847c16a8a1311bba84ee7bf9dd55592a7b97b13028f",
    "vout": 1,
    "address": "tb1qyd537gf0xmm9ehmhaf3nv0a230crg56mhp9ap3",
    "scriptPubKey": "001423691f212f36f65cdf77ea63363faa8bf034535b",
    "amount": 0.02877504,
    "confirmations": 189184,
    "spendable": true,
    "solvable": true,
    "desc": "wpkh([ec924f82/0'/1'/0']03ae333417e86840145e95ab2852c8f7ca8b8f82cd910883f7ce0c69649403cef2)#jlcj23vw",
    "safe": true
  }
]
```

さらに進む前に、アウトポイントについて話さなければなりません。1 つのトランザクションには複数のアウトプットが含まれることがあります。アウトポイントには、32 バイトの TXID と 4 バイトのアウトプットインデックス（vout）が含まれており、コロン（:）で区切られて特定のアウトプットを参照します。listunspent の出力では、2 つの UTXO を見つけることができます。それぞれの UTXO には、txid と vout があります。これらは issuance_utxo と change_utxo です。
'receive_utxo'は、受信者が制御する UTXO です。この場合、別のウォレットのアウトポイントである e40d9037e31d3f440552b30af16e764cf25ffda3899b4851cc4e38fd64718b09:0 を使用します。

- issuance_utxo: 4c1785210d8930959f530072cffea7f9606e0599b0de9e89aed60f2e9f133893:1
- change_utxo: cd66d3b77dfc1c2ecf958847c16a8a1311bba84ee7bf9dd55592a7b97b13028f:1
- receive_utxo: e40d9037e31d3f440552b30af16e764cf25ffda3899b4851cc4e38fd64718b09:0

次に、部分的に署名されたトランザクション（tx.psbt）を作成し、出力を調整して送金のコミットメントを含めます。自分の txid と vout で置き換えることを忘れないでください。宛先アドレスは実際には重要ではありません。自分のアドレスまたは他の人のアドレスであっても構いません。これらの sats がどこに行くかは重要ではありません。重要なのは、issuance_utxo を使用することです。
$ bcli walletcreatefundedpsbt "[{/"txid/":/"4c1785210d8930959f530072cffea7f9606e0599b0de9e89aed60f2e9f133893/",/"vout/":1}]" "[{/"tb1q9crtjp0y6rt00c4fcrmuamrylzkcalcxls80j9/":/"0.00050000/"}]"{
"psbt": "cHNidP8BAHECAAAAAZM4E58uD9auiZ7esJkFbmD5p/7PcgBTn5UwiQ0hhRdMAQAAAAD/////ArM7GQAAAAAAFgAU4xQr/g1lgG2P9+gZudpFD8mOGGRQwwAAAAAAABYAFC4GuQXk0Nb34qnA987sPitjv8GAAAAAAABAHECAAAAAYiK0TdTiaEs4oDovRokqspfLZr5EHYH8Pnj/Tv5GFB5AQAAAAD+////Av8Bh80AAAAAFgAUsLjOd30aRkUna41LAT5c3CnAz5obABoAAAAAABYAFJ1cXlDPuZG4vubQFDu1wqHMOubAyw8gAAEBHxsAGgAAAAAAFgAUnVxeUM+5kbi+5tAUO7XCocw65sAiBgMeD8mgPmkybD3uq/10mn97CU4xUa2pDNEwGe+sZjxWYxDskk+CAAAAgAAAAIAFAACAACICA2J21wOqW6bj7/ePTVI7QGvU6e4Sk8DhN5pmd9hrwSd7EOyST4IAAACAAQAAgAcAAIAAAA==",
"fee": 0.00000280,
"changepos": 0'

````

この抜粋では、base64でエンコードされたpsbtが与えられており、それを使用してtx.psbtを作成します。
$ echo "cHNidP8BAHECAAAAAZM4E58uD9auiZ7esJkFbmD5p/7PcgBTn5UwiQ0hhRdMAQAAAAD/////ArM7GQAAAAAAFgAU4xQr/g1lgG2P9+gZudpFD8mOGGRQwwAAAAAAABYAFC4GuQXk0Nb34qnA987sZPitjv8GAAAAAAABAHECAAAAAYiK0TdTiaEs4oDovRokqspfLZr5EHYH8Pnj/Tv5GFB5AQAAAAD+////Av8Bh80AAAAAFgAUsLjOd30aRkUna41LAT5c3CnAz5obABoAAAAAABYAFJ1cXlDPuZG4vubQFDu1wqHMOubAyw8gAAEBHxsAGgAAAAAAFgAUnVxeUM+5kbi+5tAUO7XCocw65sAiBgMeD8mgPmkybD3uq/10mn97CU4xUa2pDNEwGe+sZjxWYxDskk+CAAAAgAAAAIAFAACAACICA2J21wOqW6bj7/ePTVI7QGvU6e4Sk8DhN5pmd9hrwSd7EOyST4IAAACAAQAAgAcAAIAAAA==" | base64 -d > tx.psbt```

新しいディレクトリrgbdataを作成し、各ノードのデータディレクトリを格納します。

````

$ mkdir $HOME/rgbdata
$ cd $HOME/rgbdata

```

すでに$HOME/rgbdataにいる場合は、異なるターミナルで各ノードを起動します。~/.cargo/binは、rgb-nodeのインストール後にcargoがすべてのバイナリをコピーしたディレクトリです。

```

$ rgbd -vvvv -b ~/.cargo/bin -d ./data0 -n testnet
$ rgbd -vvvv -b ~/.cargo/bin -d ./data1 -n testnet

```

## 発行

アセットを発行するには、発行可能なサブコマンドを使用してrgb0-cliを実行し、次に引数、USDTのティッカー、"USD Tether"の名前、および割り当てで、以下に示すように発行量とissuance_utxoを使用します。

```

$ rgb0-cli fungible issue USDT "USD Tether" 1000@4c1785210d8930959f530072cffea7f9606e0599b0de9e89aed60f2e9f133893:1

```

アセットが正常に発行されました。これらの情報を共有するために使用してください：
アセットの情報：

```

```
$ rgb0-cli fungible issue-blind \
    --network testnet \
    --asset-id rgb1tadqzve7vwfh39sl6gvqenp8wegsrzreekhhu0dhthx08ppzj9wq8p0je6 \
    --amount 1000 \
    --receiver-key 02e2e4f3e7e8e8e8e8e8e8e8e8e8e8e8e8e8e8e8e8e8e8e8e8e8e8e8e8e8e8e \
    --change-key 02e2e4f3e7e8e8e8e8e8e8e8e8e8e8e8e8e8e8e8e8e8e8e8e8e8e8e8e8e8e8e \
    --fee 1000 \
    --outpoint 4c1785210d8930959f530072cffea7f9606e0599b0de9e89aed60f2e9f133893:1 \
    --blinding-key 0000000000000000000000000000000000000000000000000000000000000001 \
    --change-asset-id rgb1tadqzve7vwfh39sl6gvqenp8wegsrzreekhhu0dhthx08ppzj9wq8p0je6 \
    --change-amount 0 \
    --change-asset-tag 0 \
    --change-asset-tag-mask 0
```

La commande ci-dessus génère une UTXO aveuglée avec les paramètres suivants:

- `--network testnet`: spécifie le réseau sur lequel l'opération est effectuée (testnet).
- `--asset-id rgb1tadqzve7vwfh39sl6gvqenp8wegsrzreekhhu0dhthx08ppzj9wq8p0je6`: spécifie l'ID de l'actif (USD Tether).
- `--amount 1000`: spécifie la quantité d'actif à émettre (1000 USDT).
- `--receiver-key 02e2e4f3e7e8e8e8e8e8e8e8e8e8e8e8e8e8e8e8e8e8e8e8e8e8e8e8e8e8e8e`: spécifie la clé publique du destinataire de l'actif.
- `--change-key 02e2e4f3e7e8e8e8e8e8e8e8e8e8e8e8e8e8e8e8e8e8e8e8e8e8e8e8e8e8e8e`: spécifie la clé publique pour le changement (si nécessaire).
- `--fee 1000`: spécifie les frais de transaction (1000 sats).
- `--outpoint 4c1785210d8930959f530072cffea7f9606e0599b0de9e89aed60f2e9f133893:1`: spécifie l'outpoint de l'UTXO à dépenser.
- `--blinding-key 0000000000000000000000000000000000000000000000000000000000000001`: spécifie la clé de masquage pour l'UTXO à dépenser.
- `--change-asset-id rgb1tadqzve7vwfh39sl6gvqenp8wegsrzreekhhu0dhthx08ppzj9wq8p0je6`: spécifie l'ID de l'actif pour le changement (USD Tether).
- `--change-amount 0`: spécifie la quantité d'actif pour le changement (0 USDT).
- `--change-asset-tag 0`: spécifie le tag d'actif pour le changement (0).
- `--change-asset-tag-mask 0`: spécifie le masque de tag d'actif pour le changement (0).

La commande renvoie le résultat suivant:

```
{
  "txid": "e4e7c6d2e2a5e3a7e3e4e7e8e8e8e8e8e8e8e8e8e8e8e8e8e8e8e8e8e8e8e8e",
  "vout": 0,
  "asset_id": "rgb1tadqzve7vwfh39sl6gvqenp8wegsrzreekhhu0dhthx08ppzj9wq8p0je6",
  "amount": 1000,
  "asset_tag": 0,
  "asset_blinding_factor": "0000000000000000000000000000000000000000000000000000000000000001",
  "asset_commitment": "0e0e0e0e0e0e0e0e0e0e0e0e0e0e0e0e0e0e0e0e0e0e0e0e0e0e0e0e0e0e0e",
  "value_blinding_factor": "0000000000000000000000000000000000000000000000000000000000000001",
  "value_commitment": "0e0e0e0e0e0e0e0e0e0e0e0e0e0e0e0e0e0e0e0e0e0e0e0e0e0e0e0e0e0e0e",
  "script_pub_key": "76a914e8e8e8e8e8e8e8e8e8e8e8e8e8e8e8e8e8e8e8e88ac",
  "blind_script_pub_key": "76a914e8e8e8e8e8e8e8e8e8e8e8e8e8e8e8e8e8e8e8e88ac",
  "range_proof": "000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000000
$ rgb1-cli fungible blind e40d9037e31d3f440552b30af16e764cf25ffda3899b4851cc4e38fd64718b09:0
アウトポイントのブラインド：utxob16az597vp5nkr66nfzsykf8ngdnvzep5050rm00l7vv8wm7vew4jqj7jhhf
アウトポイントのブラインドシークレット：1679197189805229975

このUTXOに関連するトランスファーを受け入れるためには、元のreceive_utxoとblinding_factorが必要です。

## トランスファー

rgb-node-1に資産の一定量を転送するためには、ブラインドされたUTXOに送金する必要があります。rgb-node-0は送信と開示を作成し、ビットコインのトランザクションで検証する必要があります。その後、コミットメントを含めるために変更する必要があるpsbtが必要です。さらに、-iオプションと-aオプションを使用して、資産の元の出力と返金される通貨の割り当てを指定する必要があります。指定方法は次のようになります：@<change_utxo>。

```

'$ rgb0-cli fungible transfer utxob16az597vp5nkr66nfzsykf8ngdnvzep5050rm00l7vv8wm7vew4jqj7jhhf 100 rgb1tadqzve7vwfh39sl6gvqenp8wegsrzreekhhu0dhthx08ppzj9wq8p0je6 tx.psbt consignment.rgb disclosure.rgb witness.psbt -i 4c1785210d8930959f530072cffea7f9606e0599b0de9e89aed60f2e9f133893:1 -a 900@cd66d3b77dfc1c2ecf958847c16a8a1311bba84ee7bf9dd55592a7b97b13028f:1
トランスファーが成功しました。送信と開示は "consignment.rgb" と "disclosure.rgb" に書き込まれ、部分的に署名されたウィットネストランザクションは "witness.psbt" にあります。
共有するための記録データ：consignment1qxz4g7ec6da33llaxe97u9hx8p9wcgp2yv46ycudwy7ytjf4gdh88x6upcdmjfy3mp4y0n669j5ar5y6e04zfr7255kynff6eymx9tdfc7jux5jk6tgn4xm6lttlh3lh08070ltuh60l07mamlns2qyy984mg4m5dz0x6s5sy5edls2zjlmnvw708sh7fy2vuph745jcpgp92qrw27s73vm4ghrx57vammyf8wautwu5euujd8w3dupdtgp4px36gz8z0ywnuty45uqdwk672qqzjp3j77yl7urft6gewqksqgppczezn5c7gyux6gzgpye0wgyjp85ufdqlzy5cd8zwfg3q9550xq2hyf24qqz92wqskpgq8qsr8kp5p9dt49evmqlze9ylrx2sqpwpvpqp45lpvgjkgk542pks9850w5jquq3qqsj4xsqn9nu6w30lgpmrhdqs6jj0ez3myhj74kp223f0wg2y7vupczdq5pa23mzhzc6l647nl6ftrru0mjrh739yhgztsdhl2cdmhf0qm7du9n20up4rnnsp0tlp8665xldkq9z9u85tgh6nxmkfg3pc6wzk2t90pekj2d6l0km09vyt4vut24vhzg9qhrdsgr7dws828p6ejk7ddy0zkz3a2fq5648664w3se2egwvh904lzmpnc7a7wy4fayznunt6j4ndmm68y24tjje4qxnxs70w4lr9vz9q9qca903edtjd6c5f37jagafsqnhnlsuwvnqwc7uly4dw2rnlyxp4zcfqrfpkpez54c0lc3tmvppmv06ge97heevgt0acrq0ezgjr6ck9waqpanypl8dzrqdzjd05h735tdgv2wjjjucheur40h4wjw4pcdpc8pqlh7ef95rj2al8v3eexkgty8j2ne7kk2zxpe0wypq8ra0x76rt6cu00cw4w05v0u3ng6zhfrttz2c3m5nx64s8w98wa26dx79jwhne44gp9lmg6vkhxq98meslyr4zqtxjsg27xzj80m0csd77lr047vwycvdw0z8mwudm3uvlry9p9da4su72k9q84pphw4n0fyeet0ujzrdgacm6p777jun0y0v397mp4drafr6q7994kdl96m388xp6ggf5arn4d4ed53rv9tlkerckqvkng92uhdvngwcl3m6yqhxdjjnkca62tckxfnrae4cx4e6wx6ww5649v4hvuwkkajanllc38wavqy83xhn555l708354nt2quscchexsxjgezdxfnmxgue0cn4ktghd6xd2le76k5cw3t0p0nurs4h5rjz0j7twj9ulwkp7cmhhgl23r7g677gk36r5jw8panh2sq5966m08sa5632egd5ms6h0e504dtwskct3x6a93uutaumtc8aam8yyt66lrmrhcssw9ga2yg0496s6sdmaexa49064g3syc888egnwa8racrwwwwemknqamarpqlmqa5mg8zgt0dts8ehuwmgz4j3cjltr8gv78e7p84zm8pylann7dmss5suf4htqc04qx5trnk59m305ah2qp4mvkxwy6ts84sa30d80jzk9s6n40e4j8dcvq79ncg5e3z5g4esxyawmxk7lvm5efc30vtw8qqhe9xx3773djez6hjjx0x962z2radnvdmazkrmlqw7guxz29qvahcx79h33ncqhzhvekwaqqnrz3wxnp2qy3u83zdgdcgq27n5n22h7jjedrh28m8c6mn42xhfjasm5njsxtufqjxefnhc2n5zr0um0xlqk62cu25cjwuwwrcv3e4vhh2tdzn8rnlaefj98fvslg7sun95wpt2a4vcg4ua62v97aeqstvjegmlem5crnsamrhm3a2pcma2s22atr43lgx9vh7kn9lzymfe83a4vhe9rc6xl5pmy5hjw4t88k0fwh6lzmjtjvqtczq47ny7hv8ytdqdy2c7ce3gegnufkzwphkwtz6xqzklyw7e7f76fwfewfuyqal7dl8r9476jerrl40mav38sun2u8jvftw33x3r20dmeka34znmkgaz29ppk5hz3ldttw8zyz4k6q0gts8utqh53tuc7vtajl26rq2fnxr0vxcwlx9rfvn6v8ar8c73qkc3zca4mlgl7qu36sk7e

```
これにより、consignment、disclosure、およびtweakを含むpsbtと呼ばれるウィットネストランザクションを含む3つの新しいファイルが作成されます。consignmentはrgb-node-1に送信されます。

## ウィットネストランザクション

ウィットネストランザクションは署名され、ブロードキャストされる必要があります。そのため、base64でエンコードする必要があります。

```

$ base64 -w0 witness.psbt

cHNidP8BAHECAAAAAe2pydT0BqfK5nBCdBSbm3W/vNKE/QxTr4eJcjwjDLDjAQAAAAD/////AiWbAAAAAAAAFgAUO1Bi4v2VHUJPmq5iyYhDv1tyTCcQJwAAAAAAABYAFPwfm3skdSeMnOfcDqBpgVjwuwESAAAAAAABAHECAAAAAeSwUiZ+p3/NM7yt3BAoDkm/afi//lplsffwwpTqjd+CAQAAAAD/////AlDDAAAAAAAAFgAULga5BeTQ1vfiqcD3zuxk+K2O/wbDwgAAAAAAABYAFLsvLLowx0NR5NyFKj9wl3IFvNcPAAAAAAEBH8PCAAAAAAAAFgAUuy8sujDHQ1Hk3IUqP3CXcgW81w8iBgKIYFEbYKvRj25inaA0/c0PMIZD/BFAgFbjrBJe8cZ+cxDskk+CAAAAgAEAAIADAACAACICAsnwAXsMVlPXi/2ExgqtLoIN4TncWVW0EImSo9YwyhNmEOyST4IAAACAAQAAgAUAAIAG/ANSR0IBIQLJ8AF7DFZT14v9hMYKrS6CDeE53FlVtBCJkqPWMMoTZgb8A1JHQgIgMD8j8bQGB8NgEobv3NUJr7aERA/FkGgQ5w2KwF+daDgAAA==

```

walletprocesspsbtのサブコマンドで署名してください。

```

$ bcli walletprocesspsbt "cHNidP8BAHECAAAAAe2pydT0BqfK5nBCdBSbm3W/vNKE/QxTr4eJcjwjDLDjAQAAAAD/////AiWbAAAAAAAAFgAUO1Bi4v2VHUJPmq5iyYhDv1tyTCcQJwAAAAAAABYAFPwfm3skdSeMnOfcDqBpgVjwuwESAAAAAAABAHECAAAAAeSwUiZ+p3/NM7yt3BAoDkm/afi//lplsffwwpTqjd+CAQAAAAD/////AlDDAAAAAAAAFgAULga5BeTQ1vfiqcD3zuxk+K2O/wbDwgAAAAAAABYAFLsvLLowx0NR5NyFKj9wl3IFvNcPAAAAAAEBH8PCAAAAAAAAFgAUuy8sujDHQ1Hk3IUqP3CXcgW81w8iBgKIYFEbYKvRj25inaA0/c0PMIZD/BFAgFbjrBJe8cZ+cxDskk+CAAAAgAEAAIADAACAACICAsnwAXsMVlPXi/2ExgqtLoIN4TncWVW0EImSo9YwyhNmEOyST4IAAACAAQAAgAUAAIAG/ANSR0IBIQLJ8AF7DFZT14v9hMYKrS6CDeE53FlVtBCJkqPWMMoTZgb8A1JHQgIgMD8j8bQGB8NgEobv3NUJr7aERA/FkGgQ5w2KwF+daDgAAA=="{'
'"psbt": "cHNidP8BAHECAAAAAe2pydT0BqfK5nBCdBSbm3W/vNKE/QxTr4eJcjwjDLDjAQAAAAD/////AiWbAAAAAAAAFgAUO1Bi4v2VHUJPmq5iyYhDv1tyTCcQJwAAAAAAABYAFPwfm3skdSeMnOfcDqBpgVjwuwESAAAAAAABAHECAAAAAeSwUiZ+p3/NM7yt3BAoDkm/afi//lplsffwwpTqjd+CAQAAAAD/////AlDDAAAAAAAAFgAULga5BeTQ1vfiqcD3zuxk+K2O/wbDwgAAAAAAABYAFLsvLLowx0NR5NyFKj9wl3IFvNcPAAAAAAEBH8PCAAAAAAAAFgAUuy8sujDHQ1Hk3IUqP3CXcgW81w8BCGsCRzBEAiAZud+YVf1FyZq0IDQ+/oAE34TKypedrJGUcYx0QIpaygIgZJO7xvN0dOQXbXTRYE0QxGIWsfo85Dhwne0/whoO06kBIQKIYFEbYKvRj25inaA0/c0PMIZD/BFAgFbjrBJe8cZ+cwAiAgLJ8AF7DFZT14v9hMYKrS6CDeE53FlVtBCJkqPWMMoTZhDskk+CAAAAgAEAAIAFAACABvwDUkdCASECyfABewxWU9eL/YTGCq0ugg3hOdxZVbQQiZKj1jDKE2YG/ANSR0ICIDA/I/G0BgfDYBKG79zVCa+2hEQPxZBoEOcNisBfnWg4AAA=", "complete": true}

````

最後に、それを完成させて16進数を取得します。
## Diffusez-le

元のテキスト:
Diffusez-le en utilisant la sous-commande sendrawtransaction pour le faire confirmer dans la blockchain.

翻訳:
ブロックチェーンで確認するために、sendrawtransactionサブコマンドを使用してそれを送信してください。
$ bcli sendrawtransaction "02000000000101eda9c9d4f406a7cae6704274149b9b75bfbcd284fd0c53af8789723c230cb0e30100000000ffffffff02259b0000000000001600143b5062e2fd951d424f9aae62c98843bf5b724c271027000000000000160014fc1f9b7b2475278c9ce7dc0ea0698158f0bb011202473044022019b9df9855fd45c99ab420343efe8004df84caca979dac9194718c74408a5aca02206493bbc6f37474e4176d74d1604d10c46216b1fa3ce438709ded3fc21a0ed3a90121028860511b60abd18f6e629da034fdcd0f308643fc11408056e3ac125ef1c67e7300000000"8e3787fe40b5feb3044f892e739bdb4043e10de384255a915a37725811abc3fe```

## 受け入れる

入金を受け入れるためには、rgb-node-1はrgb-node-0からのconsignmentファイルを受け取り、ブラインディングUTXOの生成時に生成されたreceive_utxoと対応するblinding_factorを持っている必要があります。

````

$ rgb1-cli fungible accept consignment.rgb e40d9037e31d3f440552b30af16e764cf25ffda3899b4851cc4e38fd64718b09:0 1679197189805229975

アセットの転送が正常に受け入れられました。

```

次に、以下のコマンドを実行して、<receive_utxo>内の100単位の新しいアセットの割り当てを（knownAllocationsフィールドで）確認できます。

```

$ rgb1-cli fungible list -l

- genesis: genesis1qyfe883hey6jrgj2xvk5g3dfmfqfzm7a4wez4pd2krf7ltsxffd6u6nrvjvvnc8vt9llmp7663pgututl9heuwaudet72ay9j6thc6cetuvhxvsqqya5xjt2w9y4u6sfkuszwwctnrpug5yjxnthmr3mydg05rdrpspcxysnqvvqpfvag2w8jxzzsz9pf8pjfwf0xvln5z7w93yjln3gcnyxsa04jsf2p8vu4sxgppfv0j9qerppqxhvztpqscnjsxvq5gdfy5v6j3wvpjxxqzcerxuglngnfvpxjkgqusct7cyx8zzezcfpqv3nxjxm2kjj4d0zu0ta6fjmpr8a0calk6h88h4ap5e4nucj0ch07aa73qsh3lj5sd89a32kwy0eq7tsa5zqqjpdqvqq5s46r0
  id: rgb1tadqzve7vwfh39sl6gvqenp8wegsrzreekhhu0dhthx08ppzj9wq8p0je6 ticker: USDT'
  name: USD Tether
  description: ~
  knownCirculating: 1000
  isIssuedKnown: ~
  issueLimit: 0
  chain: テストネット
  decimalPrecision: 0
  date: "2022-02-23T20:53:26"
  knownIssues:
- id: 5c912284f3cc5db73d7eafcd798801517627cc0c18d21f967893633e33015a5f
  amount: 1000
  origin: ~
  knownInflation: {}
  knownAllocations:
- nodeId: 5c912284f3cc5db73d7eafcd798801517627cc0c18d21f967893633e33015a5f
  index: 0
  outpoint: "4c1785210d8930959f530072cffea7f9606e0599b0de9e89aed60f2e9f133893:1"
  revealedAmount:
  value: 1000
  blinding: "0000000000000000000000000000000000000000000000000000000000000001"
- nodeId: 28f82e2dcfa91282c28a8805ff0c7fde4bd4e0bdbd40c6ba55e191666e45327b
  index: 1
  outpoint: "e40d9037e31d3f440552b30af16e764cf25ffda3899b4851cc4e38fd64718b09:0"
  revealedAmount:
  value: 100
  blinding: 224561f10229eb9ebbdf05f497132d2b8344d70971c80510eddc607d615ee2a0

受信した UTXO は送金時にブラインドされたため、支払い者である rgb-node-0 には 100 USDT が送信された場所に関する情報がないため、knownAllocations には表示されません。

$ rgb0-cli fungible list -l

- genesis: genesis1qyfe883hey6jrgj2xvk5g3dfmfqfzm7a4wez4pd2krf7ltsxffd6u6nrvjvvnc8vt9llmp7663pgututl9heuwaudet72ay9j6thc6cetuvhxvsqqya5xjt2w9y4u6sfkuszwwctnrpug5yjxnthmr3mydg05rdrpspcxysnqvvqpfvag2w8jxzzsz9pf8pjfwf0xvln5z7w93yjln3gcnyxsa04jsf2p8vu4sxgppfv0j9qerppqxhvztpqscnjsxvq5gdfy5v6j3wvpjxxqzcerxuglngnfvpxjkgqusct7cyx8zzezcfpqv3nxjxm2kjj4d0zu0ta6fjmpr8a0calk6h88h4ap5e4nucj0ch07aa73qsh3lj5sd89a32kwy0eq7tsa5zqqjpdqvqq5s46r0
  id: rgb1tadqzve7vwfh39sl6gvqenp8wegsrzreekhhu0dhthx08ppzj9wq8p0je6
  ticker: USDT
  name: USD Tether
  description: ~
  knownCirculating: 1000
  isIssuedKnown: ~
  issueLimit: 0
  chain: testnet
  decimalPrecision: 0
  date: "2022-02-23T20:53:26"
  knownIssues:
  - id: 5c912284f3cc5db73d7eafcd798801517627cc0c18d21f967893633e33015a5f
    amount: 1000
    origin: ~
    knownInflation: {}
    knownAllocations:
  - nodeId: 5c912284f3cc5db73d7eafcd798801517627cc0c18d21f967893633e33015a5f
    index: 0
    outpoint: "4c1785210d8930959f530072cffea7f9606e0599b0de9e89aed60f2e9f133893:1"
    revealedAmount:
    value: 1000
    blinding: "0000000000000000000000000000000000000000000000000000000000000001"

```

しかし、rgb-node-0は、-a引数を使用して転送コマンドに提供した900の資産の変更を見ることができません。変更を記録するには、rgb-node-0は開示を受け入れる必要があります。

```

$ rgb0-cli fungible enclose disclosure.rgb

開示データが正常に含まれました。

```

rgb-node-0が成功した場合、資産をリストすることで変更を確認できます。

```

$ rgb0-cli fungible list -l

- genesis: genesis1qyfe883hey6jrgj2xvk5g3dfmfqfzm7a4wez4pd2krf7ltsxffd6u6nrvjvvnc8vt9llmp7663pgututl9heuwaudet72ay9j6thc6cetuvhxvsqqya5xjt2w9y4u6sfkuszwwctnrpug5yjxnthmr3mydg05rdrpspcxysnqvvqpfvag2w8jxzzsz9pf8pjfwf0xvln5z7w93yjln3gcnyxsa04jsf2p8vu4sxgppfv0j9qerppqxhvztpqscnjsxvq5gdfy5v6j3wvpjxxqzcerxuglngnfvpxjkgqusct7cyx8zzezcfpqv3nxjxm2kjj4d0zu0ta6fjmpr8a0calk6h88h4ap5e4nucj0ch07aa73qsh3lj5sd89a32kwy0eq7tsa5zqqjpdqvqq5s46r0
  id: rgb1tadqzve7vwfh39sl6gvqenp8wegsrzreekhhu0dhthx08ppzj9wq8p0je6
  ticker: USDT
  name: USD Tether
  description: 〜
  knownCirculating: 1000
  isIssuedKnown: 〜
  issueLimit: 0
  chain: テストネット
  decimalPrecision: 0
  date: "2022-02-23T20:53:26"
  knownIssues:
  - id: 5c912284f3cc5db73d7eafcd798801517627cc0c18d21f967893633e33015a5f
    amount: 1000
    origin: 〜
    knownInflation: {}
    knownAllocations:
  - nodeId: 5c912284f3cc5db73d7eafcd798801517627cc0c18d21f967893633e33015a5f
    index: 0
    outpoint: "4c1785210d8930959f530072cffea7f9606e0599b0de9e89aed60f2e9f133893:1"
    revealedAmount:
    value: 1000
    blinding: "0000000000000000000000000000000000000000000000000000000000000001"
  - nodeId: 28f82e2dcfa91282c28a8805ff0c7fde4bd4e0bdbd40c6ba55e191666e45327b
    index: 0
    outpoint: "cd66d3b77dfc1c2ecf958847c16a8a1311bba84ee7bf9dd55592a7b97b13028f:1"
    revealedAmount:
    value: 900
    blinding: ddba9e0efdd614614420fa0b68ecd2d3376a05dd3d809b2ad1f5fe0f6ed75ea2

## 結論

私たちは、交換可能な資産を作成し、プライバシーを保護しながらトランザクションから別のトランザクションに移動することができました。ブロックエクスプローラで確認されたトランザクションをチェックすると、通常のトランザクションとは何も変わらないことがわかります。これは、RGB がトランザクションを調整するために一度限りのシールを使用しているためです。この記事では、RGB の動作方法について紹介しました。

この記事にはバグが含まれている可能性があります。もし見つけた場合は、改善のためにお知らせください。提案や批判も歓迎です。ハッキングを楽しんでください！ 🖖

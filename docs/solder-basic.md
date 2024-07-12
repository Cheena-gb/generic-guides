# ハンダ作業 基礎ガイド
ハンダ作業は概ね、以下の手順を踏むことにより完了できます。

## ハンダ作業とは
低融点合金「ハンダ」を溶融させ、別種の金属に付着させて物理的・電気的に接合する作業です。  

## 作業に必要なもの

### 工具類
- ハンダゴテ  
  ハンダを溶融させるために使用するコテの一種です。  
  250℃～450℃程度まで、コテ毎に設定できる温度が異なります。  
  電子部品のハンダづけでは、270℃～300℃に設定することが多くなっており、これ以上の温度では作業速度を向上させますが、電子部品が過熱しやすくなり、破損にも繋がります。

- コテ台  
  作業中のハンダゴテを置くための台です。  
  コテ先を清掃するためのワイヤーやスポンジが配置されているものもあり、ワイヤーは加熱したコテ先を突っ込んで、スポンジは水で濡らしてコテ先を押し付けることで、過剰なハンダを落とします。

- ハンダ回収機  
  溶融したハンダを回収するポンプです。  
  減圧して吸気することによりハンダを回収するようになっており、ハンダの量が多すぎた場合に吸い上げることで作業をやり直します。

- ハンダ付けマット  
  シリコンゴムのマットです。
  耐熱性があり、机の焦げやハンダの落下を防止します。トレイが付いているものもあり、パーツ置き場としても機能します。

- ニッパー  
  ワイヤーやリード線を切断するための工具です。
  大きなものを使用する必要はありませんが、金属用を使用しないと刃が欠けたり、折れることがあります。
  ばね付き、キャッチングタイプ、等、複数種類があるため、好みのものを見つけましょう。

- ピンセット  
  細かいパーツをつかむ工具です。  
  特に表面実装部品では指で押さえることが不可能なため、必須の工具です。  
  先端の形状、逆作用型、等、複数種類があります。また、静電気対策を施したESDピンセットや絶縁ピンセットがあります。好みのものを見つけましょう。
  
### 消耗品類
- ハンダ  
  錫と鉛をそれぞれ63%、37%の比率で混合した低融点合金であり、融点は190℃程度となっています。
  流動性を高めるためにフラックスを混合しており、溶融した状態では、周囲の加熱された金属の表面を濡らして浸透するようになります。
  - 鉛フリーハンダ  
    鉛を使用しない低融点合金で作成したハンダです。融点が高く、流動性が低く、高価ですが、大量に使用する場合やRoHS指令への対応が必要な場合に使用します。
  - 銀入りハンダ  
    特に銀を多く混合したハンダです。銀メッキを行った部材にハンダづけを行う場合、ハンダ側への銀の流入を抑えます。
  - ヤニ無しハンダ  
    通常は電気電子工作用ではなく、板金作業に使用します。
  
  オーディオ用、表面実装用などといった区分は、基本的にハンダの径によって決定されているため、どれだけの長さを溶かすとどれだけ流れ込むかが変わります。  
  組成が同じであれば、概ね同じように扱うことができます。

- ブローケース  
  少量売りされるハンダは、プラスチックのケースに入って売られています。このケースをブローケースと呼び、ハンダの保存や作業時の持ち手として使用します。
  リール巻きのハンダや、紙ケースに入れたままの状態では持ちづらいため、ケースに入れることで火傷を予防します。

- ハンダペースト
  粉末状のハンダとフラックスを混合したペースト状のハンダです。  
  ハンダゴテを用いた作業ではなく、リワークステーションやリフロー炉を使用したハンダづけで使用します。

- フラックス  
  ハンダや被ハンダ金属の酸化被膜を除去し、ハンダが浸透できるようにする機能を持ちます。
  - 主剤  
    松脂や合成樹脂から成ります。酸化被膜を除去し、ハンダ後の表面を保護します。
  - 活性剤  
    ハロゲン化合物[^1]から成ります。主剤の作用を強化します。
    [^1]:塩素やヨウ素などの17族元素と、金属原子などの化合したもの。フラックスを加熱した時の煙の成分。
  - 溶媒  
    アルコールや水から成ります。主剤と活性剤を溶かしておき、塗布できるようにします。

- ハンダ回収線  
  銅線を綾織りしたリボンにフラックスを染み込ませたものです。  
  過剰なハンダの上に乗せ、ハンダゴテで押さえつけることで回収線にハンダが流れ込み、ハンダを回収することができます。  
  一度使用した部分は再利用できないため、ニッパーなどで切断します。

- フラックスリムーバー  
  基板表面の美観維持などの目的でフラックスを除去したい場合、液状あるいはスプレーのフラックスリムーバーを使用することで洗浄できます。
  有機溶剤であれば大抵のものが使用できますが、基板表面やパーツを侵食する可能性があるためお勧めはしません。

- コテ先  
  ハンダゴテのコテ先は、使ううちにハンダに侵食されて溶けていきます。また、酸化被膜を除去するために研磨を行うことでも消耗します。  
  適切なタイミングでコテ先を交換することで、安定した作業性を維持することができます。  
  形状には複数種類があり、初期から装着されている円錐形のB型が一般的です。  
  先端が角錐となったA型、円錐の先端を斜めに切断したC型やBC型、先端を平たくしたD型など複数の種類があります。
  とはいえ、ものすごい勢いで減るというものではないため、常備する必要はありません。

## 実作業

### 適切なハンダ
ハンダ作業には適切な作業時間、適切なハンダ量があります。  
部品へのダメージを考えると熱を与える時間は短い方が良いですが、錫と銅の合金層を形成するためには250℃以上を約3秒間維持する必要があります。  
また、ハンダ量は少なすぎても多すぎても十分な強度が出ず、かつ見た目も美しくなくなってしまいます。  
理想とされるハンダづけは、リード部品であれば、凝固したハンダは富士山型のフィレットとなり、表面にはつやがあり、周囲にフラックスが飛ぶこともなく、変色もない状態になります。  
パッド[^2]に対してハンダが多すぎると、球状に丸まるようになり、割れやすく、基板破損の原因になります。  

[^2]:基板側の、ハンダ作業を行うために金属面が露出した部分。大抵の場合、工場でハンダを塗っている(HASL/ENIG)ため、つやのある銀色か金色をしている。

加熱が長すぎたり、温度が高すぎると、温度の上がりすぎたハンダはツヤを失い、流動性が下がってコテに引かれるようになります。このまま作業を行うとツノが立った状態になり、後の破損や怪我の原因になります。  
加熱が短すぎたり、温度が低すぎると、フラックスが活性化せず、ハンダはの流動性が下がったままになります。ダマのようになった状態で凹凸のあるはんだ面が形成されます。  
  
理想的な作業サイクルを考えると、以下のような順序が考えられるでしょう。
- 予熱  
  パッド部とリードを加熱する。
- はんだ供給 2秒  
  パッドとリードがなめらかな曲線で接合されるように、十分な量のハンダを流し込む。
- 加熱 1秒程度  
  ハンダが馴染むまで待つ。理想的な量と温度であれば、リードを回り込むようにハンダが流れる。馴染んだと判断できたら、すぐにコテ先を離す。
- 冷却 5秒以上  
  
すぐに冷えてしまうとはいえ、コテを離した後も余熱で合金の形成は進むため、加熱を3秒行わなくては**ならない**というわけでは**ない**ことに注意しましょう。

### リード部品・ピン
金属の細線であるリード、太めの棒であるピンを持った部品は、それぞれの実装面から部品を通し、裏返してハンダづけすることになります。  
それぞれのスルーホールにリードやピンを通し、マスキングテープ等で仮止めして裏返します。  
露出したピンにコテ先を当て、十分に加熱したらハンダを流します。  

フィレットが形成されたらハンダを離し、その後コテを離します。

### 表面実装部品
表面実装部品は、パッド上に先にハンダを乗せておくことで固定します。これを予備ハンダと呼びます。  
予備ハンダの量は多い必要はなく、少し膨れる程度でも問題ありません。  
予備ハンダを溶融させたところに部品の金属足を接触させ、表面張力で吸着させます。  
残りの足も順次ハンダづけを行い、最後に、予備ハンダを行った足にもハンダを追加します。  
この時、予備ハンダのフラックスが飛んでしまっている場合があります。フラックスを塗って足しましょう。

### ワイヤー
銅線などのワイヤーは、細い線が複数より上げられた撚線がほとんどです。  
これらをハンダづけする必要がある場合、ワイヤー側の露出した線をハンダでメッキするハンダ上げを行います。  
この状態で予備ハンダを行ったパッドや部品に当てて加熱することで、ハンダが溶け、接合されるようになります。

## チート
はんだ作業には裏技が存在します。適切な作業ではなく、基板やハンダゴテの寿命を縮めるものも多いため、推奨はしませんが、可能です。

### コテ先のはんだ濡れ性を高める
ハンダゴテを高めの温度に加熱し、フラックスの液に一瞬突っ込んですぐに引き上げます。  
表面の酸化被膜が剥がれ、ハンダが溶けやすくなりますが、コテ先に微細なヒビが入り侵食されやすくなります。

### ハンダ回収線の強化
ハンダ回収線をフラックスに漬けてから使用します。  
ハンダが大量に回収されますが、フラックスによる基板の汚れは極めて多くなります。

### ハンダ回収をハンダで行う
部品の足をすべて覆う量のハンダを溶かし、部品全体を包み込むようにした状態で加熱を続けることで部品の解除を行います。  
基板が汚れることや、ハンダを大量に使うこと、周囲への熱の影響が大きいこと、さらに解除した部品の再利用はほぼ不可能であるため、どうしても取れない部品を解除する最終手段になります。  
スルーホールに残ったはんだは溶かしながら一気に息を吹き込むと吹き飛ぶことがあります。火傷には注意してください。
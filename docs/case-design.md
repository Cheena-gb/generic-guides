# サンドイッチケース設計ガイド
キーボードのケースは、キーボードの寿命を左右し、美観に大いに影響し、可搬性を決定し、打鍵感を左右するキーボードの重要部材です。  
最小構成たるサンドイッチマウントですら、考慮すべき要素は無数にあります。  
以下の設計ガイドは、その全てを網羅してはいないかもしれませんが、気にされづらい要素を拾いあげる助けにはなるでしょう。

## 設計
サンドイッチケースとは、基板をスイッチプレート、バックパネルの2枚で挟み、ねじ止めする形のケースです。  
自作キーボードでは最も安価なマウント方式とされ、打鍵感に優れているわけでもありませんが、設計の良し悪しが出づらいものでもあります。  

## スイッチプレート
一般的なケースと同様に、スイッチの位置に穴を開けたプレートを用意します。

## スイッチプレートと基板の接続
スイッチプレートの外側面から基板表面までの距離は5mm[^1]あり、スイッチプレートが2mm[^2]であれば3mm、1.5mm[^3]であれば3.5mmの空隙を設ける必要があります。  
[^1]:MXスイッチ互換品の場合
[^2]:アクリル板など
[^3]:FR-4、ABS板、金属板など
この空隙を生み出す方法は複数あり、概ね以下の手段が採られています。

<details><summary>スペーサー(短)</summary>
  
  スイッチプレートと基板の間に3.5mm、あるいは3mmのスペーサーを導入することで固定する方式です。  
  
  後述のスペーサー(長)を導入するよりも硬めの打鍵感になりますが、スイッチを全て引き抜いても基板が脱落しない・基板が押し込まれてもスイッチが抜けない利点があります。　　

  また、プッシュスイッチ付きロータリーエンコーダーを使用する際は、こちらの構成にすることで安定した押し込みが可能になります。
</details>

<details><summary>スペーサー(長)</summary>
  
  基板にスペーサーを通せる穴を開けておき、ねじ止めを直接行うのはスイッチプレートとバックパネルのみにする方式です。  
  
  最も安価に済みますが、スイッチを全て引き抜くと基板が脱落します。また、打鍵感がスイッチプレートの素材に依存します。  
  
  将来的に、MX互換のロープロファイルスイッチが登場した場合、こちらの方式だと簡単なロープロファイル化が可能になります。
</details>

<details><summary>ミドルプレート</summary>
  
  ミドルアクリルなどと呼ばれる方式です。  
  
  スイッチが通ることのできる通し穴を開けたプレートをスイッチプレートと基板の間に挟むため、アクリルなどでは透明感のある見た目になります。  
    
  剛性が高くなるため、打鍵感も硬くなります。
</details>

## 基板
サンドイッチケースを前提とした設計を行う場合、接続端子が基板の辺から外を向くように配置します。  
スイッチプレートとバックパネルと基板、すべて同じ位置にねじが貫通するように穴を開けるのが一般的で、基板上下でスペーサーを別に使用するか、1本のスペーサーで基板を貫通する形にするかは好みが分かれる部分です。  
3.5mmと2mmのスペーサーを使用するなど、上下で分割する場合は打鍵感が硬めになり、スイッチを全て引き抜いても基板が脱落しない利点がありますが、設計上の工夫が必要になります。  
1本のスペーサーを貫通させると、スペーサーに掛かる金額が単純に半分になる一方、打鍵感は全てスイッチプレートに依存し、剛性も少し劣ります。  
見落としがちですが、M3のスペーサーは通常キーの隙間には導入できません。1.25uと1uの間に詰め込むなど、設計時には注意が必要になります。

## 基板とバックパネルの接続
基板とバックパネルの間は、設計によりクリアランスが異なります。  
スイッチソケットを使用している場合はソケットの全高が1.85mmとなるため、クリアランスは2mmほどあればよく、スイッチをすべてはんだ付けする前提の設計では、スイッチの脚を切断することでクリアランスは1.6mmにまで抑えられます。  
MCUの交換を可能するピンソケット・ピンヘッダ、コンスルーなどを使用している場合はバックパネルを階段状にしておき、階段下の空間にパーツを納めるのが一般的ですが、こちらは今は割愛します。
<details><summary>スペーサー(短)・ナット</summary>
  
  基板とバックパネルの間に1.5mm、あるいは2mmのスペーサーを導入することで固定する方式です。ナットを使用する場合もあります。  
    
  この設計を敢えて採用する場合、ネジはスイッチプレートからバックパネルまでを貫通する長さのものにします[^4]。  
  [^4]:[ケース設計時の留意点](https://github.com/Cheena-gb/generic-guides/blob/main/docs/case-tips.md)参照  

  または、市販は少ないですが、3mmと7mmのネジで上下から挟む必要があります。  

  ナットは、M2を使用する場合は1種、2種を使用すると、1.6mmの厚みが得られます。M3ナットの場合、3種を使用すると、1.8mmの厚みになっています。

</details>

<details><summary>スペーサー(長)</summary>
  
  基板にスペーサーを通せる穴を開けておき、ねじ止めを直接行うのはスイッチプレートとバックパネルのみにする方式です。  

  スイッチプレートで説明したものと同様の手段です。

</details>

<details><summary>ミドルプレート</summary>
  
  ミドルボトムプレートなどと呼ばれる方式です。  
  ソケットやスイッチの脚、ダイオード、LEDなどすべてのパーツが通る穴を開けたプレートを用意し、基板の裏に重ねます。  
  
  加工に非常に時間がかかるため、高級なキーボードで使用されることが多くなっている一方、アンダーグローを綺麗に光らせられるという利点があります。  
  
</details>

## バックパネル
通常はスイッチプレートと同等のサイズの物を用意し、同じようにねじ止めできるようにしてあります。  
場合により、MCUのリセット/ブートスイッチを押すための穴であったり、ゴム足を接着する位置を示す標識などを追加しておきます。  


## パーツの選定

### ねじ・スペーサー・ナット
ねじの規格については割愛します。余程安いものでなければ(日本で一般的に店売りされているものであれば)特段気にせず使用することができます。  
  
通常、自作キーボードにおいて使用するねじはM2またはM3が一般的です。  
それぞれ以下のような特徴があります。  
- M2
  - ねじ通し穴の半径は1.1mm。
  - スペーサーが細く(円形…直径4mm、六角形…対辺4mmまたは3mm)、キーの隙間に配することでスペースの削減や小型化に貢献する。
  - 円形スペーサーの半径が1/8U=2.3813mmに近いため、基板の角に配置した際には半径1/8uの面取りと馴染む曲線を描かせることができる。
  - M3よりも背の低いスペーサーの市販が多く、ネジ付き2mmスペーサーなどといった部材も入手可能。
  - 規格品ナット(1種、2種)が一般的な基板厚さである1.6mm厚となっており、基板1枚分のスペーサーとして使用可能。
  - 3種ナットは1.2mm厚であり、こちらも薄い基板と同様のスペーサーとして使用できる。
  - ただし、高価。
- M3
  - ねじ通し穴の半径は1.6mm。 
  - M2と比較すると入手性がよく安価であり、また堅牢なため、壊れづらく扱いやすい。
  - キーの隙間に配置することが難しいため、基板を大型化するか、1.25u以上のキーを並べた隙間に導入するなどの工夫が必要。
  - あまり背の低いスペーサーは販売されていないことがあり、アクリルを円形に切って使うなどの工夫が必要になる。

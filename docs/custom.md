# キーボードの改造について
キーボードの改造は自己責任で行ってください。

## 音響改造
### サイレンサーパッド
スイッチプレートとスイッチの間に貼るパッド、スイッチと基板の間に貼るパッド、スタビライザーと基板の間に貼るパッド…など複数の種類があります。  
それぞれのパーツの衝突を抑えるため、打鍵間は柔らかく、音は少し小さくなります。
### フォーム追加
スイッチプレートと基板の間、基板とバックパネルの間をフォームで埋め立てます。  
ケース内での音の反響を抑えることが期待できます。  

### ルブ
打鍵感の向上が主目的のスイッチルブ・スタビライザールブですが、スプリング鳴りを抑える、スレ音を抑えるなどの要因で雑音を減らすことができます。  
通常高粘度のグリスが静音性にも優れている傾向ですが、好みで調整してください。  
つけすぎると粘性抵抗で押し込みが重くなります。

### ウエイト追加
重量のある金属板(鉛板など)をケース内に貼り付けることで重量を増し、打鍵音を低くすることができます。  

## LEDバー・LEDテープを追加して光らせる
GPIOの空きが1つと、3.3V～5C程度のVCCとGNDがあればLEDを増設できます。  
ファームウェアにライティングに関する記述を追加し、LED_PINに指定したGPIOにLEDのDINを接続します。  
VCCはマイコンの駆動電圧により決定し、ATMega32U4であれば5V駆動のため5V(RAW)とVCCを直結、RP2040であれば3.3V駆動のため5V(RAW)からダイオードを1つ挟むことで電圧を落とします。  
本来の基板と追加部分がショートしないように、カプトンテープ等で金属部分を保護して使用しましょう。
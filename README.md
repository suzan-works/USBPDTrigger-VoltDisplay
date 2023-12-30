# 電圧表示付き USB PD トリガー
 WCH CH32X035 マイコンを使用して、Vbus電圧をSSD1306 OLEDモジュールに表示する、USB PDトリガーデバイスです。  
 ![使用例](使用例.png)

# 操作手順
1. USB-CコネクタにUSB PD電源を接続します。
1. 電圧切替スイッチで出力電圧を変更します。(5→9→12→15→20Vのループ)
1. OLEDディスプレイで希望の電圧が出ていることを確認します。
1. 出力入切スイッチを押すと基板右端のヘッダピンから出力されます。  

![操作手順](操作手順.png)

# 注意
- 出力電圧はUSB電源(USB PD Source)の仕様に依存します。設定電圧とVbus電圧が乖離する場合があります。
- 表示されるVbus電圧は目安で、測定器としての精度を保証するものではありません。
- 出力電流は1A程度を想定して設計しています。
- このデバイスの使用における損害は一切保証いたしません。自己責任でご使用ください。

# マイコン開発
Arduino IDEでのファームウェア変更が可能です。  
WCH LinkEエミュレーターでPCに接続して、「ボードマネージャ」＞「CH32V EVT Boards Support」＞「CH32X035」を選択します。  
参考情報  
https://github.com/openwch/arduino_core_ch32  
https://youtu.be/PSXAfMaWH_A?si=gFLTGL1ydqfZDPP8  

# 設計資料 v1.0
- 回路図 [PDF](回路図.pdf)
- プリント基板
![プリント基板](プリント基板.jpg)
- ファームウェア [inoファイル](USBPDTrigger-VoltDisplay.ino)
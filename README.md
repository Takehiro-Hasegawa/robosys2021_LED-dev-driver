# robosys2021_LED-dev-driver
ロボットシステム学、課題１のLEDを点灯させるデバイスドライバ
# 実装について
下記に実装した内容を説明する
- 実装内容
  - 0~4までの数字をデバイスファイルに書き込むことにより各機能を有効化する
  - 0 : GPIO25に接続されているLEDの消灯
  - 1 : GPIO25に接続されているLEDの点灯
  - 2 : GPIO15に接続されているLEDの消灯
  - 3 : GPIO15に接続されているLEDの点灯
  - 4 : 踏切に模したLED2つの点滅　dmesgを確認すると最初に"The train will pass soon"が表示、最後に"The train has passed"が表示される
# 回路図
![robosys1circit_回路図](https://user-images.githubusercontent.com/39427883/148928572-411a3c62-ca13-4966-b731-75d8fe7f94cb.png)
# 実験装置
![IMG_1411](https://user-images.githubusercontent.com/39427883/148931319-423bfe1c-f42d-47dd-ad72-e175e591f46a.jpeg)

- RaspberryPi4B
- 2×200Ω
- 2×赤色LED
- 4×ジャンパーケーブル

# 動画URL
https://youtu.be/QFZw0eesHTw
# 実行
- インストールから起動

`git clone https://github.com/Takehiro-Hasegawa/robosys2021_LED-dev-driver.git`
`cd robosys2021_LED-dev-driver`
`make`
`sudo insmod myled.ko`
`sudo chmod 666 /dev/myled0`
- GPIO25 LEDの消灯
 
 `echo > 0 /dev/myled0`
- GPIO25 LEDの点灯

 `echo > 1 /dev/myled0`
 - GPIO15 LEDの消灯
 
 `echo > 2 /dev/myled0`
 - GPIO15 LEDの消灯
 
 `echo > 3 /dev/myled0`
 - 踏切を模したLEDの点滅
 
 `echo > 4 /dev/myled0`
 - The train will pass soon The train has passedの確認
 `dmesg`
- 停止

`sudo rmmod myled`

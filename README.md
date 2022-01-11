# robosys2021_LED-dev-driver
ロボットシステム学、課題１のLEDを点灯させるデバイスドライバ
# 実装について
下記に実装した内容を説明する。
- 実装内容
  - 0~4までの数字をデバイスファイルに書き込むことにより各機能を有効化する
  - 0 : GPIO25に接続されているLEDの消灯
  - 1 : GPIO25に接続されているLEDの点灯
  - 2 : GPIO15に接続されているLEDの消灯
  - 3 : GPIO15に接続されているLEDの点灯
  - 4 : 踏切に模したLED2つの点滅　dmesgを確認すると最初に"The train will pass soon"が表示、最後に"The train has passed"が表示される

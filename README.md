# ロボットシステム学　課題１
2021年ロボットシステム学の講義で作成したデバイスドライバーをベースに、作成・改造したものです。

コマンドを入力することによって4色のLEDが点灯、消灯します。

4色のLEDを使いイルミネーションをイメージして作成しました。

下に実行した様子を撮った動画のURLを載せているので是非見てください。

# 動作環境
今回は以下の環境で動作を行いました。

〇Raspberry Pi 3 Model B

〇Os:ubuntu 20.04 server

# 利用したもの
今回は以下のものを利用しました。

全て秋葉原で購入しました。

| 利用したもの | 個数 |
| ---------------------- | ---------------------- |
| Raspberry Pi 3 Model B | 1 |
| ブレッドボード | 1 |
| LED | 4(オレンジ、赤、緑、青) |
| 抵抗(220Ω) | 4 |
| ジャンパーコード | 8 |

# 完成画像
![image](https://user-images.githubusercontent.com/91820973/146629629-aa90adab-960d-49d6-8ed7-4aa1f63edbe3.png)

# PIN情報
![image](https://user-images.githubusercontent.com/91820973/146629640-0f4a0d5a-3060-4881-be11-9f2d75959726.png)

*Fritzingを利用して作成しました。

# 回路図
![image](https://user-images.githubusercontent.com/91820973/146629649-078ac357-799c-4a65-8af1-1d0529fea510.png)

*Fritzingを利用して作成しました。

# インストール
以下の手順に従って入力してください。

① $ git clone git@github.com:itsukiueno/kadai1.git

② $ cd myled/

③ $ make

④ $ sudo insmod myled.ko

⑤ $ sudo chmod 666 /dev/myled0

以上でインストールは完了です。

# 実行
以下のコマンドの数字を変えて入力することで様々なパターンで実行することができます。

是非実行してみてください。部屋の電気を消して暗くすることでより綺麗にLEDが光って見えるので試してみてください。

| コマンド | 内容 |
| -------- | ------- |
| $ echo 0 > /dev/myled0 | 点灯している全てのLEDを消灯させます。 |
| $ echo 1 > /dev/myled0 | LED1(オレンジ色)が点灯します。 |
| $ echo 2 > /dev/myled0 | LED2(赤色)が点灯します。 |
| $ echo 3 > /dev/myled0 | LED3(緑色)が点灯します。 |
| $ echo 4 > /dev/myled0 | LED4(青色)が点灯します。 |
| $ echo 5 > /dev/myled0 | 全てのLEDが点灯します。 |
| $ echo 6 > /dev/myled0 | 2色(オレンジ色・緑色)のLEDが点灯します。 |
| $ echo 7 > /dev/myled0 | 2色(赤色・青色)のLEDが点灯します。 |


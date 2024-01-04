# mypkg
[![test](https://github.com/isiyakiimo3gou/mypkg/actions/workflows/test.yml/badge.svg)](https://github.com/isiyakiimo3gou/mypkg/actions/workflows/test.yml)

* このリポジトリは千葉工業大学ロボットシステム学の授業で使用している
* このリポジトリはROS2のパッケージである。

# このパッケージでできること


talkerとlistenerの2つのノードで作成されている。
takerから出力さえれた数字のカウントをcountupを通じてlistenerに伝えることができる。

## talker

0.5秒ごとに数字をカウントしていきその結果をcountupを通じて伝える。

### 使用方法

talkerとlistenerで端末を分ける。

端末1
```
$ ros2 run mypkg talker
```

## トピック(countup)について

talkerとlistenerをlnt16型のメッセージで送信し、出力する。


## listener

talkerからcountupを通じて伝わってきた結果を出力する。

### 使用方法

端末2
```
$ ros2 run mypkg listener
```

出力結果
```
[INFO] [1703724165.061180742] [listener]: Listen: 0
[INFO] [1703724165.560874550] [listener]: Listen: 1
[INFO] [1703724166.061071847] [listener]: Listen: 2
[INFO] [1703724166.560810623] [listener]: Listen: 3
[INFO] [1703724167.060889001] [listener]: Listen: 4
[INFO] [1703724167.560992485] [listener]: Listen: 5
[INFO] [1703724168.061459758] [listener]: Listen: 6
[INFO] [1703724168.561152211] [listener]: Listen: 7
[INFO] [1703724169.061162751] [listener]: Listen: 8
[INFO] [1703724169.561171072] [listener]: Listen: 9
[INFO] [1703724170.061432208] [listener]: Listen: 10
[INFO] [1703724170.561012187] [listener]: Listen: 11
[INFO] [1703724171.061278236] [listener]: Listen: 12
[INFO] [1703724171.560766265] [listener]: Listen: 13
[INFO] [1703724172.061157728] [listener]: Listen: 14
```

## launch

talkerとlistenerを1つの端末で同時に使うことができる。

### 使用方法

```
$ ros2 launch mypkg talk_listen.launch.py
```

出力結果
```
[INFO] [launch]: Default logging verbosity is set to INFO
[INFO] [talker-1]: process started with pid [19446]
[INFO] [listener-2]: process started with pid [19448]
[listener-2] [INFO] [1703727259.790509145] [listener]: Listen: 0
[listener-2] [INFO] [1703727260.260496948] [listener]: Listen: 1
[listener-2] [INFO] [1703727260.761869980] [listener]: Listen: 2
[listener-2] [INFO] [1703727261.262054625] [listener]: Listen: 3
[listener-2] [INFO] [1703727261.762175446] [listener]: Listen: 4
[listener-2] [INFO] [1703727262.259648852] [listener]: Listen: 5
[listener-2] [INFO] [1703727262.759609649] [listener]: Listen: 6
[listener-2] [INFO] [1703727263.259626510] [listener]: Listen: 7
[listener-2] [INFO] [1703727263.759615027] [listener]: Listen: 8
[listener-2] [INFO] [1703727264.260064831] [listener]: Listen: 9
[listener-2] [INFO] [1703727264.760273480] [listener]: Listen: 10
[listener-2] [INFO] [1703727265.259993007] [listener]: Listen: 11
[listener-2] [INFO] [1703727265.761465445] [listener]: Listen: 12
[listener-2] [INFO] [1703727266.261727099] [listener]: Listen: 13
[listener-2] [INFO] [1703727266.761773901] [listener]: Listen: 14
```

## 必要なソフトウェア
* Python
  * テスト済み: 3.7〜3.10

## テスト環境
* Ubuntu 22.04
  * ROS2 humble

## ライセンス

* このソフトウェアパッケージは，3条項BSDライセンスの下，再頒布および使用が許可されます.
* このパッケージのコードは，下記のスライド（CC-BY-SA 4.0 by Ryuichi Ueda）のものを，本人の許可を得て一部自身の著作としたものです．
	* [ryuichiueda/my_slides/robosys_t2022](https://github.com/ryuichiueda/my_slides/tree/master/robosys_2022)

© 2023 hitokoto takumi



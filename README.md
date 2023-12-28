# mypkg


このリポジトリは千葉工業大学ロボットシステム学の授業で使用している

##インストール方法

ホームディレクトリにクローンし、リポジトリを複製する
```

$git clone https://github.com/isiyakiimo3gou/mypkg.git

```

その後入力する
```

$cd ~/ros2_ws

```

#ノード

##talker

０．５秒ごとに数字をカウントしていきその結果をcountupを通じて伝える。

###使用方法

talkerとlistenerで端末を分ける。

端末1
```
$ ros2 run mypkg talker
```
##listener

talkerからcountupを通じて伝わってきた結果を出力する。

###使用方法

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

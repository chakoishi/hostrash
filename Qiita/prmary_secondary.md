# ディスク名をprimary/secondaryにして気になった違和感

世の中master/slaveという名前が差別で
名前を置き換えましょうという事で
はいはいウチも対応しましょうと対応してみました。

* primary/replica
* primary/secondary
* main/sub

githubはmain/subにしたようですが
自分の場合はこの中からどれにしようかなーと思って
h1. ディスク名をprimary/secondaryにして気になった違和感

元自作派だった自分はIDE時代の名残もあって
primary/secondaryにディスク名を置き換えました。
数日経過し、何か違和感あるなーと思いました。

![prisec1.png](https://qiita-image-store.s3.ap-northeast-1.amazonaws.com/0/275150/35dc19f7-cdf6-d8bb-e5e7-f10dbbcb5081.png)
![prirep2.png](https://qiita-image-store.s3.ap-northeast-1.amazonaws.com/0/275150/794c428f-3a51-5c0b-0187-93cec0b5956b.png)
primary/secondary

画面はMac（言語：英語）での標準フォントで表示した時です。
Windows/Linuxでもこの差は出ると思います。

よく見たら文字数の差が2文字ありました。
デスクトップのHDD表示ならまだ我慢できるのですが、
パス比較とかするとこの差が開くので
それが原因だったようです。

![prirep1.png](https://qiita-image-store.s3.ap-northeast-1.amazonaws.com/0/275150/2da4d403-e73a-32cb-ad7a-1e5e2eb20740.png)
![prirep2.png](https://qiita-image-store.s3.ap-northeast-1.amazonaws.com/0/275150/6e462901-6d98-56a6-f1f5-ce40ce737cff.png)
primary/replica

![mainsub1.png](https://qiita-image-store.s3.ap-northeast-1.amazonaws.com/0/275150/40f3a7b6-d1d8-472c-e399-c1279a64c719.png)
![mainsub2.png](https://qiita-image-store.s3.ap-northeast-1.amazonaws.com/0/275150/370c3b32-04c4-f92c-e020-3ca46761ecc8.png)
main/sub

![masslv1.png](https://qiita-image-store.s3.ap-northeast-1.amazonaws.com/0/275150/aa5a3848-c015-8f52-a86e-ef0ad0c2ac65.png)
![masslv2.png](https://qiita-image-store.s3.ap-northeast-1.amazonaws.com/0/275150/b8aa3e0b-3642-2c52-af40-619f92291c97.png)
master/slave(旧)

この３つは1文字ですが、primary/replicaとmain/subは
旧master/slaveよりも文字幅が狭いので
パス比較の違和感が更に無くなります。

最終的にmain/subはソースコードでよく使うので
うちではprimary/replicaを選択しました。

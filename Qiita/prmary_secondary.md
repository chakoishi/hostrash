# ディスク名をprimary/secondaryにして気になった違和感

世の中master/slaveという名前が差別で<br>
名前を置き換えましょうという事で<br>
はいはいウチも対応しましょうと対応してみました。<br>

* primary/replica
* primary/secondary
* main/sub

githubはmain/subにしたようですが<br>
自分の場合はこの中からどれにしようかなーと思って<br>
元自作派だった自分はIDE時代の名残もあって<br>
primary/secondaryにディスク名を置き換えました。<br>
数日経過し、何か違和感あるなーと思いました。

![1](https://user-images.githubusercontent.com/31530633/117562419-cb4ac980-b0d9-11eb-81d4-8f8ed55c55cd.png)<br>
![2](https://user-images.githubusercontent.com/31530633/117562422-cede5080-b0d9-11eb-9220-a8e78e73d0c7.png)<br>
primary/secondary

画面はMac（言語：英語）での標準フォントで表示した時です。<br>
Windows/Linuxでもこの差は出ると思います。

よく見たら文字数の差が2文字ありました。<br>
デスクトップのHDD表示ならまだ我慢できるのですが、<br>
パス比較とかするとこの差が開くので<br>
それが原因だったようです。

![3](https://user-images.githubusercontent.com/31530633/117562423-d271d780-b0d9-11eb-835c-569889310190.png)<br>
![4](https://user-images.githubusercontent.com/31530633/117562427-d7cf2200-b0d9-11eb-9920-ea99ad5124e3.png)<br>
primary/replica

![5](https://user-images.githubusercontent.com/31530633/117562428-daca1280-b0d9-11eb-8258-a867874dc7a4.png)<br>
![6](https://user-images.githubusercontent.com/31530633/117562432-de5d9980-b0d9-11eb-8037-d552c977ca5e.png)<br>
main/sub

![7](https://user-images.githubusercontent.com/31530633/117562435-e1588a00-b0d9-11eb-9f2d-fe0c0f2a7b8a.png)<br>
![8](https://user-images.githubusercontent.com/31530633/117562437-e3bae400-b0d9-11eb-9d51-43b7e9e5b82e.png)<br>
master/slave(旧)

この３つは1文字ですが、primary/replicaとmain/subは<br>
旧master/slaveよりも文字幅が狭いので<br>
パス比較の違和感が更に無くなります。

最終的にmain/subはソースコードでよく使うので<br>
うちではprimary/replicaを選択しました。

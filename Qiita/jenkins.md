# jenkinsでリモートコンピュータからアクセスできない時の対処法

MacBrewでjenkinsをインストールした所ローカル環境からは入れるのに、同一ネットワークのiPadからは入れなくてあれーと悩んでいました
そういえば、昔Railsでもバインド関係で同じ事が起きたよなーと思い出し

```sh
less /usr/local/Cellar/jenkins/(Version)
```

ここを調べた所、やっぱりありました

```xml
<string>--httpListenAddress=127.0.0.1</string>
```

これを下のように置き換えます

```xml
<string>--httpListenAddress=0.0.0.0</string>
```

再起動します

```sh
brew services restart jenkins
```
<img width="187" alt="0eb93f12-034d-24ca-2954-209245278642" src="https://user-images.githubusercontent.com/31530633/117562131-a35a6680-b0d7-11eb-9170-7dcfd5b046c7.png">
リモートiPadからアクセスできました

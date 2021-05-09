# LinuxサーバでFolding@homeまとめ.md

有効期限を迎えそうなConohaクレジット消化するためにLinuxサーバでFolding@homeをしようと思ったのでメモ

## インストール

[FAHClientダウンロード](https://foldingathome.org/alternative-downloads/)に最新版がおいてあるので<br>wgetでFAHClient最新版をダウンロード
CUIで黙々解析するだけならFAHViewerとかはスルーでOK

```
# （↑のリンクで最新版URLを確認する事を推奨します）
# CentOS/Fedola
wget https://download.foldingathome.org/releases/public/release/fahclient/centos-6.7-64bit/v7.6/fahclient-7.6.13-1.x86_64.rpm
dnf localinstall fahclient-7.6.13-1.x86_64.rpm

# Debian/Ubuntu
wget https://download.foldingathome.org/releases/public/release/fahclient/debian-stable-64bit/v7.6/fahclient_7.6.13_amd64.deb
dpkg -i fahclient_7.6.13_amd64.deb
```
インストールするとfahclientが立ち上がりプロジェクト情報をダウンロードして分析開始します

## ディレクトリ
```
# 実行バイナリ
/usr/bin/FAHClient

# 起動停止
/etc/init.d/FAHClient start
/etc/init.d/FAHClient stop

# 設定ファイル
/etc/fahclient/config.xml

# ログ
/var/lib/fahclient
```

## フル稼働させたい
config.xmlで

```
  <power v='light'/>
```

これを

```
  <power v='full'/>
```

にして再起動すればフル稼働します

## 参考文献
[Folding@home COMMAND LINE ONLY OPTIONS](https://foldingathome.org/support/faq/installation-guides/linux/command-line-options/)

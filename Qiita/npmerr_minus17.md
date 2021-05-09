# npm install -g npmで-17エラーに遭遇した

npm install -g npmを実行したら下のような見慣れない-17エラーが出た

```
npm ERR! code EEXIST
npm ERR! syscall symlink
npm ERR! path ../../../lib/node_modules/npm/man/man1/npm-adduser.1
npm ERR! dest /usr/local/share/man/man1/npm-adduser.1
npm ERR! errno -17
npm ERR! EEXIST: file already exists, symlink '../../../lib/node_modules/npm/man/man1/npm-adduser.1' -> '/usr/local/share/man/man1/npm-adduser.1'
npm ERR! File exists: /usr/local/share/man/man1/npm-adduser.1
npm ERR! Remove the existing file and try again, or run npm
npm ERR! with --force to overwrite files recklessly.

npm ERR! A complete log of this run can be found in:
npm ERR!     /Users/xxx/.npm/_logs/2020-01-12T12_30_49_194Z-debug.log
```

brewで再インストールしても直らず、google先生に聞いても答えが出てこなかったので<br>
自力で解決しようと調査したところ/usr/local/share/man/man1下の<br>
npm〜のファイル全てがシンボリックリンクではないただのファイルだった<br>
恐らく何らかの理由で作成失敗したのではないか<br>
npmの他npxやman5にあるnpmrcも同じような事になっていたので以下のように削除した

```
cd /usr/local/share/man/man1
rm npm*
rm npx*
cd /usr/local/share/man/man5
rm npmrc.5
```
でもう一度npmインストール

```
npm install -g npm
/usr/local/bin/npm -> /usr/local/lib/node_modules/npm/bin/npm-cli.js
/usr/local/bin/npx -> /usr/local/lib/node_modules/npm/bin/npx-cli.js
+ npm@6.13.6
added 430 packages from 858 contributors in 15.374s
```
直った！

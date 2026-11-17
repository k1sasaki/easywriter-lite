# EasyWriter lite 連携ブックマークレット

## 使い方(2アクション)
1. Windowsの設定で `.md` ファイルの既定のアプリを普段使うブラウザ(Edge推奨)にする。
2. mdファイルをダブルクリック → ブラウザが生のテキストとして開く(アドレスバーに本当のファイルパスが出ている状態)。
3. このブックマークレットをクリック → 今開いているテキストの中身とファイル名を持って、EasyWriter liteへジャンプする。

## ブックマークレットの登録のしかた
1. ブラウザでブックマークバーを表示する(Edge/Chromeとも Ctrl+Shift+B)。
2. 空いている場所を右クリック→「ページを追加」(または「新しいブックマークを追加」)。
3. 名前は好きなもの(例:「→EasyWriter」)、URLの欄に下の1行をそのまま貼り付けて保存する。

## ブックマークレット本体(1行、URLの欄にそのまま貼る)

```
javascript:(function(){function e(s){var b=new TextEncoder().encode(s);var bin="";b.forEach(function(x){bin+=String.fromCharCode(x)});return btoa(bin)}var body=document.body.innerText||document.body.textContent||"";var p=decodeURIComponent(location.pathname);var name=p.split(/[\\/]/).pop();if(!/\.md$/i.test(name)){alert("mdファイルを開いた状態で使ってください");return}location.href="https://k1sasaki.github.io/easywriter-lite/#open="+e(name)+":"+e(body)})();
```

公開ページ(`https://k1sasaki.github.io/easywriter-lite/`)宛てのこの1行は、誰が使っても同じもので構わない。開いたファイルの中身はその場で読むだけで外部へは送らない。

## 動作の仕組み
- ブラウザがmdファイルを直接開いたとき、`document.body`の中には生のテキストがそのまま入っている(同じページ内の中身を読むだけなので、ブラウザのセキュリティ制限に触れない)。
- ファイル名は`location.pathname`(アドレスバーの実パス)から取り出す。
- 中身とファイル名をUTF-8のまま`base64`化して、EasyWriter liteのURLの`#open=...`に載せて移動する。
- EasyWriter lite側はページ読み込み時に`#open=`を見つけたらそれを読み、エディタに流し込む。

## 注意点
- この方法で読み込んだ場合、ブラウザはまだ「元のファイルへの書き込み権限」を持っていない。**保存するときは最初に一度「名前を付けて保存」で同じファイルを選び直す**必要がある(2回目以降はそのファイルに「保存」で直接上書きできる)。
- とても大きなファイル(数MB超)だとURLに乗せきれない可能性がある。普段のメモ程度のサイズなら問題ない。
- 公開URL宛てなので、どのPC・どの人の環境でも同じブックマークレットがそのまま使える。

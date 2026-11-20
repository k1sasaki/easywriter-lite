# EasyWriter lite

サーバー不要、インストール不要の軽量Markdownエディタ/ビュアー。`index.html` 1枚(約55KB)だけで完結する。

※ファイルは1枚ですが、エディタ本体([EasyMDE](https://github.com/Ionaru/easy-markdown-editor)・[marked.js](https://marked.js.org/))は毎回CDNから読み込むので、**インターネット接続が必要です**。軽さと引き換えに、オフラインでは動きません。

ダウンロード: [index.html](https://raw.githubusercontent.com/k1sasaki/easywriter-lite/main/index.html)(右クリック→名前を付けて保存)
お試し用の公開ページ: https://k1sasaki.github.io/easywriter-lite/

## できること
- Markdownをその場で編集しながらプレビュー([EasyMDE](https://github.com/Ionaru/easy-markdown-editor) + [marked.js](https://marked.js.org/))
- **開く / 保存 / 名前を付けて保存** — File System Access API対応ブラウザ(Chrome・Edge。Braveは`brave://flags/#file-system-access-api`を有効化すると対応)では、手元のファイルへ直接上書き保存できる。未対応ブラウザ(Firefox・Safariなど)は代わりにダウンロードする形にフォールバックする
- 画像はアップロードせず、URLまたは画像ファイルのパス(Windowsなら右クリック→「パスをコピー」した文字列をそのまま貼ってよい)をリンクとして貼るだけ。※パソコン内の画像パスを表示できるのは、`index.html`をダウンロードして直接(ファイルとして)開いた場合のみです。上の公開ページをブラウザで直接開いた場合は表示されません
- 配色のカスタマイズ(ツールバーの「配色」ボタン。このブラウザだけに記憶される)
- `.md`ファイルをブラウザに関連付けてダブルクリックで開き、ブックマークレットでこのページへ中身を渡す連携(`bookmarklet.md`参照)

## 使い方
`index.html`をダウンロードしてダブルクリックで開くのがおすすめです。あなたが開いたファイルの中身は、常にお手元のパソコンだけで処理され、どこにも送信されません(ダウンロード版でも、エディタ本体を読み込むためのインターネット接続は必要です)。

上の公開ページをブラウザで直接開いて試すこともできます。この場合も、ファイルの中身の扱いはダウンロード版とまったく同じです(「開く/保存」は、公開ページで使ってもダウンロード版で使っても同じく手元のファイルに対して直接動く)。

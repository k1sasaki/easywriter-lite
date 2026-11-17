# EasyWriter lite

サーバー不要、インストール不要の軽量Markdownエディタ/ビュアー。`index.html` 1枚(約55KB)だけで完結する。

ダウンロード: [index.html](https://raw.githubusercontent.com/k1sasaki/easywriter-lite/main/index.html)(右クリック→名前を付けて保存)
お試し用の公開ページ: https://k1sasaki.github.io/easywriter-lite/

## できること
- Markdownをその場で編集しながらプレビュー([EasyMDE](https://github.com/Ionaru/easy-markdown-editor) + [marked.js](https://marked.js.org/))
- **開く / 保存 / 名前を付けて保存** — File System Access API対応ブラウザ(Chrome・Edge。Braveは`brave://flags/#file-system-access-api`を有効化すると対応)では、手元のファイルへ直接上書き保存できる。未対応ブラウザ(Firefox・Safariなど)は代わりにダウンロードする形にフォールバックする
- 画像はアップロードせず、URLまたは画像ファイルのパス(Windowsなら右クリック→「パスをコピー」した文字列をそのまま貼ってよい)をリンクとして貼るだけ
- 配色のカスタマイズ(ツールバーの「配色」ボタン。このブラウザだけに記憶される)
- `.md`ファイルをブラウザに関連付けてダブルクリックで開き、ブックマークレットでこのページへ中身を渡す連携(`bookmarklet.md`参照)

## 使い方
`index.html`をダウンロードしてダブルクリックで開くのがおすすめです。ダウンロードしてしまえば、以後は完全にお手元のパソコンだけで完結し、このページを含めどこにも接続しません。

上の公開ページをブラウザで直接開いて試すこともできます。その場合もファイルの中身はその場で処理されるだけで、サーバーには一切送信されません(「開く/保存」は、公開ページで使ってもダウンロード版で使っても同じく手元のファイルに対して直接動く)。

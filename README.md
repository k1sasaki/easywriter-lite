# EasyWriter lite

サーバー不要、インストール不要の軽量Markdownエディタ/ビュアー。`index.html` 1枚(約55KB)だけで完結する。

公開ページ: https://k1sasaki.github.io/easywriter-lite/

## できること
- Markdownをその場で編集しながらプレビュー([EasyMDE](https://github.com/Ionaru/easy-markdown-editor) + [marked.js](https://marked.js.org/))
- **開く / 保存 / 名前を付けて保存** — File System Access API対応ブラウザ(Chrome・Edge。Braveは`brave://flags/#file-system-access-api`を有効化すると対応)では、手元のファイルへ直接上書き保存できる。未対応ブラウザ(Firefox・Safariなど)は代わりにダウンロードする形にフォールバックする
- 画像はアップロードせず、URLまたは画像ファイルのパス(Windowsなら右クリック→「パスをコピー」した文字列をそのまま貼ってよい)をリンクとして貼るだけ
- 配色のカスタマイズ(ツールバーの「配色」ボタン。このブラウザだけに記憶される)
- `.md`ファイルをブラウザに関連付けてダブルクリックで開き、ブックマークレットでこのページへ中身を渡す連携(`bookmarklet.md`参照)

## 使い方
`index.html`をダウンロードしてダブルクリックで開くだけ。または上の公開ページをブラウザで開いてそのまま使ってもよい(どちらでも「開く/保存」は手元のファイルに対して直接動く)。

## できないこと(本家EasyWriterとの違い)
サーバーを持たないので、ファイル一覧・複数ファイル管理・画像のアップロード保存はない。常に「今開いている1ファイル」だけを扱う、1人用の軽量ツール。

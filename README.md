# 🚀 九九シューター

こたえのブロックをえらんで撃ちぬく、奥行きスクロール型の九九れんしゅうゲームです。
ブラウザだけで動きます(インストール不要)。

## あそびかた

- `←` `→` : レーン(3つのこたえ)をえらぶ
- `Space` または `↓` : いますぐ発射(はやいほどボーナス)
- `Enter` : スタート / もういちど
- `M` : おと ON/OFF
- タブレット・スマホ: 画面の左・中・右をタップ(同じレーンをもう一度タップで発射)

### ルール

- 正解のブロックを選ぶと、ぜんぶ破壊しながら前に進みます。
- 連続正解でコンボがたまり、5コンボごとにポイントが ×2 → ×3 → … → ×5 にアップ。
- コンボが増えるとブロックが速くなります(最大で約4割短縮)。
- まちがえるとコンボがリセットされ、ライフが1つ減ります(ライフ3つ)。
- 1ラウンドは20問。まちがえた九九は「にがて」として記録され、次から出やすくなります。
- 「れんしゅうモード」はライフなしで安心して練習できます。

## Macで遊ぶ(ローカル)

`index.html` をダブルクリックするだけで、SafariやChromeで開けます。

## GitHub Pagesで公開する

1. GitHubで新しいリポジトリを作る(例: `kuku-shooter`、Public)。
2. ターミナルで、このフォルダに移動して次を実行します。

```bash
git init
git add index.html README.md
git commit -m "九九シューター"
git branch -M main
git remote add origin https://github.com/<あなたのユーザー名>/kuku-shooter.git
git push -u origin main
```

3. GitHubのリポジトリで **Settings → Pages** を開き、
   **Source: Deploy from a branch / Branch: `main` / `/ (root)`** を選んで Save。
4. 1〜2分後に `https://<あなたのユーザー名>.github.io/kuku-shooter/` で遊べます。

## ファイル構成

- `index.html` : ゲーム本体(HTML・CSS・JavaScriptがすべて入っています)

ベストスコアと「にがて」の記録は、ブラウザのlocalStorageに保存されます。

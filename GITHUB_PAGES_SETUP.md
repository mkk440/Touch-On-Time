# GitHub Pages 公開手順

## 1. GitHub にリポジトリを作成
- 新しいリポジトリを作成します
- このフォルダの内容を push します

## 2. CSV をコミットしない
- `.gitignore` で `*.csv` `*.xlsx` `*.xls` は除外しています
- Touch On Time から落とした実データはリポジトリに入れず、各事務員さんのPCから画面上でアップロードしてください
- もし一度 Git の管理対象に入ってしまった CSV がある場合は、`git rm --cached "*.csv"` で追跡対象から外してから commit してください

## 3. GitHub Pages を有効化
1. GitHub の対象リポジトリを開く
2. `Settings` → `Pages` を開く
3. `Source` を `GitHub Actions` にする
4. `main` または `master` に push すると `.github/workflows/deploy-pages.yml` が自動実行されます

## 4. 公開 URL
- 初回デプロイ完了後、`https://<owner>.github.io/<repository>/` 形式の URL が発行されます
- その URL を事務員さんへ共有すれば利用できます

## 5. 日々の運用
- 事務員さんは URL を開く
- Touch On Time の CSV を画面にアップロードする
- 月表記と申請期限文言を必要に応じて入力する
- 生成された文章をコピーして Slack / LINE WORKS に貼り付ける

## 6. 更新方法
- `index.html` を修正して GitHub に push します
- GitHub Actions が再実行され、自動で公開ページが更新されます

## 7. 注意
- この設定では公開対象は `index.html` だけです。実CSVは GitHub Pages に載りません
- GitHub Pages の URL を知っている人がアクセスできます
- GitHub Pages を非公開公開にしたい場合は、契約プラン要件を先に確認してください

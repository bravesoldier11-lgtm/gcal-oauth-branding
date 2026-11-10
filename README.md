# Google OAuth ブランディング用静的ページ

GCP「ブランディング」に載せるホームページ・プライバシーポリシー URL 用。

## GitHub Pages で公開する手順（推奨）

`git config` のユーザー名 `hirokazu` は GitHub 上に存在します（https://github.com/hirokazu）。
**この環境では `gh` が未ログインのため、プッシュは手元のターミナルで実行してください。**

```bash
cd /Users/soldier/metan_weather_10s/docs/gcal-oauth-branding
gh auth login   # 未ログインの場合
gh repo create gcal-oauth-branding --public --source=. --remote=origin --push
# または既存空リポを作ってから:
# git init && git add index.html privacy-policy.html && git commit -m "Add OAuth branding pages"
# git branch -M main && git remote add origin git@github.com:hirokazu/gcal-oauth-branding.git && git push -u origin main
```

GitHub → リポジトリ **Settings → Pages** → Source: **Deploy from branch** → `main` / `/ (root)` → Save。

## GCP に入力する URL（Pages 有効化後）

| 項目 | URL |
|------|-----|
| アプリのホームページ | `https://hirokazu.github.io/gcal-oauth-branding/` |
| プライバシーポリシー | `https://hirokazu.github.io/gcal-oauth-branding/privacy-policy.html` |
| 承認済みドメイン（追加） | `hirokazu.github.io` |

※ リポジトリ名を変えた場合は URL もそれに合わせて変更してください。

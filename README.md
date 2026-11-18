# Google OAuth ブランディング用静的ページ

GCP「ブランディング」に載せるホームページ・プライバシーポリシー URL 用。

- **リポ:** https://github.com/bravesoldier11-lgtm/gcal-oauth-branding
- **カスタムドメイン:** `gcal.rebuild-works.xyz`（`CNAME` ファイル参照）

## お名前.com での DNS（ヒロが操作）

**DNS 設定** → ホスト名などの設定 → `rebuild-works.xyz` を選択 → **DNS レコード設定を利用する**

| ホスト名 | TYPE | TTL | VALUE |
|----------|------|-----|--------|
| `gcal` | CNAME | 3600（既定で可） | `bravesoldier11-lgtm.github.io.` |

※ 末尾のドットはお名前.com の画面では省略されても可。反映まで最大数時間。

確認: `dig +short gcal.rebuild-works.xyz CNAME` で `bravesoldier11-lgtm.github.io.` が返ること。

GitHub → リポ **Settings → Pages** で Custom domain が `gcal.rebuild-works.xyz`、HTTPS が有効になるまで待つ。

## GCP に入力する URL（本番ブランディング）

| 項目 | URL |
|------|-----|
| 承認済みドメイン | `rebuild-works.xyz` |
| アプリのホームページ | `https://gcal.rebuild-works.xyz/` |
| プライバシーポリシー | `https://gcal.rebuild-works.xyz/privacy-policy.html` |

Search Console で **ドメイン** プロパティ `rebuild-works.xyz` を TXT で確認してから、上記を保存。

## ローカル更新

```bash
cd /Users/soldier/metan_weather_10s/docs/gcal-oauth-branding
git add -A && git commit -m "..." && git push origin main
```
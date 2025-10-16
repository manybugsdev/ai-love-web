# ai-love-web

完全自律型AI Web制作のランディングページ

## 機能

### 相談フォーム

相談フォームは**Netlify Forms**を使用して実装されています。

#### 実装内容

- フォームデータの自動保存
- メール通知機能（Netlify経由）
- スパム対策（honeypotフィールド）
- リアルタイムフィードバック（成功/エラーメッセージ）
- フォームバリデーション

#### デプロイ方法

1. **Netlifyにデプロイ**
   ```bash
   # GitHubリポジトリをNetlifyに接続するか、Netlify CLIを使用
   netlify init
   netlify deploy --prod
   ```

2. **フォーム通知の設定**
   - Netlifyダッシュボードにログイン
   - サイト設定 > Forms > Form notifications
   - メール通知を設定

#### ローカル開発

ローカルでテストする場合は、Netlify Devを使用してください：

```bash
npm install -g netlify-cli
netlify dev
```

#### フォームフィールド

- **会社名** (必須)
- **お名前** (必須)
- **メールアドレス** (必須)
- **電話番号** (任意)
- **ご相談内容** (任意)

#### 技術詳細

- フォームはHTML5のネイティブバリデーションを使用
- JavaScriptでAjax送信を実装
- 送信中は送信ボタンを無効化
- 成功/エラーメッセージを表示
- 5秒後にメッセージを自動非表示

## ライセンス

© 2025 AI LOVE. All rights reserved.
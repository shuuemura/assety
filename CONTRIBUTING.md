# 🤝 Contributing to Assety

Assetyへのコントリビューションをありがとうございます！このプロジェクトは**価値ある家計管理アプリケーション**の構築を目指しており、その開発プロセスを通じて**現代的なWeb技術の学習**も兼ねています。

## 🎯 プロジェクトの位置づけ

### 主目的：価値あるプロダクト開発
- ユーザーにとって本当に役立つ家計管理アプリケーションの構築
- 実用性とユーザビリティを重視した機能設計
- 長期的に運用可能な品質とアーキテクチャ

### 副次的効果：技術学習
- モダンなWeb技術スタックの実践的習得
- 実際のプロダクト開発を通じたベストプラクティスの学習
- チーム開発・OSS開発の経験

## 🚀 開発環境セットアップ

### 必要な環境
- **Node.js** 18.0.0以上
- **PostgreSQL** 14以上
- **Git** 2.30以上

### 初回セットアップ
```bash
# 1. リポジトリをフォーク・クローン
git clone https://github.com/your-username/assety.git
cd assety

# 2. 依存関係をインストール
npm install

# 3. 環境変数を設定
cp .env.example .env.local
# .env.localを編集してデータベース接続情報を設定

# 4. データベースをセットアップ
npm run db:generate
npm run db:push

# 5. 開発サーバーを起動
npm run dev
```

## 📋 コントリビューションの流れ

### 1. Issue作成・議論
- 新機能やバグ修正の前に、必ずIssueで議論
- **ユーザー価値**を明確にした提案を心がける
- 技術的な学習要素があれば併記

### 2. 開発ブランチ作成
```bash
# 機能開発の場合
git checkout -b feature/issue-number-feature-name

# バグ修正の場合
git checkout -b fix/issue-number-bug-description

# 学習目的のリファクタリングの場合
git checkout -b refactor/issue-number-learning-objective
```

### 3. 実装・テスト
- **ユーザー価値を最優先**に実装
- コードの可読性・保守性を重視
- 適切なテストを追加

### 4. プルリクエスト作成
- **ユーザーへの価値**を明確に記述
- 技術的な学習ポイントがあれば併記
- レビューしやすい粒度でPRを分割

## 📝 コミット・PR規約

### コミットメッセージ
```
<type>(<scope>): <description>

[optional body]

[optional footer]
```

**Type:**
- `feat`: 新機能（ユーザー価値の追加）
- `fix`: バグ修正
- `docs`: ドキュメント更新
- `style`: コードフォーマット（機能に影響なし）
- `refactor`: リファクタリング（学習目的含む）
- `test`: テスト追加・修正
- `chore`: その他の変更

**例:**
```
feat(dashboard): add monthly spending chart

ユーザーが月次支出をビジュアルで確認できるチャート機能を追加
- Recharts を使用したレスポンシブチャート
- カテゴリ別の色分け表示
- ホバー時の詳細情報表示

学習ポイント: React + TypeScript でのチャートライブラリ統合
```

### プルリクエストテンプレート
```markdown
## 📋 変更内容
<!-- ユーザーにとっての価値を明確に記述 -->

## 🎯 解決する課題
<!-- 関連するIssue番号 -->
Closes #123

## 🧪 テスト方法
<!-- レビュアーが確認すべき手順 -->

## 📚 学習ポイント（任意）
<!-- この実装で学んだ技術的なポイント -->

## 📸 スクリーンショット（UI変更の場合）
<!-- Before/After の画像 -->
```

## 🏗️ アーキテクチャ・設計原則

### コードベース構造
```
assety/
├── apps/web/                   # Next.js フロントエンド
│   ├── src/app/               # App Router ページ
│   ├── src/components/        # Reactコンポーネント
│   └── src/lib/               # ユーティリティ・設定
├── packages/
│   ├── database/              # Prisma スキーマ・クライアント
│   ├── graphql/               # GraphQL スキーマ・リゾルバー
│   └── ui/                    # 共通UIコンポーネント
└── infrastructure/            # AWS CDK/Terraform
```

### 設計原則
1. **ユーザーファースト** - 常にユーザー体験を最優先
2. **型安全性** - TypeScriptを活用した堅牢な実装
3. **テスタビリティ** - テストしやすい設計
4. **保守性** - 将来の変更に対応しやすい構造
5. **学習しやすさ** - 新しい開発者が理解しやすいコード

## 🧪 テスト戦略

### テストの種類
- **Unit Tests** - 個別関数・コンポーネントのテスト
- **Integration Tests** - API・データベース連携のテスト
- **E2E Tests** - ユーザーシナリオのテスト

### テスト実行
```bash
# 全テスト実行
npm run test

# ウォッチモード
npm run test:watch

# カバレッジ確認
npm run test:coverage

# E2Eテスト
npm run test:e2e
```

## 📖 学習リソース

### 技術スタック別学習ガイド

#### Next.js + React
- [Next.js公式ドキュメント](https://nextjs.org/docs)
- [React公式ドキュメント](https://react.dev)
- **学習ポイント**: App Router, Server Components, Client Components

#### TypeScript
- [TypeScript Handbook](https://www.typescriptlang.org/docs/)
- **学習ポイント**: 型定義、ジェネリクス、ユーティリティ型

#### データベース・API
- [Prisma Documentation](https://www.prisma.io/docs)
- [GraphQL Documentation](https://graphql.org/learn/)
- **学習ポイント**: スキーマ設計、型安全なクエリ

#### 状態管理
- [Redux Toolkit Documentation](https://redux-toolkit.js.org/)
- **学習ポイント**: Store設計、非同期処理

### 推奨学習フロー
1. **基礎固め** - TypeScript, React Hooks
2. **フレームワーク** - Next.js App Router
3. **データ層** - Prisma, GraphQL
4. **状態管理** - Redux Toolkit
5. **インフラ** - AWS, CI/CD

## 🎯 Issue ラベル

- `good first issue` - 初心者向けタスク
- `learning-focused` - 学習要素が強いタスク
- `user-value` - ユーザー価値が高い機能
- `technical-debt` - 技術的負債の解消
- `documentation` - ドキュメント改善
- `bug` - バグ修正
- `enhancement` - 機能改善

## 🤝 コミュニティ

### コミュニケーション
- **GitHub Discussions** - 機能提案・技術議論
- **GitHub Issues** - バグ報告・タスク管理
- **Pull Requests** - コードレビュー・学習共有

### 行動規範
- 建設的なフィードバックを心がける
- 学習過程での質問・間違いを歓迎する
- ユーザー価値を常に意識する
- 多様な技術レベルの参加者を尊重する

## 📞 サポート

質問や困ったことがあれば、遠慮なく以下で相談してください：

- **GitHub Issues** - バグ・機能要望
- **GitHub Discussions** - 技術的な質問・議論
- **Pull Request** - コードレビュー依頼

---

**🚀 一緒に価値あるプロダクトを作り、その過程で成長していきましょう！** 
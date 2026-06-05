# 要件定義
## 目的
本プロジェクトは、就活用の第三世代ポートフォリオサイトを構築することを目的とする。
短期で効率よく開発し、今後の拡張性を担保するため、フロントエンドフレームワークとして Astro を採用する。
また、Supabase を利用した画像管理、Vercel でのデプロイ、環境変数管理、UI/UX 設計など、実務に近いフロントエンド開発フローを通じて、企業に提出可能な品質のポートフォリオを完成させることを目標とする。
## スコープ
### トップページ
- MV
- キャッチコピー
- リンクとサマリー
ヘッダーなし
アニメーション
### 自己紹介
- 要約
- スキルセット
- 自己紹介
- 経歴(図)
- 今後に向けて
### ブログ一覧
拡張用
### 制作実績一覧
カードまたはリスト
画像とサマリー
### 制作実績
- 基本データ(表)、リンク
- ポイント
- 制作過程(画像多め)
- 一言(任意)
- リンク再掲
### 連絡
- フォーム(拡張用)
- 各種リンク

### グローバルナビゲーション
- レスポンシブ
- ハンバーガー
### 画像
Supabase Storage
### 公開
Vercelでデプロイ
## 前提・制約
### 開発の流れ
- githubリポジトリ作成
- astro環境構築
- レイアウトデザイン(Figma)
- 画像制作(Supabase Strage)
- コーディング(VS Code)
- デプロイ(Vercel)
### 開発の制約
- 開発期間：3日
最小構成かつ拡張性の最大化
- 予算：0円
Supabase Strage無料枠
既存の独自ドメインを活用
## 機能要件
- ヘッダー
- フッター
- MV
## 非機能要件
- 表示速度1秒以内
- GitHub push → Vercel 自動デプロイ
## 画面構成・データ構造
Layout.astro
pages/
  index.astro
  info/
    index.html
  about/
    index.astro
  skill/
    index.astro
    css.astro
  works/
    index.astro
    [slug].astro
  contact/
    index.astro
  blog/       /* 拡張用 */
    index.astro
    [slug].astro
  sitemap/
    index.html
Components/
  header.astro
  header-scrolled.astro
  footer.astro
  main.astro
  h1.astro
  h2.astro
  ui/
  feature/
Assets/
  images/
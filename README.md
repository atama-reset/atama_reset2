# reset WEBサイト

## 目指した課題解決
- 来店数増・問い合わせ数増・認知度の改善
- より見やすく、わかりやすい新サイトの構築
- よりレスポンスがよく、lighthouseで高く評価されるサイトに
- MicroCMSを利用し、サイト所有者が『お知らせ』と『ブログ』への投稿可能に

## サイトの概要
- 頭ほぐしの専門店のWEBサイト(お知らせ・ブログ投稿・予約問い合わせフォーム)

## URL
- https://atama-reset.com

## 開発したきっかけ
- 知人が経営する店舗のサイトリニューアルを打診

## 実装予定の機能
- フォームをReactHookFormで再構築

## 使用技術
- フレームワーク:Astro.js
- 言語:HTML,CSS,JavaScript,TypeScript
- インフラ:Netlify
- CMS:microCMS
- ライブラリ:dayjs emailjs swr


### デザイン
- Figmaでデザイン
- リラクゼーションを意識した柔和なデザイン、カラーリング
- ターゲット（脳疲労がある方）が見やすいようにフォントサイズを大きめに、明るさを控えめに設定
- ハンバーガーメニューをスマホサイズでは左側に、タブレット以上では右側に配置し、アニメーションを付加
- タブレットサイズ以下の画面幅でボトムナビゲーションを表示
- ブログページと予約ページへのアクセスを増やすため、画面上に常にリンクを表示

### CSS
- ヘッダーにグリッドレイアウトを使用
- 「選ばれる理由」セクションを、グリッドレイアウトでレスポンシブ化
- ハンバーガーメニューのアニメーション
- ブログサマリーにコンテナクエリを使用しHOME用、ブログ一覧用、アサイド用の3サイズに対応

### JavaScript
- IntersectionObserver スクロールに合わせて次のセクションを表示させる
- IntersectionObserver 下にスクロールするとボトムナビゲーションを表示させる（ファーストビューの表示領域を確保するため）
- IntersectionObserverをクラスコンポ―ネント化
- 「アクセス」と「最近のブログ」のスライダーにsplideを使用
- ブログ一覧、ブログ詳細ページにページネーションを実装

### React
- FAQページのアコーディオン
- ご予約・お問い合わせフォーム

### Email.js
- JavaScriptで実装すると環境変数が検証ツールから見えてしまうため、Reactで実装

### CMS
- microCMSを使用して、microCMSからブログ記事とお知らせ記事が投稿可能
- microCMSで投稿するとNetlifyで自動的にデプロイしてアップ可能

### GA4

## 制作期間
- 2024/7/7~8/8 Figmaでデザイン作成
- 2024/8/9~ コーディング開始
- 2024/12/4~ 公開開始

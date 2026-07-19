# GoldSrc SDK とアクセス方法

## 重要な注意：ソースコード非公開

**GoldSrc エンジンのソースコードは Valve によって公開されていません。** これは id Tech シリーズや Build Engine と大きく異なる点です。

### 何が非公開なのか？

| 対象 | 公開状況 | 補足 |
|---|---|---|
| **エンジンコア** | ❌ 非公開 | グラフィックス、ネットワーク、レンダリングなど |
| **ゲームロジック SDK** | ✅ 公開 | MOD 制作用の限定的なコード |
| **実行ファイル（バイナリ）** | ✅ 公開 | Steam で配布 |

## アクセス方法

### 1. Half-Life SDK（MOD 制作用）

**Steam Tools 経由**
- Steam で『Half-Life』を購入
- Tools セクションから **Half-Life SDK** をインストール
- 内容: エンティティ、武器、ゲームロジックのコード例

**GitHub ミラー**
- Half-Life SDK も GitHub に公開されているケースあり
- 正式なものは Valve GitHub を確認

### 2. Half-Life ゲーム自体

**Steam**
- URL: https://store.steampowered.com/app/70/
- 内容: GoldSrc エンジンのバイナリ版
- 価格: 無料または非常に安価

**その他のプラットフォーム**
- PlayStation 2, Xbox, Nintendo Switch などでも入手可能

## ソースコード公開されない理由

### 技術的・歴史的背景

1. **商業的価値の保持**
   - id Tech や Build Engine は発売後数年たってから公開
   - Valve は GoldSrc の技術的資産をより長く保有する戦略

2. **レガシーコード**
   - GoldSrc は Quake エンジン（id Tech 2）の改造版
   - Quake との法的・技術的な複雑さ

3. **Source Engine への移行**
   - Half-Life 2 で Valve は独自の Source Engine を開発
   - GoldSrc は「レガシー」として扱われる

## 派生プロジェクト・ソースポート

### 公式の継続サポート

- **Half-Life: Opposing Force**
- **Half-Life: Blue Shift**
- **Deathmatch Classic** など

### コミュニティによるプロジェクト

- **Half-Life: Restored** - バグ修正版
- **Half-Life Deathmatch: Source** - Source Engine への移植版
- **Black Mesa** - Unreal Engine 使用による Half-Life のリメイク

## あなたのプロジェクトに記録するもの

### ✅ 記録可能な事項
- GoldSrc の歴史と技術的な特徴
- 採用タイトル（Half-Life、Counter-Strike など）
- MOD コミュニティとエコシステム
- アクセス方法（Steam SDK、バイナリ）

### ⚠️ 記録不可の事項
- エンジンソースコード（非公開）
- 完全な技術ドキュメント（機密扱い）

## 重要なポイント

**GoldSrc は「古いが、エンジンコアはアクセス不可」という特殊な立場にあります。**

- Build Engine、id Tech とは異なり、フルソース公開されず
- ただし SDK と実行ファイルは利用可能
- MOD 制作文化は依然として活発

このため、このリポジトリでは **「技術的な知見」「歴史」「アクセス可能な範囲」** を中心に記録することになります。

## 参考資料

- (執筆時に追記)

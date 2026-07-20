# Package System

## 概要

Unreal Engine 3（UE3）のPackage Systemは、ゲームで使用されるアセットやオブジェクトを管理するためのデータ管理システムです。

UE3では、モデル、テクスチャ、マテリアル、アニメーション、サウンド、スクリプトなど、多くのゲームデータがPackage単位で管理されました。

この設計思想は、後のUnreal Engine 4・Unreal Engine 5におけるアセット管理システムにも大きな影響を与えています。

---

# Unreal EngineにおけるPackage思想

Unreal Engineでは、ゲーム内のデータを単純なファイル単位ではなく、オブジェクト集合として管理する設計が採用されています。

```text
Package

 ├── Object
 │
 ├── Texture
 │
 ├── Mesh
 │
 ├── Material
 │
 ├── Animation
 │
 └── Script
```

これにより、関連するデータをまとめて扱うことが可能になります。

---

# UE3 Package形式

Unreal Engine 3では、主に以下のPackage形式が利用されました。

## .upk

UE3における標準的なPackage形式です。

正式名称：

```
Unreal Package
```

用途：

- レベルデータ
- アセット管理
- マテリアル
- メッシュ
- アニメーション
- サウンド
- スクリプト

など。

---

# Package内部構造

UE3のPackageは、複数のオブジェクトを格納するコンテナとして機能します。

基本構造：

```text
.upk

├── Header
│
├── Name Table
│
├── Import Table
│
├── Export Table
│
└── Object Data
```

---

# Object Systemとの関係

UE3では、Package SystemはUnreal Object Systemと密接に結び付いています。

Unreal Engineでは、多くの要素がObjectとして管理されます。

例：

```text
UObject

 ├── Texture
 │
 ├── Material
 │
 ├── StaticMesh
 │
 ├── Actor
 │
 └── Sound
```

Packageは、これらのObjectを保存・管理する役割を持ちます。

---

# Asset管理

UE3では、開発者はUnrealEdを通じてPackage内のアセットを管理しました。

ワークフロー：

```text
Asset Creation

      ↓

Import

      ↓

UnrealEd

      ↓

Package保存

      ↓

Game Runtime
```

対象：

- 3Dモデル
- テクスチャ
- マテリアル
- アニメーション
- 音声データ

---

# Reference System

UE3のPackage Systemでは、Object同士の参照関係を管理します。

例：

```text
Character

 ├── Mesh Reference
 │
 ├── Material Reference
 │
 ├── Animation Reference
 │
 └── Sound Reference
```

これにより、複雑なゲームデータ構造を効率的に管理できます。

---

# Loading System

Package Systemは、ゲーム実行時のデータロードにも利用されます。

基本的な流れ：

```text
Game Start

     ↓

Load Package

     ↓

Load Required Objects

     ↓

Initialize Objects

     ↓

Gameplay
```

必要なデータのみ読み込むことで、メモリ使用量を制御できます。

---

# Cook処理

UE3では、開発用データを実際のゲーム実行用データへ変換するCook処理が存在しました。

```text
Development Data

       ↓

Cook

       ↓

Platform Optimized Data

       ↓

Game Runtime
```

Cookでは、

- 不要データ削除
- プラットフォーム最適化
- 圧縮
- 変換処理

などが行われました。

---

# コンソール対応との関係

UE3はPlayStation 3やXbox 360など、多くのプラットフォームで利用されました。

そのためPackage Systemには、

- データサイズ削減
- ロード時間短縮
- メモリ制約対応

が求められました。

Cook Pipelineは、UE3がAAAタイトル向けエンジンとして利用される上で重要な役割を果たしました。

---

# Mod文化への影響

Package SystemはUnreal EngineのMod文化にも大きな影響を与えました。

ユーザーは既存Packageを利用して、

- マップ追加
- キャラクター追加
- 武器追加
- ゲームルール変更

などを行うことができました。

代表例：

- Unreal Tournamentシリーズ
- Killing Floor
- Red Orchestra

など。

---

# UE4への継承

Unreal Engine 4ではPackage Systemの思想が発展しました。

比較：

| UE3 | UE4 |
|-|-|
| .upk | .uasset |
| Package | Asset System |
| Unreal Object | UObject |
| Cook | Cooking Pipeline |

UE4ではさらに、

- Asset管理改善
- Editor連携強化
- Blueprint対応

などが追加されています。

---

# 技術的意義

UE3のPackage Systemは、単なるファイル形式ではなく、Unreal Engineのデータ管理思想そのものでした。

影響：

- 複雑なゲームデータ管理
- EditorとRuntimeの統合
- Mod制作環境
- 後世代Asset Pipeline

など、現在のUnreal Engineにも続く設計基盤となっています。

---

# 現在の研究環境

★★★☆☆

UE3 Packageを扱うには、現在では主に以下の方法が利用されています。

- UDK環境
- UE3採用タイトル解析
- Package解析ツール
- Mod開発環境

公式開発環境の配布終了により、新規で触れる環境は限定されています。

---

# 関連項目

- [Unreal Engine 3](./README.md)
- [UDK](./UDK.md)
- [UnrealScript](./UnrealScript.md)
- [Rendering](./Rendering.md)

---

# 参考資料

- Epic Games Unreal Engine 3 Documentation
- Unreal Developer Network（UDN）
- UDK Documentation Archive
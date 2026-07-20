# Editor

## 概要

Unreal Engine 3（UE3）のEditor環境は、ゲーム制作に必要な各種ツールを統合した開発環境です。

中心となるツールはUnrealEdであり、レベル制作、アセット管理、イベント制御、マテリアル編集、アニメーション管理など、多くの開発作業を1つの環境内で行うことができます。

UE3のEditor設計は、後のUnreal Engine 4・Unreal Engine 5 Editorにも大きな影響を与えました。

---

# UnrealEdとは

UnrealEdは、Unreal Engineシリーズに標準搭載されているゲーム制作エディタです。

UE3では、UnrealEd 3として提供されました。

主な役割：

- レベル作成
- Actor配置
- アセット管理
- マテリアル編集
- イベント制作
- ライティング設定
- デバッグ

など。

---

# 統合開発環境としての設計

UE3の大きな特徴は、ゲーム制作に必要な機能を別々のツールではなく、1つのEditorへ統合したことです。

```text
                 UnrealEd

                     │

 ┌──────────┬──────────┬──────────┐

 ▼          ▼          ▼

Level     Content    Material

Editor    Browser    Editor


 ▼          ▼          ▼

Kismet    Cascade    Matinee
```

アーティスト、レベルデザイナー、プログラマーが同じ環境で作業できます。

---

# Level Editor

Level Editorはゲームステージを制作するための中心機能です。

主な機能：

- 地形配置
- Actor配置
- ライト配置
- トリガー設定
- プレイ確認

など。

基本的な制作フロー：

```text
Level Creation

      ↓

Actor Placement

      ↓

Lighting Setup

      ↓

Gameplay Setup

      ↓

Testing
```

---

# Actor System

UE3では、ゲーム世界に配置される要素をActorとして管理します。

例：

```text
Actor

├── Player

├── Enemy

├── Light

├── Trigger

└── Object
```

Editor上ではActorを配置・編集することでゲーム世界を構築できます。

---

# Content Browser

Content Browserは、ゲームアセットを管理するためのツールです。

管理対象：

- Texture
- Material
- Static Mesh
- Skeletal Mesh
- Animation
- Sound
- Package

など。

構造：

```text
Content Browser

        ↓

Package

        ↓

Asset

        ↓

Level Usage
```

この設計はUE4以降のAsset Browserへ継承されました。

---

# Property System

UE3 Editorでは、各オブジェクトの設定をPropertyによって管理します。

例：

Actor:

```text
Location

Rotation

Scale

Collision

Physics
```

Light:

```text
Color

Brightness

Radius
```

など。

プログラムを書かずに多くの設定変更が可能でした。

---

# BSP Editing

UE3ではBSP（Binary Space Partitioning）によるレベル構築も利用されました。

用途：

- 基本形状作成
- プロトタイプ制作
- 建築物ブロックアウト

など。

流れ：

```text
BSP Blockout

      ↓

Static Mesh Placement

      ↓

Final Level
```

UE1・UE2時代から続くUnreal Engineの伝統的なレベル制作手法です。

---

# 各ツールとの統合

UnrealEdにはUE3の主要システムが統合されています。

---

## Material Editor

Material Systemを編集するための環境。

関連：

- Texture
- Shader
- Surface表現

→ [Material System](./MaterialSystem.md)

---

## Cascade

パーティクルエフェクト制作環境。

関連：

- 爆発
- 炎
- 煙
- 魔法エフェクト

→ [Cascade](./Cascade.md)

---

## Kismet

イベント制御用ビジュアルスクリプト。

関連：

- Trigger
- Gameplay Event
- Sequence

→ [Kismet](./Kismet.md)

---

## Matinee

リアルタイムシネマティック制作環境。

関連：

- Camera
- Animation
- Cutscene

→ [Matinee](./Matinee.md)

---

# Play In Editor

UE3ではEditor内でゲームを実行できます。

用途：

- レベル確認
- 動作テスト
- デバッグ

制作と確認を高速化できます。

---

# Debug機能

UE3 Editorには開発向け機能も搭載されています。

例：

- View Mode切替
- Collision表示
- Performance確認
- Actor Debug

これにより、複雑なゲーム環境を調査できます。

---

# Build Pipelineとの関係

Editorで作成されたデータは、最終的にPackage化されゲームへ利用されます。

```text
Editor

 ↓

Package

 ↓

Cook

 ↓

Platform Build

 ↓

Game
```

関連：

→ [Package System](./PackageSystem.md)

---

# チーム開発への対応

UE3はAAAタイトル開発を想定して設計されました。

そのため、

- 大規模アセット管理
- 複数職種での作業
- コンソール向けビルド
- データ最適化

などに対応しています。

---

# UE4 / UE5への継承

UE4以降でもUnreal Editorの基本思想は継承されています。

| UE3 | UE4/UE5 |
|-|-|
| UnrealEd | Unreal Editor |
| Content Browser | Content Browser |
| Actor | Actor |
| Property System | Details Panel |
| Kismet | Blueprint |
| Matinee | Sequencer |
| Cascade | Niagara |

UE3で確立された「統合型ゲーム制作環境」という思想は現在も続いています。

---

# 技術的意義

UE3 Editorは、ゲームエンジンを単なる描画ライブラリから、総合開発環境へ発展させた重要な存在です。

影響：

- アーティスト主導の開発
- ノンプログラマー向け制作環境
- リアルタイム編集
- AAA開発ワークフロー

---

# 現在の研究環境

★★★☆☆

UE3 Editorを利用するには、

- UDK
- UE3開発環境
- 過去プロジェクト

などが必要です。

公式配布終了後は、主にアーカイブや技術研究目的で利用されています。

---

# 関連項目

- [Unreal Engine 3](./README.md)
- [UDK](./UDK.md)
- [Package System](./PackageSystem.md)
- [Kismet](./Kismet.md)
- [Matinee](./Matinee.md)
- [Cascade](./Cascade.md)

---

# 参考資料

- Epic Games Unreal Engine 3 Documentation
- Unreal Developer Network（UDN）
- UDK Documentation Archive
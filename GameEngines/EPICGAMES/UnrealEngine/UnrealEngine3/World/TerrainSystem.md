# Terrain System

## 概要

Unreal Engine 3（UE3）のTerrain Systemは、広大な屋外環境や自然地形を制作するための地形編集システムです。

高さ情報を利用したTerrain Actorによって、山、谷、平原などの自然環境を効率的に制作することができます。

このシステムは、後のUnreal Engine 4におけるLandscape Systemへ発展しました。

---

# 開発背景

ゲームの表現が高度化するにつれ、レベル制作では建築物だけではなく、広大な自然環境を効率的に作成する必要が生まれました。

必要となった要素：

- 広大なフィールド
- 山岳地形
- 起伏表現
- 地面テクスチャ管理
- 環境配置

UE3では、これらに対応するためTerrain Systemが提供されました。

---

# Terrain Actor

UE3ではTerrainはTerrain Actorとして管理されます。

```text
Terrain Actor

├── Height Data
│
├── Texture Layers
│
├── Material
│
└── Collision Data
```

Terrain Actorは通常のActor Systemの一部として扱われます。

---

# Heightmap

Terrain Systemの中心となるのがHeightmapです。

Heightmapは地形の高さ情報を画像データとして保持します。

```text
Heightmap

白

↓

高い地形


黒

↓

低い地形
```

この情報を元に3D地形を生成します。

---

# Terrain Editing

UnrealEd内では、Terrain Editorを利用して地形編集を行います。

主な操作：

- 隆起
- 侵食表現
- 平坦化
- 高さ調整
- 範囲編集

など。

---

# Texture Layer

Terrainでは複数のテクスチャレイヤーを重ねることができます。

例：

```text
Terrain

├── Grass Layer

├── Rock Layer

├── Sand Layer

└── Snow Layer
```

これにより自然な地表表現が可能になります。

---

# Terrain Material

TerrainはMaterial Systemと連携します。

```text
Terrain

 ↓

Material

 ↓

Shader

 ↓

Rendering
```

利用例：

- 草地
- 岩場
- 雪山
- 砂漠

など。

---

# Layer Blending

複数の地表を自然に混合するため、Layer Blendが利用されます。

例：

```text
Grass

   ↓

Transition

   ↓

Rock
```

境界を滑らかに表現できます。

---

# Lightingとの関係

TerrainはLighting Systemと連携します。

利用技術：

- Static Lighting
- Lightmass
- Shadow

など。

自然環境では、地形への光の当たり方が重要になります。

---

# Collision Systemとの関係

Terrainには物理衝突情報が生成されます。

用途：

- プレイヤー移動
- 車両走行
- 物理判定

など。

```text
Terrain Mesh

      ↓

Collision Data

      ↓

Physics System
```

---

# Vegetationとの関係

UE3 Terrainでは、自然環境制作のため、

- 草
- 木
- 岩
- 装飾物

などを配置するワークフローと組み合わせて利用されました。

ただし、UE4のFoliage Systemほど統合された仕組みではありませんでした。

---

# World制作との関係

Terrain Systemはレベル制作の基礎となります。

一般的な制作フロー：

```text
Terrain Creation

        ↓

Material Setup

        ↓

Lighting

        ↓

Object Placement

        ↓

Gameplay Setup
```

---

# BSPとの関係

UE3では、TerrainとBSPは用途が異なりました。

## BSP

用途：

- 建築物
- 室内
- ブロックアウト

## Terrain

用途：

- 屋外
- 自然環境
- 大規模地形

両者を組み合わせてレベルを構築します。

---

# 技術的意義

UE3 Terrain Systemは、ゲームエンジンにおける自然環境制作の基盤となりました。

影響：

- 大規模屋外レベル制作
- Heightmapベース地形
- Material Layer管理
- Landscape Systemへの発展

---

# UE4 Landscapeへの継承

UE4ではTerrain SystemがLandscape Systemへ発展しました。

比較：

| UE3 | UE4/UE5 |
|-|-|
| Terrain Actor | Landscape Actor |
| Heightmap | Heightmap |
| Texture Layer | Landscape Layer |
| Terrain Material | Landscape Material |

UE4 Landscapeではさらに、

- 大規模ワールド対応
- World Partition連携
- Foliage統合

などが追加されました。

---

# 現在の研究環境

★★★☆☆

UE3 Terrain Systemを利用するには、

- UDK
- UE3開発環境
- 過去プロジェクト
- 技術資料

などが必要です。

公式開発環境の配布終了後は、主に研究・保存目的で扱われています。

---

# 関連項目

- [Unreal Engine 3](./README.md)
- [Editor](./Editor.md)
- [Material System](./MaterialSystem.md)
- [Lightmass](./Lightmass.md)
- [Physics](./Physics.md)

---

# 参考資料

- Epic Games Unreal Engine 3 Documentation
- Unreal Developer Network（UDN）
- UDK Documentation Archive
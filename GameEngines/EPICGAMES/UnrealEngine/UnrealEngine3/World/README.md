# World

## 概要

`World/` は、Unreal Engine 3（UE3）におけるゲーム世界・レベル環境の構築技術を扱うカテゴリです。

UE3では、単純なステージ配置だけではなく、地形、建築物、環境オブジェクトなどを組み合わせて大規模なゲーム空間を制作することが可能でした。

このカテゴリでは、プレイヤーが存在する「世界」をどのように構築するかという観点から技術を記録します。

---

# 対象技術

現在、このカテゴリでは以下の技術を扱います。

| 技術 | 内容 |
|---|---|
| Terrain System | 高さマップベースの地形制作 |

---

# 技術構成

UE3のWorld制作は複数の技術を組み合わせて行われます。

```text
                  World

                    │

     ┌──────────────┼──────────────┐

     ▼              ▼              ▼

 Terrain          BSP          Object

 地形制作       空間構築       配置要素


                    │

                    ▼

                Level
```

---

# Terrain System

## 概要

Terrain Systemは、UE3における自然地形制作システムです。

Heightmapを利用して、

- 山
- 谷
- 平原
- 自然環境

などを効率的に制作できます。

→ [Terrain System](./TerrainSystem.md)

---

# Level制作との関係

UE3では、World制作はLevel単位で管理されます。

基本的な流れ：

```text
Terrain Creation

        ↓

Object Placement

        ↓

Lighting Setup

        ↓

Gameplay Setup

        ↓

Level Build
```

---

# BSPとの関係

UE3ではTerrainだけではなく、BSPによる空間構築も利用されました。

用途：

## BSP

- 建築物
- 室内空間
- プロトタイプ制作

## Terrain

- 屋外環境
- 自然地形
- 大規模エリア

それぞれ異なる用途で利用されました。

---

# Static Meshとの関係

最終的なゲームレベルでは、TerrainだけではなくStatic Meshを大量に配置します。

例：

```text
World

├── Terrain

├── Building

├── Props

├── Foliage

└── Lighting
```

UE3では、TerrainとMeshを組み合わせて完成した環境を制作します。

---

# Material Systemとの関係

World表現ではMaterial Systemが重要な役割を持ちます。

```text
Terrain

 ↓

Material

 ↓

Texture Layer

 ↓

Final Surface
```

地面、岩、雪などの表現はMaterialによって制御されます。

---

# Lighting Systemとの関係

環境制作ではLightingも重要な要素です。

関連：

- Static Lighting
- Lightmass
- Shadow

など。

```text
World

 ↓

Lighting Calculation

 ↓

Final Image
```

---

# Physicsとの関係

World内のオブジェクトはPhysics Systemと連携します。

例：

- 地形Collision
- 建築物Collision
- 物理オブジェクト

など。

```text
World Geometry

        ↓

Collision Data

        ↓

Physics
```

---

# UE4 / UE5への継承

UE3のWorld制作技術は、後世代で大きく発展しました。

| UE3 | UE4/UE5 |
|-|-|
| Terrain System | Landscape |
| Level | Level |
| Static Mesh配置 | Static Mesh配置 |
| Streaming Level | World Partition |

特にTerrain Systemは、UE4 Landscapeの基礎となりました。

---

# 技術的意義

UE3 World Systemは、HDゲーム世代における大規模環境制作の基盤となりました。

影響：

- オープンエリア制作
- Heightmap地形
- 大規模Level制作
- 環境アートワークの効率化

---

# 今後追加予定

以下の技術は、必要に応じて追加予定です。

- BSP System
- Level Streaming
- Foliage System
- World Building Workflow

---

# 関連項目

- [Terrain System](./TerrainSystem.md)
- [Editor](../Core/Editor.md)
- [Rendering](../Rendering/README.md)
- [Gameplay](../Gameplay/README.md)

---

# 参考資料

- Epic Games Unreal Engine Documentation
- Unreal Developer Network（UDN）
- UDK Documentation Archive
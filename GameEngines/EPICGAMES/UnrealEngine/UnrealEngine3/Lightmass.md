# Lightmass

## 概要

Lightmassは、Unreal Engine 3後期に導入されたグローバルイルミネーション（Global Illumination）向けのライティングシステムです。

静的な光源による間接光を事前計算することで、リアルタイム処理だけでは困難だった高品質な照明表現を実現しました。

Lightmassは、Unreal Engine 4以降のライティング技術にも大きな影響を与えた重要なシステムです。

---

# 開発背景

初期の3Dゲームでは、主に以下のような単純なライティングが利用されていました。

- 頂点ライティング
- 事前計算されたライトマップ
- 単純な動的ライト

しかしHDゲーム世代では、

- 建物内部の反射光
- 間接照明
- 自然な影の表現
- 光の回り込み

など、より現実的な照明表現が求められるようになりました。

UE3では、これらを実現するためLightmassが導入されました。

---

# 基本概念

Lightmassは、リアルタイムで全ての光計算を行うのではなく、事前計算によって照明情報を生成します。

```text
Level Data

     ↓

Lightmass Calculation

     ↓

Lightmap Generation

     ↓

Game Runtime
```

ゲーム実行時には計算済みデータを利用するため、高品質な照明を低い処理負荷で利用できます。

---

# Global Illumination

Lightmassの中心となる技術がGlobal Illumination（GI）です。

GIでは、直接光だけではなく、物体に反射した光も計算します。

例：

```text
Light Source

      ↓

Wall Reflection

      ↓

Indirect Light

      ↓

Object Illumination
```

これにより、より自然な光表現が可能になります。

---

# Static Lighting

Lightmassは主にStatic Lighting向けに設計されています。

対象：

- 建築物
- 地形
- 固定オブジェクト
- 環境ライト

など。

事前計算されたライト情報をLightmapとして保存します。

---

# Lightmap

Lightmassでは、計算結果をLightmapとして保存します。

```text
3D Object

      ↓

Lighting Calculation

      ↓

Lightmap Texture

      ↓

Runtime Rendering
```

メリット：

- 高品質な照明
- 少ないGPU負荷
- コンソール向け最適化

---

# Dynamic Lightingとの関係

Lightmassは全てのライトを置き換えるものではありません。

UE3では、

- Static Lighting
- Dynamic Lighting

を組み合わせて利用しました。

例：

```text
Environment Lighting

        ↓

Lightmass


Character

        ↓

Dynamic Shadow
```

固定環境はLightmass、動的オブジェクトはリアルタイム処理という分担です。

---

# UnrealEdとの連携

LightmassはUnrealEdと統合されています。

制作フロー：

```text
Level制作

    ↓

Light配置

    ↓

Lightmass Build

    ↓

Lightmap生成

    ↓

Preview確認
```

レベルデザイナーはエディタ上で照明結果を確認しながら制作できます。

---

# UE3での利用例

Lightmassは主に以下のような表現に利用されました。

- 屋内照明
- 屋外環境
- 建築物
- ファンタジー空間
- SFステージ

特にリアルな環境表現を重視するタイトルで活用されました。

---

# UE4への継承

Lightmassの思想はUE4でも継承されました。

| UE3 | UE4 |
|-|-|
| Lightmass | Lightmass |
| Static Lighting | Static Lighting |
| Lightmap | Lightmap |
| Precomputed GI | Precomputed Lighting |

UE4ではさらに、

- Distance Field Lighting
- LPV
- Ray Tracing

など新しい技術へ発展していきました。

---

# Lumenとの関係

UE5のLumenはリアルタイムGlobal Illuminationを目指した技術です。

Lightmass：

```text
事前計算型GI
```

Lumen：

```text
リアルタイムGI
```

という違いがあります。

しかし、

- 間接光表現
- 現実的な照明
- 環境光計算

という目的は共通しています。

---

# 技術的意義

Lightmassは、ゲームにおける照明表現を大きく進化させました。

影響：

- 高品質な環境表現
- 映画的なゲーム映像
- コンソール世代への対応
- 後世代GI技術への基礎

---

# 現在の研究環境

★★★☆☆

UE3版Lightmassを利用するには、

- UDK
- UE3開発環境
- 過去のプロジェクト

などが必要です。

現在は主に技術研究・歴史保存目的で扱われています。

---

# 関連項目

- [Unreal Engine 3](./README.md)
- [Rendering](./Rendering.md)
- [Material System](./MaterialSystem.md)
- [UDK](./UDK.md)

---

# 参考資料

- Epic Games Unreal Engine 3 Documentation
- Unreal Developer Network（UDN）
- UDK Documentation Archive
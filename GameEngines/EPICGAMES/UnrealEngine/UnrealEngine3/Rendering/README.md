# Rendering

## 概要

`Rendering/` は、Unreal Engine 3（UE3）における描画技術・マテリアル・ライティングシステムを扱うカテゴリです。

UE3は、HDゲーム世代に対応するため、従来の固定機能型レンダリングからプログラマブルシェーダーを中心とした高度な描画システムへ移行しました。

この世代で確立されたMaterial Systemやライティング技術は、後のUnreal Engine 4・Unreal Engine 5にも大きな影響を与えています。

---

# 対象技術

現在、このカテゴリでは以下の技術を扱います。

| 技術 | 内容 |
|---|---|
| Rendering | UE3の描画パイプライン |
| Material System | シェーダーベースの材質システム |
| Lightmass | グローバルイルミネーション計算システム |

---

# 技術構成

UE3の描画システムは、複数の技術を組み合わせて構成されています。

```text
                 Rendering

                     │

     ┌───────────────┼───────────────┐

     ▼               ▼               ▼

Material        Lighting        Post Process

 System          System          Effects


     │               │

     ▼               ▼

 Shader         Lightmass
```

---

# Rendering

## 概要

UE3 Rendering Systemは、DirectX 9世代を中心としたリアルタイム描画システムです。

対応技術：

- Programmable Shader
- Normal Mapping
- HDR Rendering
- Deferred Rendering
- Post Processing

など。

→ [Rendering](./Rendering.md)

---

# Material System

## 概要

Material Systemは、UE3における材質表現の中心となるシステムです。

ノードベースのMaterial Editorによって、複雑なシェーダー表現をアーティストが構築できます。

用途：

- 金属
- ガラス
- 水
- 炎
- 発光表現

など。

→ [Material System](./MaterialSystem.md)

---

# Lightmass

## 概要

Lightmassは、UE3に搭載された事前計算型ライティングシステムです。

静的環境の光表現を計算することで、リアルタイム処理負荷を抑えながら高品質な照明表現を実現しました。

用途：

- 間接光
- Global Illumination
- Ambient Occlusion

など。

→ [Lightmass](./Lightmass.md)

---

# UE3 Renderingの特徴

UE3では、単純なポリゴン描画ではなく、複数の技術を組み合わせて映像表現を実現しました。

```text
Mesh

 ↓

Material

 ↓

Shader

 ↓

Lighting

 ↓

Post Process

 ↓

Final Image
```

---

# Material中心設計

UE3では、モデルそのものよりもMaterialによる表現が重要になりました。

例：

同じMeshでも、

```text
Mesh A

 +

Metal Material

↓

金属表現


Mesh A

 +

Glass Material

↓

ガラス表現
```

のように、材質によって見た目を大きく変化できます。

---

# Lighting Systemとの関係

UE3ではリアルタイムライトと事前計算ライトを組み合わせました。

```text
Dynamic Lighting

        +

Static Lighting

        ↓

Final Rendering
```

これにより、

- キャラクター照明
- 建築物照明
- 屋外環境

などを両立しました。

---

# Post Processing

UE3ではポストプロセスによる映像表現も発展しました。

例：

- Bloom
- Motion Blur
- Depth of Field
- Color Grading

など。

映画的なゲーム映像表現に大きく貢献しました。

---

# Cascadeとの関係

Rendering SystemはVFXとも密接に関係しています。

```text
Cascade

 ↓

Particle

 ↓

Material

 ↓

Rendering
```

炎や煙などの表現はMaterial Systemと組み合わせて実現されます。

→ [Cascade](../Production/Cascade.md)

---

# Animation Systemとの関係

キャラクター描画では、

```text
Skeletal Mesh

 ↓

Animation

 ↓

Material

 ↓

Rendering
```

という流れで最終的な映像を生成します。

---

# 技術的意義

UE3 Rendering Systemは、現代的なゲームグラフィックスの基礎となった重要な世代です。

影響：

- Shaderベース設計
- Material Editor普及
- リアルタイム映像表現
- アーティスト主導の描画制作

---

# 後世代への継承

UE4・UE5ではUE3の思想がさらに発展しました。

| UE3 | UE4/UE5 |
|-|-|
| Material System | Material System |
| Lightmass | Lightmass / Lumen |
| Deferred Rendering | Deferred / Forward Rendering |
| Post Process | Post Process |

特にMaterial SystemはUnreal Engineシリーズ全体で継続利用されています。

---

# 関連項目

- [Rendering](./Rendering.md)
- [Material System](./MaterialSystem.md)
- [Lightmass](./Lightmass.md)
- [Core](../Core/README.md)
- [Production](../Production/README.md)

---

# 参考資料

- Epic Games Unreal Engine Documentation
- Unreal Developer Network（UDN）
- UDK Documentation Archive
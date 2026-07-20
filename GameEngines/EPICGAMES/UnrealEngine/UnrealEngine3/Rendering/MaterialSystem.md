# Material System

## 概要

Unreal Engine 3（UE3）のMaterial Systemは、リアルタイムレンダリングにおける材質表現を制御するためのシステムです。

テクスチャの表示だけではなく、光の反射、表面の質感、発光、透明表現などをノードベースで構築することができます。

UE3のMaterial Systemは、後のUnreal Engine 4・Unreal Engine 5に搭載されるMaterial Editorの基礎となった重要な技術です。

---

# 開発背景

初期の3Dゲームでは、モデルにテクスチャを貼り付ける単純な表現が中心でした。

しかし、HDゲーム世代では、

- 金属
- ガラス
- 布
- 石
- 肌
- 水

など、より現実的な材質表現が求められるようになりました。

UE3では、プログラマーが直接シェーダーを書くのではなく、アーティストが視覚的に材質を構築できる仕組みとしてMaterial Systemが発展しました。

---

# 基本構造

UE3のMaterialは、複数の入力情報を組み合わせて最終的な表面表現を生成します。

```text
Texture

   +

Normal Map

   +

Specular

   +

Emissive

   +

Opacity

        ↓

    Material

        ↓

    Shader

        ↓

  Final Rendering
```

---

# Material Editor

UE3ではUnrealEd内にMaterial Editorが搭載されました。

Material Editorでは、ノードを接続することでシェーダー処理を構築します。

特徴：

- ノードベース編集
- リアルタイムプレビュー
- 複雑な材質表現
- パラメータ調整

---

# 主なMaterial要素

## Base Color

材質の基本色を定義します。

用途：

- キャラクターの肌
- 建築物
- 地形
- オブジェクト表面

---

## Normal Map

表面の凹凸情報を制御します。

実際のポリゴン数を増やさずに、細かな凹凸表現を可能にしました。

用途：

- 金属表面
- 岩肌
- 装備品
- キャラクター表面

---

## Specular

光沢や反射の強さを制御します。

例：

- 金属 → 高い反射
- 布 → 低い反射

など、材質ごとの違いを表現できます。

---

## Emissive

自己発光表現を制御します。

用途：

- ネオン
- SF装置
- 魔法エフェクト
- 発光部品

---

## Opacity

透明度を制御します。

用途：

- ガラス
- 半透明エフェクト
- UI表現

---

# Material Instance

UE3ではMaterial Instanceによって、共通Materialから派生した設定変更が可能でした。

例：

```text
Base Material

      ↓

Material Instance

      ↓

赤い車

青い車

黒い車
```

同じシェーダー構造を共有しながら、パラメータだけを変更できます。

利点：

- メモリ効率向上
- 制作速度向上
- 大量オブジェクト管理

---

# Shader生成

UE3ではMaterial設定から内部的にシェーダーコードが生成されます。

```text
Material Graph

      ↓

Shader Compilation

      ↓

GPU Shader

      ↓

Rendering
```

アーティストはGPUシェーダーの詳細を直接記述することなく、高度な描画表現を作成できます。

---

# Lightingとの関係

Material SystemはLighting Systemと密接に連携します。

例えば：

- Normal Mapによる陰影表現
- Specularによる反射
- Emissiveによる発光

などは、ライティング処理と組み合わせることで実現されています。

---

# パラメータ化

Materialでは、実行時に変更可能なパラメータを設定できます。

用途：

- キャラクター状態変化
- ダメージ表現
- 色変更
- 特殊効果

例：

```text
通常状態

↓

ダメージ状態

↓

発光状態
```

---

# UE4 / UE5への継承

UE3のMaterial Systemは、そのまま後継世代へ発展しました。

| UE3 | UE4 / UE5 |
|-|-|
| Material Editor | Material Editor |
| Material Instance | Material Instance |
| Node Graph | Material Graph |
| Shader生成 | Shader Pipeline |

UE4以降では、PBR（Physically Based Rendering）対応などにより、さらに高度な材質表現へ発展しています。

---

# 技術的意義

UE3のMaterial Systemは、ゲーム開発におけるアーティストとプログラマーの役割分担を大きく変化させました。

影響：

- アーティストによるシェーダー構築
- 開発効率向上
- 高品質なリアルタイム表現
- 現代的Material Workflowの確立

---

# 現在の研究環境

★★★☆☆

UE3およびUDKの公式配布は終了しています。

現在では、

- UDK環境
- UE3採用タイトル解析
- 技術資料
- アーカイブ

などを利用して研究されています。

---

# 関連項目

- [Unreal Engine 3](./README.md)
- [Rendering](./Rendering.md)
- [UDK](./UDK.md)
- [Lightmass](./Lightmass.md)

---

# 参考資料

- Epic Games Unreal Engine 3 Documentation
- Unreal Developer Network（UDN）
- UDK Documentation Archive
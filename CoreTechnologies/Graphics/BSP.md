# Binary Space Partitioning (BSP)

* 分野: 3Dグラフィックス
* 初登場: 1969年（Henry Fuchsらによる空間分割アルゴリズム）
* ゲームへの本格的な採用: 1990年代
* 関連技術: CSG、Portal、Occlusion Culling

---

# 概要

**Binary Space Partitioning（BSP）** は、空間を平面によって再帰的に二分割し、木構造（BSP Tree）として管理する空間分割アルゴリズムです。

ゲーム開発では主に、

* 描画順序の決定
* 可視判定（Visibility Determination）
* 当たり判定（Collision Detection）
* レベルデータの管理

などに利用されてきました。

1990年代から2000年代前半にかけて、多くの3Dゲームエンジンで採用された代表的な技術です。

---

# 基本的な考え方

BSPでは、一枚の平面によって空間を

* 前方（Front）
* 後方（Back）

の二つに分割します。

さらに、それぞれの空間を再び平面で分割していくことで、木構造（BSP Tree）を構築します。

```text
                Root
               /    \
          Front      Back
          /  \       /  \
         ... ...   ... ...
```

描画や判定を行う際には、この木構造を利用することで効率的に処理できます。

---

# ゲーム開発で利用された理由

1990年代のPCでは、

* CPU性能
* メモリ容量
* GPU性能

が現在より大きく制限されていました。

BSPを利用することで、

* 見えていない空間を描画しない
* 衝突判定対象を減らす
* 描画順序を効率的に決定する

ことができ、限られたハードウェア性能でも広い3D空間を扱えるようになりました。

---

# ゲームエンジンでの利用例

## DOOM

DOOMでは2次元マップをBSP Treeで分割し、壁の描画順序や可視判定に利用しました。

厳密には完全な3D空間ではなく、2.5D空間に対するBSPの利用です。

---

## Quake（id Tech 2）

Quakeでは完全な3D BSPが採用されました。

マップはコンパイル時にBSP Treeへ変換され、

* 描画
* 当たり判定
* PVS（Potentially Visible Set）

などへ利用されます。

---

## Unreal Engine

Unreal Engineでは、

**CSG（Constructive Solid Geometry）**

によって作成したブラシをコンパイルし、

BSP Treeへ変換する方式を採用しています。

そのため、

「BSPブラシ」

という呼び方が一般的になりました。

厳密には、

* ブラシ = CSGによるジオメトリ
* BSP = 空間分割データ構造

ですが、Unreal Engineでは慣習的に両者がほぼ同義として扱われています。

---

## Source Engine

Source EngineでもレベルはBSP形式（`.bsp`）として保存されます。

Valve Hammer Editorで作成したブラシは、コンパイル時にBSPへ変換され、可視判定や衝突判定などに利用されます。

---

# BSPとCSGの違い

混同されやすい概念ですが、それぞれ役割が異なります。

| CSG      | BSP               |
| -------- | ----------------- |
| モデルを作る方法 | 空間を管理する方法         |
| 加算・減算ブラシ | 空間分割アルゴリズム        |
| 編集時に利用   | コンパイル後に利用されることが多い |

Unreal Engineでは両者を組み合わせて利用するため、「BSP」という言葉が広い意味で使われることがあります。

---

# BSPの長所

* 描画を高速化できる
* 可視判定が容易
* 衝突判定に利用しやすい
* 静的なマップとの相性が良い

---

# BSPの短所

* 動的オブジェクトには向かない
* マップ変更のたびに再コンパイルが必要
* 大規模・複雑なマップではツリー構築コストが増える
* 現代ではGPU性能の向上により、他の手法が主流になりつつある

---

# 現在

現在でもBSPはゲーム開発技術として重要ですが、リアルタイムレンダリングでは

* BVH（Bounding Volume Hierarchy）
* Octree
* KD-Tree
* Portal
* GPU Occlusion Culling

などの技術が用途に応じて利用されています。

一方で、レベル設計やゲームエンジンの歴史を理解する上では、BSPは現在でも欠かせない基礎技術の一つです。

---

# 関連するゲームエンジン

* DOOM Engine
* id Tech 2
* id Tech 3
* Unreal Engine 1
* Unreal Engine 2
* GoldSrc
* Source Engine

---

# 関連項目

* CSG（Constructive Solid Geometry）
* Portal
* Occlusion Culling
* Quadtree
* Octree
* KD-Tree

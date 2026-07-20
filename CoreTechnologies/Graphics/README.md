# Graphics

## 概要

Graphicsでは、ゲーム開発で用いられる描画技術やレンダリング技術を扱います。

ゲームグラフィックスは、2Dゲームから3Dゲームまで幅広い分野にわたって発展してきました。本ディレクトリでは、特定のゲームエンジンに依存しない共通技術を中心に、その歴史や基本的な仕組みを記録します。

ゲームエンジン固有の実装については、`GameEngines/` 以下の各記事を参照してください。

---

# ディレクトリ構成

## Common

2D・3Dの両方で利用される共通技術を扱います。

例:

* 座標系
* テクスチャ
* カメラ
* 色空間
* アニメーション

---

## 2D

2Dゲームに特化した描画技術を扱います。

例:

* Sprite
* Tile Map
* Palette
* Parallax Scrolling
* Raster Effects
* Mode 7

---

## 3D

3Dゲームで利用される描画技術や空間管理技術を扱います。

例:

* BSP
* CSG
* Portal
* Shadow Mapping
* Deferred Rendering
* Physically Based Rendering (PBR)

---

# 本リポジトリでの位置付け

Graphicsでは、各技術の概要や歴史を広く紹介します。

ゲームエンジンごとの具体的な実装や設計思想については、各エンジンの記事で詳しく解説します。

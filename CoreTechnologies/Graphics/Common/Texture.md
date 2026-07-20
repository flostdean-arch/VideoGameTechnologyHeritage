# Texture

* 分野: Graphics（Common）
* 関連技術: Sprite、Tile Map、Texture Atlas、UV Mapping、Material、PBR

---

# 概要

**Texture（テクスチャ）**とは、ゲーム開発においてオブジェクトの表面へ色や模様などの情報を与えるために使用される画像データです。

現在では単に「画像を貼るためのデータ」だけではなく、

* 色（Base Color）
* 法線（Normal）
* 粗さ（Roughness）
* 金属度（Metallic）
* 発光（Emission）

など、さまざまな情報を保持するためにも利用されています。

2Dゲームではスプライトやタイルマップ、3Dゲームではモデルの表面表現に利用される、ゲームグラフィックスの基本技術の一つです。

---

# Textureと画像の違い

Textureは一般的な画像ファイル（PNG、JPEGなど）と混同されることがありますが、ゲーム開発では異なる意味を持ちます。

画像ファイルは保存形式であり、そのまま描画に利用されるとは限りません。

ゲームエンジンでは画像を読み込み、GPUが扱いやすい形式へ変換したものをTextureとして管理します。

```text
画像ファイル
(PNG, JPEG, DDS...)

        ↓ 読み込み

Texture

        ↓

GPUによる描画
```

そのため、Textureは「画像そのもの」ではなく、「描画のために管理される画像データ」と考えると理解しやすくなります。

---

# 2Dゲームでの利用

2Dゲームでは、Textureは主に以下の用途で利用されます。

* Sprite
* Tile Map
* UI
* Font
* Animation

複数の画像を一枚の大きなTextureへまとめた**Texture Atlas**も広く利用されています。

---

# 3Dゲームでの利用

3Dゲームでは、Textureはモデル表面へさまざまな情報を与えます。

代表例として、

* Base Color
* Normal Map
* Roughness Map
* Metallic Map
* Ambient Occlusion
* Emissive Map

などがあります。

これらを組み合わせることで、現実的な質感を表現できます。

---

# Texture Mapping

Textureは通常、3Dモデルへそのまま貼り付けられるわけではありません。

モデルにはUV座標が設定されており、それを利用してTextureのどの部分をモデルのどの面へ対応させるかを決定します。

この処理を**Texture Mapping**と呼びます。

---

# Texture Filtering

Textureを拡大・縮小して表示すると、そのままでは画質が大きく劣化します。

そのため、多くのゲームエンジンではTexture Filteringが利用されます。

代表的な方式として、

* Nearest Neighbor
* Bilinear Filtering
* Trilinear Filtering
* Anisotropic Filtering

などがあります。

---

# Mipmap

Textureを遠距離から描画すると、本来不要な高解像度画像まで読み込むことになり、画質や性能の問題が発生します。

そこで利用されるのが**Mipmap**です。

Mipmapでは、あらかじめ複数の解像度のTextureを生成しておき、距離に応じて適切なサイズを利用します。

これにより、

* エイリアシングの軽減
* 描画品質の向上
* GPU負荷の軽減

などの効果があります。

---

# 技術の変遷

## 初期のゲーム

初期のゲームでは、専用のキャラクターパターンやタイルデータが利用されており、現在の意味でのTextureは存在しませんでした。

---

## 1990年代

リアルタイム3Dグラフィックスの普及に伴い、Texture Mappingが広く利用されるようになりました。

代表例として、

* DOOM
* Quake
* Unreal

などが挙げられます。

---

## 2000年代

GPU性能の向上により、

* DDS形式
* Texture Compression
* Mipmap
* Normal Map

などが一般化しました。

---

## 2010年代以降

PBR（Physically Based Rendering）の普及により、

1つのTextureだけではなく、

* Base Color
* Roughness
* Metallic
* Normal

など複数のTextureを組み合わせる表現が標準となりました。

さらに、大規模なオープンワールドではVirtual Texturingなどの技術も利用されるようになっています。

---

# 利点

* 見た目を豊かにできる
* モデル数を増やさず表現力を向上できる
* GPUによる高速な描画が可能
* 2D・3Dの両方で利用できる

---

# 注意点

Textureは画質向上に大きく貢献しますが、高解像度化するとメモリ使用量や読み込み時間も増加します。

そのため、多くのゲームでは、

* Texture Compression
* Texture Atlas
* Mipmap
* Streaming
* Virtual Texturing

などの技術と組み合わせて利用されています。

---

# 関連するゲームエンジン

* Build Engine
* GoldSrc
* Source Engine
* Unreal Engine
* id Tech
* CryEngine
* Unity
* Godot

---

# 関連項目

* Texture Atlas
* Texture Mapping
* UV Mapping
* Mipmap
* Texture Filtering
* Material
* Sprite
* Tile Map
* Physically Based Rendering (PBR)

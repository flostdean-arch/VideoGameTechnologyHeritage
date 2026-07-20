# Rendering

## 概要

Unreal Engine 3（UE3）は、HDゲーム世代を代表するリアルタイム3Dレンダリング技術を採用したゲームエンジンです。

PlayStation 3、Xbox 360世代のハードウェア性能を活用するため、従来世代から大きく発展したシェーダーベースの描画システムを導入しました。

UE3のレンダリング技術は、その後のUnreal Engine 4以降にも大きな影響を与えています。

---

# 開発背景

Unreal Engine 2世代では、固定機能パイプラインからプログラマブルシェーダーへの移行が進みました。

UE3ではさらに、

- 高解像度化
- 複雑な材質表現
- 動的ライティング
- 映画的な画面演出

を実現するため、より高度なレンダリングシステムが設計されました。

---

# 基本構成

UE3の描画処理は、主に以下の要素で構成されています。

```text
Game Object

      ↓

Material System

      ↓

Shader Pipeline

      ↓

Lighting

      ↓

Post Processing

      ↓

Final Image
```

---

# Shader Model対応

UE3はDirectX 9世代のShader Modelを活用しました。

主な用途：

- Vertex Shader
- Pixel Shader
- Material表現
- Lighting計算

これにより、従来より高度な表面表現が可能になりました。

---

# Material System

UE3ではMaterial Editorによる高度な材質作成環境が提供されました。

Materialは単なるテクスチャ表示ではなく、

- 色
- 法線
- 光沢
- 透明度
- 発光
- 反射

など複数の要素を組み合わせて定義されます。

例：

```text
Base Color

+

Normal Map

+

Specular

+

Emissive

        ↓

Material
```

この設計思想は、UE4以降のMaterial Editorへ継承されています。

---

# Normal Mapping

UE3ではNormal Mappingが広く利用されました。

Normal Mappingは、低ポリゴンモデルに高詳細な表面表現を追加する技術です。

用途：

- キャラクターの細かな凹凸
- 建築物の表面表現
- 金属・岩・布などの質感表現

これにより、限られたポリゴン数でも高品質な映像表現が可能になりました。

---

# Deferred Rendering

UE3ではDeferred Renderingを採用しました。

Deferred Renderingでは、まず画面上の情報を保存し、その後ライティング処理を行います。

```text
Geometry Rendering

        ↓

G-Buffer生成

        ↓

Lighting計算

        ↓

Final Image
```

利点：

- 多数のライト処理
- 複雑なシーン表現
- 高度なポスト処理

を効率的に実行できます。

---

# HDR Rendering

UE3ではHDR（High Dynamic Range）Renderingを採用しました。

HDRにより、

- 明るい光源
- 暗い影
- 自然な露出変化

など、現実に近い光表現が可能になりました。

用途：

- 太陽光
- 爆発
- 発光オブジェクト
- 屋外環境

---

# Post Processing

UE3ではポストプロセス処理によって、最終的な画面表現を向上させました。

主な処理：

- Bloom
- Motion Blur
- Depth of Field
- Color Correction

これらにより、ゲーム画面を映画的に演出することが可能になりました。

---

# Lighting System

UE3では静的・動的ライティングを組み合わせた方式が採用されました。

代表的な技術：

- Static Lighting
- Dynamic Lighting
- Lightmass

特にLightmassはUE3後期を代表する技術で、事前計算による高品質な間接光表現を実現しました。

---

# Cascadeとの関係

UE3ではCascadeによるパーティクル表現もレンダリングシステムの重要な一部でした。

用途：

- 爆発
- 炎
- 煙
- 魔法エフェクト

CascadeはUE4でも継続して採用されました。

---

# 技術的影響

UE3のレンダリング技術は、現在のゲームエンジン設計へ大きな影響を与えました。

継承された要素：

| UE3 | 後継技術 |
|-|-|
| Material System | UE4/UE5 Material Editor |
| Shader Pipeline | 現代的Rendering Pipeline |
| Post Processing | 最新ゲームエンジン標準機能 |
| Cascade | Niagaraへ発展 |
| Lightmass | UE4/UE5 Lighting技術へ影響 |

---

# 現在の研究環境

★★★☆☆

UE3本体およびUDKの公式配布は終了しています。

現在は、

- 過去資料
- UDKアーカイブ
- UE3採用タイトル解析
- 技術文献

などを通じて研究されています。

---

# 関連項目

- [Unreal Engine 3](./README.md)
- [UDK](./UDK.md)
- [Lightmass](./Lightmass.md)
- [Material System](./MaterialSystem.md)

---

# 参考資料

- Epic Games Unreal Engine 3 Documentation
- Unreal Developer Network（UDN）
- UDK Documentation Archive
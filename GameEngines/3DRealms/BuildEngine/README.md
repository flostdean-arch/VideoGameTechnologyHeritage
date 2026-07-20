# Build Engine

## 概要

Build Engineは、Ken Silvermanによって1995年頃に開発されたゲームエンジンです。

『Duke Nukem 3D』『Shadow Warrior』『Blood』『Redneck Rampage』など、多くのFPSで採用されました。

一見すると3Dゲームですが、内部的にはSector（セクター）を中心とした独特の2.5D構造を採用しており、当時としては非常に自由度の高いマップ表現を実現しました。

---

# 本リポジトリでの扱い

Build Engineには、Unreal Engineやid Techのような公式な世代区分は存在しません。

そのため、本リポジトリでは、Build Engineを一つのゲームエンジンとして扱い、技術ごとに解説します。

---

# 主な特徴

- Sectorベースのマップ構造
- Portalによる可視判定
- Room over Room（疑似多層構造）
- スプライト主体のオブジェクト
- CONスクリプト

---

# 現在の研究環境

★★★★★

Build Engineのソースコードは公開されています。

また、

- EDuke32
- Mapster32
- NBlood
- Raze

などのプロジェクトにより、現在でも研究・MOD制作が可能です。

---

# 技術解説

- Sector
- Portal
- Renderer
- CON
- Map Format
- Room over Room

---

# 採用タイトル

- Duke Nukem 3D
- Shadow Warrior
- Blood
- Redneck Rampage
- Witchaven
- TekWar

---

# 後継・影響

Build Engineは完全な3Dエンジンではありませんでしたが、

- Sectorベース設計
- 高速な可視判定
- エディタ中心の開発

などは後のゲームエンジンにも影響を与えました。

また、EDuke32などの現代的な拡張によって、現在でも新作MODやゲームが制作されています。

# Unreal

## 概要

『Unreal』は、Epic MegaGamesが開発し、1998年に発売されたファーストパーソン・シューティングゲームである。

本作はUnreal Engine 1が初めて採用されたタイトルであり、高品質な3Dグラフィックス、広大なレベルデザイン、リアルタイムライティングなど、当時としては革新的な技術を実現した。

また、後のUnreal Engineシリーズへ続く設計思想や技術基盤の多くは、本作の開発を通して確立された。

---

# 基本情報

|項目|内容|
|---|---|
|発売日|1998年5月22日|
|開発|Epic MegaGames、Digital Extremes|
|販売|GT Interactive|
|ジャンル|First-person Shooter|
|対応機種|Microsoft Windows、Mac OS、Linux|
|ゲームエンジン|Unreal Engine 1|

---

# 技術的特徴

『Unreal』は、Unreal Engine 1のリファレンスタイトルとして、エンジンの主要技術を数多く実装している。

## BSPベースのレベル構築

ゲーム全体はBSP（Binary Space Partitioning）を中心としたレベル設計で構成されている。

複雑な屋内空間や広大な屋外空間を効率的に管理し、リアルタイムな可視判定や衝突判定を実現した。

---

## リアルタイムライティング

動的な照明表現やカラーライティングを採用し、従来のFPSよりも高い没入感を実現した。

---

## UnrealScript

ゲームロジックはUnrealScriptによって実装されており、ゲームプレイとエンジン本体を分離した設計となっている。

この仕組みは後のMOD制作環境の基礎となった。

---

## Actor System

プレイヤー、敵、武器、アイテム、トリガーなど、ゲーム内のほぼすべての要素はActorクラスを基盤として実装されている。

このオブジェクト指向設計は、現在のUnreal Engineにも受け継がれている。

---

# Unreal Engine 1への影響

『Unreal』の開発を通して、多くの基盤技術が確立された。

- Object System
- Actor System
- UnrealScript
- Package System
- UnrealEd
- BSP Rendering
- Software Renderer
- Glide Renderer
- Direct3D Renderer
- Network Multiplayer

これらは後のUnreal TournamentやUnreal Engine 2以降でも継承・発展していくことになる。

---

# 歴史的意義

『Unreal』は単なるゲームタイトルではなく、Unreal Engineシリーズの出発点となった作品である。

ゲーム本体だけでなく、エディタやスクリプト環境、ネットワーク機能を含めた「ゲーム開発プラットフォーム」として設計された点は、当時として非常に先進的であった。

現在のUnreal Engine 5に至るまで続く設計思想の多くは、本作で確立されたものである。

---

# 関連資料

- ../History.md
- ../Architecture.md
- ../Runtime/
- ../Rendering/
- ../UnrealScript/
- ../Packages/
- ../Networking/
- ../Editor/

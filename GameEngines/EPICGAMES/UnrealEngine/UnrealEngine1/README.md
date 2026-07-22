# Unreal Engine 1

## 概要

Unreal Engine 1は、Epic MegaGames（現 Epic Games）が開発した初代Unreal Engineであり、1998年発売の『Unreal』で初めて採用されたゲームエンジンである。

BSPを用いたレベル構築、オブジェクト指向のゲーム設計、独自スクリプト言語「UnrealScript」、統合開発環境「UnrealEd」など、多くの革新的な技術を採用し、現在のUnreal Engineシリーズの基礎を築いた。

本ディレクトリでは、Unreal Engine 1のアーキテクチャ、主要技術、開発ツール、採用タイトルなどを体系的に整理する。

---

# 基本情報

|項目|内容|
|---|---|
|開発元|Epic MegaGames（現 Epic Games）|
|初公開|1998年|
|初採用タイトル|Unreal|
|代表タイトル|Unreal / Unreal Tournament|
|対応プラットフォーム|Windows、Linux、Mac OS、PlayStation 2 など|
|主な技術|BSP Rendering、UnrealScript、Actor System、Package System|
|後継エンジン|Unreal Engine 2|

---

# ディレクトリ構成

```text
UnrealEngine1/
├── README.md
├── History.md
├── Architecture.md
├── Runtime/
├── Rendering/
├── UnrealScript/
├── Packages/
├── Networking/
├── Physics/
├── Audio/
├── AI/
├── Editor/
├── Tools/
└── Games/
```

---

# ドキュメント

## 基本資料

|ドキュメント|概要|
|---|---|
|README.md|Unreal Engine 1の概要|
|History.md|開発の経緯と歴史|
|Architecture.md|エンジン全体のアーキテクチャ|

---

## コアシステム

|ディレクトリ|内容|
|---|---|
|Runtime|Object・Actor・Game Loopなどランタイムシステム|
|Rendering|BSP、Renderer、Lightingなど描画システム|
|UnrealScript|スクリプトシステム|
|Packages|Packageファイルとアセット管理|
|Networking|マルチプレイヤーとReplication|
|Physics|衝突判定・移動・Zone管理|
|Audio|サウンドシステム|
|AI|Pawn、Bot、ナビゲーション|

---

## 開発ツール

|ディレクトリ|内容|
|---|---|
|Editor|UnrealEdの機能とワークフロー|
|Tools|付属ツールやコマンドラインツール|

---

## 採用タイトル

|ディレクトリ|内容|
|---|---|
|Games|Unreal Engine 1を採用したゲームタイトル|

---

# Unreal Engine 1の位置付け

Unreal Engine 1は、ゲームエンジンを「ゲームを動かすライブラリ」から「ゲーム開発プラットフォーム」へと発展させた先駆的な存在である。

オブジェクト指向設計、スクリプトによるゲームロジック、統合エディタ、パッケージシステムなどの設計思想は、後継のUnreal Engine 2・3・4・5へ受け継がれ、現在のUnreal Engineシリーズの礎となっている。

---

# 関連資料

- History.md
- Architecture.md
- Runtime/
- Rendering/
- UnrealScript/
- Packages/
- Networking/
- Physics/
- Audio/
- AI/
- Editor/
- Tools/
- Games/

# Unreal Engine 1 Architecture

## 概要

Unreal Engine 1は、Epic MegaGames（現 Epic Games）が開発した
初代Unreal Engineであり、1998年に登場した『Unreal』で初めて使用された。

本エンジンは、単なる描画ライブラリではなく、
ゲーム世界の構築、編集、スクリプト制御、ネットワーク処理を統合した
総合ゲーム開発環境として設計された。

Unreal Engine 1のアーキテクチャは、後のUnreal Engineシリーズの基礎となる
以下の思想を確立した。

- オブジェクト指向型ゲーム構造
- エディタ中心の開発環境
- スクリプトによるゲームロジック制御
- データ駆動型コンテンツ管理
- ネットワーク対応を前提としたゲーム設計


---

# Engine Architecture
+------------------------------------------------+
| Unreal Engine 1 |
+------------------------------------------------+
| |
| Game Layer |
| ├── UnrealScript |
| ├── Actor Classes |
| └── Gameplay Logic |
| |
+------------------------------------------------+
| |
| Object System |
| ├── Object Management |
| ├── Class System |
| └── Package System |
| |
+------------------------------------------------+
| |
| Engine Core |
| ├── Rendering |
| ├── Physics |
| ├── Audio |
| ├── Networking |
| └── Input |
| |
+------------------------------------------------+
| |
| Tools |
| ├── UnrealEd |
| └── Content Pipeline |
| |
+------------------------------------------------+



# Core Object Architecture

## Object System

Unreal Engine 1では、ゲーム内データを管理するための
独自オブジェクトシステムが導入された。

後のUnreal Engineで中心となるUObjectシステムの原型となる仕組みであり、
ゲーム内要素をクラス単位で管理する設計思想を採用していた。

主な役割:

- オブジェクト生成
- クラス情報管理
- シリアライズ
- パッケージ管理
- スクリプト連携


---

## Actor System

ActorはUnreal Engine 1におけるゲーム世界の基本オブジェクトである。

ゲーム内に存在する動的要素はActorとして管理された。

Actor

├── Pawn
│ ├── PlayerPawn
│ └── Creature
│
├── Inventory
│ ├── Weapon
│ └── Item
│
├── Trigger
│
├── Decoration
│
└── Effects



Actor Systemによって、

- プレイヤー
- 敵キャラクター
- 武器
- アイテム
- イベント制御
- マップギミック

などを統一的に扱うことが可能になった。


---

# Rendering Architecture

## BSP Rendering

Unreal Engine 1のレベル表現の中心はBSP
(Binary Space Partitioning)である。

BSPによって3D空間を分割し、
効率的な描画処理と衝突判定を実現した。

World

├── BSP Tree
│
├── Static Geometry
│
├── Actors
│
└── Lighting Data



BSPベースの設計により、
UnrealEd上でリアルタイムにレベル編集を行うことが可能だった。


---

## Renderer

Unreal Engine 1では複数の描画方式をサポートした。

主なRenderer:

- Software Renderer
- Glide Renderer
- Direct3D Renderer
- OpenGL Renderer


当時のPC環境に合わせて、
ハードウェアアクセラレーションを段階的に利用できる設計だった。


---

# Lighting System

Unreal Engine 1では、
リアルタイム3Dゲームとして高度なライティング表現を採用した。

主な要素:

- Light Actor
- Light Map
- Zone Lighting
- Dynamic Light


特にZoneシステムと組み合わせることで、
広大な3D空間の効率的な管理を可能にした。


---

# Gameplay Architecture

## UnrealScript

Unreal Engine 1では、
ゲームロジック記述用の専用言語としてUnrealScriptを導入した。

C++ Engine
  |
  |
  v
  UnrealScript
  |
  |
  v
  Game Logic

  

エンジン本体とゲームロジックを分離することで、

- MOD制作
- ゲームルール変更
- 新規コンテンツ追加

を容易にした。


---

## Event System

Unreal Engine 1ではイベント駆動型設計を採用した。

例:

Trigger

↓

Event Dispatch

↓

Actor Response



マップ上のイベント制御をスクリプトで柔軟に定義できた。


---

## State System

Actorは状態管理機構を持ち、
状況に応じた処理切り替えを可能にした。


例:

Enemy

├── Idle
├── Patrol
├── Attack
└── Dead



この仕組みは後のUnrealScript設計にも大きな影響を与えた。


---

# Package System

Unreal Engine 1では、
ゲームデータをPackage単位で管理した。

管理対象:

- Map
- Texture
- Sound
- Mesh
- Script

Package

├── Classes
├── Textures
├── Sounds
├── Meshes
└── Objects



このデータ管理方式は、
後のUnreal Engineシリーズにも継承された。


---

# Networking Architecture

Unreal Engine 1は、
初期段階からマルチプレイヤー対応を考慮して設計された。

主な機能:

- Client / Server Model
- Actor Replication
- Network Events


特にActor単位で状態同期を行う設計は、
後のUnreal Engineシリーズのネットワークシステムの基礎となった。


---

# Editor Architecture

## UnrealEd

UnrealEdはUnreal Engine 1の重要な構成要素である。

特徴:

- レベル編集
- BSP構築
- Actor配置
- Lighting設定
- Script連携

UnrealEd

├── Level Editor
├── BSP Builder
├── Actor Browser
├── Texture Browser
└── Script Integration



エンジンと編集環境を統合する思想は、
現在のUnreal Editorへと継承された。


---

# Legacy Architecture

Unreal Engine 1で確立された設計思想は、
後続バージョンへ継承された。


|UE1|後継|
|-|-|
|Actor System|Actor / UObject Framework|
|UnrealScript|Blueprint / Gameplay Framework|
|Package System|Asset System|
|UnrealEd|Unreal Editor|
|BSP World|Level System|


---

# Summary

Unreal Engine 1は、
現代的なゲームエンジン設計の基礎となる多くの概念を初めて統合した。

特に、

- Actor中心のゲームオブジェクト管理
- UnrealScriptによる拡張性
- UnrealEdによる統合開発環境
- Packageによるデータ管理

は、その後20年以上続くUnreal Engineシリーズの基盤となった。

Unreal Engine 1は、Epic Gamesにおけるゲームエンジン開発の原点であり、
現代のUnreal Engineへ続くアーキテクチャ思想の出発点である。


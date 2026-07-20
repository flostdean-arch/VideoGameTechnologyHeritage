# Unreal Engine 1

## 概要

Unreal Engine 1は、Epic MegaGames（現 Epic Games）が開発した初代Unreal Engineであり、
1998年に発売された『Unreal』で初めて採用されたゲームエンジンである。

当時としては高度な3Dレンダリング技術、リアルタイムライティング、BSPベースの
ワールド構築、独自スクリプト言語「UnrealScript」などを備え、
後のUnreal Engineシリーズに続く基本設計思想を確立した。

Unreal Engine 1は単なるゲームタイトル向けの内部エンジンではなく、
ゲーム世界の構築・編集・拡張を重視した汎用ゲームエンジンとして設計され、
現在のUnreal Engineに続く「エディタ中心」「オブジェクト指向型ゲーム開発」
という方向性の原点となった。


## 基本情報

|項目|内容|
|-|-|
|開発元|Epic MegaGames（現 Epic Games）|
|初公開|1998年|
|初採用タイトル|Unreal|
|代表タイトル|Unreal / Unreal Tournament|
|対応プラットフォーム|Windows / Linux / Macintosh / PlayStation 2 など|
|主な技術|BSP Rendering / UnrealScript / Actor System|
|後継エンジン|Unreal Engine 2|


## 歴史

Unreal Engine 1は、Epic MegaGamesが長年開発してきたゲーム技術を統合した
初の大規模3Dゲームエンジンである。

1998年に発売された『Unreal』では、当時としては革新的だった
高品質なテクスチャ表現、複雑な3D環境表現、動的なライティングなどを実現した。

その後、『Unreal Tournament』向けに改良が加えられ、
ネットワーク対戦機能やパフォーマンス改善などが行われた。

Unreal Engine 1で確立された設計思想は、Unreal Engine 2以降にも引き継がれ、
現在のUnreal Engineシリーズの基礎となっている。


## 主な特徴

### BSPベースのレベル構築

Unreal Engine 1では、BSP（Binary Space Partitioning）を利用した
ワールド構築システムを採用した。

これにより、3D空間をリアルタイムで編集しながら、
効率的なレンダリングと衝突判定を実現した。

UnrealEdによるレベル編集環境は、後のUnreal Engineシリーズにおける
統合型ゲーム開発環境の原型となった。


### UnrealScript

Unreal Engine 1では、ゲームロジック制御のために
独自スクリプト言語「UnrealScript」が導入された。

C++によるエンジン部分と、スクリプトによるゲーム部分を分離することで、
開発者やMOD制作者がエンジン内部を変更せずにゲーム拡張を行える設計となった。


### Actor System

ゲーム内のオブジェクトはActorを基本単位として管理された。

プレイヤー、敵キャラクター、武器、アイテム、イベントオブジェクトなど、
ゲーム世界を構成する要素を統一的なオブジェクトモデルで扱う設計は、
後のUnreal Engineシリーズでも継承されている。


### UnrealEd

Unreal Engine 1には専用レベルエディタ「UnrealEd」が搭載された。

ゲームエンジン、レベルエディタ、スクリプト環境を統合する開発思想は、
現在のUnreal Engine Editorへと発展していった。


## 技術構成
Unreal Engine 1

├── Core Systems
│ ├── Object System
│ ├── Actor System
│ └── Package System
│
├── Rendering
│ ├── BSP Renderer
│ ├── Software Renderer
│ ├── Glide Renderer
│ └── Direct3D Renderer
│
├── Gameplay
│ ├── UnrealScript
│ ├── Event System
│ └── State System
│
├── Networking
│ └── Multiplayer Framework
│
└── Tools
└── UnrealEd



## 採用タイトル

### Unreal

Unreal Engine 1が初めて採用されたタイトル。

広大な3D環境、高品質なグラフィックス、没入型の世界設計によって、
当時のPCゲーム市場に大きな影響を与えた。


### Unreal Tournament

Unreal Engine 1をベースにネットワーク対戦向けに改良された作品。

高速なマルチプレイヤーFPSとして成功し、
Unreal Engineの技術力と拡張性を広く示した。


## 後世への影響

Unreal Engine 1で確立された以下の設計思想は、
後続エンジンへ継承された。

- エディタ中心のゲーム開発
- オブジェクト指向型ゲーム構造
- スクリプトによるゲームロジック制御
- MOD開発を意識した拡張性
- 統合型ゲーム制作環境


Unreal Engine 1は、単なる1990年代後半のゲームエンジンではなく、
現在のUnreal Engineシリーズへ続く技術体系の出発点として、
ゲームエンジン史において重要な位置を占めている。


## 関連資料

- Architecture.md
- CoreTechnologies/
- Technologies/
- Editor/
- Games/
- Legacy/
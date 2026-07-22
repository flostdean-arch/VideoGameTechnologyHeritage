# Unreal Engine 1 History

## 概要

Unreal Engine 1 は、Epic MegaGames（後の Epic Games）が開発した初代 Unreal Engine であり、1998 年発売の『Unreal』とともに初めて公開されたゲームエンジンです。

当時主流であった『DOOM』や『Quake』の技術を発展させながら、オブジェクト指向設計、スクリプト言語、ネットワーク機能、リアルタイムライティングなど、後のゲームエンジンの基礎となる数多くの技術を導入しました。

約10年にわたり改良が続けられ、多くのゲームで採用されたほか、後継である Unreal Engine 2・3・4・5 の設計思想にも大きな影響を与えています。

---

# 開発の背景

1990年代前半、FPSゲーム市場では id Software が『DOOM』『Quake』によって大きな成功を収めていました。

Epic MegaGames は次世代FPS『Unreal』の開発を開始し、それに合わせて独自のゲームエンジンを設計しました。

開発当初から以下のような目標が掲げられていました。

- 高品質な3Dグラフィックス
- 広大な屋内・屋外マップ
- 柔軟なゲームロジック
- マルチプレイヤーへの対応
- MOD制作を前提とした設計

これらは当時としては非常に先進的な思想であり、現在のゲームエンジンにも通じる設計となっています。

---

# Unreal (1998)

1998年、『Unreal』の発売とともに Unreal Engine 1 が正式に公開されました。

初期バージョンでは以下の特徴を備えていました。

- BSPベースのマップ構築
- Software Renderer
- Glideレンダラー
- Direct3Dレンダラー
- OpenGLレンダラー（後期）
- UnrealScript
- UnrealEd
- パッケージシステム
- ネットワークマルチプレイ

当時としては非常に高品質なライティングや広大なステージ構成を実現し、高い評価を受けました。

---

# Unreal Tournament (1999)

1999年発売の『Unreal Tournament』では、エンジンがさらに成熟しました。

主な改良点は以下のとおりです。

- ネットワーク性能の向上
- Replication機能の強化
- AIボットの改善
- UnrealScriptの機能拡張
- エディタ機能の改善
- MOD制作環境の充実

『Unreal Tournament』はMOD文化の発展にも大きく貢献し、多くのユーザー製コンテンツが制作されました。

---

# ライセンス展開

Unreal Engine 1 は Epic Games 以外の多くの開発会社へライセンス提供されました。

代表的な採用作品には以下があります。

- Unreal
- Return to Na Pali
- Unreal Tournament
- Deus Ex
- Rune
- Wheel of Time
- Harry Potter and the Sorcerer's Stone
- Harry Potter and the Chamber of Secrets
- Clive Barker's Undying

これらの作品ごとにエンジンは独自の拡張が行われ、UE1は長期間にわたって進化を続けました。

---

# Unreal Engine 2への発展

2002年頃になると Unreal Engine 2 が登場します。

UE2では、

- Static Mesh
- Karma Physics
- Terrain System
- 改良されたAnimation System
- DirectX 8世代への対応

など、多くの新技術が導入されました。

一方で、

- UnrealScript
- Package System
- Actorシステム
- Replication
- UnrealEd

などの基本設計は UE1 を継承しています。

---

# 技術的な特徴

Unreal Engine 1 は、当時としては画期的な数多くの技術を採用していました。

## オブジェクト指向設計

ゲーム内のほぼすべての要素が Object・Actor クラスを中心として設計されました。

この思想は現在の Unreal Engine 5 に至るまで受け継がれています。

## UnrealScript

ゲームロジックをスクリプトで記述できる仕組みを採用しました。

エンジン本体とゲームロジックを分離することで、高い拡張性を実現しました。

## Package System

マップ、テクスチャ、音声、音楽などをパッケージとして管理する仕組みを採用しました。

このシステムは後の Unreal Engine シリーズでも長く利用されました。

## Networking

クライアント・サーバー方式によるマルチプレイヤーを標準でサポートしました。

Replication システムにより、ゲームオブジェクトの同期を効率的に行うことができました。

## UnrealEd

ゲーム開発者だけでなく、MOD制作者にも公開された高機能なレベルエディタです。

後の Unreal Editor の原型となりました。

---

# Unreal Engine史における位置付け

Unreal Engine 1 は、単なるゲームエンジンではなく、現在の Unreal Engine シリーズの原点となる存在です。

後継となる Unreal Engine 2・3・4・5 ではレンダリング技術や物理演算などが大きく進化しましたが、

- Objectシステム
- Actorシステム
- UnrealScript（後のBlueprintへ繋がる思想）
- Package管理
- Editor中心の開発環境
- ネットワーク設計

といった基本思想は UE1 の時代に確立されました。

現在でも Unreal Engine の歴史を理解する上で、最も重要なゲームエンジンの一つとして位置付けられています。

---

# 関連項目

- README.md
- Architecture.md
- Runtime/
- Rendering/
- UnrealScript/
- Packages/
- Networking/
- Editor/
- Games/

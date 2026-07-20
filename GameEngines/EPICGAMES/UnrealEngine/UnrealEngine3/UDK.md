# UDK (Unreal Development Kit)

## 概要

UDK（Unreal Development Kit）は、Epic Gamesが公開したUnreal Engine 3ベースの無料開発環境です。

2009年に公開され、Unreal Engine 3の技術を一般開発者や学生、インディーゲーム開発者が利用できる形で提供しました。

UDKは商用版Unreal Engine 3そのものではありませんが、UnrealEd、UnrealScript、Kismetなど、UE3世代を代表する開発技術を体験できる環境として重要な役割を果たしました。

---

# 開発背景

Unreal Engine 3は、主にAAAタイトル向けの商用ゲームエンジンとして提供されていました。

しかし、Epic Gamesはゲームエンジン技術の普及を目的として、UE3の一部機能を利用できる無料開発環境としてUDKを公開しました。

これにより、

- 学習用途
- 学生向け教育
- インディーゲーム開発
- 技術研究

などでUE3技術へ触れる機会が広がりました。

---

# 基本情報

|項目|内容|
|-|-|
|名称|Unreal Development Kit|
|略称|UDK|
|開発元|Epic Games|
|ベースエンジン|Unreal Engine 3|
|公開開始|2009年|
|提供終了|2015年頃|
|主な対象|PC向けゲーム開発|

---

# 構成技術

UDKは、UE3の主要な開発環境を含んでいました。

## UnrealEd

UE3標準のレベルエディタ。

主な機能：

- BSP編集
- Static Mesh配置
- Terrain編集
- Lighting設定
- Material設定

UEシリーズの開発ワークフローの中心となるツールです。

---

## UnrealScript

UE3世代で使用されたゲームロジック用スクリプト言語。

特徴：

- オブジェクト指向設計
- Actorベースシステム
- ネットワーク同期対応

UE4以降ではBlueprintとC++へ移行しましたが、UE3以前のゲームロジック設計を理解する上で重要な技術です。

---

## Kismet

ノードベースのビジュアルスクリプティングシステム。

用途：

- イベント制御
- ギミック作成
- ステージ演出
- ゲームフロー制御

後のBlueprint Visual Scriptingへ大きな影響を与えました。

---

## Matinee

カットシーンやイベント演出を作成するためのツール。

用途：

- カメラ演出
- キャラクターアニメーション制御
- シネマティックイベント

UE4以降のSequencerへ発展しました。

---

## Cascade

パーティクルエフェクト作成ツール。

用途：

- 爆発
- 炎
- 煙
- 魔法エフェクト

UE4でも継続して採用されました。

---

# UDKによる開発ワークフロー

一般的なUE3開発では以下の流れで制作が行われました。

```text
Asset作成
    │
    ▼
UnrealEdへインポート
    │
    ▼
Material設定
    │
    ▼
Level制作
    │
    ▼
Kismet / UnrealScriptによる制御
    │
    ▼
ビルド・実行
```

---

# UDKの技術的意義

UDKは、ゲームエンジンが「企業向けの専用技術」から「一般開発者が学習できる技術」へ広がる過程で重要な存在でした。

特に、

- UnrealScript
- Kismet
- UnrealEd
- Material System
- Cascade

などは、後のUnreal Engine 4へ受け継がれる設計思想の基礎となっています。

---

# 終了と現在の状況

UDKは現在、Epic Gamesによる公式配布が終了しています。

また、Unreal Engine 3自体も現行開発環境として利用されることはなくなり、新規開発で使用されることはほぼありません。

現在では、

- 過去作品の研究
- ゲームエンジン史の調査
- 技術資料の保存
- 旧世代開発環境の研究

を目的として扱われています。

---

# Unreal Engine 4への影響

UDKで培われた技術や設計思想は、UE4へ多く継承されました。

| UDK / UE3 | UE4 |
|-|-|
| Kismet | Blueprint |
| UnrealScript | C++ + Blueprint |
| Matinee | Sequencer |
| Cascade | Cascade（継続） |
| UnrealEd | Unreal Editor |

---

# 関連項目

- [Unreal Engine 3](./README.md)
- [UnrealScript](./UnrealScript.md)
- [Kismet](./Kismet.md)
- [Rendering](./Rendering.md)

---

# 参考資料

- Epic Games Unreal Engine Documentation
- Unreal Developer Network（UDN）
- Unreal Engine 3関連アーカイブ資料
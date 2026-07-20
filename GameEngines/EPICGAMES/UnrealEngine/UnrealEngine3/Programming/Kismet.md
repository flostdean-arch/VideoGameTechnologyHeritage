# Kismet

## 概要

Kismetは、Unreal Engine 3に搭載されたビジュアルスクリプティングシステムです。

ノードを接続することでゲーム内イベントやレベル制御を作成でき、プログラミングを専門としないレベルデザイナーやアーティストでもゲーム演出を構築できる環境を提供しました。

UE3におけるKismetは、後のUnreal Engine 4に搭載されたBlueprint Visual Scriptingへ大きな影響を与えた技術です。

---

# 開発背景

Unreal Engine 3では、ゲームロジックの実装にUnrealScriptが利用されていました。

しかし、すべての処理をプログラマーが担当すると、

- レベル制作の速度低下
- 演出調整の難化
- デザイナー側での試行錯誤が困難

という問題が発生します。

そこで、レベルデザイナーが直接イベント制御を行える仕組みとしてKismetが導入されました。

---

# 役割

Kismetは主に以下のような処理に利用されました。

- レベルイベント
- カットシーン制御
- オブジェクト制御
- トリガー処理
- ゲーム進行制御
- 演出制御

---

# 基本構造

Kismetでは、処理をノードとして配置し、それらを接続して動作を定義します。

基本的な構成：

```text
Event Node

    │

    ▼

Action Node

    │

    ▼

Output / Control Node
```

例：

```text
プレイヤー接近

      ↓

Trigger発動

      ↓

ドアを開く

      ↓

ライト演出開始
```

---

# 主なノード

## Event Node

処理開始の条件を定義します。

例：

- Level Loaded
- Player Spawn
- Trigger Activated
- Object Destroyed

---

## Action Node

実際の処理を実行します。

例：

- 移動
- 回転
- 表示変更
- サウンド再生
- アニメーション制御

---

## Variable Node

ゲーム内データを扱います。

例：

- Actor参照
- 数値
- Boolean
- Object Reference

---

# UnrealScriptとの関係

KismetとUnrealScriptは競合するものではなく、用途によって使い分けられていました。

```text
UnrealScript

├── 複雑なゲームシステム
├── AI
├── 武器処理
├── ネットワーク処理
└── Gameplay Logic


Kismet

├── イベント制御
├── レベル演出
├── ギミック制御
└── シーケンス処理
```

例えば、

- 敵AI → UnrealScript
- 扉が開く演出 → Kismet
- ボス戦開始イベント → Kismet + UnrealScript

という組み合わせが一般的でした。

---

# Matineeとの連携

KismetはMatineeと連携することで、高度なカットシーンや演出を作成できました。

例：

```text
Player Trigger

      ↓

Kismet

      ↓

Matinee開始

      ↓

カメラ演出

      ↓

キャラクターアニメーション
```

これにより、ゲーム内イベントや映画的演出をプログラムを書かずに構築できました。

---

# Unreal Engine 3での利用例

Kismetは多くのUE3タイトルで利用されました。

用途：

- ストーリーイベント
- ボス戦開始処理
- ステージギミック
- ムービー演出
- インタラクション処理

特に大型タイトルでは、レベルデザイナーがゲーム進行を調整するための重要なツールでした。

---

# Blueprintへの影響

Unreal Engine 4では、Kismetの思想を発展させたBlueprint Visual Scriptingが導入されました。

比較：

| UE3 | UE4 |
|-|-|
| Kismet | Blueprint |
| Sequence | Blueprint Graph |
| Action Node | Blueprint Node |
| Variable Node | Blueprint Variable |

BlueprintではKismetよりも広範囲の処理が可能になり、ゲームプレイロジックそのものを構築できる環境へ発展しました。

---

# 技術的意義

Kismetは、ゲーム開発における「プログラマー以外でもロジックを構築できる環境」の先駆けとなりました。

影響：

- レベルデザイナーの作業範囲拡大
- 開発効率向上
- ビジュアルスクリプティング普及
- Blueprintへの発展

---

# 現在の研究環境

★★★☆☆

UE3およびUDKの公式配布は終了しています。

現在Kismetを利用するには、

- 既存UDK環境
- UE3採用タイトルの解析
- 保存された開発資料

などを利用する必要があります。

---

# 関連項目

- [Unreal Engine 3](./README.md)
- [UDK](./UDK.md)
- [UnrealScript](./UnrealScript.md)
- [Matinee](./Matinee.md)

---

# 参考資料

- Epic Games Unreal Engine 3 Documentation
- Unreal Developer Network（UDN）
- UDK Documentation Archive
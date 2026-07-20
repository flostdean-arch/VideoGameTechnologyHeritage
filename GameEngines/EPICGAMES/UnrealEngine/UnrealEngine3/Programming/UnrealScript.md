# UnrealScript

## 概要

UnrealScriptは、Epic GamesがUnreal Engineシリーズ向けに開発したゲームスクリプト言語です。

Unreal Engine 1から導入され、Unreal Engine 3ではゲームプレイロジックを実装する主要な開発手段として利用されました。

UE3におけるUnrealScriptは、単なるスクリプト言語ではなく、Unreal Engine独自のオブジェクトシステムと密接に結び付いたゲーム開発用言語として設計されています。

---

# UE3における役割

Unreal Engine 3では、エンジン内部の低レベル処理をC++で実装し、ゲーム固有の処理をUnrealScriptで記述する構成が一般的でした。

```text
C++ Engine Layer

        │

        ▼

UnrealScript Gameplay Layer

        │

        ▼

Game Logic / AI / UI / Events
```

主な用途：

- キャラクター制御
- 武器・アイテム処理
- AI制御
- ゲームルール
- UI処理
- イベント制御

---

# 開発背景

Unreal Engineでは、ゲームごとに頻繁に変更される処理を、エンジン本体を再コンパイルせずに変更できる仕組みが必要でした。

UnrealScriptはそのために設計され、

- 開発速度の向上
- ゲームデザイナーによる調整
- Mod開発支援

を目的として導入されました。

---

# 設計思想

UnrealScriptは、一般的なプログラミング言語とは異なり、Unreal Engineの内部構造を前提に設計されています。

特徴：

- オブジェクト指向
- Classベース設計
- Unreal Object Systemとの統合
- Actor中心のゲーム設計
- ネットワーク同期対応

---

# Actorシステム

UE3では、ゲーム世界に存在する多くの要素がActorとして管理されます。

例：

- プレイヤーキャラクター
- 敵キャラクター
- 武器
- アイテム
- トリガー
- エフェクト

```text
Actor

 ├── Pawn
 │     └── Character
 │
 ├── Weapon
 │
 ├── Trigger
 │
 └── Item
```

UnrealScriptは、このActorを拡張することでゲーム要素を作成します。

---

# Class構造

UnrealScriptではClassを継承することで機能を拡張します。

例：

```text
Actor

 └── Pawn

       └── Character

             └── PlayerCharacter
```

ゲーム固有の処理は既存Classを継承して作成する方式が基本でした。

---

# 主な機能

## Eventシステム

UnrealScriptではイベント駆動型の処理が多く利用されました。

例：

- BeginPlay
- Tick
- Collision Event
- Input Event

ゲーム状態の変化に応じた処理を記述できます。

---

## Replication

UE3ではネットワークゲームを重視しており、UnrealScriptにはReplication機能が組み込まれていました。

用途：

- プレイヤー位置同期
- 武器状態同期
- ゲームルール同期

Unreal Engineのマルチプレイヤー設計を支える重要な仕組みでした。

---

## Garbage Collection

UnrealScriptはUnreal Object Systemと統合されており、独自のメモリ管理機構を利用していました。

これにより、

- オブジェクト参照管理
- 不要オブジェクト削除
- 安全なゲームオブジェクト管理

を実現しました。

---

# UDKでの利用

UDKではUnrealScriptを利用して、一般開発者もUE3ベースのゲーム制作を行うことができました。

利用例：

- Gameplay Class作成
- 武器システム
- AI制御
- UI制御
- Mod制作

UDKはUnrealScriptを学習できる貴重な公式環境でした。

---

# Kismetとの関係

UE3では、プログラマー向けのUnrealScriptとは別に、レベルデザイナー向けのビジュアルスクリプト環境としてKismetが存在しました。

関係：

```text
UnrealScript

  ↓

複雑なゲームロジック
システム処理
AI制御


Kismet

  ↓

イベント制御
ステージ演出
簡易ゲームフロー
```

Kismetは後のBlueprint Visual Scriptingへ大きな影響を与えました。

---

# UE4への移行

Unreal Engine 4ではUnrealScriptは廃止されました。

代わりに、

- C++
- Blueprint Visual Scripting

という構成へ移行しました。

技術的な思想は完全に失われたわけではなく、

| UE3 | UE4 |
|-|-|
| UnrealScript | C++ |
| UnrealScript Class | UObject/C++ Class |
| Kismet | Blueprint |
| Script Actor | Blueprint Actor |

という形で発展しています。

---

# 技術的意義

UnrealScriptは、ゲームエンジンに組み込まれた専用スクリプト言語の代表例でした。

その設計思想は、

- ゲームロジックとエンジン部分の分離
- 高速なゲーム開発
- Mod文化の促進
- デザイナーとプログラマーの協調

に大きな影響を与えました。

---

# 現在の研究環境

★★★☆☆

UnrealScriptを利用できる公式環境であるUDKは現在配布終了しています。

現在では、

- 既存資料
- ソースコード解析
- 過去作品のMod環境
- アーカイブ

などを通じた研究が中心となっています。

---

# 関連項目

- [Unreal Engine 3](./README.md)
- [UDK](./UDK.md)
- [Kismet](./Kismet.md)
- [Networking](./Networking.md)

---

# 参考資料

- Epic Games Unreal Engine 3 Documentation
- Unreal Developer Network（UDN）
- UDK Documentation Archive
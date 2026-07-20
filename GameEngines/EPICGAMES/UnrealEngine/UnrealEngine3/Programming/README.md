# Programming

## 概要

`Programming/` は、Unreal Engine 3（UE3）におけるゲームロジック制作・制御システムを扱うカテゴリです。

UE3では、プログラマー向けのUnrealScriptと、デザイナー向けのビジュアルスクリプト環境であるKismetを組み合わせることで、大規模なゲーム開発に対応しました。

この設計思想は、後のUnreal Engine 4におけるBlueprintへ発展しています。

---

# 対象技術

現在、このカテゴリでは以下の技術を扱います。

| 技術 | 内容 |
|---|---|
| UnrealScript | UE3標準ゲームプログラミング言語 |
| Kismet | ノードベースのイベント制御システム |

---

# 技術構成

UE3では、コードとビジュアル制御を組み合わせてゲームを構築します。

```text
              Gameplay Logic

                    │

        ┌───────────┴───────────┐

        ▼                       ▼

 UnrealScript              Kismet

 (Code)              (Visual Script)

        │                       │

        └───────────┬───────────┘

                    ▼

              Unreal Engine 3
```

---

# UnrealScript

## 概要

UnrealScriptは、Unreal Engine 3で使用されたゲーム開発向けスクリプト言語です。

C++によるエンジン内部処理と、ゲーム固有のロジックを分離する目的で設計されました。

主な用途：

- キャラクター制御
- 武器処理
- AI制御
- ゲームルール
- イベント処理

→ [UnrealScript](./UnrealScript.md)

---

# Kismet

## 概要

Kismetは、UE3に搭載されたノードベースのビジュアルスクリプトシステムです。

プログラムコードを書かずに、ゲームイベントやレベルギミックを構築できます。

用途：

- ドア開閉
- イベント開始
- カットシーン制御
- トリガー処理

→ [Kismet](./Kismet.md)

---

# UnrealScriptとKismetの関係

UE3では、両者は競合するものではなく役割分担されていました。

```text
UnrealScript

↓

複雑なゲームシステム

↓

Kismet

↓

レベルイベント・演出制御
```

例：

敵AI：

```
UnrealScript
```

イベント発生：

```
Kismet
```

カットシーン：

```
Kismet + Matinee
```

---

# 開発ワークフロー

UE3での一般的な開発では、

```text
Engine Code

      ↓

UnrealScript

      ↓

Kismet Event Setup

      ↓

Level Integration

      ↓

Testing
```

という流れでゲームを構築しました。

---

# Editorとの関係

Programmingカテゴリの技術は、UnrealEdと密接に統合されています。

```text
UnrealEd

 ├── UnrealScript Editor

 ├── Kismet Editor

 └── Level Editor
```

コード、イベント、レベル制作を同じ環境で管理できます。

---

# 後世代への継承

UE4では、UnrealScriptは廃止され、Blueprintへ統合されました。

技術の流れ：

```text
UnrealScript

        ↓

Kismet

        ↓

Blueprint
```

比較：

| UE3 | UE4 / UE5 |
|-|-|
| UnrealScript | C++ |
| Kismet | Blueprint |
| UnrealEd Integration | Unreal Editor |

UE3で培われた「プログラマーとデザイナーが同じ環境で開発する」という思想は現在も継承されています。

---

# 技術的意義

UE3 Programming Systemは、ゲーム開発における役割分担を大きく変化させました。

影響：

- デザイナー主体のゲーム制作
- ビジュアルスクリプト普及
- GameplayとEngineの分離
- Blueprintへの発展

---

# 関連項目

- [UnrealScript](./UnrealScript.md)
- [Kismet](./Kismet.md)
- [Core](../Core/README.md)
- [Production](../Production/README.md)

---

# 参考資料

- Epic Games Unreal Engine Documentation
- Unreal Developer Network（UDN）
- UDK Documentation Archive
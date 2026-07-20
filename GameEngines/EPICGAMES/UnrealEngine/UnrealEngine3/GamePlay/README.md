# Gameplay

## 概要

`Gameplay/` は、Unreal Engine 3（UE3）におけるゲームプレイを構成する主要システムを扱うカテゴリです。

UE3では、単なる描画エンジンではなく、物理演算、ネットワーク通信、キャラクター制御などを統合した総合ゲームエンジンとして発展しました。

このカテゴリでは、プレイヤー操作やゲーム世界の挙動を支える技術について記録します。

---

# 対象技術

現在、このカテゴリでは以下の技術を扱います。

| 技術 | 内容 |
|---|---|
| Physics | 物理演算・衝突判定・Ragdoll |
| Networking | マルチプレイヤー通信システム |
| Animation System | キャラクターアニメーション制御 |

---

# 技術構成

UE3のGameplay Systemは、複数のシステムが連携して動作します。

```text
                 Gameplay

                     │

 ┌───────────────────┼───────────────────┐

 ▼                   ▼                   ▼

Physics          Networking        Animation

物理制御          通信制御          キャラクター制御


                     │

                     ▼

              Game Logic
```

---

# Physics

## 概要

Physics Systemは、ゲーム世界内の物理挙動を管理するシステムです。

主な機能：

- Collision
- Rigid Body Physics
- Constraint
- Ragdoll

など。

ゲーム内オブジェクトの自然な動きを実現します。

→ [Physics](./Physics.md)

---

# Networking

## 概要

Networking Systemは、オンラインゲーム向けの通信処理を担当します。

UE3では、クライアント・サーバー方式を中心としたネットワーク設計を採用しました。

対象：

- Player同期
- Actor同期
- Replication
- Online機能

など。

→ [Networking](./Networking.md)

---

# Animation System

## 概要

Animation Systemは、キャラクターや動的オブジェクトの動きを制御します。

主要技術：

- Skeletal Mesh
- AnimSet
- AnimTree
- Animation Blend

など。

後のUE4 Animation Blueprintへ繋がる重要なシステムです。

→ [Animation System](./AnimationSystem.md)

---

# Actor Systemとの関係

UE3では、Gameplayの中心にActor Systemがあります。

```text
Actor

├── Character

├── Vehicle

├── Physics Object

└── Interactive Object
```

各Gameplay SystemはActorを通じて連携します。

---

# PhysicsとAnimationの連携

キャラクター表現では、PhysicsとAnimationを切り替えて利用します。

通常：

```text
Animation

      ↓

Character Movement
```

死亡時：

```text
Physics Simulation

      ↓

Ragdoll
```

という流れになります。

---

# NetworkingとGameplay

オンラインゲームでは、Gameplay状態をネットワーク同期します。

例：

```text
Player Action

      ↓

Server

      ↓

Replication

      ↓

Client Update
```

UE3では、Actor単位で同期する設計が採用されました。

---

# Editorとの関係

Gameplay SystemはUnrealEd上で設定できます。

例：

- Physics設定
- Collision設定
- Animation設定
- Network設定

など。

```text
UnrealEd

      ↓

Actor Setup

      ↓

Gameplay System
```

---

# Programmingとの関係

Gameplay Systemはコード・スクリプトによって制御されます。

```text
UnrealScript

        ↓

Gameplay Logic

        ↓

Physics / Animation / Network
```

Kismetによるイベント制御とも連携します。

---

# 技術的意義

UE3 Gameplay Systemは、ゲームエンジンに必要なリアルタイムシミュレーション機能を統合しました。

影響：

- AAAタイトル向けゲームシステム
- オンラインゲーム対応
- 高度なキャラクター表現
- リアルタイム物理表現

---

# 後世代への継承

UE4・UE5では、UE3のGameplay設計をさらに発展させています。

| UE3 | UE4/UE5 |
|-|-|
| Physics System | Chaos Physics |
| Replication | Replication System |
| AnimTree | Animation Blueprint |
| Skeletal Mesh | Skeletal Mesh |

特にAnimation SystemとNetworking Systemは、現在のUnreal Engineでも重要な基盤となっています。

---

# 関連項目

- [Physics](./Physics.md)
- [Networking](./Networking.md)
- [Animation System](./AnimationSystem.md)
- [Programming](../Programming/README.md)
- [Rendering](../Rendering/README.md)

---

# 参考資料

- Epic Games Unreal Engine Documentation
- Unreal Developer Network（UDN）
- UDK Documentation Archive
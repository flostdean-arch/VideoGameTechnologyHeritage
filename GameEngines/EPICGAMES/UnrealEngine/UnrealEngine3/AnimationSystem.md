# Animation System

## 概要

Unreal Engine 3（UE3）のAnimation Systemは、キャラクターや動的オブジェクトのアニメーションを管理するためのシステムです。

UE3では、Skeletal Mesh、AnimSet、AnimTreeなどの技術を組み合わせることで、高度なキャラクターアニメーションを実現しました。

この設計は後のUnreal Engine 4・Unreal Engine 5におけるAnimation BlueprintやControl Rigなどの基礎となっています。

---

# 開発背景

ゲームキャラクターの表現が高度化するにつれ、単純なモデル切り替えではなく、リアルタイムで動きを制御する仕組みが必要になりました。

特にHDゲーム世代では、

- 滑らかなモーション
- 状況に応じた動作変化
- 武器や装備への対応
- 表情や演技表現

などが求められました。

UE3では、これらに対応するため高度なSkeletal Animation Systemが導入されました。

---

# Skeletal Mesh

UE3では、キャラクター表現にSkeletal Meshが利用されます。

Skeletal Meshは、

- 頂点情報
- ボーン構造
- ウェイト情報
- アニメーションデータ

を組み合わせて動作します。

構造：

```text
Skeletal Mesh

├── Mesh Data
│
├── Skeleton
│
├── Bone
│
└── Animation Data
```

---

# Bone System

キャラクターは複数のBone（ボーン）によって制御されます。

例：

```text
Root Bone

 ├── Spine

 │    ├── Arm

 │    └── Head

 └── Leg
```

各ボーンの変形によって、キャラクター全体の動きを表現します。

---

# AnimSet

AnimSetはアニメーションデータを管理する単位です。

含まれるもの：

- 歩行
- 走行
- 攻撃
- ジャンプ
- リロード
- 表情

など。

構造：

```text
AnimSet

├── Walk

├── Run

├── Jump

└── Attack
```

---

# AnimTree

AnimTreeは、複数のアニメーションを制御・合成するシステムです。

単純に1つのモーションを再生するのではなく、状態に応じてアニメーションを切り替えます。

例：

```text
Movement State

      ↓

AnimTree

      ↓

Walk / Run / Idle
```

---

# Animation Blend

UE3ではAnimation Blendによって、複数アニメーションを自然につなげることができます。

例：

```text
Idle

 ↓

50%

 ↓

Walk

 ↓

100%
```

急激な切り替えではなく、滑らかな遷移を実現します。

---

# Blend Space的な考え方

UE3ではUE4のBlend Spaceという名称はありませんでしたが、速度や方向によってアニメーションを制御する考え方は存在しました。

例：

```text
Speed

0       50       100

Idle --- Walk --- Run
```

この思想はUE4 Animation Blueprintへ発展します。

---

# Animation State管理

UE3では、キャラクター状態に応じてアニメーションを制御できます。

例：

```text
State

├── Idle

├── Walking

├── Running

├── Jumping

└── Attacking
```

ゲームロジックとAnimation Systemを連携させることで、自然なキャラクター制御が可能になります。

---

# Physics Assetとの連携

Animation SystemはPhysics Systemとも密接に関係しています。

通常：

```text
Animation Control
```

死亡時：

```text
Physics Simulation
```

へ切り替えることで、Ragdoll表現を実現します。

関連：

- Physics Asset
- Collision
- Ragdoll

---

# IK（Inverse Kinematics）

UE3では一部の用途でIK技術も利用されました。

用途：

- 足位置補正
- 武器位置調整
- キャラクター接地表現

など。

---

# Animation Compression

ゲームでは大量のアニメーションデータを扱うため、圧縮技術が重要になります。

UE3では、

- キーフレーム圧縮
- データ削減
- メモリ最適化

などによって大量モーションを扱いました。

---

# UnrealScriptとの関係

UE3ではUnrealScriptからAnimation制御を行うことができます。

例：

- アニメーション再生
- 状態変更
- Blend制御
- イベント発生

これによりGameplayとAnimationを連携できます。

---

# 制作ワークフロー

UE3での一般的な流れ：

```text
3D Model制作

      ↓

Skeletal Setup

      ↓

Animation Import

      ↓

AnimSet作成

      ↓

AnimTree構築

      ↓

Gameplay連携
```

---

# 技術的意義

UE3 Animation Systemは、現代的なキャラクターアニメーション制作環境の基礎を作りました。

影響：

- Skeletal Animation標準化
- アニメーション状態管理
- リアルタイムキャラクター制御
- Animation Blueprintへの発展

---

# UE4 / UE5への継承

UE4ではUE3のAnimation Systemをさらに発展させました。

比較：

| UE3 | UE4/UE5 |
|-|-|
| Skeletal Mesh | Skeletal Mesh |
| AnimSet | Animation Asset |
| AnimTree | Animation Blueprint |
| Blend System | Blend Space |
| Physics Asset | Physics Asset |

UE5ではさらに、

- Control Rig
- Motion Warping
- IK Rig

などへ発展しています。

---

# 現在の研究環境

★★★☆☆

UE3 Animation Systemを研究するには、

- UDK
- UE3開発環境
- 過去作品解析
- 技術資料

などが必要です。

---

# 関連項目

- [Unreal Engine 3](./README.md)
- [Physics](./Physics.md)
- [Material System](./MaterialSystem.md)
- [UnrealScript](./UnrealScript.md)

---

# 参考資料

- Epic Games Unreal Engine 3 Documentation
- Unreal Developer Network（UDN）
- UDK Documentation Archive
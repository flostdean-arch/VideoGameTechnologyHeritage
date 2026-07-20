# Physics

## 概要

Unreal Engine 3（UE3）のPhysics Systemは、ゲーム内の物理挙動を制御するための物理演算システムです。

UE3では、NVIDIA PhysXを採用することで、従来世代より高度なリアルタイム物理表現を実現しました。

物理演算は、キャラクター、車両、破壊表現、環境ギミックなど、現代的なゲーム表現を支える重要な要素となりました。

---

# 開発背景

Unreal Engine 2世代では、Karma Physicsなどによって基本的な物理演算が提供されていました。

しかしHDゲーム世代では、

- 大量オブジェクトの物理処理
- 車両挙動
- 破壊表現
- キャラクター物理
- 布や柔軟物表現

など、より高度な物理シミュレーションが求められるようになりました。

UE3では、これらに対応するためPhysXベースのPhysics Systemへ発展しました。

---

# PhysX採用

UE3では、NVIDIA PhysX SDKが採用されました。

PhysXは、

- リジッドボディ
- 衝突判定
- ジョイント
- 車両物理
- Cloth
- 破壊システム

などを提供します。

```text
Game Logic

      ↓

UnrealScript / Engine

      ↓

PhysX Simulation

      ↓

Physics Result

      ↓

Rendering
```

---

# Rigid Body Physics

UE3ではRigid Body Physicsによって、物体の現実的な挙動を再現できます。

対象：

- 箱
- 武器
- 瓦礫
- 小物
- 物理ギミック

例：

```text
Object

 ↓

Collision Detection

 ↓

Physics Calculation

 ↓

Movement Update
```

---

# Collision System

物理演算では、オブジェクト同士の衝突判定が重要になります。

UE3では、

- Collision Shape
- Physics Material
- Collision Channel

などを利用して衝突処理を管理します。

用途：

- 弾丸判定
- キャラクター移動
- 物理オブジェクト
- 環境判定

---

# Physics Asset

UE3ではキャラクター向けにPhysics Assetシステムが導入されました。

Physics Assetは、3Dモデルとは別に物理用ボーン構造を持たせる仕組みです。

```text
Character Mesh

        +

Physics Asset

        ↓

Ragdoll Simulation
```

用途：

- ラグドール
- 衝突判定
- 死亡時物理演算

など。

この仕組みはUE4・UE5にも継承されています。

---

# Ragdoll Physics

UE3ではキャラクター死亡時などにRagdoll Physicsが利用されました。

通常：

```text
Animation Control
```

↓

死亡時：

```text
Physics Simulation
```

へ切り替えることで、自然な倒れ方を表現できます。

---

# Vehicle Physics

UE3では車両向けPhysics Systemも提供されました。

用途：

- レーシングゲーム
- 戦車
- SFビークル
- 乗り物システム

車両では、

- タイヤ摩擦
- サスペンション
- 重量
- 加速度

などを物理計算します。

---

# Destructible Object

UE3では破壊可能オブジェクト表現にも対応しました。

例：

- 壁
- 建築物
- 障害物
- 瓦礫

物理破壊によって、固定された背景ではなく動的なゲーム環境を実現しました。

---

# Cloth Physics

UE3では布表現にも対応しています。

用途：

- キャラクター衣装
- 布
- フラッグ
- カーテン

など。

キャラクターアニメーションと組み合わせることで、より自然な動きを表現できます。

---

# PhysicsとGameplayの連携

UE3ではPhysicsは単独機能ではなく、Gameplayシステムと統合されています。

例：

```text
Player Action

      ↓

Physics Object

      ↓

Collision Event

      ↓

Gameplay Event
```

利用例：

- 物を押す
- 爆発で吹き飛ぶ
- 物理ギミックを解除する

---

# UnrealScriptとの関係

UE3ではUnrealScriptからPhysics状態を制御できます。

例：

- Physics Mode変更
- Collision設定
- Velocity制御
- Event取得

これにより、ゲームロジックと物理演算を連携できます。

---

# 採用タイトルでの利用

UE3 Physicsは、多くのAAAタイトルで利用されました。

例：

- Gears of Warシリーズ
- Batman: Arkhamシリーズ
- Mass Effectシリーズ
- Unreal Tournament 3

など。

---

# 技術的意義

UE3のPhysics Systemは、ゲームにおける物理表現を標準機能として普及させました。

影響：

- キャラクター物理
- 破壊表現
- 物理ギミック
- 車両システム
- 現代的ゲームデザイン

---

# UE4 / UE5への継承

UE4でもPhysXベースのPhysics Systemが継続利用されました。

比較：

| UE3 | UE4 |
|-|-|
| PhysX | PhysX |
| Physics Asset | Physics Asset |
| Ragdoll | Ragdoll |
| Vehicle System | Vehicle System |

その後、UE5ではChaos Physicsへ移行しています。

```text
Karma Physics

      ↓

PhysX

      ↓

Chaos Physics
```

---

# 現在の研究環境

★★★☆☆

UE3 Physicsを研究するには、

- UDK
- UE3採用タイトル
- 既存技術資料
- Mod環境

などが必要です。

公式開発環境は現在配布終了しています。

---

# 関連項目

- [Unreal Engine 3](./README.md)
- [UnrealScript](./UnrealScript.md)
- [Package System](./PackageSystem.md)
- [Rendering](./Rendering.md)

---

# 参考資料

- Epic Games Unreal Engine 3 Documentation
- Unreal Developer Network（UDN）
- NVIDIA PhysX Documentation
- UDK Documentation Archive
# Cascade

## 概要

Cascadeは、Unreal Engine 3（UE3）に搭載されたリアルタイムパーティクルエフェクト制作システムです。

炎、煙、爆発、魔法、光、環境エフェクトなど、ゲーム内で使用される視覚効果をノードベースではなくモジュール方式で構築することができます。

CascadeはUE3世代における標準的なエフェクト制作環境であり、後のUnreal Engine 4・Unreal Engine 5におけるNiagaraへと発展しました。

---

# 開発背景

3Dゲームの映像表現が高度化するにつれ、単純なモデルやテクスチャだけでは表現できない視覚効果が必要になりました。

例：

- 爆発
- 炎
- 煙
- 水しぶき
- 魔法エフェクト
- 粒子表現
- 環境演出

これらをリアルタイムで生成するため、UE3ではCascadeが導入されました。

---

# 基本概念

CascadeはParticle Systemを作成するためのエディタです。

基本構造：

```text
Particle System

      │

      ├── Emitter

      │       │

      │       ├── Spawn

      │       ├── Velocity

      │       ├── Size

      │       ├── Color

      │       └── Lifetime

      │

      └── Material
```

---

# Particle System

Particle Systemは、複数の小さな粒子（Particle）を制御してエフェクトを生成します。

粒子には、

- 位置
- 速度
- サイズ
- 色
- 寿命
- 回転

などの情報があります。

例：

```text
Explosion

Particle生成

      ↓

拡散

      ↓

消滅
```

---

# Emitter

Emitterは、Particleを生成・制御する単位です。

1つのParticle Systemに複数のEmitterを配置できます。

例：

```
Explosion Effect

├── Fire Emitter

├── Smoke Emitter

└── Spark Emitter
```

これにより複雑なエフェクトを構築できます。

---

# Module System

Cascadeの特徴はModule方式による編集です。

Emitterに対して機能単位のModuleを追加することで挙動を制御します。

例：

```text
Emitter

 ↓

Spawn Module

 ↓

Velocity Module

 ↓

Color Module

 ↓

Size Module
```

---

# 主なModule

## Spawn

粒子生成数を制御します。

設定例：

- 発生量
- 発生間隔
- ランダム生成

---

## Velocity

粒子の移動速度を制御します。

用途：

- 爆発の拡散
- 煙の上昇
- 炎の揺らぎ

---

## Lifetime

粒子の寿命を設定します。

例：

- 短時間の火花
- 長時間残る煙

---

## Size

粒子サイズを制御します。

用途：

- 大きな煙
- 小さな火花
- 光の粒

---

## Color

粒子カラーを制御します。

用途：

- 炎
- 魔法
- 発光表現

---

# Material Systemとの連携

CascadeはMaterial Systemと密接に連携します。

```text
Particle

    ↓

Material

    ↓

Shader

    ↓

Rendering
```

例えば、

- 発光する炎
- 半透明の煙
- 光る魔法粒子

などはMaterialと組み合わせて表現します。

---

# GPU Particle

UE3ではGPUを利用したParticle処理にも対応しました。

大量の粒子を効率的に処理することで、

- 爆発
- 大量の煙
- 雨
- 火花

など、より高度なエフェクトを実現しました。

---

# Physicsとの関係

CascadeはPhysics Systemとも組み合わせて利用されました。

例：

- 爆発エフェクト
- 衝撃表現
- 破壊時の粉塵
- 物理オブジェクトへの影響表現

```text
Physics Event

      ↓

Cascade Trigger

      ↓

Particle Effect
```

---

# Kismet・Matineeとの関係

Cascadeは他のUE3システムと連携します。

## Kismet

イベント発生時にエフェクトを開始。

```text
Trigger

 ↓

Kismet

 ↓

Cascade Effect
```

---

## Matinee

時間制御された演出で利用。

```text
Matinee

 ↓

Explosion Timing

 ↓

Cascade
```

---

# 制作ワークフロー

UE3では以下のような流れでエフェクトを制作しました。

```text
Concept

 ↓

Material Creation

 ↓

Cascade Setup

 ↓

Level配置

 ↓

Kismet連携

 ↓

Final Effect
```

---

# 技術的意義

Cascadeは、ゲームエンジン標準のリアルタイムエフェクト制作環境として大きな影響を与えました。

影響：

- アーティスト主体のエフェクト制作
- リアルタイムVFX制作
- AAAタイトル向け演出
- 後世代Particle System

---

# UE4 / UE5への継承

UE4ではCascadeが継続利用されました。

その後、UE4後期からUE5ではNiagaraへ移行しています。

系譜：

```text
Particle System

      ↓

Cascade

      ↓

Niagara
```

比較：

| UE3 | UE4/UE5 |
|-|-|
| Cascade | Niagara |
| Emitter | Emitter |
| Module | Module |
| Particle System | Niagara System |

Niagaraでは、

- GPU処理強化
- 大量粒子対応
- より柔軟な制御

へ発展しました。

---

# 現在の研究環境

★★★☆☆

UE3 Cascadeを利用するには、

- UDK
- UE3開発環境
- 過去プロジェクト

などが必要です。

現在では主に、技術資料や過去作品解析を通じて研究されています。

---

# 関連項目

- [Unreal Engine 3](./README.md)
- [Material System](./MaterialSystem.md)
- [Rendering](./Rendering.md)
- [Matinee](./Matinee.md)
- [Physics](./Physics.md)

---

# 参考資料

- Epic Games Unreal Engine 3 Documentation
- Unreal Developer Network（UDN）
- UDK Documentation Archive
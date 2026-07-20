# Matinee

## 概要

Matineeは、Unreal Engine 3（UE3）に搭載されたリアルタイムシネマティック制作システムです。

タイムライン形式でカメラ、キャラクター、オブジェクト、エフェクトなどを制御し、ゲーム内イベントやカットシーンを制作できます。

Matineeは、後のUnreal Engine 4に搭載されたSequencerへ発展した、Unreal Engineシリーズの映像演出システムの基礎となる技術です。

---

# 開発背景

ゲームの表現が高度化するにつれ、単純なイベント制御だけでは映画的な演出を作ることが困難になりました。

特にHDゲーム世代では、

- カメラワーク
- キャラクター演技
- 複雑なイベント
- リアルタイムムービー

などが求められるようになりました。

UE3では、これらをプログラムだけではなく、レベルデザイナーや演出担当者が編集できる環境としてMatineeが導入されました。

---

# 基本構造

Matineeはタイムラインベースで動作します。

```text
Timeline

0s ---------------------- 30s

Camera

Object

Animation

Effect

Sound
```

時間軸上にイベントや動きを配置することで、複雑な演出を作成します。

---

# UnrealEdとの統合

MatineeはUnrealEdに統合されています。

制作フロー：

```text
Level Design

      ↓

Matinee Sequence作成

      ↓

Actor配置

      ↓

Timeline編集

      ↓

ゲーム内再生
```

レベル編集と演出制作を同じ環境で行える点が特徴です。

---

# Camera制御

Matineeではカメラ演出を細かく制御できます。

制御可能な要素：

- カメラ位置
- 回転
- ズーム
- FOV
- カット切替

例：

```text
Camera A

 ↓

Character Close-up

 ↓

Camera B

 ↓

Wide Shot
```

映画的なカットシーン制作が可能になります。

---

# Actor制御

Matineeではゲーム内Actorを直接制御できます。

対象：

- キャラクター
- ドア
- エレベーター
- ギミック
- オブジェクト

例：

```text
Door Actor

0秒

閉じている

↓

5秒

開く

↓

10秒

停止
```

---

# Animation制御

キャラクターアニメーションとも連携できます。

用途：

- 会話イベント
- 演技
- ボス登場演出
- ストーリーイベント

---

# Kismetとの関係

MatineeはKismetと組み合わせて利用されます。

役割分担：

```text
Kismet

↓

イベント開始・条件制御


Matinee

↓

映像演出・時間制御
```

例：

```text
Player enters area

        ↓

Kismet Trigger

        ↓

Matinee Start

        ↓

Camera Sequence

        ↓

Character Animation
```

---

# UnrealScriptとの関係

MatineeはUnrealScriptから制御することも可能でした。

用途：

- シネマティック開始
- イベント制御
- 状態変更

ただし、一般的なレベル演出ではKismet経由で利用されることが多くありました。

---

# リアルタイムシネマティック

Matineeの特徴は、プリレンダリング動画ではなくゲームエンジン内でリアルタイム生成される点です。

メリット：

- キャラクターと環境を共有可能
- 解像度制限が少ない
- インタラクティブ要素と連携可能
- データ容量削減

---

# 採用例

UE3世代では、多くのタイトルでMatineeが利用されました。

用途：

- オープニング演出
- ボス登場
- ストーリーイベント
- チュートリアル
- ゲーム内ムービー

---

# 技術的意義

Matineeは、ゲームエンジンによる映像制作ワークフローを大きく発展させました。

影響：

- レベルデザイナーによる演出制作
- リアルタイムカットシーン
- 映画的ゲーム表現
- Sequencerへの発展

---

# UE4 Sequencerへの継承

Unreal Engine 4では、Matineeの後継としてSequencerが導入されました。

比較：

| UE3 | UE4/UE5 |
|-|-|
| Matinee | Sequencer |
| Timeline | Timeline |
| Camera Control | Camera Track |
| Actor Control | Actor Track |

基本思想は継承されています。

---

# 現在の研究環境

★★★☆☆

UE3 Matineeを利用するには、

- UDK
- UE3開発環境
- 過去プロジェクト

などが必要です。

現在では主に、過去作品の解析や技術史研究目的で扱われています。

---

# 関連項目

- [Unreal Engine 3](./README.md)
- [Kismet](./Kismet.md)
- [UnrealScript](./UnrealScript.md)
- [Rendering](./Rendering.md)

---

# 参考資料

- Epic Games Unreal Engine 3 Documentation
- Unreal Developer Network（UDN）
- UDK Documentation Archive
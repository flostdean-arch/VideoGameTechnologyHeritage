# Audio System

## 概要

Unreal Engine 3（UE3）のAudio Systemは、ゲーム内で使用される音声・効果音・BGMなどを管理するためのサウンドシステムです。

UE3では、単純な音声ファイルの再生だけではなく、SoundCueによる複雑な音響制御を導入しました。

これにより、ゲーム状況に応じた動的な音響表現が可能となり、後のUnreal Engine 4・Unreal Engine 5のAudio Systemへ繋がる基礎となりました。

---

# 開発背景

ゲーム表現が高度化するにつれて、音響にも以下のような要求が生まれました。

- 状況に応じたBGM変化
- 複数音源のランダム再生
- 距離による音量変化
- 環境音制御
- リアルタイムミックス

従来の単純なサウンド再生方式では対応が難しくなったため、UE3ではより柔軟なAudio Systemが設計されました。

---

# 基本構造

UE3 Audio Systemでは、Sound Assetを中心に音響データを管理します。

```text
Sound File

    ↓

SoundCue

    ↓

SoundNode Processing

    ↓

Audio Output
```

---

# SoundCue

SoundCueはUE3 Audio Systemの中心となる仕組みです。

単一の音声ファイルではなく、複数のSound Nodeを組み合わせて音響処理を構築できます。

例：

```text
SoundCue

├── Sound A
│
├── Sound B
│
├── Random Node
│
└── Volume Control
```

---

# SoundNode

SoundNodeはSoundCue内部で音響処理を行うノードです。

代表的な種類：

- Random
- Mixer
- Loop
- Attenuation
- Delay
- Modulation

など。

---

# Random Node

複数の音声からランダム再生を行います。

例：

```text
Footstep Sound

├── Step01.wav
├── Step02.wav
└── Step03.wav
```

同じ効果音の繰り返し感を減らすことができます。

用途：

- 足音
- 銃声
- 環境音

など。

---

# Mixer Node

複数の音声を混合します。

例：

```text
Weapon Sound

├── Fire Sound

├── Mechanical Sound

└── Impact Sound
```

複数要素を組み合わせた複雑な効果音を制作できます。

---

# Attenuation

音源からの距離による音量変化を制御します。

例：

```text
Player

    ↓

Near Object

大きい音


Far Object

小さい音
```

3D空間内で自然な音響表現を実現します。

---

# 3D Audio

UE3では3D空間内の音響配置に対応しています。

制御要素：

- 距離
- 方向
- 音量
- 減衰

用途：

- 銃声
- 敵の声
- 環境音
- 乗り物音

---

# Sound Class

Sound Classによって、音声カテゴリを管理できます。

例：

```text
Sound Class

├── Music

├── SFX

├── Voice

└── Ambient
```

これにより、ゲーム設定で音量調整などを容易にできます。

---

# Audio Mixing

UE3では複数の音を状況に応じて調整できます。

例：

戦闘開始：

```text
BGM ↑

Effect ↑

Ambient ↓
```

会話イベント：

```text
Voice ↑

BGM ↓
```

など。

---

# Gameplayとの連携

Audio SystemはGameplayシステムと密接に連携します。

例：

```text
Player Action

      ↓

Gameplay Event

      ↓

SoundCue Trigger

      ↓

Audio Playback
```

用途：

- 武器発射音
- 足音
- UI音
- イベント演出

---

# UnrealScriptとの関係

UE3ではUnrealScriptから音響制御が可能です。

例：

- Sound再生
- 音量変更
- 状態変更
- イベント連携

これにより、ゲームロジックと音響を統合できます。

---

# Kismetとの関係

KismetからAudioイベントを制御できます。

例：

```text
Trigger

 ↓

Kismet

 ↓

Play Sound

 ↓

SoundCue
```

レベルイベントやカットシーン演出で利用されました。

---

# Matineeとの関係

Matineeによる演出でもAudio Systemが利用されます。

例：

- ムービーBGM
- 効果音
- ボイスイベント

```text
Matinee Timeline

        ↓

Audio Track

        ↓

SoundCue
```

---

# 開発ワークフロー

UE3での音響制作：

```text
Audio File Creation

        ↓

Import

        ↓

SoundCue Setup

        ↓

Level Integration

        ↓

Gameplay Testing
```

---

# 技術的意義

UE3 Audio Systemは、ゲームサウンドを単純な再生処理から、ゲーム状態と連動する動的システムへ発展させました。

影響：

- アーティスト向け音響制作環境
- 動的サウンド制御
- リッチなゲーム演出
- UE4 Audio Systemへの継承

---

# UE4 / UE5への継承

UE4ではUE3のAudio System思想が継承されました。

| UE3 | UE4/UE5 |
|-|-|
| SoundCue | SoundCue |
| SoundNode | SoundNode |
| Sound Class | Sound Class |
| Audio Component | Audio Component |

さらにUE5では、

- MetaSounds
- 高度なリアルタイム音響制御

へ発展しています。

---

# 現在の研究環境

★★★☆☆

UE3 Audio Systemを研究するには、

- UDK
- UE3開発環境
- 過去タイトル解析
- 技術資料

などが必要です。

公式開発環境の配布終了後は、主に保存・研究目的で扱われています。

---

# 関連項目

- [Unreal Engine 3](./README.md)
- [Editor](./Editor.md)
- [Kismet](./Kismet.md)
- [Matinee](./Matinee.md)
- [Package System](./PackageSystem.md)

---

# 参考資料

- Epic Games Unreal Engine 3 Documentation
- Unreal Developer Network（UDN）
- UDK Documentation Archive
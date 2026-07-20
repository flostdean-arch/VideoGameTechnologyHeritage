# Production

## 概要

`Production/` は、Unreal Engine 3（UE3）におけるゲームコンテンツ制作・演出制作を支援するツール群を扱うカテゴリです。

UE3では、プログラマーだけではなく、レベルデザイナー、アーティスト、サウンドクリエイターが同じ開発環境上で作業できるよう、各種制作ツールがUnrealEdへ統合されました。

この設計思想は、後のUnreal Engine 4・Unreal Engine 5にも継承されています。

---

# 対象技術

現在、このカテゴリでは以下の技術を扱います。

| 技術 | 内容 |
|---|---|
| Matinee | リアルタイムシネマティック制作システム |
| Cascade | パーティクルエフェクト制作システム |
| Audio System | ゲームサウンド管理システム |

---

# 技術構成

UE3のProduction環境は、ゲーム演出に必要な各要素を統合しています。

```text
                 Production

                      │

 ┌────────────────────┼────────────────────┐

 ▼                    ▼                    ▼

 Matinee            Cascade            Audio System

 演出制作           VFX制作             音響制作


                      │

                      ▼

                Final Presentation
```

---

# Matinee

## 概要

Matineeは、UE3に搭載されたリアルタイムシネマティック制作システムです。

ゲーム内イベント、カットシーン、カメラ演出などをタイムライン形式で制作できます。

用途：

- オープニングムービー
- イベントシーン
- カメラ演出
- オブジェクトアニメーション

→ [Matinee](./Matinee.md)

---

# Cascade

## 概要

Cascadeは、UE3に搭載されたリアルタイムパーティクルエフェクト制作システムです。

ノード・モジュール方式によって、複雑な視覚効果を制作できます。

用途：

- 爆発
- 炎
- 煙
- 魔法エフェクト
- 環境エフェクト

→ [Cascade](./Cascade.md)

---

# Audio System

## 概要

Audio Systemは、ゲーム内音響を管理するシステムです。

SoundCueを中心として、複数の音声処理を組み合わせた柔軟なサウンド制作が可能です。

用途：

- BGM
- 効果音
- ボイス
- 環境音

→ [Audio System](./AudioSystem.md)

---

# Editorとの統合

Productionツールは、UnrealEd内部に統合されています。

```text
UnrealEd

 ├── Level Editor

 ├── Matinee

 ├── Cascade

 └── Audio Tools
```

別々の制作ツールを行き来するのではなく、ゲーム世界を確認しながら制作できます。

---

# Gameplayとの連携

ProductionツールはGameplay Systemと密接に連携します。

例：

イベント制作：

```text
Trigger

 ↓

Kismet

 ↓

Matinee

 ↓

Cascade Effect

 ↓

Audio Playback
```

ゲーム内演出を複数システムの組み合わせによって構築できます。

---

# Renderingとの関係

Productionツールで制作されたコンテンツは、Rendering Systemによって最終的に描画されます。

例：

```text
Cascade Particle

        ↓

Material System

        ↓

Rendering

        ↓

Screen Output
```

---

# アーティスト向け開発環境

UE3では、専門知識を持たないスタッフでも多くのゲーム要素を制作できるよう設計されました。

例：

| 担当 | 使用機能 |
|-|-|
| Level Designer | Matinee / Kismet |
| Artist | Cascade / Material |
| Sound Designer | Audio System |
| Programmer | UnrealScript |

---

# 技術的意義

UE3 Production Systemは、ゲーム開発における分業化を大きく進めました。

影響：

- アーティスト主導制作
- リアルタイム演出
- ノンリニアなゲームイベント制作
- AAA開発ワークフロー

---

# 後世代への継承

UE4・UE5では、UE3のProduction Systemが発展しています。

| UE3 | UE4/UE5 |
|-|-|
| Matinee | Sequencer |
| Cascade | Cascade / Niagara |
| SoundCue | SoundCue / MetaSounds |

特にMatineeからSequencer、CascadeからNiagaraへの流れは、Unreal Engineの代表的な技術継承です。

---

# 今後追加予定

必要に応じて以下を追加予定です。

- Movie Pipeline
- Cutscene Workflow
- Cinematic Tools
- Niagara比較

---

# 関連項目

- [Matinee](./Matinee.md)
- [Cascade](./Cascade.md)
- [Audio System](./AudioSystem.md)
- [Programming](../Programming/README.md)
- [Rendering](../Rendering/README.md)

---

# 参考資料

- Epic Games Unreal Engine Documentation
- Unreal Developer Network（UDN）
- UDK Documentation Archive
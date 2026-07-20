# Core

## 概要

`Core/` は、Unreal Engine 3（UE3）を構成する基盤技術を扱うカテゴリです。

ゲーム制作に直接見える機能ではなく、Unreal Engineそのものを支える開発環境・データ管理・エンジン基盤について記録します。

UE3では、これらの基盤技術によって、大規模ゲーム開発に対応した統合型ゲームエンジンとして発展しました。

---

# 対象技術

現在、このカテゴリでは以下の技術を扱います。

| 技術 | 内容 |
|---|---|
| Editor | UnrealEdを中心とした統合開発環境 |
| Package System | アセット・データ管理システム |

---

# 技術構成

UE3の基本的な制作フローは、Core技術を中心として構成されています。

```text
              Unreal Engine 3

                    │

              UnrealEd

                    │

        ┌───────────┴───────────┐

        ▼                       ▼

    Asset管理              Level制作

        │                       │

        ▼                       ▼

 Package System          Editor Tools
```

---

# Editor

## 概要

UnrealEdは、UE3における中心的な開発環境です。

以下のような作業を統合して行うことができます。

- レベル制作
- Actor配置
- アセット管理
- マテリアル編集
- イベント制作
- デバッグ

UE3以降のUnreal Engineが「エンジン」ではなく「開発環境」として利用される基礎となりました。

→ [Editor](./Editor.md)

---

# Package System

## 概要

UE3では、ゲームに使用するデータをPackage単位で管理します。

対象：

- Texture
- Mesh
- Material
- Sound
- Animation
- Level

など。

```text
Package

 ├── Texture

 ├── Material

 ├── Mesh

 └── Animation
```

この方式は、後のUE4におけるAsset Systemへ発展します。

→ [Package System](./PackageSystem.md)

---

# UE3におけるCoreの役割

UE3では、各システムが独立して存在するのではなく、Core技術を基盤として統合されています。

例：

```text
Package System

        ↓

Asset Loading

        ↓

Editor

        ↓

Rendering / Gameplay / Audio
```

この設計によって、大規模なゲーム制作環境を実現しました。

---

# 技術的意義

UE3 Core技術の重要性は、個別機能ではなく「制作環境そのもの」を提供した点にあります。

影響：

- 大規模AAA開発対応
- チーム開発環境
- アーティスト向け制作環境
- エンジン統合ワークフロー

---

# 後世代への継承

UE4以降でも、UE3で確立された思想は継承されています。

| UE3 | UE4 / UE5 |
|-|-|
| UnrealEd | Unreal Editor |
| Package | Asset System |
| Object管理 | UObject System |
| Content Browser | Content Browser |

特にEditorとAsset管理の設計思想は、現在のUnreal Engineシリーズでも重要な要素となっています。

---

# 関連項目

- [Editor](./Editor.md)
- [Package System](./PackageSystem.md)

---

# 参考資料

- Epic Games Unreal Engine Documentation
- Unreal Developer Network（UDN）
- UDK Documentation Archive
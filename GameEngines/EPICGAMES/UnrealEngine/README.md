# Unreal Engine

## 概要

Unreal Engineは、Epic Games（当時 Epic MegaGames）が開発するゲームエンジンシリーズです。

1998年に発売された『Unreal』のために開発された初代Unreal Engineを起点とし、現在のUnreal Engine 5まで継続的に発展しています。

本リポジトリでは、各世代の技術的特徴だけでなく、

- なぜその技術が採用されたのか
- 前世代から何が進化したのか
- 後継世代へどのように受け継がれたのか
- 現在でも研究・学習できる環境はあるのか

という「技術の系譜」を重視して解説します。

---

# Unreal Engineシリーズ

| 世代 | 初公開 | 主な特徴 | 現在の研究環境 |
|------|---------|---------|----------------|
| Unreal Engine 1 | 1998 | UnrealScript、BSP、UnrealEd | ★★★★★ |
| Unreal Engine 2 | 2002 | DirectX 8世代、Static Mesh、Karma Physics | ★★★★★ |
| Unreal Engine 3 | 2006 | DirectX 9、マルチスレッド、Kismet | ★★★☆☆ |
| Unreal Engine 4 | 2014 | Blueprint、PBR、GitHub公開 | ★★★★★ |
| Unreal Engine 5 | 2022 | Nanite、Lumen、World Partition | ★★★★★ |

※ 「現在の研究環境」は、本リポジトリ独自の指標です。

---

# 技術の系譜

```text
Unreal Engine 1
        │
        ▼
Unreal Engine 2
        │
        ▼
Unreal Engine 3
        │
        ▼
Unreal Engine 4
        │
        ▼
Unreal Engine 5
```

各世代では互換性だけではなく、設計思想も少しずつ変化しています。

例えば、

- UnrealScript → Blueprint
- BSP主体 → Static Mesh主体 → Nanite
- Fixed Function Pipeline → Programmable Shader → PBR
- Kismet → Blueprint Visual Scripting

など、多くの技術が継承・発展しています。

---

# 各世代

## Unreal Engine 1

シリーズ最初のゲームエンジン。

1998年発売の『Unreal』のために開発されました。

BSPを利用したレベル設計や、UnrealScriptによるゲームロジックなど、シリーズの基礎となる多くの技術がこの世代で確立されています。

→ [Unreal Engine 1](./UnrealEngine1/README.md)

---

## Unreal Engine 2

DirectX 8世代に対応し、大規模マップやStatic Meshなどを導入。

後のUE3へ繋がる設計が数多く採用されました。

→ [Unreal Engine 2](./UnrealEngine2/README.md)

---

## Unreal Engine 3

DirectX 9世代を代表するゲームエンジン。

マルチスレッド対応、Kismet、Lightmassなど、現代のゲームエンジンにも影響を与える技術を数多く採用しています。

現在は公式配布が終了しており、本リポジトリでは保存状況や研究環境についても記録しています。

→ [Unreal Engine 3](./UnrealEngine3/README.md)

---

## Unreal Engine 4

Blueprintの導入により、プログラマー以外でもゲーム開発が容易になりました。

GitHubでソースコードが公開され、インディーゲーム開発の普及にも大きく貢献しています。

→ [Unreal Engine 4](./UnrealEngine4/README.md)

---

## Unreal Engine 5

Nanite、Lumen、World Partitionなど、次世代ゲーム開発を支える技術を搭載。

現在もEpic Gamesによって継続的に開発されています。

→ [Unreal Engine 5](./UnrealEngine5/README.md)

---

# 本リポジトリの記事について

各記事では、以下の観点を共通して扱います。

- 概要
- 開発背景
- 基本情報
- 現在の研究環境
- 保存状況
- 技術解説
- 後継技術への影響
- 採用タイトル
- 関連資料
- 出典

単なる機能紹介ではなく、「なぜその技術が生まれたのか」「現在でもどのように研究できるのか」を重視しています。

---

# 関連記事

- History/GameEngineHistory.md
- Algorithms/
- Tools/

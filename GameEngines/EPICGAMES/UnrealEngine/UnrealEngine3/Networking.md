# Networking

## 概要

Unreal Engine 3（UE3）のNetworking Systemは、オンラインマルチプレイヤーゲームを構築するためのネットワーク基盤です。

UE3では、Client / Serverモデルを中心とした設計が採用され、複数プレイヤー間でのゲーム状態同期を実現しました。

このネットワーク設計は、後のUnreal Engine 4・Unreal Engine 5にも継承されています。

---

# 開発背景

UE3が登場した2000年代中盤は、オンラインゲームやコンソール向けネットワークプレイが急速に普及した時代でした。

そのため、ゲームエンジンには、

- プレイヤー同期
- オブジェクト同期
- サーバー管理
- 遅延への対応
- チート対策

などが求められました。

UE3では、これらをエンジンレベルで処理できるNetworking Systemが組み込まれました。

---

# Client / Serverモデル

UE3では、基本的にClient / Server方式が採用されています。

```text
        Server

          │

 ┌────────┼────────┐

 ▼        ▼        ▼

Client   Client   Client
```

## Server

サーバー側では、

- ゲームルール管理
- オブジェクト状態管理
- プレイヤー認証

などを担当します。

---

## Client

クライアント側では、

- 入力処理
- 描画
- ローカル演出

などを担当します。

---

# Authority System

UE3では、ゲーム状態の正しい管理者を決めるAuthorityという考え方があります。

基本的には、

```text
Server

 ↓

Game State Authority

 ↓

Client
```

という構造になります。

重要なゲーム状態はサーバー側で管理されます。

例：

- プレイヤー位置
- ダメージ結果
- アイテム取得
- 勝敗判定

---

# Actor Replication

UE3 Networkingの中心となる機能がReplicationです。

Actorの状態をネットワーク経由で同期します。

例：

```text
Server Actor

      ↓

Replication

      ↓

Client Actor
```

同期対象：

- 座標
- 回転
- 変数
- 状態情報

---

# UnrealScriptとの関係

UE3では、UnrealScriptからReplication設定を行うことができます。

例：

- Replicated Variable
- Replicated Function
- Network Event

これにより、ゲームロジックとネットワーク処理を密接に連携できます。

---

# Remote Function

UE3では、ネットワーク越しに関数を呼び出す仕組みが用意されていました。

用途：

- サーバーへの入力送信
- クライアント通知
- 状態更新

これにより、複雑なマルチプレイヤー処理を実装できます。

---

# Dedicated Server

UE3ではDedicated Serverにも対応していました。

Dedicated Serverでは、

- 描画処理を行わない
- ゲーム処理のみ実行
- 多人数接続対応

という構成になります。

用途：

- 対戦ゲーム
- 大規模マルチプレイヤー
- eSports系タイトル

---

# ネットワーク最適化

オンラインゲームでは通信量の削減が重要です。

UE3では、

- Replication制御
- 更新頻度制御
- 必要な情報のみ送信

などによって通信負荷を抑えました。

---

# Online Subsystem

UE3ではオンラインサービスとの連携も考慮されていました。

対象：

- Xbox Live
- PlayStation Network
- PCオンラインサービス

機能：

- マッチメイキング
- プレイヤー情報
- ランキング
- セッション管理

---

# 採用タイトルでの利用

UE3 Networkingは、多くのオンライン対応タイトルで利用されました。

例：

- Unreal Tournament 3
- Gears of Warシリーズ
- Borderlands
- Mass Effectシリーズ

など。

---

# 技術的意義

UE3のNetworking Systemは、ゲームエンジン内部にオンライン機能を統合する流れを加速させました。

影響：

- Client / Server設計の標準化
- Replicationシステム
- 大規模オンラインゲーム開発
- UE4 Networkingへの継承

---

# UE4への継承

UE4では、UE3のネットワーク設計思想を発展させています。

| UE3 | UE4 |
|-|-|
| Actor Replication | Actor Replication |
| UnrealScript Network | C++ / Blueprint Network |
| Dedicated Server | Dedicated Server |
| Online Subsystem | Online Subsystem |

UE4以降でもActorベースのReplicationモデルは継続して利用されています。

---

# 現在の研究環境

★★★☆☆

UE3 Networkingを実際に検証するには、

- UDK環境
- UE3採用タイトル
- 過去のMod環境
- 技術資料

などが必要です。

公式開発環境は現在配布終了しています。

---

# 関連項目

- [Unreal Engine 3](./README.md)
- [UnrealScript](./UnrealScript.md)
- [Package System](./PackageSystem.md)
- [UDK](./UDK.md)

---

# 参考資料

- Epic Games Unreal Engine 3 Documentation
- Unreal Developer Network（UDN）
- UDK Documentation Archive
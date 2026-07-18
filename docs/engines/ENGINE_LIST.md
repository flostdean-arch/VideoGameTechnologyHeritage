# エンジン一覧（候補）

このファイルは VideoGameTechnologyHeritage リポジトリの出発点として、保存・再現対象になり得る「古いゲームエンジン」の一覧と短いステータスを日本語でまとめたものです。

フォーマット（各エンジン）：
- エンジン名
- 概要
- 入手方法（公式 / コミュニティ / アーカイブ）
- 代表作（例）
- 主なソースポート／ツール
- ライセンス上の注意点
- 優先度（高 / 中 / 低）

---

1) Unreal Engine 1
- 概要: 初期のUnrealエンジン。UnrealEdなどのツールでMOD文化が発達。
- 入手方法: 古いディストリビューション（Unreal Gold 等）、コミュニティ資料、公式ソースは限定的。
- 代表作: Unreal, Unreal Tournament (原型)
- 主なソースポート／ツール: UnrealEd、非公式ドキュメント/チュートリアル
- ライセンス: 商用資産が含まれるため配布注意。ツールやドキュメントの扱いを確認。
- 優先度: 高

2) Unreal Engine 2
- 概要: UE1 の後継。MOD制作の手法が続くが、資料は分散。
- 入手方法: ゲーム付属 SDK やコミュニティ・アーカイブ
- 代表作: Unreal Championship 2 など
- 主なソースポート／ツール: UnrealEd（バージョン依存）
- ライセンス: 作品やバイナリのライセンス注意
- 優先度: 中

3) id Tech 1 (Doom 系)
- 概要: Doom のエンジン。ソースは公開済みで多数のソースポートあり。
- 入手方法: ソース公開、コミュニティ（GZDoom 等）
- 代表作: Doom, Doom II
- 主なソースポート／ツール: GZDoom, Chocolate Doom
- ライセンス: ソースはライセンスに従う（GPL等ではない歴史的混在あり）。
- 優先度: 中

4) id Tech 2–4 (Quake 系〜Doom3)
- 概要: Quake 系列（Quake、Quake II、Quake III）および id Tech 4 (Doom 3)。多くはソース公開や活発なソースポートがある。
- 入手方法: ソース公開、コミュニティビルド、ソースポート
- 代表作: Quake シリーズ、Doom 3
- 主なソースポート／ツール: DarkPlaces, ioquake3, vkQuake, ioquake2, various ports
- ライセンス: 各ソースのライセンスを確認（GPL等）
- 優先度: 中

5) Build エンジン
- 概要: Duke Nukem 3D 等で使われた Build エンジン。EDuke32 や Raze により近代環境で動作。
- 入手方法: ソースポート（EDuke32 など）
- 代表作: Duke Nukem 3D, Shadow Warrior
- 主なソースポート／ツール: EDuke32, Raze
- ライセンス: ソースポートのライセンス確認
- 優先度: 中

6) GoldSrc / Source
- 概要: Valve の GoldSrc（Half-Life 初期）および Source（Half-Life 2 等）。SDK とコミュニティ資料が豊富でモッディングがしやすい。
- 入手方法: Steam と SDK、コミュニティドキュメント
- 代表作: Half-Life シリーズ、Counter-Strike
- 主なソースポート／ツール: Source SDK, Hammer Editor, various community tools
- ライセンス: ゲームのアセットは商用、SDK利用規約要確認
- 優先度: 高

7) SCUMM 系（LucasArts アドベンチャー）
- 概要: 2Dアドベンチャー向けエンジン。ScummVM による再現性が高い。
- 入手方法: ScummVM プロジェクト、オリジナルデータはゲーム所有が前提
- 代表作: Monkey Island, Day of the Tentacle
- 主なソースポート／ツール: ScummVM
- ライセンス: 実データは権利者に依存。エンジン互換実装はOSS。
- 優先度: 低〜中

8) RenderWare
- 概要: 2000年代初頭の商用ミドルウェア。入手や権利が複雑。
- 入手方法: アーカイブやコミュニティ資料（入手困難）
- 代表作: 初期のPS2時代の多数のタイトル
- 主なソースポート／ツール: コミュニティ解析資料
- ライセンス: 商用ライセンスが絡むため注意
- 優先度: 低

9) LithTech
- 概要: Monolith のエンジン。ドキュメントは限定的。
- 入手方法: アーカイブ、コミュニティ資料
- 代表作: No One Lives Forever など
- 主なソースポート／ツール: コミュニティ解析
- ライセンス: 商用で複雑
- 優先度: 低

10) 初期 CryEngine / その他古い商用エンジン
- 概要: CryEngine の古いバージョンやその他商用エンジンは資料が散逸している。
- 入手方法: 公式アーカイブ（稀）、コミュニティ
- 代表作: Far Cry（初期）等
- 主なソースポート／ツール: 限定的
- ライセンス: 注意
- 優先度: 低

---

次のステップ（提案）:
- このファイルをベースに、優先度「高」のエンジン（例：Unreal Engine 1, GoldSrc/Source）から個別ページ（docs/engines/<engine>.md）を作成して詳細を集める。
- tools/ に入手スクリプトが必要なら順次追加する。

貢献ルール（簡易）:
- 各エンジンページの追加・更新は Pull Request で行う。
- 外部リンクやアーカイブを追加する際はライセンス注記を添える。

---

（作成日: 2026-07-18）

# Unreal Engine 1 (UE1)

- 対象: Unreal Engine 1(初代Unreal Engine)
- 年代: 1998年〜(『Unreal』にて初採用)
- 難易度: 中級
- 出典: (執筆時に追記。Wikipedia "Unreal Engine 1" "Unreal (1998 video game)" "Glide (API)"、Unreal Wiki、kentie.net "Multitexturing in the Unreal Engine" を参考に確認済みの範囲のみ記載)

## 概要

Unreal Engine 1(UE1)は、Epic Games(当時Epic MegaGames)が1998年発売のFPS『Unreal』のために開発した、シリーズ最初のゲームエンジン。開発はTim Sweeneyが中心となり、1995年頃から始まった。

その後Unreal Tournament(1999年)にも採用され、後継のUnreal Engine 2へと引き継がれた。

## 開発背景

1990年代半ば、PCゲームでは『DOOM』や『Quake』に代表されるリアルタイム3Dゲームが急速に普及していた。

Epic MegaGamesでは、それらとは異なる高品質なリアルタイム3D表現を目標として『Unreal』の開発を開始し、その中核技術としてUnreal Engineが設計された。

開発は1995年頃からTim Sweeneyを中心に進められ、約3年に及ぶ開発期間の中でPC向け3Dアクセラレータの普及に対応するため、レンダリングシステムも大きく進化していった。

## 現在の研究環境

**このセクションはこのプロジェクトの読者にとって特に重要なので、必ず維持してください。**

- **ゲーム本体(Unreal Gold / Unreal Tournament)**: Epic Games公認でInternet Archive経由で無料配布されている(実行ファイル/ゲームアセットとしての配布)
- **UnrealEd(レベルエディタ)・UnrealScript(スクリプト言語)**: 上記の無料配布版に同梱されており、MOD制作・マップ制作は現在も可能
- **エンジンのC++コア部分のソースコード**: Epicから公式に公開されたことはなく、現在も非公開(License: Proprietary commercial software)。GitHub上に見られる「UE1ソース」を名乗るリポジトリは、非公式に流出したソースやリバースエンジニアリングをベースにしたものであり、Epic公式の配布物ではない点に注意

→ 「バイナリが無料 = エンジンがオープンソース化された」ではない、という区別をこの記事内で明確にすること。

## 保存状況

Unreal Engine 1は、OldUnrealコミュニティによる継続的な保守活動が行われている数少ない歴史的ゲームエンジンである。

ゲーム本体（Unreal Gold・Unreal Tournament）はEpic Games公認の形で配布されており、現在でもレベルエディタやUnrealScriptを利用した研究・学習が可能である。

一方で、エンジンのC++コアソースコードは現在も公開されておらず、GitHub等で公開されている非公式リポジトリはEpic Gamesによる公式公開ではない点に注意が必要である。

## 基本情報

- 開発元: Epic Games(当時Epic MegaGames)
- 初版リリース: 1998年5月(『Unreal』)
- 開発言語: C++(コアエンジン)、UnrealScript(スクリプト)
- プラットフォーム展開の実際:
  - 初代『Unreal』(1998)は**PC(Windows)版のみ発売**。PlayStation版・Dreamcast版は開発が進められたが、いずれも発売中止になっている
  - PS2版・Dreamcast版が実際に発売されたのは、後発の『Unreal Tournament』(1999)から
  - → 「UE1 = PC・PS・DCで発売された」という単純化は誤りなので、記述する際は「どのタイトルの、どの移植版か」を明記すること

## 主な技術的特徴

### リアルタイム3Dレンダリング

Unrealの開発期間は非常に長く(1994〜1998年)、この間にPC向け3Dアクセラレータ市場が急速に立ち上がったため、複数のレンダリングパスを持つに至った。

- **ソフトウェアレンダラー**: 当時としては非常に高度な部類のソフトウェアレンダラーを搭載していた。カラーライティングやテクスチャフィルタリングに対応していたが、CPU負荷が非常に高かった
- **3dfx Glide**: 開発終盤、3dfxのVoodooシリーズが市場の主流になったことを受けて追加された。Voodoo上で最も安定・高速に動作するレンダラーとされ、発売当初は事実上の「推奨レンダリングパス」だった
- **Direct3D**: Unreal発売時、Microsoft Direct3Dの人気が急速に高まっていたため、Epicは急いでDirect3Dレンダラーを追加した。しかし初期のDirect3Dレンダラーは不安定・低速で、グラフィック品質の問題も多く、Glideに比べて完成度が低かった
- **OpenGL**: 公式にサポートされていた

**Unreal Tournamentエンジンでの強化(Unreal Gold等に反映):**
Unreal GoldはUnrealTournamentエンジンをベースに更新されており、ソフトウェア・Glide・Direct3Dの3レンダラーを搭載する。この時点でもGlideレンダラーが最も枯れており、Direct3Dは32bitカラーで特に低速、ガンマ補正にも問題を抱えていたとされる。

**現在の実行環境について**: 3dfx社自体が既に存在せず、Glideの動作には`nGlide`のようなラッパーソフトが必要になる。現代の環境では、有志によるD3D9/D3D10ラッパーレンダラー(`kentie.net`のものなど)や、後述のOldUnrealによる非公式パッチのレンダラーを使うのが実用的とされている。

*(このセクションは概ね確認済み。より詳細な技術的挙動〔マルチテクスチャリング対応の有無等〕は今後拡充する)*

### UnrealScript

C++で書かれたコアエンジンの上に、独自のスクリプト言語UnrealScriptを実装している。

```unrealscript
// UnrealScript の例
class MyActor extends Actor;

function BeginPlay()
{
    Log("Game Started!");
    SetTimer(1.0, true);
}
```

特徴: オブジェクト指向、コンパイル型(インタプリタではない)、ステートマシンによる状態管理をサポート。

```unrealscript
auto state Idle
{
    Begin:
        GotoState('Moving');
}

state Moving
{
    // Move logic here
}
```

### ワールドエディタ(UnrealEd)とBSP(Binary Space Partitioning)

UnrealEdは、CSG(Constructive Solid Geometry)ベースの「ブラシ」によってレベルを構築する。ブラシとは立方体や円柱などの単純な形状(あるいはそれらを組み合わせた形状)で、これを**加算(Additive)**または**減算(Subtractive)**という2種類の操作でワールドに適用していく。

**基本的な考え方:**

1. 何もない状態のレベルは、初期状態では**完全な「空(void)」**として扱われる(=プレイヤーが存在できる空間がまだない)
2. **加算ブラシ**を配置すると、その形状ぶんの「実体(ソリッド)」がワールドに追加される(例: 建物の外形や地面の塊を作る)
3. **減算ブラシ**を、追加した実体の内部に重ねて配置すると、その部分が「くり抜かれ」、プレイヤーが実際に歩き回れる空間になる(例: 建物の内部を空洞にする、壁に窓を開ける)

つまり「まず塊を作り、その中身をくり抜いて部屋にする」という彫刻的な手順でレベルを組み立てる。この加算・減算ブラシの組み合わせ結果を、内部的にBSPツリー(空間を再帰的に分割するデータ構造)としてコンパイルし、描画時の可視判定やコリジョン判定を高速化している。

*(注意: 「BSP」という呼称は本来「空間分割のデータ構造」を指す用語であり、厳密には「CSGによって作られたジオメトリ」そのものを指す言葉ではない。ただしUnreal界隈では両者がほぼ同義語として使われてきた経緯があるため、この記事でも慣習に従い「BSPブラシ」の呼称を用いる)*

**実務上のポイント:**
- ブラシには適用順序があり、後から適用したブラシが先のブラシの結果を上書きする(同じ場所に減算→加算の順で重ねれば、くり抜いた部分が再び埋まる)
- レベル全体をブラシだけで作ることは非効率なため、実際の制作では最小限のブラシで大まかな空間(プレイヤーが歩ける範囲)だけを作り、細部は別途配置するStaticMesh的なアクターで作り込むのが一般的だった

### AIシステム

敵AI(Skaarjなど)の行動制御にステートマシンベースのシステムを使用。

*(注意: 「Behavior Tree」はBehavior Treeという技法自体がゲーム業界で普及したのが2000年代半ば以降であり、1998年のUE1が採用していたとは考えにくい。この用語は使わず、実際に確認できた設計〔ステートマシン〕のみ記載する)*

### ネットワーク機能

Client-Serverアーキテクチャ、Replicationによる状態同期、RPCを備え、マルチプレイに対応。

## 有名なゲーム(UE1採用が確認できるもの)

- **Unreal**(1998, Epic Games) — シリーズ最初のUE1タイトル
- **Unreal Tournament**(1999, Epic Games / Digital Extremes) — マルチプレイFPSとして大きな成功を収めた
- **Deus Ex**(2000, Ion Storm) — アクションRPG+ステルス、UE1の拡張性を示す例
- **Rune**(2000, Human Head Studios)

**以下は要注意:**
- 『Splinter Cell』(2002, Ubisoft Montreal)は**Unreal Engine 2**採用であり、UE1ではない(誤って混同されやすいので明記)
- 『Aliens versus Predator 2』(2001, Monolith Productions)は**LithTechエンジン**採用であり、Unreal系ですらない

## 技術的な遺産と影響(検証中)

- スクリプト言語とコアエンジンの分離という設計は、後年のUnity(C#)やUnreal Engine 4/5(Blueprint)にも通じる考え方として語られることが多い
- CSGブラシによるレベルデザイン手法は、後のUnreal Engine 4でも一部踏襲されている

*(このセクションは一般論に寄りやすいので、具体的な出典・一次資料が見つかったものから優先的に肉付けすること)*

## 技術解説として今後拡充したいトピック

- [x] レンダリング方式(ソフトウェアレンダラー / Glide / Direct3D対応の変遷) — 「リアルタイム3Dレンダリング」セクションに記載済み
- [x] BSP(Binary Space Partitioning)によるレベル構造 — 「ワールドエディタ(UnrealEd)とBSP」セクションに記載済み
- [ ] UnrealScriptの言語設計の詳細
- [ ] Unreal Engine 2との違い(→ 上位の `GameEngines/UnrealEngine/README.md` にも要点を反映)

## 関連プロジェクト・参考リンク

<!-- 例: 非公式復元プロジェクト、OldUnreal、fgsfdsfgs/UE1 等。
     引用する場合は出典を明記し、著作権上のグレーゾーンには触れ方に注意すること。 -->

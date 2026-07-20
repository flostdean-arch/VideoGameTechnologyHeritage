# Build Engine

- 対象: Build Engine(Ken Silverman作)
- 年代: 1993年〜(『Duke Nukem 3D』等で使用)
- 難易度: 中級
- 出典: (執筆時に追記)

## この項目について

Unreal EngineやidTechと異なり、Build Engineは明確な「世代」に分かれておらず、1つのエンジンが継続的に拡張されてきた経緯を持つため、このフォルダでは世代分割を行わない(必要になった場合のみ後から分割する)。

## 概要

Ken Silvermanが1993年からApogee Software(3D Realms)との契約のもとで開発したFPSエンジン。『Duke Nukem 3D』(1996年)のほか、『Shadow Warrior』『Blood』『Redneck Rampage』等、当時12本以上の商用タイトルに採用された。

id Tech系やUnreal Engineとは異なり真の3D空間ではなく、セクター(Sector)ベースの構造で高さの異なるフロアやマップの傾斜表現(擬似的なroom-over-room表現の追加含む)を実現していた点が技術的特徴。

## 現在の入手性・注意点(ライセンスのグレーゾーン)

**このセクションはこのプロジェクトの読者にとって特に重要なので、必ず維持してください。**

Build Engineは「オープンソース化された」と語られることが多いが、実際には2つの異なるライセンス状態が混在しているため注意が必要:

- **Duke Nukem 3D本体のソースコード**: 2003年、3D Realmsによって**GPLライセンス**で公開されている
- **Build Engine自体のソースコード**: Ken Silvermanが独自に公開した`BUILDLIC.TXT`というライセンスのもとで配布されている。閲覧・改変は自由だが、**商用の派生物を作るには本人の許可が必要**という条件付きであり、GPLのようなOSI承認のオープンソースライセンスではない

→ 「id Tech系のような完全なGPL公開」と混同しないこと。技術解説の際は、どちらのライセンスの話をしているか(Duke3D側かBuild Engine側か)を明記すること。

- 現在も`EDuke32`(最も活発なメンテナンス版)、`JFBuild`、icculus.orgによる初期移植版など、Windows/Linuxで動く実装が複数存在し、実際に触りながら学べる環境が整っている

## 技術解説(執筆中)

<!-- 以下、サブトピックごとに rendering.md / gameplay.md 等に分割していく想定。
     まずはここに箇条書きで書きたいトピックを列挙してから、育てていくと進めやすい。 -->

- [ ] セクターベースのマップ構造(BSPを使わない設計)
- [ ] room-over-room表現の実現方法(擬似的な多層フロア)
- [ ] .CON言語によるゲームロジックのスクリプト化(Duke Nukem 3D向けにTodd Replogleが設計)
- [ ] Polymost(OpenGL対応レンダリング拡張)による技術的進化
- [ ] id Tech系・Unreal系との設計思想の違い

## 関連プロジェクト・参考リンク

<!-- 例: EDuke32、JFBuild、icculus.org/BUILD、Voxlap等。
     引用する場合は出典を明記し、ライセンスのグレーゾーンには触れ方に注意すること。 -->

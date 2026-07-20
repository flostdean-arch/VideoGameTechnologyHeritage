# Unreal Engine 2 (UE2)

- 対象: Unreal Engine 2(Unreal Engine 1の後継)
- 年代: 2002年〜(Unreal Tournament 2003にて初採用)
- 難易度: 中級
- 出典: (執筆時に追記)

## 概要

Unreal Engine 2は、Epic GamesがUnreal Engine 1の後継として開発したゲームエンジン。Unreal Tournament 2003(2002年)、Unreal Tournament 2004(2004年)、Unreal II: The Awakening等に採用された。

派生版としてUnreal Engine 2.5、2.5X(Xboxやモバイル向け最適化版など)も存在する。UE1と比べてグラフィックス表現やツール周りが強化されている一方、UnrealScriptを中心としたMOD制作の枠組みはUE1から地続きになっている。

## 現在の入手性・注意点

**このセクションはこのプロジェクトの読者にとって特に重要なので、必ず維持してください。**

- **ゲーム本体(Unreal Tournament 2004)**: Epic Games公認でOldUnrealプロジェクトを通じて無料配布されている(2026年、20年ぶりの公式パッチ3374と共に復活)。ただし配布されているのはあくまで実行ファイル/ゲームアセット
- **UnrealEd・UnrealScript**: 無料配布版に同梱されており、MOD制作・マップ制作は現在も可能。パッチ3374ではUnrealEdツールセット自体の安定性改善も行われている
- **エンジンのC++コア部分のソースコード**: UE1同様、Epicから公式に公開されたことはなく非公開のまま。`Deaod/UT2004`等、デコンパイルされたUnrealScript(.uc)を公開しているリポジトリはあるが、これはUnrealScriptレイヤーの話であり、C++コアとは別物である点に注意

→ UE1のREADMEと同様、「バイナリ/ツールが無料 ≠ エンジンがオープンソース化された」という区別を明確にすること。

## 技術解説(執筆中)

<!-- 以下、サブトピックごとに rendering.md / gameplay.md 等に分割していく想定。
     まずはここに箇条書きで書きたいトピックを列挙してから、育てていくと進めやすい。 -->

- [ ] レンダリング方式(UE1のソフトウェアレンダラーからの進化、Direct3D/OpenGL対応)
- [ ] Karmaによる物理演算の導入
- [ ] UnrealScriptの拡張点(UE1との差分)
- [ ] マテリアルシステムの強化
- [ ] UE1からの進化点(→ 上位の `GameEngines/UnrealEngine/README.md` にも要点を反映)
- [ ] UE2.5 / 2.5X 等の派生版との違い

## 関連プロジェクト・参考リンク

<!-- 例: OldUnreal、UT2004Patches、Deaod/UT2004 等。
     引用する場合は出典を明記し、著作権上のグレーゾーンには触れ方に注意すること。 -->

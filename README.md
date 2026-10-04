# cmk-mj-furikae-tutorial

マイプロジュニア（MJ）の **振替ワールド**（じゅんびひろば）で、レッスンごとに子どもへ送る MakeCode チュートリアル。

| ファイル | レッスン | 開く URL |
|---|---|---|
| `start.md` | ワールドの 初期（education.json の defaulturi）。C で ひらいた とき | `https://minecraft.makecode.com/#tutorial:github:cmk-dev-team/cmk-mj-furikae-tutorial/start` |
| `l01.md` | 1 どうぶつえん（いきもの を スポーン・みぎ うえ まえ の いち） | `https://minecraft.makecode.com/#tutorial:github:cmk-dev-team/cmk-mj-furikae-tutorial/l01` |
| `l02.md` | 2 どうぶつえん の おしごと（くりかえし） | `https://minecraft.makecode.com/#tutorial:github:cmk-dev-team/cmk-mj-furikae-tutorial/l02` |
| `l03.md` | 3 モンスター バトル（こうか。エフェクトのブロックはふつうの MakeCode のもの＝漢字のまま） | `https://minecraft.makecode.com/#tutorial:github:cmk-dev-team/cmk-mj-furikae-tutorial/l03` |

- ワールドからは `codebuilder navigate @s false <URL>` で送る（へや に 入ったとき 1回）
- ジュニアは 1ステップ 1指示。使うブロックだけ が 出るようにする（`@flyoutOnly true`）
- `images/` は教材パネル用の MakeCode 公式描画のブロック絵

作成：Aimy（ClassmallKids）

## 書きかたの決まり（2026-10-04 ブラウザで確認）

- 頭に `@flyoutOnly true`・`@hideIteration true`・`@hideDone true`（完了チェックを押すとふつうの MakeCode に戻るので隠す）。`@explicitHints` は使わない（灰色の空の箱が出る）
- ブロックは **ひらがな拡張** `cmk-hiragana-blocks#v1.7.0` を使う。最初から置いておくチャットコマンドは `hiraganaPlayer.onChatTemplate`（置き場に出ない）。ふつうの `onChat` を template に書くと置き場に "run" がもう1つ出る
- くりかえしは `hiraganaLoops.repeat(n, ...)`（「n かい くりかえす」）。スポーンはふつうの `mobs.spawn`（拡張の _locales でひらがなになる）

## 出しかた（ここを飛ばすと古いのが出る）

1. push する
2. **タグを打つ**（`git tag v0.x.y && git push origin v0.x.y`）。MakeCode はいちばん新しいタグを読む。タグを打たないと main を直しても出ない
3. `https://makecode.com/api/gh/cmk-dev-team/cmk-mj-furikae-tutorial/refs?nocache=1` を1回ひらく（MakeCode 側の覚えを更新する。しないと何時間も古いまま）

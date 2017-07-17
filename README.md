## 現在検証してほしい組み合わせ「mafuta3」60%＋「rezero8」40%[※対局結果求む](https://github.com/mafu-opening-theory/Shogi_opening_theory/releases/tag/v5.0)
- mafuta3がtanuki-wcsc27の遺伝子を色濃く受け継ぎ（６九玉、５八金の配点が高い）角換わりにおいてもelmoの６二金、８一飛型を５八金型で倒しているので、こちらの進化系に絞って配合情報を募集します。
- Qhapaq新ツールREMUで「mafuta3」を解析すると「elmo41%近似」と出ました。ＫＰＰＴ型においてelmoと玉位置配点が異なり、tanuki-wcsc27遺伝子が棋風として見えるのに驚きです。
- Qhapaq新ツールREMUが示唆しているように、人間の目で見て違っていても機械的に同一性が認められ、relmoのようにrezero8を１：１で（今回40%）配合するとレートが向上するのであれば、Qhapaq新ツールREMUはすごい配合発見器になるかもしれません。（評価関数自体が数字の集合体なので、検証の価値がかなり有ると思っています）
- キメラ配合のやり方が分からない人もいるかもしれないので、[検証プロジェクト](https://github.com/mafu-opening-theory/Shogi_opening_theory/releases/tag/v5.0)にて上記配合したもの「remutama40」をアップロードしておく。
- また安定の？野生の読み太２を48%配合した「remutama48」も次にアップロードしておく。（強そうなので私も検証中）

## 学習用定跡作成プロジェクト開始
数や偶然に頼った学習ではなく将棋として効率的な学習局面を与えることが定跡で出来るのかを検証する
- [プロジェクト１](https://github.com/mafu-opening-theory/Shogi_opening_theory/releases/tag/v1.0)※スタート前に自己解決しました。定跡を用いた学習が効果的であると結論が得られました。プロジェクト２より、少し前の評価関数を用いてレートに与える影響を検証したいので、配布する評価関数のレート計測等のお手伝いを頂けたらと思います。
- [プロジェクト２](https://github.com/mafu-opening-theory/Shogi_opening_theory/releases/tag/v2.0)※ファイル名が長すぎたのか文字化けのようになっていますが.depth.x.7zが全体型（depth３×３億局面）再学習です。
depth３とお手軽に個人作成出来るレベルで作った評価関数なので、評価関数の作り方の練習比較用等にお使い下さい。
- [プロジェクト３](https://github.com/mafu-opening-theory/Shogi_opening_theory/releases/tag/v3.0)
	- 学習用定跡作成プロジェクト２の結果より「学習用定跡」（教師局面生成用）を配布します。
	- 教師局面生成用評価関数（mafu10）を配布します。
- [プロジェクト４](https://github.com/mafu-opening-theory/Shogi_opening_theory/releases/tag/v4.0)
	- 評価関数ばかりに注目が行ってしまいましたが、私が作りたかった「学習用定跡」の有用性を示したいと思います。
	- tanuki-さんから許可を貰いましたので、野生の読み太のようにtanuki-wcsc27を私の配布している「学習用定跡」で生成した教師局面で再学習し、評価関数を作ってみようと思います。
- 現在「mafuta3」（まふ＋タヌキ評価関数）のブレンド相手の情報募集しています。この評価関数と○○％で交配すると強くなったとかの情報を受付中です。
	- 私の検証だと１手４０００万ノードだと評価値は若干おかしいが「mafuta3」が一番強い。４スレ５秒でも[実績](http://ii.ttlv.jp/20170711/)があるので。
	- 連絡先は私の[連絡用Twitter](https://twitter.com/mafu_op_theory)を誰からでもＤＭ受付しています。コンピュータ将棋スレッドへの書き込みでもＯＫです。
- レーティング関係については「コンピュータ将棋スレッド」で私の感性とは違う（４スレ５秒とかの限定的な強さ）基準で批評が多く見られたので取り下げます。

## 現在の開発過程
戦型別定跡、02_相掛かりを作成中
- 先手調整中
- 後手はいつも通り５０％程度になるように適当に調整中
- 戦型別定跡、03_横歩取り.binは５月２９日にver1を配布しました（一般向けは第５回電王戦後になります）

## 概要

まふ定跡とはオープンソースで使用出来る将棋ソフト用の定跡です。

- 技巧形式 ＝ [技巧、技巧２](https://github.com/gikou-official/Gikou/releases)に使用出来ます。
- 「技巧２」のデフォルト定跡として採用されました。ありがとうございます。
- Apery形式 ＝ [Apery（浮かむ瀬）](http://www2.computer-shogi.org/library/)、[SILENT_MAJORITY](https://github.com/Jangja/silent_majority/tree/1.2/bin)等に使用出来ます。
- [wcsc27tanuki-（wcsc27でPonanzaを倒したelmo使用と同等）](https://github.com/nodchip/hakubishin-/releases)がApery形式に対応しましたので使用出来ます。
- [wcsc27nozomi](https://github.com/saihyou/nozomi/releases)がApery形式に対応したようです。（私のＰＣでは要求スペックを満たしていなかったので動作未確認）
- [YaneuraOu-2017-early最新](https://github.com/yaneurao/YaneuraOu/releases)がApery形式に対応しましたので使用出来ます。（V4.56では正常に稼動していることを確認）

## 特徴

現存する人間が作成した誰でも使用出来る将棋の定跡としては登録数が多い。（Ver11現在）
- 登録指し手数は２５０万手以上（採用率０％も含めた数）
- 採用率の入っている登録指し手数は１３０万手以上
- そのうち調整済み有効手は４５万手以上（他で手に入る人間が作成した定跡は４万手程度が最高）

## 使い方

各使用将棋ソフトに合った下記の添付ファイルを参照下さい
- エンジン設定(参考) やねうら王early
- エンジン設定(参考) tanuki-
- エンジン設定(参考)
- Readme 9(技巧版ver10)
- Readme 8(ＳＭ版ver10)

## 過去の開発過程
- [技巧新定跡（まふ定跡）](http://www.uuunuuun.com/single-post/2016/11/06/%E6%8A%80%E5%B7%A7%E6%96%B0%E5%AE%9A%E8%B7%A1)
- [まふ定跡v9　対局データ](http://www.uuunuuun.com/single-post/2017/02/21/%E3%81%BE%E3%81%B5%E5%AE%9A%E8%B7%A1v9-%E5%AF%BE%E5%B1%80%E3%83%87%E3%83%BC%E3%82%BF)

## 目的

この定跡はアンチコンピュータ定跡ではありません。
その定跡進行において８０％以上が互角以上の中盤を迎えることが出来るなら、必敗手があったとしても採用しております。
いつもと違った状態で対局を楽しんだり、将棋ソフトのさらなる発展を願って作成しています。

## 他定跡開発者紹介
- [tibigame](https://github.com/tibigame/HandicappedRook)さん　「振り飛車定跡」を精力的に更新されています。振り飛車学習の評価関数もあります。
- [qhapaq](http://qhapaq.hatenablog.com/)さん　将棋ソフトqhapaqの開発者で真面目な定跡から、変わった定跡までいろいろ作成されています。
- [Mizar](https://onedrive.live.com/?authkey=%21APkeK0WwOdWpE8Y&id=37F98B3BB93213CD%21636&cid=37F98B3BB93213CD)さん　とにかくすごい量です。定跡作成ツールもあります。
- [やねうら王](https://github.com/yaneurao/YaneuraOu)さん　将棋ソフトを使う人で知らない人はモグリでしょう。
- [tanuki-](https://github.com/nodchip/hakubishin-/releases)さん　最近の互角局面定跡と言えば。

## ライセンス

Aperyと技巧に合わせて、GPL-3.0としました。（要約すればGPL-3.0付きのリポジトリ同士なら改変、再配布しても問題ないですよと宣言）
- 定跡ファイルはすべて１から自作していますのでお好きにお使い下さい。
- gikou_120のバイナリは定跡選択上限を５０→１２０に拡張改変を行っています。ソースコードは[こちら](http://www.uuunuuun.com/single-post/2016/11/06/%E6%8A%80%E5%B7%A7%E6%96%B0%E5%AE%9A%E8%B7%A1)

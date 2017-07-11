﻿## mafu10について
- もの凄い反響ありがとうございます。すでに短時間対局で２８００局程度の情報を頂きました。それによりますと前回の「mafu」よりＲ３０程度弱くＲ４１００程度であるという計測結果です。
- 今回の評価関数は「教師局面生成用評価関数」という位置付けで作成しています。具体的な違いは？と言われれば「mafu」＋「mafu10」の配合でもレートが少し上がります。
- これは出来るだけ正確な教師局面生成が出来るように評価パラメタの配分にこだわった効果で、次に学習した局面の特徴を捉えやすくするためです。ですから１０人が「mafu10」から評価関数を作っても特定の評価パラメタにハマリにくいので、いろいろな評価関数が出来ることが期待されます。
- さらに通常、学習で特徴を特化（過学習）してしまった評価パラメタを慣らすには、前に学習した教師局面と混ぜて再学習等行うことが必要ですが、この「mafu10」では評価パラメタが抑えられている（[まふ評価関数は何故強いのですか？](http://yaneuraou.yaneu.com/2017/07/08/%e3%81%be%e3%81%b5%e8%a9%95%e4%be%a1%e9%96%a2%e6%95%b0%e3%81%af%e4%bd%95%e6%95%85%e5%bc%b7%e3%81%84%e3%81%ae%e3%81%a7%e3%81%99%e3%81%8b%ef%bc%9f/)で私が書き込んだようなrezero系配合のような例外はあるが）ので突出した新しい評価関数と上手く配合するだけで慣らしが出来ます。（再学習を何時間もやるより超高速）
- 他にも私が思いつかなかったテクニックを発見された方は情報提供頂けたらと思います。
- 現在「mafu10」（まふ評価関数）のブレンド相手の情報募集しています。この評価関数と○○％で交配すると強くなったとかの情報を受付中です。連絡先は私の[連絡用Twitter](https://twitter.com/mafu_op_theory)を誰からでもＤＭ受付しています。コンピュータ将棋スレッドへの書き込みでもＯＫです。
	- 「mafu10」70%＋「mafu」(30%)で、4スレ1秒で勝率が上がったと報告有り※出来れば詳しい検証結果求む
	- 「mafu10」150%＋「mafu」(-50%)で、逆に減算しても強そう？評価パラメタを中央に寄せたので加算、減算のどちらかで個性を出すと強くなる？
	- 上記「mafu10」150%は１００局でrelmo8に勝率５８％も出ました。これだけ見ると配布物の中では最高レートですが、「mafu10」70%との対局では勝率３３％程度しかなく、とても逆転できそうになかったので対局止めました。誤差や相性問題にしては大きすぎて良く分かりません。※出来れば詳しい検証結果求む

## 学習用定跡作成プロジェクト開始
数や偶然に頼った学習ではなく将棋として効率的な学習局面を与えることが定跡で出来るのかを検証する
- [プロジェクト１](https://github.com/mafu-opening-theory/Shogi_opening_theory/releases/tag/v1.0)※まさに望外の結果でスタート前に自己解決しました。適当に作った物が短時間elmoに勝率７０％、長時間勝率６０％となり、定跡を用いた学習が効果的であると結論が得られました。が、まさか１発で出来ると思っていなかったので実際に何処の部分がどのくらいの効果があるのか理論的に落とし込みたいと思います。プロジェクト２より、少し前の評価関数を用いてレートに与える影響を検証したいので、配布する評価関数のレート計測等のお手伝いを頂けたらと思います。
- [プロジェクト２](https://github.com/mafu-opening-theory/Shogi_opening_theory/releases/tag/v2.0)※ファイル名が長すぎたのか文字化けのようになっていますが.depth.x.7zが全体型（depth３×３億局面）再学習です。
depth３とお手軽に個人作成出来るレベルで作った評価関数なので、評価関数の作り方の練習比較用等にお使い下さい。
- [ここ最近の評価関数のレートがひと目で分かります](http://ii.ttlv.jp/20170707/)「[局面の３駒関係](http://ii.ttlv.jp/)」開発者より４スレッド５秒で１７６７局もの対局結果を頂きました。たくさんの方に計測お手伝い頂きましたありがとうございます。結果はプロジェクト２のほうへ合算した結果を書いています。
- [プロジェクト３](https://github.com/mafu-opening-theory/Shogi_opening_theory/releases/tag/v3.0)
	- 学習用定跡作成プロジェクト２の結果より「学習用定跡」（教師局面生成用）を配布します。
	- 教師局面生成用評価関数（mafu10）を配布します。
- [プロジェクト４](https://github.com/mafu-opening-theory/Shogi_opening_theory/releases/tag/v4.0)
	- 評価関数ばかりに注目が行ってしまいましたが、私が作りたかった「学習用定跡」の有用性を示したいと思います。
	- tanuki-さんから許可を貰いましたので、野生の読み太のようにtanuki-wcsc27を私の配布している「学習用定跡」で生成した教師局面で再学習し、評価関数を作ってみようと思います。
	- mafuta1を配布。elmoは超えているだろうと思う評価関数をいくつか添付するので、どれが一番強そうか検証情報求む

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
- [YaneuraOu-2017-early最新](https://github.com/yaneurao/YaneuraOu/tree/master/exe/2017Early)がApery形式に対応しましたので使用出来ます。（V4.56では正常に稼動していることを確認）

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

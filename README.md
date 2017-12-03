## ブログを作成しましたので移転しました
- [ブログ移転先やダウンロード先はこちら](http://www.mafujyouseki.com)

## 学習用定跡作成プロジェクト終了
数や偶然に頼った学習ではなく将棋として効率的な学習局面を与えることが定跡で出来るのかを検証した
- [検証結果やダウンロード先はこちら](https://github.com/mafu-opening-theory/Shogi_opening_theory/releases)

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

各使用将棋ソフトに合った添付ファイルを参照下さい

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
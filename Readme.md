
# 数値シミュレーションで読み解く統計の仕組み・サポートサイト

こちらは「数値シミュレーションで読み解く統計の仕組み；Rでわかる心理統計」のサポートサイトです。
ここでは本書で案内していたコード，練習問題の解答例を掲載しています。

本書「はじめに」でも言及しましたが，こちらのサイトにあるコードをコピーして利用することはお勧めしません。
読者の皆さんには，Rプログラミングの技術を習得していただくことを期待しており，コードをコピー＆ペーストすることではプログラミング技術は身に付かないからです。同じデジタルな情報を*書き写す*ことは馬鹿馬鹿しいことのように思えますが，転記ミス，誤タッチ，TYPOを自分で経験し，エラーの対処を体験することが上達への近っ道だからです。

プログラミング技術を磨くためには，まず教本の写経から始め，ついでコードの一部を自分で改変し，どこがどう変わったか確認する，という段階に進んでください。常にコードを「読み」，結果に「触れる」ことで自らが体験すること，自分なりの感覚を把握することが肝要です。

また，ここに示されている練習問題の解答例は，あくまでも解答「例」であり，学力テストのような唯一の正答ではありません。FizzBuzz課題の例で示したように，機能的に一緒であれば，実装の方法についてはいくつものルートがありえます。あくまでも「そういう答え方もあるのか」という参照をしてください。

# 正誤表

万全を期して作成したつもりですが，初版で既にいくつか間違いのご指摘をいただいております。
ご指摘に御礼申し上げ，また，ここにお詫びして修正をご報告いたします。

| page                  | 誤                                                    | 正                                                           | 解説                                                                                                                                    |
|-----------------------|-------------------------------------------------------|--------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------|
| p.6　                 | Rコード`n <- 2500`                                    | `n <- 25`                                                    | テキストでは$n=25$の例として示していましたが，コードは続く$n=2500$の例を実行するものになっていました。                                  |
| p.6　5行目                | 実際に帰無仮説が採択される                                    | 実際に帰無仮説が棄却される                                                   |   |
| p.6　6行目                | 有意水準α = 0.05以下                                    | 有意水準α = 0.05未満                                                   |   |
| p.7　コード内のコメント                | データが当初の倍になるまで増やし続ける                                   | データが当初の3倍になるまで増やし続ける                                                  |   |
| p.10（下から5行目）　 | わかりやすく書いる書籍                                | わかりやすく書いている書籍                                   |                                                                                                                                         |
| p.18 L7                | BはAと同じくxを3列2行に                               | BはAと同じくxを3行2列に                                      | rowは行，colは列です。失礼しました。                                                                                                    |
| p.18                  | Rの出力の要素が全て0になっている                      | 1から24までの数字が順に入ります。                            | array関数が配列を指定するものです。                                                                                                     |
| p.26　 | Rコード`Species = "setosa"`                                |  `Species == "setosa"`                                  |   等価演算子は`==`です |
| p.26-27               | 出力                                                  | コード                                                       | 右肩に「出力」と書かれているブロックは、「コード」が正しいです。                                                                        |
| p.35-36               | 出力                                                  | コード                                                       | 右肩に「出力」と書かれているブロックは、「コード」が正しいです。                                                                        |
| p.26脚注8　 | `magritter`パッケージ                                |  `magrittr`パッケージ                            |   |
| p.40                  | 決して実行しないでくださいのコード                    | 変更なし                                                     | Rではカウンタ変数は別途割り当てられるので，永久ループにはならないそうです。しかしプログラミング言語として，一般的に避けるべき作法です。 |
| p.41                  | Rが永遠の計算ループから抜け出せなくなります。         | 抜け出せなくなることはありませんが，おかしな挙動になります。 | 両方`i`で回すと，内側の`i`ループが外側の`i`ループ分繰り返されるという動きになります                                                     |
| p.47脚注22                  | `¦`や`¦¦`   | 本文中のコードと同様に、`\|`や`\|\|` |    |
| p.49                  | モジュロ；odulo   |  モジュロ；modulo |    |
| p.80                  | Rコード`MC_demo()`   |  `mc_demo()` |    |
| p.104                 | Rコード最後の行内 `df(line_x,df1 = nu_1, df2= nu_2)`  | `df(line_x,df1 = 1, df2= nu)`                                | これに伴い、図3.29の曲線もわずかに変化します（ヒストグラムに変化はありません）。                                                        |
| P.124                 | 図4.2の結果を導いた                                | 図4.1の結果を導いた                                          |                             |
| P.134                 | Rコード`var_p`                                        | `var_p()`                                                    | Rのネイティブパイプは，関数()の形に渡すことが必要です(magritterのパイプ演算子`%>%`であれば問題ありません)                               |
| P.142本文下から3行目  | サンプルサイズ$n$が4、10、100と大きくなるにつれて　　 | サンプルサイズ$n$が4、20、100と大きくなるにつれて            |                                                                                                                                         |
| P.143図4.14           | 　　                                                  |                                                              | 誤った画像ファイルが挿入されていました。コードを実行して出力される図が正しいです                                                        |
| P.152コード最終行                 | `df = n - 2`               | `df = n - 1`         |  p151の数式と対応するので、`-1`が正しいです|
| P.182                 | Rコード`t.test(sample_r)$conf.int[1:2]`               | `cor.test(dat_obs[, 1], dat_obs[, 2])$conf.int[1:2]`         | 出力も`[1] 0.3787639 0.8187475`となります。                                                                                             |
| P.181                 | パーセンタイル信頼区間の方が広くなっています。        | 今回はパーセンタイル信頼区間の方が狭くなっています。         | ここは一般的に狭くなるわけではないので。                                                                                                |
| P.182                 | FisherのZ変換の上限(`0.4973`)と下限(`0.5011`)         | 上限は`0.5897387`，下限は`0.4217412`                         | Rのコード変更に伴って修正させていただきます。                                                                                           |

# 各章のコード

- [第1章のコード](ch1/ch1.R)
- [第2章のコード](ch2/ch2.R) / [練習問題の解答例](ch2/ch2_practice.R)
- [第3章のコード](ch3/ch3.R) / [練習問題の解答例](ch3/ch3_practice.R)
- [第4章のコード](ch4/ch4.R) / [練習問題の解答例](ch4/ch4_practice.R)
- [第5章のコード](ch5/ch5.R) / [練習問題の解答例](ch5/ch5_practice.R)
- [第6章のコード](ch6/ch6.R) / [練習問題の解答例](ch6/ch6_practice.R)
- [第7章のコード](ch7/ch7.R) / [練習問題の解答例](ch7/ch7_practice.R)

# 確認環境

コードについては以下の環境で確認しました。

------------------------------------------------------------------------

R version 4.3.1 (2023-06-16)

Platform: x86_64-apple-darwin22.4.0 (64-bit)

Running under: macOS Ventura 13.4.1

------------------------------------------------------------------------

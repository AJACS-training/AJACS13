[[AJACS13]]

        --
目次 (ver. 0.21)

#contents
        --
# Genome AnnotationとKazusa Annotation（かずさDNA研・○岡本忍、中尾光輝、藤澤貴智、中村保一） [#k08614e3]

## 【実習1】ゲノムアノテーションの検索例その２：UniProtKBで光合成系２のタンパク質のアノテーション（注釈）を眺めてみましょう [#a3c5ea26]

- UniProtKBのページ
- http://www.uniprot.org/help/uniprotkb

+1. 左側のプルダウンメニュー「Search in」を「Protein Knowledgebase」にする。
+2. 検索窓「 Query」の部分に"Photosystem II"と入力して検索してみる。→　http://www.uniprot.org/uniprot/?query=Photosystem+II&sort=score
+3. 検索窓「 Query」の部分に"Photosystem II AND Synechocystis AND PsbA2"と入力して検索してみる。→　http://www.uniprot.org/uniprot/?query=Photosystem+II+AND+Synechocystis+AND+PsbA2&sort=score
+4. エントリー P16033を眺めてみよう　→　 http://www.uniprot.org/uniprot/P16033
+5. P16033の更新履歴を見てみよう。→　http://www.uniprot.org/uniprot/P16033?version=*
+6. version 74と80を比較してみよう。→　http://www.uniprot.org/uniprot/P16033?version=74&version=80

## 【実習2】KazusaAnnotationの利用例 [#ddc2dcce]
+1. http://a.kazusa.or.jp/ を開いてみましょう [[（画像）>http://MotDB.DBCLS.jp/?plugin=attach&pcmd=open&file=%A5%D4%A5%AF%A5%C1%A5%E3%201.png&refer=AJACS5%2Fyn]]
+2. 酸素発生型光合成細菌の'''Synechocystis'''の光センサー、バクテリオフィトクロームの遺伝子cph1のアノテーションを検索しましょう。右上の検索窓に「Synechocystis cph1」と入れて「検索」を押します。
+3. このように検索結果が表示されます→ http://a.kazusa.or.jp/annotation?q=Synechocystis+cph1
+4. 検索結果のなかの遺伝子 slr0473 の赤い字でしめされた「366 annotations」をクリックするとslr0473遺伝子につけたアノテーション（ブックマーク）が一覧されます。→ http://a.kazusa.or.jp/annotations/1
+5. Pubmed ID: のなかから、15641769 をクリックすると、論文の情報が表示されます。→http://a.kazusa.or.jp/tags/3
+6. 論文情報の下部分「アノテーション数:20」は、この論文PubMed ID 9154987にGene Indexingが20個つけられてることを表しています。
数字の「20」の部分をクリック。この論文では、slr0473以外に、slr0474の遺伝子にもIntroductionとDiscussionで言及してることがわかります。
+7.論文情報の下部分「GeneIndexingView」をクリックすると、文献書式（Title, Abstract, Introduction...）のどこに、どの遺伝子が記述されているのかが参照できます。タイトルやアブストラクト、ディスカッションに出てる遺伝子は、この論文のメインテーマであると類推できます。→　http://a.kazusa.or.jp/tag/geneindex/pmid:15641769

- かずさDNA研究所が提供している、シアノバクテリア（光合成細菌）、根粒菌のデータベース →　http://genome.kazusa.or.jp/
    - CyanoBase（光合成細菌）→ http://genome.kazusa.or.jp/cyanobase
- CyanoBaseでバクテリオフィトクローム遺伝子 slr0473をみてみよう。→ http://genome.kazusa.or.jp/cyanobase/Synechocystis/genes/slr0473
    - CyanoBaseのGeneViewページの[[ Gene Annotation >http://genome.kazusa.or.jp/cyanobase/Synechocystis/genes/slr0473#gene_annotations]]のところにはKazusaAnnotationへのリンクがある。
    - CyanoBaseのGeneViewページの[[ References >http://genome.kazusa.or.jp/cyanobase/Synechocystis/genes/slr0473#gene_annotations]]の情報はKazusaAnnotationのGene Indexingから作成している。

        --

## 【参考1】Biocuratorについて [#h6f9d33f]
- 生物に関する様々な情報を整理、統合、付与、修正しゲノム情報の価値を高めるスペシャリスト
- 学会サイト →　 http://www.biocurator.org/
## 【参考2】集合知的なもののパワー [#z7f79829]
- 日本全国の鉄道の駅のデーターベース　→　[[日本の鉄道駅一覧>http://s-url.jp?53157]]
- 全国のポストをひたすらマッピング →　 [[ポストマップ>http://postmap.org/]]

## 【参考3】科学論文での集合知の利用例 [#oa186c7c]
- [[Citeulike>http://www.citeulike.org/]]
- [[connotea>http://www.connotea.org/]]
## 【参考4】OpenID について [#t1f3e408]
- OpenIDを使うと、KazusaAnnotationにあなた自身がブックマークを登録することができます。
- こちらをご覧ください。統合TV「統合DBを使い倒すためにOpenIDを取得する」http://togotv.dbcls.jp/20080507.html
- [[openid.dbcls.jp>http://openid.dbcls.jp]]
 DBCLS OpenID サービス は、DBCLS が提供する OpenID 認証サービスです。
 統合データベースプロジェクトをはじめとした OpenID に対応しているサイトについて、
 ひとつのアカウントでアクセスすることができます。
 使いかたはヘルプを御覧下さい。統合TVによる使いかた紹介
 (統合DBを使い倒すためにOpenIDを取得する)も併せて御覧下さい。
- ご自身のメールを受け取ることのできる環境で、OpenIDを取得してください
- 統合DBサービスの標準認証サービスです。Kazusa Annotation Suite以外に http://lifesciencedb.jp/ などで活用できます。
##  【参考5】KazusaAnnotationの文献表示に使われているWebService [[TogoWS >http://togows.dbcls.jp/]] [#f8051d32]
- REST/SOUPによる生物情報オブジェクトの取得

## 【参考6】論文と遺伝子の関係性を俯瞰する：[[Cytoscape >http://www.cytoscape.org/]] でみる KazusaAnnotation/Gene Indexing [#y60eab77]
- http://charles.kazusa.or.jp/~so/ajacs/syn_allgenes_ajacs.cys：Cytoscapeで開くとレイアウトされた状態で見ることが出来ます。検索等も可能。
- http://charles.kazusa.or.jp/~so/ajacs/syn_allgenes_cyt.txt：syn_allgenes_ajacs5.cysを描画するための遺伝子-文献(言及頻度）の二項関係データ、Synechocystis全遺伝子
- http://charles.kazusa.or.jp/~so/ajacs/syn_path00195_cyt.txt：syn_allgenes_ajacs5.cysを描画するための遺伝子-文献(言及頻度）の二項関係データ、Synechocystis光合成関連遺伝子

## 【参考7】論文と遺伝子の関係性を俯瞰する：[[genoDive >http://www.youtube.com/watch?v=FEQlVEAJe2k]] [#od0bb900]
- 遺伝子ごとに出版されている文献、遺伝子発現データ、アノテーションなどをリアルタイムに俯瞰できるゲノムビューア


        --
#  KazusaAnnotation Suite: かずさでのコミュニティー／ソーシャルアノテーションのこころみ [#d49f1902]

##  [[KazusaAnnotation>http://a.kazusa.or.jp/]] 【http://a.kazusa.or.jp】 [#ydda68f9]
- ソーシャルブックマークによるゲノムアノテーション蓄積／改善／統合サイト。
- 10生物種, 4003論文 131723 タグ (2009年7月3日0時現在)


## [[KazusaNavigation>http://navi.kazusa.or.jp/]] 【http://navi.kazusa.or.jp】 [#p30dae20]
- コミュニティの形成や活性化をめざしたサイト
- ソーシャルネットワークサービス (SNS)の Elgg ( http://elgg.org ) を改変して用いています

### KazusaNavigationの利用例 [#d2b36c7c]
+1. http://navi.kazusa.or.jp を開き [[（画像）>http://MotDB.DBCLS.jp/?plugin=attach&pcmd=open&file=%A5%D4%A5%AF%A5%C1%A5%E3%208.png&refer=AJACS5%2Fyn]]
+2. 右上の検索窓の下にある「一覧」をクリック＞プロジェクトとユーザの一覧が表示されます [[（画像）>http://MotDB.DBCLS.jp/?plugin=attach&pcmd=open&file=%A5%D4%A5%AF%A5%C1%A5%E3%209.png&refer=AJACS5%2Fyn]]
+3. あるいは http://www.google.co.jp で「KazusaNavigation 植物研究関連イヴェント」「KazusaNavigation 植物研究者人材募集」で 検索
+4. 「植物研究関連イヴェント」を閲覧する [[（画像）>http://MotDB.DBCLS.jp/?plugin=attach&pcmd=open&file=%A5%D4%A5%AF%A5%C1%A5%E3%2010.png&refer=AJACS5%2Fyn]] [[（画像）>http://MotDB.DBCLS.jp/?plugin=attach&pcmd=open&file=%A5%D4%A5%AF%A5%C1%A5%E3%2011.png&refer=AJACS5%2Fyn]]
+5. 「植物研究者人材募集」も同様に閲覧してみましょう。

- &ref(rss.png); RSSをブラウザに登録しておけば、毎回見に来る必要はありません。新着が報告されます
    -RSSとは？ see → http://ja.wikipedia.org/wiki/RSS

- OpenIDを取得すると、プロジェクト（コミュニティ）を作るなど、コンテンツを作成し共有することができます。

## [[KazusaWiki>http://wiki.kazusa.or.jp/]] 【http://wiki.kazusa.or.jp】 [#v279beae]
Wikipediaと同じ、Mediawikiというプログラムを利用した情報とりまとめ用サイト

### KazusaWikiの利用例 [#xf4f324b]
+1. http://wiki.kazusa.or.jp を開く [[（画像）>http://MotDB.DBCLS.jp/?plugin=attach&pcmd=open&file=%A5%D4%A5%AF%A5%C1%A5%E3%2012.png&refer=AJACS5%2Fyn]]
+2. あるいは、http://www.google.co.jp で「KazusaWiki トマト」で検索し [[（画像）>http://MotDB.DBCLS.jp/?plugin=attach&pcmd=open&file=%A5%D4%A5%AF%A5%C1%A5%E3%2013.png&refer=AJACS5%2Fyn]]
+3. トマト研究会 JSOL（ http://wiki.kazusa.or.jp/JSOL ）のコンテンツを開いてみる [[（画像）>http://MotDB.DBCLS.jp/?plugin=attach&pcmd=open&file=%A5%D4%A5%AF%A5%C1%A5%E3%2014.png&refer=AJACS5%2Fyn]]

- OpenIDを取得すると、Wikiのコンテンツを作成し共有することができます。研究会の情報共有などにどうぞ。

        --

[[AJACS13]]

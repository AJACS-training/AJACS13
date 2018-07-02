「遺伝子配列・発現データベースの利用法」

        --
[[AJACS近江2>AJACS13]] > 遺伝子配列・発現データベースの利用法
        --

# はじめに [#v716442d]
- みんなでわーっとアクセスすると、反応が遅くなったり、大量アタックと勘違いされてアクセス禁止（通称：アク禁）を食らったりするので、ばらばらとアクセスしてみてください
- というわけで、ここに書いてあること（や、他のところの）を自分なりに進めて or 自分なりにじっくりやってかまいません。
- 時間とここのコンテンツの分量があっていませんが、すでに知っている（特に塩基/アミノ酸配列のところ） or 今日は省略させてもらうところが多々あります。ご承知ください。

# （一応）自己紹介 [#z3f23573]
- どんな人が、こういう（＝ライフサイエンス統合データベースセンターみたいな）ところにいるのか参考のために
- 99-02：wet時代（別名：バイオ時代）：東京工業大学（B4-M2）
    -恐山産ウグイの酸性適応機構
    -ウナギの海水適応機構における硫酸イオントランスポーターの同定と機能解析
- 02-07：dry時代（別名：IT時代）：NEC バイオIT事業推進センター
    -多くが製薬、食品に就職する中、実験に挫折。ITの道へ
    -文献検索システムの開発など
- 07：冬の時代：NEC（別部署）
    -部署が半壊（ビジネスにならなかった）。→ 別部署に飛ばされる
    -毎日、官庁相手の営業を支援するためのPowerPoint資料作り
- 07-：dry時代、再び
    -現在の職場に拾われる。

# 塩基/アミノ酸配列 [#h0da72bb]
## とりまく状況 [#qb774524]
- 塩基配列は、GenBank(NCBI)/EMBL/DDBJに蓄積され、公開されている
- 【実習1-1】GenBankに登録されている塩基配列の登録数はどのくらいだろうか?
    -[[NCBI>http://www.ncbi.nlm.nih.gov/]]にアクセスし、「All[Filter]」で検索してみる → [[結果:http://tinyurl.com/n8fkyo]]
#fold(←こたえはここをクリック,およそ1億7000万件。正確には、169,748,738件[10/14現在]…nucleotide＋EST＋GSS)
#fold(参考,9/4は、167,207,342件だったので、1ヶ月ちょっとで、200万件増えたことに → [応用編] 最近、登録されたものにはどういうものがあるか? … Limits で 30daysにしぼるなど)
- 【実習1-2】GenBankに登録されている塩基配列の総塩基数はどのくらいだろうか?
    -Statistics のページを見てみる → [[結果:http://www.ncbi.nlm.nih.gov/Genbank/genbankstats.html]]
#fold(←こたえはここをクリック,およそ1000億bp（別の言い方すると100GB分）。正確には、99,116,431,942bp)
- 【実習1-3】どのような形式（フォーマット）でデータが収められているだろうか
    -どのような項目があるか見てみましょう
    -例：[[Tribolodon hakonensis（ウグイ [魚]） mRNA for carbonic anhydrase 2, complete cds:http://www.ncbi.nlm.nih.gov/nuccore/AB055617]]
    -解説：[[DDBJのデータ公開形式:http://www.ddbj.nig.ac.jp/sub/ref10-j.html]]
    -[応用] 配列だけ取得する
        - → Format のFASTAをクリック
        - 右の方のDownloadでダウンロードもできる

## そもそもどのエントリを選ぶべきか [#c595b435]
#ref(./flow.gbref.006.png)
- どんなデータが?
    -GenBank … 研究者が登録した配列（生データ）
    -[[RefSeq:http://www.ncbi.nlm.nih.gov/RefSeq/]] … GenBank に登録された配列を、NCBIがまとめてreferenceとしてまとめたもの
        -元来は、登録される配列は断片であったので（昔のDNAシーケンサーは長く読めなかった and/or つないでいない）
    -Entrez Gene … RefSeq の配列に対して、外部リンク、ゲノム上の位置、遺伝子名、Gene Ontology（機能を表す用語）などのアノテーション情報をつけたもの
- コメント
    -GenBankもRefSeqもNucleotide (GenBank)から検索できます
    -RefSeqは、アクセッション番号が、NM_#########、NC_#########、XM_#########などになっています。（詳細は、[[ここ:http://www.ncbi.nlm.nih.gov/books/bv.fcgi?rid=handbook.table.ch18.T18.1]]）
    -結局：RefSeqにデータがあればよいですが、微生物系はキビシイかも
    -参考：昔、キーワード検索をしたら、同じ名前の全然 違う遺伝子のデータをダウンロードしてしまい、論文出版後に再現性がとれないとクレームがついた事件があったりしたので、検索は十分に気をつけましょう

## そこで DNAデータベース総覧と検索 [#h0bd172f]
- 何コレ：DDBJ/EMBL/GenBank（DNA塩基配列のデータベース）に登録されている全レコードをプロジェクト単位で分類。「生物種」と「研究の型」の二次元で分類。データを一括ダウンロード可能
- http://lifesciencedb.jp/image/small_video_icon.png [[DNAデータベース総覧と検索を使い倒す>http://togotv.dbcls.jp/20080514.html]]
- ひとつひとつの遺伝子を見て行く時代は過去のもの。最近はプロジェクトにより大量の遺伝子が登録されている
    -[[例:http://www.ncbi.nlm.nih.gov/nuccore/74222023]]
    -→ それらを一度にダウンロードして活用という場面も
- DNAデータベース総覧と検索 (DDBJ/EMBL/GenBank)：http://lifesciencedb.jp/ddbj/ を使ってみよう
- 【実習2-1】「生物群区分」で特定のカテゴリーを選ぶと、研究プロジェクト数が絞り込まれることで数が変化する。「生物群区分」で「ヒト」を選ぶ前と後で「研究の型別分類」の「機能RNA・RNAゲノム」の項目はいくつからいくつに変化するか？
- 【実習2-2】「生物群区分」で「ヒト」、「研究の型別分類」で「mRNA」を選んで得られる研究プロジェクトのリストを、「研究プロジェクトの一覧」を「サイズ順」にすることでデータサイズの大きなプロジェクト順に並び替えなさい。トップ３にランキングされる研究プロジェクトはそれぞれ何か？
- 整理のしかた
#ref(./slc26a6.gb.004.png)
    -生物種
        -HUM：human
        -ROD：rodent（ゲッ歯類）
        -MAM：mammal（ほ乳類）
        -VRT：vertebrate（脊椎動物）
        -PAT：特許
        -ENV：環境
        -... → [応用] 自分の目的とするものはどのカテゴリだろうか。それを確認してこの「目次」で絞り込んでみよう
    -研究の型
    - 【参考】[[DDBJ のデータ公開形式 (flat file) の説明>http://www.ddbj.nig.ac.jp/sub/ref10-j.html]]
- 【実習2-3】統合ホームページ中の「ダウンロード」のタブをクリックすると、国内のゲノム・ポストゲノムプロジェクト配列データのダウンロードページに辿り着ける。この中から興味のあるプロジェクトを選び（例えば、シロイヌナズナ (Riken2004年)）、公開されている配列をFASTA形式で一括ダウンロードしなさい。
- 【応用1】上の実習でわずか数クリックで実現した一括ダウンロードできることのメリットは何だろうか？それがない場合、どういった手続きをしないといけないかを考えてみなさい。

# 遺伝子発現 [#ve7db054]

## [[&size(20){BioGPS};>https://biogps.gnf.org/]] [#t5ad14b0]
&color(green){ヒト、マウス、ラットのさまざまな組織や細胞(株)における遺伝子発現プロファイルのデータベース};

- [[BioGPS>https://biogps.gnf.org/]]はAffymetrix社製のマイクロアレイであるGeneChipを用いた遺伝子発現プロファイルのデータベース。
- [[GNF SymAtlas>http://symatlas.gnf.org/]][[【参考動画】>http://togotv.dbcls.jp/20070816.html]]のメジャーアップデート版。
- マウスのエキソンアレイのデータが追加されたので、遺伝子のスプライシングバリアント(Splicing variant)の発現状況も調べることが可能。
- 検索した遺伝子に対して、種々の外部データベースに横断検索することができる。
- 【実習3】BioGPSを使ってある遺伝子の発現プロファイルを調べる
- [[【使い方参考動画】>http://togotv.dbcls.jp/20081004.html#p01]]、[[【講習会動画】>http://togotv.dbcls.jp/20090217.html#p01]]http://lifesciencedb.jp/image/small_video_icon.png
- 1. [[https://biogps.gnf.org/>https://biogps.gnf.org/]]を開きます。
- 2.水チャネル（水を通すトランスポーター）であるAQP3 (aquaporin 3) の発現プロファイルを調べてみましょう。中央の検索窓に「AQP3」と入力し、「search」を押します。
- 3. 表示された検索結果をクリックします。
- 4. 最初はヒトのマイクロアレイデータが表示されます。
- 5. マイクロアレイデータ左上の「Human」をクリックするとマウスやラットを選択できます。また、「203737_at」（プローブID）をクリックすると、別のプローブでの発現状況（別のsplice variantなど）の結果が見られます
- 6. AQP3はどの組織、細胞で強く発現しているでしょうか？
- 7. 右上の「default rayout」をクリックすると、検索した遺伝子に関するマイクロアレイデータ以外のデータが閲覧できますが、どのようなデータが閲覧できるのか調べてみましょう。
- 8. [応用] 左上の「Search」タグをクリックして検索画面にもどり、自分の興味ある遺伝子について同様に検索してみましょう。

## [[&size(20){NCBI Gene Expression Omnibus (GEO)};>http://www.ncbi.nlm.nih.gov/geo/]] [#nd080802]
&color(green){世界最大の遺伝子発現（[[マイクロアレイ>http://ja.wikipedia.org/wiki/DNA%E3%83%9E%E3%82%A4%E3%82%AF%E3%83%AD%E3%82%A2%E3%83%AC%E3%82%A4]]）データベース（レポジトリ）};

塩基配列を研究者がGenBank (Nucleotide) に登録し、世界の人が見られるのと同じように、各々の発現情報も集められてみられるようになっています。それがGEOです。

### 【実習4-1】GEOを使って、自分の興味のある遺伝子の（ある実験条件下における）発現状況を調べる [#o6215864]
- [[【使い方参考動画】>http://togotv.dbcls.jp/20090213.html#p01]]http://lifesciencedb.jp/image/small_video_icon.png
- 1. [[http://www.ncbi.nlm.nih.gov/geo/>http://www.ncbi.nlm.nih.gov/geo/]]を開きます。
- 2.「Gene profiles」に自分の検索したい遺伝子名を入力します。
- 3. 今回は例として「[[nanog>http://www.google.co.jp/search?hl=ja&q=Nanog%E9%81%BA%E4%BC%9D%E5%AD%90]]」という遺伝子を検索してみましょう。入力終了後、「GO」をクリックします。
- 4. GEOに登録されている様々な実験条件で行なわれたマイクロアレイ実験における「nanog」遺伝子の発現データが表示されます。
- 5. 検索結果の右端にある画像をクリックすると、[[発現データの詳細をみる>http://www.ncbi.nlm.nih.gov/geo/gds/profileGraph.cgi?&dataset=DEAryz&dataset=yyyzzz$&gmin=5173.000000&gmax=11680.000000&absc=&gds=2294&idref=161072_at&annot=Nanog]]ことができます。
- 6. 「Display values」をクリックすると、発現値を一覧できます。
- 7. [[このサンプル>http://www.ncbi.nlm.nih.gov/sites/GDSbrowser?acc=GDS2294]]では、nanogはどういう細胞のどういう実験条件で発現が増減しているか調べてみましょう。
- 8. ページ下部の「samples」に列挙された[[リンク>http://www.ncbi.nlm.nih.gov/geo/query/acc.cgi?acc=GSM130365]]をクリックすると、そのサンプル（一枚のマイクロアレイ）の詳細を閲覧できます。
- 9. [[リンク先のページ>http://www.ncbi.nlm.nih.gov/geo/query/acc.cgi?acc=GSM130365]]の中ほどにある[[「series」のリンク>http://www.ncbi.nlm.nih.gov/geo/query/acc.cgi?acc=GSE5583]]をクリックすると、この実験全体の詳細情報が見られます。
- 10. [[この実験全体の詳細情報ページ>http://www.ncbi.nlm.nih.gov/geo/query/acc.cgi?acc=GSE5583]]の下部にある[[「Series Matrix File(s)」>ftp://ftp.ncbi.nih.gov/pub/geo/DATA/SeriesMatrix/GSE5583/]]をクリックすると、この実験の正規化補正済みのマイクロアレイデータをダウンロードすることができます。
### 【実習4-2】データセットブラウザ(Dataset browser)を利用して、GEOに登録されているマイクロアレイデータを解析する [#mcb0ec77]
- [[【使い方参考動画1】>http://togotv.dbcls.jp/20090221.html#p01]]http://lifesciencedb.jp/image/small_video_icon.png 、[[【使い方参考動画2】>http://togotv.dbcls.jp/20090307.html#p01]]http://lifesciencedb.jp/image/small_video_icon.png
- 1. [[http://www.ncbi.nlm.nih.gov/geo/>http://www.ncbi.nlm.nih.gov/geo/]]を開きます。
- 2.「Gene profiles」に自分の検索したい遺伝子名を入力します。
- 3. 今回は例として「[[nanog>http://www.google.co.jp/search?hl=ja&q=Nanog%E9%81%BA%E4%BC%9D%E5%AD%90]]」という遺伝子を検索してみましょう。入力終了後、「GO」をクリックします。
- 4. GEOに登録されている様々な実験条件で行なわれたマイクロアレイ実験における「nanog」遺伝子の発現データが表示されます。
- 5. 検索結果の[[アクセッション番号（今回は GDS2294）>http://www.ncbi.nlm.nih.gov/sites/GDSbrowser?acc=GDS2294]]をクリックすると、解析用の「データセットブラウザ」が開きます。
- 6. 「Expression profiles」をクリックすると、[[この実験データセットにおける個々の遺伝子発現状況を検索できるページ>http://www.ncbi.nlm.nih.gov/sites/entrez?db=geo&cmd=search&term=GDS2294[ACCN]]に飛びます。
- 7. 検索窓に表示されているアクセッション番号の後に続けて遺伝子名を追加（今回は例として [[Oct4>http://www.google.co.jp/search?q=Oct4]] ）すると、この実験データセット内におけるその遺伝子の発現データが検索できます。
- 8. 「データセットブラウザ」の「Data Analysis Tools」では詳細なデータ解析が可能です。
- 9. 「Find gene name or symbol:」のところに自分の興味ある遺伝子名を入れてみましょう。
- 10. 「Find genes that are up/down for this condition(s):」の「GO」をクリックするとどのような遺伝子がヒットするでしょうか。
- 11. 「Compare 2 sets of samples」では2群間で発現に差のある遺伝子を（統計学的に）検索できます。step1で発現量の違いを検出する方法を設定します。step.2で比較する2群の設定をします。step.3の「Query Group A vs. B」をクリックすると、検索が始まります。
- 12. 「Cluster heatmaps」では、マイクロアレイデータ解析でよく用いられる[[ヒートマップ>http://images.google.co.jp/images?q=ヒートマップ]]でのデータ表示が行なえます。分類方法としてHierarchical、Partitional (K-means/K-medians)、By location on chromosomeの3種類が選べますが、それぞれどのようにデータが分類されるか試してみましょう。
- 13.  「Experiment design and value distribution」では実験データにおける発現の分布を参照できます。これにより、各サンプルのデータが互いに比較可能か（実験上のミスがないか）チェックすることができます。

### 【実習4-3】GEOを使って、自分の興味のあるマイクロアレイ実験データセットを検索&生データをダウンロードする [#p2d60759]
- [[【使い方参考動画】>http://togotv.dbcls.jp/20081218.html#p01]]http://lifesciencedb.jp/image/small_video_icon.png
- 1. [[http://www.ncbi.nlm.nih.gov/geo/>http://www.ncbi.nlm.nih.gov/geo/]]を開きます。
- 2. 画面中央の「Platforms」をクリックします。
- 3. [[Platform(マイクロアレイの種類)の一覧画面が現れる>http://www.informatics.jax.org/javawi2/servlet/WIFetch?page=imageSummaryByMrk&key=25000&imageType=8]]ので、上部の「FIND PLATFORM」をクリックします。
- 4. [[platformの検索画面>http://www.ncbi.nlm.nih.gov/geo/query/browse.cgi?mode=findplatform]]が現れるので、「Company name」に「Affymetrix」、「organism」に「Homo sapiens」を選択し、「FIND PLATFORM」をクリックします。
- 5. [[Affymetrixのヒトのマイクロアレイの検索結果>http://www.ncbi.nlm.nih.gov/geo/query/browse.cgi?mode=foundplatform]]が表示されるので、中程にある「Affymetrix GeneChip Human Genome U133 Plus 2.0 Array」の左端にある[[「GPL570」というID>http://www.ncbi.nlm.nih.gov/geo/query/acc.cgi?acc=GPL570]]をクリックします。
- 6. [[表示された画面>http://www.ncbi.nlm.nih.gov/geo/query/acc.cgi?acc=GPL570]]の真ん中あたりにある「series」下の「More...」をクリックすると、登録されているデータセットを閲覧できます。
- 7. ブラウザの検索ボタンなどを使って「reprogramming」という単語を検索するとどういうデータがヒットするでしょうか？
- 8. ヒットしたデータの左端にあるIDをクリックすると、[[そのデータセットの詳細情報>http://www.ncbi.nlm.nih.gov/geo/query/acc.cgi?acc=GSE9832]]が閲覧できます
- 9. ページ下部の「Download family」の中にある「Series Matrix File(s)」をクリックすると正規化済みのデータのダウンロードリンクが表示されます。
- 10. ページ最下部の「Supplementary file」にあるリンクから生データをダウンロードすることができます。
- 11. 自分の研究テーマに近い、また興味のあるマイクロアレイデータが利用可能か検索してみましょう。

## 遺伝子発現バンク(GEO)目次：http://lifesciencedb.jp/geo/ [#n4bee97f]
- [[統合ホームページ>http://lifesciencedb.jp/]] > データベース > 遺伝子発現バンク(GEO)目次
- [ナニコレ] NCBIのGEO（Gene Expression Omnibus:mRNA発現情報のデータベース）に登録されている全レコードをプロジェクト単位で分類。「生物種」、「研究の型」、「部位」の三次元で分類。データを一括ダウンロード可能
- http://lifesciencedb.jp/image/small_video_icon.png [[遺伝子発現バンク(GEO)目次を使い倒す－その壱>http://togotv.dbcls.jp/20080623.html]]
- 【実習5-1】「生物種」で特定の種を選ぶと、研究プロジェクト数が絞り込まれることで数が変化する。「生物種」で「ヒト」を選ぶ前と後で「研究の型」の「GeneChip」(Affymetrixの発現アレイ)、「cDNAアレイ」、「オリゴアレイ」の項目はいくつからいくつに変化するか？また、「生物種」に「齧歯」を選ぶとそれぞれどうか？
- 【実習5-2】右上の検索フォームで'hypoxia'と入力して検索したあとで、「生物種」で「ヒト」、「研究の型」で「GeneChip」を選んで得られる研究プロジェクトのリストを表示せよ。「測定サンプル」のカラムの数字をクリックしてどのようなことが起こるか、確認してみよ。また、GSEで始まるGEOのエントリ（例えばGSE4725）をクリックするとNCBIのサイトに直接アクセスできるので、そのページにアクセスせよ。


### マイクロアレイデータの生物学的な解釈 [#d59a5949]
#ref(./microarray.analysis.005.png)
- 上で述べたマイクロアレイの結果の解析は、統計解析で、それらの遺伝子が生物学的にどういう意味を持つかわかりません。
- そこで、Gene Ontologyの用語を付与することで、生物学的な解釈を行います。
- 今回は触れられないので、[[別の回:http://motdb.dbcls.jp/?AJACS12%2Fhono3]]の資料の中のCateGOrizerや、[[DAVIDをとりあげた統合TV:http://togotv.dbcls.jp/20090925.html]]を参考にしてください。


# 次世代シーケンサのデータについて [#f5aad881]
- 次世代シーケンサのデータは、中身は配列データですが、ある状態での遺伝子発現を塩基配列として検出することもでき、遺伝子発現データとしてもとらえられます
    -ゲノム解読として使う場合は、配列データとしてで、発現データを得るためにも用いることができる、ということです。
- 次世代シーケンサによる測定結果（≠解析結果）も、登録、公開のしくみができている
    -NCBI：Short Read Archive (SRA) http://www.ncbi.nlm.nih.gov/Traces/sra/sra.cgi
    -EBI：European Read Archive (ERA)
http://www.ebi.ac.uk/embl/Documentation/ENA-Reads.html
    -DDBJ：DDBJ Read Archive (DRA) http://trace.ddbj.nig.ac.jp/dra/index.shtml
- 【実習6】どのような形でデータが登録されているか見てみよう → [[例:http://tinyurl.com/lzlles]]
    -参考：[[DRA Documentation:http://trace.ddbj.nig.ac.jp/dra/documentation.shtml]]

        --
[[AJACS近江2>AJACS13]] > 遺伝子配列・発現データベースの利用法
        --

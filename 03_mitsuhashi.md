        --
目次

#contents
        --
#  アナトモグラフィーとは [#e503e771]
解剖学用語を選択して自由に人体のモデル図(アナトモグラム)を描くツールです。

#  アナトモグラフィーの場所 [#v04d66a5]
- [[統合データベースプロジェクト:http://lifesciencedb.jp]]の「統合ツール」から。
- [[トップページURL (http://lifesciencedb.jp/ag):http://lifesciencedb.jp/ag]]
- [[「アナトモグラフィー」でgoogle検索:http://www.google.co.jp/search?q=%E3%82%A2%E3%83%8A%E3%83%88%E3%83%A2%E3%82%B0%E3%83%A9%E3%83%95%E3%82%A3%E3%83%BC&lr=lang_ja&ie=utf-8&oe=utf-8&aq=t]]

# 【実習1】エディタを使って心臓をかく [#af3cf424]

- 手順１ トップページのアナトモエディタ（[[http://lifesciencedb.jp/ag:http://lifesciencedb.jp/ag]])にアクセス
#ref(1-1.jpg,left)
- 手順２ 初期状態で表示されている「骨」を削除
    - 中央下の選択臓器リストの「骨」の左端のボックスをチェック
    -「Delete Checked」ボタンを押下
    -右下の「Drawボタン」を押下（因みに「Drawボタン」右の「Redraw on change」をチェックすると、「Drawボタン」を押下せずとも自動再描画）
#ref(1-2.jpg,left)
- 手順３ 心臓を臓器一覧から選択し、選択臓器リストに追加
    -左側臓器名のツリーの「循環器系」→「心臓」とたどり、心臓をクリック
    -左下の「Organ Information」の「add」ボタンを押下
    -右下の「Drawボタン」を押下
#ref(1-3.jpg,left)
- 手順４ 右心室を半透明にし、右心室内を表示する
    -左側臓器名のツリーを「循環器系」→「心臓」→「心室」→「右心室」とたどり、選択臓器リストに「右心室」を追加
    -「右心室」のOpacity(不透明値）を0.3～0.4程度にする
    -右下の「Drawボタン」を押下
#ref(1-4.jpg,left)
- 手順５ 心室中隔（右心室と左心室間の壁）を着色し、表示
    -左側臓器名のツリーを「循環器系」→「心臓」→「心室」→「心室中隔」とたどり、選択臓器リストに「心室中隔」を追加
    -心室中隔の領域を着色（下絵では赤）して明示
    -右下の「Drawボタン」を押下（冠状動脈が内部の心室中隔まで栄養していることが確認できる）
#ref(1-5.jpg,left)
- 手順６ 心臓周辺の血管を追加表示
    -左側臓器名のツリーで「循環器系」を選択し、「Drawボタン」を押下して表示。(BodyParts3Dで作成された範囲で）全身の血管が表示され、心臓の表示は小さくなる。血管の名前がわからなくてもまとめて追加できる。
#ref(1-6.jpg,left)
- 手順７ 右心室周辺だけを拡大
    -選択臓器リストの「右心室」の「zoom」ボックスをチェック
    -「Drawボタン」を押下
#ref(1-7.jpg,left)

# 【実習2】AQP3遺伝子の臓器別発現量を、表形式(CSVフォーマット）で一括入力して、人体ヒートマップで表示し発現状況を可視化する [#g05ada80]

#ref(2-0.jpg,left)

- 手順１．アナトモグラフィー(Anatomography)エディタ(CSVデータ入力)画面を表示します。
    -[[アナトモエディタ:http://lifesciencedb.jp/ag/]]上部の~
”臓器名と数値（例：発現量など）を表形式...こちらから”の[[”こちら”:http://lifesciencedb.jp/ag/form/indexCSV.jsp]]からをクリック。~
#ref(2-1.jpg,left)
もしくは、
    -[[URL(http://lifesciencedb.jp/ag/form/indexCSV.jsp):http://lifesciencedb.jp/ag/form/indexCSV.jsp]]を入力してアクセス。

- 手順２．以下の表形式データをマウスで選択してコピーしてテキストエリア（臓器）に貼り付けます。~
各列（カンマ区切り）の意味は以下の通りです。

 臓器名, s(表示) or z(拡大表示), 色情報（数値 or RGB(例:255,0,0)), 不透明度(0.0-1.0 省略時:1.0(不透明))

 腎臓,s,300
 気管,s,1500
 唾液腺,s,1000
 膵臓,s,1200
 前立腺,s,1250
 肺,s,1500
 肝臓,s,250
 骨,s,-1,-1,-1,0.5

骨は位置の目安として表示。数値の替わりに、色情報RGB(-1,-1,-1はデフォルトの肌色）を指定します。

#ref(2-2.jpg,left)

- 手順３．画面下の「Submit」ボタンをクリックします。~
カラーバーを表示したい場合は、「カラーバーの表示」をOnにします。

#ref(2-3.jpg,left)

- おまけ：特定の臓器を拡大表示したい場合は、s→zに変えます。以下のように皮膚以外の臓器をzにすると、骨以外の臓器全てがちょうど収まるようにズームされます。

 腎臓,z,300
 気管,z,1500
 唾液腺,z,1000
 膵臓,z,1200
 前立腺,z,1250
 肺,z,1500
 肝臓,z,250
 骨,s,-1,-1,-1,0.5

#ref(Image22.jpg,left)

#  講習会資料(pdf)ダウンロード [#r86b3350]

#ref(ajacs近江2（アナトモグラフィー）.pdf,left)

#  統合TVアナトモグラフィー [#r66ac34c]
- http://togotv.dbcls.jp/movie/080926ag3_f.html
- http://togotv.dbcls.jp/movie/080606AgService2_f.html

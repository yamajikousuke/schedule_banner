<p>ターゲット時刻にバナーを表示するプログラムです。（秒単位で設定可能）</p>
<p>時刻設定はjson配列を使っていくつでも設定可能です。setInverval関数で1秒毎に現在時刻をチェックして表示させます。</p>

<h1>ファイル構成</h1>
│  schedule_banner.html<br>
│  <br>
├─images<br>
│      img01.png<br>
│      img02.png<br>
│      img03.png<br>
│      img04.png<br>
│      img05.png<br>
│      <br>
└─js<br>
        schedule_banner.js<br>
        schedule_banner_conf.js<br>

<h1>使い方</h1>
<h2>設定ファイル</h2>
まず、設定ファイルであるschedule_banner_conf.jsに、バナー画像を格納しているフォルダのパスと表示時刻、URLを設定します。<br>
フォルダのパスは、最後にスラッシュ（/）を付けて下さい。表示時刻は、json配列で指定してください。<br>
<br>
<h3>時刻とバナー画像の設定例</h3>
{ 'year':2016, 'month':10, 'day':16, 'hour':13, 'min':50, 'sec':0, 'img':'img02.png', 'url':'url_01'}<br>
<br>
year:年<br>
month:月<br>
day:日<br>
hour:時<br>
min:分<br>
sec:秒<br>
img:バナーのファイル名（フォルダ名は省いてください。）<br>
url:aタグのhref<br>

<p>上から順番に（下へ行くほど）時間が経過していくように設定してください。</p>
<h2>バナーの表示箇所の指定方法</h2>
HTMLの中でバナーの表示箇所をdiv#scedule_bannerで指定します。

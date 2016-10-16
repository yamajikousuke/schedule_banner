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
var schedules = [<br>
    { 'year':2016, 'month':10, 'day':16, 'hour':13, 'min':50, 'sec':0, 'img':'img02.png', 'url':'url_01'},<br>
    { 'year':2016, 'month':10, 'day':16, 'hour':13, 'min':53, 'sec':0, 'img':'img03.png', 'url':'url_02'},<br>
    { 'year':2016, 'month':10, 'day':16, 'hour':14, 'min':10, 'sec':0, 'img':'img04.png', 'url':'url_03'},<br>
    { 'year':2016, 'month':10, 'day':16, 'hour':14, 'min':20, 'sec':0, 'img':'img05.png', 'url':'url_03'}<br>
];
<p>上から順番に（下へ行くほど）時間が経過していくように設定してください。</p>
<table style="margin-left:50px">
<tr><td>year</td><td>年</td></tr>
<tr><td>month</td><td>月</td></tr>
<tr><td>day</td><td>日</td></tr>
<tr><td>hour</td><td>時</td></tr>
<tr><td>min</td><td>分</td></tr>
<tr><td>sec</td><td>秒</td></tr>
<tr><td>img</td><td>バナーのファイル名（フォルダ名は省いてください。）</td></tr>
<tr><td>url</td><td>aタグのhref</td></tr>
</table>

<h2>バナーの表示箇所の指定方法</h2>
HTMLの中でバナーの表示箇所をdiv#scedule_bannerで指定します。

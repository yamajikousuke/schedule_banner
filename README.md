# schedule_banner
<h1>ファイル構成</h1>
│  schedule_banner.html
│  
├─images
│      img01.png
│      img02.png
│      img03.png
│      img04.png
│      img05.png
│      
└─js
        schedule_banner.js
        schedule_banner_conf.js

<h1>使い方</h1>
schedule_banner_conf.jsに、バナー画像を格納しているフォルダのパスと表示時刻、URLを設定します。<br>
フォルダのパスは、最後にスラッシュ（/）を付けて下さい。<br>
表示時刻は、json配列で指定してください。<br>
ターゲット時刻の指定の例<br>
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

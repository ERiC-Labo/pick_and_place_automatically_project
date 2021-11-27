# pick_and_place_automatically_projeject

## 手順
### Step1: センサ点群を入手する
<p align="center"><img src="https://github.com/ERiC-Labo/pick_and_place_automatically_projeject/blob/main/images/ima.png" width="600px" height="300px"></p>
真上から撮ったセンサ点群を入手します。画像から分かるとおり、ロボットアームから箱、床全体に向かって点群が取れていることが分かると思います。

### Step2: 平面除去する
<p align="center"><img src="https://github.com/ERiC-Labo/pick_and_place_automatically_projeject/blob/main/images/ima_1.png" width="600px" height="300px"></p>
床に平面上に広がった点群は必要がないので、平面除去するpcl(点群を処理するc++のライブラリ)の関数を用いて平面の点群を除去します。

### Step3: センサ画像から求める物体を検出する
<p align="center"><img src="https://github.com/ERiC-Labo/pick_and_place_automatically_projeject/blob/main/images/ima_2.png" width="600px" height="300px"></p>
センサから画像を入手します。そして、把持する物体を検出して、その部分の矩形を抽出します。

### Step4: Step3の矩形情報から点群を取る範囲を絞る
<p align="center"><img src="https://github.com/ERiC-Labo/pick_and_place_automatically_projeject/blob/main/images/ima_2.png" width="600px" height="300px"></p>

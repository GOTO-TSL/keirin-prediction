# ニューラルネットワークで競輪予想
## 概要
ニューラルネットワークで競輪を予想するnotebookです．
<p>主にやっていることは以下になります．</p>

* データ収集
* データ前処理
* モデル作成　学習
* 実際に予想

## 使用ライブラリ
* numpy
* tensorflow
* keras
* BeautifulSoup
* matplotlib
* sklearn
* pandas
* requests

## 各ファイルの説明
### `get_Data.ipynb`
データを収集を行うためのnotebookです．
<p>
収集元：<a href="https://keirin.kdreams.jp/">Rakuten Kドリームズ</a>
</p>
収集したデータはdataファイルにpickleファイルとして保存されdata_cleaning.ipynbで使用します．

### `data_cleaning.ipynb`
データの前処理を行うためのnotebookです．
<p>データに対して，ダミー変数化，欠損値の除去，各値の型を数値型へ変換を行っています．</p>

### `learning_model.ipynb`
学習モデルの作成と学習を行うためのnotebookです．
<p>手法はタイトルにもある通りニューラルネットワーク(多層パーセプトロン)を使っています．　入力は29個，出力は２個となっており，</p>
<p>ある選手が３着以内に入るかどうかの２値分類を行っています．</p>

### `prediction_race.ipynb`
学習済みモデルを使用して実際に予想することができるnotebookです．
<p>実際に予想したいレースのURLを入力してnotebookを走らせると，各選手が3着以内に入る確率が出力されます．</p>

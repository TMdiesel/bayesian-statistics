# BayesianPositionEstimation
## 環境
- Windows10

## 推定対象
ビーコンを使った移動体のトラッキングを行う。
- RSSIには距離減衰モデルを用いる。([RSSI方式における減衰定数の位置推定時決定手法](https://www.jstage.jst.go.jp/article/ieejeiss/128/10/128_10_1509/_pdf/-char/ja))
## モデル
- RSSI強度yは、平均が距離減衰モデルを用いて得られるRSSIとなる正規分布に従う。
- 移動体のマルコフ性は仮定しておらず、任意の時刻において移動体位置xの事前情報はないとする。

## 推論
- pymc3でしようと試みたが`AttributeError: module 'theano' has no attribute 'gof'`が出て、これの解決方法が分からなかったので、numpyroで実装
- numpyroはWindows環境ではサポートが制限されているようなので([参照](https://pypi.org/project/numpyro/))、Windows Subsystem for Linuxを使用
- 実装には、[HELLO CYBERNETICS](https://www.hellocybernetics.tech/entry/2020/09/09/093000)さんなどの記事を参照

## gif生成
```
ffmpeg -i bpe.mp4 bpe.gif
```

## 結果
図中の赤色で示す4つのビーコンの観測情報をもとに、緑色で示す移動体の位置をベイズ推定する。
ビーコン観測後の移動体位置の事後分布を青色で示す。
図より、ビーコンと移動体の位置が近いときは事後分布が鋭いピークを持ち、確信を持って推定出来ることが分かる。また、マルコフ性を仮定していないので、time=27～29において瞬間移動的挙動が観測される。

![bpe](https://user-images.githubusercontent.com/50258785/98467489-ef0b8080-2218-11eb-8d49-31ecd50df509.gif)
<!--
## notebook実行方法
poetryコマンドを先頭につけてjupyter labを立ち上げてもpoetry環境がkernelに追加されていなかったので、[Qiita記事](https://qiita.com/yuki-shark/items/fba874a109f04004158b)に従って追加した。
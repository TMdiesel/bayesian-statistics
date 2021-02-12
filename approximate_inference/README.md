# 近似推論
## ギブスサンプリング
- 二次元ガウス分布からギブスサンプリングを使ってサンプリングします。
- [gibbs_sampling.ipynb][gibbs_sampling.ipynb]

## 変分推論
- 二次元ガウス分布に変分推論を適用します。
- [variational_inference.ipynb][variational_inference.ipynb]

[gibbs_sampling.ipynb]:./notebooks/gibbs_sampling.ipynb
[variational_inference.ipynb]:./notebooks/variational_inference.ipynb

## ポアソン混合モデルにおける推論
- 1次元のポアソン混合モデルの事後分布推論の実装です。
- 実装
  - ギブスサンプリングによる事後分布推論 [poisson_mixture_model_gs.ipynb][poisson_mixture_model_gs.ipynb]
  - 変分推論による事後分布推論 [poisson_mixture_model_vi.ipynb][poisson_mixture_model_vi.ipynb]

[poisson_mixture_model_gs.ipynb]:./notebooks/poisson_mixture_model_gs.ipynb
[poisson_mixture_model_vi.ipynb]:./notebooks/poisson_mixture_model_vi.ipynb


## 参考
- [作って遊ぶ機械学習](http://machine-learning.hatenablog.com/entry/2016/02/04/201945)
- [ベイズ推論による機械学習](https://www.kspub.co.jp/book/detail/1538320.html)
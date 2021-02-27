## PyMC3
- PyMC3の練習です。

## 実装
- 状態空間モデル
    - ローカルレベルモデル：[state_space.ipynb][state_space.ipynb]
- 階層ベイズ
    - 階層ベイズによる各国のサッカーの強さの推論: [hierarchical_model.ipynb][hierarchical_model.ipynb]

## Tips
- 下記でmodelのグラフィカルモデルを描画することができます。実行のためには、graphviz本体とgraphvizのPythonラッパーのインストールが必要です。
    ```
    pm.model_to_graphviz(model)
    ```
- `ArviZ`を用いることで、簡単にパラメータの事後分布などを可視化することができます。


## 参考
- [A Hierarchical model for Rugby prediction][A Hierarchical model for Rugby prediction]
- [JFA 2018年W杯アジア最終予選][JFA]

[state_space.ipynb]:./notebooks/state_space.ipynb
[hierarchical_model.ipynb]:./notebooks/hierarchical_model.ipynb
[A Hierarchical model for Rugby prediction]:https://pymc3.readthedocs.io/en/latest/notebooks/rugby_analytics.html
[JFA]:https://www.jfa.jp/samuraiblue/worldcup2018_final_q/schedule_result/
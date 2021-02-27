## PyMC3
- PyMC3の練習です。

## 実装
- 状態空間モデル
    - ローカルレベルモデルの実装：[state_space.ipynb][state_space.ipynb]

## Tips
- 下記でmodelのグラフィカルモデルを描画することができます。実行のためには、graphviz本体とgraphvizのPythonラッパーのインストールが必要です。
    ```
    pm.model_to_graphviz(model)
    ```
- `ArviZ`を用いることで、簡単にパラメータの事後分布などを可視化することができます。


[state_space.ipynb]:./notebooks/state_space.ipynb
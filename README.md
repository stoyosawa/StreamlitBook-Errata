## 『作ってわかる［入門］Streamlit』正誤表

> *Last updated: 2026-03-30

本リポジトリには技術評論社刊『[作ってわかる［入門］Streamlit](https://gihyo.jp/book/2025/978-4-297-14764-8)』（2025年2月）の正誤表および注意事項を示します。


### pip requirements.txt (25-05-08, 26-03-28)

場所： pp. ix, 268, （ダウンロードパッケージの）`Codes/requirements.txt`

誤: `$ pip install transformers["ja"]`

正: `$ pip install transformers[ja]==4.51.3`

- 角カッコの中の文字 `ja` の引用符は不要です。コンソール（`bash`等）での実行では影響はありませんが、`requirements.txt`にそのまま書くとエラーが上がります。
- Hugging Face `transformers` は2026年1月リリースの version 5 で構成が変わったため、本書のコードでは使用したモデルがそのままでは使えなくなりました。本書発行時のバージョンである 4.51.3 で固定して使ってください。


### 7.6節 句読点の挿入（26-03-30）

リスト7.3 `fill_mask.py` は Python 3.9～3.13 でなければ動作しません。`pip install transformers[ja]==4.51.3` で追加でインストールされる [sudachipy](https://pypi.org/project/SudachiPy/#files) の最新版 0.6.10 (2025-01-10) の wheel がそれ以外のバージョンではサポートされていないからです。

Streamlit Community Cloud でも同様です。デフォルトでは（現在）Python 3.14 が用いられるので、設定から 3.12 に変更します。

<img src="260330_python_version.png" width="800">

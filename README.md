## 『作ってわかる［入門］Streamlit』正誤表

> *Last updated: 2025-05-08*

本リポジトリには技術評論社刊『[作ってわかる［入門］Streamlit](https://gihyo.jp/book/2025/978-4-297-14764-8)』（2025年2月）の正誤表を発見順で列挙します。


#### pip requirements.txt

pp. ix, 268, （ダウンロードパッケージの）`Codes/requirements.txt`

誤: `$ pip install transformers["ja"]`

正：`$ pip install transformers[ja]`

角カッコの中の文字（`ja`）の引用符は不要。コンソール（`bash`等）での実行では影響はありませんが、`requirements.txt`にそのまま書くとエラーが上がります。

---
layout: content
transition: none
title: 研究目的
subtitle: フォトウォークデータの生成
---

- **目的：データ生成による解決**
  - 収集困難なデータを，**LLMを用いて生成**することで解決する
  - 同時クラスタリングの入力として耐えうるデータ基盤を構築

- **アプローチと独自性**
  - 既存の空間データ生成（Liら<Cite index="2" />）をフォトウォーク用に拡張
  - **意味的情報の付与**：位置だけでなく「被写体カテゴリ」を生成
  - **制約の遵守**：周回性（Start=End）などの行動制約を保証

<Footer>
<Caption index="2" caption='Li et al. "Large Language Model-Driven Structured Output: A Comprehensive Benchmark and Spatial Data Generation Framework," ISPRS International Journal of Geo-Information, 2024.' />
</Footer>

<!--
そこで本研究では，「データ生成」によってこの問題を解決することを目的とします．
具体的には，LLMを用いて架空のフォトウォークデータを生成します．
Liらの空間データ生成研究を参考にしつつ，本研究独自の点として，
位置情報だけでなく「被写体カテゴリ」という意味情報を付与すること，
そして周回性などの行動制約を確実に守る仕組みを取り入れています．
-->

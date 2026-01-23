---
layout: content
transition: none
title: 実装
subtitle: 実装とモデル選定
---

- **実装環境**
  - Python と Google GenAI SDK による実装
  - 並列処理による高速な大規模データ生成

- **モデル選定の経緯**
  - **Gemini 2.5 Flash**：エリア内という地理的整合性を遵守できない
  - **Gemini 2.5 Flash Lite**：「出発地と到着地が同一」という制約を遵守できない
  - **Gemini 3 Flash Preview**：全ての制約を遵守したため採用

<!--
実装はPythonとGoogle GenAI SDKを使用し，並列処理による高速な大規模データ生成を実現しました．

モデル選定においては，比較実験を行いました．
Gemini 2.5 Flashでは「エリア内」という地理的整合性を遵守できないケースが見られました．
また，Gemini 2.5 Flash Liteでは「出発地点と到着地点が同一」という行動の完結性に関する制約を遵守できませんでした．
最終的に，これらの制約を全て遵守できたGemini 3 Flash Previewを採用しました．
-->

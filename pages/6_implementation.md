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
  - Gemini 2.5 Flash / Lite
    - 地理的整合性が不十分
  - **Gemini 3 Flash Preview を採用**
    - 地理的制約を遵守

<!--
実装はPythonとGoogle GenAI SDKを使用し，並列処理による高速な大規模データ生成を実現しました．
モデル選定では，当初Gemini 2.5 Flash/Liteを試しましたが，地理的整合性に問題がありました．
最終的にGemini 3 Flash Previewを採用し，地理的制約を遵守するようになりました．
-->

---
layout: content
transition: none
title: 提案手法
subtitle: 実装
---

- Python と Google GenAI SDK を使用
- 並行処理による高速なデータ生成
- Gemini 3 Flash Preview を使用
  - Gemini 2.5 Flash Lite: 周回性制約を遵守できない
  - Gemini 2.5 Flash: 地理的整合性を遵守できない

<!--
次に実装の詳細について説明します。

言語は Python を使用し、Google GenAI SDK を介して Gemini API にアクセスしました。
大量のデータを効率的に生成するため、1つのセッションを生成するタスクを並行に処理するように実装しました。

モデルの選定においては、Gemini 3 Flash Preview を採用しました。
比較検討として Gemini 2.5 Flash Lite と Gemini 2.5 Flash も試しましたが、
Flash Lite は周回性制約を遵守できず、
Flash はエリアの指定を遵守できないという結果になりました。
Gemini 3 Flash Preview はこれらの制約を最もよく遵守できました。
-->

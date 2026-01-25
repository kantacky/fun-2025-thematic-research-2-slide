---
layout: content
transition: none
title: 提案手法
subtitle: Gemini API の構造化出力機能を用いたフォトウォークデータ生成
---

# Google Gemini API の構造化出力機能を使用

- コンテキスト容量
- 構造化出力の安定性
- スループット

<!--
-->

---
layout: content
transition: none
title: 提案手法
subtitle: フォトウォークデータに求める要件（スキーマ設計）
---

# Session（1回のフォトウォーク）とRecord（各撮影地点）から構成
- Session: ユーザID, Recordリスト
- Record: 時刻, 緯度・経度, 被写体カテゴリ（landscape, building, vehicle, person, ...）
- それぞれのフィールドの説明を記述

<!--
-->

---
layout: content
transition: none
title: 提案手法
subtitle: フォトウォークデータに求める要件（プロンプト設計）
---

<div class="split">
<div>

# プロンプトに含める条件

- エージェントの役割を明確化
- 周回性
- 地理的整合性
- 生成条件（エリア名，データ規模）

</div>
<div>

# プロンプトの例

```text
あなたは<エリア名>エリアをフォトウォークするエージェントである．
以下の条件に従って，フォトウォークを行いなさい．
- <画像の枚数>枚程度の画像を撮影すること．
- 徒歩<1セッションの時間>分程度の距離を歩くこと．
- 出発地点と到着地点が同一であること．
- 撮影する場所が地図の道路上であること．
```

</div>
</div>

<!--
-->

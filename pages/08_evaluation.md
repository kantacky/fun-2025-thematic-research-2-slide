---
layout: content
transition: none
title: 生成したデータの評価
subtitle: スキーマ準拠
---

あらかじめ指定したスキーマに準拠した出力を得られた

```json
{
  "sessions": [
    {
      "id": "7649d012-780c-4e89-8d19-35a09c279491",
      "user_id": "0aee7cee-6c1b-4983-9bba-b73a48b70724",
      "records": [
        {
          "id": "e305e552-0941-450a-9d62-10f540778f65",
          "timestamp": "2023-10-25T10:00:00Z",
          "latitude": 41.815,
          "longitude": 140.75,
          "category": "landscape"
        },
        ...
```

<!--
-->

---
layout: content
transition: none
title: 生成したデータの評価
subtitle: 地理的整合性
---

<div class="split">
<div>

# 撮影地点が道路上に存在する

- 厳密には道路上ではない撮影地点がある
  - 小数点以下第3位までの精度であり  
    100m程度の誤差が生じる
  - フィールドの説明に加えたが遵守されない

# セッションがエリア内に存在する

- 生成した全てのデータが  
  概ね指定したエリア内に存在する

</div>
<div>

<Image image="https://i.gyazo.com/2f780e47e91f1959ebef7787708e8c32.png" class="w-[80%] mx-auto" />

</div>
</div>

<!--
-->

---
layout: content
transition: none
title: 生成したデータの評価
subtitle: 行動制約の遵守
---

<div class="split">
<div>

# 周回性

- スタート地点とゴール地点が  
  同一地点になるようなセッションが生成される

# 距離・時間

- 1セッションの地点感距離の合計は 1.55 - 5.04 km
- 4.8 km/h で歩いた場合 19 - 63 分
- 30 - 60 分という条件を概ね満たしている
- 道路に沿った距離を計測した場合はさらに長くなる

# 撮影枚数

- 1セッションで撮影された画像は 12 - 21 枚
- 10 - 30 枚という条件を概ね満たしている

</div>
<div>

<Image image="https://i.gyazo.com/2f780e47e91f1959ebef7787708e8c32.png" class="w-[80%] mx-auto" />

</div>
</div>

<!--
-->

---
layout: content
transition: none
title: 生成したデータの評価
subtitle: 多様性
---

<div class="split">
<div>

# 経路の多様性

- 指定したエリア全域にわたって  
  多様な撮影地点が生成される

# 被写体の多様性

- 偏りがなく多様なカテゴリの撮影データが生成される
- 撮影者による偏りがない
  - 撮影者の嗜好を分析するにあたって必要になる

</div>
<div>

<Image image="https://i.gyazo.com/2f780e47e91f1959ebef7787708e8c32.png" class="w-[80%] mx-auto" />

</div>
</div>

<!--
-->

---
layout: content
transition: none
title: 問題と解決策
---

# 座標が小数点以下第3位までの精度

- プロンプトで改善しなかったため今後検討

# 道路に沿った距離が指定した時間を超える

- 撮影地点以外の移動経路も生成させるようにする

# 撮影者による被写体カテゴリの偏りがない

- プロンプトでエージェントに興味を持たせるようにする

<!--
-->

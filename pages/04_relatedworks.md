---
layout: content
transition: none
title: 関連研究
subtitle: LLMによる合成データ生成の信頼性
---

# アンケート回答の再現性

- 多様な背景設定（人種，年齢，政治的思想など）を与えることで  
  実際の人間によるアンケート回答の分布（政治的選好など）を高い精度で再現できる<Cite index="1" />

# 行動シミュレーションの信頼性

- 人間らしい社会的振る舞いや長期的な計画行動を自律的に生成できる<Cite index="2" />

<Footer>
<Caption index="1" caption='L. P. Argyle, E. C. Busby, N. Fulda, J. R. Gubler, C. Rytting, and D. Wingate, “Out of One, Many: Using Language Models to Simulate Human Samples,” Political Analysis, vol. 31, no. 3, pp. 337–351, Feb. 2023.' />
<Caption index="2" caption='J. Park et al., "Generative Agents: Interactive Simulacra of Human Behavior," Proceedings of the 36th Annual ACM Symposium on User Interface Software and Technology, vol. 23, 2023.' />
</Footer>

<!--
関連研究について説明します。
まず、LLMによる合成データ生成の信頼性に関する研究です。

Argyle（アーガイル）らの研究では、LLMに多様な背景設定を与えることで、実際の人間によるアンケート回答の分布を高い精度で再現できることが示されています。
また、Parkらの研究では、LLMを搭載したエージェントが、人間らしい社会的振る舞いや長期的な計画行動を自律的に生成できることが実証されています。

このように，LLMによる人間の行動データを生成する試みが行われており，その信頼性は高まっています．
-->

---
layout: content
transition: none
title: 関連研究
subtitle: 地理空間情報の生成能力
---

# 地理空間推論のための階層的エージェント

- 複雑な地理的クエリをサブゴールに分解し，階層的に処理することで計画と実行を分離<Cite index="1" />
- マップ操作に特化した専用エージェントが複数のAPIを適応的に並列実行し，ツール選択の精度を向上

# 空間検索拡張生成

- 空間データベースによる検索と意味的類似度による検索を統合し，空間制約と意味的関連性のバランスを最適化<Cite index="2" />
- 実世界の観光データセットにおいて，空間的な質問応答の精度を大幅に改善

<Footer>
<Caption index="1" caption='M. H. Hasan, D. M. Labib, T. Hashem, M. E. Ali, and M. R. Parvez, “MapAgent: A Hierarchical Agent for Geospatial Reasoning with Dynamic Map Tool Integration,” arXiv.org, 2025.' />
<Caption index="2" caption='D. Yu, R. Bao, R. Ning, J. Peng, G. Mai, and L. Zhao, “Spatial-RAG: Spatial Retrieval Augmented Generation for Real-World Geospatial Reasoning Questions,” arXiv.org, 2025.' />
</Footer>

<!--
次に、LLMの地理空間情報の生成能力に関する研究です。

MapAgentの研究では、LLMが地図ツールと連携し、階層的な推論を行うことで、複雑な地理的タスクを遂行できることを示しています。これは、LLM単体では難しい正確な空間把握を、ツール利用によって補えることを意味します。
また、Spatial-RAGの研究では、空間的な検索とLLMの生成を組み合わせることで、現実世界の空間に関する質問応答の精度を向上させています。

本研究では，RAGを用いた実装は行なっていませんが，このような空間データベースを利用した地理空間での推論に関する研究も行われています．

これらの関連研究により、LLMが「人間らしい行動の模倣」や「地理空間情報の処理」に有用であることが示されました。
しかし、これらは一般的な移動ログやテキスト生成が中心であり、「特定の被写体を撮影しながら道路上を周回する」という、フォトウォーク特有の複合的な制約を満たすデータの生成については検証されていません。
そこで本提案手法では、Geminiの構造化出力を活用し、これらの制約をプロンプトとして明示的に与えることで、フォトウォークデータの生成を試みます。
-->

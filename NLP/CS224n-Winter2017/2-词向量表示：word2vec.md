# Word Vector Representations: word2vec

## 如何表达一个单词的意义
1. 词典
   1. discrete representation
   2. problem
      1. 丢失了一些细微的差别(Great as a resource but missing nuances)
      2. 无法即使更新(Missing new words	(impossible to keep up to date))
      3. 主观性(Subjctive)
      4. 需要大量人力物力(Requires	human	labor	to	create	and	adapt)
      5. 无法计算单词之间的相似度(Hard	to	compute	accurate	word	similarity	)
   3. one-hot
      1. 每个one-hot表示的词语正交，无法计算相似度
2. 分布相似性
   1. distributional similarity based representation
   2. 通过某个词语的上下文得到其表示的含义。
   3. 通过一个向量去表示一个词，并且可计算各个词中间的相似性。
3. word2vec的主要思想
   1. 两种算法
      1. Skip-grams(SG)
         1. 通过给出的中心词，预测上下文
      2. 连续词袋模型(CBOW)
         1. 通过上下文，预测中心词
   2. 两种训练方法
      1. Hierarchical softmax（分层softmax）
      2. Negative sampling（负采样）
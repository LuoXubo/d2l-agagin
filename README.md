# d2l-agagin

Re-learn dive into deep learning

## Attention mechanisms

* *是否包含自主性提示*是注意力机制与全连接层/汇聚层的主要区别
* 注意力机制通过*注意力汇聚*使选择偏向于值VALUE，其中包含查询QUERY和键KEY
* QUERY-KEY越接近，注意力汇聚的**注意力权重**就越高
* **多头注意力融合**多个注意力汇聚的不同知识
* 比较卷积神经网络、循环神经网络和自注意力

1. CNN：$O(knd^2)$
2. RNN:  $O(nd^2)$
3. Self-attention: $O(n^2d)$

* **自注意力机制**，QUERY、KEY和VALUE来自同一组输入。为了并行计算放弃了顺序操作，因此要加入**位置编码**

* Transformer的编码器和解码器是基于自注意力的模块叠加而成的，输入序列和输出序列的嵌入(embedding)表示将加上位置编码(positional encoding)，再分别输入到编码器和解码器中

* Transformer的解码器在两个子层之间插入了**编码器-解码器注意力层**

* **基于位置的前馈网络**对序列中的所有位置的表示进行变换时使用的是同一个多层感知机(MLP)，是**基于位置**的(positionwise)
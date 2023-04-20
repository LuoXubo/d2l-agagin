# d2l-agagin
Re-learn dive into deep learning

## Attention mechanisms
* *是否包含自主性提示*是注意力机制与全连接层/汇聚层的主要区别
* 注意力机制通过*注意力汇聚*使选择偏向于值VALUE，其中包含查询QUERY和键KEY
* QUERY-KEY越接近，注意力汇聚的**注意力权重**就越高
* **多头注意力融合**多个注意力汇聚的不同知识
* **自注意力机制**，QUERY、KEY和VALUE来自同一组输入。为了并行计算放弃了顺序操作，因此要加入**位置编码**
* 
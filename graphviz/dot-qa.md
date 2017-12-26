# Dot Q&A

## 如何将集群放置在相同的等级上？

*   设置边属性 `constraint=false`，表示边不会影响节点等级。

*   设置图属性 `newrank=true`，这将激活新的排序算法，可以为属于集群的节点定义 `rank=same`。

	`newrank` 属性在 GraphViz 2.30 中添加，而且貌似没有收录到文档中。

参考 [Placing clusters on the same rank in Graphviz](https://stackoverflow.com/questions/6824431/placing-clusters-on-the-same-rank-in-graphviz)。
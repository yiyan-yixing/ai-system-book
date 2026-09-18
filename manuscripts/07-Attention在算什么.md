# 第 7 节 · Attention 在算什么：Q·K、softmax、O(n²)

Q 乘 K，过一层 softmax，再乘 V。这一节把这步算清楚，以及为什么它的代价是 n 的平方。

> 🚧 本节写作中

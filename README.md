# FastLexRank
A streamlined and approximate implementation of the LexRank algorithm for rapid text summarization.

## LexRank for large scale data
The original implementation of LexRank utilizes the power method to calculate the eigenvector associated with an eigenvalue of 1. In the foundational paper by Erkan and Radev[[1]](#1), they mathematically demonstrated why the normalized similarity matrix is a stochastic matrix and will, therefore, converge.

However, a key challenge with the original LexRank algorithm is its dependence on the power method, which often requires multiple iterations to converge. For a large corpus, matrix multiplication can become a bottleneck, slowing down the computation considerably.

To address this issue, we introduce an approximate approach that efficiently computes a score for each sentence while retaining the essential characteristic of relative centrality. Our modified method offers significant speed improvements in LexRank calculations and delivers reliable results.

## Reference
<a id="1">[1]</a>
Erkan, G., & Radev, D. R. (2004). **Lexrank: Graph-based lexical centrality as salience in text summarization**. *Journal of artificial intelligence research*, 22, 457-479.

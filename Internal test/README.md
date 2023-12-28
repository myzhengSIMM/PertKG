## Internal test to find a more generalizable link prediction algorithm
  Considering the standard paradigm of causal reasoning (causal reasoning = predefined prior knowledge network (PKN) + scoring function), an internal test in LINCS Phase I was conducted to identify a more generalizable link prediction algorithm for PertKG's scoring function. In this section, We evaluated 12 algorithms, including 11 link prediction algorithms commonly used in the [Open Graph Benchmark (OGB)](https://ogb.stanford.edu/docs/leader_linkprop/), and KGE_NFM (2021, NC), as it can also be applied to our knowledge graph.
  
## Random mask settings

* Actives_screening
| Method   | MRR | Hits@10  | Hits@30  | Hits@100  |
|--------|------|--------|--------|--------|
| 张三   | 25   | 男     | 男     | 男     |
| 李四   | 30   | 女     | 男     | 男     |
| 王五   | 28   | 男     | 男     | 男     |


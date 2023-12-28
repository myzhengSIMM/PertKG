## Internal test to find a more generalizable link prediction algorithm
Considering the standard paradigm of causal reasoning (causal reasoning = predefined prior knowledge network (PKN) + scoring function), an internal test in LINCS Phase I was conducted to identify a more generalizable link prediction algorithm for PertKG's scoring function. In this section, We evaluated 12 algorithms, including 11 link prediction algorithms commonly used in the [Open Graph Benchmark (OGB)](https://ogb.stanford.edu/docs/leader_linkprop/), and KGE_NFM (2021, NC), as it can also be applied to our knowledge graph.
  
## Random mask settings
* Actives_screening

| Method   | MR | MRR | Hits@10  | Hits@30  | Hits@100  |
|--------|------|------|--------|--------|--------|
| CN   | 1155.2   | 0.179 | 0.291 |0.390 |0.508 |
| AA   | 1136.7   | 0.228 | 0.360 |0.486 |0.583 |
| RA   | 28   | 男     | 男     | 男     |      |
| TransE   | 28   | 男     | 男     | 男     |      |
| TransH   | 28   | 男     | 男     | 男     |      |
| DistMult   | 28   | 男     | 男     | 男     |      |
| ComplEx   | 28   | 男     | 男     | 男     |      |
| GCN   | 28   | 男     | 男     | 男     |      |
| GAT   | 28   | 男     | 男     | 男     |      |
| SAGE   | 28   | 男     | 男     | 男     |      |
| NCN   | 28   | 男     | 男     | 男     |      |
| KGE_NFM   | 28   | 男     | 男     | 男     |      |


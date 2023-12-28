## Internal test to find a more generalizable link prediction algorithm
Considering the standard paradigm of causal reasoning (causal reasoning = predefined prior knowledge network (PKN) + scoring function), an internal test in LINCS Phase I was conducted to identify a more generalizable link prediction algorithm for PertKG's scoring function. In this section, We evaluated 12 algorithms, including 11 link prediction algorithms commonly used in the [Open Graph Benchmark (OGB)](https://ogb.stanford.edu/docs/leader_linkprop/), and KGE_NFM (2021, NC), as it can also be applied to our knowledge graph.
  
## Random mask settings
* Actives_screening

| Method   | MR | MRR | Hits@10  | Hits@30  | Hits@100  |
|--------|------|------|--------|--------|--------|
| CN   | 1155.2   | 0.179 | 0.291 |0.390 |0.508 |
| AA   | 1136.7   | 0.228 | 0.360 |0.486 |0.583 |
| RA   | 1137.4   | 0.219     | 0.351     | 0.471     |0.583      |
| TransE   | 301.6±69.1   |0.063±0.004      | 0.133±0.006     | 0.272±0.005     |0.502±0.012      |
| TransH   | 303.5±59.0   |0.060±0.004     | 0.130±0.008     | 0.273±0.008     |0.500±0.014      |
| DistMult   | 28   | 男     | 男     | 男     |      |
| ComplEx   | 28   | 男     | 男     | 男     |      |
| GCN   | 28   | 男     | 男     | 男     |      |
| GAT   | 28   | 男     | 男     | 男     |      |
| SAGE   | 28   | 男     | 男     | 男     |      |
| NCN   | 28   | 男     | 男     | 男     |      |
| KGE_NFM   | 28   | 男     | 男     | 男     |      |


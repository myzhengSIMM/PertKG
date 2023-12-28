## Internal test to find a more generalizable link prediction algorithm
Considering the standard paradigm of causal reasoning (causal reasoning = predefined prior knowledge network (PKN) + scoring function), an internal test in LINCS Phase I was conducted to identify a more generalizable link prediction algorithm for PertKG's scoring function. In this section, We evaluated 12 algorithms, including 11 link prediction algorithms commonly used in the [Open Graph Benchmark (OGB)](https://ogb.stanford.edu/docs/leader_linkprop/), and KGE_NFM (2021, NC), as it can also be applied to our knowledge graph.

## Implement
Most LP algorithm‘s implement can be find in the OGB, including CN,AA,RA,NCN. KGE methods (TransE/TransH/DistMult/ComplEx) was implement by using TorchKGE, detailes plz refer to our codes. Three commonly used GNN (GCN/GAT/SAGE) was reimplemented by ourselves, each has three gnn layers equiped with linear layers. KGE_NFM was introduced by field recently, we just follow the same settings (hyper-para) in provied code.

## Random mask setting
This setting randomly masking the binding events within the knowledge graph, following an 8:1:1 ratio. To evaluate efficiently, for each masked positive edge, we sampled 3,000 decoys from the corresponding node type respectively. learning-based methods was reruned 5 times to report mean±std.

* Actives screening

| Method   | MR | MRR | Hits@10  | Hits@30  | Hits@100  |
|--------|------|------|--------|--------|--------|
| CN   | 1155.2   | 0.179 | 0.291 |0.390 |0.508 |
| AA   | 1136.7   | 0.228 | 0.360 |0.486 |0.583 |
| RA   | 1137.4   | 0.219     | 0.351     | 0.471     |0.583      |
| TransE   | 301.6±69.1   |0.063±0.004      | 0.133±0.006     | 0.272±0.005     |0.502±0.012      |
| TransH   | 303.5±59.0   |0.060±0.004     | 0.130±0.008     | 0.273±0.008     |0.500±0.014      |
| DistMult   | 267.3±9.2   | 0.146±0.007| 0.262±0.012     | 0.402±0.014     |0.591±0.010      |
| ComplEx   | 249.8±8.6   | 0.121±0.003     | 0.235±0.008     | 0.374±0.013     |0.576±0.012      |
| GCN   |    | 男     | 男     | 男     |      |
| GAT   | 28   | 男     | 男     | 男     |      |
| SAGE   | 28   | 男     | 男     | 男     |      |
| NCN   | 154.3±8.9   |0.290±0.011      | 0.496±0.007     | 0.630±0.005     |0.769±0.010      |
| KGE_NFM   | 28   | 男     | 男     | 男     |      |

* Targets fishing

| Method   | MR | MRR | Hits@10  | Hits@30  | Hits@100  |
|--------|------|------|--------|--------|--------|
| CN   | 1158.3   | 0.024 | 0.022 |0.329 |0.467 |
| AA   | 1140.0   | 0.031 | 0.035 |0.422 |0.597 |
| RA   | 1139.4   | 0.041     | 0.089     | 0.423     |0.595      |
| TransE   | 83.9±1.4   |0.188±0.004      | 0.350±0.006     | 0.564±0.009|0.810±0.004      |
| TransH   | 83.2±1.1   |0.188±0.004     | 0.356±0.005     | 0.571±0.004     |0.815±0.004      |
| DistMult   | 82.9±6.4   | 0.285±0.006| 0.524±0.005     | 0.723±0.002     |0.876±0.004      |
| ComplEx   | 70.9±1.9   | 0.258±0.005     | 0.482±0.011     | 0.693±0.006     |0.869±0.004      |
| GCN   | 111.7±12.8   | 0.223±0.014     | 0.440±0.023     | 0.620±0.016     |0.807±0.012      |
| GAT   | 97.7±5.0   | 0.363±0.015     | 0.628±0.015     | 0.753±0.013     |0.863±0.016      |
| SAGE   | 181.5±39.7   | 0.308±0.015     | 0.578±0.017     | 0.734±0.012     |0.824±0.007      |
| NCN   | 72.0±1.1   |0.367±0.138      | 0.622±0.209     | 0.783±0.010     |0.901±0.005      |
| KGE_NFM   | 72.0±1.1   | 0.367±0.138     | 0.622±0.209     | 男     |      |

## Hard cold-start settings
This settings are more challengable than normal cold-starts (details refer to our papar) to evaluate the generalization capabilities. For convenience, we directly use the model trained under Random masking setting to evaluate the samples in the test set that meet hard cold-start settings.

![](./Extended.4.jpg)

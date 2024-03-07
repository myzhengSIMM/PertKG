# Identify compound-protein interaction with chemical perturbation knowledge graph
The emergence of transcriptomic data provides a new perspective and opportunity for drug discovery. In this work, we present PertKG, a chemical perturbation knowledge graph-based method designed to improve compound-protein interactions prediction from compound-induced transcriptomic data. PertKG incorporates diverse regulatory elements and accounts for multi-level regulatory events within biological systems, leading to significant improvements compared to existing baselines in two critical "cold-start" settings: inferring binding targets for new compounds and conducting virtual ligand screening for new targets. We further demonstrate the pivotal role of incorporating multi-level regulatory events in accurately mapping compound-induced differentially expressed genes to compound-protein interactions. Notably, it enables the identification of ectonucleotide pyrophosphatase-1 as the target responsible for the unique anti-tumor immunotherapy effect of tankyrase inhibitor K-756, and the discovery of five novel hits targeting the emerging cancer therapeutic target, aldehyde dehydrogenase 1B1, with a remarkable hit rate of 10.2%. These findings highlight the potential of PertKG to accelerate drug discovery by elucidating mechanisms of action and identifying novel therapeutic compounds.
![](/fig1.jpg)

## Requirements
Dependencies (with python >= 3.7): 
Main dependencie is [TorchKGE](https://github.com/torchkge-team/torchkge/tree/master)  
Others and detailed version can be touched in requirements.txt

## Data
All the data related to this work is stored on Google Drive for reproducibility and usage.



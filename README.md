# iGEP 

## Identifying cell types and activity programs in simulated scRNA-seq data using Linear CorEx

[Linear CorEx](https://github.com/gregversteeg/LinearCorex) finds latent factors that are as informative as possible about relationships in the data. The approach is described in this paper: [Low Complexity Gaussian Latent Factor Models and a Blessing of Dimensionality](https://arxiv.org/abs/1706.03353). This is useful for covariance estimation, clustering related variables, and dimensionality reduction, especially in the high-dimensional, under-sampled regime.

To install:

```shell
pip install linearcorex
```

In this tutorial, we analyze the synthetic scRNA-seq data with known 13 cell types and 1 acivity program that in expressed across 4 cell types. First, we create an anndata object using the count matrix obtained with Splatter data simulation R package. Then we feed the normalized counts into CorEx algorithm and find latent factors. Finally, we correlate ground truth and CorEx-inferred genes' expression in each GEP. We also visualize each CorEx-inferred GEPs' expression in each cell.

Links to real-world datasets:
The murine dentate gyrus datasets: NCBI GEO [GSE104323](https://www.ncbi.nlm.nih.gov/geo/query/acc.cgi?acc=GSE104323) and [GSE95315](https://www.ncbi.nlm.nih.gov/geo/query/acc.cgi?acc=GSE95315)
The human dentate gyrus dataset: NCBI GEO [GSE186538](https://www.ncbi.nlm.nih.gov/geo/query/acc.cgi?acc=GSE186538)
The mouse embryonic colon development dataset: [GSE154007](https://www.ncbi.nlm.nih.gov/geo/query/acc.cgi?acc=GSE154007)
The mouse adult colon dataset: [GSE151257](https://www.ncbi.nlm.nih.gov/geo/query/acc.cgi?acc=GSE151257)


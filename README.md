# VoxHunt <img src="figures/logo.png" align="right" width="100" />


An R package for projecting single cell transcriptomes to spatial brain maps.


## Introduction 

Brain organoids are complex and can contain cells at various stages of differentiation from different brain structures. Single cell genomic methods provide powerful approaches to explore cell composition, differentiation trajectories, gene regulation, and genetic perturbations in brain organoid systems. VoxHunt is a handy little tool to assess brain organoid patterning, developmental state, and cell composition through systematic comparisons to three-dimensional in situ hybridization data from the Allen Brain Atlas.

<img src="figures/abstract.png" align="center" />


## Installation

Presto, one of VoxHunt dependencies is not on CRAN and has to be installed from GitHub:
```{r}
# install.packages('devtools')
devtools::install_github('immunogenomics/presto')
```
Once Presto is installed, you can install VoxHunt with
```{r}
devtools::install_github('quadbiolab/voxhunt')
```

## Quick start

If you have a `seurat_object` with single cell transcriptomic data of your organoid ready, you can start right away with projecting them to the brain:
```{r}
genes_use <- variable_genes('E13', 300)$gene

```

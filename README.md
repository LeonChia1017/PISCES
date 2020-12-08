---
title: "PISCES Tutorial"
authors: 
 - Lukas Vlahos
 - Pasquale Laise
 - Andrea Califano
---
**Authors:** Lukas Vlahos, Pasquale Laise, Andrea Califano  
**Correspondence:** Pasquale Laise and Andrea Califano  
**Contacts:**

* Lukas Vlahos: lv2395@cumc.columbia.edu
* Pasquale Laise: pl2959@cumc.columbia.edu
* Andrea Califano: ac2248@cumc.columbia.edu

### Introduction

The pipeline for Protein Activity Inference in Single Cells (PISCES) is a regulatory-network-based methdology for the analysis of single cell gene expression profiles.

PISCES transforms highly variable and noisy single cell gene expression profiles into robust and reproducible protein activity profiles. PISCES  is centered around two key algorithms: the Algorithm for the Reconstruction of Accurate Cellular Networks ARACNe [1]; and the algorithm for  Virtual Inference of Protein-activity by Enriched Regulon analysis (VIPER/metaVIPER) [2,3].

Briefly, the ARACNe  algorithm is  one of the most widely used methods for inferring transcriptional interactions from gene expression data. The VIPER algorithm uses the expression of the ARACNe-inferred regulatory targets of a given protein, such as the targets of a transcription factor (TF), as an accurate reporter of its activity. Typically, PISCES  can accurately assess the activity of up to 6000 regulatory proteins  from single cell gene expression profiles,  significantly increasing the ability to analyze the biological function and relevance of gene products whose mRNAs are undetectable in individual cells (e.g. dropout effect).

### Installation

Here's how you can install the PISCES package:

```
install.packages('devtools')
devtools::install_github(repo = "califano-lab/PISCES", force = TRUE, build_vignettes = TRUE)
```

You can then learn about how to use PISCES with our vignettes:

```
library(PISCES)
browseVignettes(package = "PISCES")
```

Some other features we're working on right now:
* Vignette demonstating the functionality of MWKMeans for analyzing trajectories
* Manuscript for citation
* RCPP ARACNe for easier network generation

### References

1.	Lachmann, A., et al., *ARACNe-AP: gene network reverse engineering through adaptive partitioning inference of mutual information*. Bioinformatics, 2016. 32(14): p. 2233-5.  
2.	Califano, H.D.a.A., *iterClust: Iterative Clustering*. R package version 1.4.0. 2018: https://github.com/hd2326/iterClust.  
3.	Ding, H., et al., *Quantitative assessment of protein activity in orphan tissues and single cells using the metaVIPER algorithm*. Nat Commun, 2018. 9(1): p. 1471.  
4.  Rosseeuw, P.J., *Journal of Computational and Applied Mathematics* 20 (1987) 53-65  
5.  Izenman, A.J., *Modern Multivariate Statistical Techniques. Regression, Classification, and Manifold Learning*. Springer text in statistics, 2008 (Chapter 12)

#### Acknowledgements

Jeremy Dooley - for his advice and expertise in single cell sequencing experiments.  
Hongxu Ding - whose work in the Califano laid the groundwork for the development of this pipeline.  
Evan Paull - for help with software and tutorial development and testing.


# CARD+: CARD with your genes of interest
When using CARD, interesting genes are often filtered away. This CARD+ version bypasses the gene selection in two ways that are different from the original version:

1) For the basis matrix, genes are selected with a mean expression level in a given cell type of at least 0.5 (instead of 1.25) log-fold higher than its mean expression level across all remaining cell. This increases the number of genes without generally affecting algorithm quality.
2) Genes of interest can be added by creating a vector 'my.genes' containing your genes of interest. e.g.
``` r
 my.genes = c("GENE1","GENE2")
``` 
Then just run the whole thing like you would run CARD.

To install this version, just run 
``` r
library(devtools)
install_github("NicolaasVanRenne/CARD")
library(CARD)"
``` 
Kind regards and good luck, 

Nicolaas Van Renne

## Spatially Informed Cell Type Deconvolution for Spatial Transcriptomics 

![CARD\_pipeline](Overview.jpg)
We developed a statistical method for spatially informed cell type deconvolution for spatial transcriptomics. Briefly,CARD is a reference-based deconvolution method that estimates cell type composition in spatial transcriptomics based on cell type specific expression information obtained from a reference scRNA-seq data. A key feature of CARD is its ability to accommodate spatial correlation in the cell type composition across tissue locations, enabling accurate and spatially informed cell type deconvolution as well as refined spatial map construction. CARD relies on an efficient optimization algorithm for constrained maximum likelihood estimation and is scalable to spatial transcriptomics with tens of thousands of spatial locations and tens of thousands of genes. CARD is implemented as an open-source R package, freely available at www.xzlab.org/software.html. 

Installation
------------
You can install the released version of CARD from Github with the following code, for more installation details or solutions that might solve related issues (specifically MacOS system) see the [link](https://yingma0107.github.io/CARD/documentation/02_installation.html).

## Dependencies 
* R version >= 4.0.0.
* R packages: SingleCellExperiment, SummarizedExperiment, concaveman, sp, Matrix, methods, ggplot2, ggcorrplot, MuSiC, fields, MCMCpack, dplyr, sf, RANN, stats, reshape2, RColorBrewe, scatterpie, grDevices, stats, nnls, pbmcapply, spatstat, gtools, RcppML, NMF

``` r
# install devtools if necessary
install.packages('devtools')

# install the CARD package
devtools::install_github('YingMa0107/CARD')

# load package
library(CARD)

```
The R package has been installed successfully on Operating systems: 
* macOS Catalina 10.15, macOS Monterey 12.3.1
* Ubuntu 18.04.5 LTS (Bionic Beaver) 
* Windows 10

# Issues
All feedback, bug reports and suggestions are warmly welcomed! Please make sure to raise issues with a detailed and reproducible exmple and also please provide the output of your sessionInfo() in R! 

How to cite `CARD`
-------------------
Ying Ma, Xiang Zhou#. Spatially Informed Cell Type Deconvolution for Spatial Transcriptomics, 2021. 

How to use `CARD`
-------------------
Details in [Tutorial](https://yingma0107.github.io/CARD/)

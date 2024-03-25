BiocManager::install("ggplot2")		#v2_3.4.3 
BiocManager::install("readxl")		#v1.4.3
BiocManager::install("ggrepel")		#v0.9.3
BiocManager::install("tidyverse")		#v2.0.0
BiocManager::install("RColorBrewer")		#v1.1.3
BiocManager::install("ggsci")			#v3.0.0
BiocManager::install("stringr")		#v1.5.0
BiocManager::install("PerformanceAnalytics")		#v2.0.4
BiocManager::install("reshape2")		#v1.4.4
BiocManager::install("pheatmap")		#v1.0.12
BiocManager::install("showtext")		#v0.9.6
BiocManager::install("corrplot")		#v0.92
BiocManager::install("Matrix")		#v1.6.1.1
BiocManager::install("ggraph")		#v2.1.0
BiocManager::install("igraph")		#v1.5.1
BiocManager::install("clusterProfiler")		#v4.8.3
BiocManager::install("enrichplot")		#v1.20.3

install.packages("D:/project/rpackages/BaseMet_1.01.tar.gz", repos = NULL, type = "source")
library(BaseMet)
getwd(
  
)
setwd("D:/project/rpackages/")

input_martix="test.xlsx"
ALLsample="ALLTYPE.txt"
group_sample="TYPE.txt"
foldChange=0.585
padj=0.05
SELECT="PValue"# or FDR
group_meta="Type2.xlsx"

pca_plot(input_martix,ALLsample)
call_diff(group_sample, input_martix)
heatmap_cor(group_sample, input_martix,group_meta)
pie_plot(group_meta)
QC_plot(group_sample, input_martix)
ggraph_plot(input_martix,group_meta,group_sample)
kegg_plot(input_martix,group_meta,group_sample)

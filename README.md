ScRNA-sequencing:
Single-Cell RNA-Seq provides transcriptional profiling of thousands of individual cells. 
This level of throughput analysis enables researchers to understand at the single-cell level what genes are expressed, 
in what quantities, and how they differ across thousands of cells within a heterogeneous sample.


Analysis:
Analysis is done using R.
where we used the Seurat R package for analysis.
A toolkit for quality control, analysis, and exploration of single cell RNA sequencing data. 
Seurat aims to enable users to identify and interpret sources of heterogeneity from single cell transcriptomic measurements, 
and to integrate diverse types of single cell data.


Interpretation:
Find relationships between features: 
1. nFeature_RNA and nCount_RNA
![image](https://user-images.githubusercontent.com/112052476/199076175-2fcf2f66-0bbb-4c10-b988-bf96a9d0b252.png)
where the correlation between them is 0.95

2. percent.mt and nCount_RNA
![image](https://user-images.githubusercontent.com/112052476/199160472-67af677b-73e6-45b3-82f0-55cb0d537e49.png)
where the correlation between them is -0.13

3. plot variable features without labels:
![image](https://user-images.githubusercontent.com/112052476/199160643-e33e8ac9-4584-4a31-a0aa-fdaee4623bc8.png)


Dimheatmap:
In particular DimHeatmap allows for easy exploration of the primary sources of heterogeneity in a dataset, 
and can be useful when trying to decide which PCs to include for further downstream analyses. 
Both cells and features are ordered according to their PCA scores. 
Setting cells to a number plots the 'extreme' cells on both ends of the spectrum, which dramatically speeds plotting for large datasets
![image](https://user-images.githubusercontent.com/112052476/199161155-98a89b12-7a1a-4972-97f2-1fdd6d3566b9.png)

![image](https://user-images.githubusercontent.com/112052476/199161236-ec82e319-0554-4dd6-8207-6c922f70250d.png)
Elbow starts appearing by pc5-10 . So it indicates that first 10 PCs are acceptable as majority of true signal is captured in the first 10 PCs .

Dimplot of clusters using UMAP:
1. Using UMAP method clusters of cells with features that are very similar to each other are created with labels and without labels:
![image](https://user-images.githubusercontent.com/112052476/199161510-85db91b2-7ce4-40f2-b74a-6d5b568f7ba5.png)
![image](https://user-images.githubusercontent.com/112052476/199161678-b3f2ed5a-c09d-4639-b40b-921f0ce0fd77.png)

2. Assign markers to the clustered data
![image](https://user-images.githubusercontent.com/112052476/199161859-60316f51-6479-4677-a076-475277ebe72b.png)
Concluding that the Cell type identification based on single-cell RNA sequencing involves partitioning the data into “clusters” of single cells.
Based on this , 2 clusters were created .Based on those clusters , LDH and CCR7 are highly expressed genes in single-cell RNA data .




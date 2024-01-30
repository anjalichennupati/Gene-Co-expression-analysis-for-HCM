This file gives and outline of the project. It describes what is flow of operations in this project.
The project is the implementation of WGCNA for HCM. It has been implemented on Python Jupyter.
The neccesary packages must be imported form R and R must be installed to successfully run this code.


1)	Dataset :
•	The chosen dataset is GSE36961.
•	The dataset contains 145 samples with different details for Hypertrophic Cardiomyopathy

2)	R-packages :
•	Several R packages have been imported into python such as WGCNA, stats, DESeq2 and base.
•	Each of them are used for performing different analysis and visualization processes.

3)	Pre-processing :
•	The metadata is the original data which contains count values of genes with their respective gene samples.
•	Phenodata is basically the data combined with certain additional details such as gender, disease state etc.
•	Phenodata is then filtered to only columns of considerable data.
•	Counts are now displayed for their respective geo accession ids.

4)	Outlier detection:
•	goodSamplegenes() is an inbuilt function in the WGCNA packages of R which is used to detected outliers. The results are summarized and filtered based on quality. The filtered genes are then used to filter the data.
•	Identifying outliers are computed using two methods :
a.	Hierarchical clustering :
•	Hierarchical clustering is performed on the transposed data matrix, and a dendrogram is plotted using scipy.cluster.hierarchy and matplotlib.pyplot.
b.	PCA ( Principal Component Analysis ) :
•	PCA is performed on the transposed data matrix using sklearn.decomposition.
•	The PCA results are accessed and stored in a pandas DataFrame named pca_dat. The explained variance ratio is calculated.
•	A scatter plot of the first two principal components (PC1 and PC2) is plotted using matplotlib.pyplot.scatter(). Labels corresponding to the samples are added to the plot.
•	Outlier samples are excluded from the data

5)	Normalization:
•	A DESeq2 dataset is created from the normalized data subset and the sample metadata. Genes with low counts are removed based on a count threshold.
•	Variance stabilization is performed on the DESeq2 dataset.
•	Normalized counts are obtained from the DESeq2 dataset and stored in a pandas DataFrame.

6)	Network Construction:
•	A set of soft-thresholding powers is chosen, and the network topology analysis is performed. The results are visualized using matplotlib and seaborn.
•	The blockwiseModules function returns a set of modules.

7)	Module Eigengenes :
•	They are the first principal component of the expression matrix of the corresponding module.
•	The module eigengenes are extracted and stored in a pandas DataFrame.
•	The number of genes in each module is counted and stored.
•	The dendrogram and module colours are plotted.

8)	Identifying driver genes :
•	Trait information is prepared, binarizing categorical variables. Correlation analysis between modules and traits is performed.
•	Module-gene mapping is stored in a pandas DataFrame.

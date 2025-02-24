
# Weighted Gene Co-Expression Analysis for HCM

# Overview

This project implements Weighted Gene Co-expression Network Analysis (WGCNA) for Hypertrophic Cardiomyopathy (HCM) using a dataset from GEO-NCBI (GSE36961). The analysis involves gene expression profiling of 145 samples, preprocessing, outlier detection, network construction, and identifying driver genes. The results are visualized using hierarchical clustering, PCA, and correlation heatmaps, helping to identify key biomarkers for HCM.




## Block Diagram

- The below block diagram gives an overview of the overall funtionality of the implemented project
 <p align="center">
  <img src="https://i.postimg.cc/Wzwb0YDT/Picture11.png" alt="App Screenshot" width="600">
</p>

## Features

- **Outlier Detection using PCA & Clustering**: Outliers are identified using Principal Component Analysis (PCA) and hierarchical clustering. This step ensures high-quality data by removing noise and irrelevant samples.
 <p align="center">
  <img src="https://i.postimg.cc/3xHNz7Zn/Picture10.png" alt="App Screenshot" width="500">
</p>


- **Driver Gene Identification & Visualization**: Correlation analysis is performed to identify key genes (hub genes) linked to HCM. These results are visualized using correlation heatmaps and eigengene plots.
  <p align="center">
  <img src="https://i.postimg.cc/7hm9dXFN/Picture9.png" alt="App Screenshot" width="500">
</p>

- **Correlation of the first 25 samples**: correlation values of the first 25 gene sample from the dataset of which sample number 7 and 13 have relatively higher correlation values than the remaining. These values are computed by taking various other parameters into consideration. The higher correlation values indicated that those are the gene samples that where a higher risk for HCM is identified. These genes with high correlation can be identified as the hub genes and placed into the cluster with high correlation.
 <p align="center">
  <img src="https://i.postimg.cc/L8HRzsDK/Picture8.png" alt="App Screenshot" width="150">
</p>


## Tech Stack

- **Programming Language**: Python
- **Libraries**: pandas, numpy, matplotlib, seaborn, sklearn, rpy2
- **R Packages Used**: WGCNA, stats, DESeq2, base

## Installation

1. **Install Dependencies**:
- This project was implemented on Google Colab
- Upload the required dataset files to Colab or mount Google Drive.
- Run the cells step by step to execute the workflow.
- Ensure R and rpy2 are installed in Colab before executing the analysis.

2. **Dataset**: Download the dataset (GSE36961) from GEO-NCBI and place it in the appropriate directory.
https://www.ncbi.nlm.nih.gov/geo/query/acc.cgi?acc=GSE36961



## Running Tests

The project can be implemented and tested to verify funtionality


# SociallyFairKMeans
Matlab implementation of the Fair Lloyd algorithm introduced in "Socially Fair 𝑘-Means Clustering" paper. Read the full paper at https://arxiv.org/pdf/2006.10085.pdf


Description of the folders and files:

- Folder "Fair Lloyd": this folder contains all the main functions. 

-- bSearch : computing fair centers using a binary search (section 2.2)

-- compCost : computing fair or vanilla k-means cost of a clustering (based on the value of isFair variable)

-- fairPCA: the fair PCA projection of the data to featureNum dimensions. For details of the fairPCA code, please look at https://github.com/samirasamadi/Fair-PCA

-- findCenters: given a clustering of the data, computers vanilla or fair centers (based on the value of isFair variable)

-- findClustering: given k centers, find the vanilla or fair clustering (based on the value of isFair variable)

-- giveRandCenters: initializes k random centers

-- kmeansCost_S_C: given a set of clusters and a set of arbitrary centers (centers might not be the average of clusters), calculate the kmeans cost

-- Lloyd: Lloyd algorithm. Choose the best among bestOutOf different center initializations. numIters is the number of iteartions for each center initialization.

-- LoadData: oads the datasets that we are using in our experiments. For description of the datasets please refer to section 4 (compasWB was ultimately not used, ignore it)

-- mainK: Lloyd's versus Fair Lloyd for number of clusters = k. 

-- mw: multiplicative weight update algorithm. Used in fair PCA.

-- normalizeData: normalize the mean and standard deviation of the data

-- optApprox: the optimal rank d PCA approximation of matrix M. Used in fair PCA. 

-- preProcessEductaionVector: converts the education vector for the credit dataset to high-educated and low-educated. 

-- projectData: projects the high dimensional data into numFeatures dimension either using PCA or fair PCA. Referred to as pre-processing in section 4. 

-- re: Calculate the reconstruction error of matrix Y with respect to matrix Z. Used in fair PCA. 



- Folder "plotsCode": this folder contains the specific codes for plotting the results. 


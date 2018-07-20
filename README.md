Speaker Recognition System Scoring Backend
======================================
*Reference code for CSLT @Tsinghua University*

Project summary is in `Scoring-Task-Review.pdf`.

### Important notebooks
1. `Variable EER.ipynb` - Final summary and compilation of individual factor + factor combination experiments. 
    - **This notebook has the latest versions of all functions**
2. `Data Processing.ipynb` - Contains functions that process .ark and .spk2utt files into formatted h5 files. 
    - Shows results of cosine similarity baseline EER 
    - the function `ark_to_hdf5` computes the normalized means for each utterance. 
    - **This notebook contains older code**
3. `Similarity Test KL.ipynb` - Development on KL-divergence factor
    - Contains the `ark_to_hdf5_raw` function that directly translates .ark files to a MultiIndex h5 dataset. (It is in this notebook because this function wasn't needed until now)
4. `Similarity Test Stats.ipynb` - Contains early work on Z-score & KL-div, also trials of Mahalanobis with PCA. 
    - This notebook generally does not have new code
5. `Similarity Tests Mahalanobis.ipynb` - More thorough trials of Mahalanobis distance - proves to yield about 50% EER. 
6. `Similarity Test Manhattan.ipynb` - Contains trials of Manhattan distance. A potentially good distance metric for high-dimensional data.  

#### Not so important notebooks 
Some notebooks for the archive: 

1. `Similarity Tests.ipynb` - Early attempts at topics mentioned above. Also contains results of SVM, RF methods mentioned in paper. 
2. `Similarity Tests ML.ipynb` - Brief attempts at further ML. Progress halted due to change of direction. 

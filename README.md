# Comparative Study of Image Anomaly Detection

This repository contains a comparative study of **image anomaly detection** using multiple machine learning (ML) and deep learning (DL) methods.  
We evaluated five unsupervised anomaly detection techniques on two subsets of the **MVTec AD dataset** (Hazelnut and Carpet).  

## Project Overview
- **Objective**: Investigate effective methods for unsupervised image anomaly detection in industrial settings.  
- **Datasets**:  
  - **Hazelnut**: 391 normal training images, 110 test images (4 defect types).  
  - **Carpet**: 280 normal training patches, 117 test patches (5 defect types).  
- **Methods compared**:
  1. DBSCAN (Density-based)  
  2. One-Class SVM (Boundary-based)  
  3. Isolation Forest (Tree-based)  
  4. Autoencoder (Reconstruction-based)  
  5. PatchCore (Distance-based, patch-level)

All methods were trained only on **normal data** (unsupervised setting).  
Evaluation metrics include **F1 Score, Precision, Recall, ROC-AUC, PR-AUC**.
* Note: This is a course team project.
---

## Repository Structure
```
** image-anomaly-detection **
┣ appendix_dbscan.ipynb # DBSCAN implementation
┣ appendix_oneclasssvm.ipynb # One-Class SVM implementation
┣ appendix_isolationforest.ipynb # Isolation Forest implementation
┣ appendix_autoencoder.ipynb # Autoencoder implementation
┣ appendix_patchcore.ipynb # PatchCore implementation
┣ 1st Group_Anomaly Detection Presentation.pdf # project presentation slides with explanations
┗ README.md
'''
### Appendix Notebooks
All five methods are provided as **separate code-only notebooks** in the root directory of this repository.  
Detailed explanations, methodology, and result interpretation are documented in the **presentation PDF**.  

- `appendix_dbscan.ipynb` – DBSCAN (Density-based)  
- `appendix_oneclasssvm.ipynb` – One-Class SVM (Boundary-based)  
- `appendix_isolationforest.ipynb` – Isolation Forest (Tree-based)  
- `appendix_autoencoder.ipynb` – Autoencoder (Reconstruction-based)  
- `appendix_patchcore.ipynb` – PatchCore (Distance-based)  

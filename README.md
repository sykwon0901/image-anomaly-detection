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

---

## Repository Structure
```
** image-anomaly-detection **
┣ Appendix_Dataset/ # dataset sample images or download instructions
┣ Autoencoder.ipynb # Autoencoder implementation
┣ DBSCAN.ipynb # DBSCAN clustering implementation
┣ Isolation Forest.ipynb # Isolation Forest implementation
┣ One Class SVM.ipynb # One-Class SVM implementation
┣ Patchcore.ipynb # PatchCore implementation
┣ 1st Group_Anomaly Detection Presentation.pdf # project presentation slides
┗ README.md
'''

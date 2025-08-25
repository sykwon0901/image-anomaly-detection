# Comparative Study of Image Anomaly Detection

This repository contains a comparative study of **image anomaly detection** using multiple machine learning (ML) and deep learning (DL) methods.  
We evaluated five unsupervised anomaly detection techniques on two subsets of the **MVTec AD dataset** (Hazelnut and Carpet).  

---

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
'''
image-anomaly-detection
┣ appendix_dbscan.ipynb # DBSCAN (Density-based)
┣ appendix_oneclasssvm.ipynb # One-Class SVM (Boundary-based)
┣ appendix_isolationforest.ipynb # Isolation Forest (Tree-based)
┣ appendix_autoencoder.ipynb # Autoencoder (Reconstruction-based)
┣ appendix_patchcore.ipynb # PatchCore (Distance-based)
┣ 1st Group_Anomaly Detection Presentation.pdf # project presentation slides with explanations
┗ README.md
'''
* Note: All five methods are provided as **separate code-only notebooks** in the root directory of this repository.  
Detailed explanations, methodology, and result interpretation are documented in the **presentation PDF**.  

---

## Results Summary

| Dataset   | Method          | Accuracy | Precision | Recall | F1 Score | ROC AUC | PR AUC |
|-----------|-----------------|----------|-----------|--------|----------|---------|--------|
| Hazelnut  | One-Class SVM   | 0.80     | 0.77      | **0.97** | **0.86** | 0.94    | 0.97   |
|           | Isolation Forest| 0.71     | **0.98**  | 0.56   | 0.71     | 0.90    | 0.95   |
|           | PatchCore       | 0.76     | 0.84      | 0.81   | 0.81     | 0.79    | 0.90   |
|           | Autoencoder     | 0.80     | 1.00      | 0.51   | 0.68     | 0.85    | 0.80   |
|           | DBSCAN          | 0.64     | 0.64      | 1.00   | 0.78     | 0.95    | 0.97   |
| Carpet    | One-Class SVM   | 0.76     | 0.77      | **0.99** | **0.86** | 0.60    | 0.85   |
|           | Isolation Forest| 0.63     | 0.81      | 0.66   | 0.73     | 0.67    | 0.88   |
|           | PatchCore       | **0.89** | 0.75      | 0.81   | 0.81     | 0.77    | 0.90   |
|           | Autoencoder     | 0.52     | 0.31      | 0.32   | 0.32     | 0.50    | 0.42   |

**Ranking (Image-level F1 performance):**  
PatchCore > One-Class SVM > Isolation Forest > Autoencoder > DBSCAN

---

## Key Insights
- **PatchCore** consistently achieved strong results across both datasets, with pixel-level anomaly maps.  
- **One-Class SVM** excelled on Hazelnut (PR AUC 0.97) but struggled on Carpet due to high texture variability.  
- **Isolation Forest** balanced performance well, though recall was moderate.  
- **Autoencoder** worked reasonably on Hazelnut but failed on Carpet due to small sample size.  
- **DBSCAN** was unreliable without domain-specific embeddings.
  
---

## Applications
- **Autoencoder**: Semiconductor wafer defect detection, medical image screening.  
- **One-Class SVM**: Fraud detection, network intrusion detection.  
- **Isolation Forest**: Real-time IoT and manufacturing anomaly alarms.  
- **DBSCAN**: Clustering-based defect detection in point clouds.  
- **PatchCore**: Industrial inspection with defect localization (PCB solder joints, assembly lines).
  
---

## How to Run
1. Clone the repo:
   ```bash
   git clone https://github.com/username/image-anomaly-detection.git
   cd image-anomaly-detection

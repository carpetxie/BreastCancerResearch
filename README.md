*Cumulative research comparing machine learning models on breast cancer classification (benign, malignant, normal) without using regions of interest (ROI), which are often used in breast cancer classification.*

---

# Breast Cancer Classification with Machine Learning

Spring 2024 Research Project  
By Krish Badri, Leah Parparov, and Jeffrey Xie  

---

## Paper

The corresponding paper is linked here:  
https://www.linkedin.com/in/jeffreyxiekl/overlay/1723089641788/single-media-viewer/?profileId=ACoAAEL4pUsBzQhrvhH3IyWZmWD7XO_cCuKrRT0

---

## Abstract

This project evaluates several Scikit-Learn machine learning models for classifying breast cancer from ultrasound images without regions of interest (ROI) masks. Motivated by resource-limited clinical settings, we compare five classifiers—Logistic Regression, MLP Classifier, Support Vector Classifier, Random Forest, and Gradient Boosting—on a dataset of 780 images.

- Best-performing model: Random Forest  
- Accuracy: 78.43%  
- AUC-ROC: 0.86  

The results suggest that relatively simple ML pipelines can provide reasonably strong diagnostic performance without ROI segmentation, potentially improving accessibility in low-resource environments.

---

## Dataset

- 780 ultrasound images labeled as **normal**, **benign**, or **malignant**
- Preprocessing steps:
  - Images cropped and resized to 300×300 pixels  
  - Converted to grayscale  
  - Labels encoded as:
    - `0 = Benign`  
    - `1 = Malignant`  
    - `2 = Normal`  

---

## Methodology

### Models Evaluated
1. Logistic Regression  
2. MLP Classifier (feedforward neural network)  
3. Support Vector Classifier  
4. Random Forest  
5. Gradient Boosting  

### Evaluation Metrics
- Accuracy  
- Precision  
- Recall  
- F1 Score  
- ROC-AUC  

### Training and Evaluation
- 5-fold cross-validation  
- Confusion matrices and ROC curves used for comparative analysis  

---

## Results

| Model                  | Accuracy | Precision | Recall | F1 Score | AUC-ROC |
|------------------------|----------|-----------|--------|----------|---------|
| Random Forest          | 78.43%   | 75.37%    | 74.50% | 73.69%   | 0.86    |
| MLP Classifier (NN)    | 74.50%   | 84.25%    | 74.50% | 74.36%   | 0.72    |
| Logistic Regression    | 72.00%   | 73.49%    | 72.00% | 70.48%   | 0.77    |
| Support Vector Machine | 71.50%   | 72.30%    | 71.50% | 69.62%   | 0.84    |
| Gradient Boosting      | 72.00%   | 73.18%    | 72.00% | 70.65%   | 0.84    |

Visual results (in `/results` directory):
- Confusion matrices  
- ROC curve comparisons  

---

## Impact and Future Work

This project supports diagnostic workflows in underserved and low-resource regions where ROI segmentation or advanced compute is not always feasible.

Planned future improvements include:
- Addressing class imbalance using SMOTE  
- Exploring deep learning frameworks such as PyTorch or TensorFlow  
- Integrating additional patient or contextual data  

---

## Technologies Used

- **Language**: Python  
- **Libraries**: Scikit-Learn, NumPy, Pandas, Matplotlib  

---

## Team Contributions

- **Jeffrey Xie**: Implemented Random Forest, Logistic Regression, and MLP; built K-Fold pipeline; analysis, visualizations, abstract, and discussion writing  
- **Leah Parparov**: Literature review, ethical considerations, conclusion writing  
- **Krish Badri**: Implemented SVM and Gradient Boosting; introduction; LaTeX formatting  

---

## Repository Structure

- `data/`: Dataset and preprocessing scripts  
- `models/`: Model training and evaluation code  
- `results/`: ROC curves, confusion matrices, performance metrics  

---

## Contact

For inquiries, contact: **jeffrey.xie.28@dartmouth.edu**

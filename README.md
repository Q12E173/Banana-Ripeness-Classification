# Banana Ripeness Classification

## Overview

This project develops a machine learning-based system for classifying banana ripeness into four categories: **Unripe, Semi-ripe, Ripe, and Overripe-Rotten**.

The project investigates the impact of different image preprocessing techniques on classification performance and compares three machine learning models: **Support Vector Machine (SVM), Random Forest, and AdaBoost**.

The system aims to provide an automated approach to banana ripeness assessment, with potential applications in agriculture, retail, inventory management, and food waste reduction.

---

## Objectives

The main objectives of this project are to:

- Develop a machine learning-based system for banana ripeness classification.
- Compare the effectiveness of SVM, Random Forest, and AdaBoost models.
- Investigate the impact of different image preprocessing techniques on model performance.
- Evaluate model performance using both conventional test data and real-world banana images.
- Explore the potential application of automated ripeness classification in agricultural and retail environments.

---

## Dataset

The training dataset consists of **1,400 banana images**, categorized into four ripeness classes:

- **Unripe**
- **Semi-ripe**
- **Ripe**
- **Overripe-Rotten**

The training dataset was divided into:

- 80% Training
- 20% Testing

For real-world evaluation, a self-collected dataset was used. From the 800 self-collected images, **280 images** were selected for testing, with **70 images from each ripeness class**.

The self-collected images were captured under different lighting conditions, viewing angles, and backgrounds to represent real-world variations.

All images were resized to **224 × 224 pixels** before model training.

---

## Methodology

The overall workflow consists of the following stages:

1. Dataset Collection
2. Image Preprocessing
3. Image Segmentation
4. Feature Extraction
5. Model Training
6. Model Evaluation

The project investigates image characteristics such as:

- Color
- Texture
- Shape

These features are used to help distinguish different banana ripeness stages.

---

## Image Preprocessing

Three different preprocessing methods were investigated and compared with a baseline experiment without preprocessing.

### Preprocessing Method 1

The first preprocessing method includes:

- Fast Non-Local Means Denoising
- CLAHE Contrast Enhancement
- HSV Color Space Conversion
- HSV Masking
- Morphological Operations
- Binary Thresholding
- Contour Detection

This method focuses on reducing image noise, improving contrast, and isolating the banana from its background.

### Preprocessing Method 2

The second preprocessing method includes:

- LAB Color Space Brightness Normalization
- CLAHE Contrast Enhancement
- GrabCut Segmentation
- Morphological Operations

This method focuses on improving lighting consistency and separating the banana from the background.

### Preprocessing Method 3

The third preprocessing method includes:

- Gamma Correction
- CLAHE Contrast Enhancement
- Median Filtering
- HSV Masking
- Improved GrabCut Segmentation
- Mask Post-processing

This method combines brightness adjustment, noise reduction, color-based segmentation, and background removal.

---

## Machine Learning Models

Three machine learning classifiers were implemented.

### Support Vector Machine (SVM)

A linear SVM classifier was used with a regularization parameter of **C = 1.0**.

### Random Forest

A Random Forest classifier was implemented using:

- 100 estimators
- Random state = 42

Random Forest was selected as an ensemble learning approach to improve classification stability and reduce overfitting.

### AdaBoost

AdaBoost was implemented using:

- Decision Tree as the weak learner
- Maximum tree depth = 1
- 50 estimators
- Learning rate = 1.0

---

## Experimental Design

The models were evaluated under four experimental conditions:

1. Without preprocessing
2. Preprocessing Method 1
3. Preprocessing Method 2
4. Preprocessing Method 3

Each preprocessing condition was evaluated using:

- SVM
- Random Forest
- AdaBoost

This allows the effect of different preprocessing techniques on different machine learning models to be compared.

---

## Evaluation Metrics

The models were evaluated using:

- Accuracy
- Precision
- Recall
- F1-score
- Confusion Matrix

Both the conventional test dataset and the real-world self-collected dataset were used to evaluate model performance.

---

## Results

The experiments demonstrated that different preprocessing techniques affected each machine learning model differently.

### Training and Testing Performance

Random Forest demonstrated the most stable performance across the experiments.

The best overall classifier reported in this study was **Random Forest**, achieving an accuracy of **86.79%**.

The experiments also showed that preprocessing methods can have different effects depending on the machine learning model being used.

For real-world testing, Random Forest maintained relatively stable performance compared with SVM and AdaBoost, demonstrating better robustness across different preprocessing conditions.

---

## Real-World Applications

The proposed banana ripeness classification system has potential applications in:

- Automated banana sorting
- Supermarket inventory management
- Agricultural quality control
- Supply chain management
- Ripeness monitoring
- Food waste reduction
- Food processing

The system could potentially be integrated with camera-based sorting systems or mobile applications to assist farmers, retailers, and other users in assessing banana ripeness.

---

## Limitations and Future Improvements

Potential improvements identified in the project include:

- Increasing the size and diversity of the dataset
- Applying data augmentation
- Improving feature selection
- Performing further hyperparameter tuning
- Using cross-validation
- Exploring deep learning models such as CNNs
- Investigating pretrained deep learning models
- Developing ensemble models
- Exploring edge computing for real-time deployment

These improvements could help increase model robustness and generalization to different real-world environments.

---

## Technologies

- Python
- Jupyter Notebook
- Google Colab
- Scikit-learn
- NumPy
- Pandas
- Matplotlib
- Computer Vision
- Machine Learning

---


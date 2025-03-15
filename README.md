# PhiUSIIL-A-Machine-Learning-Based-Phishing-URL-Classifier

### Problem Description :
With the increasing reliance on the internet for financial transactions, personal communications, and business operations, phishing attacks have emerged as a significant cybersecurity threat. Phishing websites impersonate legitimate entities to deceive users into revealing sensitive information, such as passwords, credit card details, and personal data.

Detecting phishing websites accurately and efficiently is a crucial challenge in cybersecurity. Traditional methods, such as blacklists, fail to detect new phishing sites in real time. Therefore, machine learning-based approaches using URL and webpage source code features have gained prominence in identifying phishing threats proactively.

In this project, we utilize the PhiUSIIL Phishing URL Dataset, which contains 134,850 legitimate URLs and 100,945 phishing URLs, to develop a robust phishing detection model. The dataset includes features extracted from the webpage source code and URL structure, such as CharContinuationRate, URLTitleMatchScore, URLCharProb, and TLDLegitimateProb, which are derived from existing URL-based attributes.

### Objective :
To analyze these features and implement machine learning techniques to classify URLs as legitimate or phishing, improving the accuracy and efficiency of phishing detection systems. Through this project, we aim to contribute to the development of automated security solutions that help protect users from online fraud and cyber threats.

### DataSet :
(https://archive.ics.uci.edu/dataset/967/phiusiil+phishing+url+dataset)

## Data Preprocessing

### Handling Missing and Duplicate Values
- Checked for null values and duplicate records, ensuring a clean dataset.

### Exploratory Data Analysis (EDA)
- **Univariate Analysis**: Examined individual feature distributions.
- **Bivariate Analysis**: Analyzed relationships between two variables.
- **Multivariate Analysis**: Explored interactions among multiple features.
- **Skewness Correction**: Applied transformations to normalize skewed features.
- **Final Cleaned Dataset**: Prepared a refined dataset for further processing.

## Feature Engineering

### Encoding Categorical Features
- Converted categorical data into numerical format where necessary.

### Feature Selection
- Used the **SelectKBest** method to select the most relevant features.
- Applied the **Elbow Method** to determine the optimal number of features (k).
- Selected **50,000 random instances** for model training and evaluation.

### Feature Scaling
- Standardized features to ensure uniformity.

### Dimensionality Reduction
- Applied **Principal Component Analysis (PCA)** to reduce the dataset to **10 features**.

## Model Training and Evaluation

### Train-Test Split
- Divided the dataset into training and test sets.

### Machine Learning Models Used
- **Random Forest**
- **XGBoost**
- **Support Vector Machine (SVM)**
- **Decision Tree (Two variations)**
- **Logistic Regression**

### Evaluation Metrics
- **Accuracy**
- **Precision, Recall, and F1-Score**
- **Training vs. Test Accuracy Comparison**
- **Overfitting Issue**: Initially observed overfitting in some models.

## Hyperparameter Tuning

- Applied hyperparameter tuning to all models to improve performance.

### Best Performing Model
- **Decision Tree** achieved an accuracy of **97%** after tuning.

### Final Model Validation
- Compared training and test accuracy to confirm model performance and generalization.
- 
### Limitations of the model:
* Generalization Issues – Might fail on new phishing techniques or domains not in training data.
* Class Imbalance – If legitimate URLs dominate, the model may favor non-phishing classifications.
* Overfitting – If overly tuned to training data, it might perform poorly on unseen URLs.
* Latency & Performance – Too slow for real-time use if complex, making deployment difficult.
* Lack of Adaptive Learning – Phishing tactics evolve, and a static model may become outdated.
* Lack of Real-Time Analysis – The model may not work effectively on live URLs without additional web-based features.
* Static Analysis Constraint – Only analyzing the URL structure may miss phishing pages that dynamically load content.

### Future Scopes :
* Integrate NLP Techniques – Use TF-IDF, word embeddings, or transformers (BERT/LSTM) to analyze URL text patterns.
* Enhance Feature Engineering – Include domain similarity (Levenshtein distance), tokenization, and n-gram analysis.
* Train Deep Learning Models – Use CNNs, RNNs, or transformers to better understand URL structures.
* Handle Real-Time URL Analysis – Implement live detection using APIs (e.g., Google Safe Browsing, VirusTotal).
* Improve Model Generalization – Regularly update the dataset to detect new phishing tactics.
* Optimize for Deployment – Convert the model into a lightweight API or browser extension for real-time use.


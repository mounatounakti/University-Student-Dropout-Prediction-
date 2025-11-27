# Student Dropout Prediction  
A data mining project that analyzes student data (demographic, parental, financial, academic, etc.) to estimate the probability of student dropout.  
The goal is to help educational institutions identify at-risk students early and improve academic retention strategies.

---

## Project Overview
The pipeline used in this project is inspired by a research paper, but we expanded the approach by adding additional steps in the EDA phase and introducing an extra machine learning model (**XGBoost**) to compare its performance with the models originally used in the paper.


## Dataset  
**Source:** UCI – *Student Dropout and Academic Success*  
Our dataset contains **4,424 students** and **36 features + `Target`** (Dropout – Graduate – Enrolled).


## Pipline

### **1. Exploratory Data Analysis**
- Computed statistical insights such as mean, mode, median, and IQR  
- Analyzed feature distributions
    
→ After EDA, we found that the dataset was clean and balanced with no missing values 🎉  
→ We only needed to **encode the `Target`** and **reduce the number of features**, keeping the most relevant ones,
  because irrelevant features can reduce accuracy and harm model performance

### **2. Data Preprocessing**
- Encoding `Target`
- Feature reduction: **from 36 features to 15 relevant features**

### **Model Training**
Trained and evaluated the following models:
- KNN  
- Decision Tree  
- Random Forest  
- SVM  
- Naive Bayes  
- XGBoost  

### **Model Evaluation Metrics**
- Accuracy  
- Precision  
- Recall  
- F1-score  
- ROC–AUC  
- Precision–Recall Curve  


## 📁 Project Structure
├── data.csv **#Main Dataset**   
├── uni_dropout.ipynb **#Main notebook**  
├── University Student Dropout Prediction 2021.pdf **#Research paper**   
├── README.md **#Project documentation**

---
## **Conclusion**

Through detailed EDA, data preprocessing, mode training and model evaluation, we aimed to identify the most effective machine learning models for predicting student dropout.

Our analysis revealed that **XGBoost** and **Random Forest** achieved the **highest overall performance**, with accuracies around **88–89%**, outperforming traditional models such as KNN, SVM, and Naive Bayes.  
Both models consistently highlighted **academic performance indicators** (approved curricular units, admission grade) and **financial regularity** as the strongest predictors of student retention.

The ROC and Precision–Recall curves confirmed that these ensemble models not only achieved high accuracy but also maintained robust balance between **precision** and **recall**, making them reliable for real-world deployment.

In conclusion, the project demonstrates that **machine learning can effectively predict student dropout** with high accuracy, enabling universities to:
- Detect at-risk students early.  
- Provide targeted support.  
- Reduce overall dropout rates efficiently.  

→ This work validates the potential of data-driven decision systems as valuable tools in educational management, offering a fast, precise, and scalable alternative to traditional manual analysis.
 

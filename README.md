# Credit_Card_Fraud_Detection
Develop a machine learning model to detect fraudulent credit card transactions, focusing on handling imbalanced datasets and minimizing false positives/negatives. The solution aims to deliver real-time predictions to mitigate financial risks effectively.

#### *Problem Statement*
With the rapid increase in the number of credit card transactions occurring globally, the threat of fraudulent activities has grown significantly. Millions of transactions are processed every second, and while most are legitimate, a small fraction involve fraudulent behavior, posing a serious risk to consumers and financial institutions. Detecting these fraudulent transactions in real-time is critical to prevent substantial financial losses. However, accurately identifying fraud is challenging due to the inherent imbalance in the data, where fraudulent transactions are rare compared to legitimate ones. The problem is to build an efficient and accurate fraud detection model that can classify transactions as fraudulent or legitimate while being aware of the large volume of transactions and minimizing false positives and false negatives

#### *Objective:*
The primary objective of this project is to develop a machine learning model capable of detecting fraudulent credit card transactions. The model should:
1. Accurately classify fraudulent and legitimate transactions.
2. Handle imbalanced datasets effectively.
3. Minimize the occurrence of false positives (classifying legitimate transactions as fraud) and false negatives (failing to detect fraud).
4. Provide real-time or near-real-time predictions to prevent potential financial losses.
   
## *About Dataset*
### **Description:**
This dataset contains credit card transactions made by European cardholders in the year 2023. It comprises over 550,000 records, and the data has been anonymized to protect the cardholders' identities. The primary objective of this dataset is to facilitate the development of fraud detection algorithms and models to identify potentially fraudulent transactions.

### **Key Features:**

**id:** Unique identifier for each transaction
V1-V28: Anonymized features representing various transaction attributes (e.g., time, location, etc.)

**Amount:** The transaction amount

**Class:** Binary label indicating whether the transaction is fraudulent (1) or not (0)


### **Potential Use Cases:**

**Credit Card Fraud Detection:** Build machine learning models to detect and prevent credit card fraud by identifying suspicious transactions based on the provided features.

**Merchant Category Analysis:** Examine how different merchant categories are associated with fraud.

**Transaction Type Analysis:** Analyze whether certain types of transactions are more prone to fraud than others.

**Data Source:** "The dataset, collected from credit card transactions made by European cardholders in 2023, has been anonymized with sensitive information removed to ensure privacy and compliance with ethical guidelines. The data will be imported via the Kaggle API to train the fraud detection model.

# **Conclusion**
In this analysis, we evaluated several machine learning models to detect fraudulent transactions, assessing them on key performance metrics such as accuracy, precision, recall, F1-score, and the AUC-ROC curve. Below is a summary of the models tested and their respective results:

1. **Logistic Regression**:  
   - **Accuracy**: 95.72%  
   - **Precision**: 0.98  
   - **Recall**: 0.94  
   - **F1-Score**: 0.96  
   - **AUC Score**: 1.00  
   - While the Logistic Regression model performed well, achieving high accuracy and near-perfect precision, its lower recall compared to more complex models suggests it may not be the top choice for this task.

2. **Decision Tree**:  
   - **Accuracy**: 99.75%  
   - **Precision**: 1.00  
   - **Recall**: 1.00  
   - **F1-Score**: 1.00  
   - **AUC Score**: 1.00  
   - The Decision Tree model displayed high accuracy with perfect precision and recall, but it is prone to overfitting. The near-perfect ROC and AUC scores could indicate strong performance, but the model’s simplicity can lead to overfitting on the training data.

3. **Random Forest**:  
   - **Accuracy**: 99.98%  
   - **Precision**: 1.00  
   - **Recall**: 1.00  
   - **F1-Score**: 1.00  
   - **AUC Score**: 1.00  
   - **ROC Curve Issue**: The ROC curve is stacked upon the TPR line, which is usually a sign of overfitting. While the model performs exceptionally well with perfect classification scores, this overfitting might make it less reliable on new, unseen data. Thus, it’s crucial to interpret its perfect scores with caution.

4. **XGBoost**:  
   - **Accuracy**: 99.96%  
   - **Precision**: 1.00  
   - **Recall**: 1.00  
   - **F1-Score**: 1.00  
   - **AUC Score**: 1.00  
   - Similar to Random Forest, XGBoost delivered near-perfect performance, but the ROC curve also stacked on the TPR line indicates potential overfitting. This could make XGBoost less reliable for future data.

5. **Gradient Boosting**:  
   - **Accuracy**: 97.60%  
   - **Precision**: 0.99  
   - **Recall**: 0.97  
   - **F1-Score**: 0.98  
   - **AUC Score**: 0.98  
   - Gradient Boosting performed well, but its accuracy was slightly lower compared to Random Forest and XGBoost. However, it shows better generalization as the ROC curve and AUC score indicate more realistic and reliable performance.

6. **Naive Bayes**:  
   - **Accuracy**: 91.85%  
   - **Precision**: 0.99  
   - **Recall**: 0.85  
   - **F1-Score**: 0.91  
   - **AUC Score**: 0.98  
   - Naive Bayes performed reasonably well, but it struggled with recall for the fraudulent class. While its simplicity is advantageous for quick predictions, it is outperformed by more advanced models.

---

### Best Model for Fraud Detection

After reviewing all models, **Gradient Boosting** stands out as the most reliable option. Although models like **Random Forest** and **XGBoost** achieved near-perfect metrics (accuracy, precision, and AUC scores), their ROC curves stacked on the TPR line raise concerns of overfitting, suggesting that these models may not generalize well to new data.

On the other hand, **Gradient Boosting** with an **AUC score of 0.98** and a more balanced ROC curve shows strong generalization ability. It provides reliable performance without the overfitting issues seen in the other models, making it a better option for real-world fraud detection. Therefore, **Gradient Boosting** is recommended for deployment, offering a solid balance between accuracy and robustness for detecting fraudulent transactions.

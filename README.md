# Company Bankruptcy

## Description

This project applies various machine learning models to predict company bankruptcy based on financial indicators.

Key steps include:

* **Exploratory Data Analysis (EDA)** to understand feature distributions and class imbalance
* **Dimensionality reduction** to reduce overfitting and improve efficiency
* **Data balancing techniques** (e.g., SMOTE) to address severe class imbalance
* **Model training and evaluation** using Logistic Regression, KNN, Decision Tree, Neural Networks, Random Forest, and Gradient Boosting
* **Performance comparison** before and after balancing, with a focus on minimizing **Type II errors** (failing to detect actual bankruptcies)

The goal was to identify the most reliable model for imbalanced classification tasks in financial risk prediction.

## Concluding Thoughts

So, after evaluating the models with and without SMOTE, it's pretty evident that data balancing significantly improves performance across all models. The assessment metrics—including precision, recall, F1-score, and AUC-ROC—show that applying SMOTE results in more consistent and reliable classification, especially between the two classes.

Even in cases where the overall performance metrics may appear low after SMOTE, the key difference is balance and consistency :) Without SMOTE, models tend to either overfit to the majority class (non-bankrupt) or demonstrate high variance between precision and recall for the minority class (bankrupt). In contrast, post-SMOTE models exhibit a pretty noticeable reduction in the inconsistency between the classes, meaning both bankrupt and non-bankrupt cases are being handled more equitably.

Moreover, graphing the metrics clearly illustrates a sharp increase across all evaluation scores—indicating that SMOTE not only improved consistency but also pushed the overall performance higher. This improvement is further supported by the confusion matrices, which show significantly higher true positives (TP) and true negatives (TN) in the post-SMOTE models compared to the pre-SMOTE versions. Now, this is crucial in the bankruptcy prediction context, where correctly identifying at-risk companies (TP) is just as important as not misclassifying stable ones (TN).

Lastly, as mentioned in the notebook, when analyzing the AUC-ROC scores, two models stand out: the Neural Network model, which achieves the highest score (~0.968) and demonstrates robust handling of both classes, followed by the K-Nearest Neighbors (KNN) (~0.96) model, which also shows strong performance. These models not only achieved higher predictive accuracy but also maintained balance across precision and recall, making them superior to the other models.

In summary, applying SMOTE led to substantial improvements in model performance across all key metrics and provided more balanced and interpretable results — particularly important when the goal is to mitigate the risk of failing to predict actual bankruptcies (Type II errors).

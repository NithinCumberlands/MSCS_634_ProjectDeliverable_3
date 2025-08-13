# MSCS_634_ProjectDeliverable_3
# Customer Data Analysis: Classification, Clustering, and Pattern Mining

## Overview
In this project, I applied machine learning techniques to analyze customer data with the goal of predicting purchasing behavior, segmenting customers, and uncovering hidden patterns. The project involves the following steps:

1. **Developing classification models**: I built two classification models (Decision Tree and k-NN) to predict whether a customer will make a purchase based on their age, income, and spending behavior.
2. **Hyperparameter tuning**: I used **GridSearchCV** to optimize the hyperparameters of the Decision Tree classifier for better model performance.
3. **Evaluating model performance**: The models were evaluated using confusion matrices, ROC curves, and accuracy/F1 scores.
4. **Developing a clustering model**: I implemented **K-Means clustering** to segment customers into different groups based on their features.
5. **Association rule mining**: I applied the **Apriori algorithm** to identify potential patterns in customer behavior, although no significant patterns were discovered.

## Key Insights
- **Classification Models**:
  - The **Decision Tree classifier** performed perfectly with an accuracy and F1 score of 1.0, meaning it could perfectly predict customer purchases. The model achieved this by recursively splitting data based on feature values.
  - The **k-NN classifier** performed well with an accuracy of 0.75 and an F1 score of 0.4. While its ability to predict purchases was decent, it struggled with identifying customers who made purchases.
  - Hyperparameter tuning through **GridSearchCV** improved the performance of the Decision Tree by optimizing key parameters such as max depth and min samples per split.

- **Clustering**:
  - **K-Means clustering** effectively segmented customers into three distinct groups based on their age and income. These groups were:
    - **Low-income, young customers**
    - **Mid-income, middle-aged customers**
    - **High-income, older customers**
  - The clustering results can be applied to develop targeted marketing strategies, where each segment receives tailored messaging and promotions.

- **Association Rule Mining**:
  - The **Apriori algorithm** was used to find associations between different customer attributes. However, despite preprocessing the data by binning and one-hot encoding continuous variables, the results did not yield meaningful association rules. This suggests that the dataset may lack strong categorical relationships, or the minimum support parameter may have been too restrictive.

## Practical Relevance
- **Customer Classification**: The Decision Tree model can be used in businesses to predict whether a customer is likely to make a purchase based on their profile. For example, retailers can identify high-value customers and target them with personalized offers or promotions.
- **Segmentation with Clustering**: K-Means clustering provides valuable insights for customer segmentation, which can be leveraged to design personalized marketing campaigns for different customer groups. For example, low-income, young customers can be offered budget-friendly products, while high-income, older customers can be targeted with premium offerings.
- **Association Rule Mining**: Although no significant patterns were discovered in this dataset, association rule mining is a widely used technique in retail. It can help uncover relationships between products that customers frequently purchase together. This information can be used for cross-selling or bundling strategies.

## Challenges Encountered and How They Were Addressed
- **Overfitting in Decision Tree**: The Decision Tree model initially showed perfect performance, which raised concerns about overfitting. To address this, I performed hyperparameter tuning to limit the tree depth and prevent overfitting, which allowed the model to generalize better.
- **Association Rule Mining Limitations**: The association rule mining step did not yield meaningful patterns. This could have been due to the nature of the dataset, which was relatively small and lacked strong categorical relationships. To improve this in future projects, I would try applying the algorithm to a larger dataset with more categorical features.
- **Choosing the Right Number of Clusters**: For K-Means clustering, choosing the right number of clusters (**k**) can significantly affect the results. I chose **k = 3** based on visual inspection, but further experimentation with different values could have yielded better customer segments. A more systematic approach like the **Elbow Method** could help refine this choice.

## Conclusion
This project demonstrated the power of machine learning models in analyzing customer data. The **Decision Tree classifier** and **k-NN** provided insights into customer purchasing behavior, while **K-Means clustering** segmented customers for more targeted marketing. Despite some challenges with **association rule mining**, the project highlighted how machine learning techniques can extract actionable insights that can drive business decisions.

### Future Improvements:
- Exploring larger datasets for better results in association rule mining.
- Implementing advanced clustering techniques (e.g., DBSCAN) to handle more complex customer data.
- Using ensemble methods (e.g., Random Forest or Gradient Boosting) to improve the performance of classification models.



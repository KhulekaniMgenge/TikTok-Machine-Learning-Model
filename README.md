READ ME FILE

# Tik Tok Video Classification algorithm (2023)
Constructing a machine learning algorithm to classify videos as either claim or opinion. Since claim video content are more likely to violates the platform’s terms of service. The model will reduce backlog of user reports and prioritize them more efficiently for review.

# Solution	
Built two tree-based classification models. Both models were used to predict on a held-out validation dataset, and final model selection was determined by the model with the best recall score. The final model was then used to score a test dataset to estimate future performance.

# Summary Insight
 ![image](https://github.com/user-attachments/assets/d905e630-f349-451d-bfd3-92e3387902b3)

Both model architectures—random forest (RF) and XGBoost—performed exceptionally well. The RF model had a better recall score (0.995) and was selected as champion.
Performance on the test holdout data yielded near perfect scores, with only five misclassified samples out of 3,817.
Subsequent analysis indicated that, as expected, the primary predictors were all related to video engagement levels, with video view count, like count, share count, and download count accounting for nearly all predictive signal in the data. With these results, we can conclude that videos with higher user engagement levels were much more likely to be claims. In fact, no opinion video had more than 10,000 views.

# Recommendations
The model performed exceptionally well on the test holdout data. Before deploying the model, a further evaluation using additional subsets of user data might be needed. Furthermore, a recommendation of monitoring the distributions of video engagement levels to ensure that the model remains robust to fluctuations in its most predictive features.


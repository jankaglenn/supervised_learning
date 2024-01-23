# supervised_learning

Background
In this Challenge, I used various techniques to train and evaluate a model based on loan risk. I used a dataset of historical lending activity from a peer-to-peer lending services company to build a model that can identify the creditworthiness of borrowers.

This project involves constructing two logistic regression models for supervised machine learning, utilizing data from a hypothetical peer-to-peer lending services company ("crowdlending"). The comparison of both models reveals a recommendation in favor of the latter model, designed to address sample size data skewing. The primary goal is to minimize the risk associated with loans to both lenders and borrowers.

The training and testing datasets encompass various standard financial loan attributes (loan size, debt-to-income ratio, interest rate, etc.), with labels indicating whether the loans were repaid. The models are evaluated based on their ability to predict creditworthiness versus default.

Notably, the majority of data points (approximately 97%) are classified as creditworthy (75,036) compared to defaulters (2,500). To mitigate the impact of this disproportionate sample, the second model employs the RandomOverSampler module from the imbalanced-learn library. This ensures equal representation of creditworthy and default-prone cases in the training data, leading to statistically superior results.

Results:
Machine Learning Model 1 (Logistic Regression predictions):

Accuracy: 99.2%
Balanced Accuracy: 94.4%
Precision and Recall (Creditworthy): 100%, 100%
Precision and Recall (Defaulters): 87%, 89%
Machine Learning Model 2 (Resampled Logistic Regression):

Accuracy: 99.5%
Balanced Accuracy: 99.6%
Precision and Recall (Creditworthy): 100%, 100%
Precision and Recall (Defaulters): 87%, 100%
Comparative Stats (Resampled Model's Numbers Listed First):

Lower False Negatives (2 vs. 67)
Slightly Higher Rate of False Positives (91 vs. 80)
Higher True Negatives (623 vs. 558)
Lower True Positives (18679 vs. 18668)
Summary:
The second model may approve a few more loans for the default-prone, but this is offset by a significantly higher identification of true defaulters. Although there are 11 more approved loans for defaulters, 65 more defaulters are accurately identified. In general, the second model is expected to result in numerically more loan repayments. Assuming proportional loan values, this model offers lenders a greater return on investment, with a marginal increase in losses but substantial income gains.

While the second model may approve loans for a few individuals who should be denied (false positives), it excels in identifying many more individuals who should be denied loans (true negatives). This approach reduces risk for lenders and is likely to enhance overall profitability.







# Cryotherapy-Prediction-in-R


##This project aimed to analyze and model the effectiveness of wart treatments (cryotherapy and immunotherapy) using patient data and various predictive modeling techniques. This dataset contains information about wart treatment results of 90 patients using cryotherapy.
Data Source: Cryotherapy Dataset
https://archive.ics.uci.edu/dataset/429/cryotherapy+dataset



Exploration and Visualizations of the data:
The relationships between several key variables such as age, sex, number of warts, and treatment results were visualized. 


Findings:

1.	Exploratory Data Analysis:
o	A histogram of age showed the age distribution of patients, with most patients being under 40.
o	Boxplots for age by treatment results indicated that younger patients tended to respond better to treatments.
o	Scatter plots revealed that treatment success was generally better for patients younger than 30, regardless of the number of warts or the area affected.
o	No strong correlation was found between the number of warts and the success of the treatment, indicating that other factors like age and treatment time had more predictive power.


2.	Modeling Techniques:
Given the binary nature of the target variable (0 = negative response, 1 = positive response), Logistic Regression and Random Forest were chosen as suitable models. These models are well-suited for classification tasks involving binary outcomes.

o	A Logistic Regression model was built using variables like age, sex, number of warts, wart area, wart type, and treatment time.
	The accuracy of the logistic regression model was 89.29%.
	Significant predictors included age (p = 0.019) and treatment time (p = 0.002), while other variables like sex and number of warts were not significant.


o	A Random Forest model was also applied, achieving the same accuracy of 89.29%, with no false negatives but a few false positives.
	This model captured non-linear relationships but did not perform significantly better than logistic regression.

3.	Model Evaluation:
o	Both models had high accuracy, with logistic regression having a balanced accuracy of 88.75%, and the random forest model demonstrating robustness in detecting successful treatments with no false negatives.
o	However, the Logistic Regression model provided more interpretability with clearer insights into which variables were significant predictors.

Recommendations:

•	Model Choice: If interpretability and simplicity are most important, Logistic Regression is preferable. If avoiding false negatives (missing potential treatment successes) is crucial, Random Forest may be more reliable. So, while both models are equally accurate, the Random Forest model could be considered more reliable in a clinical setting where treatment success is vital to predict accurately.

•	Improvements: Random Forest can be further optimized by adjusting hyperparameters like the number of trees or maximum depth to improve specificity. Additionally, cross-validation could be implemented to ensure that the model's performance generalizes well to unseen data.

•	Recommendations: Future analysis could investigate more granular relationships between treatment type and other patient characteristics to refine predictive accuracy. 



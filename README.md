# Credit_Risk_Analysis

In this project I use various sampling techniques from scikit-learn libraries to train a logistic regression model to predict high risk loan applicants

## Sampling Methods

	### *Oversampling*
		I used random oversampling and SMOTE to increase the smaller target set. It wasn't very effective in the logistic regression model as the predictive recall was around .6 in either case, and the predictive precision was at .01 in both.

	### *Undersampling*
		I used cluster centroids undersampling to reduce the larger target set and used that dataset to run a logistic regression model. The outcomes for this set were no better with recall at .69 and predictive accuracy at around .50 (essentially guessing).

	### *Combination*
		To perform combination sampling I used SMOTEENN algorithm to even out both target sets. This produced a model with .64 accuracy and recall at .71. This is a lot better than both the previous models.

	### *Ensemble*
		In this section I used both the balanced random forest and easy ansemble adaboost classifiers from the imbalanced learn library. Both performed much better than the logistic regression algorithm with over and undersampling. the random forest produced a model with an accuracy of .78 and recall of .70. The ensemble adaboost model got an accuracy of .93 and recall of .92.

## Results
Ensemble learning is the clear winner here, specifically the adaboost. Because we are looking for high risk loans, we are most interested in recall. Adaboost was able to produce a recall rate of 92%.


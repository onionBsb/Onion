# Project Name
Classification of 5g users

# Description
Aim：Based on user basic information and communication related data, such as user call fee information, traffic volume, active behavior, package type, regional information and other characteristic fields, the model is trained through training data to predict whether each sample in the test set belongs to 5G users.

Data：The data contains 60 fields, among which the target field is the predicted target, and the main feature fields are divided into two categories: cat and num, which are discrete feature and numerical feature respectively


Evaluation：The evaluation standard adopts AUC, that is, the higher the score, the better the effect

# Installation
Installation dependency：NumPy、Pandas、Matplotlib、Scikit-learn

Configuration environment: operate in jupyter notebook

# Usage
You just need to execute the code in my file one by one in jupyter notebook，I set the parameters myself, you can also try to change the parameters to see if there is any difference.

# eg
`#Decision tree model`<br>
`estimator_tree = DecisionTreeClassifier()`<br>
`estimator_tree.fit(X_train,y_train)`<br>
`#Calculate the value of the AUC`<br>
`y_pred = estimator_tree.predict(X_test)`<br>
`auc_tree = roc_auc_score(y_test,y_pred)`<br>
`#The running result is that the value of AUC is equal to 0.56, and no processing analysis is done from the initial model, and then the methods to improve AUC are studied from different aspects`<br>
`#The following is an example of tuning the parameters of the decision tree model`<br>
`#Searching the grid to find the best max_depth and min_samples_split results are 10 and 14, respectively`<br>
`#retrain`<br>
`estimator_tree = DecisionTreeClassifier(max_depth=10, min_samples_split= 14`<br>
`estimator_tree.fit(X_train,y_train)`<br>
`#Got an AUC of 0.88, a significant improvement, there are other aspects can also refer to my code`<br>

# Reference material
CSDN，《Principles and applications of machine learning》

# file




In this particular project, we are using a dataset that contains information like State, 
account length, international plan, Total day cells, Total day charge and using that to predict whether 
the customer will remain a customer in the future.

1) Data Exploration

Feature variables:-
• State: Self Explanatory (string)
• Account length: Self Explanatory (integer)
• Area code: Self Explanatory (integer)
• International plan: Self Explanatory (string)
• Voice mail plan: Self Explanatory (string)
• Number vmail messages: Self Explanatory (integer)
• Total day minutes: Self Explanatory (double)
• Total day calls: Self Explanatory (integer)
• Total day charge: Self Explanatory (double)
• Total eve minutes: Self Explanatory (double)
• Total eve calls: Self Explanatory (integer)
• Total eve charge: Self Explanatory (double)
• Total night minutes: Self Explanatory (double)
• Total night calls: Self Explanatory (integer)
• Total night charge: Self Explanatory (double)
• Total intl minutes: Self Explanatory (double)
• Total intl calls: Self Explanatory (integer)
• Total intl charge: Self Explanatory (double)
• Customer service calls: Self Explanatory (integer)

Target variable:-
• Churn: Self Explanatory (string)



2) Data Cleaning
State (dropped) :Tells about the location of the customer 
No null values found

3) Feature Engineering: Feature Encoding, Feature Selection, Feature Scaling

Feature Encoding

Label Encoding :-
Churn: Decision whethere customer will continue the service or not.
International Plan: Tells whether the customer has an international plan or not
Voice mail plan: Tells whether the customer has a voice plan or not

Feature Scaling
Standard Scalar: Applied because there was no requirement of using quartiles.
(Applied to all features)

Feature Selection
SelectK best (Chi2) and Correlation was used to select best features.
Intersected Features are: 
['Total day minutes', 'Total day minutes', 'Total day charge', 'Total day charge', 'International plan', 'International plan', 
'Total eve minutes', 'Total eve minutes', 'Customer service calls', 'Customer service calls', 'Total eve charge', 'Total eve charge',
'Total intl minutes', 'Total intl minutes', 'Total intl charge', 'Total intl charge']

4) Visualization 
Scatterplot, boxplot, piechart, histograms were used to know about graphical representations.

5) Hyperparameter Tuning

Logistic Regression 
Score of Logistic Regression is 0.846441947565543 where solver is 'lbfgs' and max_iterations is  6
Score of Logistic Regression is 0.8445692883895131 where solver is 'newton-cg' and max_iterations is  6
Score of Logistic Regression is 0.8445692883895131 where solver is 'saga' and max_iterations is  11

Support Vector Machine 
{'kernel': 'rbf', 'C': 79}

6) Cross Validation
KFold validation was used to find more about accuracies.

7) Model fitting and Evaluation 
Logistic Regression
Precision score is: 0.3870967741935484
Recall score is: 0.16
Accuracy score is: 0.846441947565543
F1 score is: 0.22641509433962265


SVC
Precision score is: 0.5846153846153846
Recall score is: 0.5066666666666667
Accuracy score is: 0.8801498127340824
F1 score is: 0.5428571428571428


Clustering
Silhouette Score is: 0.1802133362156861

PCA with SVC
Precision score is: 1.0
Recall score is: 0.02666666666666667
Accuracy score is: 0.8632958801498127
F1 score is: 0.05194805194805195


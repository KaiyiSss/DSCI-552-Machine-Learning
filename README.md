
### Breast Cancer classification using various classification models, including Supervisied, Semi-Superivised, Unsupervisied Learning and etc. 
#### Downloaded datasets about patients who have been diagnosed. The dataset shows a few features to indicate breast cancer. 
(Benigh = B, Malignant = M). Replace benign value with 0 and malignant value with 1 to represent categorical bool variables.
For splitting the train and test data, I set up 20% of the positive and negative classes as the test set.
Monte-Carlo Simulation: there are three parts to construct the Monte-Carlo Simulation. The three parts are Supervised Learning, Semi-Supervised Learning, and Unsupervised Learning.
Supervised Learning:
CV(Cross Validation)
Normalization
Grid Search(GridSearchCV implements a “fit” and a “score” method. It also implements “score_samples”, “predict”, “predict_proba”, “decision_function”, “transform” and “inverse_transform” if they are implemented in the estimator used)
Record and update prediction probabilities for each run of the model/algorithm in order to pick the best model configuration.
Result:
![image](https://github.com/KaiyiSss/DSCI-552-Machine-Learning/assets/60586553/e6b0a8b9-8625-4645-9586-13fceabd390f)
![image](https://github.com/KaiyiSss/DSCI-552-Machine-Learning/assets/60586553/d3fdfadf-98f2-4452-9a70-4a2e05cde523)



#### Semi-Supervised Learning:
From lists I have constructed for categories 1 and 0, I randomly pick 50% of them to be unlabeled datasets.
Get labeled and unlabeled data indices to identify the two kinds of data and create two datasets(labeled and unlabeled datasets).
Build a Linear Support Vector Classification model and fit the data.
Grid Search(GridSearchCV implements a “fit” and a “score” method. It also implements “score_samples”, “predict”, “predict_proba”, “decision_function”, “transform” and “inverse_transform” if they are implemented in the estimator used)
Loop the grid search process until all unlabeled data is labeled(letting it self-learning).
Record and update prediction probabilities for each run of the model/algorithm to pick the best model configuration.
Result:
![image](https://github.com/KaiyiSss/DSCI-552-Machine-Learning/assets/60586553/9fa166dc-01f8-44ec-8f65-6d3511a14cce)
![image](https://github.com/KaiyiSss/DSCI-552-Machine-Learning/assets/60586553/620a1c4f-cc51-4d4a-a5ab-6de2f96cae7e)
![image](https://github.com/KaiyiSss/DSCI-552-Machine-Learning/assets/60586553/2e9ca456-4995-4ddb-b4ac-61a2ef4efc4a)





##### Unsupervised Learning
Clustering: find of each point from both centers and probability of each point being in cluster 1 or 0 and label clusters based on the majority labels in the same cluster.
Create k-means model and get information for each run to estimate the optimal model configuration
Results:
![image](https://github.com/KaiyiSss/DSCI-552-Machine-Learning/assets/60586553/7b29eb89-92e9-4d18-b29c-b994875f7da7)
![image](https://github.com/KaiyiSss/DSCI-552-Machine-Learning/assets/60586553/35d86f30-270e-4e51-9ddc-642e402f9ed5)
![image](https://github.com/KaiyiSss/DSCI-552-Machine-Learning/assets/60586553/0a0f5fae-8364-49f0-a4ed-1433bf171f4d)








Spectral Clustering: utilizing the spectrum of the data's similarity matrix for dimensionality reduction, allowing for clustering in a reduced dimensional space
Use the Radial basis function kernel (RBS Kernal) with gamma=1 or find a gamma for which the two clusters have the same balance as the one in original data set. 
Use “Fit and Predict” method to label data in the clustering.
Results:
![image](https://github.com/KaiyiSss/DSCI-552-Machine-Learning/assets/60586553/5046d474-d4c4-4b35-854e-6c0e66596245)
![image](https://github.com/KaiyiSss/DSCI-552-Machine-Learning/assets/60586553/06f50f08-e3c4-4986-82bf-4450144a9268)
![image](https://github.com/KaiyiSss/DSCI-552-Machine-Learning/assets/60586553/57005167-b4d8-45aa-ac6b-df9a82f87852)



  


Compare the performance of each model:


![image](https://github.com/KaiyiSss/DSCI-552-Machine-Learning/assets/60586553/a0b5ccb2-00ae-4711-bdc4-18add8ffc2c0)


Based on the average accuracy results we can see that Supervisied Learning results in the highest accuracy (98%) followed by Semi-Supervisied, and finally Unsuperivised.
Active Learning Using Support Vector Machines
Download the banknote authentication Data Set
Repeat each of the following two procedures 50 times
 Passive
Active
 Average the 50 test errors and get results:
 ![image](https://github.com/KaiyiSss/DSCI-552-Machine-Learning/assets/60586553/239488ba-06fb-4d4d-8c85-ffc903d16705)



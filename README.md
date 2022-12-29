Decision Tree Classifier in SciKitLearn for Multi-Class Classification - Base problem category as per Ready Tensor specifications.

- decision tree
- multi-class classification
- sklearn
- python
- pandas
- numpy
- scikit-optimize
- flask
- nginx
- uvicorn
- docker

This is a Multi-Class Classifier that uses a Decision Tree Classifier implemented through SciKitLearn.

The classifier starts by creating decision trees that look at whether the variables meet certain thresholds to create leaf nodes that allow the classifier to assign the sample into a specific class.

The data preprocessing step includes missing data imputation, standardization, one-hot encoding for categorical variables, datatype casting, etc. The missing categorical values are imputed using the most frequent value if they are rare. Otherwise if the missing value is frequent, they are give a "missing" label instead. Missing numerical values are imputed using the mean and a binary column is added to show a 'missing' indicator for the missing values. Numerical values are also scaled using a Yeo-Johnson transformation in order to get the data close to a Gaussian distribution.

Hyperparameter Tuning (HPT) is conducted by finding the optimal number of samples required to split an internal node as well as the optimal number of samples required to be at a leaf node.

During the model development process, the algorithm was trained and evaluated on a variety of publicly available datasets such as email primary-tumor, splice, stalog, steel plate fault, wine, and car.

This Multi-Class Classifier is written using Python as its programming language. SciKitLearn is used to implement the main algorithm, evaluate the model, and preprocess the data. Numpy, pandas, and feature_engine are used for the data preprocessing steps. SciKit-Optimize was used to handle the HPT. Flask + Nginx + gunicorn are used to provide web service which includes two endpoints- /ping for health check and /infer for predictions in real time.

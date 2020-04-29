# Semiconductor Backend Production Rate Dataset with Partial Combination Models
A dataset from semiconductor assembly and testing processes is used to evaluate the model selection prediction method. The response variable refers to the throughput rate of a specific machine–product combination in one of the assembly and testing process steps based on historical data. This data set includes 1 response variable, 5 categorical machine and product attributes and 11 numerical attributes. The dataset contains 13186 observations collected between Oct. 2018 and Mar. 2019 from a world-leading semiconductor assembly and testing company in Taiwan.

mixed_categorical_numerical_data.csv: the raw data.

mixed_categorical_numerical_dataDummy.csv: the transformed one-hot encoded data.

Full_Model.rds: the full model built from the whole dataset.

Fundamental_Model.rds: the fundamental model built from one specific fundamental dataset.

Partial_Model_1-11.rds: the partial combination models related to the fundamental model mentioned above.

training datasets : Full_training_dataset,Partial_1-11_training_dataset and Fundamental_training_dataset for Figure(2).

validation datasets : Full_validation_dataset,Partial_1-11_validation_dataset and Fundamental_validation_dataset for Figure(2).

Prediction steps :
We construct xgb.DMatrix object and use our model to make predictions and calculate the rmse index.
The input dataset(x) and label(y) need to be stored separately and the function code is as follows: 
xgb.DMatrix(label = y, data = as.matrix(x))


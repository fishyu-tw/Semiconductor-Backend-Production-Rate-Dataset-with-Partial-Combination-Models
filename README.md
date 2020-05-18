# Semiconductor Backend Production Rate Dataset with Partial Combination Models
A dataset from semiconductor assembly and testing processes is used to evaluate the model selection prediction method. The response variable refers to the throughput rate of a specific machine–product combination in one of the assembly and testing process steps based on historical data. This data set includes 1 response variable, 5 categorical machine and product attributes and 11 numerical attributes. The dataset contains 13186 observations collected between Oct. 2018 and Mar. 2019 from a world-leading semiconductor assembly and testing company in Taiwan.

mixed_categorical_numerical_data.csv: the raw data.

mixed_categorical_numerical_data(one-hot encoded).csv: the transformed one-hot encoded data.

+ one-specific-fundamental-dataset
  + models-trained
    - Full_Model.rds: the full model built from the whole dataset.
	- Fundamental_Model.rds: the fundamental model built from one specific fundamental dataset.
	- Partial_Model_1-11.rds: the partial combination models related to the fundamental model mentioned above.
  + fundamental-training-datasets
    - Full_training_dataset.csv: to evaludate RMSE_Tr of Full_Model.rds. 
	- Fundamental_training_dataset.csv: to evaludate RMSE_Tr of Fundamental_Model.rds.
	- Partial_1-11_training_dataset.csv: to evaludate RMSE_Tr of Partial_Model_1-11.rds.  
  + fundamental-evaluation-datasets
    - Full_evaluation_dataset.csv: to evaludate RMSE_V of Full_Model.rds.
	- Fundamental_evaluation_dataset.csv: to evaludate RMSE_V of Fundamental_Model.rds.
	- Partial_1-11_evaluation_dataset.csv: to evaludate RMSE_V of Partial_Model_1-11.rds. 

Note: the Prediction steps:
We construct xgb.DMatrix object and use our model to make predictions and calculate the rmse index.
The input dataset(x) and label(y) need to be stored separately and the function code is as follows: 
xgb.DMatrix(label = y, data = as.matrix(x))


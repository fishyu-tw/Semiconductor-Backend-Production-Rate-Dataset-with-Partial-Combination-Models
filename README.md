# PartialCombinationModels
A dataset from semiconductor assembly and testing processes is used to evaluate the model selection prediction method. The response variable refers to the throughput rate of a specific machine–product combination in one of the assembly and testing process steps based on historical data. This data set includes 1 resonse variable, 5 categorical machine and product attributes and 11 numerical attributes. The dataset contains 13186 observations.

mixed_categorical_numerical_data.csv: the raw data.

mixed_categorical_numerical_dataDummy.csv: the transformed one-hot encoded data.

Full_Model.rds: the full model built from the whole dataset.

Fundamental_Model.rds: the fundamental model built from one fundamental dataset.

Partial_Model_1-11.rds: the models related to the fundamental model mentioned above.

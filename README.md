# Semiconductor Backend Production Rate Dataset with Partial Combination Models
A dataset from semiconductor assembly and testing processes is used to evaluate the model selection prediction method. The response variable refers to the throughput rate of a specific machine–product combination in one of the assembly and testing process steps based on historical data. This data set includes 1 response variable, 5 categorical machine and product attributes and 11 numerical attributes. The dataset contains 13186 observations collected between Oct. 2018 and Mar. 2019 from a world-leading semiconductor assembly and testing company in Taiwan.

mixed_categorical_numerical_data.csv: the raw data.

mixed_categorical_numerical_dataDummy.csv: the transformed one-hot encoded data.

Full_Model.rds: the full model built from the whole dataset.

Fundamental_Model.rds: the fundamental model built from one specific fundamental dataset.

Partial_Model_1-11.rds: the partial combination models related to the fundamental model mentioned above.

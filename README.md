# Optimizing-ML-pipeline-AzureML-UdacityND
# Objective <br>
This Project aims at making a binary prediction on a Dataset as part of Udacity Azure ML Engineer Nano Degree.We are given with two files namely
- Train.py<br>
- Project.ipynb<br>
We need to build a Machine learning model using skikit learn and tune the hyper parameters to find the best model using azure ML python SDK and Hyper Drive<br>
Also we need to  use the Azure auto ML Feature  to find the best model and best Hyperparameters.<br>
# Train Test Split<br>
I have choosen to use 70% and 30 % datasets for Train and test splits.<br>
# Hyperparameters used
Learning rate with different values . As per literature survey learning rate should not be too long or too small for better model performances. Hence I choose a list of learning rates
using Azure ML python SDK Hyper Drive Parameters. Also in Logistic  regression  C is called inverse regularisation parameter so lesser  C values penalises the model more for better results.<br>
Maximum iterations is another hyper parameter choosen , maximum iterations is the number of times your model should be trained with the  given hyper parameters.<br>
# Sampling Method Used<br>
I have choosen the Random Sampling method  becuase of its advantage of performing equally as Grid Search with lesser compute power requirements.<br>
# Early Stopping Technique used <br>
I have choosen to use Bandit policy stopping because of its advanatges using the Slack Factor and Slack amount to decide  on  creating the next runs. <br>
# AutoML Configuration<br>
Since this is a two class Binary classification I have choosen the task as Classification in Auto M config along with following configurations  number of iterations =20 , maximum number of Concurrent iterations =4, K fold Cross Validations =5. After Running the model with therse configurations Best model choosen was Voting Ensemble with an accuracy of 91%.
# Comparisons between AutoML and Hyper Drive<br>
Though both Hyper Drive and Auto Ml performed almost same with an accuracy of 91% approximately , I feel Hyper drive is bes t to choose in terms of feature engineering as we have limited scope of feature engineering in terms of Auto Ml .<br>
# Future Scope<br>
This Dataset is hugely Imbalanced , performing more future Engineering technqiues may slightly improve the accuracy.<br>
# Resources that Helped me during this Project
[Hyper Parameter Tuning Using Azure ML](https://docs.microsoft.com/en-us/azure/machine-learning/how-to-tune-hyperparameters)<br>
[DataSets and Data Stores Azure ML](https://docs.microsoft.com/en-us/azure/machine-learning/how-to-create-register-datasets)<br>
[Tabular Datasets using Azure Python SDK](https://docs.microsoft.com/en-us/python/api/azureml-core/azureml.data.dataset_factory.tabulardatasetfactory?view=azure-ml-py)<br>
[GithUb Repo From Azure ML Python SDK examples](https://github.com/Azure/MachineLearningNotebooks/blob/master/tutorials/create-first-ml-experiment/tutorial-1st-experiment-sdk-train.ipynb)

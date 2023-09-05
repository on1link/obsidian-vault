#googleCloudPlatform 
# Understanding the ML Enterprise Workflow
## Quiz
* Which process covers algorithm selection, model training, hyperparameter tuning, and model evaluation in the Experimentation and Prototyping activity?
	* Model prototyping
* Which two activities are involved in ML development?
	* Experimentation and training operationalization.
* If the model needs to be repeatedly retrained in the future, an automated training pipeline is also developed. Which task do we use for this?
	* Training operationalization
* What is the process that data scientists use to develop the models on an experimentation platform?
	* Problem definition > Data selection > Data exploration > Feature engineering > Model prototyping > Model validation
# Data in the Enterprise
## Quiz
* Which Data processing option can be used for transforming large unstructured data in Google Cloud?
	* Dataflorw
* Which of the following statements is not a feature of Analytics Hub?
	* *Analytics Hub requires batch data pipelines that extract data from databases, storer it in flat file, and transmit them tot he consumer where they are ingested into another database*
	* Analytics Hub efficiently and securely exchanges data analytics assets across organizations to address challenges of data reliability and cost
	* There are three roles in Analytics Hub - A Data Publisher, Exchange Administrator, and a Data Subscriber.
	* You can create and access a curated library of internal and external assets, including unique datasets like Google Trends, backed by the power of BigQuery.
* What does the Aggregation Values contain in any feature
	* The min, median, and max values for each features.
* Which of the following is correct for Online serving?
	* Online serving is for low-latency data retrieval of small batches of data for real-time processing.
* Which of the following is not a part of Google's enterprise data management and governance tool?
	* Analytics Catalog
# Science of Machine Learning and Custom Training
## Quiz
* Which of the following can make a huge difference in model quality?
	* Setting hyperparameters to their optimal values for a given dataset
* Which of the following is a black-box optimization service?
	* Vertex Vizier
* Which of the following algorithms is useful, if you want to specify a quantity of trials that is greater than the number of points in the feasible space?
	* Grid Search
* Black box optimization algorithms find the best operating parameters for any system whose ______?
	* performance can be measure as a function of adjustable parameters.
* Bayesian optimization takes into account past evaluations when choosing the hyperparameter set to evaluate next. By choosing its parameters combinations in an informed way, it enables itself to focus on those areas of the parameter space that it believes will bring the most promising validation scores. Therefore it _______
	* limits the number of times a model needs to be trained for validation.
	* requires less iterations to get to the optimal set of hyperparameter values.
	* enables itself to focus on those areas of the parameter space that it believes will bring the most promising validation scores

# Vertex Vizier Hyperparameter Tuning
## Quiz
* Which of the following can make a huge difference in model quality?
	* Setting hyperparameters to their optimal values for a given dataset.
* Which of the following is a black-box optimization service?
	* Vertex Vizier
* Which of the following algorithms is useful, if you want to specify a quantity of trials that is greater than the number of points in the feasible space?
	* Grid Search
* Black box optimization algorithms find the best operating parameters for any system whose _____?
	* performance can be measured as a function of adjustable parameters.
* Bayesian optimization takes into account past evaluations when choosing the hyperparameter set to evaluate next. By choosing its parameter combinations in an informed way, it enables itself to focus on those areas of the parameter space that it believes will bring the most promising validation scores. Therefore it ______
	* limits the number of times a model needs to be trained for validation
	* requires less iterations to get to the optimal set of hyperparameter values.
	* enables itself to focus on those areas of the parameter space that it believes will bring the most promising validation scores.

# Prediction and Model Monitoring Using Vertex AI
## Quiz
* Which statement is correct regarding the maximum size for a CSV file during batch prediction?
	* Each data source file must not be larger than 10 GB. You can include multiple files, up to a maximum amount of 100 GB.
* Which of the following statements is invalid for a data source file in batch prediction?
	* *You must use a regional BigQuery dataset*
	* BigQuery data source tables must be no larger than 100 GB.
	* The first line of the data source CSV file must contain the name of the columns.
	* If the Cloud Storage bucket is in a different project than where you use Vertex AI, you must provide the Storage Object Creator role to the Vertex AI service account in that project.
* For which, the baseline is the statistical distribution of the feature's values seen in production in the recent past
	* Drift detection
* What should be done if the source table is in a different project?
	* You should provide the BigQuery Data Editor role to the Vertex AI service account in that project.
* Which statements are correct for serving predictions using Pre-built containers?
	* Pre-built containers are organized by Machine learning framework and framework version.
	* Vertex AI provides Docker container images that you run as pre-built containers for serving predictions.
	* Pre-built containers provide HTTP prediction servers that you can use to serve prediction using minimal configurations.
* What are the features of Vertex AI models monitoring?
	* Feature Attribution and UI visualizations
	* Drift in data quality
	* Skew in training vs. serving data
# Vertex AI Pipelines
## Quiz 
* Which package is used to define and interact with pipelines and components
	* kfp.dsl package
* What can you use to create a pipeline run on Vertex AI Pipelines?
	* Vertex AI python client
* What can you use to compile the pipeline?
	* kfp.v2.compiler.Compiler
* How can you define the pipeline's workflow as a grarph?
	* By using the outputs of a component as an input of another component
# Quizes
Enlace: ![[T-MLGCP5-A-m8-l2-file-en-46.pdf.en.pdf]]
# Best Practices for ML Development
# Course Summary
# Series Summary
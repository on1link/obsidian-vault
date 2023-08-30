# Architecting production ML systems
## Quiz 
* What percent of system code does the ML model account for?
	* 5%
* In the featurestore, the timestamps are an attribute of the feature values, not a separate resource type
	* True
* Match the three of data ingest with an appropriate source of training data
	* Streaming (Pub/Sub), structured batch (BigQuery), unstructured batch (Cloud Storage)
* Which type of training do you use if your data set doesn't change over time?
	* Static training
* [[Vetex AI]] has a unified dat preparation tool that supports image, tabular, text, and video content. Where are uploaded datasets stored in [[Vertex AI]]?
	* A [[Google Cloud Storage]] bucket that acts as an input for both [[AutoML]] and custom training jobs.
* Which type of logging should be enabled in the online prediction that logs the stderr and stdout streams from your prediction nodes to [[Cloud Logging]] and can be useful for debugging?
	* Container loggin
* When you use the data to train a model, [[Vertex AI]] examines the source data type and feature values and infers how it will use that feature in model training. This is called the ______ for that feature.
	* Transformation
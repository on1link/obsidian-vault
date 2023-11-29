#googleCloudPlatform 
# Architecting production ML systems
## Quiz 
* What percent of system code does the ML model account for?
	* 5%
* In the [[Feature Store]], the timestamps are an attribute of the feature values, not a separate resource type
	* True
* Match the three of data ingest with an appropriate source of training data
	* Streaming (Pub/Sub), structured batch ([[BigQuery]]), unstructured batch ([[Cloud Storage]])
* Which type of training do you use if your data set doesn't change over time?
	* Static training
* [[Vertex AI]] has a unified dat preparation tool that supports image, tabular, text, and video content. Where are uploaded datasets stored in [[Vertex AI]]?
	* A Google [[Cloud Storage]] bucket that acts as an input for both [[AutoML]] and custom training jobs.
* Which type of logging should be enabled in the online prediction that logs the stderr and stdout streams from your prediction nodes to [[Cloud Logging]] and can be useful for debugging?
	* Container logging
* When you use the data to train a model, [[Vertex AI]] examines the source data type and feature values and infers how it will use that feature in model training. This is called the ______ for that feature.
	* Transformation
# Designing adaptable ML systems
## Quiz
* Suppose you are building an ML-based system to predict the likelihood that a customer will leave a positive review. The user interface that customers leave reviews on changed a few months ago, but you don't know about this. Which of these is a potential consequence of mismanaging this data dependency?
	* Losses in prediction quality
* What is the shift in the actual relationship between the model inputs and the output called?
	* Concept drift
* Which of the following models are susceptible too a feedback loop? Check all that apply
	* A university-ranking model that rates schools in part by their selectivity (the percentage of students who applied that were admitted).
		* Correct! The model's rankings may drive additional interest to top-rated schools, increasing the number of applications they receive. If these schools continue to admit the same number of students, selectivity will increase (the percentage of students admitted will go down). This will boost these schools' rankings, which will further increase prospective student interest, and so on…
	* A book-recommendation model that suggests novels its users may like based on their popularity (i.e., the number of times the books have been purchased).
		* Correct! Book recommendations are likely to drive purchases, and these additional sales will be fed back into the model as input, making it more likely to recommend these same books in the future.
	* A traffic-forecasting model that predicts congestion at highway exits near the beach, using beach crowd size as one of its features.
		* Correct! Some beachgoers are likely to base their plans on the traffic forecast. If there is a large beach crowd and traffic is forecast to be heavy, many people may make alternative plans. This may depress beach turnout, resulting in a lighter traffic forecast, which then may increase attendance, and the cycle repeats.
* What is training skew caused by?
	* Your development and production environments are different, or different code is used in the training environment than in the development environment
		* Correct! Different versions may cause predictions to be significantly slower or consume more memory in the training environment than in the development environment. Different code may result in different performance.
* Which of the following tools help software users manage dependency issues?
	* Maven, Gradle, and Pip
* Gradual drift is used for which of the following?
	* And old concept that incrementally changes to a new concept over a period of time.
* Which component identifies anomalies in training and serving data and can automatically create a schema by examining the data?
	* Data validation
# Designing High-Performance ML Systems
## Quiz
* If each of your examples is large in terms of size and requires parsing, and your model is relatively simple and shallow, your model is likely to be:
	* I/O bound, so you should look for ways to store data in more efficiently and ways to parallelize the reads.
		* Correct! Your ML training will be I/O bound if the number of inputs is large or heterogeneous (requires parsing) or if the model is so small that the compute requirements are trivial. This also tends to be the case if the input data is on a storage system with low throughput. If you are I/O bound, look at storing the data more efficiently, storing the data on a storage system with higher throughput, or parallelizing the reads. Although it is not ideal, you might consider reducing the batch size so that you are reading less data in each step.
* For fastest I/O performance in TensorFlow...
	* Read in parallel threads.
		* This is one of the correct answers. dataset = tf.data.TFRecordDataset(files, num_parallel_reads=40) When you're dealing with a large dataset sharded across Cloud Storage, you can speed up by reading multiple files in parallel to increase the effective throughput. You can use this feature with a single option to the TFRecordDataset constructor called num_parallel_reads.
	* Prefetch the data
		* This is one of the correct answers. dataset.prefetch decouples the time data is produced from the time it is consumed. It prefetches the data into a buffer in parallel with the training step. This means that we have input data for the next training step before the current one is completed.
	* Read TF records into your model.
		* This is one of the correct answers. dataset = tf.data.TFRecordDataset(...) TF Records are set for fast, efficient, batch reads, without the overhead of having to parse the data in Python.
	* Optimize TensorFlow performance using the Profiler
* What does high-performance machine learning determine?
	* Time taken to train a model
* Which of the following indicates that ML training is CPU bound?
	* If I/O is simple, but the model involves lots of complex/expensive computations.
# Hybrid ML Systems
## Quiz
* To copy the input data into TensorFlow, which of the following syntaxes is correct?
	* inferenceInterface.feed(inputName, floatValues, 1, inputSize, inputSize, 3);
* A key principle behind Kubeflow is portability so that you can:
	* Move your model from on-premises to Google Cloud.
		* Portability is at the container level, and you can move to any environment that offers Kubernetes.
* Which of the following determines the correct property of Tensorflow Lite? 
	* Lower precision arithmetic
	* Quantization
* Which of these are reasons that you may not be able to perform machine learning solely on Google Cloud?
	* You need to run inference on the edge.
	* You are tied to on-premises or multi-cloud infrastructure due to business reasons.
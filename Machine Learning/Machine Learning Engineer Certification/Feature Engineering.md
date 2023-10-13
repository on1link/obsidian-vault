#googleCloudPlatform
## Objetives
- Describe Vertex AI Feature Store and compare the key required aspects of a good feature.
- Perform feature engineering using BigQuery ML, Keras, and TensorFlow.
- Discuss how to preprocess and explore features with Dataflow and Dataprep.
- Use tf.Transform.
# Introduction to [[Vertex AI]] [[Feature Store]]
## [[Feature Store]] benefits
## Feature Store terminology and concepts
## The Feature Store data model

## Creating a Feature Store
## Serving features: Batch and online
## Resources
## Quiz
1. Vertex AI Feature Store provides a centralized repository for organizing, storing, and serving ML features. Using a central feature store, enables an organization to efficiently share, discover, and re-use ML features at scale, which can increase the velocity of developing and deploying new ML applications. What are the key challenges that Vertex AI Feature Store solves
	* Mitigate data storage silos, which occurs when you might have built and managed separate solutions for storage and the consumption of feature values.
	* Detect drift, as a result of significant changes to your feature data distribution over time
	* Mitigate training-serving skew, which occurs when the feature data distribution that you use in production differs from the feature data distribution that was used to train your model.
2. What is one definition of a feature in machine learning?
	* A value that is passed as input to a model
3. Where are the features registered?
	* Feature registry
4. What are the two methods feature store offers for serving features?
	*  Batch serving and Online serving
5. Which of the following is an instance of an entity type? 
	* Entity
6. Which of the following is the process of importing feature values computed by your feature engineering jobs into a featurestore?
	* Feature ingestion
# Raw Data to Features
Feature engineering is often the longest and most difficult phase of building your ML project. In the feature engineering process, you start with your raw data and use your own domain knowledge to create features that will make your machine learning algorithms work. In this module we explore what makes a good feature and how to represent them in your ML model.
## Overview of feature engineering
## Raw data to features
## Good features versus bad features
## Features should be know at prediction-time
## Features should be numeric
## Features should have enough examples
## Bringing human insight
## Representing features
## Resources
## Quiz
* Which of the following statements is true?
	* Different problems in the same domain may need different features.
* A good feature has which of the following characteristics?
	* It should be numeric with meaningful magnitude.
	* It should be related to the objective.
	* It should be known at prediction time.
* Which of the following are the requirements to build an effective machine learning model?
	* It should be able to preprocess with Vertex AI Platform.
	* It should scale to a large dataset.
	* It should find good features.
* In what form can raw data be used inside ML models?
	* After turning your raw data into a useful feature vectors
* Which of the following statements is true about preprocessing?
	* Preprocessing within the context of Cloud ML allow you to do it at scale
# Feature Engineering

This module reviews the differences between machine learning and statistics, and how to perform feature engineering in both [[BigQuery ML]] and [[Keras]]. We'll also cover some advanced feature engineering practices.
## Machine learning versus statistics

## Basic feature engineering
## Advanced feature engineering: Feature crosses
## Bucketize and Transform Functions
## Temporal and geolocation features
## Quiz
* Which of the following is true about Feature Cross?
	* Feature Cross enables a model to learn separate weights for each  combination of features
	* It is a process of combining features into a single feature.
* What is the significance of ML.FEATURE_CROSS?
	* ML.FEATURE_CROSS generates a STRUCT feature with all combinations of crosses categorical features except for 1-degree items.
* Which of the following statements are true regarding the ML.EVALUATE function?
	* The ML.EVALUATE function evaluates the predicted values against the actual data.
	* The ML.EVALUATE function can be used with linear regression, logistic regression, k-means, matrix factorization, and ARIMA-based time series models.
	* You can use the ML.EVALUATE function to evaluate model metrics.
* What is [[one-hot encoding]]?
	* One-hot encoding is a process by which categorical variables are converted into a form that could be provided to neural networks to do a better job in prediction.
* True or False:  Feature Engineering is often one of the most valuable tasks a data scientist can do to improve model performance, for three main reasons:
	1. You can isolate and highlight key information, which helps your algorithms "focus" on what’s important.
	2. You can bring in your own domain expertise.
	3. Once you understand the "vocabulary" of feature engineering, you can bring in other people’s domain expertise.
* What do you use the tf.feature_column.bucketized_column function for?
	* To discretize floating point values into a smaller number of categorical bins
* What is a feature cross?
	* A feature cross is a synthetic feature formed by multiplying (crossing) two or more features. Crossing combinations of features can provide predictive abilities beyond what those features can provide individually.
* Which of the following statements are true regarding the ML.BUCKETIZE function?
	* It bucketizes a continuous numerical feature into a string feature with bucket names as the value
	* ML.BUCKETIZE is a pre-processing function that creates buckets by returning a STRING as the bucket name after numerical_expression is split into buckets by array_split_points.
# Preprocessing and Feature Creation
In this module you will learn more about Dataflow, which is a complementary technology to Apache Beam and both of them can help you build and run preprocessing and feature engineering.
## Apache Beam and Dataflow
## Dataflow terms and concepts
## Resources
## Quiz
* What is one key advantage of preprocessing your features using Apache Beam?
	* Apache Beam transformations are written in Standard SQL which is scalable and easy to author.
* What is the purpose of a Cloud Dataflow connector? .apply(TextIO.write().to(“gs://…”));
	* Connectors allow you to output the results of a pipeline to a specific data sink like Bigtable, Google Cloud Storage, flat file, BigQuery, and more.
* True or False: The Filter method can be carried out in parallel and autoscaled by the execution framework:
	* True: Anything in Map or FlatMap can be parallelized by the Beam execution framework.
* Which of these accurately describes the relationship between Apache Beam and Dataflow?
	* Apache Beam is the API for data pipeline building in Java or Python and Dataflow is the implementation and execution framework.
* Your development team is about to execute this code block. What is your team about to do?
	* ![[Pasted image 20230828171858.png]]
	* We are compiling our Cloud Dataflow pipeline written in Java and are submitting it to the cloud for execution.Notice that we are calling mvn compile and passing in --runner=DataflowRunner.
* To run a pipeline you need something called a ___ ________.
	* runner
* What is one key advantage of preprocessing your features using Apache Beam?
	* The same code you use to preprocess features in training and evaluation can also be used in serving.
* True or False: A ParDo acts on all items at once (like a Map in MapReduce).
	* False
# Feature Crosses - Tensforflow Playground
## What is a feature cross
## Discretization
## Quiz
* Fill in the blanks: In the __ ________ layers, the lines are colored by the __________ of the connections between neurons. Blue shows a _________ weight, which means the network is using that _________ of the neuron as given. An orange line shows that the network is assigning a ___ ______ weight.
	* Hidden, weights, positive, output, negative
* Why might you create an embedding of a feature cross?
	* To create a lower-dimensional representation of the input space
	* To identify similar sets of inputs for clustering
	* To reuse weights learned in one problem in another problem
* True or False: In TensorFlow Playground, in the output layer, the dots are colored orange or blue depending on their original values. The background color shows what the network is predicting for a particular area. The intensity of the color shows how confident that prediction is.
	* True
* True or False:  We can create many different kinds of feature crosses. For example:  
	* [A X B]: a feature cross formed by multiplying the values of two features.  
	* [A x B x C x D x E]: a feature cross formed by multiplying the values of five features.  
	* [A x A]: a feature cross formed by squaring a single feature.
		* **True**
* True or False:  In TensorFlow Playground, orange and blue are used throughout the visualization in slightly different ways, but in general orange shows negative values while blue shows positive values.
	* True
* True or False: In TensorFlow Playground, the data points (represented by small circles) are initially colored orange or blue, which correspond to zero and negative one.
	* False
# Introduction to TensforFlow Transform
## TensorFlow Transform
## Analyze phase
## Transform phase
## Supporting serving
## Quiz
* As an approach to feature engineering, which of the following most accurately describes what TensorFlow Transform is a hybrid of?
	* Apache Beam and TensorFlow
* Fill in the blank: The ______________ _______________ is the most important concept of tf.Transform. The ______________ _______________ is a logical description of a transformation of the dataset. The ______________ _______________ accepts and returns a dictionary of tensors, where a tensor means Tensor or 2D SparseTensor.
	* Preprocessing function
* True or False: One of the goals of tf.Transform is to provide a TensorFlow graph for preprocessing that can be incorporated into the serving graph (and, optionally, the training graph).
	* True
* What does tf.Transform do during the training and serving phase?
	* Provides a TensorFlow graph for preprocessing

# Summary

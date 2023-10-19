#googleCloudPlatform 

# Objectives
* Discuss Data Scientist pain points (Por qué es necesario? MLOps)
* Identify ML Engineering characteristics and challenges (Por qué es necesario? MLOps)
* Compare and contrast DevOps vs MLOps
* Understand the Machine Learning Operations MLOps concept. (Para que sirve MLOps?)
* Introduction to MLOps - a ML model lifecycle management discipline (Para que sirve MLOps?)
* Define how Google Cloud can help with MLOps (Cómo se aplica en el eco sistema de Google Cloud)

# Summary
* Learned how to employing Machine Learning Operations, explore ML models from an operational perspective
	* Examine the challenges that ML practitioners face when they operationalize ML models and deploy to production
	* The concept of DevOps in ML and the phases of the ML lifecycle
	* Main phases of an ML lifecycle, and how these phases map to tasks within MLOps
* Learned [[Vertex AI]] and [[Machine Learning Operations (MLOps)]] on [[Vertex AI]]
	* What vertex AI is
	* MLOps capabilities of Vertex AI
	* Lab

Introduction to MLOps tools and best practices for deploying, evaluating, monitoring and operating production ML systems on Google Cloud

MLOps is a discipline focused on the deployment, testing, monitoring, and automation of ML systems in production.

Machine Learning professionals use tools for continuous improvement and evaluation of deployed models.

The concept of Machine Learning Operations and the considerations behind it 

# Employing Machine Learning Operations
## Why and when to employ MLOps

Why: To shorten the development lifecycle of systems and ensure that high quality software is continuously developed, delivered, and maintained in production
## Machine Learning (ML) practitioners' pain points
Practitioners:
	ML practitioner is used to describe all these different roles throughout the ML lifecycle
Paint point from ML practitioners
* Keeping track of different versions
	* Models and code
	* Data, model architectures
* Controlling the experiment space
	* Different training procedure parameters
	* Hyperparameter values in each trial
	* Performance metrics control
	*  Changes being made
	* Ideas are being tried
		* Which work and which don't
* Pin-pointing the best-performing model
		The best model here refers to the one that delivers the ideal result for the specific use case.
		
* Collaborating
	* With Data Scientist, Data Engineers, ML Engineers, App Devs, site reliability engineers, business analysts and business users in operationalizing the ML models.

* There is the matter of reproducibility
	* Deploying a model to a prodududction environment is difficult unless it can be reproduced.
	* a production application, the model needs to be updated regularly as new data comes in. Therefore, traceability becomes paramount
## The concept of devOps in ML

Operationalizing a model means balancing time, resources, and quality througout the whole system. In software engineering, this approach is called [[DevOps]].

MLOps is a lifecycle management discipline for machine learning.

### Continuous integration (CI)
1. Checkout the code.
2. Complete the task.
3. Validate against the code base.
4. Perform unit testing.
5. Merge the code.
### Continuous delivery or deployment (CD)
1. Build.
2. Test.
3. Release.
![[20231017_230951.png]]

### Continuous training (CT)
1. Monitor.
2. Measure.
3. Retrain.
4. Serve.

MLOps differs from DevOps in important ways:

| DevOps                                          | MLOps                                                     |
|:----------------------------------------------- |:--------------------------------------------------------- |
| Test and validates code and components.         | Also tests and validates data, data schemas, and models.  |
| Focuses on a single software package or service | Also considers the whole system: the ML training pipeline |
| Deploys code and moves the next task.           | Constantly monitors, retrains, and serves the model.      |

ML systems can easily accumulate technical debt due to challenge:
* Multi-functional teams
	* ML projects require significant multi-functional expertise.
* Experimental nature
	* Which requires constantly approaching the data, the models, and parameter configuration in new ways. The real challenge is to try to track all experiments and metadata while try to maintain reproducibility and maximize code reusability.
* Testing complexity
	* Which is more complex than testing other software systems because you need to validate data, parameters, code, and hyperparameters together in a system, instead of only unit-testing methods or functions.
* Deployment complexity
	* ML systems might require you to deploy a multi-step pipeline to automatically retrain and deploy models.
* Model decay
	* Data profiles constantly change, if something changes in the data input, the predictive power of the model in production will probably change with it. Is needed to track summary statistics of the data and monitor the online performance of the model to send notifications or roll back when values deviate from your expectations. Drift is the change in an entity regarding a baseline. With a production ML model, this is the change between the real-time production data and a baseline dataset, most likely the training set, that’s representative of the task the model is intended to perform.
## ML lifecycle


## Automating the ML process

## Quiz
* Which of the following characteristics of delivering an ML model is considered as a characteristic of maturity level 0?
	* Manual, script-driven, and interactive process
* Which of the following steps is part of continuous integration and delivery (CI/CD) but not continuous training (CT)?
	* Building the model
* What is the important aspect of MLOps which differs from DevOps?
	* MLOps constantly monitors, retrains, and serves the model.
* What is the process of monitoring, measuring, retraining, and serving ML models automatically and continuously to adapt to changes in the data before they're redeployed?
	*  Continuous Training
# Vertex AI and MLOps on Vertex AI

## What is [[Vertex AI]] and why does a unified platform matter?
## Introduction to MLOps on [[Vertex AI]]
## How does [[Vertex AI]] help with the MLOps workflow

## Quiz

# Reading List
![[All Reading - MLOps - Getting Started.pdf]]`

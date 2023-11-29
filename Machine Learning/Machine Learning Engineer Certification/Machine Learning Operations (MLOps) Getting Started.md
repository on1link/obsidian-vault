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
	* Examine the challenges that ML practitioners face when they operationalize ML models and deploy to production.
	* The concept of DevOps in ML and the phases of the ML lifecycle.
	* Main phases of an ML lifecycle, and how these phases map to tasks within MLOps.
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
#### The three phases of the ML lifecycle
* Discovery phase
	* Business use case definition
		* Who are the users or who may be affected by the solution?
		* Is developing a model for this use case feasible?
	* Data exploration
	* Architecture and algorithm selection
		* Priotizing use cases
* Development phase
	* It beging in Data exploration with some proof of concepts being developed
	* Data pipeline creation and feature engineering
	* Model building
	* Model evaluation
	* Presentation of results
	* Iterate on approach:
		* Model evaluation - Business use case definition
		* Data should be revisited
		* Consider additional data ETL

* Deployment phase
	* Plan for deployment
		* Which platform host the model
		* how to scale the model
	* Model Operationalization
	* Model Monitoring

## Automating the ML process

![[Captura de pantalla 2023-10-20 a la(s) 11.58.20.png]]

The above steps automated or the level of automation defines the maturity of the ML process
#### Levels of maturity
##### Level 0
Build and deploy manually.
![[Captura de pantalla 2023-10-20 a la(s) 12.02.04.png]]
The characteristics of MLOps level 0 are:
* A manual script-driven and interactive process.
* A disconnection between ML and operation teams.
* Infrequent releases iterations.
* No continuous integration, continuous delivery or continuous deployment.
##### Level 1: ML pipeline automation
Automate the training phase.
![[Captura de pantalla 2023-10-20 a la(s) 12.05.36.png]]
The goal of MLOps level 1 is to perform continuous training of the model by automating the ML pipeline. 
This achieve the Continuous delivery of the model prediction service.
The characteristics of MLOps level 1 are:
* Rapid experiment
* Continuous training of the model in production
* Experimental operational symmetry.
* Modularized code for components and pipelines.
* Continuous deployment of models, which mean continuous delivery of models and automated pipeline deployment.
##### Level 2: CI/CD pipeline automation
Automate training, validation, and deployment.
![[Captura de pantalla 2023-10-20 a la(s) 12.12.40.png]]
MLOps level 2 can be characterized as CI/CD automation for the need of a system for a rapid and reliable update of the pipelines in production.
This allow to rapidly explore new ideas with [[Feature Engineering]], model architecture, and [[hyperparameters]].
This is achieved by the following components:
* Source control
* Test and build services.
* Deployment services.
* [[Model Registry]].
* [[Feature Store]].
* [[ML metadata store]].
* [[ML pipeline orchestrator]].
![[Captura de pantalla 2023-10-20 a la(s) 12.19.15.png]]

#### Full stack for ML system with Vertex AI
![[Captura de pantalla 2023-10-20 a la(s) 12.21.02.png]]

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
### Objetives
* Introduction to [[Vertex AI]], Google's unified AI platform.
* Introduction to [[MLOps]] on [[Vertex AI]].
* Explore how [[Vertex AI]] helps with the [[MLOps]] workflow.

Reming Key construts in machine learning
* Create datasets.
* Train model.
* Iterate the model.
* Evaluate the model.
* Deploy the model.
This end to end process is called MLOps
[[Vertex AI]]
Bring together all the [[Google Cloud]] services for building ML and AI in one unified platform which helps enterprises realized more value with their data and accelerate time to value.
The user interface can be used to directly manage the following stages in the ML workflow.
![[Captura de pantalla 2023-10-20 a la(s) 12.51.43.png]]
In summary [[Vertex AI]] offers to achieve ML goals:
* Fast experimentation
* Accelerated deployment
* Simplified model management 

## Introduction to MLOps on [[Vertex AI]]

## Summary
### MLOps
A set of **standardized** processes and capabilities for building, deploying, and operationalizing ML systems **rapidly** and **reliably**

MLOps concept
MLOps aims to unify ML system development or ML with ML system operations or Ops. Automating and monitoring every step of ML system construction. And finally, it maintains aligned versions of data and models alongside code and components.

**How does MLOps achieve each of these goals?**
![[Captura de pantalla 2023-11-23 a la(s) 17.59.17.png]]

Important to understand what ML engineering is, and how it is tighly couple with data engineering and app enginering

### ML engineering
Superset of the discipline of software enginerring and is disegned to handle the unique complexities of the practical application of ML.
MLOps is one of the pracitces modified

DE: ingesting, processing, and transform data, 
APP: Design, migration app

Engineering an ML-enable solution in a ciclic way between data, ml and app engineering

MLOps lifecycle
![[Captura de pantalla 2023-11-23 a la(s) 18.03.39.png]]
ML dev
Experimentation
Training operationalization
check when model works in production
Continuous training
You retrain prod model with new data
Model deplyment
Predicting serving
Model serving online and bacth prediciton
Continuous monitoring
Model degradetion 

Data & model managament
The most important, to support auditability, traeability, compliance, shareabilit, reusability, and discoberability of ML assets
	datasets, models, inputs file, trainig logs
![[Captura de pantalla 2023-11-23 a la(s) 18.06.48.png]]
Vertex AI automate some of the steps of the pipeline
![[Captura de pantalla 2023-11-23 a la(s) 18.07.18.png]]

Why Vertex serves for this purpose
![[Captura de pantalla 2023-11-23 a la(s) 18.08.23.png]]

4 reason Vertex work
![[Captura de pantalla 2023-11-23 a la(s) 18.10.28.png]]

## How does [[Vertex AI]] help with the MLOps workflow
![[Captura de pantalla 2023-11-23 a la(s) 18.21.59.png]]
Vertex was design to automate and scale the process

1. Set up ML enviroments quickly
2. Automate orchestration
3. Manage large clusters
4. Set up low latency apps

Manage and govern
Explaniation
Experimentation
#### Managing and governing capabilities.
![[Captura de pantalla 2023-11-23 a la(s) 18.23.43.png]]
#### Orchestrating ML workflows capabilities

![[Captura de pantalla 2023-11-23 a la(s) 18.25.53.png]]
#### Understand models behavior
There is the need to reveal the why behind model and its predictions

Vertex Explainable AI
* Provides robust, actionable explanations.
	Feature-base explanaition
	Feature importance into Vertex AI
	Sample Shapley
	Integrated gradients, and Explanation with ranked Area integrals (XRAI)
* Is built into multiple Vertex AI services.
* Is flexible, fast and scalable.
![[Captura de pantalla 2023-11-27 a la(s) 17.42.35.png]]
Fetaure attributions is supported by all type of mdoels
	Frameworks
		Tensorflow, scikit-learn, XGBoost
	AutoML and custom-trained models
	Modelities
		Images, text, tabular, video

Vertex Explainable AI offers three methods to use for feature attributions. Each one is based in Shapley values, a cooperate game theory altorigthm that assigns credit to each player in a game for a particular outcome.
	Sampled Shapley
	Integrated gradients
	XRAI

For more comparison attribution methods, see:
	AI Explanations Whitepaper
	Feature-based explanations documentation

### Monitor
Vertex AI is proactively monitoring the model
	Monitor and alert
	Diagnose
	Update the model
The model perform best when the prediction data is similar to the training data. When the input data deviates from the data used to train the model, the model's performance is deteriorate even if the model hasn't change.
Vertex monitor the model's prediction input data for feature skew and drift. Training skew occurs when the feature data distribution and production deviates from the feature data distribution used to train the model.
If the original data is available, you can enbale skew detection.
Prediction drift occurs when feature data distribution and production changes significantly over time. If the original training data isn't available, you can enable drift detection to monitor the input data for changes over time.

Track
Tracking and comparing mutiple experiments runs and analyzing main model metrics.
The goal is to identify the best model for a particular case.
Vertex AI host different products to monitor and govern your models

![[Captura de pantalla 2023-11-27 a la(s) 18.02.06.png]]

Recall
An artifact is a discrete entity or piece of data produced and consumed by an ML workflow. 
A **context** is used to group artifacts and execution together under a single queriable and taped category.
Context can be used to represent sets of metadata.
Example: Run of ML pipeline

Another Tool to track, visualize, and compare ML experiments and share is [[Vertex AI TensorBoard]] is an enterprise ready managed version of tensorboard.
	Execution and artifacts of a pipeline run are viewable in the GC console.
	Vertex AI TensorBoard provides detailed visualizations, including traicking and visualizing metrics.
![[Captura de pantalla 2023-11-27 a la(s) 18.10.04.png]]

Vertex AI Tabular Workflows
![[Captura de pantalla 2023-11-27 a la(s) 18.10.23.png]]

## Lab
### Learning objectives

- Train a TensorFlow model locally in a hosted [Vertex AI Workbench](https://cloud.google.com/vertex-ai/docs/general/notebooks?hl=sv).
- Create a [managed Tabular dataset](https://cloud.google.com/vertex-ai/docs/training/using-managed-datasets?hl=sv) artifact for experiment tracking.
- Containerize your training code with [Cloud Build](https://cloud.google.com/build) and push it to [Google Cloud Artifact Registry](https://cloud.google.com/artifact-registry).
- Run a [Vertex AI custom training job](https://cloud.google.com/vertex-ai/docs/training/custom-training) with your custom model container.
- Use [Vertex TensorBoard](https://cloud.google.com/vertex-ai/docs/experiments/tensorboard-overview) to visualize model performance.
- Deploy your trained model to a [Vertex Online Prediction Endpoint](https://cloud.google.com/vertex-ai/docs/predictions/getting-predictions) for serving predictions.
- Request an online prediction and explanation and see the response.
Vertex AI custom ML model training workflow
There are two ways you can train a custom model on Vertex AI:

Before you submit a custom training job, hyperparameter tuning job, or a training pipeline to Vertex AI, you need to create a Python training application or a custom container to define the training code and dependencies you want to run on Vertex AI.

**1. Use a Google Cloud prebuilt container**: if you use a Vertex AI prebuilt container, you write a Python `task.py` script or Python package to install into the container image that defines your code for training a custom model. See [Creating a Python training application for a pre-built container](https://cloud.google.com/vertex-ai/docs/training/create-python-pre-built-container) for more details on how to structure you Python code. Choose this option if a prebuilt container already contains the model training libraries you need such as `tensorflow` or `xgboost` and you are just doing ML training and prediction quickly. You can also specific additional Python dependencies to install through the `CustomTrainingJob(requirements=...` argument.

**2. Use your own custom container image**: If you want to use your own custom container, you write your Python training scripts and a Dockerfile that contains instructions on your ML model code, dependencies, and execution instructions. You will build your custom container with Cloud Build, whose instructions are specified in `cloudbuild.yaml` and publish your container to your Artifact Registry. Choose this option if you want to package your ML model code with dependencies together in a container to build toward running as part of a portable and scalable [Vertex Pipelines](https://cloud.google.com/vertex-ai/docs/pipelines/introduction) workflow. 

## Quiz
START
Basic
What is the MLOps life cycle iterative process that retrains you production models with the new data?
Back: Continuous training
Tags: Machine Learning
<!--ID: 1700833050080-->
END
* What component of an ML pipeline is responsible for deploying the model to any edge devices?
	* Upload model and deploy endpoint
* How does end-to-end MLOps help ML practitioners with the [[#ML lifecycle]].
	* End-to-end MLOps helps ML practitioners efficiently and responsibly manage, monitor, govern, and explain ML projects throughout the entire development lifecycle.

# Reading List
![[All Reading - MLOps - Getting Started.pdf]]`
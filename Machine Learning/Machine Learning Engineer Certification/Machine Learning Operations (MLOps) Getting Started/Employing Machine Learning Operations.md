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
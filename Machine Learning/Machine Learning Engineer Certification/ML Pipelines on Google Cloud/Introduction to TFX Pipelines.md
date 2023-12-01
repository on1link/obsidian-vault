### Quiz
START
Which of the following are benefits of running TFX on Google Cloud? Select all that apply.
* I: AI Platform Pipelines is the only supported orchestrator for TFX pipelines.
* II: Simplify scaling of TFX pipeline data processing as your data grows.
* III: Automate your ML operational processes for individual and multiple ML pipelines.
* IV: Increase your pipeline development and experimentation velocity.
Back:
* II: Simplify scaling of TFX pipeline data processing as your data grows.
	* Google Cloud’s managed Dataflow service enables scalable, distributed data processing for your TFX pipeline.
* III: Automate your ML operational processes for individual and multiple ML pipelines.
	* Google Cloud development tools like Cloud Functions, Container Registry, and Cloud Build streamline TFX pipeline code sharing, testing, deployment, and continuous training.
* IV: Increase your pipeline development and experimentation velocity.
	* Running TFX on Google Cloud enables you to run multiple pipelines in parallel on distributed resources with different sets of data splits, models, and hyperparameters to build and deploy TensorFlow models to production faster.
Tags: TFX Machine_leargning_engineer_certification
END
START
Which of the 5 parts of a TFX component is responsible for declaring a component’s input artifacts, output artifacts, and parameters for execution? Select one.
* Component Executor
* ComponentSpec
* Component Interface
* Component Driver
Back:
* ComponentSpec
	* ComponentSpecs are classes for defining a component’s input artifacts, output artifacts, and runtime parameters required for component execution.
Tags: TFX Machine_learning_engineer_certification
END
START
How is TFX pipeline data organized after ingestion by the ExampleGen component? Select one.
* Datasets, Versions, Splits
* Datasets, Splits, Versions
* Spans, Versions, Splits
* Train, Dev, Test Splits.
Back:
* Datasets, Versions, Splits
	* ExampleGen organizes data into Spans, which can contain multiple Versions, which can contain multiple Splits such as train, dev, and test for model performance evaluation.
Tags: TFX Machine_learning_enginner_certification
END
START
Which of the following are benefits of incorporating the ExampleValidator component into your ML project lifecycle? Select all that apply.
* ExampleValidator generates a schema by inferring dataset properties that serves as a common data description for downstream components.
* ExampleValidator can assist in monitoring train/serving skew.
* ExampleValidator can identify data anomalies such as missing values, values outside expected ranges.
* ExampleValidator can be configured to monitor for data drift that can negatively impact model performance.
Back:
* ExampleValidator can assist in monitoring train/serving skew.
	* ExampleValidator is a key part of a TFX continuous training pipeline that compares data splits against the schema artifact to identify train/serving skew that can negatively impact model performance.
* ExampleValidator can identify data anomalies such as missing values, values outside expected ranges.
* ExampleValidator can be configured to monitor for data drift that can negatively impact model performance.
Tags: TFX Machine_learning_enginner_certification
END
# TFX
## TensorFlow Extended
Production-Scale ML Platform based on the TensorFlow Ecosystem
Provides a flexible configuration framework 
Make MLOps easier through the ML lifecycle
Apache Airflow
Apache Beam

- Overview of TFX:
	- Production-scale machine learning platform based on TensorFlow 
	- Open-sourced in 2019, provides flexible configuration and shared libraries
	- Simplifies MLOps through all phases of ML project life cycle
	- Supports Apache Airflow, Apache Beam, and [[Kubeflow]]
	- Deployment targets: TF Serving, TF Lite, TensorFlow JS, TFO
	- Portable to various platforms, including on-premise and Google Cloud
- Benefits of TFX on Google Cloud:
	- Scales ML workflows with data using Dataflow
	- Increases development and experimentation velocity
	- Automates ML operational processes with Google Cloud tools
- TFX Adoption: 
	- Widely used in Alphabet companies and Google's core products
	- Adopted by Twitter, Airbus, SAP Concur, and Yahoo! Japan
	- Active open-source community and corporate partners
- Evolution of TFX:
	- Began with Sibyl in 2007, evolved into TFX with TensorFlow
	- Open-sourced in 2019 to be used globally
- Importance of TFX:
	- Represents best practices in data and model management from Google
	- Implementing ML workflows with TFX improves project success
	- Running TFX on Google Cloud supports infrastructure at scale
# TFX concepts
## Component
A TFX component
	Five elements
	Component specification
	Component driver
	Component executor
	Component publusher
	Component interface

Artifacst
Components at runtime
1. Driver
2. Executor
3. Publisher
TFX pipeline is a seuqence of components connected by channels in a directed acyclic graph (DAG) or artifact dependencies
Runtime parameters
Metadata Store
	Artifact management and an orchestrator for sequential component execution
Horizontal layr coordinate pipeline compoentns
	Integrated Frontend
	Orchestrator: Run pipelines using shared code and condif to distributed
	Shared Libs and Protobufs
		TFXIO
	Pipeline Storage: artifact storage and ML Metadata for piepeline run and artifact metadata


# TFX Libraries


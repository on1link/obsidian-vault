### Quiz

# TFX
## TensorFlow Extended
Production-Scale ML Platform based on the TensorFlow Ecosystem
Provides a flexible configuration framework 
Make MLops easier through the ML lifecicle
Apache Airflow
Apache Beam

- Overview of TFX:
	- Production-scale machine learning platform based on TensorFlow 
	- Open-sourced in 2019, provides flexible configuration and shared libraries
	- Simplifies MLOps through all phases of ML project life cycle
	- Supports Apache Airflow, Apache Beam, and Kubeflow
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


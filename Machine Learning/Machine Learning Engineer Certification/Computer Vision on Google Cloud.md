#googleCloudPlatform 
# Introduction to Computer Vision and Pre-built ML Models for Image Classification
## Quiz
* What does the Vision API do?
	* It assigns labels to images and quickly classifies them into millions of predefined categories. It detects objects and faces, reads printed and handwritten text, and builds valuable metadata into the image catalog
* Which pre-built ML API is used for language translations?
	* Translation API
		* Is built on parallel texts from language translations. It translates texts into more than one hundred languages.
* How does OCR (optical character recognition) transform images into an electronic form?
	* OCR analyzes the patterns of light and dark that make up the letters and numbers to turn the scanned image into text.
		* OCR examines the text of a document and translates the characters into code that can be used for data processing
* How does instance segmentation help in classifying the images?
	* It identifies the boundaries of an object and labels pixels with different colors.
* What are the possible consequences for an ML model being trained with high resolution photos with high color depth?
	* It may lead to performance issues like insufficient computing power.
		* If the ML models is trained with high resolution photos with high color depth, there will be performance issues and an increase in input size with longer training time for the ML model
	* It will increase the input size with longer training time for an ML models
		* If the ML model is trained wiht high resolution photos with high color depth, there will be performance issues and an increase in input size with longer training time for the ML model

# [[Vertex AI]] and [[AutoML]] Vision on Vertex AI
## Quiz
* What does Vertex AI offer to achieve your ML goals?
	* Fast experimentation, accelerated deployment, and simplified model management
* What prediction method do you use for synchronous or real-time prediction that quickly returns a prediction but only accepts one prediction request per API call?
	* Online prediction
		* Vertex AI online prediction is optimized to run your data through hosted models with as little latency as possible.
* What is true about batch prediction?
	* Batch prediction is useful for making several prediction requests at the same time and is optimized to handle a high volume of instances in a job.
* Which AutoML model type analyzes your video data and returns a list of shots and segments where objects are detected?
	* Video object tracking model
		* A video object tracking model analyzes video data and returns a list of shots and segments where certain objects were detected. For example, if it analyzes video data from a soccer game, it can identify and track the ball.
* What method do you use to create and train a model with minimal technical effort to quickly prototype models and explore new datasets before investing in development?
	* [[AutoML]]
		* AutoML lets you create and train a model with minimal technical effort. Even if you want the flexibility of a custom training application, you can use AutoML to quickly prototype models and explore new datasets before investing in development.

# [[Custom Training]] with Linear, Neural Network and Deep Neural Network models
## Quiz
* What does the loss function do?
	* The loss function measures how accurate the model is during training.
		* The loss function is a measure of how accurately your prediction model predicts the expected outcome (or value)
* When can a sequential model be used?
	* A sequential model is appropriate for a plain stack of layers where each layer has exactly one input tensor and one output tensor
		* A sequential model is not appropriate when the model has multiple inputs or multiple outputs.
* What function can be used for a model to do prediction?
	* model.predict()
		* 
# Dealing with image Data
## Quiz
* What is the proportion of the number of parameters in the entire network (CNN) while computing?
	* A large number of parameters comes from the dense layers at the end, and the convolutional layers contain far fewer parameters.
		* To compute the number of parameters in a convolutional layer, multiply the number of parameters per filter by the number of filters and divide by the stride, and then finally add bias terms for each filter.
* How does preprocessing help to improve the quality of the image?
	* Preprocessing suppresses unwanted distortions and enhances the required features that are essential for the application.
		* Before raw images can be fed into an image model, they usually have to be preprocessed. These preprocessing operations can be include resizing, converting between color spaces, cropping, flipping, rotating and transposing for shape transformation or image adjustments, segmentation, and compression for quality enhancement.
* What is data augmentation?
	* Data augmentation is a set of techniques that enhance the size and quality of training datasets with the goal of creating more accurate ML models that generalize better.
		* Data augmentation improves the model's resilience and accuracy by creating more data
* What is negative transfer learning in computer vision?
	* When knowledge is transferred from a less related source, the target performance might be degraded.
		* When labeled data is scarce for a specific target task, the target performance is affected.
* How does transfer learning deal with the data scarcity problem?
	* Transfer learning transfers knowledge across tasks so, instead of creating more data, transfer learning decreases the need for data by initializing the parameters with better values.
		* Transfer learning uses knowledge acquired for one task to solve related tasks.

#googleCloudPlatform 
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
# Vertex AI and [[AutoML]] Vision on Vertex AI

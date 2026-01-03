# Face-Mask-Detection

# **Project : Face Mask Detection Using CNN**

**1. Problem Definition**

The goal of this project is to automatically detect whether a person is wearing a face mask or not using images captured from a camera. This has real-world relevance for public safety, healthcare environments, and access-controlled spaces.

*The task is Binary Image Classification Problem*
*   Class 0 -> Wearing a Mask
*   Class 1 -> Not Wearing a Mask

**2. Dataset Preparation**

2.1 Data Collection

A labeled dataset of facial images was used containing two categories:
With Mask
Without Mask
Each image belongs to exactly one class.

2.2 Data Preprocessing

Before training, the images were processed so the neural network could learn effectively:
* **Resize images**	CNNs require fixed-size inputs
* **Normalize pixel values**	Scale values to 0–1 for stable learning
* **Convert to arrays**	Enable numerical computation
* **Assign labels**	Encode “mask” and “no mask” as numeric classes

This ensures that every image is represented as a consistent numerical tensor.

with mask  -->  1
without mask  -->  0

**Image Processing**
1. Resize the Images
2. Convert the images to numpy arrays


**3. Data Splitting**

The dataset was divided into:
* Training set → Used to learn patterns
* Test set → Used to evaluate final performance
This separation ensures the model is tested on unseen data.

**4. CNN Architecture Design**
A Convolutional Neural Network (CNN) was built from scratch. It has three main types of layers:

4.1 Convolution Layers
These extract visual features like:
* Edges
* Facial contours
* Mask boundaries
They act like pattern detectors.

4.2 Pooling Layers
Pooling layers reduce spatial size while keeping important features.
This:

* Reduces computation
* Makes the model robust to small image shifts

4.3 Fully Connected Layers
After convolution:
* Feature maps are flattened
* Dense layers learn the final decision boundary
* Final layer outputs probability of Mask vs No Mask

**5. Model Compilation**

The network was configured using:
Component	Purpose
* Loss function (binary cross-entropy)	Measures how wrong predictions are
* Optimizer (Adam)	Efficient weight updates
* Metrics (accuracy)	Track classification performance
This prepares the CNN for training.

**6. Model Training**

The CNN was trained over multiple epochs using batches of images.

During training:
* The model learns visual differences between masked and unmasked faces
* Validation accuracy ensures it is not memorizing data
* Loss curves show convergence

**7. Performance Evaluation**

After training, the model was evaluated on test images:
* **Accuracy**	Overall correctness
* **Loss**	Confidence of predictions

**Predictive System**


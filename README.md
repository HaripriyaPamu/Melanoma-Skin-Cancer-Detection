# Melanoma-Skin-Cancer-Detection
## Abstract
> Cancer encompasses more than 200 distinct types, with melanoma being the most lethal form of skin cancer. The diagnostic process for melanoma begins with a clinical assessment, followed by dermoscopic imaging and histopathological analysis. If detected in its early stages, melanoma is highly treatable. The initial step in diagnosing melanoma is performing a visual inspection of the affected skin area. Dermatologists capture dermatoscopic images of skin lesions using a high-resolution camera, which provides an accuracy range of 65-80% in identifying melanoma without additional technical assistance. Through further visual assessment by oncologists and analysis of dermatoscopic images, the overall diagnostic accuracy of melanoma increases to 75-84%. This project aims to develop an automated classification system using image processing techniques to identify skin cancer from images of skin lesions.

## Problem Statement
To build a CNN based model which can accurately detect melanoma. Melanoma is a type of cancer that can be deadly if not detected early. It accounts for 75% of skin cancer deaths. A solution which can evaluate images and alert the dermatologists about the presence of melanoma has the potential to reduce a lot of manual effort needed in diagnosis.

## Table of Contents
* [General Info](#general-information)
* [Model Architecture](#model-architecture)
* [Model Summary](#model-summary)
* [Model Evaluation](#model-evaluation)
* [Technologies Used](#technologies-used)
* [Conclusions](#conclusions)
* [Acknowledgements](#acknowledgements)


## General Information
The dataset consists of 2357 images of malignant and benign oncological diseases, which were formed from the International Skin Imaging Collaboration (ISIC). All images were sorted according to the classification taken with ISIC, and all subsets were divided into the same number of images.

The data set contains the following diseases:

![image](https://github.com/user-attachments/assets/646da812-18a9-4cd7-8432-43e67db86f71)

![image](https://github.com/user-attachments/assets/5f2c5b25-5b44-462c-9db2-d6c06f7fb3fb)

In order to address the challenge of class imbalance, the Augmentor Python package (https://augmentor.readthedocs.io/en/master/) was employed to augment the dataset. This involved generating additional samples for all classes, ensuring that none of the classes had insufficient representation.

### Pictorial representation of skin types

![image](https://github.com/user-attachments/assets/bce6f7d6-6187-4887-88e8-0f828b3bb9b5)

The aim of this task is to assign a specific class label to a particular type of skin cancer.

## Model Architecture
The goal is to classify skin cancer using images of skin lesions. To enhance the accuracy and performance of the classification task, I have designed a custom CNN (Convolutional Neural Network) model.

**Rescaling Layer** – This layer rescales the input values from the range of [0, 255] to a normalized range of [0, 1] to facilitate efficient processing.

**Convolutional Layer** – Convolutional layers apply convolution operations to the input, generating feature maps that are passed to the subsequent layer. The convolution operation reduces the image size by summarizing pixel information from its receptive field into a single value, effectively capturing important features.

**Pooling Layer** – Pooling layers help reduce the spatial dimensions of feature maps, which in turn reduces the number of parameters to learn and decreases the computational load. This layer condenses the information present in a specific region of the feature map produced by the convolution layer.

**Dropout Layer** – The Dropout layer randomly sets a proportion of input units to zero during training, with the frequency determined by a set rate. This technique helps to prevent overfitting by making the model more robust.

**Flatten Layer** – The flattening process transforms the multi-dimensional data output from the convolutional layers into a one-dimensional array, preparing it for input into the next layer. This process creates a long feature vector that connects to the fully connected layer in the final classification model.

**Dense Layer** – Dense layers, also known as fully connected layers, have neurons that are deeply interconnected. Each neuron in the dense layer receives input from all neurons in the preceding layer, allowing for complex learning and pattern recognition.

**Activation Function (ReLU)** – The Rectified Linear Unit (ReLU) is an activation function that outputs the input directly if it is positive and outputs zero if the input is negative. ReLU overcomes the vanishing gradient problem, leading to faster learning and improved model performance.

**Activation Function (Softmax)** – The Softmax function is typically used in the output layer of neural network models that predict multinomial probability distributions. It converts the output into probabilities, ensuring that the sum of all probabilities equals one, with each probability ranging from 0 to 1. This makes it ideal for multi-class classification tasks.

## Model Summary

![image](https://github.com/user-attachments/assets/c2d23105-fc4c-4c7a-aafc-bfbd56da8e35)

## Model Evaluation

![image](https://github.com/user-attachments/assets/83a93fc9-ff1c-46dd-9c3a-5332682f6a92)


## Conclusions
- Accuracy of the model on Training Data is: 83.98%
- Accuracy of the model on Validation Data is: 81.96%
- The training and validation accuracy of the aforementioned model fall within a similar range, displaying no signs of underfitting or overfitting.
- The model's training accuracy shows a steady increase of upto 83.98%, and validation accuracy also showed the increase till 81.96%.
- A high training and validation accuracy suggests the model has effectively captured the noise within the data and is well fitted on the validation dataset


## Technologies Used
- Python - version 3.11.4
- Matplotlib - version 3.7.1
- Numpy - version 1.24.3
- Pandas - version 1.5.3
- Seaborn - version 0.12.2
- Tensorflow - version 2.15.0


## Acknowledgements
- UpGrad tutorials on Convolution Neural Networks (CNNs) on the learning platform and the professors of IIITB

- [Melanoma Skin Cancer](https://www.cancer.org/cancer/types/melanoma-skin-cancer/about/what-is-melanoma.html)

- [Introduction to CNN]( https://www.analyticsvidhya.com/blog/2021/05/convolutional-neural-networks-cnn/) 


## Contributors
[Haripriya_Pamu](https://github.com/HaripriyaPamu)


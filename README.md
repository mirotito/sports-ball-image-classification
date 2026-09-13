# Sports Ball Image Classification

A computer vision project investigating sports-ball image classification through two progressively advanced approaches: classical feature-based machine learning and a custom convolutional neural network (CNN) trained from scratch.

---

## Project Overview

This project explores how different computer vision and machine learning approaches can be applied to classify images of sports balls across six categories.

The work was developed through multiple milestones, progressing from manually engineered visual features and traditional machine learning to deep learning with a custom CNN.

The project therefore provides a practical comparison between:

- **Classical Computer Vision + Support Vector Machine (SVM)**
- **Deep Learning + Custom Convolutional Neural Network**

The objective was not only to achieve accurate classification, but also to understand the complete image-classification pipeline, from image preprocessing and feature extraction to model training and evaluation.

---

## Project Development

The project follows a progressive development path:

```text
                    SPORTS BALL IMAGES
                           |
                           v
              +------------------------+
              | Image Preprocessing    |
              | OpenCV                 |
              +-----------+------------+
                          |
             +------------+------------+
             |                         |
             v                         v
   CLASSICAL COMPUTER VISION      DEEP LEARNING
             |                         |
             v                         v
       HSV Features              Raw Images
       HOG Features                   |
             |                         v
             v                  Custom CNN
       Feature Scaling                 |
             |                         v
             v                  Softmax Output
       SVM Classifier                  |
             |                         |
             v                         v
       Classification          Classification
             |                         |
             +------------+------------+
                          |
                          v
                  MODEL COMPARISON


Milestone 2 — Classical Computer Vision

The first milestone investigates a traditional computer-vision pipeline based on manually engineered visual features.

Instead of learning image representations automatically, relevant information is extracted from the images and provided to a Support Vector Machine classifier.

Image Processing Pipeline

The classical approach consists of the following stages:

Image loading
Image preprocessing using OpenCV
Conversion to HSV color space
Gaussian blurring
HOG feature extraction
HSV color histogram extraction
Feature normalization
SVM classification using an RBF kernel
Model evaluation
Feature Representation

Two complementary types of visual information were extracted:

HOG — Histogram of Oriented Gradients

HOG captures local gradient and edge information, providing information about the visual structure and shape of objects.

HSV Color Histograms

HSV-based features capture color-distribution information that can help distinguish between different sports-ball categories.

The extracted features were combined and normalized before being provided to the classifier.

Classifier

The resulting feature representation was classified using a:

Support Vector Machine (SVM) with an RBF kernel

Reported Performance

The classical computer-vision approach achieved approximately:

78% classification accuracy

Milestone 3 — Custom Convolutional Neural Network

The third milestone advances the project from manually engineered features to deep learning.

A custom Convolutional Neural Network was designed and trained from scratch, without relying on a pretrained model.

Instead of explicitly defining visual features such as HOG or color histograms, the CNN learns useful image representations during training.

CNN Architecture

The network incorporates several fundamental deep-learning components:

Convolutional layers
Batch normalization
Max pooling
Dropout
Fully connected layers
Softmax output layer

Processing Concept::
Input Image
     |
     v
Convolution
     |
     v
Batch Normalization
     |
     v
Pooling
     |
     v
Convolutional Feature Extraction
     |
     v
Dropout
     |
     v
Fully Connected Layers
     |
     v
Softmax Classification
     |
     v
Predicted Sports-Ball Class

Classification

The CNN was trained to classify images across six sports-ball categories.

Reported Performance

The final CNN achieved approximately:

86% test accuracy


Classical Computer Vision vs. CNN

The project provides a direct comparison between manually engineered image features and learned deep visual representations.

| Approach                  | Feature Representation         | Classifier          | Reported Accuracy |
| ------------------------- | ------------------------------ | ------------------- | ----------------: |
| Classical Computer Vision | HOG + HSV features             | SVM with RBF kernel |              ~78% |
| Deep Learning             | Learned convolutional features | Custom CNN          |              ~86% |




The reported results show an improvement from approximately 78% with the classical computer-vision pipeline to approximately 86% with the custom CNN.

This progression demonstrates the practical difference between explicitly engineered image features and representations learned automatically through convolutional layers.

Technical Methodology
1. Image Preprocessing

OpenCV was used as part of the image-processing pipeline.

The preprocessing stage included operations such as:

Image loading
Color-space conversion
Gaussian blurring
Preparation of images for feature extraction or neural-network training
2. Feature Engineering

For the classical computer-vision approach, visual information was represented using:

HOG descriptors
HSV color histograms

These features provide complementary information about image structure and color distribution.

3. Traditional Machine Learning

The engineered features were normalized and passed to an SVM classifier using an RBF kernel.

This approach represents a traditional machine-learning workflow in which the quality of the manually designed feature representation plays an important role in classification performance.

4. Deep Learning

The second approach replaces manual feature engineering with a custom CNN.

The CNN learns hierarchical image representations directly from the training data through convolutional operations.

The architecture incorporates normalization, pooling, regularization, and fully connected classification layers.

5. Model Evaluation

The approaches were evaluated using classification accuracy, allowing the performance of the classical and deep-learning pipelines to be compared.

The reported results were:

SVM: ~78%
CNN: ~86%
Key Concepts Demonstrated
Computer Vision
Image preprocessing
OpenCV
HSV color space
Gaussian filtering
HOG feature extraction
Color histograms
Image classification
Machine Learning
Feature engineering
Feature normalization
Support Vector Machines
RBF kernels
Classification evaluation
Deep Learning
Convolutional Neural Networks
Convolutional feature extraction
Batch normalization
Max pooling
Dropout
Fully connected layers
Softmax classification
Training a CNN from scratch
Technologies & Tools
Python
OpenCV
NumPy
Scikit-learn
TensorFlow / Keras
Jupyter Notebook
Support Vector Machines
Convolutional Neural Networks
Repository Structure
sports-ball-image-classification/
│
├── Milestone_2.ipynb
│   └── Classical computer vision and SVM pipeline
│
├── milestone_3.ipynb
│   └── Custom CNN classification pipeline
│
├── Milestone 3 Report.pdf
│   └── Detailed project documentation and evaluation
│
├── sports_ball_classification_presentation.pptx
│   └── Project methodology, results, and presentation material
│
└── README.md
    └── Project documentation


Results Summary::::

| Metric              | Classical CV + SVM |             Custom CNN |
| ------------------- | -----------------: | ---------------------: |
| Feature Engineering |           Required |  Learned automatically |
| Main Features       |          HOG + HSV | Convolutional features |
| Classifier          |            RBF SVM |         Neural Network |
| Pretrained Model    |                 No |                     No |
| Reported Accuracy   |               ~78% |                   ~86% |


Author

Omar Hammad

Automation & Control Engineering
AI | Computer Vision | Embedded Systems | Robotics | Industrial Automation

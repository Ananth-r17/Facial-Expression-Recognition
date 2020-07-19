# Facial Expression Recognition
To perform Facial Expression Recognition using Keras and Tensorflow.

## Description:
In this project we are presenting the real time facial expression recognition of seven most basic human expressions: ANGER, DISGUST, FEAR, HAPPY, NEUTRAL SAD, SURPRISE.
This model can be used for prediction of expressions of both still images and real time video. However, in both the cases we have to provide image to the model. In case of real time video the image should be taken at any point in time and feed it to the model for prediction of expression. The model will generate seven probability values corresponding to seven expressions. The highest probability value to the corresponding expression will be the predicted expression for that image. For better prediction we have decided to keep the size of each image 350*350.

![alt](https://github.com/Ananth-r17/Facial-Expression-Recognition/blob/master/2-Figure1-1.png)

## Problem Statement:
##### CLASSIFY THE EXPRESSION OF FACE IN IMAGE OUT OF SEVEN BASIC HUMAN EXPRESSION

## Source Data:
The source data is taken from Kaggle. It includes the Training and Test Dataset as well as the video for Facial Expression Recognition.
- Source Data: https://www.kaggle.com/c/challenges-in-representation-learning-facial-expression-recognition-challenge

## Prerequisits:
- Python 3+
- Anaconda Navigator (It contains ipython notebook and most of the libraries which are needed like sklearn, pandas, seaborn, matplotlib, numpy)
- Keras
- Tensorflow

## Installing:
- Python 3: https://www.python.org/downloads/
- Anaconda: https://www.anaconda.com/download/
- Tensorflow: In conda environment ``` conda install -c conda-forge tensorflow ```
- Keras: In conda environment ```conda install -c conda-forge keras```

### Task 1: Importing:

#### Libraries:

For Analysis of of Test Data:
- Numpy
- Seaborn
- Matplotlib

For Fitting the Sample for Facial Recognition:
- Tensorflow
- Keras

#### Packages:

Image Preprocessing:
- ImageDataGenerator

Layers for Neural Networks:
- Dense
- Input
- Dropout
- Flatten
- Conv2D
- BatchNormalization
- MaxPooling2D

Models:
- Model
- Sequential

Optimizer:
- Adam

Utils:
 plot_model-
 
 
 ### Task 2: Generate Training and Validation Batches:
 
ImageDataGenerator for Train:
- flow_from_directory (Train)

ImageDataGenerator for Validation
- flow_from_directory (Test)

### Task 3: Creating CNN Model:

Initialising the CNN (relu activation):
- Sequential()

Steps:
- 1st Convolution layer (Conv2D - 64,(3,3))
- 2nd Convolution layer (Conv2D - 128,(5,5))
- 3rd Convolution layer (Conv2D - 512,(3,3))
- 4th Convolution layer (Conv2D - 512,(3,3))
- Flattening
- Fully Connected 1st layer (Batch Norm - Dense(256))
- Fully connected 2nd layer (Batch Norm - Dense(512))
- Adam Optimizer (lr=0.0005)

#### Task 4: Visualizing Model Architecture

![alt](https://github.com/Ananth-r17/Facial-Expression-Recognition/blob/master/model.png)

#### Task 6: Train and Evaluate Model

- Training with 15 epochs
- ReduceLROnPlateau
- ModelCheckpoint
- model.fit
 
## Author:
Ananth Rajagopal: https://github.com/Ananth-r17

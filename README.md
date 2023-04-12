# Object-Detection-using-Tensorflow-API

This repository consists of an Object detection project using Tensorflow API. Also, it includes some finetuning of an SSD model using Modelzoo.

### Introduction to Dataset

The dataset consisting of images of construction workers was trained on a SSD model. This model was obtained from a modelzoo, a platform that provides a collection of pre-trained machine learning models and deep learning models for a variety of tasks such as image classification, object detection, semantic segmentation, natural language processing, and more. The models on ModelZoo are trained on large datasets and are made available for the community to use and build upon.

### Setting up environment for Tensorflow API

In order to use a model from Modelzoo it is crucial to set up a tensorflow api on a local machine or on the web-based IDE. For this model I used colab as a platform as it easily adjusts and integrates to a variety of APIs. 

Once the environment was set, I created directories for uploading the training and test images obtained from yolo, and performed annotations to train the model further. 

### SSD Model architecture

An SSD model with following specifications was downloaded and imported for further fine tuning. The model consisted of a Single Shot Detector architecture, a pretrained model that was previously trained on coco-dataset from ModelZoo. This model has 50 layered ResNet with a Feature Pyramid Network for multiscale feature extraction. Along with a RetinaNet50 Object detection head.

Model Type :SSD ResNet50 V1 FPN 640x640 (RetinaNet50)
Speed(mS): 46
mAP: 34.3

### Finetuning the model

Using a batch-size of 4, for a number of 100 batches, with SGD optimizer with a learning rate of 0.01, I trained the model for over 30 epochs. Once the SSD model from Modelzoo was fine-tuned, a number of test images were passed on to the trained model.  

![image](https://user-images.githubusercontent.com/54207028/231530846-ca1d5ad6-a7dd-47d2-bbf9-7ffb32da5af9.png)

After training the model, initially fluctuations were observed in the loss where in the later batches, the loss started to decrease.

![image](https://user-images.githubusercontent.com/54207028/231531088-63a2b248-f802-4903-9138-82731a96e50d.png)

### Inference

Although the model did predict well for most of the images during the inference, however not all of the images were predicted correctly. The model did overfit on the images that were presented during the training set and couldnt generalize well on the test set.

![image](https://user-images.githubusercontent.com/54207028/231529233-e22b2709-5be4-4d2a-b0dc-a43ff6df2c04.png)

Linkto my colab file: https://colab.research.google.com/drive/1s8SGKRrVF-lwYJtHK0YuDugFXc0nN8WT

Thanks.

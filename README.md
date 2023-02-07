# Pneumonia Detection through X-Ray Images

#### Ángela Gómez Sacristán, Álvaro González Berdasco y Lucía Martín Fernández

## Introduction

https://www.mayoclinic.org/es-es/diseases-conditions/pneumonia/symptoms-causes/syc-20354204#:~:text=La%20neumon%C3%ADa%20es%20una%20infecci%C3%B3n,escalofr%C3%ADos%20y%20dificultad%20para%20respirar.

Pneumonia is an infection that inflames the air sacs of one or both lungs. The air sacs may fill with fluid or pus (purulent material), causing coughing up phlegm or pus, fever, chills and shortness of breath. Various microorganisms, such as bacteria, viruses and fungi, can cause pneumonia.
Signs and symptoms of pneumonia vary from moderate to severe and depend on several factors, such as the type of germ that caused the infection, age and general health. Moderate signs and symptoms are often similar to those of a cold or the flu, but last longer.
Signs and symptoms of pneumonia may include the following:
- Chest pain when breathing or coughing.
- Disorientation or changes in mental perception (in adults age 65 and older)
- Cough that may produce phlegm
- Fatigue
- Fever, sweating, and shaking chills
- Lower than normal body temperature (in adults over age 65 and people with weak immune systems)
- Nausea, vomiting or diarrhea
- Shortness of breath

The models included in this repository, serve to predict whether a patient has pneumonia or not from an X-ray image of their lungs. The data used to train, validate and test these models can be downloaded in https://www.kaggle.com/paultimothymooney/chest-xray-pneumonia. 

First, we performed an Exploratory Anlysis of the Data that can be found in the `Data_exploration.ipynb` notebook. Then, we proceed to generate the following models: 

## 1. LeNet5 with BigDL

Code inspired by https://github.com/intel-analytics/BigDL/blob/main/python/dllib/examples/lenet/lenet.py


## 2. Resnet50

ResNet-50 is a convolutional neural network that is 50 layers deep. 
Code inspired by https://www.kaggle.com/code/danushkumarv/pneumonia-detection-resnet

## 3. CovNet

Code inspired by https://www.kaggle.com/code/karnikakapoor/pneumonia-diagnosis-convnet-model

## Conclusions



### Requirements

To run the colab notebookes attached, it is necesary to download the data (https://www.kaggle.com/paultimothymooney/chest-xray-pneumonia) and upload it to yout Colab Notebook folder in your Google Drive. 

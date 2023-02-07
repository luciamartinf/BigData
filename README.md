# Pneumonia Detection through X-Ray Images

#### Ángela Gómez Sacristán, Álvaro González Berdasco y Lucía Martín Fernández

## Introduction

Pneumonia is an infection that inflames the air sacs of one or both lungs. The air sacs may fill with fluid or pus (purulent material), causing coughing up phlegm or pus, fever, chills and shortness of breath. Various microorganisms, such as bacteria, viruses and fungi, can cause pneumonia.
Signs and symptoms of pneumonia vary from moderate to severe and depend on several factors, such as the type of germ that caused the infection, age and general health. Moderate signs and symptoms are often similar to those of a cold or the flu, but last longer [1].
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

First, we performed an Exploratory Anlysis of the Data that can be found in the `Data_exploration.ipynb` notebook. Then, we proceed to generate different deep learning models based on convolutional neural network. A Convolutional Neural Network, also known as CNN or ConvNet, is a class of neural networks that specializes in processing data that has a grid-like topology, such as an image. The following steps were involved in the convolutional neural network model building:

1. Initialising the model
2. Defining by adding layers
3. Compiling the model (not necessary for the ResNet50 Model)
4. Fitting (training) the model 
5. Evaluate the model with the test dataset


## 1. LeNet5 with BigDL

LeNet-5 was one of the first convolutional applications of image processing [2]. It was originally created for digit classification. Its architecture is made up of 7 layers excluding the input layer. The 7 layers consist of 3 convolutional layers, 2 subsampling layers and 2 fully connected layers. 

`LeNet5_BigDL.ipynb` code is inspired by https://github.com/intel-analytics/BigDL/blob/main/python/dllib/examples/lenet/lenet.py

**Accuracy: 0.8125**

We found out that functions and methods implemented in the bigdl.dllib library are sometimes pretty different from original keras methods and functions which complicated the building of different models implement the bigdl.dllib library.

Considering these difficulties, we decided to build the lenet model implement the bigdl.dllib library and two other different models using tensorflow


## 2. Generic CovNet

`CovNet.ipynb` code is inspired by https://www.kaggle.com/code/karnikakapoor/pneumonia-diagnosis-convnet-model

**Accuracy: 0.8478**


## 3. ResNet50

ResNet-50 is a convolutional neural network that is 50 layers deep. 

`ResNet50.ipynb` code is inspired by https://www.kaggle.com/code/danushkumarv/pneumonia-detection-resnet

**Accuracy: 0.8958**


## Conclusions

Regarding the LeNet5 model we observe that it can still improve a lot since we obtained a pretty high loss. However, the accuracy obtained (81.25%) is not so bad. This shows the potential of this model, with further training and using more data, we could expect some promising results. 

However, the best results are shown for the ResNet50 model. It has a great number of layers and reaches the best results (89.58%). Nevertheless, the generic CovNet model shows also some promising results (84.78% accuracy) 


## Requirements

To run the colab notebookes attached, it is necesary to download the data (https://www.kaggle.com/paultimothymooney/chest-xray-pneumonia) and upload it to yout Colab Notebook folder in your Google Drive. 

## References

[1] https://www.mayoclinic.org/es-es/diseases-conditions/pneumonia/symptoms-causes/syc-20354204#:~:text=La%20neumon%C3%ADa%20es%20una%20infecci%C3%B3n,escalofr%C3%ADos%20y%20dificultad%20para%20respirar.

[2] Lecun, Y. et al. (1998) 'LeNet', Proceedings of the IEEE, (November), pp. 1-46.

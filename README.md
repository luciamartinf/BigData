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

Code inspired by https://github.com/intel-analytics/BigDL/blob/main/python/dllib/examples/lenet/lenet.py

We found out that functions and methods implemented in the bigdl.dllib library are sometimes pretty different from original keras methods and functions which complicated the building of different models implement the bigdl.dllib library.

Considering these difficulties, we decided to build the lenet model implement the bigdl.dllib library and two other different models using tensorflow


## 2. Generic CovNet

Code inspired by https://www.kaggle.com/code/karnikakapoor/pneumonia-diagnosis-convnet-model


## 3. ResNet50

ResNet-50 is a convolutional neural network that is 50 layers deep. 

Code inspired by https://www.kaggle.com/code/danushkumarv/pneumonia-detection-resnet


## Conclusions

We observe that the model can still improve a lot since we are obtained a pretty high Loss. However, the accuracy obtained is not so bad. This shows the potential of this model, with further training and using more data, we could expect some promising results

The results of this model are very good (84.8% accuracy).

163/163 [==============================] - 1149s 7s/step - loss: 0.1887 - accuracy: 0.9237
Train Loss:  0.1886528730392456
Train Accuracy:  0.9236963391304016
312/312 [==============================] - 142s 456ms/step - loss: 0.2596 - accuracy: 0.8958

Test loss:  0.2596129775047302
Test Accuracy:  0.8958333134651184

Resnet50 shows that we could create a model with a great number of layers and reach very good results, as we can see in the accuracy of the train dataset

Still, the convnet model does not reach de accuracy levels of the resnet50 model (around 89% accuracy on the test set).


### Requirements

To run the colab notebookes attached, it is necesary to download the data (https://www.kaggle.com/paultimothymooney/chest-xray-pneumonia) and upload it to yout Colab Notebook folder in your Google Drive. 

## References

[1] https://www.mayoclinic.org/es-es/diseases-conditions/pneumonia/symptoms-causes/syc-20354204#:~:text=La%20neumon%C3%ADa%20es%20una%20infecci%C3%B3n,escalofr%C3%ADos%20y%20dificultad%20para%20respirar.

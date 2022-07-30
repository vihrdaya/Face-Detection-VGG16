# Face-Detection-VGG16
Using the VGG16 CNN to model face detection

## Introduction

I am training the VGG16 CNN model to detect and classify pictures of faces. This is an update of an earlier project I made in 2020 where I used a haar cascade to find faces in an image and used a gaussian blur to blur the faces. I wanted to use something a tad more complicated and newer to try facial detection. My original intention was to create my own cascades, but after some research I found out that cascades were becoming obsolete. Thus, I arrived at CNNs. Although I am only at the edge of the field, I am very fascinated at the power and efficiency of the models. I've been experimenting non-stop with snippets of code I almost forgot to actually work on a full project. I can't wait to see how far I can push these models.

## The Model

I trained the model on four epochs, anymore was overkill, even four might have been overkill.

##### Epoch 1/4
485/485 [==============================] - 445s 916ms/step - loss: 0.0197 - accuracy: 0.9977
##### Epoch 2/4
485/485 [==============================] - 449s 926ms/step - loss: 0.0075 - accuracy: 0.9994
##### Epoch 3/4
485/485 [==============================] - 452s 931ms/step - loss: 0.0010 - accuracy: 0.9999
##### Epoch 4/4
485/485 [==============================] - 452s 933ms/step - loss: 1.0392e-07 - accuracy: 1.0000

##### Loss against Epochs:
![Loss_Chart ](https://user-images.githubusercontent.com/49893887/181924783-fb968de5-74ec-4b4f-b5b8-73dd1a7b8ff0.png)

##### Accuracy against Epochs:

![Acc_Chart ](https://user-images.githubusercontent.com/49893887/181924810-6856b814-5990-4d36-85ea-300fbd6cd5e6.png)

## The Prediction Results

I have split my data with train_test_split(), and have a list of directories of images (both of faces and non faces) that I can use to test against. Here is a random test image.


1/1 [==============================] - 0s 60ms/step

probability: 100.0%

Predicted class :  not face

![output1](https://user-images.githubusercontent.com/49893887/181924838-0580ab8c-f6a1-44d3-b05b-0c610b00e11c.png)

I wanted to use an external image from outside the dataset. I thought that perhaps the training dataset was too homogenious mixed with my concerned about the model being overtrained, it would perform pooly with an external image.

1/1 [==============================] - 0s 46ms/step

probability: 99.96482133865356%

Predicted class :  face


![output2](https://user-images.githubusercontent.com/49893887/181924857-5ef3c879-1183-473d-a4c7-6c9cd7117d9c.png)




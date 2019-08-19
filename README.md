# Multi Class Image Classification of Yoga postures using Watson Studio and Deep Learning as a Service

Computer vision usability is on the rise these days and there could be scenarios where a machine has to classify images based on their class to aid the decision making process. In this pattern, we will demonstrate a methodology to do multi class classification (with around 4 classes) using Watson Studio. We will be using yoga postures data to identify the class given an image. This methodology can be applied to any domain and dataset which requires multiple classes of images to be classified accurately which can be extended for further analysis. Some of the advantages of computer vision are reliability, accuracy, cost reduction, wide range of use and simpler processes. We will demonstrate how to use Python scripts & drag n drop GUI for achieving the objective.

## Introduction
The purpose of this tutorial is to discuss a few methods to preprocess the images before it is ingested into model building process. This includes resizing the images, creating the pixel arrays of images and pickling the data, removing background noise from the images et'al.

## Prerequisites
Users are expected to be aware of Python, computer vision, deep learning and IBM cloud environment & services.

## Estimated time
It should take about 45 mins to an hour to complete the tutorial.

## Steps

**Resizing the images** : This is an important step where the images are standardized and resized to a specific shape which is usually 224/224. Images come in different shapes and to help the model learn better, it is necessary to resize it to avoid extra padding of the images. The pre-trained models also require the images to be resized before they are ingested into the models.

![](https://github.com/IBM/image-preprocessing-for-deep-learning-models/blob/master/doc/source/images/resize_image.png)

**Pickle the data** : In this step, we will discuss how and why do we need to pickle the images data. The primary reason is to convert the images from jpeg/png format into a pixel array which will have inputs and targets defined. This array of numbers will help any model (machine learning, deep learning & pretrained) to learn the features and understand the pattern well of any given class which will enhance the accuracy of the model. We will see in below steps how to create a pixel array and write it into a pickle file.

`First step`

![](https://github.com/IBM/image-preprocessing-for-deep-learning-models/blob/master/doc/source/images/create_txt.png)

`Next Step`

![](https://github.com/IBM/image-preprocessing-for-deep-learning-models/blob/master/doc/source/images/extract_data.png)

`Subsequent Steps`
![](https://github.com/IBM/image-preprocessing-for-deep-learning-models/blob/master/doc/source/images/create_pkl_file_1.png)
![](https://github.com/IBM/image-preprocessing-for-deep-learning-models/blob/master/doc/source/images/create_pkl_file_2.png)

From the screenshots, we are able to define the input & target parameters using a text file, convert the raw image data into pixel array and then dump them into a pickle file which will be consumed by deep learning models. `This step is mandatory for deep learning frameworks like Tensorflow or Keras and for creating experiments in Watson Machine Learning.` Repeat this process thrice for creating training, testing & validation pickle files. Another point to be noted is that all images are to be of same size in order to pickle the data which is why the resizing of images has to be done first before pickling the data.

**Remove background noise** : This step is to enhance accuracy by removing the background of an image. An image consists of features and if the goal is to identify a person or an object, then we can try to remove all other features apart from the one in question. An example is given below with code snippet where we try to identify the posture of the person and we are removing most of the other features which are not relevant.

![](https://github.com/IBM/image-preprocessing-for-deep-learning-models/blob/master/doc/source/images/rmv_bckgnd_1.png)
![](https://github.com/IBM/image-preprocessing-for-deep-learning-models/blob/master/doc/source/images/rmv_bckgnd_2.png)

![](https://github.com/IBM/image-preprocessing-for-deep-learning-models/blob/master/doc/source/images/remove_bckgrnd.png)

## Summary
We have discussed a few steps which are part of image preprocessing and these steps can help a great deal with regards to enhancing model accuracy. I will try to add a few more as and when time permits.

## Related links
The implementation of deep learning methodology for image classification is available here. Please explore these steps and see how the performance improves with preprocessing the images. 

View the code, demo and more at https://github.com/IBM/create-a-predictive-system-for-image-classification-using-deep-learning-as-a-service

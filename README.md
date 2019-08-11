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
![](https://github.com/IBM/image-preprocessing-for-deep-learning-models/blob/master/doc/source/images/create_txt_file.png)

`Next Steps`
![](https://github.com/IBM/image-preprocessing-for-deep-learning-models/blob/master/doc/source/images/extract_data.png)

`Subsequent Steps`
![](https://github.com/IBM/image-preprocessing-for-deep-learning-models/blob/master/doc/source/images/create_pkl_file_1.png)
![](https://github.com/IBM/image-preprocessing-for-deep-learning-models/blob/master/doc/source/images/create_pkl_file_2.png)

From the screenshots, we are able to define the input & target parameters using a text file, convert the raw image data into pixel array and then dump them into a pickle file which will be consumed by deep learning models. Repeat this process thrice for creating training, testing & validation pickle files. Another point to be noted is that all images are to be of same size in order to pickle the data which is why the resizing of images has to be done first before pickling the data.

**Remove background noise** :


## Summary
State any closing remarks about the task or goal you described and its importance. Reiterate specific benefits the reader can expect from completing your tutorial. Recommend a next step (with link if possible) where they can continue to expand their skills after completing your tutorial.
## Related links
Include links to other resources that may be of interest to someone who is reading your tutorial.

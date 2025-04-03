# Dog Breed Detector

A simple AI model for detecting dog breeds in a given image.

## Introduction

This repo demonstrates a complete pipeline for the training of a computer vision model. It is consisted of 2 main notebooks:

+ `dog_breed_detector.ipynb` which is the main notebook for training the model.
+ `dog_breed_detector_app.ipynb` which is a simple _prototype_ app that could be run with `voila`.

## The Pipeline

You can view the main pipeline for training a computer vision model in `dog_breed_detector.ipynb`.

We used DuckDuckGo search engine to gather images of 3 different dog breeds. Then we resize images and remove invalid ones. The images would finally go through _data augmentation_ in order to get prepared to be used for training our model.

We used the `resnet18` architecture for training our model. In order to clean our data, we use the model to find images with highest loss and then use the `fastai`'s `ImageClassifierCleaner` widget to clean our data and re-train the model.

The final weights are exported into `dog_breed_detector.pkl`.

## Prototype Web App

You need to install `voila` for running the Web App.

```bash
pip install voila
```

Then, you can simply run the app notebook by Voila.

```bash
voila dog_breed_detector_app.ipynb
```

This opens up a webpage in your default browser which allows you to upload an image and get the inference of the model about which breed of dog is present in the image.

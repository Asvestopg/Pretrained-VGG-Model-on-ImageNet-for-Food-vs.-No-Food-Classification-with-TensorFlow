
---

# Food vs. Non-Food Image Classification using VGG

This repository contains a Convolutional Neural Network (CNN) model trained to classify images into two categories: Food and Non-Food, using the VGG16 architecture as the feature extractor. The model was trained on a subset of the Food vs. Non-Food dataset, consisting of 3000 training images and 1000 testing images.

## Dataset
The original dataset used in this project can be found on IEEE DataPort. The dataset comprises a variety of food and non-food images, which can be used for image classification tasks.

## Data Preprocessing
The image data was preprocessed using the `preprocess_input` function. This preprocessing step is crucial to ensure that the images are in the correct format for compatibility with the VGG16 model. The `preprocess_input` function adjusts the image data to match the preprocessing applied to the ImageNet dataset, which the VGG16 model was originally trained on. This includes mean subtraction and scaling to bring the images to a format compatible with the pre-trained model.

## Model Architecture
The VGG16 model was used as the base architecture for feature extraction, and the top classification layers were customized for the Food vs. Non-Food classification task. The model's top layers include a Flatten layer and a Dense layer with softmax activation, resulting in two output classes.

## Training
The VGG16 model's pre-trained weights on the ImageNet dataset were used as a starting point. These pre-trained weights contain valuable feature representations that help the model perform well on various image classification tasks, including Food vs. Non-Food. By using the ImageNet weights, the model already possesses a good understanding of general visual features, allowing it to focus on learning the specific distinctions between food and non-food classes during fine-tuning. The model's layers were frozen to retain these weights.

The model was trained extremely quickly, as evidenced by the accuracy history plot. In just one epoch, the model reached an impressive accuracy of 98%. This rapid convergence can be attributed to the use of pre-trained weights from ImageNet, highlighting the value of leveraging these weights in transfer learning.


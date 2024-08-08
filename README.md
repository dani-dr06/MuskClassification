# Musk or Not

## Project Overview
The goal of this project is to experiment with TensorFlow and combine different neural network models to solve a task. I decided that I would combine an Autoencoder for dimensionality reduction and then use the encoded features in an ANN for the purposes of classification.

AutoEncoders are a type of neural network which are trained to learn to copy the input to the output. It consists of an encoder which encodes or breaks down the input into lower dimension representation, and then has an encoder which decodes the lower dimension representation back to its input. From being used for dimensionality reduction and recommendation systems to denoising images and image colorization, Autoencoders have many interesting applications. 

***Rationale behind this decision***:
Dimensionality reduction is important as not only does it reduce computational requirements, but it also can help prevent overfitting and ultimately result in a better performance, as dimensionality reduction aims to extract only the meaningful features from the data.

## Data
The dataset was obtained from the UCI Machine Learning Repository and contains information about a set of molecules. This dataset is geared towards a binary classification task, with the goal of predicting whether a molecule is a musk or not. The data is made up of 166 features containing distance and spatial information.

## Results and Conclusion
I was able to successfully combine an autoencoder along with the ANN, achieving an accuracy of around 92% on the validation data while reducing the number of features to just 16 from the original 166 dimensions.
This project was a good exercise on training neural networks using TensorFlow and specifically on getting more familiar with autoencoders and their usefulness when it comes to dimensionality reduction.

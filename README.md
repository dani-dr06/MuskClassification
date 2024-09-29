# Musk or Not

## Project Overview
The goal of this project is to experiment with TensorFlow and combine different neural network models to solve a task. I decided that I would combine an Autoencoder for dimensionality reduction and then use the encoded features in an ANN for the purposes of classification.

AutoEncoders are a type of neural network which are trained to learn to copy the input to the output. It consists of an encoder which encodes or breaks down the input into lower dimension representation, and then has an encoder which decodes the lower dimension representation back to its input. From being used for dimensionality reduction and recommendation systems to denoising images and image colorization, Autoencoders have many interesting applications. 

***Rationale behind this decision***:
Dimensionality reduction is important as not only does it reduce computational requirements, but it also can help prevent overfitting and ultimately result in a better performance, as dimensionality reduction aims to extract only the meaningful features from the data.

## Data
The dataset used in this project is sourced from the [UCI Machine Learning Repository](https://archive.ics.uci.edu/dataset/75/musk+version+2). It contains information about molecules, with the goal of predicting whether a molecule is a musk or non-musk. The dataset has the following characteristics:

- **Features**: 166 features related to the molecular structure.
- **Target**: A binary variable indicating whether the molecule is a musk (1) or non-musk (0).

## Project Structure

1. **Data Preprocessing**:
   - Checked the dataset for missing values and ensured that all features are numerical.
   - Standardized the features to prepare them for neural network input.

2. **Autoencoder**:
   - Designed an Autoencoder to reduce the dimensionality of the feature space.
   - The encoder compresses the input features, and the decoder reconstructs the original input from the compressed representation.
   - Trained the Autoencoder on the dataset to learn a lower-dimensional representation of the data.

3. **ANN Classifier**:
   - Built an Artificial Neural Network (ANN) using the compressed features generated by the Autoencoder.
   - The ANN is a binary classifier designed to predict whether a molecule is a musk or non-musk.

4. **Model Training and Evaluation**:
   - Trained both the Autoencoder and the ANN on the dataset.
   - Evaluated the performance of the classifier using accuracy and loss metrics.
   - Visualized the training process and final results using various plots.


## Results and Conclusion
I was able to successfully combine an autoencoder along with the ANN, achieving an accuracy of around 92% on the validation data while reducing the number of features to just 16 from the original 166 dimensions. The combination of an Autoencoder for dimensionality reduction and an ANN for classification proved to be effective in this project. This approach not only allowed for high performance of the classifier but also made the model more computationally efficient. This project demonstrates the potential of using dimensionality reduction techniques in conjunction with deep learning models for complex classification tasks, and it was a good exercise on training neural networks using TensorFlow and specifically on getting more familiar with autoencoders and their usefulness when it comes to dimensionality reduction.

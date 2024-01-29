# Normal Nails vs Terry's Nails Classification using Simple CNN and MobileNet Transfer Learning

## Introduction
This notebook focuses on classifying images of nails into two categories: normal nails and Terry's nails. Terry's nails are characterized by a whitish or grayish appearance with dark red or brown lines at the tips. The condition is associated with various serious health issues such as liver, kidney, heart problems, and diabetes. The classification is performed using two different models: a Simple Convolutional Neural Network (CNN) and MobileNet Transfer Learning.

## Setup
The notebook begins by installing necessary packages, including TensorFlow, OpenCV, and Matplotlib. It then mounts Google Drive to access the dataset, which is organized into two classes: normal and Terry's nails.

## Data Preprocessing
The dataset is loaded using TensorFlow's `image_dataset_from_directory` function. The images are preprocessed by scaling the pixel values to the range [0,1]. The dataset is split into training, validation, and test sets.

## Simple CNN
### Model Architecture
The Simple CNN model consists of three convolutional blocks, each followed by a max-pooling layer. The final layers include a flattened layer, a dense layer with 256 neurons and ReLU activation, a dropout layer for regularization, and a final dense layer with a sigmoid activation function.

### Training
The model is compiled with the Adam optimizer, binary cross-entropy loss, and accuracy as the evaluation metric. The training process is visualized using loss and accuracy plots.

### Evaluation
The model is evaluated on the test set, and precision, recall, and accuracy metrics are calculated.

### Testing
The model is tested on new images to demonstrate its predictions.

## MobileNet Transfer Learning
### Model Architecture
MobileNet, a pre-trained model, is utilized as a base. Additional layers, including a convolutional layer, max-pooling, global average pooling, dropout, and a final dense layer with sigmoid activation, are added for classification.

### Training
The MobileNet-based model is compiled with the Adam optimizer, binary cross-entropy loss, and accuracy as the evaluation metric. The training process is visualized using loss and accuracy plots.

### Evaluation
The model is evaluated on the test set, and precision, recall, and accuracy metrics are calculated.

### Testing
The model is tested on new images to demonstrate its predictions.

## Model Comparison
Both models' predictions are visually compared using a grid layout. Confusion matrices are presented to analyze the classification results. Sensitivity and specificity metrics are calculated to evaluate the models' performance.

## Conclusion
The notebook concludes with a summary of the models' performance, strengths, and areas for improvement. Further enhancements and evaluations are suggested for achieving more accurate and reliable results.

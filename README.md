# Forest Fire Classification using Logistic Regression
This project focuses on binary classification of forest landscape images to detect fire and non-fire instances. The classification is performed using logistic regression.

## Implementation Steps
a) **Pre-processing**
Image Resizing: The images in the dataset may have different sizes. Use the OpenCV library to resize the images, ensuring they have consistent dimensions for further processing.
Image Normalization: Normalize the pixel values of the images to a common range, such as scaling them between 0 and 1. This step ensures consistent data representation across all images.
Target Assignment: Determine the target label (Fire or No-Fire) for each image based on the provided dataset labels. Associate the image file name or metadata with the corresponding target class.

b) **Splitting the Data**
Train-Test Split: Divide the pre-processed dataset into a training set and a test set. The recommended split ratio is typically 80:20 or 70:30, ensuring a representative distribution of both classes in each set.

c) **Logistic Regression**
Model Training: Apply logistic regression to the training set using a suitable library or implementation, such as scikit-learn. Train the logistic regression model on the training data to learn the relationships between the image features and the target labels.

d) **Evaluation**
Model Testing: Apply the trained logistic regression model to the test set to predict the labels.
Accuracy and Confusion Matrix: Evaluate the accuracy of the model by comparing the predicted labels with the true labels of the test set. Compute a confusion matrix to assess the classification performance, indicating the number of correctly and incorrectly classified instances for each class.

e) **Finding the Best Probability Threshold**
Probability Threshold Selection: Extract the probabilities predicted by the logistic regression model for the training set.
Threshold Optimization: Iterate through different probability thresholds and select the threshold that maximizes a chosen evaluation metric, such as accuracy or F1-score, on the training data.
Evaluation with Best Threshold: Report the accuracy and confusion matrix using the best probability threshold on the training data.

f) **Saving the Best Model and Prediction**
Model Persistence: Save the logistic regression model with the best probability threshold for future use.
Importing and Prediction: Import the saved model into another file, such as classifier.py, for inference purposes.
Image Downloads: Download new forest images (fire and non-fire) for prediction.
Model Inference: Feed the downloaded images to the classifier and make predictions using the loaded model.
Displaying Results: Show the label and probability of each image, highlighting fire instances in red and non-fire instances in green.

## Dependencies
The project requires the following dependencies: OpenCV, scikit-learn, and any other relevant libraries for image processing and logistic regression.

## Contributing
If you would like to contribute to this project, please follow the standard guidelines for contributions, such as opening an issue for bug fixes or feature requests and creating a pull request for proposed changes.

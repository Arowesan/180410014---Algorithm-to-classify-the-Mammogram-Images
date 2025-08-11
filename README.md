Algorithm Used
Import Required Libraries

Loaded Python libraries for image processing (os, cv2, numpy), visualisation (matplotlib), and machine learning (tensorflow, keras).

Set Dataset Path

Defined the dataset directory containing the subfolders: benign, malignant, and normal.

Load and Preprocess Images

Iterated through each category folder.

Read each image using OpenCV (cv2.imread).

Resized all images to a fixed dimension for consistency.

Normalised pixel values to the range [0, 1] for faster training.

Label the Data

Assigned a numeric label to each category:

Benign → 0

Malignant → 1

Normal → 2

Split Data into Training and Testing Sets

Used train_test_split to separate images into training and testing datasets.

Build Convolutional Neural Network (CNN) Model (if training was done)

Created a sequential CNN architecture with convolution, pooling, and dense layers.

Added a softmax output layer for classification into three categories.

Compile the Model

Used adam optimizer and categorical_crossentropy loss function.

Tracked performance using accuracy metrics.

Train the Model (optional if pre-trained model not used)

Trained the CNN for a set number of epochs (full passes through the dataset).

Used the training set for learning and validation set for performance monitoring.

Evaluate the Model

Tested the model on unseen images from the test set.

Calculated accuracy and loss.

Predict New Images

Loaded a new image, preprocessed it (resize, normalize), and used the model to predict the category.

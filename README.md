# Image_Classification

This is a deep learning model that helps to classify the human images in "happy" and "sad" categories based on their facial expressions.

## Requirements :

```
Tensorflow
OpenCV-python
Numpy
Matplotlib
Jupyternotebook

```

## Getting started

- Acquiring the data from kaggle ["Dataset"](https://www.kaggle.com/datasets/sanidhyak/human-face-emotions).
- Installing the dependencies.
- Preprocess the data to ensure data quality and enhance model performance.
- Scaling the data to ensure fair contribution of features and improves algorithm performance.
- Split the data for training(70%), validation(20%) and testing(10%).
- Build a deep learning model and compile it </br> ``` In this project it is Sequential(). ```
- Train the model.
- Plot the model performance to ensure the model does not overfit or underfit. </br>

- If the model overfit or underfit,

use Droupout() dropout randomly disables a fraction of neurons during training
```
from tensorflow.keras.layers import Dropout

model.add(Flatten())
model.add(Dense(256, activation='relu'))
model.add(Dropout(0.5))  # Drop 50% of the neurons
model.add(Dense(1, activation='sigmoid'))

```

Use data augmentation to increases the diversity of your training data without collecting more images.
```
from tensorflow.keras.preprocessing.image import ImageDataGenerator

datagen = ImageDataGenerator(
    rotation_range=15,
    width_shift_range=0.1,
    height_shift_range=0.1,
    horizontal_flip=True,
    zoom_range=0.1,
)

```

Add Regularization (L2) to discourage complexity.
```
from tensorflow.keras.regularizers import l2

model.add(Dense(256, activation='relu', kernel_regularizer=l2(0.001)))

```

IF ANY OF THE STEPS DOES NOT WORK, THEN CHANGE THE DATASET.

- Evaluate the model.
- Test the model using any image.


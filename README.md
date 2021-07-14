# Brain-Tumor-Detection
## Overview
Building a detection model using a Convolutional Neural Network in Tensorflow &amp; Keras. Used a brain MRI images dataset founded on Kaggle.

#### **About the data:**
The dataset contains 2 folders: The folder **yes** contains **155** Brain MRI Images that are tumorous and the folder **no** contains **98** Brain MRI Images that are non-tumorous.

---
## Data Augmentation
There wasn't enough examples to train the neural network. Also, data augmentation was useful in taclking the data imbalance issue in the data.

Before data augmentation, the dataset consisted of:
155 positive and 98 negative examples, resulting in 253 example images.

After data augmentation, now the dataset consists of:
1085 positive and 980 examples, resulting in 2065 example images.

Note: these 2065 examples contains also the 253 original images. They are found in folder named **'augmented data'**.

---
## Data Preprocessing
For every image, the following preprocessing steps were applied:

1. Crop the part of the image that contains only the brain.
2. Resize the image to have a shape of (240, 240, 3). So, all images should have the same shape to feed it as an input to the neural network.
3. Apply normalization

---
## Data Splitting
* 70% of the data for training.
* 15% of the data for validation.
* 15% of the data for testing.

---
## Conclusion:
Now, the model detects brain tumor with:

* 83.6% accuracy on the test set.

* 85.87% f1 score on the test set.


### **Dataset:** https://www.kaggle.com/navoneel/brain-mri-images-for-brain-tumor-detection
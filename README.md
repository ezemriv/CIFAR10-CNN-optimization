<img src="https://img.shields.io/badge/Python-white?logo=Python" style="height: 25px; width: auto;"> <img src="https://img.shields.io/badge/NumPy-white?logo=numpy&logoColor=013243" style="height: 25px; width: auto;"> <img src="https://img.shields.io/badge/TensorFlow-white?logo=TensorFlow" style="height: 25px; width: auto;"> <img src="https://img.shields.io/badge/Keras-white?logo=Keras&logoColor=D00000" style="height: 25px; width: auto;">

# CIFAR10 image classification CNN optimization

In this project, I aim to systematically optimize a neural network classifier for this dataset, exploring both architectural modifications and the benefits of transfer learning.

## The CIFAR-10 dataset:

The CIFAR-10 dataset consists of 60000 32x32 colour images in 10 classes, with 6000 images per class. There are 50000 training images and 10000 test images.The CIFAR-10 dataset

<img src="https://miro.medium.com/max/709/1*LyV7_xga4jUHdx4_jHk1PQ.png" width="400" height="300" alt="cifar10">

Initially, I focused on refining the model architecture itself. I`ve created the CIFAR10ModelTester class to streamline the evaluation process.

The goal in this phase is to determine the highest achievable test accuracy through iterative improvements to the architecture and hyperparameter tuning alone.

- Dropout & Normalization: Added dropout layers for regularization, batch normalization for stability.
- Increased Complexity: Gradually added convolutional layers, experimented with filter sizes.
- Callbacks: Implemented early stopping, model checkpointing, and learning rate scheduling.
- Hyperparameter Tuning: Tested batch sizes, optimized learning rate, weight decay.
- Regularization: Applied weight decay, utilized learning rate schedules.
- Global Average Pooling: Replaced fully connected layers to reduce overfitting.

#### **Best test accuracy (arch and hyperparam tunning)**
***0.894 (Model 7).***

In the end, I explored the potential of transfer learning.

I experimented with **Xception and EfficientNetB2** from Keras, as well as **ResNet34** from FastAI.

By fine-tuning these models on the CIFAR-10 dataset, I further boosted classification accuracy.

#### **Best final test accuracy:**
***0.9706 using ResNet34.***

<img src="https://ezemriv.github.io/images/cifar_preds.png" width="600" height="600" alt="cifar10_preds">



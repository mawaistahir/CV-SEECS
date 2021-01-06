## Image Classification using VGG16 CNN
This repository contains codes to train VGG16 based CNN deep neural network on intel-image classification dataset consisting of 25k 150x150 RGB images of natural scenes belong to 6 different classes. Dataset is divided in to 3 categories i.e. 14k training images, 3k validation images and 8k test images. Network is built by using primitive layers of keras framework. Input size of the network is kept 150x150 in accordance with the provided dataset. 16 layers having trainable weights are added including 2D convolutions, max pooling and fully connected layers. Total trainable parameters are above 50M.


I have trained the network six times in total, starting with the training of base network without experimenting with any hyper parameter. Keeping it as a reference performance I then trained the network second time. This time I subjected the rescaled/normalized training images to the network for quick convergence of training. Keeping in view of its results I then opted for early stopping in combination with adaptive learning for the purpose of training the network third time. Fourth time I experimented with data augmentation. After getting significantly better results I then decided for transfer learning by using the trained weights of fourth network. I initialized the fifth network with weights of pre-trained fourth network. Only last 3 layers of fifth network were kept trainable and rest were frozen. In the last I once again experimented with transfer learning by using the weights of pre-trained fourth network but this time I kept all the layers trainable.

[1. Training of VGG16 base model on Intel-Image-Classification dataset](https://github.com/mawaistahir/CV-SEECS/blob/main/VGG16%20Training%20on%20Intel-Image-Classification%20Dataset.ipynb)

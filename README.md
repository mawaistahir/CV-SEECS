## Image Classification using VGG16 CNN
This repository contains codes to train VGG16 based CNN deep neural network on intel-image classification dataset consisting of 25k 150x150 RGB images of natural scenes belong to 6 different classes. Dataset is divided in to 3 categories i.e. 14k training images, 3k validation images and 8k test images. Network is built by using primitive layers of keras framework. Input size of the network is kept 150x150 in accordance with the provided dataset. 16 layers having trainable weights are added including 2D convolutions, max pooling and fully connected layers. Total trainable parameters are above 50M.


I have trained the network six times in total, starting with the training of base network without experimenting with any hyper parameter. 

[1. Training of VGG16 base model on Intel-Image-Classification dataset](https://github.com/mawaistahir/CV-SEECS/blob/main/VGG16%20Training%20on%20Intel-Image-Classification%20Dataset.ipynb).

Keeping its performance as a reference I then trained the network second time. This time I rescaled/normalized the training images before putting them to the network for training purpose. It resulted in quick convergence of training.

[2. Training of VGG16 with rescaled/normalized Intel-Image-Classification dataset](https://github.com/mawaistahir/CV-SEECS/blob/main/VGG16%20Training%20with%20Rescaled%20Intel-Image-Classification%20Dataset.ipynb).

Both of the above trained networks were overfitted. I then opted for early stopping in combination with adaptive learning rate. 

[3. Training of VGG16 with Early Stopping and Adaptive Learning Rate](https://github.com/mawaistahir/CV-SEECS/blob/main/VGG16%20Training%20with%20Early%20Stopping%20and%20Adaptive%20Learning%20Rate.ipynb).

Fourth time I experimented with data augmentation. It gave me significantly better results.

[4. Training of VGG16 using Data Augmentation](https://github.com/mawaistahir/CV-SEECS/blob/main/VGG16%20Training%20with%20Data%20Augmentation.ipynb).

I then decided for transfer learning. I initialized the fifth network with the weights of pre-trained fourth network (trained with data augmentation). Only last 4 layers of fifth network were kept trainable and rest were frozen. 

[5. Training of VGG16 using Transfer Learning](https://github.com/mawaistahir/CV-SEECS/blob/main/VGG16%20Training%20with%20Transfer%20Learning.ipynb).

I once again experimented with transfer learning. This time I kept all the layers trainable.

[6. Training of VGG16 using Transfer Learning 2](https://github.com/mawaistahir/CV-SEECS/blob/main/VGG16%20Training%20with%20Transfer%20Learning%202.ipynb).



Here is the link to download the pre-trained networks weights of training # 4
https://drive.google.com/file/d/1A0Whi0FVDdjVvj0DhqHhQiteFQfc3tsp/view?usp=sharing



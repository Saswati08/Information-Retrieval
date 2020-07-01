# Triplet-Networks-with-GANs
This repository is the implementation of the paper "Training Triplet Networks with GANs"(https://arxiv.org/pdf/1704.02227.pdf)
The implemented architecture is an amalgation of GANs and triplet networks and can be trained using train function in pipeline.ipynb. 
Pre training can be done by commenting out the loss_triplet in trainD function to stop taking supervised loss into account.
You dont need to download any data for running this file. Mnist dataset is dowmloaded in functions MnistLabel(), MnistUnlabel() and MnistTest()

#Libraries and Dependencies used
pytorch
itertools
sklearn
os

# About
Triplet networks are widely used models that are characterized by good performance in classification and retrieval tasks. In the paper the authors proposed to train a
triplet network by putting it as the discriminator in Generative Adversarial Nets(GANs). Using above mentioned architecture we can get an accuracy of 94% in 100 epochs
using only 100 labelled samples of MNIST data.

# Results

**For m(output dimension) = 32 and n(number of labelled samples used) = 100**
![](/images/pretraining_loss.png)

Loss during training 
![](/images/training_loss.png)

Unsupervised Loss         |  Triplet Loss
:-------------------------:|:-------------------------:
![](/images/unsupervised.png) | ![](/images/triplet_loss.png)

**Generated Images**
![](/images/generated_img1.png)  ![](/images/generated_img2.png)

**Accuracy = 94% and mAP = 0.86**


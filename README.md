# All_ResNet_Implementations

Implementation of Resnet18, Resnet34 and Resnet50 as per the original paper (in Tensorflow)

In this [jupyter notebook](https://github.com/archit-lahiri/All_ResNet_Implementations/blob/main/ResNet.ipynb) file I implement the Resnet architectures as they were proposed in the paper:

[He et al., 2015. Deep residual networks for image recognition](https://arxiv.org/pdf/1512.03385.pdf)

The proposed models in the paper were created to fascilitate the training and use of very deep neural networks as the norm is that the deeper the neural net is, the more accurate it is as it is able to learn more complicated mathematical functions.

To solve the issues of degradation that often used to plague deep convolutional neural networks, the authors came up with the Residual Block. In this, there are skip connections which directly feeds the output of one layer to another layer which is deeper in the network- hence skipping some layers, like a shortcut. The residual function is the difference between the expected output and the input to a particular layer. It allows the network to focus on learning incremental changes (residuals) instead of attempting to learn the entire mapping from scratch, the training process becomes more manageable and convergence is improved.The residual function can easily learn the identiy mapping or get close. This means for backpropogation, lower layers are more easily influenced by changes in the deeper layers. This solves to a great degree the issue of degradation.

In this implementation I will replicate the model architecture and train a dataset and observe train and validation loss and accuracy. The original paper tested their models on datasets such as ImageNet and CIFAR-10. I instead use the [Coffee Beans dataset](https://www.kaggle.com/datasets/gpiosenka/coffee-bean-dataset-resized-224-x-224) for simplicity. It consists of 4 classes: Dark, Green, Light and Medium. The dataset is already divided into train (consisting of 1200 images: 300 per class) and test (consisting of 400 images: 100 per class).

In this [notebook](https://github.com/archit-lahiri/All_ResNet_Implementations/blob/main/ResNet.ipynb) I achieve a train and validation accuracy of over 90%. 


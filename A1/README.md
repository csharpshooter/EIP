EIP Phase 1 Assignment 1

Contributors:
Abhijit Mali

Model Evaluation Output :
print(score)
[0.060999790370383014, 0.9907]

Convolution - Convolution is like a correlation. We are doing a dot product between the image and the kernel.

Filters/Kernels - They are feature extractors. Most widely used kernel is 3 x 3 matrix kernel. The output of a kernel is a feature map. Number of kernels used is the number of channels made in output.

Epochs - 1 epoch is when we have covered our dataset once. A epoch can also be very large. So to cover a epoch we can use batch size. With smaller batches we can cover a large epoch. For ex: for epoch of 500 images batch size can be 50 images in a batch. So epoch will have 10 batches.

1x1 Convolution - It is a type of feature extractor. It combines features contextually linked with each other. For ex. like left eye with right eye.

3x3 Convolution - It is also a type of feature extractor. We use it to extarct edges and gradients.

Feature Maps - Feature map is collection of all features. The output of a kernel is a feature map.

Activation Function - While initialising a convolution mode we can set the activation. In the assignment we have used 'relu' activation.
We have also used 'softmax' activation function in our model

Receptive Field - There a 2 types of receptive fields. 
Local Receptive field 
Global Receptive field

1. Local receptive field - It is the image data of the image which is seen by the kernel for a pixel on which convolution is being done. For a kernel of 3 x 3 the local receptive field will be 3 x 3.

2. Global receptive field - It is the image data on which convolution is being done by the kernel which contains convolution data of all pixels. Ideally the global receptive field of last layer should be as same as size of image i.e. last layer should have data for all pixels of the image.

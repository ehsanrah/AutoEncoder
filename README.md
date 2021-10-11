An autoencoder can be used to filter noise (denoise) from data samples.
In this repository a denoising autoencoder is implemented. The architecture of
a denoising autoencoder is no different than that of a regular autoencoder. In fact, the only
difference between a normal autoencoder and a denoising autoencoder is the training data.
To see an implementation of autoencoders refer to the following repository where both fully-connected 
and convolutional autoencoders are implemented:

https://github.com/ehsanrah/AutoEncoder

A denoising autoencoder is trained to filter noise from the input and produce a denoised version
of the input as the reconstructed output. This is achieved during training by using the noisy
sample as the input and the original noise-free sample as the target reconstruction. Here,
a denoising autoencoder is implemented to filter Gaussian noise injected
into the MNIST dataset of handwritten digits. The noisy data is created by generating 784 values, 
per sample, from a zero mean unit variance Gaussian distribution, scaling them by 0.25 (to make the
additional noise more intense), and adding them to each point in the original image. Each image is 
then clipped to stay in the valid pixel range. The autoencoder will then be trained to eliminate this
added noise.
Here architecture of the autoencoder is a fully connected but it can be applied exactly the same to 
convolutional autoencoder . 

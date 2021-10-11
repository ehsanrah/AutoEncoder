An autoencoder is simply a neural network which is trained to reproduce an approximation of
its input at its output. Typically, the input is mapped to a reduced dimension representation in
the hidden layer, referred to as the "bottleneck" layer, and then the "bottleneck" layer representation
is used to calculate the reconstruction of the input sample. The encoder of the autoencoder
is the portion of the neural network that maps the input to the hidden layer representation,
and the decoder maps the hidden layer representation to an approximate reconstruction
of the input at the output. Initially,an autoencoder may not seem useful since the objective is 
to obtain an input reconstruction, which will be slightly different than the input. However, once
an autoencoder is trained, its bottleneck layer is of more interest than its reconstruction. Of
course, during training, the reconstruction should have a minimum error w.r.t. the input, but, by
training a neural network in this way, the bottleneck layer is forced to learn a reduced dimensional
 representation of the input. In other words, a trained autoencdoer can be used for dimensionality 
reduction. Using an autoencoder for dimensionality reduction is much different than other methods (such as
PCA) because the network is learning a non-linear mapping (due to the activation functions)
of the input to a reduced dimensional space. The new representation may capture aspects of
the input that linear dimensionality reduction algorithmsmay fail to represent. 

So in this repository an autoencoder with two architecture (fully connected and convolutional neural network)
is implemented to encode the fashion_MNIST handwritten digits in bottleneck layer. 
Also in every architecture two loss function (Binary_Crossentropy and Mean_Squared_Error) are examined to find the 
best one and it turned out that MSE is the better choice. 

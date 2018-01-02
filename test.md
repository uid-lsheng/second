Q1. Which of the following do you typically see as you move to deeper layers in a ConvNet? 

 - nH and nW increases, while nC also increases
 - **nH and nW decrease, while nC increases**
 - nH and nW decreases, while nC also decreases
 - nH and nW increases, while nC decreases

> That's what the "deep" means

Q2. Which of the following do you typically see in a ConvNet? (Check all that apply.)

- **Multiple CONV layers followed by a POOL layer**
- Multiple POOL layers followed by a CONV layer
- **FC layers in the last few layers**
- FC layers in the first few layers

Q3. In order to be able to build very deep networks, we usually only use pooling layers to downsize the height/width of the activation volumes while convolutions are used with “valid” padding. Otherwise, we would downsize the input of the model too quickly.
**False**
> Convolutions can also be used for downsizing

Q4. Training a deeper network (for example, adding additional layers to the network) allows the network to fit more complex functions and thus almost always results in lower training error. For this question, assume we’re referring to “plain” networks.
**False**
> Plain deep network does not always reduce training error, that's why we need ResNet

Q5. The following equation captures the computation in a ResNet block. What goes into the two blanks above?
a[l+2]=g(W[l+2]g(W[l+1]a[l]+b[l+1])+bl+2+_______ )+_______

- 0 and a[l], respectively
- z[l] and a[l], respectively
- 0 and z[l+1], respectively
- **a[l] and 0, respectively**

Q6. Which ones of the following statements on Residual Networks are true? (Check all that apply.)

- The skip-connections compute a complex non-linear function of the input to pass to a deeper layer in the network.
- **The skip-connection makes it easy for the network to learn an identity mapping between the input and the output within the ResNet block.**
- A ResNet with L layers would have on the order of L^2 skip connections in total.
- **Using a skip-connection helps the gradient to backpropagate and thus helps you to train deeper networks**

> Should be linear, of order L-1?

Q7. Suppose you have an input volume of dimension 64x64x16. How many parameters would a single 1x1 convolutional filter have (including the bias)?

- **17** 
- 2
- 4097
- 1

> Number of channels + 1 = 17

Q8. Suppose you have an input volume of dimension nH x nW x nC. Which of the following statements you agree with? (Assume that “1x1 convolutional layer” below always uses a stride of 1 and no padding.)

- **You can use a pooling layer to reduce nH, nW, but not nC.**
- You can use a 1x1 convolutional layer to reduce nH, nW, and nC.
- You can use a pooling layer to reduce nH, nW, and nC.
- **You can use a 1x1 convolutional layer to reduce nC but not nH, nW.**

Q9. Which ones of the following statements on Inception Networks are true? (Check all that apply.)

- **Inception blocks usually use 1x1 convolutions to reduce the input data volume’s size before applying 3x3 and 5x5 convolutions.**
- Inception networks incorporates a variety of network architectures (similar to dropout, which randomly chooses a network architecture on each step) and thus has a similar regularizing effect as dropout.
- Making an inception network deeper (by stacking more inception blocks together) should not hurt training set performance.
- **A single inception block allows the network to use a combination of 1x1, 3x3, 5x5 convolutions and pooling.**

> This answer is correct, although I don't know why the other two should not be selected

Q10. Which of the following are common reasons for using open-source implementations of ConvNets (both the model and/or weights)? Check all that apply.

- A model trained for one computer vision task can usually be used to perform data augmentation even for a different computer vision task.
- **Parameters trained for one computer vision task are often useful as pretraining for other computer vision tasks.**
- The same techniques for winning computer vision competitions, such as using multiple crops at test time, are widely used in practical deployments (or production system deployments) of ConvNets.
- **It is a convenient way to get working an implementation of a complex ConvNet architecture.**
## Week 2 Quiz - Deep Convolutional Models

1. Which of the following do you typically see in a ConvNet? (Check all that apply.)
   
    - [x] Multiple CONV layers followed by a POOL layer
    - [ ] Multiple POOL layers followed by a CONV layer
    - [x] FC layers in the last few layers 
    - [ ] FC layers in the first few layers

2. In order to be able to build very deep networks, we usually only use pooling layers to downsize the height/width of the activation volumes while convolutions are used with “valid” padding. Otherwise, we would downsize the input of the model too quickly.

    - [ ] True
    - [x] False

3. Training a deeper network (for example, adding additional layers to the network) allows the network to fit more complex functions and thus almost always results in lower training error. For this question, assume we’re referring to “plain” networks. 

    - [ ] True
    - [x] False

4. The following equation captures the computation in a ResNet block. What goes into the two blanks above? 
a^{[l+2]}=g(W^{[l+2]}g(W^{[l+1]}a^{[l]}+b^{[l+1]})+b^{[l]}+2+_______ )+_______
    
    - a^{[l]} and 0, respectively

5. Which ones of the following statements on Residual Networks are true? (Check all that apply.)
    
    - [ ] A ResNet with L layers would have on the order of L^{2} skip connections in total. 
    - [ ] The skip-connections compute a complex non-linear function of the input to pass to a deeper layer in the network.
    - [x] Using a skip-connection helps the gradient to backpropagate and thus helps you to train deeper networks
    - [x] The skip-connection makes it easy for the network to learn an identity mapping between the input and the output within the ResNet block. 

6. Suppose you have an input volume of dimension n_{H} x n_{W} x n_{C}. Which of the following statements you agree with? (Assume that “1x1 convolutional layer” below always uses a stride of 1 and no padding.) 

    - [x] You can use a 2D pooling layer to reduce n_{H}, n_{W}, but not n_{C}.
    - [ ] You can use a 1x1 convolutional layer to reduce n_{H}, n_{W}, and n_{C}.
    - [x] You can use a 1x1 convolutional layer to reduce n_{C} but not n_{H}, n_{W}.
    - [ ] You can use a 2D pooling layer to reduce n_{H}, n_{W}, and n_{C}.  
        
7. Which ones of the following statements on Inception Networks are true? (Check all that apply.)
	
    - [x] Inception blocks usually use 1x1 convolutions to reduce the input data volume’s size before applying 3x3 and 5x5 convolutions.
    - [ ] Inception networks incorporate a variety of network architectures (similar to dropout, which randomly chooses a network architecture on each step) and thus has a similar regularizing effect as dropout. 
    - [ ] Making an inception network deeper (by stacking more inception blocks together) might not hurt training set performance.
    - [x] A single inception block allows the network to use a combination of 1x1, 3x3, 5x5 convolutions and pooling. 

8. Which of the following are common reasons for using open-source implementations of ConvNets (both the model and/or weights)? Check all that apply. 

    - [ ] A model trained for one computer vision task can usually be used to perform data augmentation even for a different computer vision task. 
    - [ ] The same techniques for winning computer vision competitions, such as using multiple crops at test time, are widely used in practical deployments (or production system deployments) of ConvNets.
    - [x] It is a convenient way to get working with an implementation of a complex ConvNet architecture. 
    - [x] Parameters trained for one computer vision task are often useful as pretraining for other computer vision tasks. 

9.  In Depthwise Separable Convolution you:

	  - [x] You convolve the input image with n_{c} number of n_{f} x n_{f} filters (n_{c} is the number of color channels of the input image).
	  - [ ] The final output is of the dimension n_{out} x n_{out} x n_{c} (where n_{c} is the number of color channels of the input image).
	  - [x] The final output is of the dimension n_{out} x n_{out} x n^{'}_{c} (where n^{'}_{c}) is the number of filters used in the previous convolution step).
	  - [ ] For the “Depthwise” computations each filter convolves with all of the color channels of the input image.
	  - [ ] You convolve the input image with a filter of n_{f} x n_{f} x n_{c} where n_{c} acts as the depth of the filter (n_{c} is the number of color channels of the input image).
	  - [x] For the “Depthwise” computations each filter convolves with only one corresponding color channel of the input image.
	  - [ ] Perform one step of convolution.
	  - [x] Perform two steps of convolution.

10. Fill in the missing dimensions shown in the image below (marked W, Y, Z).
    ![mobilenet](images/mobilenet%20v2.png)
    - W = 5, Y = 30, Z = 20
# ADL22

## 1. Introduction

- What is your MSE/MAE with linereg vs tuned network?

  MSE/MAE of my tuned network reduced from 24.29 to 17.90, respectively, after changing the number of neurons from 30 to 25.
  

- What happens to your train and test results if you add 5 hidden layers with 128 neurons each?

  What happens to the train and test results when you add 5 hidden layers with 128 neurons each is the performance is better and results are better and the model starts to overfit.
  

## 2. Intro to Convolution Operations: Padding

- What is a response layer? (Give a brief, 1-sentence description)

  A response layer is the result of doing convolution where the result is the number of filters and each filter is in a resulting size stacked on top of each other.
  

- Given the filter space of (26,26,32), what does each number represent?

  Given the filter space of (26,26,32), the 32 represents 32 filters and the (26,26) is the size of the filters.
  

- Given 6x6 input and filter of (3,3): what is the response shape that we get?

  Given 6x6 input and filter of (3,3) the response shape that we get is (4,4).
  

- Given (33,33,1) input and filter of (2,2): what is the respose shape that we get?

  Given (33,33,1) input and filter of (2,2) the response shape that we get is (30,30).
  

- What is the difference between 'valid' and 'same' padding? Given 6x6 input and filter of (3,3), what are the response shapes for both options?

  The difference between 'valid' and 'same' padding is 'valid' padding is the default meaning padding is disabled, where as 'same' padding is automatic padding so that the output size is equal to the input size. Given 6x6 input and filter of (3x3) the response shape for 'valid' is (4,4) and for 'same' it is (5,5).


## 3. Convolution Parameters: Stride and Pooling

- What is max pooling? (Give a brief, 1-sentence description)

  Max pooling is an aggressive downsampling where the window is extracted and the output is the max of that window.

- If I apply pooling of 2 (2,2 window with a stride of 2) to a (6,6) array, what is the resulting size?

  If a pooling of 2 is applied to a (6,6) array the resulting size is (3,3).

## 4. ConvNet Architectures, Layers

- Define I, O, F, S, P as used in this lecture (Give a brief, 1-sentence description)

  I = Input Volume
  F = Filter, Kernal size
  S = Stride
  P = Zero-Padding
  O = Output Neural Count, O = (I - F + 2P)/S +1

- What is my output size if Input = (100,100), kernel size=(2,2), the stride of 1, and no pooling?

  The output size if input = (100,100), kernal size = (2,2), the stride of 1 and no pooling is (99,99).

- How many weights do I have if I have 24 such filters stacked (conv2_24)?

 96 weights 

- Solve for the padding (P), in terms of I, F, and S, if we want the input and output size to remain the same.

  P = ((S - 1) * I - S + F) / 2


## 5. Practical Patterns

- What can we use the ImageDataGenerator for? What can it help us fight? (Give a brief, 1-sentence description)

  We can use the ImageDataGenerator for randomly rotating, shifting, flipping, zomming, etc. on images. It does not add new information, but gives a nice remix so it might help fight overfitting.

- What is a better idea: TO use one large kernel (8,8) or multiple stacked smaller ones, 4x(2,2)? Why? Show the number of weights for each option.

  It is better to use multiple stacked smaller ones because it is better for a deeper neural network, it gives more powerful features, fewer parameters, and option to add additional non-linearities. One large kernel (8,8) number of weights is 64. Multiple stacked smaller ones 4x(2,2) number of weights is 16. 


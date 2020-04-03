# single-frame Low illumination image enhancemnt
 - [x] LLNet: A Deep Autoencoder approach to Natural Low-light Image
Enhancement  
      Description: the early learning based work of low illumination image enhancement; simulated dark datasets; conventional methods comparison. 
 - [x] MSR-net:Low-light Image Enhancement Using Deep Convolutional Network
      Description: multi-scale logarithmatic processing for multi-scale retinex simultation; Analogy between convolution and difference of Gaussian; color restoration function with 1x1 conv; 
      - [x] have no idea why and how adopt log space?( learn the code later): maybe the log space for add operation.
 - [x] Deep Retinex Decomposition for Low-Light Enhancement
      Description: interersting work! decompose the image into constant reflectance and illumination and then enhance the illumation map to reconstruct the normal light image.
      - [x] try the code to find if any lighting condition: I tried to decompose the image with different exposure time and multiplied t1's reflectance and t2's illumination. Then the generated t2's(more light) have a bigger difference than the true t2's.
      - [x] This work deserves reading as the concept is simple and easy to apply. Many successive work based on it.
 - [x] Self-supervised Image Enhancement Network: Training with Low Light Images Only
      Description: process the image quickly; give the repeatbale results; based on Retinex-net;add the maximum channel assumption on the reflectance map-- the maximum channel of the enhanced image should conform to the histogram distribution of the maximum channel of the low light image after histogram equalization.


# single-frame Low illumination image enhancemnt
 - [x] LLNet: A Deep Autoencoder approach to Natural Low-light Image
Enhancement  
      Description: the early learning based work of low illumination image enhancement; simulated dark datasets; conventional methods comparison. 
 - [x] MSR-net:Low-light Image Enhancement Using Deep Convolutional Network  
      Description: multi-scale logarithmatic processing for multi-scale retinex simultation; Analogy between convolution and difference of Gaussian; color restoration function with 1x1 conv; 
      - [x] have no idea why and how adopt log space?( learn the code later): maybe the log space for add operation.
 - [x] Deep Retinex Decomposition for Low-Light Enhancement  [code][trial]
      Description: interersting work! decompose the image into constant reflectance and illumination and then enhance the illumation map to reconstruct the normal light image.
      - [x] try the code to find if any lighting condition: I tried to decompose the image with different exposure time and multiplied t1's reflectance and t2's illumination. Then the generated t2's(more light) have a bigger difference than the true t2's.
      - [x] This work deserves reading as the concept is simple and easy to apply. Many successive work based on it.
 - [x] Self-supervised Image Enhancement Network: Training with Low Light Images Only 
      Description: process the image quickly; give the repeatbale results; based on Retinex-net;add the maximum channel assumption on the reflectance map-- the maximum channel of the enhanced image should conform to the histogram distribution of the maximum channel of the low light image after histogram equalization.


# colorization:
- [x] Pixel-level Semantics Guided Image Colorization [no-reference][plausible color][no code]  
      Description: combining with semantic segementation loss to get more robust color;joint bilinear lateral filter for edge preserving; calculate color probability for 313 potential values(classification label).

- [x] Tracking Emerges by Colorizing Videos (ECCV18) [no code]  
      Description: 3 successive frames as the input reference color and output the fllowing fourth frame. The loss is dicrete categories loss and this work use k-means to quantize the color values  into 16 categories. And then the embedding of this model can be exploted to tracking and outperform the optical-flow based method.

- [x] Instance-aware Image Colorization [no-reference]    
      Description: detect N objects in advance and then colorize the full image and seperate object respectively. Finally, fuse the features of the  full image and local objects with the weighted map to output the final color images. use smooth L1 loss.    

- [x] Deep Exemplar-based Video Colorization [example-based]   
      Description: use vgg feature to calculate the correlation between  reference image's chrome channel and input gray image and then obtain the warped color information and the corresponding confidence map. Afterwards, the final output rgb image depends on the last rgb image, warped color information, confidence map and the current gray map. This work used many loss functions to supervise the result, from contextual, temporal, realistic view. Good work. 


# alignment:
- [x] When Deep Learning Meets Data Alignment: A Review on Deep Registration Networks(DRNs)  
      Description: a review for data alignment. Maybe 3D data alignment  dominates the paper. Provide a list of data alignment paper and summary them in categories with the module constitution: CNN, deformable transformation, voxel, mesh?( some points I remembered). Emmm. I think maybe I need to read specific paper to know some new ideas.
     
     
      



      

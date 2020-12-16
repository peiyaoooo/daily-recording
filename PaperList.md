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

- [x] Zero-Reference Deep Curve Estimation for Low-Light Image Enhancement     
      Description: exploit cnn framework to generate pixel-wised adjustment matrix for high order adjustment function. Recursively iterate the function: LE(I(x);\Alpha) = I(x)+\Alpha I(x)(1-I(x)) about 8 times for output the final reconstruction. The losses they proposed are novel which are used to limit the function. For avoiding the overexposure, they add the overexposure photo to train this network. Good work. [https://li-chongyi.github.io/Proj_Zero-DCE.html/]  
      

# multi-frame Low illumination image enhancemnt     
 - [x] Dynamic Low-light Imaging with Quanta Image Sensors     
       Description: Exploit multi-frame of images captured via quanta image sensors to reconstruct the scene, which show better performance than normal sensorin extremely low-light condition. This work proposed the teacher-student strategy to guide the encoder's performance. The strategy is aimed to make encoder-extracted features of clean and noisy images similar. The performance is impressive but still a little blurry in local details.

 


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
      
# frame interpolation  
- [x] Channel Attention Is All You Need for Video Frame Interpolation  (20)    
     Description: a method for **intermediate frame interpolation**; combine the start and end frame to obtain the intermediate frame from pixel level. Directly output the predicted pixel rather than the optical flow which reduces the complexity and cost time. It leverages the pixel shuffle to covert the spatial information into channel dimension and then calculate the channel attention for better prediction. Nice job.

- [x] Learning Image Matching by Simply Watching Video  (16)    
   Description: flownet module calculates  the flow and evaluate the input frames' influence on output image via the gradient map. end2end pixel generation concept.

- [x] Video Frame Interpolation via Adaptive Separable Convolution (17)    
   Description: separate the large 2D convolutional kernel into two 1D kernel for compact representation of large motion. Reduce the parameters for estimation. Directly generate the pixel    
   Github: https://github.com/sniklaus/sepconv-slomo   
   
- [x] Video Frame Synthesis using Deep Voxel Flow(17)    
   Description: encoder-decoder framework to calculate the voxel flow ( the referenced position in the given frames) and then warp.Multi-sacle flow. Multi-step concept is to predict the next D frames rather than single frame.    

- [x] Super SloMo: High Quality Estimation of Multiple Intermediate Frames or Video Interpolation (18)  
   Description: U-net module for flow estimation and impose the probability map for the forward and backward flow. linearly interpolate the frames according to the time interval.    
   webpage: http://jianghz.me/projects/superslomo   

- [ ] MEMC-Net: Motion Estimation and Motion Compensation Driven Neural Network for Video Interpolation and Enhancement  
  github: https://github.com/baowenbo/MEMC-Net  
  
- [ ] Space-Time-Aware Multi-Resolution Video Enhancement    
  github: https://github.com/alterzero/STARnet  
  
 

# optical flow estimation  
- [ ] Learning by Analogy: Reliable Supervision from Transformations
for Unsupervised Optical Flow Estimation  
- [ ] Flownet  
- [ ] Flownet2  
- [x] PWCnet   
- [ ] IRR-PWC  
- [x] Optical Flow in the Dark  
  Description: It claims that could calculate the optical flow from underexposed pairs and have a better performance than the enhanced one which doesn't make sense to me. But many details are not clearly introduced in the paper. Wait for multi-exposure datasets and the pretrained model with their datasets.They provide a Gaussian-Possion-hybird noise model in this work and measure the noise level with a standard.



  
   
 
     
# super resolution  
- [x] Invertible Image Rescaling    
Description： [an interesting work with the independent probability usage]. First, exploit the Harr Transformation to decompose the image into low and high frequency information which resembles the bicubic-downsampling image. Then generage the case-independent high frequency probability with GAN and then reconstruct the high resolution image. The distribution loss is to describe the data distribution betweent the reconstructed image and orgin HR image
 
- [x] Learning for Video Super-Resolution through HR Optical Flow Estimation    
Description: Super resolve the coarse optical flow into fine optical flow at the high resolution and then pixelshuffle the warped HR images in LR cubes.  Fuse these referenced cubes and LR frames to generate the HR frames. The framework is compact and easy to use. [try this code]


- [x]   Zooming Slow-Mo: Fast and Accurate One-Stage Space-Time Video  Super-Resolution      
     Description: generate the high resolution high frame rate results. leverage deformable mechanism to extract information. Deformable conv to obtain lf lr's feature and then deformable convLSTM for temporal information interpolation. Then exploit resblock groups to super resolution. One stage pipeline.(Different from others)
     Github:https://github.com/Mukosame/Zooming-Slow-Mo-CVPR-2020/tree/4cc771888c9944ad61ba73295ac0dcafa557b7e8  

- [x] Learning Parallax Attention for Stereo Image Super-Resolution    
 Description: combine stereo low resolution images to interpolate high resolution images. Pixel shift is benefit to learn pixel value distribution rule. And in the feature  extraction, this proposal concats features filtered via different receptive fields. And in the warp session, the consistent loss and cycle loss exploits the the warped image is similar to the origin one and double warp images identify the origin one. 


- [ ] Learning Texture Transformer Network for Image Super-Resolution[ref-sr]

- [ ] cross-net[ref-sr]

# HDR
- [x] Merging-ISP: Multi-Exposure High Dynamic Range Image Signal Processing  (raw data)
Description: the procedure could be divided into the isp and fusion. This work generates the LDR images with different exposure and then fuse them to  output the final prediction in an end-to-end way. The author refers that the pre-alignment in raw space may result in the irreparable wrong signal which could not be handled in the last fusion network. And its presented result evidences this assumption. The network of this work is based on resblocks and different exposure image are concated and followed with conv 7x7,5x5,3x3,1x1.

- [x] Deep HDR Video from Sequences with Alternating Exposures  
Description: align  the medium exposure (ME) frame to the low/high exposure frame (LE/HE) and then merge the aligned frames and origin frames with the learned weight to generate the HDR image. The flow estimaiton resembles to SPYnet and add some tone perturbations for robust performance. But the output aligned frame is warped via the raw frame.

- [x] Deep SR-ITM: Joint Learning of Super-Resolution and Inverse Tone-Mapping for 4K UHD HDR Applications   
Description: fuse SR and tone-mapping in the pipeline. And firstly the work divides the image into the base image and detailed image and then learn the residual between the hdr GT and bicubic-upsampled sdr. Here, there are some confusion on the residual. The gap bewteen the sdr and hdr. Emmmm.  


# raw image processing

## color constancy
- [x] A Multi-Hypothesis Approach to Color Constancy    
Description: the AWB processing for the raw images. Convert the raw images to the 2-dimension(Nx2) vectors (b/g, r/g) and then choose several candiates to adjust the tone (diag(l_i)^-1Y) for several hidden versions. And then calculate the probability of different candidates and optimize their expectation with MSE loss for the final out. Note that 
the log-posterior probability can be formulated as:$$log(P(l|Y}}= G_l \cdot log(P(Y|l))+B_l$$. Learn how to write a story. ** should try the code**  
[code] : https://github.com/huawei-noah/multi_hyp_cc/tree/2377430f528aea2fb6d4fd4e861d9196e00a94d9  


# multiview video enhancement  
- [x] Multiview video quality enhancement without depth information  
Description: Fuse the image pair with the high compression quality and low compression quality without the aid of depth or disparity in an end-to-end framework. Averaged 2 dB higher than HEVC when QP=50.  

- [x] Blind Video Temporal Consistency via Deep Video Prior  
Description: propose a constraint to limit the temporal consistency and only need to train the first frame to acknowledge the input distribution of the videos. An confidence map is used to fuse the mainly-true prediction and the minorly-true prediction. The idea seems similar to tripet loss. Maybe I should use the module in the code.

# novel view synthesis
- [x] Stereo Magnification: Learning view synthesis using multiplane images  
Description: propose the concept of the MPI to blend the input image for view synthesis. Add camera parameters and image pairs for training. Interesting work! ** should try the code **
# network basis
- [x] Making Convolutional Networks Shift-Invariant Again   
Description: from my point of view, he proposed a method for anti-alias interpolation with convolutions. The key is to keep the upsampling or downsampling in a reproducable and reliable way.

- [x] CBAM: Convolutional Block Attention Module  
Description: introduce the spatial and channel attention module and obtatin the conclusion that  the
channel-first order performs slightly better than the spatial-first order.   

# point cloud
## Point cloud quality assessment
- [x] a paper related to energy



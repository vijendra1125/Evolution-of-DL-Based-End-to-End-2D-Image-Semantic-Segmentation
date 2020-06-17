# Post-FCN-Evolution-of-End-to-End-2D-Image-Semantic-Segmentation
In this repository I focus on compiling noticable research done in the field of end to end semantic segmentation of 2D-images post Fully Convolutional Network (FCN) publication in 2014. 

Hopefully I will also add some implementaiton and summary notes in future.

## Evolution
### FCN
All current state-of-art deep learning methods for semantic segmentation has been evolved from FCN. FCN introduced the concept of replacing fully connected layer in the classification network with convolutional layers and hence a mean for end-to-end training of semantic segmentation and learning dense prediction for input image of any size. It also presented how skip connection and learned upsampling (deconvolution) could be used to recover spatial information which is lost in Deep Convolutional Neural Network (DCNN) due to max-pooling and sub-sampling. 

There were three major issue with FCN which was further followed by researchers to improve performance.
* Loss of spatial information - Due to downsampling of input using max-pooling and sub-sampling
* Inability to capture global context - Due to inherent spatial invariance
* Lack of mechanism for multi-scale processing - Due to fixed-size receptive field 

### Loss of spatial inforamtion
Giving a bigger picture, most noticable approach could be seen as follow:
* Limiting the loss of spatial information
  * Use of dilated convolution in encoder in order to retain a dense feature map output from encoder without compromising on expanding receptiv field as we go deeper in the network and hence limiting the loss of spatial information.
    * Papers: DeepLab, DilateNet
* Recovering the lost spatial information
  * Recovering by complemeting the decoding process with the available infromation from encoder
    * Skip connections from feature map before max-pooling
      * Elementwise addition
        * Papers: FCN, SegNet
      * Concatenation
        * Papers: UNet
    * Max-pooling indices
      * Papers: DeconNet, SegNet
  * Recovering by learning the lost spatial information during decoding process
    * Learning using convolutional layers
      * Papers: UNet, SegNet
    * Learning using deconvolutional layers
      * Papers: FCN, DeconvNet
    
### Inability to capture global context
In progress
* Conditional Random Field (CRF)
  * Papers: DeepLab, CRFasRNN

### Lack of Mechanism for multi-scale processing
Coming in future

## Survey
* 20160221 [A Survey of Semantic Segmentation](https://arxiv.org/abs/1602.06541)
* 20170422 [A Review on Deep Learning Techniques Applied to Semantic Segmentation](https://arxiv.org/abs/1704.06857) :heart:
* 20170708 [Deep Semantic Segmentation for Automated Driving: Taxonomy, Roadmap and Challenges](https://arxiv.org/abs/1707.02432)
* 201711xx [A review of semantic segmentation using deep neural networks](https://www.researchgate.net/publication/321283063_A_review_of_semantic_segmentation_using_deep_neural_networks)
* 20180307 [RTSeg: Real-time Semantic Segmentation Comparative Study](https://arxiv.org/abs/1803.02758) :heart:
* 20180823 [Methods and datasets on semantic segmentation: A review](https://www.sciencedirect.com/science/article/abs/pii/S0925231218304077)
* 20180920 [Recent progress in semantic image segmentation](https://arxiv.org/abs/1809.10198)
* 20190421 [Survey on semantic segmentation using deep learning techniques](https://www.sciencedirect.com/science/article/abs/pii/S092523121930181X)
* 20191221 [A Survey on Deep Learning-based Architectures for Semantic Segmentation on 2D images](https://arxiv.org/abs/1912.10230) :heart:


## Research 
* 20141114 FCN [Fully Convolutional Networks for Semantic Segmentation](https://arxiv.org/abs/1411.4038)
* 20141222 DeepLab V1 [Semantic Image Segmentation with Deep Convolutional Nets and Fully Connected CRFs](https://arxiv.org/abs/1412.7062)
* 20150211 CRFasRNN [Conditional Random Fields as Recurrent Neural Networks](https://arxiv.org/abs/1502.03240)
* 20150517 DeConvNet [Learning Deconvolution Network for Semantic Segmentation](https://arxiv.org/abs/1505.04366)
* 20150518 U-Net [U-Net: Convolutional Networks for Biomedical Image Segmentation](https://arxiv.org/abs/1505.04597)
* 20150615 ParseNet [ParseNet: Looking Wider to See Better](https://arxiv.org/abs/1506.04579)
* 20150902 DAG-RNN [DAG-Recurrent Neural Networks For Scene Labeling](https://arxiv.org/abs/1509.00552)
* 20151102 SegNet [SegNet: A Deep Convolutional Encoder-Decoder Architecture for Image Segmentation](https://arxiv.org/abs/1511.00561)
* 20151109 Bayesian SegNet [Bayesian SegNet: Model Uncertainty in Deep Convolutional Encoder-Decoder Architectures for Scene Understanding](https://arxiv.org/abs/1511.02680)
* 20151110 [Attention to scale: Scale-aware semantic image segmentation](https://arxiv.org/abs/1511.03339)
* 20151122 ReSeG [ReSeg: A Recurrent Neural Network-based Model for Semantic Segmentation](https://arxiv.org/abs/1511.07053)
* 20151123 DilateNet [Multi-Scale Context Aggregation by Dilated Convolutions](https://arxiv.org/abs/1511.07122)
* 20160329 sharpMask [Learning to Refine Object Segments](https://arxiv.org/abs/1603.08695)
* 20160418 LSTM-CF [LSTM-CF: Unifying Context Modeling and Fusion with LSTMs for RGB-D Scene Labeling](https://arxiv.org/abs/1604.05000)
* 20160602 DeepLab V2 [DeepLab: Semantic Image Segmentation with Deep Convolutional Nets, Atrous Convolution, and Fully Connected CRFs](https://arxiv.org/abs/1606.00915)
* 20160607 ENet [ENet: A Deep Neural Network Architecture for Real-Time Semantic Segmentation](https://arxiv.org/abs/1606.02147)
* 20161120 RefineNet [RefineNet: Multi-Path Refinement Networks for High-Resolution Semantic Segmentation](https://arxiv.org/abs/1611.06612)
* 20161130 Wider or Deeper [Wider or Deeper: Revisiting the ResNet Model for Visual Recognition](https://arxiv.org/abs/1611.10080)
* 20161204 PSPNet [Pyramid Scene Parsing Network](https://arxiv.org/abs/1612.01105)
* 20170617 DeepLab V3 [Rethinking Atrous Convolution for Semantic Image Segmentation](https://arxiv.org/abs/1706.05587)



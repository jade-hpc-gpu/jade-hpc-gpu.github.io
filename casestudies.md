---
title: JADE Case Studies and Success Stories
layout: page
permalink: "/casestudies/"
---


--------------------------
## Newcastle University 
### Dermatologically Inspired Deep Face Analytics 
<br>
Introduction 

The ability to detect face ageing which is localised to specific regions of the face has shown to be useful to both the medical and research communities. In medical practice it could be used to inform the diagnosis of conditions, and subsequently the speed and accuracy of screening. However, large-scale facial screening by human experts is laborious and requires specialised expertise. Hence, there is great value in the development of automated methods for feature extraction and decision making from facial Imagery in a health and well-being context 
<br>

Explaining the Science <br>
The main challenge in training any machine learning problem is data. In order to train a deep neural network to predict something accurately, there must be a large number of known data points. When approaching the field of ageing, there is no dataset in existence labelling the rate at which different face regions have aged. 

Our approach to this lack of data is to build on the work of others who have developed models for global face ageing and semantic face segmentation. Semantic face segmentation is a field which splits face regions at a pixel level. We intend to learn from both existing datasets of segmented faces and datasets containing global face ages. The combination of these two types of data provide a framework to develop novel new methods for grading the ageing of faces at a feature level. 

Aside from grading the uneven rate of ageing across the human face, we also access a novel dataset of elderly individuals who have died since the images were taken. We use these faces in combination with the number of years they lived following the photograph, to attempt to extract features relevant to their mortality.  <br>

Project aims <br>
The aims and objectives of this project are interdisciplinary at their core. Ranging from novel contributions in data annotation, to neural network architecture; to dermatological analyses. We intend to explore the active research area of ageing and vitality, covering gaps in existing research and propose a new deep learning model to analyse the heterogeneous ageing of human faces. While there is existing work detailing both human and computational methods for grading face ageing, little research has been done to apply deep learning to this problem. We aim to train convolutional neural networks to extract features related to age, health and ultimately mortality. <br>

Applications <br>
Our work is highly applicable to several practical and research areas, with many more possible applications materialising as the wealth of academic data grows. 

The ability to accurately extract age and health related features from face images allows Dermatological research to be carried on sample sizes which are several orders of magnitude larger than without. Presently clinical trials for dermatological treatment are run in labs, with expensive photography equipment and highly skilled reviewers needed to evaluate outcomes. Given an effectively trained neural network, these analyses can be carried out automatically using selfie images from mobile phones; allowing participants to be located anywhere globally. The benefits of remote face skin analysis also extend to every-day practice, where pre-appointment screening can be carried out to filter patients who may not need to see a doctor immediately. 

Given a mortality feature extractor with a good correlation to the endpoint of death, it is possible to implement screening systems in high risk locations such as GP surgeries and Care Homes. These systems could be designed to flag individuals with a higher relative mortality risk for their age, allowing them to receive care in a timely fashion. 

### Estimating individual pig liveweight trajectories from group-level weight measurements 

Introduction <br>
Recent years have seen an increase in the use of advanced data collection systems to improve management in pig farms, however, the cost of implementing such systems remains a barrier to many. Some of the most useful data for farm management are on an individual pig level, which requires investment of labour and expense of systems such as RFID tagging. Machine learning approaches can help to alleviate this issue for instance by estimating individual growth trajectories from unknown weight measurements without requiring expensive RFID systems. 

Explaining the science <br>
Machine learning methods can be used to estimate individual-level pig growth trajectories as a cheaper alternative to using RFID tag systems. However, the use of traditional machine learning methods in this task has several limitations, namely that they cannot incorporate all data on a group-level time series simultaneously. This limitation could have a potentially profound impact on their predictive accuracy and thus also their applicability. 

Project aims <br>
This project aims to develop more accurate methods for the prediction of individual-level growth trajectories. To achieve this, attention methods capable of integrating all contextual data within group-level time series will be developed, and comparisons between these methods and existing machine learning methods will be made. 

This project will also involve the exploration of attention weights produced by the attention methods to allow for the interpretation of resulting predictions. In addition, this project seeks to develop additional metrics for evaluating the accuracy of predicted growth trajectories, and to improve the ability of methods to generalize to pigs of different breeds than those that they were trained on. 

Applications <br>
The methods developed during this project have the potential to be used as a significantly cheaper alternative to RFID tagging systems for the tracking of individual-level pig weights when combined with either weighting platforms or camera-based pig weight estimation systems. This work could also be used as a foundation for the development of methods that can be applied to other livestock.

## Loughborough University

Yang Zhou 

As a PhD student from Department of Computer Science at Loughborough University, I have been using the JADE-2 to train an anomaly detection model for underwater unknown detection. In this case, apart from the normal layers like convolutional layers, activation functions etc., I implemented a new layer named Mask Fully Connected (MFC) layer, which was successfully run on the JADE-2. Four datasets were used in this experiment: CIFAR-10 dataset with 60,000 images, a simulation dataset with around 100 images, an underwater statue dataset around 4,000 images and a public underwater dataset SUIM around 5,000 images. Thus, I used JADE-2 to train different models on these datasets respectively and train the comparison methods such as GAN, VAE and LSA models as well. With JADE-2, the training process can be accelerated, and the model can be easily downloaded to my workstation for further validation locally. 

Lei Jiang  

I am a PhD student from the computer science department, Loughborough University. In my case, I mainly use Jade2 time to train/test models in novel view synthesis based on depth or neural radiance fields with the help of multi-gpus. The trained model can recover partial or completed 3D information from input images, allowing the further view transformation and neural rendering for new views. Two datasets including ShapeNet and KITTI dataset are used to validate the effectiveness of my method on JADE2. 

Jinze Huo 

My research interest lies in skeleton-based action recognition and my approach uses GCN to analyse skeleton data. I have to utilise Jade2 because the skeleton dataset is too big. The first paper has been published as below, while the second and third projects are in progress. 


Ye Wei 

The reason for me to use the JADE2 HPC is to train a traffic forecasting model based on Graph Neural Networks (GNNs). Traffic forecasting aims to predict future traffic conditions (e.g., congestion class or speed) in road networks based on historical observations (e.g., sensor recording). This task is an indispensable part of Intelligent Traffic System (ITS) and it has a wide range of applications from route planning and travel time estimation, to supply chain management. Since the network structure of urban cities is large and complex, GNN models are very slow to train on ordinary graphics cards such as RTX 2080 Ti. With the help of JADE2, the training process can be accelerated, and this can greatly enhance the efficiency of my research. 

Yixiao Zhang 

I developed a number of variants of Transformer neural network to recognize audio events. The training of Transformer costs a lot of time on local deep learning machines, so I used JADE2 to speed up my experiments. JADE2 has a strong computational power which significantly reduced my experiment time. 

Siyuan Deng 

I have been utilising the JADE-2 to train a re-identification model for visible-infrared person as a PhD student at Loughborough University's Department of Computer Science. In this instance, I employ JADE-2 to establish a baseline for a recent study that employs three modalities and contrastive learning to create an aggregate memory-based deep metric learning framework. The benchmark VIReID dataset SYSU-MM01 that was used has 491 identities that were gathered from two near-infrared cameras and four visible cameras. The training set contain 395 identities with 22,258 RGB and 11,909 infrared images. With JADE-2, the model can be trained to the baseline and quickly downloaded to the local workspace. The work submission and environment setup, however, are a little challenging. 

Jiangtao Wang 

JADE-2 is used to train and validate several computer vision deep networks in my PhD study. We used to employ single or dual NVIDIA graphic cards to develop, train and improve the neural networks for our underwater robot's exploration. This including the image segmentation, image enhancement, depth estimation and other robotic tasks. 

However once dealing with high quality images (e.g. 2k resolution) we used to wait for quiet longer time to complete network training and much longer time to improve its performance. As long as we moved our work to JADE-2, we use typical configurations such as 8 GPUs to train network in parallel to significantly save time from network training. 

Wenjuan Zhou 

Title: Visual focus of attention detection in an unconstrained environment 

The visual focus of attention (VFOA) is this kind of human behaviour which is determined by eye gaze and head pose dynamics. We need to estimate the Gaze to determine where the visual focus of attention is. Gaze estimation can be applied to many scenarios, such as driving, and human-robot interaction. In addition, the detection of abnormal gaze is also widely used in the medical field. For example, in the standard of early screening and treatment of autism spectrum disorder (ASD), reduced eye contact is considered an important indicator. There is a robot-assisted system that can help with the treatment in the early stage of ASD. In this system, the robot needs to judge the child’s gaze information to give the corresponding response. If the robot wants to interact with humans, the robot needs to determine whether the gaze attention of the person is concentrated on the robot or not, this will help the robot to catch the timing of interacting with the human. 

The visual focus of attention detection as an important topic under the Human-Robot interaction scenes faced the huge challenge of low detection accuracy in real-world applications compared with laboratory scenes. Since most of the images obtained through the robot camera have no restrictions on the light source, posture, and scene. Recently, with the development of deep learning technology, the performance of visual focus of attention detection-based deep learning models has been significantly improved. We aim to build deep learning models that enable the robot to detect the visual focus of attention in an unconstrained environment in real-time. For achieving the aim, we need a larger dataset to train the deeper model we built, this needs a huge number of computational resources, and we would like to use Jade2 HPC to speed up our experiments and finish our study quickly. 

Up till now, we have already configured the environment on Jade2 to train models. For the next step, we will train the models we build, and enlarge the annotated training dataset to achieve better performance in our study. 




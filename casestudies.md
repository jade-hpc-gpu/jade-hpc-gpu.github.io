---
title: JADE Case Studies and Success Stories
layout: page
permalink: "/casestudies/"
---


--------------------------
## Newcastle University 
## Dermatologically Inspired Deep Face Analytics 
<br>
Introduction 

The ability to detect face ageing which is localised to specific regions of the face has shown to be useful to both the medical and research communities. In medical practice it could be used to inform the diagnosis of conditions, and subsequently the speed and accuracy of screening. However, large-scale facial screening by human experts is laborious and requires specialised expertise. Hence, there is great value in the development of automated methods for feature extraction and decision making from facial Imagery in a health and well-being context 
<br>

Explaining the Science <br>
The main challenge in training any machine learning problem is data. In order to train a deep neural network to predict something accurately, there must be a large number of known data points. When approaching the field of ageing, there is no dataset in existence labelling the rate at which different face regions have aged. 

Our approach to this lack of data is to build on the work of others who have developed models for global face ageing and semantic face segmentation. Semantic face segmentation is a field which splits face regions at a pixel level. We intend to learn from both existing datasets of segmented faces and datasets containing global face ages. The combination of these two types of data provide a framework to develop novel new methods for grading the ageing of faces at a feature level. 

Aside from grading the uneven rate of ageing across the human face, we also access a novel dataset of elderly individuals who have died since the images were taken. We use these faces in combination with the number of years they lived following the photograph, to attempt to extract features relevant to their mortality.  
<br>

Project aims <br>
The aims and objectives of this project are interdisciplinary at their core. Ranging from novel contributions in data annotation, to neural network architecture; to dermatological analyses. We intend to explore the active research area of ageing and vitality, covering gaps in existing research and propose a new deep learning model to analyse the heterogeneous ageing of human faces. While there is existing work detailing both human and computational methods for grading face ageing, little research has been done to apply deep learning to this problem. We aim to train convolutional neural networks to extract features related to age, health and ultimately mortality. 
<br>

Applications <br>
Our work is highly applicable to several practical and research areas, with many more possible applications materialising as the wealth of academic data grows. 

The ability to accurately extract age and health related features from face images allows Dermatological research to be carried on sample sizes which are several orders of magnitude larger than without. Presently clinical trials for dermatological treatment are run in labs, with expensive photography equipment and highly skilled reviewers needed to evaluate outcomes. Given an effectively trained neural network, these analyses can be carried out automatically using selfie images from mobile phones; allowing participants to be located anywhere globally. The benefits of remote face skin analysis also extend to every-day practice, where pre-appointment screening can be carried out to filter patients who may not need to see a doctor immediately. 

Given a mortality feature extractor with a good correlation to the endpoint of death, it is possible to implement screening systems in high risk locations such as GP surgeries and Care Homes. These systems could be designed to flag individuals with a higher relative mortality risk for their age, allowing them to receive care in a timely fashion. 

## Estimating individual pig liveweight trajectories from group-level weight measurements 

Introduction <br>
Recent years have seen an increase in the use of advanced data collection systems to improve management in pig farms, however, the cost of implementing such systems remains a barrier to many. Some of the most useful data for farm management are on an individual pig level, which requires investment of labour and expense of systems such as RFID tagging. Machine learning approaches can help to alleviate this issue for instance by estimating individual growth trajectories from unknown weight measurements without requiring expensive RFID systems. 

Explaining the science <br>
Machine learning methods can be used to estimate individual-level pig growth trajectories as a cheaper alternative to using RFID tag systems. However, the use of traditional machine learning methods in this task has several limitations, namely that they cannot incorporate all data on a group-level time series simultaneously. This limitation could have a potentially profound impact on their predictive accuracy and thus also their applicability. 

Project aims <br>
This project aims to develop more accurate methods for the prediction of individual-level growth trajectories. To achieve this, attention methods capable of integrating all contextual data within group-level time series will be developed, and comparisons between these methods and existing machine learning methods will be made. 

This project will also involve the exploration of attention weights produced by the attention methods to allow for the interpretation of resulting predictions. In addition, this project seeks to develop additional metrics for evaluating the accuracy of predicted growth trajectories, and to improve the ability of methods to generalize to pigs of different breeds than those that they were trained on. 

Applications <br>
The methods developed during this project have the potential to be used as a significantly cheaper alternative to RFID tagging systems for the tracking of individual-level pig weights when combined with either weighting platforms or camera-based pig weight estimation systems. This work could also be used as a foundation for the development of methods that can be applied to other livestock. 

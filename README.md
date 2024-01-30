# Automated Social Distancing Monitoring Project
## 1. Intro
### 1.1 Problem statement
<p align="justify">The Covid-19 pandemic has resulted in a significant loss of human life around the world. It poses an unparalled threat to public health. food systems, and the workplace. The pandemic's economic and social effects are devastating, and tens of millions of people are at risk of falling into extreme poverty. Many people are vulnerable especially in certain job sectors as they lack social security and quality health care. A lot more are also unable to feed themselves and their families during lockdowns too because they lack the resources to make a living. This means that if precautions are not taken to minimize these risks, a lot of people are going to lose their jobs and company layoffs would be increasing as the pandemic goes on.</p>

<p align="justify">Even as the pandemic is going on and lockdowns are happening, people are still not taking this health hazard as seriously as they should and are not following the correct procedures to minimize the spread of the virus. If this problem is not solved quickly, we will face bigger problems that will worsen the situation as it is just a matter of time. The Coronavirus has a faster mutation rate than influenza, so by the time billions of people are infected with this coronavirus strain which is SARS-COV-2, it is possible that it could mutate into a few other strains which would require its own vaccines. This will cause not only the loss of life of more humans, but also greatly impact the workforce making people lose their jobs even more.</p>

### 1.2 Objective
<p align="justify">The aim of this project is to make sure that people practice good social distancing due to the severity of the situation by building an automated social distancing monitoring system. This project will also aim to minimize the transmission of the Covid-19 strain by minimizing the contact between potential individual that may be infected with Covid-19 or between groups that has a high chance of transmission and by doing that, the chances of the virus spreading can be lowered. This system is also to observe if people are violating the safe distance one person and another. When two people are having a distance with each other that is deemed safe, the detection circles around them will light up green, however, if they violate the distance rules, the circle will light up red considering it a distance violation.</p>

## 2. Overall System Architecture
<p align="justify">The system built generally contains two modules which are the people detection, which is implemented using the object detection models, and a person-to-person distance analysis module. The object detection model built is based on the YoloV5 model and further train the model to fit into the problem. As for the distance analysis module, Bird’s-Eye View technique is used to develop the analysis module to predict the distance between the people detection and analyse whether they have violated the social distance or not. The user is able to interact with the system through a Graphical User Interface (GUI). The system is able to take in two forms of inputs which are 1920 x 1080 images and videos which allows better analysis, and it outputs the same images and videos with the violations indicated as well as the ones without violating the social distance. A simple line chart visualisation will also be produced by the system which plots the number of violations against the frames of the video.  </p>

## 3. Implemented ML Techniques for People Detection
### 3.1 Object Detection Architecture
<p align="justify">The concept that the system is built on is object detection. Using computer vision, the system is able to identify and locate the ocjects present within the image or video, and then a bounding is box is drawn on the detected object which in this case are the humans in the image or video. The model is trained to also differentiate between people and objects so that it can detect people accurately even if their full body is not shown in the frame.</p>

### 3.2 SSD MobileNetV2
<p align="justify">One of the approaches used to develop the object detection model was SSD MobileNetV2. MobileNet is a replacement for the standard convolutional network with a depth-wise separable convolution, which reduces the complexity and model size. The way that this works is that in the convolutional blocks for this model, the first layer aims to make the ouput have more channels than the input. Afterwards, the lightweight depth-wise convolutions are used to filter features as sources of ReLU5 non-linearity. The third layer of the model, the 1x1 convolution layer projects data with a high number of dimensions into a tensor with a lower number of dimensions also called the bottleneck layer. The MobileNet network was developed to improve the real-time performance of deep learning under limited hardware conditions and this network is able to reduce the number of parameters without sacrificing accuracy.</p>

### 3.3 YoloV5
<p align="justify">The other approach used is YoloV5 which has its own convolutional architecture compared to the SSD models. Yolo has multiple versions in the past and the V5 has outperformed its past versions and managed to get an average precision (AP) score close to EfficientDet with higher fps. The overall architecture of the Yolo network consists of three main stuctures. Firstly is the backbone which is a convolutional neural network that extracts all the important features of the given input image. In YoloV5, the CSP networks are used to achieve this. Next, the architecture also consists of the neck which is a series of layers that are responsible to combine the features from the backbone and forward them for prediction. Feature pyramids are generated to help the model generalize on object scaling which will help to identify the same objects of different sizes. Lastly, the structure is the head which takes features from the neck and perform the final detection. Anchor boxes on features are applied and final output vectors with class probabilities, object scores, and bounding boxes are generated.</p>

## 4. System Demo
![](Demo Assets/socialdistancedemo.gif)

## 5. Critical Analysis of Implementation
### 5.1 Qualitative Analysis
<p align="justify"></p>

### 5.2 Quantitative Analysis
<p align="justify"></p>

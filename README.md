## An Effective Technique for Vehicle Collision Detection System

## Certificate of Presentation

![image](https://github.com/user-attachments/assets/224d26ac-6402-48b4-b2ed-9674c06aa103)


## Abstract 
<p>The proposed research paper gives us an insight to the YOLO model system which helps us in avoiding vehicle collisions by identifying cars and pedestrians, separating sidewalks and crosswalks from the street, identifying traffic lights and signs, identifying road lanes, and calculating the distance from surrounding cars. The accuracy of the proposed research is 87% i.e it will help us in avoiding vehicle collisions by 87%.</p>

## I.	Introduction 
<p>With the increasing number of vehicles and population, road congestion has become a major problem, which increases the risk of road accidents. To enhance road safety, image processing techniques can be used to detect and objects in images. There are two types of CNN-based approaches for object detection: two-stage and one-stage methods[1]. One-stage methods like YOLO can detect objects in real-time with high accuracy, while two-stage methods are more accurate but slower. Real-time classification of intelligent transport systems using CNN-based models such as YOLO and DRoINs can achieve high accuracy rates for object detection.</p>

  ## II. Related Study
<p>The researchers proposed a long short-term memory convolutional neural network to propose a real-time crash risk prediction model for urban arterials (LSTM-CNN). The model takes into account a variety of factors such as traffic flow patterns, signal timing, and weather conditions. The training dataset is resampled using the synthetic minority over-sampling method (SMOTE). The suggested 2 model beats five conventional models in terms of Area Under the Curve (AUC), sensitivity, and false alarm rate. According to the findings, LSTM-CNN can be a useful technique for forecasting real-time accident risk on arterials. [2] Researchers proposed an effective technique to detect traffic incidents in Chicago, the study employs sophisticated deep learning algorithms such as LSTM and GRU. The dataset contains spatiotemporal data, meteorological conditions, and congestion status information. Because of the unbalanced dataset, SMOTE is used. With an AUC of 0.85, both models perform very well, however the GRU model exceeds the LSTM model in terms of detection rate. Both models have a comparable false alarm rate. [3] An autonomous automobile is a driverless vehicle that can navigate without human intervention by detecting its surroundings. Researchers proposed a solution for real-time 3D collision detection and avoidance algorithms based on Deep Learning and Convolutional Neural Networks.[4]. The model achieves an accuracy of 98% in detecting accidents in public traffic accident datasets, indicating high detection capacity independent of road structure. </p>
 
 ![image](https://github.com/user-attachments/assets/884c3d61-812a-4f5b-88eb-c902eb6f6629)

<p>Figure 1:Behavior of the models accuracy by epochs with the training set and validation set.[5]</p>
<p>The researcher discusses the use of social media and open data to predict traffic accidents. The proposed model utilizes an ensemble Deep Learning Model, consisting of Gated Recurrent Units and Convolutional Neural Networks. [3] The researcher proposes an advanced traffic monitoring system that can identify and detect moving objects in live camera feeds and detect collisions, sending emergency alerts to nearby authorities for necessary actions. The system builds upon traditional traffic systems that use IP cameras and sensors to monitor and control traffic, but with added capabilities for detecting accidents[5].</p>

## III.	Methodology

![image](https://github.com/user-attachments/assets/b3f7025a-713a-431b-9125-947d0186c966)


       
  ![Screenshot (1)](https://github.com/user-attachments/assets/02af48c6-95a3-456a-a9d5-d64af3139ae1)

## IV. Results
<p>Using the Vicos and Tsinghua datasets, the YOLO5 network has shown that it can detect traffic signs. About 7000 high-resolution images of 200 different traffic signs were taken while traveling on Slovenian highways and included in the Vicos collection[6]. This dataset was labeled by a Slovenian business called DFG, sometimes known as the DFG dataset.</p>
          
  ![Screenshot (2)](https://github.com/user-attachments/assets/51897f9d-e6f1-4de4-a72e-e0f9c2d40628)

<p>100,000 photos and more than 30,000 traffic signs, including 200 different traffic sign types, are involved in the Tsinghua dataset[7].For these sections, in addition to the YOLO5 network for detection, the model is tweaked using COCO, the default dataset used by YOLO itself.</p>     
<h3>A.	Walking paths detected</h3>
<p>We need a semantically separated image to find the pavement. The SGDepth network is utilized in this section.</p>

![image](https://github.com/user-attachments/assets/7e937725-37c7-492a-84ac-98cf7829dfc6)
                                                                                                                                             
<p>Additionally, the SGDepth network in this part has been taught using the Kitti and Cityscapes datasets[8].</p>
  
  ![image](https://github.com/user-attachments/assets/624da5c8-98be-4006-a568-25c05bd19cb2)

<h3>B.	Detection of crosswalks</h3>
In this proposed work, the OpenCV Python Library's supplied contours have been used to detect crosswalks.
      
  ![image](https://github.com/user-attachments/assets/fcea9fa5-47a8-4aca-b38c-6b1e080bc3ef)

<h3>C.	Lane detection on roads</h3>
<p>The PINet network's key point estimate and instance segmentation procedures are particularly important to the researcher. The network is trained using the CULane and TuSimple datasets[9]. The CULane dataset contains more than 55 hours of video that were recorded by cameras placed on six different vehicles being operated by diverse drivers in Beijing.</p>
  
  ![image](https://github.com/user-attachments/assets/ad8e585e-bb58-4c8f-975e-74f430d47574)
<p>There are 3626 videos in the TuSimple dataset, each lasting one second distance calculation Again, the SGDepth network has been employed in this section to measure the separation[10] between vehicles, but unlike the pavement detection section, the pink portion of the network structure has been utilized.   </p>                                                                                           



## Results

### Results on BDD100K dataset

![bdd](https://user-images.githubusercontent.com/61879630/199363094-6149ddd8-d2e8-4343-bea1-fee052d8bd5b.jpg)

### Results on our local dataset

![local](https://user-images.githubusercontent.com/61879630/199363107-e4ebb719-ac51-49f7-ae61-f663caaad6c6.jpg)


## Inference
To run the program, first install the requirements using the code below:
```
$ pip install -r requirements.txt
```
Then create a folder named 'weights' in the main directory and download all the weights in [this](https://drive.google.com/uc?export=download&id=1X1uKaGENEBZamF6tOfx9eKLTIQLsBN5h) shared google drive folder.

Then, place your video in the main folder of this repo and then run the following command.
```
$ python main.py --video yourvideoname.mp4 [--save] [--noshow] [--output-name myoutputvideo.mp4] [--fps]
```
--save argument will save the output video.

--noshow will not show you a preview of the output.

--output-name will determine the name you want for your output video

--fps will plot the fps results on the output frames

"yourvideoname.mp4" is the name of your video file added to the main folder.
"myoutputvideo.mp4" is the name you want for your output video.

Afterwards, the program starts running and the output video will be saved in the specified directory. To view the output while running, do not use '--no-show' argument.

There you have it.

## Colab Notebook
You can also use the provided colab notebook to automatically download all the weights and sample video, and run the program in a matter of seconds!

Simply open the following colab notebook

[![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/drive/1LcbZPaMPTWZf-4ZThsvwqzBi2BxtA3Br?usp=sharing)


1. Yolov5 ([Github](https://github.com/ultralytics/yolov5))
2. SGDepth ([Github](https://github.com/ifnspaml/SGDepth))
3. PINet ([Github](https://github.com/koyeongmin/PINet_new))

## Datasets

### Test Videos:
Please download from [here](https://drive.google.com/uc?export=download&id=1-bRFhDt5EZULnQaKO35U3oX-p6yZwteB).

### Sign Datasets:
1. Traffic-Sign Detection and Classification in the Wild [Link](https://cg.cs.tsinghua.edu.cn/traffic-sign/)
2. DFG Traffic Sign Data Set [Link](https://www.vicos.si/Downloads/DFGTSD#:~:text=Dataset%20consists%20of%20200%20traffic,around%207000%20high%2Dresolution%20images.&text=The%20images%20have%20been%20anonymized,with%20the%20EU%20GDPR%20legislation.)

## REFERENCES
1.	 L. K. Wani; Md Maaz Momin; Sharwari Bhosale; Abhishek Yadav; Manas Nili et al, VehCrash     Detection using YOLO Algorithm, International Journal of Computer Science and Mobile Computing, Vol.11 Issue.5, May- 2022.
2.	Pei Li, Mohamed Abdel-Aty, Jinghui Yuan, Accident Analysis & Prevention,Volume 135, February 2020, 105371
3.	 Gutierrez-Osorio, C; González, F.A.; Pedraza, C.A. Deep, Learning Ensemble Model for the Prediction of Traffic Accidents Using Social Media Data Computers 2022,11,126
4.	Applying Deep Learning to Detect Traffic Accidents in Real Time Using Spatiotemporal Sequential Data Amir Bahador Parsa Rishabh Singh Chauhan a, Homa Taghipour a, Sybil Derrible a, Abolfazl (Kouros) Mohammadian
5.	Robles-Serrano, S.;Sanchez-Torres, G.; Branch-Bedoya, J. Automatic Detection of Traffic Accidents from Video Using Deep Learning Techniques. Computers 2021, 10, 148
6.	Deep learning for Real Time Collision Detection and Avoidance Jagannath Aghav, Poorwa Hirve Mayura Nene
7.	NPSNET: Real-Time Collision Detection and Responses Zyda, Michael J. Pratt David R., Osborne, William D, N. Monahan
8.	Flora Dilys Salim, Seng Wai Loke, Andry Rakotonirainy, Bala Srinivasan, Shonali Krishnaswamy Collision Pattern Modeling and Real-Time Collision Detection at Road Intersections, Proceedings of the 2007 IEEE Intelligent Transportation Systems Conference Seattle, WA, USA, Sept. 30 - Oct. 3, 2007
9.	Sumeyye CEPNI, Muhammed Enes ATIK, Zaide DURAN Vehicle Detection Using Different Deep Learning  Algorithms from Image Sequence Baltic J. Modern Computing, Vol. 8 (2020), No. 2, 347-358 https://doi.org/10.22364/bjmc.2020.8.2.10
10.	H. L. Wang and M. A. Jia-Liang, ‘‘A design of smart car accident rescue system combined with WeChat  platform,’’ J. Transp. Eng., vol. 17, no. 2, pp. 48–52, Apr. 2017.

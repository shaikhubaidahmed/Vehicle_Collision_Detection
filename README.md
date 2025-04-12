# Vehicle_Collision_Detection
This research explores a YOLO model system for advanced driver-assistance. It aims to enhance safety by detecting cars, pedestrians, and obstacles, differentiating sidewalks/crosswalks from roads, recognizing traffic signals, marking road lanes, and estimating distances. The model boasts an 87% accuracy in preventing vehicle collisions.

<h1>I. Introduction</h1>
With the increasing number of vehicles and population, road congestion has become a major problem, which increases the risk of road accidents. To enhance road safety, image processing techniques can be used to detect and objects in images. There are two types of CNN-based approaches for object detection: two-stage and one-stage methods[1]. One-stage methods like YOLO can detect objects in real-time with high accuracy, while two-stage methods are more accurate but slower. Real-time classification of intelligent transport systems using CNN-based models such as YOLO and DRoINs can achieve high accuracy rates for object detection.

<h1>II.	Related Study</h1>
<p>The researchers proposed a long short-term memory convolutional neural network to propose a real-time crash risk prediction model for urban arterials (LSTM-CNN). The model takes into account a variety of factors such as traffic flow patterns, signal timing, and weather conditions. The training dataset is resampled using the synthetic minority over-sampling method (SMOTE). The suggested 2 model beats five conventional models in terms of Area Under the Curve (AUC), sensitivity, and false alarm rate. According to the findings, LSTM-CNN can be a useful technique for forecasting real-time accident risk on arterials. [2] Researchers proposed an effective technique to detect traffic incidents in Chicago, the study employs sophisticated deep learning algorithms such as LSTM and GRU. The dataset contains spatiotemporal data, meteorological conditions, and congestion status information. Because of the unbalanced dataset, SMOTE is used. With an AUC of 0.85, both models perform very well, however the GRU model exceeds the LSTM model in terms of detection rate. Both models have a comparable false alarm rate. [3] An autonomous automobile is a driverless vehicle that can navigate without human intervention by detecting its surroundings. Researchers proposed a solution for real-time 3D collision detection and avoidance algorithms based on Deep Learning and Convolutional Neural Networks.[4]. The model achieves an accuracy of 98% in detecting accidents in public traffic accident datasets, indicating high detection capacity independent of road structure.</p>
 

<p>Figure 1:Behavior of the models accuracy by epochs with the training set and validation set.[5]</p>
<p>
The researcher discusses the use of social media and open data to predict traffic accidents. The proposed model utilizes an ensemble Deep Learning Model, consisting of Gated Recurrent Units and Convolutional Neural Networks. [3] The researcher proposes an advanced traffic monitoring system that can identify and detect moving objects in live camera feeds and detect collisions, sending emergency alerts to nearby authorities for necessary actions. The system builds upon traditional traffic systems that use IP cameras and sensors to monitor and control traffic, but with added capabilities for detecting accidents[5].
</p>





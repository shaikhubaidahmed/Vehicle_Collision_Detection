# An Intelligent Modular Real-Time Vision-Based System for Environment Perception

With the increasing number of vehicles and population, road congestion has become a major problem, which increases the risk of road accidents. To enhance road safety, image processing techniques can be used to detect and objects in images. There are two types of CNN-based approaches for object detection: two-stage and one-stage methods[1]. One-stage methods like YOLO can detect objects in real-time with high accuracy, while two-stage methods are more accurate but slower. Real-time classification of intelligent transport systems using CNN-based models such as YOLO and DRoINs can achieve high accuracy rates for object detection.



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

# Custom_Obeject_detection-My-Guitar

I have used this youtube video for my reference -> https://www.youtube.com/watch?v=GRtgLlwxpc4&t=627s

I have trained a model to detect the object(which is guitar in my case) with help of YOLOv5 configration model.

My model is pretty weak as I have given less test images due to which the accuracy of predcition/detection of guitar in image is pretty low.

It can be improved by giving a much more labelled images.

I took 27 pics of my guitar and divided it into test and validaiton dataset.
I used https://www.makesense.ai/ website to give my images a label.

After giving labels to the image I just went to the officail github website of YOLOv5 https://github.com/ultralytics/yolov5 and opend this project in google colab.

[you can watch the video mentioned above for creating the folders and uploading them to google colab]

# Steps for Training!!
1. Download the coco128.yaml file > give the path for training set and validation set.
2. change the number of objects which are going to be detected and also the provide the label of your object.
3. Now after doing this go to the training section and train the model.



##HYPERPARAMETERS
lr0: 0.01
lrf: 0.1
momentum: 0.937
weight_decay: 0.0005
warmup_epochs: 3.0
warmup_momentum: 0.8
warmup_bias_lr: 0.1
box: 0.05
cls: 0.5
cls_pw: 1.0
obj: 1.0
obj_pw: 1.0
iou_t: 0.2
anchor_t: 4.0
fl_gamma: 0.0
hsv_h: 0.015
hsv_s: 0.7
hsv_v: 0.4
degrees: 0.0
translate: 0.1
scale: 0.5
shear: 0.0
perspective: 0.0
flipud: 0.0
fliplr: 0.5
mosaic: 1.0
mixup: 0.0
copy_paste: 0.0

--------------------------------


Test Image used for my model
![test2](https://user-images.githubusercontent.com/92587549/140666562-35c7d3c6-6613-46c1-b06e-9990bcd8db19.jpg)


Result of my training.
![results](https://user-images.githubusercontent.com/92587549/140666984-2086cb56-8b4d-4515-8fbb-aa15e87fa4d4.png)


Labels which were given to my validation set.
![val_batch0_labels](https://user-images.githubusercontent.com/92587549/140667002-da6973ff-e7fc-4ea8-8484-950768d58ab7.jpg)


Prediction for my validaiton set.

![val_batch0_pred](https://user-images.githubusercontent.com/92587549/140667009-9712c59a-cba6-4ec2-9bf2-1d3cf94d6009.jpg)

Confusion matrix
![confusion_matrix](https://user-images.githubusercontent.com/92587549/140667115-43042ee5-ec97-4df8-8f77-579808ccdb00.png)


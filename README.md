# Versions
```
- python 3.7.0
- pytorch 1.7.1+cu101
- torchvision 0.8.2+cu101
- opencv 3.4.4
- onnx 1.6.0
- onnxruntime 1.10.0
- cuda 10.1
- NVIDIA Driver Version: 430.64
```

# Absract
Yolov4 and Yolov4-tiny which can get good accuracy from training. 
These model are base-body model for more high perfomanse model with custmized.
It also can be converted as onnx.

<img src="https://user-images.githubusercontent.com/48679574/145718477-f56d9fdc-8ff5-44be-89a8-428de7787b64.png" width="600px">


## download weights
- [yolov4 (Pytorch)：yolov4.conv.137.pth](https://drive.google.com/open?id=1fcbR0bWzYfIEdLJPzOsn4R5mlvR6IQyA)
- [yolov4.pth](https://drive.google.com/open?id=1wv_LiFeCRYwtpkqREPeI13-gPELBDwuJ)
- [yolov4-tiny (Pytorch)：yolov4-tiny.conv.29](https://github.com/AlexeyAB/darknet/releases/download/darknet_yolo_v4_pre/yolov4-tiny.conv.29)
- [yolov4 (Darknet)：yolov4.weights](https://www.google.com/url?sa=t&rct=j&q=&esrc=s&source=web&cd=&ved=2ahUKEwj74fGktd70AhVWk1YBHe9bDjMQFnoECAQQAQ&url=https%3A%2F%2Fgithub.com%2FAlexeyAB%2Fdarknet%2Freleases%2Fdownload%2Fdarknet_yolo_v3_optimal%2Fyolov4.weights&usg=AOvVaw30if4joxtTaS8DAh12vYQ4)
- [yolov4-tiny (Darknet)：yolov4-tiny.weights](https://github.com/AlexeyAB/darknet/releases/download/darknet_yolo_v4_pre/yolov4-tiny.weights)



# Results

# Note: cfg parameter when original class dataset training
if num_class is 1, convolutional-filters is 18 (=```(5+num_class)*3```)

```tiny-yolov4.cfg
[convolutional]
size=1
stride=1
pad=1
filters=18
activation=linear

[yolo]
mask = 3,4,5
anchors = 10,14,  23,27,  37,58,  81,82,  135,169,  344,319
classes=1
```

# References
- [pytorch-YOLOv4](https://github.com/Tianxiaomo/pytorch-YOLOv4)
- [OIDv4_ToolKit](https://github.com/EscVM/OIDv4_ToolKit)
- [Google Open Images Dataset V6 +](https://storage.googleapis.com/openimages/web/index.html)

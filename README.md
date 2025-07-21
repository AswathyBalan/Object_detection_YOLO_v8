**INTRODUCTION**

Object detection is a crucial task in computer vision, enabling systems to identify and localize
objects within an image. This project focuses on detecting various car parts using a YOLO v8
object detection model. The goal is to evaluate model performance on a custom dataset, analyze
challenging categories, and propose strategies for improvement. This project aims to build an
object detection model to identify and localize car parts in images using the YOLOv8 architecture.
The primary objective is to achieve high accuracy in detecting car parts, evaluated through mAP
(Mean Average Precision) metrics. This work has practical implications, such as improving vehicle
inspection and maintenance systems.

**Method**

The project implements the YOLO v8 model due to its balance between speed and detection
accuracy. Key features of the approach include:
● Fast Inference: Capable of real-time detection with minimal latency.
● Anchor-free Detection: Enhances bounding box placement, especially for overlapping
or small objects.
● Extensive Customizability: The framework integrates smoothly with PyTorch,
facilitating customization .
The training process involved optimizing loss functions, including classification and
bounding box regression losses, over 50 epochs. 

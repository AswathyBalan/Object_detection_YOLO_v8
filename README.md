**Car Parts Detection**

**Introduction**

Object detection is a crucial task in computer vision, enabling systems to identify and localize
objects within an image. This project focuses on detecting various car parts using a YOLO v8
object detection model. The goal is to evaluate model performance on a custom dataset, analyze
challenging categories, and propose strategies for improvement. This project aims to build an
object detection model to identify and localize car parts in images using the YOLOv8 architecture.
The primary objective is to achieve high accuracy in detecting car parts, evaluated through mAP
(Mean Average Precision) metrics. This work has practical implications, such as improving vehicle
inspection and maintenance systems.


**Dataset**

The dataset for this project is sourced from the Car Parts Segmentation GitHub repository. (https://github.com/dsmlr/Car-Parts-Segmentation)

It consists of:

● Training Dataset: 400 images with annotated bounding boxes.

● Testing Dataset: 100 images with annotated bounding boxes


The dataset utilized consists of images annotated with bounding boxes for various car parts. It is
divided into three subsets:

● Training set: Used to train the detection model.

● Validation set: Used to monitor model performance during training and ne-tune
hyperparameters.

● Testing set: Contains 80 images with 617 labeled instances, reserved for nal evaluation
Key aspects of the dataset

● The images represent 18 distinct car part categories, such as front_bumper,
rear_bumper, windshield, and tires.

● Each instance in the dataset is annotated with precise bounding boxes and corresponding
class IDs.

**Method**

The project implements the YOLO v8 model due to its balance between speed and detection
accuracy. Key features of the approach include:

● Fast Inference: Capable of real-time detection with minimal latency.

● Anchor-free Detection: Enhances bounding box placement, especially for overlapping
or small objects.

● Extensive Customizability: The framework integrates smoothly with PyTorch,
facilitating customization.

The training process involved optimizing loss functions, including classification and
bounding box regression losses, over 50 epochs

**Results and Analysis**

The model’s accuracy was evaluated using Mean Average Precision (mAP):

mAP@[IoU=50]: 0.7310210283491267

mAP@[IoU=50:95]: 0.7915177417014643

These results demonstrate that the model is procient in detecting car parts with good
precision at IoU thresholds of 50%, though stricter thresholds remain challenging.


Visualization

Sample predictions on the test dataset were visualized, showing bounding boxes, class
labels, and condence scores for detected objects. The visualizations demonstrate the
model's capability to localize car parts accurately, even in complex images


Certain categories were harder for the model to detect accurately. By analyzing detection
errors and condence scores, the following challenging categories were identied,

● Headlights and Tail Lights: Errors due to glare and reection.

● Side Mirrors: Mislocalization in images with occlusions.

● Small Components: Diculty with tiny parts like door handles

To address these challenges and improve detection accuracy for difficult classes, the following
enhancements are suggested:

● Augment the Dataset: Increase the variety of training images for underrepresented
categories through techniques like synthetic occlusions and perspective shifts.

● Focused Training: Fine-tune the model specically on challenging categories to improve
performance.

● Hyperparameter Tuning: Adjust learning rates and loss weights to optimize
category-specic detection.

● Model Ensemble: Combine YOLO v8 with complementary detection models to enhance
robustness

● Extended Training: Increase the number of epochs to allow better convergence of model
parameters.

Conclusion

This project demonstrated the effectiveness of YOLO v8 for object detection tasks,
particularly for car part localization. Although the model achieved strong
performance overall, the challenges faced in detecting certain categories highlight
the importance of high-quality data and targeted improvements. The project
required substantial computational resources, and training took a considerable
amount of time. In some cases, the system crashed during processing, indicating a
need for more robust hardware.

# Car-detection-with-YOLO
# Autonomous Driving - Car Detection using YOLO

Welcome to the Autonomous Driving Car Detection project! This repository guides you through the implementation of object detection using the powerful YOLO (You Only Look Once) model. By the end of this project, you will have the ability to detect objects in a car detection dataset, implement non-max suppression to improve accuracy, and understand key concepts like intersection over union and bounding boxes.

## Problem Statement

Imagine you are working on a self-driving car project. As a crucial component, you need to develop a car detection system. To collect data, you've mounted a camera on the front of the car, capturing images of the road while driving. The dataset consists of these images, with bounding boxes drawn around each car. Your task is to build a car detection model.

![image](https://github.com/meliikaa/Car-detection-with-YOLO/assets/111120849/20812a29-5143-4595-a746-a4cbcff1ba9b)


## YOLO - You Only Look Once

The YOLO (You Only Look Once) algorithm is known for its high accuracy and real-time processing capabilities. It stands out because it requires only a single forward pass through the network to make predictions, making it exceptionally efficient.

### Model Details

- Inputs and Outputs: The input consists of batches of images, each with a shape of (608, 608, 3). The output is a list of bounding boxes along with recognized classes, represented as 6 numbers per bounding box (𝑝𝑐,𝑏𝑥,𝑏𝑦,𝑏ℎ,𝑏𝑤,𝑐).

- Anchor Boxes: YOLO uses anchor boxes to represent different classes. For this assignment, 5 anchor boxes are provided, covering the 80 classes. These anchor boxes are defined by width and height.

- Encoding: The encoding tensor's dimension is (𝑚,𝑛𝐻,𝑛𝑊,𝑎𝑛𝑐ℎ𝑜𝑟𝑠,𝑐𝑙𝑎𝑠𝑠𝑒𝑠). The architecture is: IMAGE (m, 608, 608, 3) -> DEEP CNN -> ENCODING (m, 19, 19, 5, 85).

### Class Score

For each box, the class score is calculated as 𝑠𝑐𝑜𝑟𝑒𝑐,𝑖=𝑝𝑐×𝑐𝑖, representing the probability that an object exists (𝑝𝑐) times the probability that the object is a certain class (𝑐𝑖).

### Visualization

YOLO's output can be visualized by coloring grid cells based on the most likely object class. Bounding boxes can also be plotted, representing the detected objects.

### Non-Max Suppression

To reduce the number of detected objects, non-max suppression is applied. This involves filtering boxes based on a threshold for class scores and selecting a single box when multiple boxes overlap.


## Conclusion

By the end of this project, you will have gained valuable experience in object detection and understanding how YOLO performs it efficiently. Dive into the world of autonomous driving and enjoy building a car detection system. If you have questions or need assistance, feel free to reach out to the project contributors or the community. Happy coding!

## Credits

Thanks to DeepLearning.Ai for their Deep Learning course on coursera.

#AutonomousDriving #CarDetection #ObjectDetection #YOLO #DeepLearning #ComputerVision #MachineLearning #ProgrammingAssignment

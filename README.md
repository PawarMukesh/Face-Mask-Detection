# FACE MASK DETECTION
To build a system for detectiong if an individual is wearing a mask in a give image.

## DATA OVERVIEW & COLLECTION:
The Mask Wearing dataset is an object detection dataset of individuals wearing various types of masks and those without masks. The images were originally collected by Cheng Hsun Teng from Eden Social Welfare Foundation, Taiwan and relabeled by the Roboflow team.

* Download from: https://public.roboflow.ai/object-detection/mask-wearing
* Dataset contain total 149 images into two classes i.e Mask & Without Mask
* Example image (some with masks, some without):
  
![image](https://github.com/PawarMukesh/Face-Mask-Detection/assets/101791322/747497ce-ebde-4964-9283-3438eb133b34)


## DATA PREPRATION:
* Prepare folder structure that can be accept by YoloV5.
* Total 105 images for training and 29 images for validation present in 2 classes.
* Create a bounding boxes with the help of label-img And makesense.ai website according to YoloV5.

## STEPS TO USE YOLOV5
* Cloning the YoloV5 file from official repository.
* Changing the directory of yolov5
* Installing the dependencies
* Download all versions pre-trained weights

## STEPS BEFORE TRAINING CUSTOM DATASET:
1. Go to yolov5/data/
2. Open coco128.yaml
3. Edit the following inside it:

     A. Training and Validation file path

     B. Number of classes and Class names.

## TRAINING YOLOV5 MODEL
* Set images size 640 with batch of 8
* Train model around 1000 epochs but Stopping training early as no improvement observed in last 100 epochs Best results observed at epoch 278 i.e P:0.877    R:0.876      mAP50:0.909   mAP50-95:0.62
* Visualise the training metrics with the help of tensorboard

## TESTING IMAGES USING TEST DATA
![Test image1](https://github.com/PawarMukesh/Face-Mask-Detection/assets/101791322/123b0cd3-48c4-4a1d-9e6c-80d3a918f669)
![Test image 2](https://github.com/PawarMukesh/Face-Mask-Detection/assets/101791322/3ae5be9f-4e1e-42b4-9451-acd37552c94c)


## TESTING LOW QUALITY VIDEO DEMO
https://github.com/PawarMukesh/Face-Mask-Detection/assets/101791322/10381404-5456-4517-9bfc-c1d25709fbf3

## CHALLENGES FACED:
*	challenge faced in bounding boxes creation
*	Assign the same no for all classes
*	Made mistake in yolov5 folder structure
*	Take lots of time to create bounding boxes

# WHAT WE LEARN:
*	Understand the YoloV5 folder structure as well as learn label-IMG tool.
*	Learn Pytorch library.



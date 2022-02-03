# Image Segmentation Project

### Overview

A typical image taken from a camera during cooking has pixels which belong to one of the three categories:

1. Stirrer Region (marked as red{255, 0, 0})
2. Pan+Background Region(marked as green{0, 255, 0} )
3. Food region (marked as blue{0, 0, 255} )

The goal of the task is to train a segmentation model that classifies each pixel of an image into one of three classes(pan+background, stirrer, food)

Here are two sample image, mask pairs one from training and one from validation set.

<img src="https://nymblelabs.notion.site/image/https%3A%2F%2Fs3-us-west-2.amazonaws.com%2Fsecure.notion-static.com%2Fc371699d-1bcb-418e-a7f6-6a81409f8e5d%2Fupma4_671.jpg?table=block&id=a2b2ff84-48fb-417a-875e-9e89e79ee2bf&spaceId=1702510d-17cc-4333-ad95-b1762bbaf10d&width=2000&userId=&cache=v2" alt="img" style="zoom: 80%;" /> <img src="https://nymblelabs.notion.site/image/https%3A%2F%2Fs3-us-west-2.amazonaws.com%2Fsecure.notion-static.com%2F7edadcdd-a065-466a-89d9-061b815c9c3f%2Fupma4_671.png?table=block&id=0f753cba-9cbc-47cb-bee6-c0d824140b83&spaceId=1702510d-17cc-4333-ad95-b1762bbaf10d&width=1000&userId=&cache=v2" alt="img" style="zoom:80%;" /> 

<img src="https://nymblelabs.notion.site/image/https%3A%2F%2Fs3-us-west-2.amazonaws.com%2Fsecure.notion-static.com%2F9aede2d5-dea7-40c4-9be9-eff9e358148d%2Fpalakpaneer_1610_533.png?table=block&id=c09d4dee-2f3b-4e59-ad0e-1fcc61041e4a&spaceId=1702510d-17cc-4333-ad95-b1762bbaf10d&width=580&userId=&cache=v2" alt="img" style="zoom:80%;" /><img src="https://nymblelabs.notion.site/image/https%3A%2F%2Fs3-us-west-2.amazonaws.com%2Fsecure.notion-static.com%2F81b7b896-0d87-43b7-9e82-0f3cc2138d70%2Fpalakpaneer_1610_533.png?table=block&id=6e2d3d5f-b4ee-4694-9f0d-3fcfe34fb731&spaceId=1702510d-17cc-4333-ad95-b1762bbaf10d&width=960&userId=&cache=v2" alt="img" style="zoom:80%;" />

### Data

- 448 Training Images and Masks (with classes being color coded, red for stirrer, green for pan and blue for food)
- 137 Validation Images and Masks (with classes being color coded)
- 129 Test Set Images (For inference)

### Objectives

- A UNET Model is trained using PyTorch Framework. 
- Evaluation script for evaluating the accuracy, precision and recall of all three classes on the validation set using the trained model predictions and ground truth available.
- Inference script to generate the color coded mask for each of the test set images using the trained model.
- Color coded masks for all test set images are generated and stored in the folder 'test_inf_masks'.

#### Resources

kaggle Notebooks

- https://www.kaggle.com/dhananjay3/image-segmentation-from-scratch-in-pytorch
- https://www.kaggle.com/bulentsiyah/deep-learning-based-semantic-segmentation-keras


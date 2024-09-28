# Gesture Recognition By Implementing CNN and RNN Models

## Project Description
This project aims to develop a gesture recognition feature for smart TVs that allows users to control the device without a remote. Using a dataset of categorized videos, the model will recognize five gestures: thumbs up, thumbs down, left swipe, right swipe, and stop, translating them into corresponding commands for volume adjustment and playback control.

**Note:** Original files related to this project are not shared publicly as they are part of my academic assignments.

## Table of Contents
- [Project Structure](#project-structure)
- [Installation Instructions](#installation-instructions)
- [Libraries Used](#libraries-used)
- [Data Description](#data-description)
- [Generator](#generator)
- [Different Models Deployed](#different-models-deployed)

## Project Structure
- `final copy for nn.ipynb`: Jupyter notebook containing the code for data analysis, model building, and evaluation.
- `Model_Write_Up_NN_Project.pdf`: Document providing an overview of the models implemented, findings, and conclusions.
- `README.md`: This file provides an overview of the project, analysis, and instructions for setup and usage.

## Installation Instructions
1. Ensure you have Python 3.x installed.
2. Install required libraries using:
   ```bash
   pip install numpy keras tensorflow scikit-image imageio
   ```


## Libraries Used
The following libraries were used to perform the analysis and model building:
- **numpy**
- **os**
- **skimage**
- **imageio**
- **keras**
- **tensorflow**
- **datetime**

## Data Description
The training data consists of a few hundred videos categorized into one of five classes, each representing a specific gesture. Each video (typically 2-3 seconds long) is divided into a sequence of 30 frames (images). These videos have been recorded by various people performing one of the five gestures in front of a webcam. The classes are as follows:
1. Thumbs Up: Increase the volume
2. Thumbs Down: Decrease the volume
3. Left Swipe: 'Jump' backwards 10 seconds
4. Right Swipe: 'Jump' forward 10 seconds
5. Stop: Pause the movie

## Generator
In the generator, we preprocess the images to accommodate different dimensions and create batches of video frames for model training. This process ensures consistent input shapes and enhances the training efficiency.

## Different Models Deployed
1. **Simple Conv3D** (Batch size = 40, No. of epochs = 10)

2. **Conv3D with BatchNormalization** (Batch size = 40, No. of epochs = 15)

3. **Conv3D with BatchNormalization and Dropout** (Batch size = 40, No. of epochs = 20)

4. **Conv3D with BatchNormalization, Dropout, and GlobalAveragePooling** (Batch size = 40, No. of epochs = 30)

5. **Conv2D and LSTM** (Batch size = 40, No. of epochs = 40)

6. **Conv2D + GRU** (Batch size = 40, No. of epochs = 40)

7. **Transfer Learning (VGG16) + LSTM** (Batch size = 40, No. of epochs = 30)

8. **VGG16 + LSTM with BatchNormalization** (Batch size = 40, No. of epochs = 30)

9. **VGG16 + GRU** (Batch size = 40, No. of epochs = 20)

10. **Transfer Learning (MobileNet) + GRU** (Batch size = 40, No. of epochs = 15)

The implementation details and findings from these models are documented in `Model_Write_Up_NN_Project.pdf`.

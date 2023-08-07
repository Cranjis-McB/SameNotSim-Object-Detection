# SameNotSim-Object-Detection

## Goal

* The ultimate objective is to detect a specific type of object within a frame. However, there are a few objects in the scene that possess a similar appearance to our target object, and our goal is to exclude or avoid detecting those similar-looking objects.

* We are developing an end-to-end pipeline for a specific object detection task. This project contains 4 Notebooks namely:

  * **DataGeneration**: This notebook (to be uploaded) serves as the initial step, In this notebook, we aim to **generate data** for our object detection task from the raw data.
  * **cv_augmentations**: This notebook (to be uploaded) contains different types of augmentations to be done on the object (Logo) during data generation. (This will add robustness to our detection model.)
  * **Model_Training**: This notebook shows how to Train our detection model and use Various Data augmentation during Training.
  * **Model_Inference**: How to use the model for inference.

* Let's understand our folder structure.

  *  **<font color="red">RawData</font>** -> Consists of two main folders named "Train" and "Valid." Each of these folders contains several YouTube Reels that will be utilized to create the data required for our object detection task.
  
  * **<font color="red">Logos</font>** -> Contains three logos that are identical except for the color of the circle surrounding each logo. (shown in below Image)
  
  * **<font color="red">Data</font>**  -> At the beginning of this notebook, the folder is empty. However, by the end of the notebook, it will be populated with the generated data for our object detection task. The data will be derived from the "Train" and "Valid" folders within the "RawData" directory, and the generated data will then be organized into corresponding "Train" and "Valid" folders in this directory.

## Task Description

The objective is to detect the Red logo within the frame while excluding the Green and Blue logos from the detection process.


<img src="https://github.com/Cranjis-McB/SameNotSim-Object-Detection/blob/main/three_logo_img.png" alt="Picture" height = "250" width="250">

## Data Generation Procedure

1. Process the one Video from RAW_DIR.
2. Select a Random Frame.
3. Reads the Red LOGO and adds some augmentation to it. (For Robustness)
4. Paste it randomly on the Frame selected in Step-2.
5. Save the Image and Bounding Box Label in DATA_DIR.
6. Do this a number of times for each video.
7. Do this for all the Videos.

**Additionally** (To avoid Detecting Blue and Green Logos.)

After step-4 above, paste the Blue/Green Logo randomly with some probability  **<font color="red">but DO NOT store the Bounding Box for it.</font>**.

**By employing this approach, the model will be trained to selectively focus on detecting the red logo while disregarding the blue and green logos during the detection process.**

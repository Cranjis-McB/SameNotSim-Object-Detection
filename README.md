# SameNotSim-Object-Detection

## Goal

* The ultimate objective is to detect a specific type of object within a frame. However, there are a few objects in the scene that possess a similar appearance to our target object, and our goal is to exclude or avoid detecting those similar-looking objects.

* We are developing an end-to-end pipeline for a specific object detection task. This notebook serves as the initial step, where we will focus on explaining one particular scenario. In this scenario, we aim to generate data for our object detection task from the raw data.

* Let's understand our folder structure.

  1. RawData -> Consists of two main folders named "Train" and "Valid." Each of these folders contains several YouTube Reels that will be utilized to create the data required for our object detection task.
  
  2. Logos -> Contains three logos that are identical except for the color of the circle surrounding each logo. (shown in below Image)
  
  3. Data -> At the beginning of this notebook, the folder is empty. However, by the end of the notebook, it will be populated with the generated data for our object detection task. The data will be derived from the "Train" and "Valid" folders within the "RawData" directory, and the generated data will then be organized into corresponding "Train" and "Valid" folders in this directory.

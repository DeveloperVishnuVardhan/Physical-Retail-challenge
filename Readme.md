# Project Description
The goal of the project is to build a prototype that can demonstrate how the process of retail
shopping can be fully automated using computer Vision.

**The Project consists of two tracks:**
1. Activity based recognition.
2. Appearance based verification.

**Activity based recognition:** This is the phase-1 of the project pipeline here we process the
video of a customer and we will try to assign an certain activity category to the frames associated 
to it and also draw bounding boxes to the area involving the action (holding the object and placing
it into cart or stand).

**Appearance based verification:** Given an input query image we try to match it with the images
in the inventory. we do it for all products picked by customer at the end of shopping to produce 
the final bill.

## Description of the data
1. **Activity based recognition**
The dataset folder contains two sub-directories anns, frames where anns folder
contains text files with bounding boxes and activity class that belongs to each frame.
2. **Appearance based recognition** Yet to work on this (stay tuned)

## step-1:Setting up the project environment
* Install Anaconda Package manager.
* Create a new python environment: conda create --name "env-name" python=3.9
* Run pip install -r requirements.txt
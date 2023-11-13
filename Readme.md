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

## step-1:Setting up the project environment.
* Install Anaconda Package manager.
* Create a new python environment: conda create --name "env-name" python=3.9
* Run pip install -r requirements.txt

## Step-2: Literature Review.

Plan for literature review:
1. Understanding Video analytics in general by reading some basic papers.
2. Research for SOTA papers for TAL.
3. Research for SOTA papers for STAL.
4. Research for SOTA papers on Action recognition, Object detection.

**Understanding Video analytics in general by reading some basic papers**
1. Zelnik-Manor and Irani, "Event-Based Analysis of Video", CVPR 2001.
2. Zhong, Shi, and Visontai, "Detecting Ununsual Activity in Video
3. Yuen and Torralba, "A data-driven approach for event prediction", ECCV 2010.
4. karpathy, toderici, Shetty, Leung, Sukthankar, and Fei-Fei, "Large-scale Video Classification with Convolutional Neural Networks", CVPR 2014.
5. Simonyan and Zisserman, "Two-Stream Convolutional Networks for Action Recognition in Videos", NeuroIPS 2014.

**Learnings From Event-Based Analysis of video of paper**
<br>
This paper in general explains about the use cases of identifying events in videos and defines 
what an event is and explains about clustering based approach to group similar events in long video 
sequences together using a custom similarity based distance metric.

**Temporal Action Localization**
<br>
**Definition:** Temporal Action localization is the process of determining when a particular
action occurs in a video. in simple terms, given a video and a target action, the task is to
predict the start and end times(or frames) of this action.

**Key Concepts in TAL:**
<br>
1. Action Proposals: These are potential segments in the video where an action might occur. often, the
first step is generate a set of proposals that can be classified into specific action classes.
2. Classification of proposals: once we have proposals, the next step is to classify each proposal into
a specific action class or determine it as background.
---
title: Hip implant classifier
category: Projects
order: 0
year: 2017
thumbsize: 2
tags: [machine learning, prototyping, engineering]
---
# #Hip implant classifier


![Logo Khapto](images/hip implant classifier/thumb.jpg)

A common problem among orthopedic surgeons is the recognition of patients' hip implants through an x-ray. Given the number of implants available in the market, recognizing them becomes a difficult task, especially for traumatologists with few years of experience. That's why, in conjunction with my brother -who is a doctor-, I started to build an application to recognize hip implants.

To achieve a good recognition, I decided to solve 3 tasks:
- Hip implant detector in the image
- Align the implant
- Apply a classifier to the final images
They were solved using CNN's for each task.


![Software workflow](images/hip implant classifier/hip_implant_workflow.jpg)



## Hip implant detector

Detecting the implant in the image was the first task to be solved. For this, the "tensorflow" library was used, and a detector was trained with manually tagged images.

![Hip implant detector](images/hip implant classifier/hip_implant_detector.jpg)

The results of the detector were highly satisfactory

## Hip implant aligner

After obtaining the bounding box of the image, a CNN was trained to find the ends of the implant and thus align the image.

To align the image, the following architecture was used.

![Hip implant aligner architecture](images/hip implant classifier/architecture.jpg)


## Hip classifier

After obtaining a straightened image, a classifier with Google's inception architecture was used.

![Image 3](images/hip implant classifier/final_output.jpg)


## Future work

I am currently testing other architectures and testing filters to improve the accuracy of the model, because CNN's currently identify and learn from other parts of the X-ray that are not of interest (no hip implants).

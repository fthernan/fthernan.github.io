---
title: Hip implant classifier
category: Projects
order: 0
year: 2017
thumbsize: 2
tags: [design, prototyping, engineering]
---
# #Hip implant classifier


![Logo Khapto](images/hip implant classifier/thumb.jpg)

A common problem among orthopedic surgeons is the recognition of patients' hip implants through an x-ray. Given the number of implants available in the market, recognizing them becomes a difficult task, especially for traumatologists with few years of experience. That's why, in conjunction with my brother -who is a doctor-, I started to build an application to recognize hip implants.

To achieve a good recognition, I decided to solve 3 tasks:
- Hip implant detector in the image
- Align the implant
- Apply a classifier to the final images
They were solved using CNN's for each task.


## Hip detector

Detecting the implant in the image was the first task to be solved. For this, the "tensorflow" library was used, and a detector was trained with manually tagged images.

![Image 0](images/hip implant classifier/img0.jpg)

The results of the detector were highly satisfactory

## Hip classifier

![Image 3](images/hip_implants/img00.jpg)

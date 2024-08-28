# Abandoned_baggage_detection
This is a computer vision project which detects when baggage is left undetected.

# Introduction

The project uses a pretrained yolo v8 model. The program detects when a baggage is left unattended and displays it on the screen.

# problem definition

In this project an abandoned baggage is defined as "any baggage which is not in proximity of a person for a predefined number of frames is defined as an abandoned baggage". We have considered 3 test cases for the problem. 
1. when the baggage is left unattended for a period
2. when the baggage is left unattended for a period less than the said amount of time and it comes into proximity again.
3. when the baggage is left unattended for a period and it is classified as abandoned but it comes into proximity again.

# methodology
the model detects baggage and person. then we use a euclidian distance between centers of the bounding boxes to classify if the baggage is in proximity or not. if it is not in poximity a countdown starts when it hits the threshold the baggage is classified as abandoned. it checks again if the baggage ever comes into proximity again. if yes the baggage is declassified.

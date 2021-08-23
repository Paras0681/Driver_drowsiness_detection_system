## Applications
### This can be used by riders who tends to drive the vehicle for a longer period of time that may lead to accidents
## Dependencies
```
 1)import cv2
 2)import immutils
 3)import dlib
 4)import scipy
 5)import playsound
 6)import queue
 7)import time
 8)import sys
 ```
## Description
###  A computer vision system made with the help of opencv that can automatically detect driver drowsiness in a real-time video stream and then play an alarm if the driver appears to be drowsy.
## Algorithm
● We utilised a pre trained frontal face detector from Dlib’s library which is based on  a modification to the Histogram of Oriented Gradients in combination with Linear  SVM for classification.  

● The pre-trained facial landmark detector inside the dlib library is used to estimate  the location of 68 (x, y)-coordinates that map to facial structures on the face. The 68  landmark output is shown in the figure below. However, we utilised the 70 landmark  model.

● We then calculate the aspect ratio to check whether eyes are opened or closed.

● The eye is open if Eye Aspect ratio is greater than threshold. (Around 0.3)

● A blink is supposed to last 200-300 milliseconds.

● A drowsy blink would last for  800-900  ms. 

## Execution
To run the code, run 

```
python blinkDetect.py
```
=======
# Driver_drowsiness_detection_system
**Drowsiness of the drivers is the main cause of accidents in the world as well as India. Due to lack of sleep and tiredness, drowsiness can occur while driving. The best way to avoid accidents caused by drivers’ drowsiness is to detect drowsiness of the driver and warn him before fall into sleep. To detect drowsiness many techniques like eye retina detection, facial feature recognition has been used. Here in this report, we propose a method of detecting driver drowsiness using eye retina detection of the driver. In this report, we propose a more accurate drowsiness detection method which is a hybrid approach of eye retina detection .**

# First it detects the eyes on the screen
![Output2](https://user-images.githubusercontent.com/77244089/130503712-a6a52cf8-e595-48de-9ddc-d2051ed9dd35.png)

# Then calulates the limit for blinking eyes normally
![Output3](https://user-images.githubusercontent.com/77244089/130503713-359c24f3-12de-4d97-adff-6623caf4878e.png)

# Then starts the count of blinking from zero along with time limit
![Output4](https://user-images.githubusercontent.com/77244089/130503715-0ed61c8c-6d29-42b3-aec2-c7cabee23b76.png)

# If the count increase raises an alert!!
![Output5](https://user-images.githubusercontent.com/77244089/130503718-5864f967-22a5-4b44-a036-ee5f3f6079b1.png)
![Output6](https://user-images.githubusercontent.com/77244089/130503719-0854b189-2e38-4dc8-8f37-677d38bdb7f9.png)

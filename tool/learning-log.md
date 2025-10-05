# Tool Learning Log

## Tool: **OpenCV, Swift, TensorFlow, MediaPipe**

## Project: **Cat Cam**



OpenCV has a full course on freecodecamp which ill link [here](https://www.freecodecamp.org/news/opencv-full-course/); its a source that interprets and manipulates images, some essential functions include 

```python
import cv2 as cv

image = cv.imread('Img/Cat.jpg') //this reads the image sourced from your files 

cv.imshow('Cat', img) //this shows it on a new window

cv.waitKey(0) 
```

```python
capture = cv.VideoCapture(0) //connects to webcam via int 0, but in the parantheses youd usually put the link to a video already existing//

while True;
  isTrue, frame = capture.read //this line reads the video frame by frame as it runs//
cv.imshow('video', frame)

if.cv.waitKey(20) & 0xFF==ord('d'): //in order to stop the video from playing indefinetly, we stop the video when d is pressed; which wont be needed in the case of my freedom project but is good to know//
    break
capture.release()
cv.destroyAllWindows() 

cv.waitKey(0) 
```

Whats great is that with these two functions we learn at the beginning of the video, im already recognizing a way that it can be connected or repurposed to my freedom project. For my next log id like to aim to testing this out with my computer webcam and testing if i can run the video in a new window. 

### X/X/XX:
* Text

### X/X/XX:
* Text


<!-- 
* Links you used today (websites, videos, etc)
* Things you tried, progress you made, etc
* Challenges, a-ha moments, etc
* Questions you still have
* What you're going to try next
-->

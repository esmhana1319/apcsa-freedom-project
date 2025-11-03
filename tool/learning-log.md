# Tool Learning Log

## Tool: **OpenCV, Swift, TensorFlow, MediaPipe**

## Project: **Cat Cam**

### 10/4/25

OpenCV has a full course on freecodecamp which ill link [here](https://www.freecodecamp.org/news/opencv-full-course/); its a source that interprets and manipulates images

```python
import cv2 as cv

image = cv.imread('Img/Cat.jpg') #this reads the image sourced from your files 

cv.imshow('Cat', img) #this shows it on a new window

cv.waitKey(0) 
```

```python
capture = cv.VideoCapture(0) #connects to webcam via int 0, but in the parantheses youd usually put the link to a video already existing

while True;
  isTrue, frame = capture.read #this line reads the video frame by frame as it runs//
cv.imshow('video', frame)

if.cv.waitKey(20) & 0xFF==ord('d'): #in order to stop the video from playing indefinetly, we stop the video when d is pressed; which wont be needed in the case of my freedom project but is good to know//
    break
capture.release()
cv.destroyAllWindows() 

cv.waitKey(0) 
```

Whats great is that with these two functions we learn at the beginning of the video, im already recognizing a way that it can be connected or repurposed to my freedom project. For my next log id like to aim to testing this out with my computer webcam and testing if i can run the video in a new window. 

### 11/2/25

the great news is that i successfully downloaded tensorflow on my device, but the bad news is i have less than 5% of storage left. On a better note, tensorflow has a lot of available resources to go off of. 

the one i am using at the moment is [geeksforgeeks](https://www.geeksforgeeks.org/deep-learning/tensorflow/) 

tensors are fundamental data structures that can represent multidimensional arrays like this

```
[[],[],
[],[]}
```

they can be Scalars (0) , Vectors (1) , Matrices (2) , and higher dimensional arrays (>2); A 2x3 matrix will contain 2 rows 3 columns 

A lot of the skills we learnt in SEP11 are paramount to Tesor indexing, such as methods used for slicing and inserting. 

For instance say we had this array; 

```python
import tensorflow as tf
t1 = tf.constant([0, 1, 2, 3, 4, 5, 6, 7])
t1
```

in order to slice, wed use 
```python 
s1 = tf.slice(t1, begin=[start#], size=[stop#])
```
or 
```python
s1 = t1[start#:stop#]
```






<!-- 
* Links you used today (websites, videos, etc)
* Things you tried, progress you made, etc
* Challenges, a-ha moments, etc
* Questions you still have
* What you're going to try next
-->

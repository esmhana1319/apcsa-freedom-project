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

### 11/16/25

some good news is that ive been learning python in my weekly meetings with Girls.incs coding bootcamp; some bad news is that we are so behind we havent started on making our own ai yet. Have i been misdirected or am i just impatient? Im not sure exactly but lets get started with some Mediapipe!!

I downloaded mediapipe to my terminal via ```pip install mediapipe``` led by [this website](https://pypi.org/project/mediapipe/) and [MediaPipes python framework](https://chuoling.github.io/mediapipe/getting_started/python_framework.html) section that had some really good pointers

<img width="730" height="638" alt="Screenshot 2025-11-16 at 9 54 38 PM" src="https://github.com/user-attachments/assets/af9c4700-bc7d-4eb7-b31b-c8e1ce4b899c" />

one of the code snippets that stook out to me here was 

```python
create_image_frame(format=ImageFormat.SRGB,data=mat) 
```

Similar to OpenCV, MediaPipe also works with videos, and Image Frames are their container for a video or picture. In order to get the pixel data for arrays you can use 

```python
image_frame.numpy_view()
```

One thing to note for the future is that downloading mediapipe took up a lot more of my space alongside tensor flow, if theres any alternative ways i could free up space ill look into them soon. 

### 12/7/25 

I looked into an alternate way to do my project without taking up as much space in the ide that i use for my APCSA assignments from our meetings in the coding bootcamp i signed up for. Currently we are using VSCODE, which i connected to my github account and am teaching myself the wraps of. The great news is that its extremely similar to cs50s IDE despite having a couple different shortcuts. 

As for what ive recently took notes on during said meetings, weve been delving into the AI side and will probably start coding our own in the next sessions. 

Models learn from datasets, which are a collection of labeled examples. 
ie, if you're training an AI to recognize cats in my case, the dataset would contain images of cats labeled as "cat" and images of things other than cats labeled as "not cats."
When the computer gives a wrong answer, it does a calculation on how to adapt to be less wrong over time. 

Different algorithms are used for learning and their common goal is to minimize the error between the model's predictions and the actual labels in the training data. The Ai will make predictions and a function will measure the difference between these predictions and the correct answers. It will constantly adapt to these parameters to reduce the chance of it being  wrong; AI learning 

Iteration, refinement and creating successful datasets are the main things i should focus on in future logs. My aim overall for this project is to make an ai that can recognize my cats behavior, i can focus on outputting that in a user friendly format later on. 


On a positive note, Vidhi and Copeland are great networks to expand my knowledge on this stuff, i plan to send an email their way if the meetings we have later on are a bit slow so i can manage my time wisely and get ahead on information regarding more resources that can help me build an Machine Learning Model as a complete noob to the concept. 

3/21/26

Ive been learning how to draw, preview images, and webcam footage via openCV. Suprisingly the only frustrating part was installing and making sure everything ran on vscode, but after that was dealt with, everything was smooth from there on! 

Recap on how to preview an img with opencv 

```python
import cv2 
import numpy as np

img = cv2.imread('photos/cat.jpg')


cv2.imshow('Cat', img)
cv2.waitKey(0)
cv2.destroyAllWindows()
```
<img width="767" height="745" alt="Screenshot 2026-03-21 at 5 57 39 PM" src="https://github.com/user-attachments/assets/4ce0bbdd-7568-4ed1-ba11-4f880189f2b7" />

How to make a rectangle in open cv 

```python
cv2.rectangle(blank, (0,0), (250,500), (255,0,0), thickness=4)
cv2.imshow('rectangle2', blank)
cv2.waitKey(0)
cv2.destroyAllWindows() 
```
How to make a square in open cv 

```python
cv2.rectangle(blank, (0,0), (250,250), (255,0,0), thickness=4)
cv2.imshow('rectangle2', blank)
cv2.waitKey(0)
cv2.destroyAllWindows() 
```

How to make a circle in open cv 

```python
blank = np.zeros((500, 500, 3), dtype='uint8')
cv2.circle(blank, (250,250), 40, (0,0,255), thickness=-1)
cv2.imshow('circle', blank)
cv2.waitKey(0)
cv2.destroyAllWindows()
```
<img width="1420" height="773" alt="Screenshot 2026-03-21 at 5 24 52 PM" src="https://github.com/user-attachments/assets/398f39df-aecf-408d-9cb5-bfd42200749e" />

Recap on how to preview webcam footage 

```python
import numpy as np
import cv2

cap = cv2.VideoCapture(0)

while True: 
    success,frame=cap.read() 
    if success:
        cv2.imshow('Video',frame)

    if cv2.waitKey(1) & 0xFF == ord('e'):
        break 

cap.release() 
cv2.destroyAllWindows()
```

<img width="1395" height="720" alt="Screenshot 2026-03-21 at 5 11 32 PM" src="https://github.com/user-attachments/assets/629fc38b-9f22-4fff-931c-9fac231faaf5" />


<!-- 
* Links you used today (websites, videos, etc)
* Things you tried, progress you made, etc
* Challenges, a-ha moments, etc
* Questions you still have
* What you're going to try next
-->

# Entry 4
##### 3/21/26

### What ive been focusing on with building my MVP

As i previously mentioned, my objective was to build a mockup 'security camera' that could watch my cats and possibly give input on their behavior. One of the tools im using to create this, OPENCV, works to give live computer visuals and previews alongside propelling image processing and machine learning. 

Recently ive been busy with the process of moving!! Although i havent been able to tinker as much, i picked up on something cool recently. While living in my current apartment, we havent had to worry much about the security aspect of residency (we live on the top story, and are fortunate to not have a break in happen like last time). On the contrary, the place im moving to finally got security cameras installed for our front, side, and backdoors. This is all previewed on a monitor we placed on the second floor, which reminded me that OPENCV can serve a similar function. 

Previously, ive made progress with learning python and opencvs functions with FreeCodeCamps course on youtube that dives into the basics all the way to the AI recognition aspect of opencv. 

So far ive learned to preview images, drawings, and finally webcam footage. Ive listed this in my learning log but id like to go more in depth on my process and challenges here, since i deffo made some silly mistakes 

Recap on how to preview an img with opencv - i already learned this while tinkering before, but demoing it in my own ide was something i hadnt done just yet as at the time i had no space to install within my cs50 ide. Getting used to how to run thinga in vscode was a bit unfamiliar but went swell. 

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

I did this one entirely by accident when they were showcasing how to make a square in the video. I notice they do this pretty quick without detailing what information was what, so because i made this little whoopsie, i was able to dumb things down to which numbers were coordinates, size, and color (1 2 and 3 respectively). In setting thickness to =-1 instead of =1 i got to learn that -1 could also sub as filling the drawing entirely 

How to make a square in open cv 

```python
cv2.rectangle(blank, (0,0), (250,250), (255,0,0), thickness=-1)
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

If you ignore my pajamas in the picture i will thank you spiritually. I had a bit of trouble getting this code to run, and im still unsure as to why my previous code wasnt working, but my general idea might be that certain parts of my code using methods like waitKey() were capitalized or spelt incorrectly (when i corrected this and changed the value to 1 and not 0 it seemed to work properly). 

My next objective, especially for monday 23rd, is seeing if i can overlay drawings on the webcam footage (to satiate my curiosity) aswell as dive into the next parts of the video that detail face recognition and deep computer vision




[Previous](entry03.md) | [Next](entry05.md)

[Home](../README.md)

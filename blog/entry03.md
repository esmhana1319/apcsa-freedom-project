# Entry 3
##### 2/8/26

### What ive been up to so far with tinkering: 

My previous motto from the last entry was to focus full throttle on tensor flow, atleast dedicating a day to learning more on how to code a Machine Learning Model. Over the weekend that i had free i chose to do a couple things i had spoken about in previous learning logs. 

1. I was running out of space in the codespace for SEP on css.dev so i moved all of the freedom project related things to my codespace in vscode; we have been using this during meetings with Marguerite and Vidhi and it worked wonders at being a good alternative

2. I got started on learning about Linear regression and how to predict future data via line of best fit and tensor flow. This is the one of the first things thats gone over in the FCC course on tensor flow, and prior to this they teach us about installation, tensor variables and constants, aswell as a couple methods used to reshape and interpret data within tensors.

For instance, our first initial tensor is filled of one list, with two lists inside, and three elements. When we reshape it and set its value to tensor2, we have two lists, with three lists inside, and one element in each. For the third tensor -1 is used to interpret the missing number; ie if we have a total of three lists, the only number that would fit here is 2, making 2 elements within the three lists. Its essentially all multiplication which is nice 

```python
tensor1 = tf.ones ([1,2,3]) 
tensor2 = tf.reshape(tensor1, [2,3,1])
tensor3 = tf.reshape(tensor2, [3, -1])

print (tensor1)
print (tensor2)
print (tensor3)
```

```python
tf. Tensor (
[[1. 1. 1.]
[1. 1. 1.]]], shape=(1, 2, 3), dtype=float32)
tf. Tensor(
[[[1.]
[1.]
[1. ]]
[[1.]
[1. ]
[1.]]], shape=(2, 3, 1), dtype=float32)
tf. Tensor(
[[1. 1.]
[1. 1.]
[1. 1.]], shape=(3, 2), dtype=float32)
```

After this we quickly move on to linear regression models, which are primarily based on a dataset which determines the line of best fit. 

<img width="359" height="267" alt="Screenshot 2026-02-08 at 3 42 40 PM" src="https://github.com/user-attachments/assets/a6351f25-2bcc-4d1d-85ac-9c8d02b817fb" />

<img width="749" height="771" alt="Screenshot 2026-02-08 at 1 46 00 PM" src="https://github.com/user-attachments/assets/3bac6bb1-6d1e-4ccf-98f0-4d36bcfd8df6" />

Here was where i ran into my first couple issues where i had to install certain things into vscode terminal in order to properly import them in my py file. What i wasnt able to solve though was gaining access to the colab dataset used within the linear regression course shown below.  

<img width="595" height="507" alt="Screenshot 2026-02-08 at 1 51 59 PM" src="https://github.com/user-attachments/assets/9c2a18aa-98a9-4cb0-8666-f0100143fbd7" />

I tried a couple different datasets out to see if theyd work but encountered the same error, for a future log id like to demo this model with my own data set and see if i can incorporate what i learn here into something ill use for my projects model. 


### Sources 

##### Previous 
1. [Swift](https://developer.apple.com/ios/get-started/) Documentation; this is where i got to learn how it works and what kind of things i can create with this tool.

2. [OpenCV](https://docs.opencv.org/4.x/d0/d3d/tutorial_general_install.html) Documentation; ive been using [freecodecamps course](https://www.freecodecamp.org/news/opencv-full-course/) to learn the wraps of how it works along with their youtube tutorials

3. [MediaPipe](https://ai.google.dev/edge/mediapipe/solutions/guide) Documentation; Aswell as [this website](https://chuoling.github.io/mediapipe/) which ive been using to get started

4. [TensorFlow](https://www.tensorflow.org/) Documentation, along with [this website](https://www.geeksforgeeks.org/python/introduction-to-tensorflow/) that ive been using to get the hang of it

5. VSCODE - this is the ide we have been using during meetings to work with ai
   
6. GROQ - the website we have been using to access and create api keys that can be used within our code
   
7. [NeuralNine](https://www.youtube.com/watch?v=72s6hJwyfDg)  and  [FireShips](https://youtu.be/PeMlggyqz0Y?si=-9MhlJIidMM3NJRe)  crash course videos on TensorFlow and Machine Learning Models 

##### Current 

8. [stack overflow](https://stackoverflow.com) has helped me significantly in learning how to debug certain errors id come across as well as find good alternatives throughout the process 

9. [Free Code Camps video on TensorFlow](https://www.youtube.com/watch?v=tPYj3fFJGjk&t=4769s) which is a 7 hour long course on making a machine learning model with TensorFlow

10. [Standford Universitys dataset on titanic survival](titanic.csv) which i used as a temporary alternative to the one provided by google which was blocked on my school computer 
    
### EDP 

The steps of the Engineering and design process consist of... 

#### 1. Defining the problem [x]
   
#### 2.Research the problem [x]

#### 3.Brainstorm possible solutions [x]

#### 4.Plan the most promising solution [x]

#### 5.Create a prototype [x]

#### 6.Test and evaluate the prototype [ ] 

#### 7.Improve as needed [ ]

#### 8.Communicate the results [ ]

   Currently, i am on step 5. I brainstormed solutions and have begun creating prototypes

  ### Skills 

   A skill ive developed here was debugging. I encountered a lot of bugs along my way and scrounging my terminal and stack overflow for solutions taught me that theres always an alternative way to go about something. 
```
developed skill *-*-*-*-*-*-*-*-*-*-*-*-*-*-*-*-*-*-*-*-*-*-*-*-*-*
  debugging lvl 5
-*-*-*-*-*-*-*-*-*-*-*-*-*-*-*-*-*-*-*-*-*-*-*-*-*-*-*-*-*-*-*-*-*-
```
   Another skill ive developed was finding alternatives. Colab was sadly blocked on my school computer, so following the course video seemed to be a little bit harder than i anticipated. I explored a lot of different websites to source different datasets to work with when the one provided in the video was inaccessible.  
```
developed skill *-*-*-*-*-*-*-*-*-*-*-*-*-*-*-*-*-*-*-*-*-*-*-*-*-*-*
  Finding alternatives lvl 4
-*-*-*-*-*-*-*-*-*-*-*-*-*-*-*-*-*-*-*-*-*-*-*-*-*-*-*-*-*-*-*-*-*-*-
```

[Previous](entry02.md) | [Next](entry04.md)

[Home](../README.md)

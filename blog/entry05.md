# Entry 5
##### 4/26/26

### Building my MVP (struggles I had alongside their respective solutions) 

My biggest struggle with my making my final MVP was that i didnt know what i wanted the bare bones of my program to look like. I think i spent the most of the spring break trying to jump ahead to getting my program to identify what was on the screen when it couldnt properly track them yet. After scrolling through tutorials, failing to download different models of YOLO, and scanning what webcams to buy (im thinking about raspberryPi right now but thats a hill ill cross after the show (may 1st and 2nd 6:30 tickets are five dollars shh)), i finally settled on just making a program that would utilize two skills i focused on learning that i documented during my last blog. 

Making a bounding box and previewing webcam footage with OPENCV were two things i had learned how to do already. My next step, and the bare bones for my MVP were utilizing those two skills to make a program that can track a selected object on screen. Initially, as i mentioned earlier, i wanted to use either raspberryPi or YOLOv8 to do this with an already programmed tracking model. This would make the overall process much easier as both programs are good for tracking animals (YOLOv8 from what i know does this swellingly). The Mac i am currently working on though, and my ide were unfortunately not compatible with YOLOv8 or YOLOv11; i tried two methods of dowload, tried torch n anaconda to create environments where itd work but on the time crunch i was on this led me into a bad loophole that just wouldnt really work out by deadline day. 

The solution i came across was one of the pre-built in trackers with OPENCV, CSRT which i dropped in a tracker var to be used on my capture var ( 0 for the webcam) like this 

```python
tracker = cv2.TrackerCSRT_create()

cap = cv2.VideoCapture(0) 
```

The first instance i had to be aware of was if the footage was unreadable and couldnt be opened, which is signified by the boolean success

```python
success, frame = cap.read()
if not success:
    print("Could not open video")
    exit()
```

Next, with selectROI the user can pic a frame of interest to make a box around, which is represented by the variable bbox 

```python
bbox = cv2.selectROI("Tracking", frame, False)
tracker.init(frame, bbox)
```

initially though i was very confused about the footage freezing to one frame, aswell as being incredibly slow, so i added an aspect to my loop that could break if frames werent read and showcase the framerate; this is represented by the variables timer fps and .getTickCount and .getTickFrequency 

```python
if success:

        p1 = (int(bbox[0]), int(bbox[1]))
        p2 = (int(bbox[0] + bbox[2]), int(bbox[1] + bbox[3]))
        cv2.rectangle(frame, p1, p2, (255, 0, 0), 2, 1)

#theres an else statement in between these two snippets that ill show below here 

 cv2.putText(frame, f"FPS: {int(fps)}", (100, 50), 
                cv2.FONT_HERSHEY_SIMPLEX, 0.7, (50, 170, 50), 2)
    
    cv2.imshow("Tracking", frame)
```

the else statement between these would account for if footage was lost, which i could demo easily by swiping the cover on my webcamera (its this cool sticker that i placed ONLY because im very paranoid, love it though) 

```python
else:
        cv2.putText(frame, "Tracking Lost", (100, 80), 
                    cv2.FONT_HERSHEY_SIMPLEX, 0.7, (0, 0, 255), 2)
```

and the final lines which are dedicated to stopping the footage were something i demoed before in a previous blog 

```python
if cv2.waitKey(1) & 0xFF == ord('q'):
        break

cap.release()
cv2.destroyAllWindows()
```

Altogether it made a program that ran like this 
<img width="1154" height="689" alt="Screenshot 2026-04-26 at 5 29 47 PM" src="https://github.com/user-attachments/assets/33ab95c5-e923-42a0-b353-2c1020a41649" />

(the footage exceeds 10mb so i will simply have to explain that in the video the bounding box selected on the perfume bottle follows it as i move it across the screen) 






[Previous](entry04.md) | [Next](entry06.md)

[Home](../README.md)

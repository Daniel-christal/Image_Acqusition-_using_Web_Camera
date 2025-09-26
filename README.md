## Image_Acqusition-_using_Web_Camera:
# Name:DANIEL C
# REG NO:212223240023

# Aim:
 
To write a python program using OpenCV to capture the image from the web camera and do the following image manipulations.

i) Write the frame as JPG 

ii) Display the video 

iii) Display the video by resizing the window

iv) Rotate and display the video

## Software Used
Anaconda - Python 3.7
## Algorithm
### Step 1:
Use cv2.VideoCapture(0) to access web camera.



### Step 2:
Use cv2.imread to read the video or image.


### Step 3:
Use cv2.imwrite to save the image.


### Step 4:Use cv2.imshow to show the video.



### Step 5:
End the program and close the output video window by pressing 'q'.


## Program:
``` Python
### Developed By:Daniel C
### Register No:212223240023

## i) Write the frame as JPG file
```
import cv2
import numpy as np
viedoCaptureObject=cv2.VideoCapture(0)
ret,frame=viedoCaptureObject.read()
cv2.imwrite("captured_frame.jpg",frame)
viedoCaptureObject.release()
cv2.destroyAllWindows()
```



## ii) Display the video
```
cap = cv2.VideoCapture(0)
ret, frame = cap.read()
cv2.imshow('captured_frame', frame)
cv2.waitKey(10000)
cap.release()
cv2.destroyAllWindows()
```



## iii) Display the video by resizing the window
```
cap=cv2.VideoCapture(0)
ret,frame=cap.read()
width=int(cap.get(3))
height=int(cap.get(4))
image=np.zeros(frame.shape,np.uint8)
smaller_frame=cv2.resize(frame,(0,0),fx=0.5,fy=0.5)
image[:height//2, :width//2]=smaller_frame
image[height//2:, :width//2]=smaller_frame
image[:height//2, width//2:]=smaller_frame
image[height//2:, width//2:]=smaller_frame
cv2.imshow('',image)
cv2.waitKey(5000)  
image_dict = {'captured_image1': image}
cv2.imwrite('captured_image1.jpg', image)
cap.release()
cv2.destroyAllWindows()
```


## iv) Rotate and display the video

```
cap=cv2.VideoCapture(0)
ret,frame=cap.read()
width=int(cap.get(3))
height=int(cap.get(4))
image=np.zeros(frame.shape,np.uint8)
smaller_frame=cv2.resize(frame,(0,0),fx=0.5,fy=0.5)
image[:height//2, :width//2]=cv2.rotate(smaller_frame,cv2.ROTATE_180)
image[height//2:, :width//2]=smaller_frame
image[:height//2, width//2:]=cv2.rotate(smaller_frame,cv2.ROTATE_180)
image[height//2:, width//2:]=smaller_frame
cv2.imshow('',image)
cv2.waitKey(5000) 
image_dict = {'captured_image2': image}
cv2.imwrite('captured_image2.jpg', image)
cap.release()
cv2.destroyAllWindows()
```
# Output

## i) Write the frame as JPG image
<img width="727" height="540" alt="image" src="https://github.com/user-attachments/assets/8b8e23b1-375d-46a6-8f1c-87058ae660b9" />



### ii) Display the video
<img width="752" height="632" alt="image" src="https://github.com/user-attachments/assets/c7ca6460-2779-41c9-b63c-55c527272dce" />



### iii) Display the video by resizing the window
<img width="732" height="538" alt="image" src="https://github.com/user-attachments/assets/44d9a6db-eb7a-40f4-a65f-79986d3eb0e9" />




### iv) Rotate and display the video
<img width="722" height="541" alt="image" src="https://github.com/user-attachments/assets/345704f9-0611-4811-99e7-f8df8830401b" />






## Result:
Thus the image is accessed from webcamera and displayed using openCV.

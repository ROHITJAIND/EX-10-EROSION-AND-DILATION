# EX-10 EROSION AND DILATION
### Aim
To implement Erosion and Dilation using Python and OpenCV.
### Software Required
Anaconda - Python 3.7 , OpenCV
### Algorithm:
- Step1: Import the necessary packages.
- Step2: Read the image.
- Step3: Create the structuring element or kernal element.
- Step4: Use Opening Operation.
- Step5: Use Closing Operation.

Developed By: ROHIT JAIN D
Register No: 212222230120<br>
### Program:
- Importing the necessary packages
  ``` Python
  import cv2
  import numpy as np
  ```
- Create the Text using cv2.putText.
  ```Python
  img1=np.zeros((100,500),dtype="uint8")
  font=cv2.FONT_HERSHEY_PLAIN
  cv2.putText(img1,"ROHIT JAIN D 212222230120",(5,60),font,2,(255),5,cv2.LINE_AA)
  cv2.imshow("Original Image",img1)
  cv2.waitKey(0)
  ```
  <img height=10% width=80% src="https://github.com/ROHITJAIND/EX-10-EROSION-AND-DILATION/assets/118707073/4d241402-e96a-4c28-9017-30946f815cfc">
- Create the structuring element.
  ```Python
  kernel=np.ones((5,5),np.uint8)
  kernel1=cv2.getStructuringElement(cv2.MORPH_CROSS,(7,7))
  ```
- Erode the image.
  ```Python
  cv2.erode(img1, kernel)
  image_erode = cv2.erode(img1,kernel1)
  cv2.imshow("Erode Image",image_erode)
  cv2.waitKey(0)
  ```
  <img height=10% width=80% src="https://github.com/ROHITJAIND/EX-10-EROSION-AND-DILATION/assets/118707073/f062aabb-dd88-4eab-9963-0fd1746e71b0">
- Dilate the image.
  ```Python
  image_dilatel=cv2.dilate(img1,kernel1)
  cv2.imshow("Dilate Image",image_dilatel)
  cv2.waitKey(0)
  ```
  <img height=10% width=80% src="https://github.com/ROHITJAIND/EX-10-EROSION-AND-DILATION/assets/118707073/c17f47e8-7d8c-4efe-85a1-254e4cd1b186">

### Result
Thus the generated text image is eroded and dilated using python and OpenCV.

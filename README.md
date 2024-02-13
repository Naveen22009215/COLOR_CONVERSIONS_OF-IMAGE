# COLOR_CONVERSIONS_OF-IMAGE
## AIM
To write a python program using OpenCV to do the following image manipulations.

i) Read, display, and write an image.

ii) Access the rows and columns in an image.

iii) Cut and paste a small portion of the image.

iv)To perform the color conversion between RGB, BGR, HSV, and YCbCr color models.


## Software Required:
Anaconda - Python 3.7
## Algorithm:
### Step1: Choose an image and save it as a filename.jpg ,
### Step2: Use imread(filename, flags) to read the file.
### Step3: Use imshow(window_name, image) to display the image.
### Step4: Use imwrite(filename, image) to write the image.
### Step5: End the program and close the output image windows.
### Step6: Convert BGR and RGB to HSV and GRAY
### Step7: Convert HSV to RGB and BGR
### Step8: Convert RGB and BGR to YCrCb
### Step9: Split and Merge RGB Image
### Step10: Split and merge HSV Image

##### Program:
```
### Developed By: Naveen Kumar P
### Register Number: 212222230092
```
<table>
  <tr>
    <td width=50%>

### i) Read and display the image
```Python
    import cv2
    image=cv2.imread('dip1.jpg',1)
    image=cv2.resize(image,(400,300))
    cv2.imshow('NAVEEN',image)
    cv2.waitKey(0)
    cv2.destroyAllWindows()
``` 
  </td>
  <td>

### OUTPUT:

 <img src="https://github.com/Naveen22009215/COLOR_CONVERSIONS_OF-IMAGE/assets/119401470/05f9998b-0f59-492f-bd43-54e5c67c7725">
  </td>
  </tr>

   <tr>
    <td width=50%>

### ii)Write the image
```Python
    import cv2
    image=cv2.imread('dip1.jpg',0)
    cv2.imwrite('demos.jpg',image)
```
  </td>
  <td>

### OUTPUT:

<img src="https://github.com/Naveen22009215/COLOR_CONVERSIONS_OF-IMAGE/assets/119401470/da85973f-9922-427d-b74e-29262f90aea2">
  </td>
  </tr>
  <tr>
    <td width=50%>

### iii)Shape of the Image
```Python
    import cv2
    image=cv2.imread('dip1.jpg',1)
    print(image.shape)
```
  </td>
  <td>

### OUTPUT:
<img src="https://github.com/Naveen22009215/COLOR_CONVERSIONS_OF-IMAGE/assets/119401470/ed9740ba-390c-4e90-8a02-617cadcd87f3">
  </td>
  </tr>
  <tr>
    <td>
      
### iv)Access rows and columns
```Python
    import random
    import cv2
    image=cv2.imread('dip1.jpg',1)
    image=cv2.resize(image,(400,400))
    for i in range (150,200):
      for j in range(image.shape[1]):
          image[i][j]=[random.randint(0,255),
                       random.randint(0,255),
                       random.randint(0,255)] 
    cv2.imshow('part image',image)
    cv2.waitKey(0)
    cv2.destroyAllWindows()
```
  </td>
  <td width="50%">

### OUTPUT:

 <img src="https://github.com/Naveen22009215/COLOR_CONVERSIONS_OF-IMAGE/assets/119401470/d65ad6a0-623e-49da-acea-9da7c6e6ee2b">
  </td>
  </tr>
  <tr>
    <td width=50%>
      
### v)Cut and paste portion of image

 ```Python
    import cv2
    image=cv2.imread('dip1.jpg',1)
    image=cv2.resize(image,(400,400))
    tag =image[130:200,110:190]
    image[110:180,120:200] = tag
    cv2.imshow('partimage1',image)
    cv2.waitKey(0)
    cv2.destroyAllWindows()
```
  </td>
  <td>
    
### OUTPUT:

<img src="https://github.com/Naveen22009215/COLOR_CONVERSIONS_OF-IMAGE/assets/119401470/ea812db9-7224-46ff-843f-b8678d77c381">
  </td>
  </tr>
</table>

### vi) BGR and RGB to HSV and GRAY
```Python
import cv2
img = cv2.imread('dip1.jpg',1)
img = cv2.resize(img,(300,200))
cv2.imshow('Original Image',img)
hsv1 = cv2.cvtColor(img,cv2.COLOR_BGR2HSV)
cv2.imshow('BGR2HSV',hsv1)
hsv2 = cv2.cvtColor(img,cv2.COLOR_RGB2HSV)
cv2.imshow('RGB2HSV',hsv2)
gray1 = cv2.cvtColor(img,cv2.COLOR_BGR2GRAY)
cv2.imshow('BGR2GRAY',gray1)
gray2 = cv2.cvtColor(img,cv2.COLOR_RGB2GRAY)
cv2.imshow('RGB2GRAY',gray2)
cv2.waitKey(0)
cv2.destroyAllWindows()
```

### OUTPUT:
![WhatsApp Image 2024-02-13 at 08 59 05_8fb1f6ec](https://github.com/Naveen22009215/COLOR_CONVERSIONS_OF-IMAGE/assets/119401470/ec22f334-4ebc-4724-a007-0a58559b42e9)


### vii) HSV to RGB and BGR
```Python
import cv2
img = cv2.imread('dip1.jpg')
img = cv2.resize(img,(300,200))
img = cv2.cvtColor(img,cv2.COLOR_BGR2HSV)
cv2.imshow('Original HSV Image',img)
RGB = cv2.cvtColor(img,cv2.COLOR_HSV2RGB)
cv2.imshow('2HSV2BGR',RGB)
BGR = cv2.cvtColor(img,cv2.COLOR_HSV2BGR)
cv2.imshow('HSV2RGB',BGR)
cv2.waitKey(0)
cv2.destroyAllWindows()
```

### OUTPUT:
![WhatsApp Image 2024-02-13 at 08 59 05_3feae25e](https://github.com/Naveen22009215/COLOR_CONVERSIONS_OF-IMAGE/assets/119401470/b79af7ce-6b84-43f4-abc2-582414132bdf)


### viii) RGB and BGR to YCrCb
```Python
import cv2
img = cv2.imread('dip.jpg')
img = cv2.resize(img,(300,200))
cv2.imshow('Original RGB Image',img)
YCrCb1 = cv2.cvtColor(img, cv2.COLOR_BGR2YCrCb)
cv2.imshow('RGB-2-YCrCb',YCrCb1)
YCrCb2 = cv2.cvtColor(img, cv2.COLOR_RGB2YCrCb)
cv2.imshow('BGR-2-YCrCb',YCrCb2)
cv2.waitKey(0)
cv2.destroyAllWindows()
```

### OUTPUT:

![WhatsApp Image 2024-02-13 at 09 28 41_1bf79f18](https://github.com/Naveen22009215/COLOR_CONVERSIONS_OF-IMAGE/assets/119401470/095ba90b-c5a9-4a37-b364-5990d8a4af9d)


### ix) Split and merge RGB Image
```Python
import cv2
img = cv2.imread('dip1.jpg',1)
img = cv2.resize(img,(300,200))
R = img[:,:,2]
G = img[:,:,1]
B = img[:,:,0]
cv2.imshow('R-Channel',R)
cv2.imshow('G-Channel',G)
cv2.imshow('B-Channel',B)
merged = cv2.merge((B,G,R))
cv2.imshow('Merged RGB image',merged)
cv2.waitKey(0)
cv2.destroyAllWindows()
```

### OUTPUT:
![WhatsApp Image 2024-02-13 at 08 59 05_f4557b1a](https://github.com/Naveen22009215/COLOR_CONVERSIONS_OF-IMAGE/assets/119401470/45aebb97-c49c-438c-b5c2-06aeb8bd1049)


### x) Split and merge HSV Image
```Python
import cv2
img = cv2.imread("dip1.jpg",1)
img = cv2.resize(img,(300,200))
img=cv2.cvtColor(img,cv2.COLOR_RGB2HSV)
H,S,V=cv2.split(img)
cv2.imshow('Hue',H)
cv2.imshow('Saturation',S)
cv2.imshow('Value',V)
merged = cv2.merge((H,S,V))
cv2.imshow('Merged',merged)
cv2.waitKey(0)
cv2.destroyAllWindows()
```

### OUTPUT:

![WhatsApp Image 2024-02-13 at 08 59 06_0cc2e66d](https://github.com/Naveen22009215/COLOR_CONVERSIONS_OF-IMAGE/assets/119401470/c44cac90-6749-4800-aa5b-bd0cb390362b)


## Result:
Thus the images are read, displayed, and written ,and color conversion was performed between RGB, HSV and YCbCr color models successfully using the python program.








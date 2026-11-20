# Image-Handling-and-Pixel-Transformations-Using-OpenCV 

## AIM:
Write a Python program using OpenCV that performs the following tasks:

1) Read and Display an Image.  
2) Adjust the brightness of an image.  
3) Modify the image contrast.  
4) Generate a third image using bitwise operations.

## Software Required:
- Anaconda - Python 3.7
- Jupyter Notebook (for interactive development and execution)

## Algorithm:
### Step 1:
Load an image from your local directory and display it.

### Step 2:
Create a matrix of ones (with data type float64) to adjust brightness.

### Step 3:
Create brighter and darker images by adding and subtracting the matrix from the original image.  
Display the original, brighter, and darker images.

### Step 4:
Modify the image contrast by creating two higher contrast images using scaling factors of 1.1 and 1.2 (without overflow fix).  
Display the original, lower contrast, and higher contrast images.

### Step 5:
Split the image (boy.jpg) into B, G, R components and display the channels

## Program Developed By:
- **Name:** MIDHUN S 
- **Register Number:** 212224230158

  ### Ex. No. 01

1. Read the image ('Eagle_in_Flight.jpg') using OpenCV imread() as a grayscale image.
```PYTHON
import cv2
import matplotlib.pyplot as plt
```

Read the image using OpenCV
```
img = cv2.imread('VIN.jpeg', cv2.IMREAD_COLOR)
```
Convert BGR (OpenCV's default) to RGB (Matplotlib's expected color order)#
```
img_rgb = cv2.cvtColor(img, cv2.COLOR_BGR2RGB)
```
Display the image using Matplotlib
```
plt.imshow(img_rgb, cmap='viridis')  # You can change 'viridis' to another cmap or use None for RGB images
plt.title("Original Image")
plt.axis('off')  # Removes axis ticks and labels
plt.show()
```
Load the image
```
image = cv2.imread('VIN.jpeg')
```
Convert BGR (OpenCV's default) to RGB (Matplotlib's expected color order)
```
img_rgb = cv2.cvtColor(img, cv2.COLOR_BGR2RGB)
img_rgb.shape
(1536, 941, 3)
```
Draw a line from top-left to bottom-right
```
line_img = cv2.line(img_rgb, (0, 0), (768, 600), (255, 0, 0), 2) # cv2.line(image, start_point, end_point, color, thickness)
plt.imshow(line_img, cmap='viridis')  
plt.title("Image with Line")
plt.axis('off')  
plt.show()
```
Load the image
```
image = cv2.imread('VIN.jepg')
```
Convert BGR (OpenCV's default) to RGB (Matplotlib's expected color order)
```
img_rgb = cv2.cvtColor(img, cv2.COLOR_BGR2RGB)
img_rgb.shape
(1536, 941, 3)
circle_img = cv2.circle(img_rgb,(400,300),150,(255,0,0),10) # cv2.circle(image, center, radius, color, thickness)
plt.imshow(circle_img, cmap='viridis')  
plt.title("Image with Circle")
plt.axis('off')  
plt.show()
```
Load the image
```
image = cv2.imread('VIN.jpeg')
```
Convert BGR (OpenCV's default) to RGB (Matplotlib's expected color order)
```
img_rgb = cv2.cvtColor(img, cv2.COLOR_BGR2RGB)
img.shape
(1536, 941, 3)
```
Draw a rectangle around the Whole image
```
rectangle_img = cv2.rectangle(img_rgb, (0, 0), (768, 600), (0, 0, 255), 10)  # cv2.rectangle(image, start_point, end_point, color, thickness)
plt.imshow(rectangle_img, cmap='viridis')  
plt.title("Image with Rectangle")
plt.axis('off')  
plt.show()
```

Load the image
```
image = cv2.imread('VIN.jpeg')
```
Convert BGR (OpenCV's default) to RGB (Matplotlib's expected color order)
```
img_rgb = cv2.cvtColor(img, cv2.COLOR_BGR2RGB)
```
Add text to the image
```
text_img = cv2.putText(img_rgb, "Opencv Drawing", (10, 35), cv2.FONT_HERSHEY_SIMPLEX, 1, (255, 255, 255), 10)  ## cv2.putText(image, text, position, font, font_scale, color, thickness)
plt.imshow(text_img, cmap='viridis')  
plt.title("Image with Text")
plt.axis('off')  
plt.show()
```
Load the image
```
image = cv2.imread('VIN.jpeg') 
image_rgb = cv2.cvtColor(image, cv2.COLOR_BGR2RGB)
```



## Output:

## original image
<img width="781" height="363" alt="image" src="https://github.com/user-attachments/assets/2a041582-cff4-4ac7-97d2-b2cc56cb7e37" />


## Image with Line
<img width="572" height="362" alt="image" src="https://github.com/user-attachments/assets/a234e843-1f8d-48a7-9a7c-7d07f05fc374" />




## Image with Circle
<img width="577" height="358" alt="image" src="https://github.com/user-attachments/assets/013fc02d-b5ce-47f2-9256-73a356dd8d7b" />



## Image with Rectangle
<img width="592" height="372" alt="image" src="https://github.com/user-attachments/assets/ee0c70ee-8bb9-4b36-ada2-caa24bec1239" />


## Image with Text
<img width="580" height="365" alt="image" src="https://github.com/user-attachments/assets/f45d024d-9f7e-48db-b994-6f70228d84d6" />




## Original RGB Image
<img width="573" height="356" alt="image" src="https://github.com/user-attachments/assets/f67cea02-28f0-4495-94f1-5eabef77eb0a" />



## HSV Image
<img width="622" height="356" alt="image" src="https://github.com/user-attachments/assets/dd589603-2586-4964-84e2-52961040a2cc" />



## Grayscale Image
<img width="577" height="360" alt="image" src="https://github.com/user-attachments/assets/abed604d-f869-4a01-b638-3554d3ad06ec" />

## YCrCb Image
<img width="582" height="352" alt="image" src="https://github.com/user-attachments/assets/7fd05b64-57c8-4ea8-b723-1f6ccaf587ab" />


## HSV to RGB Image
<img width="590" height="357" alt="image" src="https://github.com/user-attachments/assets/a2021422-af75-4cad-b183-20d4aec82f3c" />





## Image with 300x300 White Block
<img width="572" height="362" alt="image" src="https://github.com/user-attachments/assets/793cbbff-dcba-4c6c-82e7-225eabf46136" />



## Resized Image (Half Size)
<img width="547" height="461" alt="image" src="https://github.com/user-attachments/assets/28270999-d709-452f-b3bd-f024061554e8" />


## Cropped Region of Interest (ROI)
<img width="446" height="467" alt="image" src="https://github.com/user-attachments/assets/e3ecd47f-991e-49f4-b42e-8569cd783ec7" />




## Flipped Horizontally
<img width="562" height="352" alt="image" src="https://github.com/user-attachments/assets/01d6a679-cc11-4bf0-aff2-cc2d19a718f9" />


## Flipped Vertically
<img width="560" height="366" alt="image" src="https://github.com/user-attachments/assets/602b2775-5541-4cda-b99e-ea21390e9cb5" />






## Result:
Thus, the images were read, displayed, brightness and contrast adjustments were made, and bitwise operations were performed successfully using the Python program.


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
<img width="562" height="353" alt="image" src="https://github.com/user-attachments/assets/ebdb834b-82f9-459c-9235-b8d510e2daad" />

## Image with Line
<img width="770" height="385" alt="image" src="https://github.com/user-attachments/assets/07e64248-9b3d-450d-abd6-38f65b43b7d1" />



## Image with Circle
<img width="858" height="371" alt="image" src="https://github.com/user-attachments/assets/c2da871a-c71c-4d4b-b0f6-cc9f200a0360" />


## Image with Rectangle
<img width="987" height="367" alt="image" src="https://github.com/user-attachments/assets/c2ea663f-5218-4669-aa1f-22082b67149e" />


## Image with Text
<img width="895" height="357" alt="image" src="https://github.com/user-attachments/assets/93caba16-9143-44f4-b945-19b460e14f8b" />



## Original RGB Image
<img width="871" height="358" alt="image" src="https://github.com/user-attachments/assets/144d4185-8ff6-497b-8259-b8fc1710d3bb" />


## HSV Image
<img width="882" height="351" alt="image" src="https://github.com/user-attachments/assets/d4ff43a3-a2b6-4066-be51-bb968e950f1c" />


## Grayscale Image
<img width="920" height="356" alt="image" src="https://github.com/user-attachments/assets/8314b357-c4df-446f-aea4-040fdf40d587" />


## HSV to RGB Image
<img width="906" height="353" alt="image" src="https://github.com/user-attachments/assets/76713914-6f49-40db-9944-3146d122df0d" />


## Image with 300x300 White Block
<img width="825" height="367" alt="image" src="https://github.com/user-attachments/assets/e332c712-5c9d-4608-a5da-3abbb5b036e4" />


## Resized Image (Half Size)
<img width="850" height="461" alt="image" src="https://github.com/user-attachments/assets/473bc968-f047-47e3-a9b9-ff73c5e8df4a" />


## Cropped Region of Interest (ROI)

<img width="687" height="472" alt="image" src="https://github.com/user-attachments/assets/ae383e0d-29c6-4f3b-90ec-40088a7af84a" />




## Flipped Horizontally

![Uploading image.png…]()


## Flipped Vertically

![Uploading image.png…]()



## Result:
Thus, the images were read, displayed, brightness and contrast adjustments were made, and bitwise operations were performed successfully using the Python program.


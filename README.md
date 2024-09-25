# COLOR_CONVERSIONS_OF-IMAGE
## AIM
Write a Python program using OpenCV that performs the following tasks:

i) Read and Display an Image.

ii) 	Draw Shapes and Add Text.

iii) Image Color Conversion.

iv) Access and Manipulate Image Pixels.

v) Image Resizing

vi) Image Cropping

vii) Image Flipping

viii)	Write and Save the Modified Image


## Software Required:
Anaconda - Python 3.7
## Algorithm:
### Step1:
Load an image from your local directory and display it.
### Step2:
o	Draw a line from the top-left to the bottom-right of the image.
o	Draw a circle at the center of the image.
o	Draw a rectangle around a specific region of interest in the image.
o	Add the text "OpenCV Drawing" at the top-left corner of the image.

### Step3:
o	Convert the image from RGB to HSV and display it.
o	Convert the image from RGB to GRAY and display it.
o	Convert the image from RGB to YCrCb and display it.
o	Convert the HSV image back to RGB and display it.

### Step4:
o	Access and print the value of the pixel at coordinates (100, 100).
o	Modify the color of the pixel at (200, 200) to white.

### Step5:
o	Resize the original image to half its size and display it.
### Step6:
o	Crop a region of interest (ROI) from the image (e.g., a 100x100 pixel area starting at (50, 50)) and display it.
### Step7:
o	Flip the original image horizontally and display it.
o	Flip the original image vertically and display it.

### Step8:
o	Save the final modified image to your local directory.


##### Program:
### Developed By: MOUNESH P
### Register Number: 212222230084


## Output:

### i)Read and Display an Image

```python
import cv2
# Read the image
image = cv2.imread('Lokesh.JPG')
# Display the image in a window
cv2.imshow('Image Window', image)
# Wait indefinitely for a key press
cv2.waitKey(0)
# Destroy all windows created by OpenCV
cv2.destroyAllWindows()
```
![image](https://github.com/user-attachments/assets/c737e722-5fe5-475e-8cde-8455830a9e95)
<br>
<br>

### ii)Draw Shapes and Add Text

```python
import cv2

# Load the image
img = cv2.imread("Lokesh.JPG")

# Define parameters for the drawings
start = (0, 0)
stop = (600, 400)
color = (100, 255, 100)
thickness = 10

# 1. Draw a circle
circle_img = img.copy()  # Create a copy of the original image
cv2.circle(circle_img, (330, 225), 150, (255, 0, 0), 10)
cv2.imshow('Circle', circle_img)
cv2.imwrite('Circle_Image.jpg', circle_img)  # Save the image
cv2.waitKey(0)

# 2. Draw a rectangle
rectangle_img = img.copy()  # Create a copy of the original image
cv2.rectangle(rectangle_img, start, stop, color, thickness)
cv2.imshow('Rectangle', rectangle_img)
cv2.imwrite('Rectangle_Image.jpg', rectangle_img)  # Save the image
cv2.waitKey(0)

# 3. Draw a line
line_img = img.copy()  # Create a copy of the original image
cv2.line(line_img, (100, 200), (900, 100), (200, 100, 205), 10)
cv2.imshow('Line', line_img)
cv2.imwrite('Line_Image.jpg', line_img)  # Save the image
cv2.waitKey(0)

# 4. Add text to the image
text_img = img.copy()  # Create a copy of the original image
text = "OpenCV Drawing"
org = (10, 30)  # top-left corner of the text string
font = cv2.FONT_HERSHEY_SIMPLEX
font_scale = 1
text_color = (255, 255, 255)  # White color
thickness = 2
cv2.putText(text_img, text, org, font, font_scale, text_color, thickness, cv2.LINE_AA)
cv2.imshow('Text', text_img)
cv2.imwrite('Text_Image.jpg', text_img)  # Save the image
cv2.waitKey(0)

# Clean up windows
cv2.destroyAllWindows()
```
![image](https://github.com/user-attachments/assets/56416a64-fc63-4ef2-ad24-26f0126984f4)
![image](https://github.com/user-attachments/assets/b1a57435-f2ba-489f-b5be-a98f54d9df53)
![image](https://github.com/user-attachments/assets/a1a956e6-ce4a-4298-bba6-5cd8fd346819)
![image](https://github.com/user-attachments/assets/12627465-7ccb-4d87-b4d3-938f6da6061d)

<br>
<br>

### iii)Image Color Conversion

```python
import cv2

# Read the image
image = cv2.imread("Lokesh.JPG")

# Convert to HSV color space
img_hsv = cv2.cvtColor(image, cv2.COLOR_BGR2HSV)
cv2.imshow('Image Window (HSV)', img_hsv)
cv2.imwrite('Lokesh_HSV.jpg', img_hsv)  # Save HSV image
cv2.waitKey(0)

# Convert to grayscale
img_gray = cv2.cvtColor(image, cv2.COLOR_BGR2GRAY)
cv2.imshow('Grayscale Image', img_gray)
cv2.imwrite('Lokesh_Gray.jpg', img_gray)  # Save grayscale image
cv2.waitKey(0)

# Convert the image from RGB to YCrCb and display it
ycrcb_image = cv2.cvtColor(image, cv2.COLOR_BGR2YCrCb)
cv2.imshow('YCrCb Image', ycrcb_image)
cv2.imwrite('Lokesh_YCrCb.jpg', ycrcb_image)  # Save YCrCb image
cv2.waitKey(0)

# Convert the HSV image back to RGB and display it
hsv_to_rgb_image = cv2.cvtColor(img_hsv, cv2.COLOR_HSV2BGR)
cv2.imshow('HSV to RGB Image', hsv_to_rgb_image)
cv2.imwrite('Lokesh_HSV_to_RGB.jpg', hsv_to_rgb_image)  # Save the converted RGB image
cv2.waitKey(0)

# Clean up
cv2.destroyAllWindows()

```
### Convert the image from RGB to HSV and display it:
![image](https://github.com/user-attachments/assets/9eb9d0f1-d03a-4474-953a-8fb7d3d48ff3)
### Convert the image from RGB to GRAY and display it:
![image](https://github.com/user-attachments/assets/baee897c-5af8-455c-b713-a65bfd0bd60a)
### Convert the image from RGB to YCrCb and display it:
![image](https://github.com/user-attachments/assets/d2b826c3-5c61-4cc2-bd19-3b299aa3f0e2)
### Convert the HSV image back to RGB and display it:
![image](https://github.com/user-attachments/assets/454ebfb4-dc49-4392-90e6-21d024285e66)

<br>
<br>

### iv)Access and Manipulate Image Pixels

```
# Step 4: Access and Manipulate Image Pixels
# Access and print the value of the pixel at coordinates (100, 100)
pixel_value = image[100, 100]
print(f"Pixel value at (100, 100): {pixel_value}")

# Modify the color of the pixel at (200, 200) to white
image[200, 200] = [255, 255, 255]
print(f"Modified pixel value at (200, 200): {image[200, 200]}")
```
![image](https://github.com/user-attachments/assets/68ecfe0c-2d9d-4c57-9627-a18afa44996f)

<br>
<br>

### v)Image Resizing
```
# Image Resizing
# Resize the original image to half its size and display it
resized_image = cv2.resize(image, (image.shape[1] // 2, image.shape[0] // 2))
cv2.imshow('Resized Image', resized_image)
cv2.waitKey(0)
```
![image](https://github.com/user-attachments/assets/7f241fde-e0e0-4dcb-bc7f-e4fdb89c877f)

<br>
<br>

### vi)Image Cropping:

```
# Image Cropping
# Crop a region of interest (100x100 pixels starting at (50, 50)) and display it
roi = image[50:150, 50:150]
cv2.imshow('Cropped ROI Image', roi)
cv2.waitKey(0)
```
![image](https://github.com/user-attachments/assets/d380958b-561b-4f35-992d-d36bbd18e474)

<br>
<br>

### vii)Image Flipping

```
# Flip the original image horizontally and display it
flipped_horizontally = cv2.flip(image, 1)
cv2.imshow('Horizontally Flipped Image', flipped_horizontally)
cv2.waitKey(0)

# Flip the original image vertically and display it
flipped_vertically = cv2.flip(image, 0)
cv2.imshow('Vertically Flipped Image', flipped_vertically)
cv2.waitKey(0)
```

### Flip the original image horizontally and display it:
![image](https://github.com/user-attachments/assets/f42e9650-7bd1-4153-bba5-3e617de642f1)

### Flip the original image vertically and display it:
![image](https://github.com/user-attachments/assets/69c8f22f-e9c9-411a-8d1a-13a0897b1055)

<br>
<br>

### viii)Write and Save the Modified Image

```
# Step 8: Write and Save the Modified Image
output_path = 'output.jpg'
cv2.imwrite(output_path, image_with_text)
print(f"Modified image saved as {output_path}")
```
![image](https://github.com/user-attachments/assets/b9f19a09-ef8c-445d-aa31-cfe83440384e)

<br>
<br>

## Result:
Thus the images are read, displayed, and written ,and color conversion was performed  successfully using the python program.

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
- **Name:** [GOKUL B]  
- **Register Number:** [212225230076]

  ### Ex. No. 01

#### 1. Read the image ('Eagle_in_Flight.jpg') using OpenCV imread() as a grayscale image.
```python
import cv2
import matplotlib.pyplot as plt
img = cv2.imread('fly.png', cv2.IMREAD_COLOR)
img_rgb = cv2.cvtColor(img, cv2.COLOR_BGR2RGB)
plt.imshow(img_rgb, cmap='viridis') 
plt.title("Original Image")
plt.axis('off')  
plt.show()
```

#### 2. Print the image width, height & Channel.
```python
image = cv2.imread('fly.png')
img_rgb = cv2.cvtColor(img, cv2.COLOR_BGR2RGB)
img_rgb.shape
```

#### 3. Display the image using matplotlib imshow().
```python
line_img = cv2.line(img_rgb, (0, 0), (768, 600), (255, 0, 0), 10)
plt.imshow(line_img, cmap='viridis')  
plt.title("Image with Line")
plt.axis('off')  
plt.show()
```

#### 4. Save the image as a PNG file using OpenCV imwrite().
```python
image = cv2.imread('fly.png') 
img_rgb = cv2.cvtColor(img, cv2.COLOR_BGR2RGB)
img_rgb.shape
```

#### 5. Read the saved image above as a color image using cv2.cvtColor().
```python
circle_img = cv2.circle(img_rgb,(100,150),100,(255,0,0),10)
plt.imshow(circle_img, cmap='viridis')  
plt.title("Image with Circle")
plt.axis('off')  
plt.show()
```

#### 6. Display the Colour image using matplotlib imshow() & Print the image width, height & channel.
```python
image = cv2.imread('fly.png') 
img_rgb = cv2.cvtColor(img, cv2.COLOR_BGR2RGB)
text_img = cv2.putText(img_rgb, "OpenCV Drawing butterfly", (10, 30), cv2.FONT_HERSHEY_SIMPLEX, 1, (255, 255, 255), 10) 
plt.imshow(text_img, cmap='viridis')  
plt.title("Image with Text")
plt.axis('off')  
plt.show()
```

#### 7. Crop the image to extract any specific (Eagle alone) object from the image.
```python
image = cv2.imread('fly.png')
mage_rgb = cv2.cvtCoilor(image, cv2.COLOR_BGR2RGB)
plt.imshow(image_rgb)
plt.title("Original RGB Image")
plt.axis("off")
```

#### 8. Resize the image up by a factor of 2x.
```python
image_hsv = cv2.cvtColor(image_rgb, cv2.COLOR_RGB2HSV)
plt.imshow(image_hsv)
plt.title("HSV Image")
plt.axis("off")
```

#### 9. Flip the cropped/resized image horizontally.
```python
image_gray = cv2.cvtColor(image_rgb, cv2.COLOR_RGB2GRAY)
plt.imshow(image_gray, cmap='gray')
plt.title("Grayscale Image")
plt.axis("off")
```

#### 10. Read in the image ('Apollo-11-launch.jpg').
```python
image_ycrcb = cv2.cvtColor(image_rgb, cv2.COLOR_RGB2YCrCb)
plt.imshow(image_ycrcb)
plt.title("YCrCb Image")
plt.axis("off")
```

#### 11. Add the following text to the dark area at the bottom of the image (centered on the image):
```python
image_hsv_to_rgb = cv2.cvtColor(image_hsv, cv2.COLOR_HSV2RGB)
plt.imshow(image_hsv_to_rgb)
plt.title("HSV to RGB Image")
plt.axis("off")
```

#### 12. Draw a magenta rectangle that encompasses the launch tower and the rocket.
```python
image[100:300, 100:300] = [255, 255, 255] 
image_rgb = cv2.cvtColor(image, cv2.COLOR_BGR2RGB)
plt.imshow(image_rgb)
plt.title("Image with 300x300 White Block")
plt.axis("off")
plt.show()
```

#### 13. Display the final annotated image.
```python
image = cv2.imread('fly.png')
image.shape
```

#### 14. Read the image ('Boy.jpg').
```python
resized_image = cv2.resize(image, (768 // 2, 600 // 2))
resized_image_rgb = cv2.cvtColor(resized_image, cv2.COLOR_BGR2RGB)
resized_image_rgb.shape
plt.imshow(resized_image_rgb)
plt.title("Resized Image (Half Size)")
plt.axis("off")
plt.show()
```

#### 15. Adjust the brightness of the image.
```python
image = cv2.imread('fly.png') 
image.shape
roi = image[50:250, 50:250]
roi_rgb = cv2.cvtColor(roi, cv2.COLOR_BGR2RGB)
plt.imshow(roi_rgb)
plt.title("Cropped Region of Interest (ROI)")
plt.axis("off")
plt.show()
```

#### 16. Create brighter and darker images.
```python
img_brighter = cv2.add(img, matrix)
img_darker = cv2.subtract(img, matrix)

```

#### 17. Display the images (Original Image, Darker Image, Brighter Image).
```python
image = cv2.imread('fly.png') 
flipped_horizontally = cv2.flip(image, 1)
flipped_horizontally_rgb = cv2.cvtColor(flipped_horizontally, cv2.COLOR_BGR2RGB)
plt.imshow(flipped_horizontally_rgb)
plt.title("Flipped Horizontally")
plt.axis("off")
```

#### 18. Modify the image contrast.
```python
flipped_vertically = cv2.flip(image, 0)
flipped_vertically_rgb = cv2.cvtColor(flipped_vertically, cv2.COLOR_BGR2RGB)
plt.imshow(flipped_vertically_rgb)
plt.title("Flipped Vertically")
plt.axis("off")
```

## Output:
<img width="630" height="442" alt="image" src="https://github.com/user-attachments/assets/63b46f1e-d6d1-44ab-bd82-1529d45b76eb" />
<img width="637" height="433" alt="image" src="https://github.com/user-attachments/assets/a49d2941-4d53-4c26-b322-1978aa7f13a9" />
<img width="620" height="437" alt="image" src="https://github.com/user-attachments/assets/bfa937ad-ecb9-49a1-9a50-c6003e53bb02" />
<img width="652" height="437" alt="image" src="https://github.com/user-attachments/assets/273620c6-2bad-4923-ba8a-6c7aa62e4ce9" />
<img width="616" height="442" alt="image" src="https://github.com/user-attachments/assets/4cd49a3a-3b98-4deb-9f07-ef9728a508d4" />
<img width="618" height="436" alt="image" src="https://github.com/user-attachments/assets/108dd743-1a2f-47ab-a610-729a6ce9c25a" />
<img width="650" height="437" alt="image" src="https://github.com/user-attachments/assets/fd595a83-67a6-46c9-8405-d8d03e7ef3aa" />
<img width="631" height="431" alt="image" src="https://github.com/user-attachments/assets/95437200-19e8-4d1a-9cb7-942cc10b1b2a" />

## Result:
Thus, the images were read, displayed, brightness and contrast adjustments were made, and bitwise operations were performed successfully using the Python program.


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
 ## Name:JANANI S 
 ## Register Number:212223230086

  ### Ex. No. 01
```
import cv2
import matplotlib.pyplot as plt
```
```python
# Read the image using OpenCV
img = cv2.imread('photo.jpeg', cv2.IMREAD_COLOR)
```
```python
# Convert BGR (OpenCV's default) to RGB (Matplotlib's expected color order)
img_rgb = cv2.cvtColor(img, cv2.COLOR_BGR2RGB)
```

```python
# Display the image using matplotlib imshow().
plt.imshow(img_rgb, cmap='viridis')  # You can change 'viridis' to another cmap or use None for RGB images
plt.title("Original Image")
plt.axis('off')  # Removes axis ticks and labels
plt.show()
```
## OUTPUT :

<img width="494" height="523" alt="image" src="https://github.com/user-attachments/assets/0e71ef05-4223-4e49-8486-ca8d850cbce2" />

```python
# Load the image
image = cv2.imread('photo.jpeg') 
```
```python
# Convert BGR (OpenCV's default) to RGB (Matplotlib's expected color order)
img_rgb = cv2.cvtColor(img, cv2.COLOR_BGR2RGB)
img_rgb.shape
```

<img width="244" height="43" alt="image" src="https://github.com/user-attachments/assets/d25ddf8f-aba8-498f-9fab-6e8c3245e94c" />

```python
# Draw a line from top-left to bottom-right
line_img = cv2.line(img_rgb, (0, 0), (768, 600), (255, 0, 0), 2) # cv2.line(image, start_point, end_point, color, thickness)
```
```python
plt.imshow(line_img, cmap='viridis')  
plt.title("Image with Line")
plt.axis('off')  
plt.show()
```

## OUTPUT :

<img width="515" height="523" alt="image" src="https://github.com/user-attachments/assets/bc61524c-72b1-4330-a80b-bde67abf9029" />

```python
# Load the image
image = cv2.imread('photo.jpeg')

# Convert BGR (OpenCV's default) to RGB (Matplotlib's expected color order)
img_rgb = cv2.cvtColor(img, cv2.COLOR_BGR2RGB)
img_rgb.shape

```
## OUTPUT :

<img width="228" height="49" alt="image" src="https://github.com/user-attachments/assets/94cdca8b-8ada-4dc5-a286-6d61c0fc1c54" />

```
circle_img = cv2.circle(img_rgb,(400,300),150,(255,0,0),10) # cv2.circle(image, center, radius, color, thickness)
```

```python
plt.imshow(circle_img, cmap='viridis')  
plt.title("Image with Circle")
plt.axis('off')  
plt.show()
```

## OUTPUT :

<img width="497" height="526" alt="image" src="https://github.com/user-attachments/assets/cd3293e2-67cb-432a-80b0-31ff1c58bc55" />

```
# Load the image
image = cv2.imread('photo.jpeg') 

# Convert BGR (OpenCV's default) to RGB (Matplotlib's expected color order)
img_rgb = cv2.cvtColor(img, cv2.COLOR_BGR2RGB)
img.shape
```

<img width="233" height="42" alt="image" src="https://github.com/user-attachments/assets/4e124fc0-a314-4e0d-8b77-814ce105e62f" />

```python
# Draw a rectangle around the Whole image
rectangle_img = cv2.rectangle(img_rgb, (0, 0), (768, 600), (0, 0, 255), 10)  # cv2.rectangle(image, start_point, end_point, color, thickness)
```
```python
plt.imshow(rectangle_img, cmap='viridis')  
plt.title("Image with Rectangle")
plt.axis('off')  
plt.show()
```

## OUTPUT :

<img width="513" height="513" alt="image" src="https://github.com/user-attachments/assets/b6062c5e-41c7-42d9-9480-04471ce61399" />

```
# Load the image
image = cv2.imread('photo.jpeg') 

# Convert BGR (OpenCV's default) to RGB (Matplotlib's expected color order)
img_rgb = cv2.cvtColor(img, cv2.COLOR_BGR2RGB)
```
```
# Add text to the image
text_img = cv2.putText(img_rgb, "OpenCV Drawing", (10, 30), cv2.FONT_HERSHEY_SIMPLEX, 1, (255, 255, 255), 10)  ## cv2.putText(image, text, position, font, font_scale, color, thickness)
```
```
plt.imshow(text_img, cmap='viridis')  
plt.title("Image with Text")
plt.axis('off')  
plt.show()
```

## OUTPUT :

<img width="487" height="521" alt="image" src="https://github.com/user-attachments/assets/49b236b9-671c-4e39-9cac-b01407b3649b" />

```python
# Load the image
image = cv2.imread('photo.jpeg')
image_rgb = cv2.cvtColor(image, cv2.COLOR_BGR2RGB)
```
```python
# Original RGB Image
plt.imshow(image_rgb)
plt.title("Original RGB Image")
plt.axis("off")
```
## OUTPUT : 

<img width="757" height="551" alt="image" src="https://github.com/user-attachments/assets/4cdfb038-deab-4f43-b221-0abe03f9f03b" />

```python
# Convert RGB to HSV
image_hsv = cv2.cvtColor(image_rgb, cv2.COLOR_RGB2HSV)

# HSV Image
plt.imshow(image_hsv)
plt.title("HSV Image")
plt.axis("off")
```

# OUTPUT :

<img width="745" height="567" alt="image" src="https://github.com/user-attachments/assets/1c9f2e70-15d1-459a-9d5e-07cce34b3aac" />

```python
# Convert RGB to GRAY
image_gray = cv2.cvtColor(image_rgb, cv2.COLOR_RGB2GRAY)
```
```python
# Grayscale Image
plt.imshow(image_gray, cmap='gray')
plt.title("Grayscale Image")
plt.axis("off")
```

## OUTPUT :

<img width="765" height="568" alt="image" src="https://github.com/user-attachments/assets/e4218f0a-12ea-4241-bd2b-1ffcef0a81d1" />

```python
# Convert RGB to YCrCb
image_ycrcb = cv2.cvtColor(image_rgb, cv2.COLOR_RGB2YCrCb)
```
```
# YCrCb Image
plt.imshow(image_ycrcb)
plt.title("YCrCb Image")
plt.axis("off")
```

## OUTPUT :

<img width="753" height="549" alt="image" src="https://github.com/user-attachments/assets/57599572-e535-4221-91db-545dc8c24e22" />

```python
# Convert HSV back to RGB
image_hsv_to_rgb = cv2.cvtColor(image_hsv, cv2.COLOR_HSV2RGB)
plt.imshow(image_hsv_to_rgb)
plt.title("HSV to RGB Image")
plt.axis("off")
```

## OUTPUT :

<img width="754" height="549" alt="image" src="https://github.com/user-attachments/assets/2be813ef-6661-4ea9-bbc8-06b1067ba612" />

```python
# Modify a block of pixels (300x300) to white, starting from (200, 200)
image[200:500, 200:500] = [255, 255, 255]  # Rows: 200-499, Columns: 200-499

# Convert BGR to RGB for displaying with Matplotlib
image_rgb = cv2.cvtColor(image, cv2.COLOR_BGR2RGB)
```
```
# Display the modified image
plt.imshow(image_rgb)
plt.title("Image with 300x300 White Block")
plt.axis("off")
plt.show()
```

## OUTPUT :

<img width="496" height="521" alt="image" src="https://github.com/user-attachments/assets/818dd7f9-f491-43f3-8bf9-f1798e497de3" />

```
# Load the image
image = cv2.imread('photo.jpeg')
image.shape
```
<img width="183" height="44" alt="image" src="https://github.com/user-attachments/assets/877e33d2-5758-43bb-b338-d7e2933874ec" />

```
# Resize the image to half its size
resized_image = cv2.resize(image, (768 // 2, 600 // 2))  # (new_width, new_height)

# Convert BGR to RGB for displaying with Matplotlib
resized_image_rgb = cv2.cvtColor(resized_image, cv2.COLOR_BGR2RGB)
resized_image_rgb.shape
```

<img width="199" height="44" alt="image" src="https://github.com/user-attachments/assets/ae8f2ba6-05c1-44e6-83e4-b274aac15330" />

```
# Display the resized image
plt.imshow(resized_image_rgb)
plt.title("Resized Image (Half Size)")
plt.axis("off")
plt.show()
```

## OUTPUT :

<img width="694" height="520" alt="image" src="https://github.com/user-attachments/assets/ab476f61-77ed-46e0-aaff-d99e5b059622" />

```
# Load the image
image = cv2.imread('photo.jpeg')
image.shape
```
<img width="204" height="48" alt="image" src="https://github.com/user-attachments/assets/e9d9fcba-6eaa-428d-813b-581e412d6358" />

```
# Crop a 300x300 region starting from (50, 50)
roi = image[50:350, 50:350]  # Rows: 50-349, Columns: 50-349

# Convert BGR to RGB for displaying with Matplotlib
roi_rgb = cv2.cvtColor(roi, cv2.COLOR_BGR2RGB)
```
```
# Display the cropped region (ROI)
plt.imshow(roi_rgb)
plt.title("Cropped Region of Interest (ROI)")
plt.axis("off")
plt.show()
```
## OUTPUT :

<img width="524" height="523" alt="image" src="https://github.com/user-attachments/assets/3ae4a0d5-0c1d-40c1-90c6-b8b925eea26b" />

```
# Load the image
image = cv2.imread('photo.jpeg')

# Flip the image horizontally (left-right)
flipped_horizontally = cv2.flip(image, 1)

# Convert BGR to RGB for displaying with Matplotlib
flipped_horizontally_rgb = cv2.cvtColor(flipped_horizontally, cv2.COLOR_BGR2RGB)
```
```
# Horizontal flip
plt.imshow(flipped_horizontally_rgb)
plt.title("Flipped Horizontally")
plt.axis("off")
```
## OUTPUT :

<img width="749" height="565" alt="image" src="https://github.com/user-attachments/assets/68821dd7-743e-49c6-b3ae-8af2b15f445b" />

```
# Flip the image vertically (up-down)
flipped_vertically = cv2.flip(image, 0)

# Convert BGR to RGB for displaying with Matplotlib
flipped_vertically_rgb = cv2.cvtColor(flipped_vertically, cv2.COLOR_BGR2RGB)
```
```
# Vertical flip
plt.imshow(flipped_vertically_rgb)
plt.title("Flipped Vertically")
plt.axis("off")
```
## OUTPUT :

<img width="754" height="561" alt="image" src="https://github.com/user-attachments/assets/30ab3245-6e7e-4dda-9511-c6bd109a1057" />

## Result:
Thus, the images were read, displayed, brightness and contrast adjustments were made, and bitwise operations were performed successfully using the Python program.


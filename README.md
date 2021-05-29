# Image-Processing-Extraction-Classification
Notebook for image 
*Processing 
*Extraction
*Classification

**Processing**
>Resizing
>Masking 

```
masked_image = np.copy(image)
masked_image[mask != 0] = [0, 0, 0]
```

**Masking with RGB**
For `Non-Gradient` green background
```
mask = cv2.inRange(image, lower_green, upper_green)
```
**Masking with HSV**
For `Gradient` green background

```
hsv = cv2.cvtColor(image, cv2.COLOR_RGB2HSV)
h = hsv[:,:,0]
lower_hue = 40
upper_hue = 80

mask=cv2.inRange(h,lower_hue,upper_hue)
```

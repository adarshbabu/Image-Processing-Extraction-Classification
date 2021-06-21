# Image-Processing-Extraction-Classification
Notebook for image 
-Processing
-Extraction
-Classification

**Processing**
- Resizing
- Masking
  - with RGB
  - with HSV

**A. Masking with RGB**
For `Non-Gradient` green background
```
lower_green = np.array([0,180,0]) 
upper_green = np.array([100,255,100])

mask = cv2.inRange(image, lower_green, upper_green)
```  

**B. Masking with HSV**
For `Gradient` green background

```
hsv = cv2.cvtColor(image, cv2.COLOR_RGB2HSV)
h = hsv[:,:,0]
lower_hue = 40
upper_hue = 80

mask=cv2.inRange(h,lower_hue,upper_hue)
```
***masking syntax***
```
masked_image[mask != 0] = [0, 0, 0]
```

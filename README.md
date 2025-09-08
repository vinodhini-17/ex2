# Ex. No: 02  
# Image Acquisition using Web Camera  

**Name:** __VINODHINI K__________    **Reg. No:** __212223230245__________

## Dr. Michael Mahesh K Saveetha Engineering College
- michaelmaheshk@gmail.com 
- CNN using Custom Images 
- 19AI413-Digital Image Processing Techincs 

- EVEN SEM ( Slot: 4D1-1 & 4K1-1)
#i)Write the frameas JPG file
```
import cv2
import matplotlib.pyplot as plt
from IPython.display import clear_output
import time
```
```
cap = cv2.VideoCapture(0)
ret, frame = cap.read()
if ret:
    cv2.imwrite("captured_frame.jpg", frame)
cap.release()
```
```
captured_image = cv2.imread('captured_frame.jpg')
```
```
plt.imshow(captured_image[:,:,::-1])
plt.title('Captured Frame')
plt.axis('off')
plt.show()
```
<img width="633" height="505" alt="image" src="https://github.com/user-attachments/assets/5ddb0e97-65be-4af7-b05b-1aab50ad37ff" />

#ii)Display the vedio
```
cap = cv2.VideoCapture(0)

for i in range(50):
    ret, frame = cap.read()
    if not ret:
        break
    frame_rgb = cv2.cvtColor(frame, cv2.COLOR_BGR2RGB)
    clear_output(wait=True)
    plt.imshow(frame_rgb)
    plt.axis('off')
    plt.show()
    time.sleep(0.05)

cap.release()
```
<img width="627" height="483" alt="image" src="https://github.com/user-attachments/assets/aca09b50-e6f0-4e55-802d-6441efab8b97" />

#iii) Display the video by resizing the window
```
cap = cv2.VideoCapture(0)

for i in range(50):
    ret, frame = cap.read()
    if not ret:
        break
    resized_frame = cv2.resize(frame, (100, 150))  # Resize to 320x240
    frame_rgb = cv2.cvtColor(resized_frame, cv2.COLOR_BGR2RGB)
    clear_output(wait=True)
    plt.imshow(frame_rgb)
    plt.axis('off')
    plt.show()
    time.sleep(0.05)

cap.release()
```

<img width="326" height="477" alt="image" src="https://github.com/user-attachments/assets/88ef4591-faf9-4c22-8bc6-b0d04bfceb4e" />

# iv) Rotate and display the video
```
cap = cv2.VideoCapture(0)

for i in range(50):
    ret, frame = cap.read()
    if not ret:
        break
    rotated_frame = cv2.rotate(frame, cv2.ROTATE_90_CLOCKWISE)
    frame_rgb = cv2.cvtColor(rotated_frame, cv2.COLOR_BGR2RGB)
    clear_output(wait=True)
    plt.imshow(frame_rgb)
    plt.axis('off')
    plt.show()
    time.sleep(0.05)

cap.release()
```
<img width="365" height="474" alt="image" src="https://github.com/user-attachments/assets/c3eee653-7ec1-4ad6-8269-1943463dc8df" />


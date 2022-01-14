# Hand-Tracking-Module
### Simple hand landmarks detection and hand tracking module on python3 using openCV and mediapipe
I'm using python 3.7.9, opencv 4.5.5.62 and mediapipe 0.8.9.1

## Requirements
* opencv
* mediapipe

## Features
* Tracking Hands
* Opens Camera instantly
* Detecting if fingers are up or down

## Usage
import libraries:
```python
import cv2 as cv
import HandTrackingModule as hd
```
to use the library:
```python
cap = cv.VideoCapture(1)
detector = hd.handDetector()
while True:
  sucess, img = cap.read()
  img = detector.findHands(img)
  try:
    fingers = detector.getFingers(img)
    print(fingers)
  except Exception as ex:
    Print(f'An Exception Occurred: {ex}')
  cv.imshow('image', img)
  k = cv.waitKey(1)
  if k == 27:
    break
```

## Support
if you are having issues let me know

## License
MIT license.

### Thank You

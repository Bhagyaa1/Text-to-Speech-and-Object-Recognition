This project integrates real-time object recognition with text-to-speech capabilities, providing an interactive experience that announces detected objects to the user. It uses the YOLO (You Only Look Once) algorithm for object detection and both gTTS and pyttsx3 for converting detected objects' names into speech.

Features
Real-Time Object Detection: Uses the YOLO algorithm to detect objects in video feed from the webcam.
Text-to-Speech Output: Converts detected object names into spoken words, providing auditory feedback to the user.
gTTS: Utilizes Google's Text-to-Speech service for generating speech, requiring an internet connection.
pyttsx3: Provides an offline alternative for text-to-speech, ensuring the functionality works without an internet connection.
Dynamic Frame Processing: Measures frames processed per second (FPS) to monitor performance.
pyttsx3 is a text-to-speech conversion library in Python that works offline, unlike many other text-to-speech libraries that require an internet connection. It supports multiple TTS engines, including SAPI5 on Windows, NSSpeechSynthesizer on macOS, and espeak on Linux. pyttsx3 allows you to customize speech properties such as rate, volume, and voice, providing flexibility in how the text is spoken. It is particularly useful for applications that need consistent and reliable voice output without dependency on online services.
Requirements
Python 3.x
OpenCV (cv2)
NumPy
gTTS (gtts)
pyttsx3
playsound
Installation
!pip install pyttsx3

!pip install opencv-python-headless

!pip install gtts

!wget https://pjreddie.com/media/files/yolov3.weights

!wget https://raw.githubusercontent.com/pjreddie/darknet/master/cfg/yolov3.cfg



yolov3.cfg and yolov3.weights (You can download these from the official YOLO website).
coco.names file containing the list of object classes.




bash
Copy code
python object_recognition.py
The script will:

Capture video input from the webcam.
Detect objects in real-time using YOLO.
Convert the detected objects' names into speech using gTTS or pyttsx3.
Provide auditory feedback with the names of the detected objects.
Customization
Object Detection Threshold: You can adjust the confidence threshold for object detection by modifying the confidence > 0.6 line in the script.

Text-to-Speech Engine: Switch between gTTS and pyttsx3 by commenting/uncommenting the respective lines in the script.



Voice Properties: Modify the speech rate, volume, or voice using pyttsx3 by adjusting the rate, volume, and voice properties in the script.










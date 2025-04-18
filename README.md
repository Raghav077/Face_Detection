Real-Time Face Detection using OpenCV
This project demonstrates real-time face detection using a webcam feed and OpenCV's Haar Cascade classifier.

🧠 How It Works
Uses OpenCV's haarcascade_frontalface_default.xml to detect faces.
Captures live video from your webcam.
Converts each frame to grayscale for processing.
Detects faces and draws rectangles around them in real-time.

📸 Preview
When you run the script, your webcam will open and show a window titled "Face Detection" with rectangles around detected faces. Press 'q' to quit.

🛠 Requirements
Python 3.x
OpenCV (cv2)

Step-2  Install OpenCV:
 pip install opencv-python
 
Step-3  🚀 Run the Script
   python face_detection.py
   
🧾 Code Overview
face_cascade = cv2.CascadeClassifier(cv2.data.haarcascades + 'haarcascade_frontalface_default.xml')

Loads the pre-trained face detection model.
cap = cv2.VideoCapture(0) 

Accesses the webcam (0 is the default camera index)
gray = cv2.cvtColor(frame, cv2.COLOR_BGR2GRAY)
faces = face_cascade.detectMultiScale(gray, scaleFactor=1.1, minNeighbors=5, minSize=(30, 30))

Converts the frame to grayscale and detects faces.
cv2.rectangle(frame, (x, y), (x + w, y + h), (255, 0, 0), 2)
🛑 Exit
Press 'q' to stop the webcam and close the window.

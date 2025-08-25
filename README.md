# Hand Tracker

This project is a **simple implementation of real-time hand tracking** using [MediaPipe Hands](https://developers.google.com/mediapipe/solutions/vision/hand_landmarker) and OpenCV.  
It uses your webcam to detect one or more hands, track their movement, and draw landmarks (key points like fingertips, joints, and wrist) on the screen.  

The goal of this project is to provide an **easy-to-understand starting point** for anyone who wants to explore **computer vision, gesture recognition, or human-computer interaction**.

---

## 🔍 How It Works

1. **Capture video input**  
   - The script uses OpenCV to access your webcam (`cv2.VideoCapture(0)`).
   - Each frame from the webcam is read in real-time.

2. **Convert image format**  
   - OpenCV uses **BGR** format by default, while MediaPipe requires **RGB**.
   - Each frame is converted before being processed.

3. **Hand detection and tracking**  
   - MediaPipe’s `Hands` solution detects hands in the frame.
   - It identifies up to **21 landmarks per hand** (fingertips, knuckles, palm base, etc.).
   - Both hands can be tracked at the same time.

4. **Draw landmarks on the frame**  
   - The detected landmarks and their connections are drawn on top of the video.
   - This makes it easy to see how the model recognizes the hand structure.

5. **Display the results**  
   - The annotated video is shown in a window called **"MediaPipe Hands"**.
   - The image is flipped horizontally so it feels like looking in a mirror.

6. **Exit the program**  
   - Press **`ESC`** on your keyboard to close the window and stop tracking.

---

## 🛠️ Requirements

- **Python**: `3.8 – 3.11` (MediaPipe does not support 3.12+ yet)  
- Install dependencies with:

```bash
pip install opencv-python mediapipe

# 🛠️ Real-Time Defect & Change Detection System (Multi-Camera)

A real-time computer vision–based defect and change detection system built using **Python, OpenCV, and Flask**.  
The system supports **multiple camera feeds**, detects structural defects such as cracks or object displacement, and displays results on a centralized web dashboard.

This project is suitable for **industrial inspection, surveillance, and structural health monitoring**.

---

## ✨ Features

- Real-time video capture using webcams
- Change and defect detection using frame differencing
- Region of Interest (ROI) based processing
- Background suppression for accurate detection
- Directional movement detection with dynamic ROI shifting
- Multi-camera support:
  - Multiple webcams on a single PC
  - Multiple laptops streaming to a central server
- Live video streaming using Flask
- Centralized monitoring dashboard
- Visual alerts on detected defects or changes
- Timestamped detection events
- Automatic saving of reference and processed images

---

## 🧠 Working Principle

1. The system captures an initial **reference frame**.
2. Incoming frames are continuously compared with the reference.
3. Image processing steps include:
   - Grayscale conversion
   - Gaussian blurring
   - Frame differencing
   - Thresholding
   - Contour detection
4. Significant changes within the ROI are identified as **defects or movements**.
5. Detected changes are highlighted on the video stream and logged with timestamps.
6. For object movement:
   - Direction is shown using arrows
   - ROI automatically shifts with the object

---

## 🧰 Tech Stack

- **Language:** Python  
- **Computer Vision:** OpenCV  
- **Backend:** Flask  
- **Frontend:** HTML, CSS, JavaScript  
- **Streaming:** Flask routes / ports  
- **Storage:** Local file system  

---

## 📂 Project Structure

```text
real-time-defect-detection-system/
│
├── server/
│   │
│   ├── server.py               # Flask server (dashboard + stream consumer)
│   │
│   ├── templates/
│   │   └── index.html           # Server dashboard UI
│   │
│   └── static/
│       └── captured_images/     # Saved reference & processed images
│
├── client/
│   │
│   ├── client.py               # Camera client (starts stream first)
│   │
│   └── static/
│       └── captured_images/     # Client-side saved frames (if used)
│
├── crack_detection.py           # Core defect/change detection logic
├── requirements.txt
└── README.md

```
---

## ▶️ How to Run

### 1. Clone the Repository

```bash
git clone https://github.com/Mayukh27/Real-Time_Defect-_and_Change_Detection_System.git
cd Real-Time_Defect-_and_Change_Detection_System

```
### 2. Install Dependencies

pip install -r requirements.txt

### 3. Start Client Streaming

python client.py

### 4. Start Server

Add client streaming urls to the server

python server.py

## 📊 Applications

Structural crack detection

Industrial defect inspection

Construction site monitoring

Surveillance systems

Smart infrastructure monitoring

## 👨‍💻 Author

Mayukh Ghosh
B.Tech – Computer Science




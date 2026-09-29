# face_detection

A simple web application that triggers real-time face detection using OpenCV, controlled through a Flask-powered web interface.

## Overview

This project provides a lightweight browser-based front end for starting a live face detection session on the host machine's webcam. The Flask backend serves a web page with a start control, which spawns a Python/OpenCV script that opens a video feed and detects faces in real time.

## Features

- Simple, clean web interface built with HTML/CSS
- Flask backend to handle requests and manage the detection process
- Real-time face detection powered by OpenCV
- One-click start from the browser

## Tech Stack

- **Backend:** Python, Flask
- **Computer Vision:** OpenCV
- **Frontend:** HTML, CSS
- **Server:** Gunicorn (production), Flask dev server (local)

## Prerequisites

- Python 3.9–3.11
- A webcam connected to the machine running the app
- pip

## Installation

1. Clone the repository:
   ```bash
   git clone https://github.com/EnugutalaMonika/face_detection.git
   cd face_detection
   ```

2. Create and activate a virtual environment:
   ```bash
   python -m venv venv
   # Windows
   venv\Scripts\activate
   # macOS/Linux
   source venv/bin/activate
   ```

3. Install dependencies:
   ```bash
   pip install -r requirements.txt
   ```

## Usage

1. Start the Flask server:
   ```bash
   python app.py
   ```

2. Open your browser and go to:
   ```
   http://127.0.0.1:8000
   ```

3. Click the **Start** button on the page to launch face detection. This opens a window showing your webcam feed with detected faces highlighted.

4. Close the detection window (or stop the script from your terminal) to end the session.

## Project Structure

```
face_detection/
├── app.py                 # Flask app entry point and routes
├── face_detection.py      # OpenCV face detection logic
├── templates/
│   └── index.html         # Web interface
├── requirements.txt       # Python dependencies
└── README.md
```

## Future Improvements

- Add a `/stop` endpoint to gracefully end detection from the web UI
- Stream the detected video feed directly into the browser instead of a separate OpenCV window
- Add face recognition/labeling on top of detection

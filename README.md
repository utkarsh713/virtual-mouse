<div align="center">

# 🖐️ AI Virtual Desktop Pro

### Control Your Computer With Hand Gestures

A futuristic AI-powered virtual desktop system that lets you control your computer using **hand gestures, computer vision, and real-time hand tracking**.

<br>

<img src="assets/ai-virtual-desktop-pro.png" alt="AI Virtual Desktop Pro" width="100%">

<br><br>

<img src="https://img.shields.io/badge/Python-3.11+-3776AB?style=for-the-badge&logo=python&logoColor=white">
<img src="https://img.shields.io/badge/OpenCV-Computer%20Vision-5C3EE8?style=for-the-badge&logo=opencv&logoColor=white">
<img src="https://img.shields.io/badge/MediaPipe-Hand%20Tracking-FF6F00?style=for-the-badge">
<img src="https://img.shields.io/badge/PyAutoGUI-Automation-00A67E?style=for-the-badge">

<br><br>

**Gesture Control** • **Computer Vision** • **Hands-Free Interaction**

</div>

---

# 🚀 About The Project

**AI Virtual Desktop Pro** is an AI-powered computer vision project that enables users to control their computer using **hand gestures instead of a traditional mouse and keyboard**.

The system uses a webcam to detect and track hand landmarks in real time. Different finger positions and gestures are mapped to desktop actions such as:

- 🖱️ Cursor movement
- 👆 Left click
- 🖱️ Right click
- 🖱️ Double click
- ✋ Drag and drop
- 📜 Scrolling
- 🔊 Volume control
- 💡 Brightness control
- 🎵 Media play/pause
- 📸 Screenshot
- 🌐 Application launching
- 🪟 Window switching
- 🖥️ Show desktop
- 🔒 Cursor locking

The goal is to provide a **natural, touch-free and interactive way of controlling a computer** using real-time computer vision.

---

# ✨ Key Features

| Feature | Description |
|---|---|
| 🖐️ Real-Time Hand Tracking | Detects hand landmarks using MediaPipe |
| 🖱️ Virtual Mouse | Controls the system cursor using the index finger |
| 👆 Gesture Clicking | Supports left, right and double click gestures |
| ✋ Drag & Drop | Drag objects using hand gestures |
| 📜 Gesture Scrolling | Scroll webpages and documents using finger movement |
| 🔊 Volume Control | Control system volume using pinch gestures |
| 💡 Brightness Control | Adjust screen brightness using finger gestures |
| 🎵 Media Control | Play or pause media using a thumbs-up gesture |
| 📸 Screenshot | Capture screenshots using a hand gesture |
| 🌐 Application Control | Launch applications using predefined gestures |
| 🪟 Window Control | Switch windows and show desktop |
| 🔒 Cursor Lock | Temporarily lock cursor movement |
| ⏸️ Control Pause | Pause gesture controls whenever required |
| 🎥 Real-Time Visualization | Displays hand landmarks and current actions |

---

# 🖐️ Gesture Controls

The project maps different hand gestures to desktop operations.

| Gesture | Action |
|---|---|
| ☝️ Index Finger | Move Cursor |
| 🤏 Thumb + Index | Left Click |
| 🤏 Thumb + Middle | Right Click |
| 🤏 Thumb + Ring | Double Click |
| 🤏 Thumb + Pinky | Drag & Drop |
| ✌️ Index + Middle | Scroll |
| 👍 Thumbs Up | Play / Pause |
| ✌️ Two Fingers | Brightness Control |
| 🤏 Pinch | Volume Control |
| 🤟 Three Fingers | Open Chrome |
| 🖐️ Four Fingers | Open Application |
| 🖐️ All Fingers | Take Screenshot |
| 👋 Swipe Left / Right | Previous / Next Track |
| 👇 Swipe Down | Switch Window |
| 👆 Swipe Up | Show Desktop |
| 🖐️ Open Palm | Cursor Pause |
| ✊ Fist | Cursor Lock |

---

# 🧠 How It Works

The system follows a real-time computer vision pipeline:

```text
                Webcam
                   ↓
          Capture Video Frame
                   ↓
          OpenCV Image Processing
                   ↓
           MediaPipe Hand Tracking
                   ↓
          Detect Hand Landmarks
                   ↓
          Gesture Recognition
                   ↓
        ┌──────────┼──────────┐
        ↓          ↓          ↓
     Cursor      Click      Control
        ↓          ↓          ↓
     PyAutoGUI   Mouse     System APIs
                   ↓
            Desktop Action
```

---

# 🔍 Hand Tracking

The webcam continuously captures frames and sends them to the computer vision pipeline.

MediaPipe detects the hand and provides landmark coordinates for different points of the hand.

```text
                Wrist
                  ●
             ●         ●
           ●             ●
         ●                 ●
       ●                     ●

     Thumb  Index  Middle  Ring  Pinky
```

These landmark positions are then used to calculate distances, movements and gesture patterns.

---

# 🖱️ Virtual Mouse

The **index finger** acts as the virtual mouse pointer.

```text
Camera
   ↓
Hand Detection
   ↓
Index Finger Position
   ↓
Screen Coordinate Mapping
   ↓
Mouse Cursor Movement
```

The detected hand coordinates are mapped to the computer screen dimensions and controlled through PyAutoGUI.

---

# 👆 Click Controls

### Left Click

The distance between the **thumb and index finger** is calculated.

```text
Thumb + Index
      ↓
Distance Check
      ↓
Left Click
```

### Right Click

The distance between the **thumb and middle finger** is used.

```text
Thumb + Middle
      ↓
Distance Check
      ↓
Right Click
```

### Double Click

The **thumb and ring finger** gesture triggers a double click.

---

# ✋ Drag & Drop

The **thumb + pinky** gesture activates drag mode.

```text
Thumb + Pinky
      ↓
Drag Mode
      ↓
Mouse Button Down
      ↓
Move Hand
      ↓
Mouse Button Up
      ↓
Drop
```

---

# 📜 Scroll Control

The movement of the index finger is tracked vertically.

```text
Index Finger Movement
        ↓
Vertical Distance
        ↓
Direction Detection
        ↓
Scroll Up / Down
```

---

# 🔊 Volume Control

A pinch gesture between the thumb and index finger is used for volume control.

```text
Thumb + Index
      ↓
Distance Calculation
      ↓
Pinch Detection
      ↓
Volume Control
```

---

# 💡 Brightness Control

Two-finger interaction can be used to control screen brightness.

```text
Finger Position
      ↓
Vertical Mapping
      ↓
Brightness Value
      ↓
System Brightness
```

---

# 🎵 Media Control

A **thumbs-up gesture** can trigger media play/pause.

```text
👍 Thumbs Up
      ↓
Gesture Detection
      ↓
Media Command
      ↓
Play / Pause
```

---

# 📸 Screenshot

A dedicated hand gesture can capture the current screen.

```text
Screenshot Gesture
       ↓
Gesture Detection
       ↓
PyAutoGUI Screenshot
       ↓
AI_Screenshot.png
```

---

# 🌐 Application Control

Specific gestures can launch applications.

### Three Fingers

```text
Three Fingers
      ↓
Gesture Detection
      ↓
Open Chrome
```

### Four Fingers

```text
Four Fingers
      ↓
Gesture Detection
      ↓
Open Application
```

---

# 🪟 Desktop Controls

The system also supports additional desktop interaction.

```text
Swipe Left / Right
        ↓
Previous / Next Track

Swipe Down
        ↓
Switch Window

Swipe Up
        ↓
Show Desktop

Open Palm
        ↓
Pause Cursor

Fist
        ↓
Lock Cursor
```

---

# ⌨️ Keyboard Controls

The application provides keyboard shortcuts for additional control.

| Key | Action |
|---|---|
| `ESC` | Exit application |
| `P` | Pause / Resume controls |
| `L` | Lock / Unlock cursor |
| `H` | Show gesture help |

---

# 🛠️ Tech Stack

## Programming Language

- Python

## Computer Vision

- OpenCV
- MediaPipe

## Desktop Automation

- PyAutoGUI

## System Control

- Screen Brightness Control
- Pycaw
- Windows system APIs

## Development Tools

- Visual Studio Code
- Git
- GitHub

---

# 📦 Installation

## 1. Clone the Repository

```bash
git clone https://github.com/utkarsh713/AI-Virtual-Desktop.git
```

```bash
cd AI-Virtual-Desktop
```

---

## 2. Create Virtual Environment

```bash
python -m venv venv
```

### Windows

```bash
venv\Scripts\activate
```

### macOS / Linux

```bash
source venv/bin/activate
```

---

## 3. Install Dependencies

```bash
pip install opencv-python mediapipe pyautogui screen-brightness-control pycaw comtypes
```

Or, if `requirements.txt` is available:

```bash
pip install -r requirements.txt
```

---

# ▶️ Run the Project

Run the main Python file:

```bash
python virtual_mouse.py
```

After starting the application, the webcam window will open.

You should see:

```text
AI Virtual Desktop Pro
```

Make sure your webcam is available and your system has permission to access the camera.

---

# 📁 Project Structure

```text
AI-Virtual-Desktop/
│
├── assets/
│   └── ai-virtual-desktop-pro.png
│
├── virtual_mouse.py
│
├── requirements.txt
│
├── AI_Screenshot.png
│
└── README.md
```

---

# ⚙️ System Requirements

### Recommended

- Windows 10 / 11
- Python 3.10+
- Working webcam
- At least 4 GB RAM
- VS Code or another Python IDE

The project is primarily designed for **desktop environments** because it interacts directly with the mouse, keyboard, screen brightness, volume and applications.

---

# 🎯 Project Objectives

The project aims to explore how **computer vision and gesture recognition** can be used to create a more natural human-computer interaction system.

### Main objectives

- Reduce dependency on physical input devices
- Explore real-time hand tracking
- Implement gesture-based interaction
- Control desktop operations through computer vision
- Combine AI with practical desktop automation
- Build an accessible and interactive user interface

---

# 🔮 Future Improvements

Potential future improvements include:

- 🤖 More accurate gesture recognition
- 🧠 Custom machine learning gesture classifier
- 👥 Multi-hand support
- 🎯 Improved cursor stabilization
- 🖥️ Cross-platform desktop support
- 🎮 Custom gesture mapping
- ⚙️ User-configurable gestures
- 📊 Gesture analytics
- 🗣️ Voice + Gesture combined control
- 📱 Integration with smart devices
- 🔐 Gesture-based authentication

---

# 📸 Project Preview

<div align="center">

<img src="assets/ai-virtual-desktop-pro.png" alt="AI Virtual Desktop Pro Preview" width="90%">

</div>

---

# 💡 Use Cases

This project can be useful for exploring:

- 🖥️ Touchless computer interaction
- ♿ Assistive technology
- 🤖 Human-computer interaction
- 👁️ Computer vision applications
- 🏠 Smart desktop environments
- 🎮 Gesture-based interfaces
- 🔬 AI/ML research projects
- 🎓 Academic and hackathon projects

---

# 👨‍💻 Developer

<div align="center">

### Utkarsh Barnwal

**BCA (Hons.) Computer Science Student**

Interested in:

`Java` • `Spring Boot` • `React.js` • `AI/ML` • `Computer Vision` • `DSA`

<br>

<a href="https://github.com/utkarsh713">
  <img src="https://img.shields.io/badge/GitHub-Utkarsh%20Barnwal-181717?style=for-the-badge&logo=github&logoColor=white">
</a>

</div>

---

# ⭐ Support

If you found this project interesting, consider giving the repository a ⭐ on GitHub.

<div align="center">

### 🖐️ AI Virtual Desktop Pro

**Control your computer.  
Without touching the mouse.**

🚀 **Computer Vision • Gesture Recognition • Desktop Automation**

</div>

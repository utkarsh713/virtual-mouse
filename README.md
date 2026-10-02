# 🖐️ AI Virtual Desktop Pro

<p align="center">
  <img src="https://capsule-render.vercel.app/api?type=waving&color=0:00F5FF,50:0066FF,100:8A2BE2&height=200&section=header&text=AI%20Virtual%20Desktop%20Pro&fontSize=42&fontAlignY=35&animation=fadeIn" width="100%" />
</p>

<p align="center">
  <strong>🤖 Control Your Desktop Using Hand Gestures & Computer Vision</strong>
</p>

<p align="center">
  <img src="https://img.shields.io/badge/Python-3.x-3776AB?style=for-the-badge&logo=python&logoColor=white" />
  <img src="https://img.shields.io/badge/OpenCV-Computer%20Vision-5C3EE8?style=for-the-badge&logo=opencv&logoColor=white" />
  <img src="https://img.shields.io/badge/MediaPipe-Hand%20Tracking-00A67E?style=for-the-badge" />
  <img src="https://img.shields.io/badge/PyAutoGUI-Desktop%20Control-FF6B35?style=for-the-badge" />
  <img src="https://img.shields.io/badge/AI-Gesture%20Control-8A2BE2?style=for-the-badge" />
</p>

<p align="center">
  🖱️ Cursor • 👆 Click • 🤏 Drag • ↕️ Scroll • ☀️ Brightness • 🎵 Media • 📸 Screenshot
</p>

---

## 🚀 About The Project

**AI Virtual Desktop Pro** is a computer-vision based desktop control system that lets you interact with your computer using **hand gestures instead of a physical mouse**.

The project uses **OpenCV** for webcam processing, **MediaPipe Hands** for hand-landmark detection, **PyAutoGUI** for controlling the operating system, and **Screen Brightness Control** for display brightness management.

The webcam tracks a hand in real time, detects the current gesture, and converts that gesture into a desktop action. fileciteturn33file0L123-L159

---

## ✨ Key Features

| Feature | Gesture / Control |
|---|---|
| 🖱️ Cursor Movement | Index finger |
| 👆 Left Click | Thumb + Index pinch |
| 🖱️ Right Click | Thumb + Middle pinch |
| 🖱️ Double Click | Thumb + Ring pinch |
| 🤏 Drag & Drop | Thumb + Pinky pinch |
| ↕️ Scrolling | Index + Middle fingers |
| 🎵 Play / Pause | Thumbs Up |
| ☀️ Brightness Control | Two fingers |
| 🌐 Open Chrome | Three fingers |
| 📂 Open Explorer / App | Four fingers |
| 📸 Screenshot | Open hand / all fingers |
| ⏸️ Cursor Pause | Open Palm |
| 🔒 Cursor Lock | Fist |
| 👈 Swipe Left | Previous Track |
| 👉 Swipe Right | Next Track |
| ⬆️ Swipe Up | Show Desktop |
| ⬇️ Swipe Down | Switch Window |
| ⏸️ Pause Controls | `P` key |
| 🔒 Lock / Unlock Cursor | `L` key |
| ❓ Help Panel | `H` key |
| 🚪 Exit | `ESC` |

The gesture mappings and keyboard controls are implemented in the current project source. fileciteturn33file0L35-L69

---

## 🧠 How It Works

```text
             📷 WEBCAM
                 │
                 ▼
        ┌─────────────────┐
        │    OpenCV       │
        │ Frame Capture   │
        └────────┬────────┘
                 │
                 ▼
        ┌─────────────────┐
        │   MediaPipe     │
        │ Hand Detection  │
        └────────┬────────┘
                 │
                 ▼
        ┌─────────────────┐
        │ 21 Hand         │
        │ Landmarks       │
        └────────┬────────┘
                 │
                 ▼
        ┌─────────────────┐
        │ Gesture Engine  │
        │ Pinch / Fingers │
        │ Swipe / Pose    │
        └────────┬────────┘
                 │
                 ▼
        ┌─────────────────┐
        │ Action Mapping  │
        └────────┬────────┘
                 │
       ┌─────────┼─────────┐
       ▼         ▼         ▼
    🖱️ Mouse   ⌨️ Keys   🖥️ Desktop
```

---

## 🎯 Gesture System

### 🖱️ Mouse Controls

**Index Finger**
```text
☝️
```
Move the index finger to control the desktop cursor.

**Thumb + Index**
```text
🤏
```
Performs a left click.

**Thumb + Middle**
```text
🤏
```
Performs a right click.

**Thumb + Ring**
```text
🤏
```
Performs a double click.

**Thumb + Pinky**
```text
🤏
```
Starts drag mode. Releasing the gesture ends the drag.

---

## 📜 Scrolling

Raise your **index + middle fingers** together:

```text
☝️🖕
```

Move your hand vertically to scroll up or down.

The project includes cooldown handling to reduce excessive scrolling. fileciteturn33file0L1495-L1547

---

## 🎵 Media Control

### 👍 Thumbs Up

A thumbs-up gesture triggers:

```text
Play / Pause
```

The media command is sent through PyAutoGUI's media key handling. fileciteturn33file0L1557-L1579

Swipe gestures can also control tracks:

```text
👈  → Previous Track

👉  → Next Track
```

---

## ☀️ Brightness Control

With **two fingers**, the position of the index finger is mapped to a brightness value.

```text
Higher hand position
        ↓
Higher brightness

Lower hand position
        ↓
Lower brightness
```

The project uses `screen-brightness-control` to apply the brightness value. fileciteturn33file0L1643-L1665

---

## 📸 Screenshot

Show all fingers:

```text
🖐️
```

The application captures the current desktop screen and saves it inside:

```text
Screenshots/
```

Screenshots are automatically named using the current date and time. fileciteturn33file0L447-L467

Example:

```text
Screenshots/
├── Screenshot_2026-10-02_18-30-21.png
├── Screenshot_2026-10-02_18-32-04.png
└── Screenshot_2026-10-02_18-35-17.png
```

---

## 🌐 Quick Desktop Actions

### Three Fingers

```text
🖖
```

Opens Chrome.

### Four Fingers

```text
🖐️
```

Opens File Explorer on Windows.

On other systems, the project attempts to open VS Code.

---

## 👈👉 Swipe Controls

The project tracks movement of the palm center to detect swipe actions.

```text
Swipe Right  → Next Track
Swipe Left   → Previous Track
Swipe Up     → Show Desktop
Swipe Down   → Switch Window
```

Swipe cooldown prevents repeated actions from firing continuously. fileciteturn33file0L697-L761

---

## 🔒 Safety & Control Modes

### ✋ Open Palm

```text
🖐️
```

Pauses cursor control.

### ✊ Fist

```text
✊
```

Locks the cursor.

### Keyboard Controls

| Key | Action |
|---|---|
| `P` | Pause / Resume all controls |
| `L` | Lock / Unlock cursor |
| `H` | Open gesture help |
| `ESC` | Exit application |

These controls are handled directly inside the main application loop. fileciteturn33file0L1821-L1903

---

## 🧩 Technologies Used

<p align="center">
  <img src="https://skillicons.dev/icons?i=python,opencv" />
</p>

### Core Technologies

- 🐍 **Python**
- 👁️ **OpenCV**
- ✋ **MediaPipe**
- 🖱️ **PyAutoGUI**
- ☀️ **Screen Brightness Control**
- 🖥️ **OS / subprocess APIs**

### Libraries

```text
opencv-python
mediapipe
pyautogui
screen-brightness-control
```

The source initializes the webcam at up to **1280 × 720** and uses MediaPipe Hands for real-time landmark tracking. fileciteturn33file0L77-L159

---

## 📦 Installation

### 1. Clone the Repository

```bash
git clone https://github.com/yourusername/ai-virtual-desktop-pro.git
cd ai-virtual-desktop-pro
```

### 2. Install Dependencies

```bash
pip install opencv-python mediapipe pyautogui screen-brightness-control
```

### 3. Run

```bash
python AI_Virtual_Desktop_Pro.py
```

---

## 📁 Project Structure

```text
AI-Virtual-Desktop-Pro/
│
├── AI_Virtual_Desktop_Pro.py
├── Screenshots/
│   └── generated screenshots
│
└── README.md
```

---

## ⚙️ Configuration

The project provides configurable values for:

```python
settings = {
    "smoothing": 0.30,
    "click_ratio": 0.30,
    "release_ratio": 0.45,
    "scroll_speed": 4,
    "swipe_threshold": 110,
    "show_landmarks": True,
    "stable_frames": 2
}
```

These settings control cursor smoothing, pinch sensitivity, scroll speed, swipe sensitivity, landmark display, and gesture stabilization. fileciteturn33file0L99-L113

---

## 🎥 User Interface

The application displays a live webcam window containing:

- 🤖 Application title
- ✋ Detected gesture
- 📊 Gesture confidence
- 🖐️ Number of detected hands
- 🖱️ Cursor status
- ⏯️ Control mode
- ⚡ Last performed action
- 🟢 Hand landmarks
- ⌨️ Keyboard shortcut bar

The status panel and live gesture visualization are rendered directly using OpenCV. fileciteturn33file0L777-L953

---

## 🛡️ Stability Features

The project includes several mechanisms to make gesture interaction more reliable:

- 🎯 Gesture stabilization
- ⏱️ Action cooldowns
- 🔒 Click latches
- 🖱️ Drag release handling
- 🧮 Palm-size based pinch detection
- 🎚️ Cursor smoothing
- 🛑 PyAutoGUI failsafe
- 📷 Camera permission/error handling

Pinch detection uses palm-relative measurements so the gesture can work at different distances from the camera. fileciteturn33file0L249-L289

---

## 🔮 Future Enhancements

Possible future upgrades:

- 🤖 AI gesture learning
- ✋ Two-hand gesture combinations
- 🔊 Dedicated gesture-based volume control
- 🎚️ On-screen sensitivity settings
- 🎮 Custom gesture mapping
- 🪟 Application-specific controls
- 🎙️ Voice + gesture hybrid control
- 🧠 ML-based personalized gesture recognition
- 📊 Gesture usage analytics
- 🌈 Modern graphical control dashboard
- 🔐 Gesture-based system unlock
- 🖥️ Multi-monitor cursor control
- 🎥 Gesture-controlled presentations
- 🎮 Gesture-controlled games

---

## ⚠️ Notes

- A webcam is required.
- Good lighting improves hand detection.
- Keep the hand clearly visible inside the camera frame.
- Desktop actions depend on the operating system and application receiving the generated mouse/keyboard/media events.
- Brightness control depends on hardware/OS support.
- The current source contains a volume-key helper, but no active gesture mapping invokes it yet.

---

## 👨‍💻 Author

**Utkarsh Barnwal**

BCA | Developer | AI/ML Enthusiast

---

## ⭐ Support

If you like this project:

```text
⭐ Star the repository
🍴 Fork it
💻 Try it
🚀 Build your own gesture controls
```

<p align="center">
  Made with ❤️ + 🐍 Python + 👁️ Computer Vision
</p>

<p align="center">
  <strong>Turn your webcam into a virtual mouse. 🖐️🖥️</strong>
</p>

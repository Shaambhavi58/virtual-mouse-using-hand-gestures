# Virtual Mouse Using Hand Gestures

A hand gesture recognition system using **OpenCV**, **MediaPipe**, and **PyAutoGUI** to control the mouse in real-time.

---

## ✨ Features

- **Cursor Control**: Move the mouse cursor with your index finger.
- **Left Click**: Tap gesture using index and thumb.
- **Right Click**: Two-finger gesture (index + middle).
- **Double Click**: Close all fingers except thumb and index.
- **Screenshot**: Close all fingers (fist gesture).
- **Real-Time Feedback**: Displays detected gesture on screen.
- **Cross-Platform**: Works on Windows, macOS, and Linux.

---

## 🛠️ Tech Stack

- **Python 3.9+**
- [OpenCV](https://opencv.org/) - Real-time image processing  
- [MediaPipe](https://google.github.io/mediapipe/) - Hand landmark detection  
- [PyAutoGUI](https://pyautogui.readthedocs.io/) - Mouse and keyboard control  
- [Pynput](https://pypi.org/project/pynput/) - Low-level mouse interactions  

---

## 📂 Project Structure
Virtual-Mouse-Using-Hand-Gestures/
│── Virtual Mouse.ipynb # Main Jupyter Notebook
│── util.py # Utility functions (angles, distances)
│── README.md # Documentation
│── requirements.txt # Dependencies
│── screenshots/ # Saved screenshots (auto-generated)

---

## 🚀 Setup & Installation
1. **Clone this repository:**
   ```bash
   git clone https://github.com/Shaambhavi58/virtual-mouse-using-hand-gestures.git
   cd virtual-mouse-using-hand-gestures
2. **Create a virtual environment (optional but recommended):**
python -m venv venv
source venv/bin/activate  # On Mac/Linux
venv\Scripts\activate     # On Windows
3. **Install Dependencies:**
pip install -r requirements.txt
4. **Run the Project:**
python Virtual_Mouse.ipynb

---

## 🎮 Usage Flow
1.Launch the program (via Jupyter Notebook or Python script).
2.Place your hand in front of the webcam.
3.Perform gestures:
-Move cursor → point with index finger.
-Pinch thumb + index → left click.
-Pinch thumb + ring finger → right click.
-Close fist → double click.
-Close all fingers → take screenshot (saved in / screenshots).

---

## 🔧 Technical Implementation
**Hand Landmark Detection**
  -Uses 21 keypoints per hand from MediaPipe.
  -Coordinates normalized to screen resolution.
**Gesture Recognition Logic**
  -Angles calculated using 3 landmarks (via util.get_angle).

  -Distances (Euclidean norm) used for pinch/screenshot logic.
  -Example:
  if util.get_angle(landmarks[5], landmarks[6], landmarks[8]) < 50:
   (#Index finger bent)
**Mouse Control**
  -Pynput.Controller for button press/release events.
  -PyAutoGUI for screenshots and double clicks.

---

## 📸 Demo

  -Move Mouse: Index finger moves cursor
  -Left Click: Thumb + index pinch
  -Right Click: Index + middle pinch
  -Double Click: Close fingers
  -Screenshot: Fist gesture

  ---

## 📈 Future Enhancements
  -Add multi-hand support.
  -Integrate gesture customization.
  -Optimize for low-light environments.
  -Build standalone desktop app (PyInstaller).

---
## 📜 License

This project is licensed under the MIT License.
See [LICENSE](LICENSE) file for more details.

---

## 🙌 Credits

-[OpenCV](https://opencv.org/) for computer vision.
-[MediaPipe](https://mediapipe.dev/)for landmark detection.
-[PyAutoGUI](https://pypi.org/project/PyAutoGUI/) & [Pynput](https://pypi.org/project/pynput/) for mouse automation.

---

##🔗 Source Code
[![Source Code](https://img.shields.io/badge/Source%20Code-GitHub-black?style=flat&logo=github)](https://github.com/Shaambhavi58/virtual-mouse-using-hand-gestures)
GitHub Repository


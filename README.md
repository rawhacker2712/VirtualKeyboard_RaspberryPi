# 🖐️ Two-Hand Virtual Keyboard Using OpenCV and cvzone

This project uses computer vision to recognize hand gestures from **two hands** via webcam and simulate **keyboard number input (0-9)** using `pyautogui`.

## 🛠️ Tech Used

- Python
- OpenCV
- [cvzone](https://github.com/cvzone/cvzone)
- PyAutoGUI

## 💡 How It Works

- The webcam captures hand landmarks using `cvzone.HandDetector`.
- The project checks for two hands.
- Based on the number of fingers shown by both hands, it maps the combination to a digit.
- It simulates a keyboard press (`press('1')`, etc.)
- Closes when a specific gesture is made.

## 🔢 Finger Gesture Mapping

| Finger Pattern (10)      | Output |
|--------------------------|--------|
| [0,1,0,0,0,0,0,0,0,0]     | 1      |
| [0,1,1,0,0,0,0,0,0,0]     | 2      |
| [1,1,1,1,1,0,1,1,1,1]     | 9      |
| [1]*10                   | 0      |
| [0,0,0,0,0,0,1,1,0,0]     | Exit   |

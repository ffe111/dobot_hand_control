# Dobot Hand Control

English | [ภาษาไทย](README.th.md)

A Raspberry Pi robotics prototype that maps webcam hand gestures to Dobot arm movement. MediaPipe detects hand landmarks, OpenCV handles camera input, and PyDobot sends commands over a serial connection.

## Where to start

| File | Purpose |
| --- | --- |
| [`track.py`](track.py) | Camera input and gesture-to-movement mapping |
| [`dobot.py`](dobot.py) | Serial connection and a manual control menu |
| [`requirement.txt`](requirement.txt) | Python dependencies |

The code targets Linux with a webcam and a compatible Dobot connected over serial. Use Python 3.10 or newer (the manual menu uses `match`) and a virtual environment: `python -m pip install -r requirement.txt`. Review `serial_port` in `dobot.py` for your setup. The manual entry point is `python dobot.py`; the webcam entry point is `python track.py`.

## Hardware precautions

Connecting commands the arm to move, and frequent gesture events can overwhelm the controller. Clear the workspace, keep people out of reach of the arm, and confirm you can stop motion before testing either entry point. This is a prototype, not a safety-rated control system. Contributions that make gesture input more predictable, such as debouncing, are welcome.

<!-- Maintainers: Update the English README first, then mirror the change in README.th.md. -->

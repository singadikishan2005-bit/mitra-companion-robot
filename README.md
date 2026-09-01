# MITRA (मित्र) — AI Emotionally Intelligent Companion Robot

<div align="center">

[![Portfolio Demo](https://img.shields.io/badge/Live_Demo-View_MITRA_on_Portfolio-06B6D4?style=for-the-badge&logo=google-chrome)](https://kishan-sp-portfolio.surge.sh)
![Python](https://img.shields.io/badge/Python-3776AB?style=flat-square&logo=python&logoColor=white)
![OpenCV](https://img.shields.io/badge/OpenCV-5C3EE8?style=flat-square&logo=opencv&logoColor=white)
![Flask](https://img.shields.io/badge/Flask-000000?style=flat-square&logo=flask&logoColor=white)
![Raspberry Pi](https://img.shields.io/badge/Raspberry_Pi-A22846?style=flat-square&logo=raspberry-pi&logoColor=white)
![Arduino](https://img.shields.io/badge/Arduino-00979D?style=flat-square&logo=arduino&logoColor=white)

</div>

---

## What is MITRA?

MITRA (meaning "Friend" in Sanskrit) is a fully autonomous AI companion robot that:

- Recognizes **8 Ekman human emotions** in real time using computer vision
- Displays **animated emotional responses** on a 128x64 SSD1306 OLED display
- Responds to voice commands via **offline wake-word detection** and speech recognition
- Navigates autonomously with **ultrasonic obstacle avoidance**
- Runs a **Flask REST API backend** for state management and remote control

> *Built as a Final Year Engineering Project at S.J.C. Institute of Technology (VTU)*

---

## System Architecture

```
┌─────────────────────────────────────────────────────┐
│                   MITRA System                      │
├──────────────┬──────────────────┬───────────────────┤
│  Vision Layer│   Backend Layer  │  Hardware Layer   │
│              │                  │                   │
│  Webcam      │  Flask REST API  │  Raspberry Pi 4   │
│  OpenCV FER  │  SQLite DB       │  Arduino Nano     │
│  8 Emotions  │  Token Auth      │  L298N H-Bridge   │
│  Real-time   │  Offline Queue   │  HC-SR04 Sonar    │
│              │  Auto-sync       │  SSD1306 OLED     │
├──────────────┴──────────────────┴───────────────────┤
│              Voice Assistant Layer                   │
│  Picovoice Porcupine (wake-word) + Vosk STT         │
│  pyttsx3 TTS + NLP response engine                  │
└─────────────────────────────────────────────────────┘
```

---

## Key Features

| Feature | Details |
|:---|:---|
| Emotion Recognition | 8 Ekman emotions via OpenCV + FER library |
| OLED Facial Display | 128x64 SSD1306 displaying animated emotion faces |
| Voice Wake Word | "Hey MITRA" via Picovoice Porcupine (offline) |
| Speech-to-Text | Vosk STT engine (fully offline, no cloud) |
| Text-to-Speech | pyttsx3 (offline) |
| Motor Control | L298N H-Bridge driven by Arduino Nano |
| Obstacle Avoidance | HC-SR04 ultrasonic sensor with auto-stop |
| REST API | Flask with SQLite, token auth, request queuing |
| Mobile UI | Flet cross-platform dashboard for remote control |
| Testing | 14 automated tests (pytest) with CI/CD on push |

---

## Tech Stack

| Layer | Technology |
|:---|:---|
| Computer Vision | Python 3.11, OpenCV 4.9, FER 22.5 |
| Voice AI | Picovoice Porcupine, Vosk, pyttsx3 |
| Backend | Flask 3.0, SQLite, REST API |
| Embedded | Raspberry Pi 4 (4GB), Arduino Nano |
| Actuators | L298N Motor Driver, HC-SR04 Sonar |
| Display | SSD1306 128x64 OLED (I2C) |
| Mobile UI | Flet (Flutter-based Python UI) |
| Testing | pytest, GitHub Actions CI/CD |

---

## Project Context

- **Type**: B.E. Final Year Project — AI & Data Science
- **Institution**: S.J.C. Institute of Technology, Bengaluru (Affiliated: VTU)
- **USN**: 1SJ23AD019
- **Developer**: Kishan S P

---

## Interactive Demo

Visit the live MITRA OLED simulator at: [kishan-sp-portfolio.surge.sh](https://kishan-sp-portfolio.surge.sh)

---

## Author

**Kishan S P** — AI & Embedded Systems Engineer
- Portfolio: https://kishan-sp-portfolio.surge.sh
- LinkedIn: https://www.linkedin.com/in/kishan-s-p-2766282bb
- Email: singadikishan2005@gmail.com

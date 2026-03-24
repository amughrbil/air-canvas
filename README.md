# 🎨 Air Canvas Drawing Engine

[![Live Demo](https://img.shields.io/badge/demo-live_now-brightgreen?style=for-the-badge&logo=vercel)](air-canvas-pi.vercel.app)

A bare-metal, native HTML/JS drawing engine using Google MediaPipe. This allows users to draw on the screen using real-time hand tracking and computer vision, with zero external UI frameworks (no React, no extra dependencies).
## 🚀 Getting Started

Because this application requires webcam access, modern browsers will block camera permissions if you try to run the file directly (`file:///` protocol). You **must** run it through a local server.

### Running with VS Code 
1. Open this project folder in **VS Code**.
2. Install the **Live Server** extension if you haven't already.
3. Right-click `index.html` and select **"Open with Live Server"**.
4. The app will open in your browser (usually at `http://localhost:5500`).
5. **Accept the camera permissions** when prompted!

### Pro Tips for Best Performance
* **Lighting:** Ensure your hands and face are clearly visible in the camera frame.
* **Full Screen:** Hit `F11` (or `Fn + F11`) for a more immersive drawing experience.

## 🎮 Gesture Controls

The engine uses a strict 1:1 screen mapping and custom "bone measurement" math to prevent accidental ghost triggers.

| Gesture | Action |
| :--- | :--- |
| 🎯 **Left Hand (Index)** | Acts as your laser pointer / cursor. |
| 🤏 **Right Hand (Pinch)** | Draw on the canvas or click UI buttons. |
| ✋ **Right Hand (Open Palm)** | Acts as a radius eraser. Swipe over lines to delete. |
| ✌️ **Right Hand (Peace Sign)** | Toggles screen lock (Hold for 5 frames). |
| ↩️ **Undo Button** | Hover and pinch to delete your last stroke. |
| 🎨 **Color Wheel** | Hover to preview; pinch to select a color. |

## 🛠️ Technical Stack

This engine is built focusing on performance and mathematical stability:

* **Core Tracking:** Powered by `@mediapipe/hands` and `@mediapipe/face_mesh`.
* **Stability:** Implements a `OneEuroFilter` to ensure a highly stabilized, jitter-free cursor.
* **Memory Management:** Features a custom smart-undo history stack to manage canvas states efficiently.
* **No Frameworks:** 100% Vanilla JavaScript, HTML5 Canvas, and CSS3.

## 📜 License

This project is licensed under the **MIT License** - see the [LICENSE](LICENSE) file for details.


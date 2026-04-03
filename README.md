# 🎨 VisualPainter

A real-time **AI-powered air drawing application** that lets you paint on screen using just your fingers — no mouse, no touch screen needed. Built with Python, OpenCV, and MediaPipe.

---

## ✨ Demo

> Move your index finger to draw. Raise two fingers to pause. Switch colors using the header menu.

---

## 🚀 Features

- 🖐️ **Hand gesture recognition** using MediaPipe to track finger positions in real time
- 🎨 **Draw in the air** — use your index finger as a brush via webcam
- 🖍️ **Multiple colors** selectable from an on-screen header
- 🧹 **Eraser mode** to clear strokes
- ⚡ **Smooth, low-latency** rendering with OpenCV

---

## 🛠️ Tech Stack

| Tool | Purpose |
|------|---------|
| Python | Core language |
| OpenCV | Webcam feed & canvas rendering |
| MediaPipe | Hand landmark detection |
| NumPy | Array/image manipulation |

---

## 📁 Project Structure

```
VisualPainter/
├── visualPainterMain.py     # Main application entry point
├── HandsTrackingModule.py   # Hand detection & landmark tracking module
├── Header/                  # Color selection header images
└── README.md
```

---

## ⚙️ Installation & Setup

**Prerequisites:** Python 3.7+, a working webcam

```bash
# 1. Clone the repository
git clone https://github.com/kartiksuri10/VisualPainter.git
cd VisualPainter

# 2. Install dependencies
pip install opencv-python mediapipe numpy

# 3. Run the app
python visualPainterMain.py
```

---

## 🎮 How to Use

| Gesture | Action |
|---------|--------|
| ☝️ Index finger up | Draw mode — paint on canvas |
| ✌️ Two fingers up | Selection mode — pick color from header |
| Select header color | Switch brush color |
| Select eraser | Erase strokes |

---

## 💡 How It Works

1. Webcam captures live video feed
2. MediaPipe identifies 21 hand landmarks per frame
3. Fingertip position (landmark 8) is tracked across frames
4. OpenCV draws strokes on a transparent overlay, merged with the live feed
5. Header UI allows color/tool switching via gesture-based selection

---

## 🔮 Future Improvements

- [ ] Save canvas as image file
- [ ] Adjust brush thickness with gesture
- [ ] Multi-hand support
- [ ] Shape recognition mode

---

## 🧑‍💻 Author

**Kartik Suri** — [GitHub](https://github.com/kartiksuri10)

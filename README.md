# 🎨 VisualPainter
A real-time **AI-powered air drawing application** that lets you paint and draw geometric shapes on screen using just your fingers — no mouse, no touch screen needed. Built with Python, OpenCV, and MediaPipe.

---

## ✨ Demo
> Move your index finger to draw. Raise two fingers to pause and auto-recognize your shape. Switch colors using the header menu.

---

## 🚀 Features
- 🖐️ **Hand gesture recognition** using MediaPipe to track finger positions in real time
- 🎨 **Draw in the air** — use your index finger as a brush via webcam
- 🔷 **Automatic shape recognition** — draw freehand and the app snaps it to a clean rectangle, circle, triangle, or line
- 🖍️ **Multiple colors** selectable from an on-screen header
- 🧹 **Eraser mode** to clear strokes
- ⚡ **Smooth, low-latency** rendering with OpenCV

---

## 🛠️ Tech Stack
| Tool | Purpose |
|------|---------|
| Python | Core language |
| OpenCV | Webcam feed, canvas rendering & shape drawing |
| MediaPipe | Hand landmark detection |
| NumPy | Array/image manipulation |
| SciPy | Euclidean distance calculations for shape detection |

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


## 🎮 How to Use
| Gesture | Action |
|---------|--------|
| ☝️ Index finger up | Draw mode — paint freehand on canvas |
| ✌️ Two fingers up | Selection mode — finalizes & recognizes your shape |
| Select header color | Switch brush color |
| Select eraser | Erase strokes |

---

## 🔷 Shape Recognition
When you switch to **selection mode** (two fingers up), VisualPainter analyzes your freehand stroke and automatically snaps it to the nearest clean geometric shape:

| Shape | How it's detected |
|-------|-------------------|
| **Line** | Fewer than 5 recorded points |
| **Rectangle** | 85%+ of points lie near the bounding box edges |
| **Circle** | All points stay within a consistent radius from the centroid (±20px tolerance) |
| **Triangle** | Contour approximation yields exactly 3 vertices |

Once recognized, the freehand stroke is replaced with a clean, pixel-perfect version of the shape drawn in your selected color.

---

## 💡 How It Works
1. Webcam captures live video feed
2. MediaPipe identifies 21 hand landmarks per frame
3. Fingertip position (landmark 8) is tracked across frames
4. OpenCV draws strokes on a transparent overlay, merged with the live feed
5. On switching to selection mode, all recorded points are passed through the shape recognition pipeline
6. The recognized shape is redrawn cleanly on the canvas, replacing the freehand stroke
7. Header UI allows color/tool switching via gesture-based selection

---

## 🔮 Future Improvements
- [ ] Save canvas as image file
- [ ] Adjust brush thickness with gesture
- [ ] Multi-hand support
- [ ] Recognize more shapes (pentagon, star, arrow)
- [ ] Confidence score display for shape recognition

---

## 🧑‍💻 Author
**Kartik Suri** — [LinkedIn](https://www.linkedin.com/in/kartik-suri/)

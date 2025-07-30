# 👋 Hi there, I'm Deep Rudra!
🎓 I'm an Electronics and Communication Engineering student at Kalyani Government Engineering College with hands-on experience in embedded systems, robotics, VLSI, and machine learning. I enjoy solving real-world problems through technology and continuously seek to learn, innovate, and contribute with energy and teamwork.



# 🎨 Air Canvas Drawing Tool (Color Marker-Based Virtual Whiteboard) 

This is a computer vision-based air drawing tool that allows users to draw on a virtual whiteboard using colored markers tracked in real-time via a webcam. It uses OpenCV and NumPy to detect the position of a colored object (marker) and translate its motion into drawn lines on a canvas. The GUI includes color selection and a "Clear" button to reset the canvas.

---

## 🛠️ Features

- Real-time color marker tracking via webcam
- Interactive canvas with:
  - Color buttons (Blue, Green, Red, Yellow)
  - "Clear" button to reset the drawing
- Custom HSV trackbars to adjust color detection range
- Supports drawing in 4 different colors
- Displays:
  - Live webcam feed with marker detection
  - The whiteboard canvas
  - The binary mask of the tracked object

---

## 🧠 Technologies Used

| Library         | Purpose                             |
|----------------|-------------------------------------|
| `OpenCV`       | Video capture, GUI, image processing |
| `NumPy`        | Matrix operations, kernel creation   |
| `collections.deque` | Store drawing points for each color |

---

## 🖥️ How It Works

1. Launches webcam and detects a colored object based on adjustable HSV values.
2. When the marker is moved:
   - Inside the button area → performs button actions (clear or color select)
   - Outside the button area → draws on the whiteboard
3. The contour of the object is detected and used to calculate the center, which determines where to draw.
4. Lines are continuously drawn between previous and current positions using OpenCV.

---

## 🎛️ GUI Controls

- `Trackbars`: Adjust HSV values to fine-tune marker detection.
- `Canvas Buttons`:  
  - 🎨 Color selection: Blue, Green, Red, Yellow  
  - 🧹 Clear button: Clears the canvas
## 📦 Requirements

Install the following Python packages:

```bash
pip install numpy opencv-python

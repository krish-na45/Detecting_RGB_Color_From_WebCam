# 🎨 Real-Time Color Detection using OpenCV

## 📌 Project Overview

This project is a simple **Computer Vision application** that detects the **dominant color (Red, Green, or Blue)** from a live webcam feed using **OpenCV and NumPy**.

The program captures frames from the webcam, separates the RGB channels, calculates the **mean intensity of each channel**, and determines which color is dominant in the frame.

This project demonstrates basic concepts of:

* Image processing
* Color channel manipulation
* Real-time webcam streaming
* Computer vision using Python

---

## ⚙️ Technologies Used

* **Python**
* **OpenCV**
* **NumPy**

---

## 📂 Project Structure

```
CV-Color-Detection/
│
├── proj.py
├── README.md
└── requirements.txt
```

---

## 🧠 How the Program Works

1. The webcam captures frames in real-time using OpenCV.
2. Each frame is split into **Blue, Green, and Red channels**.
3. The **mean value of each channel** is calculated.
4. The channel with the **highest average intensity** is considered the dominant color.
5. The detected color is printed in the console.

---

## ▶️ How to Run the Project

### Step 1: Install dependencies

```bash
pip install opencv-python numpy
```

### Step 2: Run the script

```bash
python proj.py
```

### Step 3: Exit the program

Press **Q** on the keyboard to close the webcam window.

---

## 🖥️ Example Output

Console Output:

```
Blue
Blue
Green
Red
Red
```

Webcam Window:
Displays the **live camera feed**.

---

## 📊 Code Explanation

### 1. Capture Video from Webcam

```python
vid = cv2.VideoCapture(0)
```

### 2. Split RGB Channels

```python
b = frame[:, :, 0]
g = frame[:, :, 1]
r = frame[:, :, 2]
```

### 3. Calculate Mean Intensity

```python
b_mean = np.mean(b)
g_mean = np.mean(g)
r_mean = np.mean(r)
```

### 4. Detect Dominant Color

```python
if b_mean > g_mean and b_mean > r_mean:
    print("Blue")
```

---

## 🚀 Possible Improvements

* Display detected color **on the video frame**
* Add **HSV color detection**
* Detect **multiple colors**
* Create **colored bounding boxes**
* Build a **real-time color detector for objects**

---

## 📚 Learning Outcomes

This project helps understand:

* Image pixel structure
* RGB color space
* Basic computer vision workflow
* Real-time image processing with OpenCV

---

## 👨‍💻 Author

**Krishna Mishra**
B.Tech – Artificial Intelligence & Data Science

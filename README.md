# 🚗 Lane Detection using OpenCV

## 📌 Project Overview

This project implements a **lane detection pipeline** using computer vision techniques to identify road lane boundaries from images. The system processes input images and highlights lane lines, which can be used in applications like **autonomous driving and driver assistance systems (ADAS)**.

---

## 🎯 Objectives

* Detect edges of the road using image processing techniques
* Identify lane boundaries using Hough Transform
* Apply Region of Interest (ROI) to focus on the road area
* Visualize detected lane lines on the original image

---

## 🧠 Technologies Used

* Python
* OpenCV
* NumPy
* Matplotlib

---

## ⚙️ Pipeline

The lane detection process follows these steps:

1. **Image Acquisition**

   * Load image using OpenCV

2. **Grayscale Conversion**

   * Simplifies image by removing color information

3. **Gaussian Blur**

   * Reduces noise for better edge detection

4. **Edge Detection (Canny)**

   * Detects edges in the image

5. **Region of Interest (ROI)**

   * Masks irrelevant areas and focuses only on the road

6. **Hough Transform**

   * Detects straight lines (lane boundaries)

7. **Overlay**

   * Draw detected lane lines on the original image

---

## 🧪 Example Workflow

```python
img = cv2.imread('road.jpg')
gray = cv2.cvtColor(img, cv2.COLOR_BGR2GRAY)
blur = cv2.GaussianBlur(gray, (5,5), 0)
edges = cv2.Canny(blur, 50, 150)

roi = region_of_interest(edges)

lines = cv2.HoughLinesP(roi, 1, np.pi/180, 100, minLineLength=50, maxLineGap=10)
```

---

## 📊 Output

* Edge-detected image
* Masked ROI
* Final image with detected lane lines

---

## 🚀 Features

* Works on static road images
* Detects multiple lane lines
* Customizable ROI
* Adjustable parameters for edge and line detection

---

## ⚠️ Limitations

* Works best on clear road images
* Sensitive to lighting conditions
* Cannot handle curved lanes (basic implementation)

---

## 🔥 Future Improvements

* Lane averaging (left & right lane detection)
* Real-time video processing
* Curved lane detection
* Integration with steering prediction models

---

## 💼 Use Cases

* Autonomous vehicles
* Driver assistance systems (ADAS)
* Road analysis and monitoring

---

## 👨‍💻 Author

**Aaryan Khadka**

---

## ⭐ Conclusion

This project demonstrates a fundamental approach to lane detection using classical computer vision techniques. It serves as a strong foundation for building more advanced autonomous driving systems.

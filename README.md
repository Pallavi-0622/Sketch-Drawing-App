# ✏️ Pencil Sketch Converter

This project allows you to convert normal images into pencil sketch-style images using Python and OpenCV.

## 📸 Overview

Using basic image processing techniques like grayscale conversion, Gaussian blur, and image division, this tool transforms photos into realistic pencil sketches.

## 🛠️ Technologies Used

- Python 3.x
- OpenCV (`cv2`)

## 📁 File Structure

Sketch-Drawing-App/
├── pencil_sketch.py
├── input.jpg    
├── output.jpg
└── README.md


## 🚀 How to Run

1. **Clone the repository**:
   git clone https://github.com/Pallavi-0622/Pencil-sketch-.git
   cd Pencil-sketch-

2. **Install required libraries**:
   pip install opencv-python

3. **Run the script**:
   python pencil_sketch.py

4. **View output**:
   - The resulting sketch will be saved as `output.jpg` in the same folder.

## 📌 Example Code Snippet

import cv2

image = cv2.imread("input.jpg")
gray_image = cv2.cvtColor(image, cv2.COLOR_BGR2GRAY)
inverted = 255 - gray_image
blur = cv2.GaussianBlur(inverted, (21, 21), 0)
sketch = cv2.divide(gray_image, 255 - blur, scale=256)

cv2.imwrite("output.jpg", sketch)

## 👩‍💻 Author

- Pallavi-0622 (https://github.com/Pallavi-0622)

## 📄 License

This project is licensed under the MIT License.

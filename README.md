# Optical-Character-Recognition-of-handwritten-digits
Optical Character Recognition (OCR) of Handwritten Digits

This project demonstrates how to build a simple Optical Character Recognition (OCR) system that can recognize handwritten digits using OpenCV and the k-Nearest Neighbors (kNN) algorithm.

It uses an image containing 5000 samples of handwritten digits (each of size 20×20 pixels), splits them into individual cells, trains a kNN model, and then evaluates its accuracy.

🧠 Features

Converts image to grayscale

Splits the source image into 5000 individual digit images

Prepares training and testing datasets

Trains a kNN classifier

Evaluates the model and displays its accuracy

📂 File Structure
.
├── digits1.png          # Image containing 5000 handwritten digits (50 rows × 100 columns)
├── ocr_digits.py        # Python script for OCR using OpenCV
└── README.md

⚙️ Requirements
Library	Version (recommended)
Python	3.x
OpenCV	>= 4.0
NumPy	>= 1.20

Install the required packages using:

pip install opencv-python numpy

▶️ How to Run

Place digits1.png in the same directory as the script.

Run the script:

python ocr_digits.py


You should see the model’s accuracy printed in the terminal.

💡 How It Works
Step	Description
1	Read digits1.png and convert it to grayscale
2	Split the image into 20×20 pixel cells (50 rows × 100 columns = 5000 samples)
3	Create training data from the first 50 columns and test data from the next 50 columns
4	Assign labels (0–9) to each digit sample
5	Train a kNN classifier using OpenCV
6	Use the classifier to predict test samples
7	Calculate and display the recognition accuracy
✅ Output

The script prints the accuracy of the kNN classifier.
For example:

Accuracy = 94.72%


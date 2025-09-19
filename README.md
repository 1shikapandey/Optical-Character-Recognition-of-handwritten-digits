<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8" />
</head>
<body>

<h1></h1>
<p>
This project demonstrates how to build a simple Optical Character Recognition (OCR) system that can recognize handwritten digits using <strong>OpenCV</strong> and the <strong>k-Nearest Neighbors (kNN)</strong> algorithm.
It uses an image containing 5000 samples of handwritten digits (each of size <strong>20×20 pixels</strong>), splits them into individual cells, trains a kNN model, and then evaluates its accuracy.
</p>

<h2>Features </h2>
<ul>
  <li>Converts image to grayscale</li>
  <li>Splits the source image into <strong>5000</strong> individual digit images</li>
  <li>Prepares <strong>training</strong> and <strong>testing</strong> datasets</li>
  <li>Trains a <strong>kNN classifier</strong></li>
  <li>Evaluates the model and displays its <strong>accuracy</strong></li>
</ul>

<h2>File Structure </h2>
<pre>
.
├── digits1.png          # Image containing 5000 handwritten digits (50 rows × 100 columns)
├── ocr_digits.py        # Python script for OCR using OpenCV
└── README.html
</pre>

<h2>Requirements</h2>
<table border="1" cellpadding="5" cellspacing="0">
  <tr>
    <th>Library</th>
    <th>Version (recommended)</th>
  </tr>
  <tr>
    <td>Python</td>
    <td>3.x</td>
  </tr>
  <tr>
    <td>OpenCV</td>
    <td>&gt;= 4.0</td>
  </tr>
  <tr>
    <td>NumPy</td>
    <td>&gt;= 1.20</td>
  </tr>
</table>

<p>Install the required packages using:</p>
<pre><code>pip install opencv-python numpy</code></pre>

<h2> How to Run</h2>
<ol>
  <li>Place <strong>digits1.png</strong> in the same directory as the script.</li>
  <li>Run the script:</li>
</ol>
<pre><code>python ocr_digits.py</code></pre>

<p>You should see the model’s <strong>accuracy</strong> printed in the terminal.</p>

<h2>How It Works</h2>
<table border="1" cellpadding="5" cellspacing="0">
  <tr>
    <th>Step</th>
    <th>Description</th>
  </tr>
  <tr>
    <td>1</td>
    <td>Read <code>digits1.png</code> and convert it to grayscale</td>
  </tr>
  <tr>
    <td>2</td>
    <td>Split the image into 20×20 pixel cells (50 rows × 100 columns = 5000 samples)</td>
  </tr>
  <tr>
    <td>3</td>
    <td>Create training data from the first 50 columns and test data from the next 50 columns</td>
  </tr>
  <tr>
    <td>4</td>
    <td>Assign labels (0–9) to each digit sample</td>
  </tr>
  <tr>
    <td>5</td>
    <td>Train a <strong>kNN classifier</strong> using OpenCV</td>
  </tr>
  <tr>
    <td>6</td>
    <td>Use the classifier to predict test samples</td>
  </tr>
  <tr>
    <td>7</td>
    <td>Calculate and display the recognition <strong>accuracy</strong></td>
  </tr>
</table>

<h2>Output</h2>
<pre><code>Accuracy = 94.72%</code></pre>

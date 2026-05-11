# Handdrawn AlphaNumeric Recognizer using CNN
#### Made by :- Srivatsa Gorti

---

## Overview

An end-to-end web application for recognizing hand-drawn alphanumeric characters — both digits (0–9) and letters (A–Z) — using a Convolutional Neural Network (CNN). Users draw directly on an interactive browser canvas, and the model identifies the character in real time with audio feedback, making it both a powerful ML demo and an engaging user experience.

This project demonstrates the full lifecycle of a deep learning product: from training a CNN on the EMNIST dataset, to deploying it as a live Streamlit web app that anyone can interact with instantly — no setup required.

---

## Demo

🔗 **Try it live:** https://srivat-1--handwritten-alphanumeric-recognizer-using-cnn-1hkq8f.streamlit.app/

<video src="https://user-images.githubusercontent.com/76219802/212941157-f99cda4f-4912-4e08-9ed9-a47a42d4363e.mp4" controls="controls" style="max-width: 1000px;" autoplay="autoplay">
</video>

<p align="center">
  <img src="https://user-images.githubusercontent.com/76219802/212941341-6e9784a0-7151-4edb-a09d-69b61a9491bb.png" />
</p>

---

## What It Does

- Accepts hand-drawn input from the user through a browser canvas
- Classifies both **letters (A–Z)** and **digits (0–9)** using a trained CNN
- Returns predictions in real time with **audio feedback via gTTS**
- Demonstrates a complete ML pipeline from model inference to deployed user-facing app

---

## Why This Project Matters

Handwriting recognition is a classic computer vision challenge because no two people write the same way — strokes vary in scale, thickness, alignment, and style. By supporting the full alphanumeric range (not just digits), this project tackles a broader and harder classification problem than standard MNIST-based demos.

What sets it apart is the product thinking behind it: the model isn't locked in a notebook. It's wrapped in a live, interactive interface where users test it in real time — making it immediately demonstrable and portfolio-worthy.

---

## How It Works

```
User draws on canvas
        ↓
Canvas image captured & preprocessed
        ↓
CNN model inference (EMNIST-trained)
        ↓
Predicted character returned
        ↓
Result displayed + audio feedback played
```

---

## Technology Stack

| Component | Technology |
|---|---|
| Programming Language | Python |
| Web App Framework | Streamlit |
| Drawing Interface | streamlit-drawable-canvas |
| Deep Learning | TensorFlow / Keras (CNN) |
| Dataset | EMNIST (Letters + Digits) |
| Data Handling | NumPy, Pandas |
| Image Processing | Pillow |
| Audio Feedback | gTTS (Google Text-to-Speech) |

---

## Model Architecture

The CNN is trained on the **EMNIST dataset**, which extends MNIST to include handwritten letters alongside digits. The architecture follows a standard convolutional pipeline:

- **Conv2D layers** — extract spatial features from the 28×28 pixel input
- **MaxPooling layers** — downsample and reduce spatial dimensions
- **Dropout layers** — prevent overfitting during training
- **Dense output layer** — Softmax activation over all alphanumeric classes

---

## Features

- ✅ Light/dark mode toggle
- ✅ Live canvas drawing with instant prediction
- ✅ Recognizes both **letters and numbers**
- ✅ Audio feedback on each prediction
- ✅ Cross-platform — runs entirely in the browser

---

## Installation & Setup

> **Note:** The trained model file is not included publicly. Contact the author with an appropriate reason to obtain it.

```bash
# Clone the repository
git clone https://github.com/srivatsacool/Handwritten_AlphaNumeric_Recognizer_using_CNN
cd Handwritten_AlphaNumeric_Recognizer_using_CNN

# Install dependencies
pip install -r requirements.txt

# Run the app
streamlit run app.py
```

### Dependencies

```
streamlit
streamlit_drawable_canvas
numpy
Pillow
tensorflow
pandas
gtts
gtts-token
```

---

## Author

**Srivatsa Gorti**  
[GitHub](https://github.com/srivatsacool)

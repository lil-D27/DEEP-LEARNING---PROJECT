# Handwritten Digit Recognition using CNN

A Deep Learning project that uses a **Convolutional Neural Network (CNN)** to identify handwritten digits (0–9) from images. The model is trained on the **MNIST** dataset using Keras/TensorFlow, and includes a demo where you can **draw or upload a digit** and see the prediction.

## Team Members

| Name | Roll Number |
|---|---|
| Darsha Padmanaban | 24BAD017 |
| Jessica Sam. B | <!-- add correct roll number --> |
| Dhanya G | 24BAD019 |
| Harshitha S K | 24BAD034 |

## Problem Statement

Develop a CNN that identifies handwritten digits from images and predicts the corresponding number from 0 to 9.

## Dataset

- **MNIST**, loaded directly with `keras.datasets.mnist`
- 60,000 training images and 10,000 test images
- 28×28 grayscale images, 10 classes (digits 0–9)
- Preprocessing: pixel values normalised to 0–1 and reshaped to `(28, 28, 1)`

## Model Architecture

| Layer | Details |
|---|---|
| Conv2D | 32 filters, 3×3, ReLU |
| MaxPooling2D | 2×2 |
| Conv2D | 64 filters, 3×3, ReLU |
| MaxPooling2D | 2×2 |
| Flatten + Dropout | Dropout 0.5 |
| Dense (Output) | 10 units, Softmax |

- **Optimizer:** Adam
- **Loss:** Sparse categorical cross-entropy
- **Epochs:** 10, **Batch size:** 128, **Validation split:** 10%

## Results

| Metric | Value |
|---|---|
| Test Accuracy | **XX.XX%** <!-- replace with your result --> |

### Screenshots

| Sample Data | Training Curves |
|---|---|
| ![Samples](screenshots/1_sample_digits.png) | ![Curves](screenshots/3_training_curves.png) |

| Confusion Matrix | Sample Predictions |
|---|---|
| ![Confusion](screenshots/5_confusion_matrix.png) | ![Predictions](screenshots/6_sample_predictions.png) |

### Demo

| Draw a digit | Upload a digit |
|---|---|
| ![Draw](screenshots/7_demo_draw.png) | ![Upload](screenshots/8_demo_upload.png) |

## How to Run

### Option 1: Google Colab (recommended)
1. Open `Handwritten_Digit_Recognition_CNN.ipynb` in [Google Colab](https://colab.research.google.com) (File → Upload notebook).
2. Click **Runtime → Run all**.
3. The last cell launches a Gradio demo with a public link. Draw or upload a digit to see the prediction.

### Option 2: Run locally
```bash
git clone https://github.com/<your-username>/<your-repo-name>.git
cd <your-repo-name>
pip install tensorflow numpy matplotlib scikit-learn gradio pillow
jupyter notebook Handwritten_Digit_Recognition_CNN.ipynb
```

## Project Structure

```
├── Handwritten_Digit_Recognition_CNN.ipynb   # Training, evaluation and demo
├── digit_cnn.keras                           # Trained model (optional, after training)
├── screenshots/                              # Result and demo screenshots
├── demo_video.mp4                            # Working demo video (optional)
└── README.md
```

## Tech Stack

Python, TensorFlow/Keras, NumPy, Matplotlib, scikit-learn, Gradio, Google Colab

## Applications

Bank cheque processing, postal code sorting, form and exam sheet digitisation, number plate and meter reading, and as a base for OCR systems.

## Future Scope

- Recognise handwritten letters and multi-digit numbers
- Use data augmentation for better robustness
- Deploy as a web or mobile app

## Acknowledgements

- [MNIST Database](http://yann.lecun.com/exdb/mnist/) by Yann LeCun et al.
- Developed as part of the Deep Learning course project.

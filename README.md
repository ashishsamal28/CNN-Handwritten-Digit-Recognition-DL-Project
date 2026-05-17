# CNN-Handwritten-Digit-Recognition-DL-Project


A Convolutional Neural Network (CNN) built with TensorFlow/Keras that recognizes handwritten digits (0–9) from images with high accuracy. Trained and evaluated on the classic **MNIST dataset**.

---

## Dataset — MNIST

| Property | Details |
|---|---|
| Total Images | 70,000 |
| Training Set | 60,000 images |
| Test Set | 10,000 images |
| Image Size | 28×28 pixels, grayscale |
| Classes | 10 (digits 0 to 9) |
| Source | Built into Keras — no download needed! |

---

## Model Architecture

```
Input (28×28×1)
      ↓
Conv2D (32 filters, 3×3, ReLU)
      ↓
MaxPooling2D (2×2)
      ↓
Conv2D (64 filters, 3×3, ReLU)
      ↓
MaxPooling2D (2×2)
      ↓
Flatten
      ↓
Dense (128, ReLU)
      ↓
Dropout (0.3)
      ↓
Dense (10, Softmax)  ← Output: digit 0–9
```

| Parameter | Value |
|---|---|
| Optimizer | Adam |
| Loss Function | Categorical Crossentropy |
| Epochs | 10 |
| Batch Size | 128 |
| Validation Split | 10% |

---

## Pipeline

```
Load MNIST Dataset (via Keras)
      ↓
Visualize Sample Images
      ↓
Preprocessing (Reshape + Normalize + One-Hot Encode)
      ↓
Build CNN Model
      ↓
Train (10 epochs)
      ↓
Plot Accuracy & Loss Curves
      ↓
Evaluate on Test Set
      ↓
Visualize Predictions & Mistakes
      ↓
Save Model → digit_recognizer_cnn.h5
```

---

## Results

- Evaluated on 10,000 test images
- Training and validation accuracy plotted over epochs
- Wrong predictions visualized to understand model mistakes

---

## Project Structure

```
Handwritten-Digit-Recognition-CNN/
│
├── Handwritten_Digit_Recognition_CNN.ipynb   # Main notebook
├── digit_recognizer_cnn.h5                   # Saved model (after training)
└── README.md
```

---

## Requirements

```bash
pip install tensorflow numpy matplotlib
```

---

## How to Run

1. **Clone the repository**
   ```bash
   git clone https://github.com/ashishsamal28/Handwritten-Digit-Recognition-CNN.git
   cd Handwritten-Digit-Recognition-CNN
   ```

2. **Open in Google Colab or Jupyter**
   ```bash
   jupyter notebook Handwritten_Digit_Recognition_CNN.ipynb
   ```

3. **Run all cells** — MNIST loads automatically, no dataset download needed

4. The trained model will be saved as `digit_recognizer_cnn.h5`

---

## Tech Stack

- **Language:** Python 3
- **Framework:** TensorFlow / Keras
- **Libraries:** NumPy, Matplotlib
- **Environment:** Google Colab / Jupyter Notebook

---

## Author

**Ashish Samal**  
[GitHub](https://github.com/ashishsamal28)


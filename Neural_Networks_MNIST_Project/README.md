# Neural Networks for MNIST Classification

## Overview
This project compares two neural network architectures for classifying handwritten digits (0–9) from the MNIST dataset: a regularized feedforward neural network (FNN) and a convolutional neural network (CNN). Each model was trained and evaluated 5 times to check that the results are stable, not a lucky single run.

## Data
- **Dataset:** MNIST handwritten digits (28×28 grayscale images, 10 classes), loaded from the original IDX files
- **Split:** the 60,000 training images were split 80/20 into training and validation sets; the 10,000-image MNIST test set was held out for final evaluation
- **Preprocessing:** pixel values scaled to [0, 1], then standardized with `StandardScaler` fit on the training set only

## Models
| | Feedforward NN | Convolutional NN |
|---|---|---|
| Architecture | Flatten → Dense(128) → Dense(64) → Dense(10) | Conv(32) → Pool → Conv(64) → Pool → Dense(128) → Dense(64) → Dense(10) |
| Regularization | L2 (0.01) + Dropout(0.5) | Dropout(0.5) |
| Training | Adam (lr 0.001), 10 epochs, batch size 64 | Adam (lr 0.001), 10 epochs, batch size 64 |

## Results
Average test accuracy over 5 independent runs:

| Model | Run 1 | Run 2 | Run 3 | Run 4 | Run 5 | **Average** |
|---|---|---|---|---|---|---|
| Feedforward NN | 94.34% | 94.28% | 94.14% | 94.09% | 94.48% | **94.27%** |
| CNN | 99.01% | 99.08% | 99.04% | 98.98% | 99.02% | **99.03%** |

## Key Takeaways
- The CNN cut the error rate from about 5.7% to about 1.0%, because convolutional layers learn local patterns (strokes, edges) that a flattened feedforward network cannot see.
- Results were consistent across runs (each model's accuracy stayed within about 0.4 percentage points), so the gap between the two models is real, not noise.

## Files
- `Neural_Networks_MNIST_Project.ipynb`: data loading, both model definitions, 5-run evaluation, and summary report

## Tools
Python, TensorFlow, Keras, NumPy, scikit-learn

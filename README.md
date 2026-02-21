<img width="1000" height="279" alt="header" src="https://github.com/user-attachments/assets/699f6feb-ccf4-4fda-8893-f9969711ae88" />



# MNIST-Digits-MLP-CNN

![Python](https://img.shields.io/badge/python-3.10-lightblue)
![PyTorch](https://img.shields.io/badge/PyTorch-2.x-lightblue)
![Kaggle](https://img.shields.io/badge/dataset-Digit%20Recognizer-lightblue)
![License](https://img.shields.io/badge/license-MIT-lightblue)

Simple PyTorch neural networks (MLP and CNN) trained on the Kaggle digit-recognizer dataset (MNIST in CSV format). The goal is practice with neural nets, not leaderboard sniping.



## Models

- **Linear baseline**: single `Linear(784 → 10)` classifier.
- **MLP**: `784 → 128 → 10` with ReLU.
- **MLP + Dropout + Adam**: `784 → 128 → Dropout(0.5) → 10`.
- **CNN**:
  - Conv(1 → 32, 3×3) → Conv(32 → 64, 3×3) → MaxPool(2×2)
  - Flatten → Linear(64×14×14 → 128) → Linear(128 → 10)

### Approximate performance

| Model                 | Notes                  | Val acc (≈) |
|-----------------------|------------------------|------------|
| Linear                | SGD, lr=0.1           | 92.1%      |
| MLP                   | SGD, lr=0.1           | 97.2%      |
| MLP + Dropout + Adam  | Adam, lr=1e-3         | 97.5%      |
| CNN                   | Adam, lr=1e-3, 10 ep  | 98.6%      |

## Data

- Competition: [Kaggle Digit Recognizer](https://www.kaggle.com/c/digit-recognizer).
- `data/train.csv` and `data/test.csv` should be downloaded from Kaggle and placed under `data/`.


## License

MIT 2026©


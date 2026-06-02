# Deep Learning with PyTorch

A comprehensive collection of Jupyter notebooks demonstrating PyTorch fundamentals and deep learning models, including tensor operations, neural networks, and convolutional neural networks.

## 📁 Project Structure

```
DL-PyTorch/
├── Cnn.ipynb                 # Convolutional Neural Network (MNIST)
├── Simple-NN.ipynb           # Simple Neural Network (Iris)
├── Main.ipynb                # PyTorch Tensor Basics
├── Math-Operation.ipynb      # Tensor Mathematical Operations
├── iris_model.pt             # Trained Iris model (saved state)
└── README.md
```

## 📚 Notebooks Overview

### 1. **Math-Operation.ipynb**
**Basics of PyTorch Tensor Operations**

Learn fundamental tensor mathematical operations:
- Element-wise addition, subtraction, division, modulo
- Using PyTorch functional methods (`torch.add()`, `torch.sub()`, etc.)
- Tensor indexing and slicing

**Topics Covered:**
- Tensor creation
- Arithmetic operations
- Remainder operations

---

### 2. **Main.ipynb**
**PyTorch Tensor Manipulation**

Explore tensor reshaping and manipulation:
- View operations for reshaping tensors
- Reshape vs. view
- Tensor element access and modification
- Indexing and slicing operations

**Topics Covered:**
- Tensor viewing and reshaping
- Element-wise access
- Column and row slicing

---

### 3. **Simple-NN.ipynb**
**Neural Network for Iris Flower Classification**

Build a simple feed-forward neural network to classify iris flowers:
- Model architecture with multiple hidden layers
- Data loading from URL
- Train-test split
- Model training and evaluation

**Model Architecture:**
- Input Layer: 4 features
- Hidden Layer 1: 8 neurons + ReLU
- Hidden Layer 2: 9 neurons + ReLU
- Output Layer: 3 classes (Setosa, Versicolor, Virginica)

**Dataset:** 
- Iris dataset (150 samples)
- 4 input features (sepal length, sepal width, petal length, petal width)
- 3 output classes

**Key Results:**
- Model saved as `iris_model.pt`

---

### 4. **Cnn.ipynb**
**Convolutional Neural Network for MNIST Digit Recognition**

A complete CNN implementation for handwritten digit classification:
- Convolutional layers with max pooling
- Fully connected layers
- Model training and evaluation
- Accuracy tracking and visualization
- Single sample prediction

**Model Architecture:**
- Conv2d Layer 1: 1→6 channels, 3×3 kernel
- Max Pool: 2×2
- Conv2d Layer 2: 6→16 channels, 3×3 kernel
- Max Pool: 2×2
- Fully Connected: 16×5×5 → 120 → 84 → 10 (digits)
- Loss Function: CrossEntropyLoss
- Optimizer: Adam (lr=0.001)

**Dataset:**
- MNIST (60,000 training, 10,000 test samples)
- 28×28 grayscale images
- 10 output classes (digits 0-9)

**Features:**
- Training/validation loss curves
- Training/validation accuracy curves
- Real-time batch loss tracking
- Individual sample prediction and visualization

**Results:**
- Training for 5 epochs
- Loss and accuracy visualization
- Sample digit prediction with visual confirmation

---

## 🚀 Getting Started

### Prerequisites

```bash
pip install torch torchvision pytorch-cuda=11.8
pip install pandas scikit-learn matplotlib numpy
```

### Installation

1. Clone the repository:
```bash
git clone https://github.com/yourusername/DL-PyTorch.git
cd DL-PyTorch
```

2. Install dependencies:
```bash
pip install -r requirements.txt
```

3. Launch Jupyter:
```bash
jupyter notebook
```

## 📊 How to Run

### Run Individual Notebooks

Open Jupyter and navigate to each notebook:

1. **Start with Math-Operation.ipynb** - Learn tensor basics
2. **Then Main.ipynb** - Understand tensor manipulation
3. **Then Simple-NN.ipynb** - Build your first neural network
4. **Finally Cnn.ipynb** - Explore convolutional networks

### Run All Cells

```python
# In Jupyter, press: Ctrl+A then Ctrl+Enter
# Or use: Cell > Run All
```

## 📈 Model Performance

### Iris Classification (Simple-NN)
- Classification on 3 iris flower species
- Trained on 80% of 150 samples
- Model saved for later use

### MNIST Digit Recognition (CNN)
- **Training Accuracy:** ~96% (after 5 epochs)
- **Validation Accuracy:** ~95%
- Successfully classifies handwritten digits
- Real-time prediction on individual samples

## 📝 Key Concepts Covered

### Fundamentals
- Tensor creation and manipulation
- Mathematical operations on tensors
- Tensor reshaping and indexing

### Neural Networks
- Model architecture design
- Loss functions and optimizers
- Training loops and backpropagation
- Accuracy metrics

### Convolutional Networks
- Conv2d layers
- Max pooling
- Feature extraction
- Image classification workflow

### Visualization
- Training/validation curves
- Loss tracking
- Image visualization
- Prediction confidence

## 🔧 Troubleshooting

### Common Issues

1. **MNIST Data Download**
   - First run may take time downloading data
   - Data stored in `/cnn_data` directory

2. **GPU Support**
   - Models run on CPU by default
   - To enable GPU: Add `.cuda()` to model

3. **Dependencies Missing**
   - Ensure all packages installed: `pip install -r requirements.txt`

## 📚 Learning Resources

- [PyTorch Official Documentation](https://pytorch.org/docs/stable/index.html)
- [PyTorch Tutorials](https://pytorch.org/tutorials/)
- [Deep Learning Specialization](https://www.deeplearning.ai/)

## 💡 Extensions & Improvements

- Implement data augmentation for MNIST
- Add dropout layers for regularization
- Use pre-trained models with transfer learning
- Implement batch normalization
- Add model checkpointing and early stopping

## 📄 License

This project is open source and available under the MIT License.

## 👤 Author

Created for educational purposes in deep learning with PyTorch.

---

## 🎯 Quick Start Example

```python
import torch
import torch.nn as nn

# Simple tensor operation
t1 = torch.tensor([1, 2, 3, 4])
t2 = torch.tensor([5, 6, 7, 8])
result = t1 + t2  # Element-wise addition

# Create and train a model
model = nn.Linear(4, 3)
optimizer = torch.optim.Adam(model.parameters())
criterion = nn.CrossEntropyLoss()

# Training step
output = model(input_data)
loss = criterion(output, target)
loss.backward()
optimizer.step()
```

---

**Happy Learning! 🚀**

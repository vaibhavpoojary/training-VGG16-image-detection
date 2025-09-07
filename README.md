
# Image detection with VGG16 (Transfer Learning)

This project trains a **VGG16‑based image classifier** to detect images using **transfer learning**. The workflow is implemented in a single Jupyter notebook:

This repo contains the image detector models under different branches 

> **Why VGG16?** It’s a proven convolutional backbone for image tasks, simple to fine‑tune, and widely available via Keras/TensorFlow.

---

## ✨ Key Features

- Transfer learning with **VGG16 (ImageNet weights)**
- Data loading & augmentation via Keras `ImageDataGenerator`
- Freezing base layers + custom classification head
- Training curves, metrics, and confusion‑matrix style evaluation
- Optional single‑image prediction utilities

---

## ⚙️ Environment & Prerequisites

### Python / OS
- **Recommended (Windows):** Python **3.11** (TensorFlow provides official Windows wheels up to 3.11 for TF 2.20). If you need Python 3.12/3.13 on Windows, use **WSL2 (Ubuntu)** or Linux for TensorFlow wheels. [1](https://www.tensorflow.org/install/pip)
- **Linux/macOS:** Python 3.9–3.13 are available for TF 2.20 on Linux; macOS supports CPU wheels. See the TF install guide for details. [1](https://www.tensorflow.org/install/pip)
### TensorFlow I/O note (GCS filesystem)
Starting with **TensorFlow 2.20**, the `tensorflow-io-gcs-filesystem` package is **optional** and not installed by default. Install it only if you explicitly need to read/write to **Google Cloud Storage** (GCS). [2](https://github.com/tensorflow/tensorflow/releases)

> On Windows, new wheels for `tensorflow-io-gcs-filesystem` have had **limited/unstable availability**, which can trigger the “No matching distribution found” pip error. If you don’t use GCS, omit the package entirely. [3](https://github.com/tensorflow/io/issues/2087)

---

## 🔧 Quick Start

> Below are **two** safe setup paths. If you’re on Windows and don’t need GPU, **Option A** is the quickest.

### Option A — Native Windows (CPU) with Python 3.11

```powershell
# 1) Create & activate a clean venv (Python 3.11)
py -3.11 -m venv .venv
.\.venv\Scripts\Activate.ps1

# 2) Upgrade pip
python -m pip install --upgrade pip

# 3) Install core deps
pip install tensorflow==2.20.0  # CPU build on Windows (official wheels for py3.11)
pip install numpy matplotlib pillow scikit-learn
# If your notebook imports extras (e.g., opencv-python, seaborn), install them too:
# pip install opencv-python seaborn

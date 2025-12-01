# Fashion-MNIST CNN Image Classification — End-to-End Deep Learning (Docker + Streamlit)

## Project Description
This is an end-to-end deep learning image classification project using a Convolutional Neural Network trained on the Fashion-MNIST dataset. The pipeline covers model training, evaluation, inference on custom images, containerized deployment using Docker, and a real-time UI built with Streamlit.

## Features
- 10-class apparel classification
- CNN model trained using TensorFlow/Keras
- Custom image inference support
- Docker container deployment
- Streamlit interactive web UI
- Model saved in `.h5` format
- Reproducible dependency management

## Tech Stack
- **Deep Learning Framework:** :contentReference[oaicite:0]{index=0} + :contentReference[oaicite:1]{index=1}
- **UI Framework:** :contentReference[oaicite:2]{index=2}
- **Containerization:** :contentReference[oaicite:3]{index=3}
- **IDE:** :contentReference[oaicite:4]{index=4}
- **Language:** :contentReference[oaicite:5]{index=5}
- **Dataset:** Fashion-MNIST
- **Model Format:** `.h5`

## Directory Structure
```bash
├── .vscode/ # Editor settings
├── app/ # Streamlit UI package
├── trained_model/ # Saved CNN model (.h5)
├── test_images/ # Images for inference tests
├── config.toml # Optional config
├── credentials.toml # Optional credentials config
├── Dockerfile # Docker build file
├── main.py # App entry point for container
├── requirements.txt # Dependency file
├── Fashion-MNIST-Image-Classification-CNN.ipynb # Model training notebook
├── LICENSE # License file
├── .gitignore # Git ignore rules
```

## Model Architecture (CNN)
Typical layers implemented in the notebook:
1. Conv2D → Activation (ReLU)
2. MaxPooling2D
3. Conv2D → Activation (ReLU)
4. MaxPooling2D
5. Flatten
6. Dense → ReLU
7. Dense → Softmax (Output Layer)

## Installation & Setup

### 1. Clone the Repository

git clone <https://github.com/sharma-piyush1/End-to-END-Fashion-MNIST-Classification-with-Docker>
cd <repo-folder>


### 2. Create a Virtual Environment
```bash
python -m venv venv
```


### 3. Activate Environment

**Windows**
```bash
venv\Scripts\activate
```

### 4. Install Dependencies
```bash
pip install -r requirements.txt
```


## Run the App Locally
```bash
streamlit run app/main.py
```


## Docker Build & Deployment

### 1. Build Docker Image
```bash
docker build -t fashion-mnist-cnn .
```


### 2. Run Docker Container
```bash
docker run -p 8501:8501 fashion-mnist-cnn
```


### 3. Access UI in Browser
```bash
http://localhost:8501
```


## Inference on Custom Images
The UI accepts images from `test_images/`. Preprocessing steps include:
- Convert to grayscale
- Resize to 28×28
- Normalize pixel values (0-1)
- Model prediction using Softmax output mapping

## Apparel Classes
| Label | Category |
|-------|----------|
| 0 | T-shirt/Top |
| 1 | Trouser |
| 2 | Pullover |
| 3 | Dress |
| 4 | Coat |
| 5 | Sandal |
| 6 | Shirt |
| 7 | Sneaker |
| 8 | Bag |
| 9 | Ankle Boot |

## Future Improvements
- Model quantization (`.tflite`)
- GPU support using Docker NVIDIA toolkit
- CI/CD integration using GitHub Actions
- Cloud deployment on AWS/GCP/Azure








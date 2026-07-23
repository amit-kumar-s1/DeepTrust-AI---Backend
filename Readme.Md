# DeepTrust AI - Backend

## Overview

DeepTrust AI Backend is a FastAPI-based application that powers the AI services for the DeepTrust AI platform. It provides REST APIs for detecting manipulated images using deep learning models. The backend is responsible for processing uploaded images, running inference through trained models, and returning prediction results with confidence scores.

---

## Features

* DeepFake image detection
* FastAPI REST API
* Image upload and validation
* AI model inference
* Confidence score generation
* Modular project structure
* Docker support
* Automatic API documentation
* Frontend integration support

---

## Technology Stack

* Python
* FastAPI
* PyTorch
* TIMM
* Pillow
* NumPy
* Uvicorn
* Pydantic

---

## Project Structure

```
DeepTrust-AI---Backend/
│
├── app/
│   ├── api/
│   ├── core/
│   ├── schemas/
│   ├── services/
│   └── utils/
│
├── ml/
│   └── image_detection/
│       ├── inference/
│       ├── models/
│       ├── config.py
│       └── service.py
│
├── main.py
├── requirements.txt
├── Dockerfile
└── .dockerignore
```

---

## Installation

Clone the repository.

```bash
git clone https://github.com/amit-kumar-s1/DeepTrust-AI---Backend.git

cd DeepTrust-AI---Backend
```

Create a virtual environment.

### Windows

```bash
python -m venv venv
venv\Scripts\activate
```

### Linux/macOS

```bash
python3 -m venv venv
source venv/bin/activate
```

Install the required dependencies.

```bash
pip install -r requirements.txt
```

---

## Running the Application

Start the development server.

```bash
uvicorn main:app --reload
```

The application will be available at:

```
http://127.0.0.1:8000
```

Interactive API documentation:

```
http://127.0.0.1:8000/docs
```

---

## API Endpoint

### Detect Image

**Method**

```
POST
```

**Endpoint**

```
/api/v1/detect/image
```

**Request**

Content-Type:

```
multipart/form-data
```

Parameter:

| Name | Type  | Description                |
| ---- | ----- | -------------------------- |
| file | Image | Input image for prediction |

---

## Response

Example response:

```json
{
    "prediction": "Fake",
    "confidence": 97.82
}
```

---

## Detection Workflow

1. Receive image from the client.
2. Validate the uploaded file.
3. Preprocess the image.
4. Load trained AI models.
5. Perform inference.
6. Generate prediction and confidence score.
7. Return the result as a JSON response.

---

## Machine Learning Components

The backend includes an inference pipeline for image deepfake detection.

Components include:

* Image preprocessing
* Model loading
* Prediction pipeline
* Confidence calculation
* Result generation

---

## Docker

Build the Docker image.

```bash
docker build -t deeptrust-backend .
```

Run the container.

```bash
docker run -p 8000:8000 deeptrust-backend
```

---

## Development

Install dependencies.

```bash
pip install -r requirements.txt
```

Run the server.

```bash
uvicorn main:app --reload
```

---

## Future Improvements

* Video deepfake detection
* Document verification
* Text detection
* Batch prediction
* Authentication
* Logging and monitoring
* Model versioning

---

## License

This project is intended for educational and research purposes. Update the license according to your project requirements.

---

## Author

Kundan Kumar Thakur  & Amit Kumar Saw

GitHub: https://github.com/amit-kumar-s1

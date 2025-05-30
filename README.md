# Personality Trait Predictor

A Streamlit web application that uses a convolutional neural network to predict Big Five personality traits from facial images.

## Features

- Face detection and cropping using Haar Cascade
- Personality trait prediction using a pre-trained CNN model
- Interactive visualization of prediction results using Plotly gauges
- User-friendly Streamlit interface

## Usage

### Using Docker Hub

You can run this Docker image using:

```bash
docker pull notyouranas/personality-trait-predictor:latest
docker run -p 8502:8501 notyouranas/personality-trait-predictor:latest
```

Then open your browser and navigate to http://localhost:8502

### Using Docker Compose

Alternatively, you can use Docker Compose:

```bash
docker compose up
```

This will also map port 8502 on your host to port 8501 in the container, as specified in the compose.yaml file.

### Port Configuration

- The application runs on port 8501 inside the container (as defined in the Dockerfile)
- The port is mapped to 8502 on the host in both examples above
- This means you'll always access the application at http://localhost:8502

## Model Information

The application uses a pre-trained model (Model_2.0.h5) to predict the Big Five personality traits:
- Extraversion
- Agreeableness
- Conscientiousness
- Neuroticism
- Openness

## Technologies Used

- Streamlit for the web interface
- TensorFlow/Keras for the CNN model
- OpenCV for face detection
- Plotly for interactive visualizations
- Docker for containerization

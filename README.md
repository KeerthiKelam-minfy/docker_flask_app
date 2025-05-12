# My Flask App - Docker Image

A minimal Flask web app wrapped in a Docker container. When you run this image, it starts a simple web server that responds with:
### "Hello from my Docker image!"

## How to Use:

### Pull and Run from Docker Hub:
  docker run -p 5000:5000 keerthikelam/my-flask-app

### Then open your browser and go to:
  http://localhost:5000

  You’ll see:
### Hello from my Docker image!



**Dockerfile (Reference)**

FROM python:3.9-slim  
WORKDIR /app    
COPY app.py .
RUN pip install flask
CMD ["python", "app.py"]

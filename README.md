# My Flask App Docker Image

This is a simple Flask application that I’ve packaged into a Docker image. It’s a basic app that responds with a message when you visit it through your web browser.

## Prerequisites

Before you get started, you'll need:

- Docker installed on your system.
- A Docker Hub account if you plan to pull the image from Docker Hub.

## How to Build the Docker Image Locally

If you want to build the image yourself, follow these steps:

1. First, clone or download this repository to your local machine.
2. Open a terminal (or the terminal in VS Code), and navigate to the folder where the `Dockerfile` and `app.py` are located.
3. Run this command to build the Docker image:

    ```bash
    docker build -t keerthikelam/my-flask-app .
    ```

This command will pull the necessary Python image, install dependencies (like Flask), and build the image. Once the build is complete, you’ll have your Docker image ready to run!

## How the Image Was Created

I created this image by writing a `Dockerfile` that contains the instructions for Docker to build the app’s environment. Here’s a quick rundown of what’s inside the `Dockerfile`:

- **Base Image**: It uses the official `python:3.9-slim` image as the starting point.
- **Working Directory**: The app is placed in the `/app` directory inside the container.
- **Flask Installation**: It installs Flask using pip.
- **Port Exposure**: The app runs on port `5000`, which is exposed so you can access it.
- **Command**: The app is launched by running `python app.py`.

Here’s what the `Dockerfile` looks like:

```Dockerfile
FROM python:3.9-slim
WORKDIR /app
COPY app.py .
RUN pip install flask
EXPOSE 5000
CMD ["python", "app.py"]

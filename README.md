# my-flask-app

A simple Flask-based "Hello from my docker Image!" web application running in a Docker container.

This app demonstrates basic Docker usage with a Flask server listening on port `5000`.

---

## To Pull the Image:

```bash
docker pull keerthikelam/my-flask-app:latest
```

## To run this image:
```bash
docker run -p 5000:5000 keerthikelam/my-flask-app

```

## Accessing the App:
Once the container is running, open your browser and go to:
```bash
http://localhost:5000
```
You should see the message: **"Hello from my Docker image!"**

<br/>
<br/>

Dockerhub link: https://hub.docker.com/r/keerthikelam/my-flask-app 

Github link: https://github.com/KeerthiKelam-minfy/docker_flask_app⁠

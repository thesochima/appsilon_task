# appsilon_task

To run this simple flask Hello World app on your PC.

Follow the steps below:

1 - clone app Repo

2 - Navigate to project directory

!! Please ensure you have python and pip installed on your system.

3 - Then type 'pip install -r requirements.txt' this will install all the needed dependencies for the application locally

4 - Then type 'python app.py' this will start the application locally using your localhost

The CI uses github actions to build the Dockerfile 
The steps in the job perform the following actions:

The CI step uses the actions/checkout@v2 action to clone the source code repository into the workflow workspace.

Set up Docker Buildx: This step uses the docker/setup-buildx-action@v1 action to set up Docker Buildx, which is a Docker CLI plugin for building multi-platform images.

Next github action uses the docker/login-action@v1 action to authenticate with Docker Hub using the provided Docker Hub username and password. The secrets are retrieved from the GitHub repository's secrets.

Build and Push Docker image: This step uses the docker/build-push-action@v2 action to build a Docker image and push it to Docker Hub. it also sets the image tags as thesochima/appsilon:latest.

Overall, this job configuration sets up a CI/CD pipeline that automatically builds a Docker image from the source code and pushes it to Docker Hub whenever changes are pushed to the repository. 
The image is tagged as thesochima/appsilon:latest.

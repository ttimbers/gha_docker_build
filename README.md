# GitHub Actions Docker build

This repository is an example how to use GitHub Actions to build a Docker image and publish it on DockerHub when a commit that changes the `Dockerfile` is pushed to the `main` branch. It also versions the Docker image (using tags) and the GitHub reposiroty (using releases) with the same version number (so you can tell which version of the Dockerfile created which version of the Docker image).

This requires:
- A DockerHub account, and the DockerHub username and password stored as GitHub secrets in the repository with the Dockerfile (named `DOCKER_PASSWORD` and `DOCKER_USERNAME`). 
- A DockerHub repository to be created, and the name of it to be added to [line 37](https://github.com/ttimbers/gha_docker_build/blob/e114ee95b5339d44f2e651535c21435f22c561aa/.github/workflows/publish_docker_images.yml#L37)of the [`.github/workflows/publish_docker_images.yml`](https://github.com/ttimbers/gha_docker_build/blob/main/.github/workflows/publish_docker_images.yml) file

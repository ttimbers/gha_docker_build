# GitHub Actions Docker build

This repository is an example how to use GitHub Actions to build a Docker image and publish it on [DockerHub](https://hub.docker.com/) when a commit that changes the `Dockerfile` is pushed to the `main` branch. It also versions the Docker image (using tags) and the GitHub reposiroty (using releases) with the same version number (so you can tell which version of the Dockerfile created which version of the Docker image), and parses the commit message to determine the semantic version bump.

This requires:
- A [DockerHub](https://hub.docker.com/) account, and the DockerHub username and password stored as GitHub secrets in the repository with the Dockerfile (named `DOCKER_PASSWORD` and `DOCKER_USERNAME`). 
- A DockerHub repository to be created, and the name of it to be added to [line 38](https://github.com/ttimbers/gha_docker_build/blob/fae92e51ae6520d22d6632c5bafd30bd3fdbdc00/.github/workflows/publish_docker_images.yml#L38)of the [`.github/workflows/publish_docker_images.yml`](https://github.com/ttimbers/gha_docker_build/blob/main/.github/workflows/publish_docker_images.yml) file

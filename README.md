# Docker Image for Google Cloud SDK and Terraform
This is a Docker image that extends the official Google Cloud SDK image with the addition of Terraform.

[https://hub.docker.com/r/cedricguadalupe/terraform-gcloud](https://hub.docker.com/r/cedricguadalupe/terraform-gcloud)

## Versions
This image is built using the following versions:
 - Google Cloud SDK: 445.0.0
 - Terraform: 1.5.6

Latest version : [![latest](https://img.shields.io/badge/terraform--gcloud-1.5.6--445.0.0-green.svg)](https://hub.docker.com/r/cedricguadalupe/terraform-gcloud)

## Usage
To use this image, you will need Docker installed on your system.

## Pulling the Image
You can pull the image from Docker Hub using the following command:

```sh
docker pull cedricguadalupe/terraform-gcloud
```

## Running the Image
To run the image, you will need to provide your Google Cloud credentials and mount a directory for Terraform files. You can do this using the following command:

```sh
docker run -it -v /path/to/terraform/files:/terraform -v /path/to/credentials:/root/.config/gcloud -w /terraform cedricguadalupe/terraform-gcloud
```
This will start a container with the current working directory set to the mounted Terraform directory.

## Building the Image
If you prefer to build the image locally, you can do so using the following command:

```sh
docker build -t cedricguadalupe/terraform-gcloud .
```

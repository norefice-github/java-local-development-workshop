# Step 1: Getting Started
Before getting started, let's make sure you have everything you need for this workshop.

## Prerequisites

### Install Java 17 or newer
You'll need Java 17 or newer for this workshop.
Testcontainers libraries are compatible with Java 8+, but this workshop uses a Spring Boot 3.x application which requires Java 17 or newer.

I would recommend using [SDKMAN](https://sdkman.io/) to install Java on your machine.

## Install Docker

Make sure you have a Docker environment available on your machine.

* It can be [Testcontainers Cloud](https://testcontainers.com/cloud) recommended to avoid straining the conference network by pulling heavy Docker images.

* It can be a local Docker, which you can check by running:
```shell
$ docker version

Client:
 Version:           24.0.6-rd
 API version:       1.43
 Go version:        go1.20.7
 Git commit:        da4c87c
 Built:             Wed Sep  6 16:40:13 2023
 OS/Arch:           darwin/arm64
 Context:           desktop-linux
Server: Docker Desktop 4.24.2 (124339)
 Engine:
  Version:          24.0.6
  API version:      1.43 (minimum version 1.12)
  Go version:       go1.20.7
  Git commit:       1a79695
  Built:            Mon Sep  4 12:31:36 2023
  OS/Arch:          linux/arm64
  Experimental:     false
  ...
```

## Install Testcontainers Desktop
[Testcontainers Desktop](https://testcontainers.com/desktop/) is a companion app for the open source Testcontainers libraries 
that makes local development and testing with real dependencies simple.

Download the latest version of Testcontainers Desktop app from [https://testcontainers.com/desktop/](https://testcontainers.com/desktop/) 
and install it on your machine. 

Once you start the Testcontainers Desktop application, it will automatically detect the container runtimes 
installed on your system (Docker Desktop, OrbStack, etc) 
and allows you to choose which container runtime you want to use by Testcontainers.

## Download the project

Clone the [java-local-development-workshop](https://github.com/testcontainers/java-local-development-workshop) repository from GitHub to your computer:  

```shell
git clone https://github.com/testcontainers/java-local-development-workshop.git
```

## Compile the project to download the dependencies

With Maven:
```shell
./mvnw compile
```

## \(optionally\) Pull the required images before doing the workshop

This might be helpful if the internet connection at the workshop venue is somewhat slow.

```shell
docker pull postgres:16-alpine
docker pull localstack/localstack:2.3
docker pull wiremock/wiremock:3.2.0-alpine
docker pull confluentinc/cp-kafka:7.5.0
docker pull confluentinc/cp-schema-registry:7.5.0
docker pull confluentinc/cp-enterprise-control-center:7.5.0
```

### 
[Next](step-2-exploring-the-app.md)
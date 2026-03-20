# cicd-sample-app

> A Spring Boot sample application demonstrating multiple CI/CD pipeline integrations: Jenkins, CircleCI, GitHub Actions, and AWS CodeDeploy.

[![Java](https://img.shields.io/badge/Java-8+-orange?logo=java&logoColor=white)](https://java.com)
[![Spring Boot](https://img.shields.io/badge/Spring_Boot-2.x-6DB33F?logo=spring&logoColor=white)](https://spring.io/projects/spring-boot)
[![Docker](https://img.shields.io/badge/Docker-ready-2496ED?logo=docker&logoColor=white)](https://docker.com)
[![CI/CD](https://img.shields.io/badge/CI%2FCD-Jenkins%20%7C%20CircleCI%20%7C%20GHA-brightgreen)](https://github.com/misoboy/cicd-sample-app)

## Overview

This project serves as a **reference implementation** for setting up CI/CD pipelines with a Spring Boot application. It includes configurations for multiple CI/CD platforms.

## Supported CI/CD Platforms

| Platform | Config File | Description |
|----------|-------------|-------------|
| Jenkins | `Jenkinsfile` | Pipeline-as-code with Docker build & deploy |
| CircleCI | `.circleci/config.yml` | CircleCI workflow with Maven and Docker |
| GitHub Actions | `.github/workflows/` | GitHub-native CI/CD |
| AWS CodeDeploy | `appspec.yml` + `scripts/` | EC2 deployment lifecycle |

## Getting Started

```bash
git clone https://github.com/misoboy/cicd-sample-app.git
cd cicd-sample-app

# Build
./mvnw clean package

# Run
java -jar target/cicd-sample-app-*.jar
```

### Docker

```bash
docker build -t cicd-sample-app .
docker run -p 8080:8080 cicd-sample-app
```

## License

MIT


# Flask Static App with Kubernetes and Docker

This project demonstrates a simple Flask application containerized with Docker and deployed to a Kubernetes cluster using Minikube. The app serves a static webpage.

## Features
- Flask web application serving a static HTML page
- Dockerized for easy deployment
- Kubernetes configuration files for deployment to a Minikube cluster

## Technologies Used
- **Flask**: A micro web framework for Python
- **Docker**: For containerizing the application
- **Kubernetes**: For deploying the app in a cluster
- **Minikube**: Local Kubernetes cluster for development

## Getting Started

### Prerequisites

- Install [Docker](https://www.docker.com/get-started)
- Install [Minikube](https://minikube.sigs.k8s.io/docs/)
- Install [Kubectl](https://kubernetes.io/docs/tasks/tools/install-kubectl/)

### Steps

1. **Clone the repository**:
    ```bash
    git clone https://github.com/YOUR_USERNAME/flask-k8s-app.git
    cd flask-k8s-app
    ```

2. **Build the Docker image**:
    ```bash
    docker build -t flask-static-app .
    ```

3. **Start Minikube** (if not already started):
    ```bash
    minikube start
    ```

4. **Apply the Kubernetes deployment**:
    ```bash
    kubectl apply -f k8s/deployment.yaml
    kubectl apply -f k8s/service.yaml
    ```

5. **Access the app**:
    ```bash
    minikube service flask-service
    ```

This will open the Flask app running on your local Minikube Kubernetes cluster.

## License
This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

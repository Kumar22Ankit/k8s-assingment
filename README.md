# Hello Kubernetes with NGINX

This project demonstrates a simple HTML page served using an NGINX Docker container. The HTML page displays a "Hello, World from Kubernetes!" message.

## Project Structure
. ├── app/ 
│ └── index.html # The HTML file to be served
├── demo/ 
│ └── video explaination of the project
├── docker/ 
│ └── Dockerfile # Dockerfile to build the NGINX image
└── README.md # Project documentation

## Prerequisites

- Docker installed on your system.

## Steps to Build and Run the Project

1. **Clone the Repository**:
```bash
git clone https://github.com/Kumar22Ankit/k8s-assingment.git
cd assingment
```

2. **Build the Docker Image: Run the following command to build the Docker image:**
```bash
docker build -t hello-world-nginx ..
docker run -d -p 8080:80 hello-world-nginx
```
3. **Apply the Deployment & service: Apply the deployment & service to your Kubernetes cluster:**
```bash
kubectl apply -f k8s/
```
4. **Using Port Forwarding**
If you are running this application in a Kubernetes cluster, you can use port forwarding to access the application:
```bash
kubectl port-forward service/hello-world-service 8080:80
```

5. **Access the Application: Open your browser and navigate to:**
http://localhost:8080

You should see the "Hello, World from Kubernetes!" message.
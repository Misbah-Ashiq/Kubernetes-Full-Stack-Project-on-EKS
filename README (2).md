# Kubernetes Full-Stack Application on AWS EKS

## 📌 Project Overview
This project demonstrates the deployment of a **Full-Stack Application** (Frontend + Backend + MySQL Database) on **Amazon EKS (Elastic Kubernetes Service)**.  
It uses **ECR** for container image storage and **Kubernetes Deployments & Services** for orchestration.

---

## 🏗️ Architecture
The system consists of:
- **Frontend**: Handles the user interface.
- **Backend**: Provides business logic and API endpoints.
- **MySQL Database**: Stores persistent application data.
- **ECR**: Stores Docker images for frontend and backend services.
- **EKS Cluster**: Manages deployments and services.

![Architecture Diagram](architecture.png)

---

## 🚀 Features
- Kubernetes-based deployment for scalability and resilience.
- AWS ECR integration for container image management.
- Microservices architecture (Frontend + Backend).
- Persistent storage for MySQL using PVC (PersistentVolumeClaim).
- Service exposure via Kubernetes Services (ClusterIP, NodePort, or LoadBalancer).

---

## ⚙️ Technologies Used
- **AWS EKS**
- **AWS ECR**
- **Kubernetes**
- **Docker**
- **MySQL**
- **Flask (Backend)**
- **React (Frontend)**

---

## 📂 Project Structure
```
eks-project/
├── backend/        # Flask backend application
├── frontend/       # React frontend application
├── k8s/            # Kubernetes manifests (YAML files)
├── architecture.png # Architecture diagram
└── README.md       # Project documentation
```

---

## 📖 Deployment Steps
1. **Build and Push Images to ECR**
   ```bash
   docker build -t <ecr-repo-uri>:latest ./backend
   docker build -t <ecr-repo-uri>:latest ./frontend
   docker push <ecr-repo-uri>:latest
   ```

2. **Apply Kubernetes Manifests**
   ```bash
   kubectl apply -f k8s/mysql-deployment.yaml
   kubectl apply -f k8s/backend-deployment.yaml
   kubectl apply -f k8s/frontend-deployment.yaml
   ```

3. **Check Pods & Services**
   ```bash
   kubectl get pods
   kubectl get svc
   ```

4. **Access Application**
   - Use the LoadBalancer/NodePort URL for frontend.
   - The frontend communicates with backend which interacts with MySQL.

---

## 👨‍💻 Author

Developed by **Misbah Ashiq**  

- 📧 Contact: misbahdevops46@gmail.com
- GitHub: [Misbah-Ashiq](https://github.com/Misbah-Ashiq/Kubernetes-Full-Stack-Project-on-EKS.git)
- Linkedin: [Misbah Ashiq](www.linkedin.com/in/misbah-ashiq-14a0aa356)
- UpWork: [Misbah Ashiq](https://www.upwork.com/freelancers/~0174d196bc738ae9ea)


Hey there! 🚀 Welcome to my DevOps & Cloud Computing Showcase!

🌐 This project demonstrates a 3-tier architecture deployed on AWS EKS with Kubernetes. Here’s the breakdown:

🔧 DevOps Magic

Built and containerized a frontend, backend, and database using Docker.
Set up a CI/CD pipeline with GitHub Actions to build, test, and deploy automatically.
Docker images pushed to DockerHub and seamlessly deployed to EKS.
☁️ Cloud-Native Infrastructure

Everything runs on Amazon Elastic Kubernetes Service (EKS).
Kubernetes handles scaling and service discovery.
Configured Load Balancers to expose services and manage traffic.
Persistent Volumes on Amazon EFS for reliable database storage.
⚡ Key Features

Microservices architecture for scalability and resilience.
Automated deployments for efficiency and speed.
Entire infrastructure is managed through Kubernetes manifests.
Ready to see cloud-native and DevOps in action? Let’s dive in! 🚢

### To start the application:

1. **Run each Dockerfile and publish the image to your DockerHub** or just use the pre-built images:  
   [Pre-built Images](https://hub.docker.com/u/krisssssssss) (already in the source code).  

2. **Set up cluster infrastructure:**  
   - **Create a cluster:**  
     ```bash
     eksctl create cluster --name <name-of-cluster> --region <region> --node-type t3.medium --nodes 3 --nodes-min 3 --nodes-max 6 --managed
     ```  

   - **Apply the manifests:**  
     ```bash
     kubectl apply -f frontend.yaml
     kubectl apply -f backend.yaml
     kubectl apply -f postgres.yaml
     ```  

   - **Get the DNS:**  
     ```bash
     kubectl get svc frontend-service
     ```  
     Copy the external IP and paste it into your browser.  

Enjoy! 🎉






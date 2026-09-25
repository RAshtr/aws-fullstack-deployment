# AWS Full-Stack Multi-Stage Deployment

A full-stack application consisting of an Express (Node.js) frontend and a Flask (Python) REST backend, deployed across multiple architectures on Amazon Web Services (AWS) ending with a containerized deployment on AWS ECS Fargate.

---

## Live Deployment & Repository Links

- **Live Deployed URL:** http://43.204.19.83:3000
- **GitHub Repository:** https://github.com/RAshtr/aws-fullstack-deployment

---

## Project Structure

```text
AWS_Ravi_Shankar_Tripathi/
├── AWS_Ravi_Shankar_Tripathi.pdf    # Complete documentation with screenshots
├── course-ravi.pem                  # Key pair for EC2 instances
└── app/                             # Source code directory
    ├── backend/
    │   ├── app.py
    │   ├── requirements.txt
    │   └── Dockerfile
    ├── frontend/
    │   ├── public/
    │   │   └── index.html
    │   ├── package.json
    │   ├── server.js
    │   └── Dockerfile
    ├── docker-compose.yml
    ├── .gitignore
    └── README.md

Deployment Architecture Overview
Task 1 (Single EC2 Instance): Both Flask backend (Port 5000) and Express frontend (Port 3000) deployed on a single Ubuntu t2.micro instance communicating via 127.0.0.1:5000.

Task 2 (Separated EC2 Instances): Decoupled backend and frontend across two independent Ubuntu t2.micro instances with configured Security Groups.

Task 3 (Serverless Containers with ECR & ECS Fargate):

Containerized both services using Docker.

Pushed images to private Amazon ECR repositories (fullstack-backend, fullstack-frontend).

Deployed as a multi-container task on an AWS ECS Fargate cluster (course) with public IP access enabled.

Ports & Services Configuration
Frontend: Port 3000

Backend API: Port 5000

Region: ap-south-1 (Asia Pacific - Mumbai)

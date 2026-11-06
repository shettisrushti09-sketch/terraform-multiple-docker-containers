# Deploy Multiple Docker Containers Using Terraform

## 1. Project Overview

This project demonstrates Infrastructure as Code (IaC) using Terraform to deploy and manage multiple Docker containers.

Two Docker containers are created:
- **Nginx:** A web server running on port 8080.
- **Python HTTP Server:** A Python-based HTTP server running on port 8081.

Terraform automates the creation and management of Docker images and containers.

## 2. Technologies Used

- Terraform
- Docker
- Nginx
- Python 3.12
- HCL (HashiCorp Configuration Language)

## 3. Project Structure

```text
terraform-multiple-containers/
│
├── main.tf
├── .terraform.lock.hcl
├── .gitignore
├── README.md
│
└── screenshots/
    ├── 01-docker-version.png
    ├── 02-docker-ps.png
    ├── 03-terraform-version.png
    ├── 04-terraform-init.png
    ├── 05-terraform-validate.png
    ├── 06-terraform-fmt.png
    ├── 07-terraform-plan.png
    ├── 08-terraform-apply.png
    ├── 09-docker-images.png
    ├── 10-running-containers.png
    ├── 11-nginx.png
    └── 12-python-server.png
```

## 4. Container Configuration

| Container | Docker Image | Host Port | Container Port |
|---|---|---:|---:|
| Nginx | nginx:alpine | 8080 | 80 |
| Python | python:3.12-slim | 8081 | 8000 |

## 5. Implementation Steps

1. Install and verify Docker and Terraform.
2. Configure the Docker provider in Terraform.
3. Define the required Docker images.
4. Define the Nginx and Python containers.
5. Initialize the Terraform working directory.
6. Validate and format the Terraform configuration.
7. Generate and review the execution plan.
8. Apply the configuration to create the containers.
9. Verify the running containers and test the web servers.

## 6. Terraform Commands

```powershell
terraform init
terraform validate
terraform fmt
terraform plan
terraform apply
```

Useful Docker verification commands:

```powershell
docker images
docker ps
```

## 7. Access the Applications

After successful deployment, open these URLs in a browser:

- Nginx: http://localhost:8080
- Python HTTP Server: http://localhost:8081

## 8. Expected Results

- Terraform successfully initializes and validates the configuration.
- Both Docker images are available.
- Both containers are created and running.
- The Nginx welcome page is accessible on port 8080.
- The Python HTTP server directory listing is accessible on port 8081.

Screenshots of the implementation and verification are available in the `screenshots` directory.

## 9. Conclusion

This experiment demonstrates how Terraform can automate Docker infrastructure management. Multiple containers can be provisioned and managed through configuration files instead of creating them manually.

The project provides practical experience with Infrastructure as Code, Docker containerization, and Terraform resource management.
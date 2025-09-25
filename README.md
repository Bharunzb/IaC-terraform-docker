# IaC-terraform-docker
# Terraform Docker task : Nginx Container

## Objective
Provision a local Docker container using Terraform on an Amazon Linux EC2 instance.

## Tools Used
- Terraform
- Docker
- Amazon Linux 2 (EC2)

## Steps Performed
1. Launched an Amazon Linux 2 EC2 instance.
2. <img width="1917" height="1075" alt="Screenshot 2025-09-25 132903" src="https://github.com/user-attachments/assets/eaa0a65f-d599-4436-ab6c-866da9b46c23" />

3. Installed Docker and started the Docker service.
4. Installed Terraform CLI.
5. Created `main.tf` to define the Docker image and container.
6. Initialized Terraform: `terraform init`.
7.  <img width="1917" height="1072" alt="Screenshot 2025-09-25 130845" src="https://github.com/user-attachments/assets/ea2424c3-3efa-4226-8d1c-0248792e91d1" />

6.Planned the infrastructure: `terraform plan`.
7.  <img width="1919" height="1077" alt="Screenshot 2025-09-25 130954" src="https://github.com/user-attachments/assets/09213272-9754-4130-a6f5-b470064a57a8" />
<img width="1919" height="1079" alt="Screenshot 2025-09-25 131004" src="https://github.com/user-attachments/assets/8d55b270-8814-40fc-8b1f-0b382051bba4" />
 
9. Applied the plan: `terraform apply`.
10. <img width="1908" height="1079" alt="Screenshot 2025-09-25 131037" src="https://github.com/user-attachments/assets/4b4e1ece-e86b-42d9-a2e1-7b2ff24bc2c8" />
 12. Verified container: `docker ps` and accessed `http://<EC2_PUBLIC_IP>:8000`.
 13. <img width="1623" height="303" alt="Screenshot 2025-09-25 133638" src="https://github.com/user-attachments/assets/bdc6e1f2-3e3c-4871-aac5-2cee4ff5ff7f" />

<img width="1913" height="1058" alt="Screenshot 2025-09-25 130654" src="https://github.com/user-attachments/assets/48db563e-2bce-4773-a946-6981b497ecee" />
Check terraform state command

<img width="1919" height="460" alt="Screenshot 2025-09-25 131151" src="https://github.com/user-attachments/assets/0b2954bd-3682-47f7-90e7-5f854977ad08" />

14. Destroyed infrastructure after testing: `terraform destroy`.
<img width="1917" height="1075" alt="image" src="https://github.com/user-attachments/assets/a1891696-ae04-457e-8fe8-61051046cf72" />

## Directory Structure
.
├── main.tf
├── terraform.tfstate
├── terraform.tfstate.backup
└── README.md

## Terraform Commands Used
```bash
terraform init
terraform plan 
terraform apply --auto-approve
terraform state list
terraform show
terraform destroy

# Ansible Playbook: Deploy Nginx Ingress and Sample Application on Kubernetes

This Ansible playbook automates the deployment of an Nginx Ingress controller and a sample "Hello World" application on a Kubernetes cluster. The playbook also implements TLS termination using a self-signed certificate.

## Table of Contents
- [Requirements](#requirements)
- [Playbook Structure](#playbook-structure)
- [Usage](#usage)

## Requirements
- **Kubernetes Cluster:** Ensure you have a running Kubernetes cluster.
- **Ansible:** Installed on your local machine or control node.
- **kubectl and Helm:** Available on the machine running the playbook.
- **Access to the Kubernetes Cluster:** Ensure you have cluster admin privileges.

## Playbook Structure

- **`deploy_k8s.yml`:** The main playbook file containing all tasks.
- **`/tmp/hello-world-tls.yaml`:** Temporary manifest file generated by the playbook for deploying the sample application with TLS.

## Usage

1. Go to https://killercoda.com/playgrounds/scenario/kubernetes [This will give empty k8s cluster for 60min]
2. **Install Ansible**
   ```bash
   apt install ansible
3. **Clone the Repository:**
   ```bash
   git clone https://github.com/swapnilraw15/AshnikAssignment.git
   cd  AshnikAssignment/
4. **Run the Playbook:**
   ```bash
   ansible-playbook deploy_k8s.yml
This command will execute all the tasks in the playbook, deploying the Nginx Ingress controller and the "Hello World" application with TLS.

5. **Access the application:**
   - Click on hamburger on right top and go to traffic/ports
   - Access application using port 30007

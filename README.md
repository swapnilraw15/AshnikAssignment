# Ansible Playbook: Deploy Nginx Ingress and Sample Application on Kubernetes

This Ansible playbook automates the deployment of an Nginx Ingress controller and a sample "Hello World" application on a Kubernetes cluster. The playbook also implements TLS termination using a self-signed certificate.

## Table of Contents
- [Requirements](#requirements)
- [Playbook Structure](#playbook-structure)
- [Usage](#usage)
- [Tasks Breakdown](#tasks-breakdown)
- [Troubleshooting](#troubleshooting)

## Requirements
- **Kubernetes Cluster:** Ensure you have a running Kubernetes cluster.
- **Ansible:** Installed on your local machine or control node.
- **kubectl and Helm:** Available on the machine running the playbook.
- **Access to the Kubernetes Cluster:** Ensure you have cluster admin privileges.

## Playbook Structure

- **`deploy_k8s.yml`:** The main playbook file containing all tasks.
- **`/tmp/hello-world-tls.yaml`:** Temporary manifest file generated by the playbook for deploying the sample application with TLS.

## Usage

1. **Clone the Repository:**
   ```bash
   git clone <repository_url>
   cd <repository_directory>
2. **Run the Playbook:**
   ```bash
   ansible-playbook deploy_k8s.yml
   
   This command will execute all the tasks in the playbook, deploying the Nginx Ingress controller and the "Hello World" application with TLS.

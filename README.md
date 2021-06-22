# README

## Requirements

- Ansible >= 2.10

## Features

- Installs Docker and Kubernetes on host specified in `hosts` file
- Performs basic server hardening on the server
- Assigns kubernetes master and worker nodes

## Usage

1. Run `ansible-playbook main.yaml` to run all playbooks in intended sequence.

### About Docker Installation
Docker is installed using the [Docker Docks].

### About Kubernetes Installation
Docker is installed using the [Kubernetes Docks].


   [Docker Docks]: <https://docs.docker.com/engine/install/ubuntu/#install-using-the-repository>
   [Kubernetes Docks]: <https://kubernetes.io/docs/setup/production-environment/tools/kubeadm/install-kubeadm/#installing-kubeadm-kubelet-and-kubectl>
   

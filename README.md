# README

## Requirements

- Ansible >= 2.10

## Features

- Installs Docker and Kubernetes on host specified in `hosts` file
- Performs basic server hardening on the server

## Usage

1. Run `ansible-playbook install.yaml` to install docker and kubernetes on the server.
2. Run `ansible-playbook server-hardening.yaml` to being server hardening.

### About Docker Installation
Docker is installed using the [Docker Docks].

### About Kubernetes Installation
Docker is installed using the [Kubernetes Docks].

### About Server Hardening
The `server-hardening.yaml` playbook performs the following tasks on the server
* Updates and upgrades the packages
* Uses [unattended-upgrades] to automate the package upgradation process
* Creates a user "user" in the "root" group
* Applies the following changes to `/etc/ssh/sshd_config` file:
    * Disables empty password login
    * Disables remote root login
    * Disables password login
    * Changes ssh port from 22 to 4268 (!!)

## Note
1. To access the machine (Before server hardening):
    ```sh
    ssh -i keys/id_ed25519 root@207.148.73.66
    ```
2. To access the machine (After server hardening):
    ```sh
    ssh -i keys/user user@207.148.73.66 -p 4268
    ```



   [unattended-upgrades]: <https://wiki.debian.org/UnattendedUpgrades#Automatic_call_via_.2Fetc.2Fapt.2Fapt.conf.d.2F20auto-upgrades>
   [Docker Docks]: <https://docs.docker.com/engine/install/ubuntu/#install-using-the-repository>
   [Kubernetes Docks]: <https://kubernetes.io/docs/setup/production-environment/tools/kubeadm/install-kubeadm/#installing-kubeadm-kubelet-and-kubectl>
   

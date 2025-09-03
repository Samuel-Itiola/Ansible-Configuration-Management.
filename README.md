# Ansible-Configuration-Management.
Ansible playbook with roles for automated Linux server setup, Nginx configuration, SSH key management, and static website deployment.


# Ansible Server Setup

This project demonstrates **Configuration Management with Ansible**.  
It provisions a Linux server on AWS (or any cloud provider), installs required packages, configures Nginx, manages SSH keys, and deploys a static website.

---

## 🚀 Features
- **Base role**: Updates server, installs utilities, sets up security tools like fail2ban.
- **Nginx role**: Installs and configures Nginx to serve a static site.
- **App role**: Deploys a static HTML/CSS website from an archive.
- **SSH role**: Adds developer’s SSH public key for secure access.

---

## 📂 Project Structure

# Ansible Server Setup

Automated Linux server provisioning using **Ansible**.  
This project sets up a Linux server, installs utilities, configures Nginx, deploys a static website, and manages SSH access.

---

## 🚀 Features
- **Base role**: Updates OS, installs utilities (git, curl, vim, htop), sets up `fail2ban`.
- **Nginx role**: Installs and configures Nginx, points to the deployed website.
- **App role**: Uploads and extracts a static website archive.
- **SSH role**: Adds the developer’s public key for passwordless SSH login.

---

## 📂 Project Structure

```text
ansible-server-setup/
├── inventory.ini          # Server inventory (hosts, SSH key path)
├── setup.yml              # Main playbook orchestrating roles
├── 2137_barista_cafe.zip  # Static website archive
├── ansiblekey.pem         # AWS EC2 private key (control node, do not commit)
├── id_ed25519.pub         # Developer public key
└── roles/
    ├── base/              # Basic server setup
    ├── nginx/             # Nginx installation & configuration
    ├── app/               # Website deployment
    └── ssh/               # SSH key management


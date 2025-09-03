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

ansible-server-setup/
├── inventory.ini          # Server inventory (hosts, SSH key path)
├── setup.yml              # Main playbook orchestrating roles
├── 2137_barista_cafe.zip  # Static website archive
├── ansiblekey.pem         # AWS EC2 private key (control node)
├── id_ed25519.pub         # Developer public key
└── roles/
    ├── base/
    │   └── tasks/
    │       └── main.yml        # Update OS, install utilities, fail2ban
    ├── nginx/
    │   ├── tasks/
    │   │   └── main.yml        # Install & configure Nginx
    │   └── templates/
    │       └── site.conf.j2    # Optional Nginx config template
    ├── app/
    │   └── tasks/
    │       └── main.yml        # Upload & extract website
    └── ssh/
        └── tasks/
            └── main.yml        # Add developer public key to server

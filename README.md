<!-- Badges (using shields.io for visual appeal) -->
![Vagrant](https://img.shields.io/badge/Vagrant-%3E%3D2.2-blue?logo=vagrant&logoColor=white)
![Provider](https://img.shields.io/badge/Provider-VirtualBox-lightgrey?logo=virtualbox&logoColor=white)
![Box](https://img.shields.io/badge/Box-CentOS_Stream_9-red?logo=centos&logoColor=white)
![License](https://img.shields.io/badge/License-MIT-green)

# 🏦 Mini Finance Vagrant Setup

## 🚀 Project Description
This repository provides a Vagrant configuration and provisioning script to spin up a CentOS Stream 9 VM, install Apache (httpd), download a “mini finance” HTML template, and deploy it under `/var/www/html`. Ideal for demos, learning VM provisioning, or quickly standing up a static site environment in a reproducible way.

> **Level**: Intermediate  
> Requires some familiarity with Vagrant, Linux basics, and Git.

---

## 📋 Table of Contents
1. [Features](#features)  
2. [Prerequisites](#prerequisites)  
3. [Installation & Setup](#installation--setup)  
4. [Accessing the Deployed Site](#accessing-the-deployed-site)  
5. [Customization & Configuration](#customization--configuration)  
6. [Usage Examples](#usage-examples)  
7. [Troubleshooting](#troubleshooting)  
8. [Project Structure](#project-structure)  
9. [Contributing](#contributing)  
10. [License](#license)  
11. [Contact](#contact)

---

## ✨ Features
- **Automated VM Provisioning**: Single `vagrant up` command to:
  - Download the CentOS Stream 9 box (`eurolinux-vagrant/centos-stream-9`).
  - Install and enable Apache (`httpd`).
  - Fetch and deploy the “mini finance” HTML template.
  - Clean up temporary files.
- **Networking**:
  - Private network with a fixed IP (configurable).
  - Optionally bridged network for direct LAN access.
- **Lightweight & Reproducible**:
  - Inline shell provisioning for quick demo.
  - Easily extendable to full LAMP or other stacks.
- **Customization Hooks**:
  - Modify package list, template URL, memory, or networking settings in one Vagrantfile.
  - Add synced folders, forwarded ports, extra provisioning tools.
- **Cross-Platform Host Support**:
  - Works on Windows/macOS/Linux hosts with VirtualBox (or other providers).

---

## ⚙️ Prerequisites
Before you begin, ensure you have:
- **Host Machine**:
  - Vagrant installed (≥ 2.2.0). Verify with:
    ```bash
    vagrant --version
    ```
  - VirtualBox installed (or another supported Vagrant provider). Verify VirtualBox installation as per your OS.
- **Git & GitHub**:
  - A GitHub account (to clone/fork this repo or contribute).
  - Git installed locally to clone and version your own changes.
- **Basic Knowledge**:
  - Command-line / terminal usage.
  - Basic Linux commands and system administration (installing packages, checking logs, `systemctl`).
  - Understanding of Vagrant workflows: `vagrant up`, `vagrant ssh`, `vagrant halt`, etc.
- **Networking Considerations**:
  - Ensure chosen private-network IP does not conflict with existing host networks.
  - If using bridged networking, you may need host network permissions.

---

## 🚀 Installation & Setup

1. **Clone the repository**:
   ```bash


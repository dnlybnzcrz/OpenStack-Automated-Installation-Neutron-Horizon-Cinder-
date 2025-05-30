# OpenStack Automated Installation (Neutron, Horizon, Cinder)

An automated Ansible-based deployment solution for OpenStack core components including Neutron (Networking), Horizon (Dashboard), and Cinder (Block Storage).

## Overview

This repository contains Ansible playbooks and roles for automating the installation and configuration of essential OpenStack components on Ubuntu servers. The deployment is designed to set up a functional OpenStack environment with networking, storage, and dashboard capabilities.

## Components

- **Neutron**: OpenStack Networking service
- **Horizon**: OpenStack Dashboard web interface
- **Cinder**: OpenStack Block Storage service

## Prerequisites

- Ubuntu server(s)
- Ansible installed on the control node
- SSH access to target servers
- Proper network connectivity between nodes
- Python installed on target nodes

## Repository Structure

```
.
├── roles/
│   ├── NEUTRON/    # Neutron networking service configuration
│   ├── HORIZON/    # Dashboard installation and setup
│   ├── CINDER/     # Block storage service configuration
├── ansible.cfg     # Ansible configuration
├── config.yml      # Main playbook configuration
└── inventory       # Inventory file for target hosts
```

## Configuration

The deployment is configured through the following files:

- `config.yml`: Main playbook that orchestrates the installation
- `inventory`: Defines the target hosts
- `ansible.cfg`: Ansible configuration settings

## Usage

1. Update the `inventory` file with your target hosts
2. Verify connectivity to all hosts
3. Run the playbook:

```bash
ansible-playbook -i inventory config.yml
```

## Features

- Automated dpkg configuration fixing
- System updates and upgrades handling
- Modular role-based installation
- Separate configuration for controller node

## Requirements

- Ubuntu Server (recommended version: 20.04 LTS or later)
- Ansible 2.9+
- Sufficient system resources as per OpenStack requirements
- Network access to Ubuntu repositories

## Contributing

Contributions are welcome! Please feel free to submit a Pull Request.

## Support

For issues and feature requests, please open an issue in the GitHub repository.

---
*Note: Make sure to properly configure your OpenStack environment variables and security settings before deploying to production.*

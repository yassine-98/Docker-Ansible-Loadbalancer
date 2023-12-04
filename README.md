# Nginx Load Balancer Setup with Ansible

## Project Overview

The purpose of this project is to set up an Nginx load balancer server using Ansible and Docker.

## Prerequisites

Ensure that Docker and Docker Compose are installed on your local machine.

## Setup Instructions

### 1. Build Services

```bash
docker-compose up -d
```

### 2. Execute Ansible Playbook

Execute the Ansible playbook inside the master container:

```bash
docker-compose exec master ansible-playbook /etc/ansible/playbooks/playbook.yml
```

### 3. Run Curl Command

Run the Curl command from the machine that you have mapped with the lb container:

```bash
curl localhost
```
or
```bash
curl lb_ip_address  # e.g., 172.17.0.4
```







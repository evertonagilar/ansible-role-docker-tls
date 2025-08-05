# Ansible Role: docker-tls

![Ansible Galaxy](https://img.shields.io/badge/Ansible--Galaxy-docker__tls-blue?style=flat-square)
![License](https://img.shields.io/github/license/evertonagilar/ansible-role-docker_tls?style=flat-square)

## Description

This Ansible role installs **Docker Engine** with **TLS support** on Debian-based systems. It generates **self-signed X.509 certificates** to enable secure communication with the Docker daemon over TCP.

---

## Features

- Installs Docker Engine on Ubuntu/Debian
- Generates a local Certificate Authority (CA)
- Creates self-signed certificates for client and server authentication
- Configures the Docker daemon to expose `tcp://0.0.0.0:2376` with TLS enabled
- Copies client certificates to `~/.docker/` for convenient CLI usage

---

## Supported Platforms

- Ubuntu 20.04+
- Debian 11+

---

## Example Usage

```yaml
- hosts: docker_hosts
  become: true
  roles:
    - role: evertonagilar.docker-tls

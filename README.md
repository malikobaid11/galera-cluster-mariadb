# galera-cluster-mariadb

# Galera Cluster with MariaDB

This repository provides step-by-step instructions and scripts to configure a Galera Cluster with MariaDB on Ubuntu 18.04 servers.

## Features
- Multi-master database clustering
- Synchronous replication
- High availability

## Getting Started
Follow the detailed guides in the [docs](docs/) directory for installation and configuration.

## Repository Structure
- `docs/`: Documentation for each step of the setup process
- `scripts/`: Scripts for automating installation and setup

## Prerequisites
- Ubuntu 18.04 servers
- Root access to the servers
- Servers with the following IPs:
  - Server1: `10.0.0.5`
  - Server2: `10.0.0.6`
  - Server3: `10.0.0.7`

## Usage
1. Clone this repository:
    ```bash
    git clone https://github.com/yourusername/galera-cluster-mariadb.git
    cd galera-cluster-mariadb
    ```
2. Follow the [installation guide](/installation.md).


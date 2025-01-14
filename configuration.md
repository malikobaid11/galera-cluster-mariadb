# Configuration Guide

## Configuring Nodes
Edit the Galera configuration file on each server:
```bash
sudo nano /etc/mysql/conf.d/galera.cnf
```

Add the following content:

```
[mysqld]
binlog_format=ROW
default-storage-engine=innodb
innodb_autoinc_lock_mode=2
bind-address=0.0.0.0

# Galera Provider Configuration
wsrep_on=ON
wsrep_provider=/usr/lib/galera/libgalera_smm.so

# Galera Cluster Configuration
wsrep_cluster_name="test_cluster"
wsrep_cluster_address="gcomm://10.0.0.5,10.0.0.6,10.0.0.7"

# Galera Synchronization Configuration
wsrep_sst_method=rsync

# Galera Node Configuration
wsrep_node_address="server_ip"
wsrep_node_name="node_name"
```

#### `scripts/install_mariadb.sh`
```bash
#!/bin/bash
# Script to install MariaDB and rsync on Ubuntu 18.04

echo "Updating system and installing MariaDB..."
sudo apt update
sudo apt install -y mariadb-server rsync

echo "MariaDB and rsync installed."
```

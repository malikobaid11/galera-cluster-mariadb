# Installation Guide

## Adding MariaDB Repositories
1. Add the MariaDB GPG key:
    ```bash
    sudo apt-key adv --recv-keys --keyserver hkp://keyserver.ubuntu.com:80 0xF1656F24C74CD1D8
    ```
2. Add the repository:
    ```bash
    sudo add-apt-repository 'deb [arch=amd64] http://nyc2.mirrors.digitalocean.com/mariadb/repo/10.4/ubuntu bionic main'
    ```
3. Update the package list:
    ```bash
    sudo apt update
    ```

## Installing MariaDB
1. Install MariaDB:
    ```bash
    sudo apt install mariadb-server
    ```
2. Secure the installation:
    ```bash
    sudo mysql_secure_installation
    ```
3. Install rsync:
    ```bash
    sudo apt install rsync
    ```

Continue to [Configuration Guide](configuration.md).


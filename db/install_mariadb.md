# How to Install MariaDB 10.1 on CentOS 7

In this article, we will outline the process of installing PHP 7.x MariaDB 10.1, the latest stable release of the MariaDB 10.x series at the time of writing this article, on CentOS 7.

Prerequisites:

    An up-to-date CentOS 7 Server.
    A sudo user.

# Step 1: Create the MariaDB 10.1 YUM repo file
```
cat <<EOF | sudo tee -a /etc/yum.repos.d/MariaDB.repo
# MariaDB 10.1 CentOS repository list
# http://downloads.mariadb.org/mariadb/repositories/
[mariadb]
name = MariaDB
baseurl = http://yum.mariadb.org/10.1/centos7-amd64
gpgkey=https://yum.mariadb.org/RPM-GPG-KEY-MariaDB
gpgcheck=1
EOF
```
*Note: The code for setting up newer releases of MariaDB 10.x may wary in the future. You should always check out the official MariaDB website to confirm the code to be used.*

# Step 2: Install MariaDB 10.1 using YUM
```
sudo yum install MariaDB-server MariaDB-client -y
```
# Step 3: Start the MariaDB service and make it auto-start on system boot
```
sudo systemctl start mariadb.service
sudo systemctl enable mariadb.service
```
# Step 4: Secure the installation of MariaDB
```
sudo /usr/bin/mysql_secure_installation
```
Answer questions as below, and ensure that you will use your own MariaDB root password:

    Enter current password for root (enter for none): Just press the Enter button
    Set root password? [Y/n]: Y
    New password: your-MariaDB-root-password
    Re-enter new password: your-MariaDB-root-password
    Remove anonymous users? [Y/n]: Y
    Disallow root login remotely? [Y/n]: Y
    Remove test database and access to it? [Y/n]: Y
    Reload privilege tables now? [Y/n]: Y
    That's it. From now on, you can use MariaDB to create and maintain MySQL databases in accordance with your requirements.
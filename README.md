# Task 1 - Using Google Cloud
## Creating and configure a web server on Google Cloud Platform 

### Creating and configuring a VM
- Log in Google Cloud console 
- Press on Compute engine 
- Go to VM instance 
- Enable the Vm 
- Click on create instance 
- Select closest region 
- Select zone
- Select series and machine type
- Click on disk and change operating system to CentOS and select version 
- Enable Allow HTTP traffic 
- Enable Allow HTTPs traffic 
- create VM 
- Open in browser window

### Deploying Web Server 1st way
- sudo dnf update
- sudo dnf install httpd
- sudo systemctl start httpd
- sudo systemctl status httpd
- curl -4 icanhazip.com 
- sudo vi /var/www/html/index.html
- Configure the html file to make it readable 

### Deploying Web Server 2nd way
- curl -O https://wordpress.org/wordpress-6.0.2.tar.gz
- sudo dnf install httpd php-fpm php-json php-mysqlnd @mysql
- sudo systemctl enable --now httpd
- sudo systemctl enable php-fpm
- sudo systemctl start php-fpm
- sudo systemctl start httpd.service 
- sudo mv wordpress-6.0.2.tar.gz /var/www/html
- cd /var/www/html
- sudo tar xf wordpress-6.0.2.tar.gz
- sudo vi /etc/httpd/conf/httpd.conf
- sudo systemctl restart httpd
- sudo chown -R apache:apache wordpress
- sudo systemctl start mysqld
- sudo systemctl enable --now mysqld
- sudo systemctl status mysqld
- mysql_secure_installation
- mysql -u root -p
- cd /var/www/html
- cd wordpress
- sudo vi wp-config.php



### Links Used 
Installing Apache Web Server on CentOS
[https://www.digitalocean.com/community/tutorials/how-to-install-the-apache-web-server-on-centos-8]

create and start a VM instance
[https://cloud.google.com/compute/docs/instances/create-start-instance] 

Learn GitHub and how to use Markdown for documentation
[https://www.youtube.com/watch?v=yXY3f9jw7fg]

How to Install MySQL 8.0 on CentOS 8 / RHEL 8 
[https://www.tecmint.com/install-mysql-on-centos-8/]

How to Install WordPress with LAMP in RHEL-Based Distributions [https://www.tecmint.com/install-wordpress-with-apache-on-centos-rhel-fedora/]





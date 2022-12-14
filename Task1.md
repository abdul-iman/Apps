# Task 1 - Using Google Cloud
## Creating and configure a web server on Google Cloud Platform 

### Creating and configuring a VM
- Log in Google Cloud console 
- Press on Compute engine 
- Go to VM instance 
- Enable the VM
- Click on create instance 
- Select closest region 
- Select zone
- Select series and machine type
- Click on disk, change operating system to CentOS, and select version 
- Enable Allow HTTP traffic 
- Enable Allow HTTPs traffic 
- create VM 
- Open in browser window

### Deploying Web Server 1 option
- sudo dnf update
- sudo dnf install httpd - installing Apache 
- sudo systemctl start httpd - Starting 
- sudo systemctl status httpd - showing the status of the httpd service
- curl -4 icanhazip.com - Getting own IP address 
- sudo vi /var/www/html/index.html - configure the html to add more context

### Deploying Web Server 2nd option
- curl -O https://wordpress.org/wordpress-6.0.2.tar.gz - To download WordPress using curl 
##### WordPress is a LAMP stack application it runs on Linux, Apache HTTPd, MySQL and PHP
- sudo dnf install httpd php-fpm php-json php-mysqlnd @mysql
- sudo systemctl enable --now httpd
- sudo systemctl enable php-fpm
- sudo systemctl start php-fpm
- sudo systemctl start httpd.service - Now httpd is running and we should see the test page.
- sudo mv wordpress-6.0.2.tar.gz /var/www/html - This command will move WordPress to the requested directory.
- cd /var/www/html
- sudo tar xf wordpress-6.0.2.tar.gz - Inside the requested directory we can extract the file using this command
- sudo vi /etc/httpd/conf/httpd.conf - To deploy WordPress we must configure the conf file and change DocumentRoot from “/var/www/html” to “/var/www/html/wordpress”
- sudo systemctl restart httpd - Once any changes are made we must restart httpd
- sudo chown -R apache:apache wordpress - User and group both Apache 
- sudo systemctl start mysqld - starting MySQL
- sudo systemctl enable --now mysqld - Enabling MySQL
- sudo systemctl status mysqld
- mysql_secure_installation - Secure the MySQL installation by running this command
- mysql -u root -p - creating new database to host the wordpress
- cd /var/www/html/wordpress 
- sudo vi wp-config.php - creating this file in the wp-config.php file and and manully add paste a following text you get from wordpress installation


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
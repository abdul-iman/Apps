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

### Deploying Web Server
- sudo dnf update
- sudo dnf install httpd
- sudo systemctl start httpd
- sudo systemctl status httpd
- curl -4 icanhazip.com 
- sudo vi /var/www/html/index.html
- Configure the html file to make it readable 


### Links Used 
Installing Apache Web Server on CentOS
[https://www.digitalocean.com/community/tutorials/how-to-install-the-apache-web-server-on-centos-8]

create and start a VM instance
[https://cloud.google.com/compute/docs/instances/create-start-instance] 





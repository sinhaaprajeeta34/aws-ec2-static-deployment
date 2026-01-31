# Apache Web Server Setup Commands

## System Update
sudo yum update -y

## Install Apache
sudo yum install httpd -y

## Start and Enable Apache
sudo systemctl start httpd
sudo systemctl enable httpd

## Website Deployment
cd /var/www/html
sudo nano index.html

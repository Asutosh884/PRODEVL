PROJECT 2: LEMP STACK IMPLEMENTATION

*Step 1 – Installing the Nginx Web Server

 sudo apt update
 
 sudo apt install nginx
![image](https://user-images.githubusercontent.com/83317716/127902218-04171f74-23a1-45d8-9bf7-f4d26009d72e.png)

Verify ngnix was succefully installed and is running as service 

sudo systemctl status nginx

![image](https://user-images.githubusercontent.com/83317716/127902732-dd38d6e7-b35c-4e78-886f-137ecabf1c2a.png)

curl http://localhost:80

![image](https://user-images.githubusercontent.com/83317716/127903023-31ef8154-197b-4348-93c1-b2918231caf3.png)

Checking NGNIX on browser

![image](https://user-images.githubusercontent.com/83317716/127903293-649980b0-3fd5-45a5-bb9c-bbd6cfbc33f9.png)

STEP 2 — INSTALLING MYSQL

sudo apt install mysql-server

![image](https://user-images.githubusercontent.com/83317716/127903470-d65f420c-939f-4776-81bb-00675b9ea7c1.png)

sudo mysql

![image](https://user-images.githubusercontent.com/83317716/127903567-c3d7ed3d-3697-4a23-b6f6-8ff7db0c70c3.png)

STEP 3 – INSTALLING PHP

sudo apt install php-fpm php-mysql

![image](https://user-images.githubusercontent.com/83317716/127903891-f3962c84-5d6a-4780-8018-5a75b843606c.png)

STEP 4 — CONFIGURING NGINX TO USE PHP PROCESSOR

sudo mkdir /var/www/projectLEMP

sudo chown -R $USER:$USER /var/www/projectLEMP

sudo nano /etc/nginx/sites-available/projectLEMP

sudo nginx -t

![image](https://user-images.githubusercontent.com/83317716/127904230-d0af4139-c6b4-476d-a2a7-cba0811bee2c.png)

sudo unlink /etc/nginx/sites-enabled/default

sudo systemctl reload nginx

sudo echo 'Hello LEMP from hostname' $(curl -s http://169.254.169.254/latest/meta-data/public-hostname) 'with public IP' $(curl -s http://169.254.169.254/latest/meta-data/public-ipv4) > /var/www/projectLEMP/index.html

STEP 5 – TESTING PHP WITH NGINX

sudo nano /var/www/projectLEMP/info.php

![image](https://user-images.githubusercontent.com/83317716/127905295-b1db8710-aff4-461a-9e36-4b1ca1aed7e9.png)

sudo rm /var/www/your_domain/info.php

STEP 6 – RETRIEVING DATA FROM MYSQL DATABASE WITH PHP

sudo mysql

mysql> CREATE DATABASE `example_database`;

mysql>  CREATE USER 'example_user'@'%' IDENTIFIED WITH mysql_native_password BY 'password';

mysql> GRANT ALL ON example_database.* TO 'example_user'@'%';

![image](https://user-images.githubusercontent.com/83317716/127905555-3ac5a39e-b924-4d18-b1cd-7f97b37da479.png)

mysql -u example_user -p

mysql> SHOW DATABASES;

![image](https://user-images.githubusercontent.com/83317716/127905648-f9962a34-4edb-4582-b1d9-04ee4e97e215.png)

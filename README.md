# Step 1 — Installing Apache and Updating the Firewall
- #update a list of packages in package manager
- $ sudo apt update
![image](https://user-images.githubusercontent.com/83317716/116784031-99b97900-aaaf-11eb-840b-7d4e5ac3525b.png)

- #run apache2 package installation
- $ sudo apt install apache2
![image](https://user-images.githubusercontent.com/83317716/116784083-d5544300-aaaf-11eb-9f39-f61a6732ee73.png)

- To verify that apache2 is running as a Service in our OS
- sudo systemctl status apache2
- ![image](https://user-images.githubusercontent.com/83317716/116784122-19474800-aab0-11eb-8397-05575c5cf43c.png)

- To access it on ubuntu shell
- curl http://localhost:80
- ![image](https://user-images.githubusercontent.com/83317716/116784148-4ac01380-aab0-11eb-94cd-fe34b88ee180.png)

- Testing apache HTTP webserver response from internet
- http://<Public-IP-Address>:80
- ![image](https://user-images.githubusercontent.com/83317716/116784333-57913700-aab1-11eb-94b5-cd2a8d6ca7d2.png)

# Step 2 — Installing MySQL
- sudo apt install mysql-server
- ![image](https://user-images.githubusercontent.com/83317716/116784412-ab9c1b80-aab1-11eb-86f8-de6b8d85e35c.png)
- sudo mysql_secure_installation
- ![image](https://user-images.githubusercontent.com/83317716/116784487-10f00c80-aab2-11eb-9f60-ea391403b6d3.png)
- log into mysql
- sudo mysql
- ![image](https://user-images.githubusercontent.com/83317716/116784511-3aa93380-aab2-11eb-9152-2f9e8616cee8.png)
- mysql > exit

# Step 3 — Installing PHP
- sudo apt install php libapache2-mod-php php-mysql
- ![image](https://user-images.githubusercontent.com/83317716/116784580-a8edf600-aab2-11eb-8841-ebefc3feaaf2.png)
- php -v
- ![image](https://user-images.githubusercontent.com/83317716/116784613-cde26900-aab2-11eb-9888-977cb4eb4e6b.png)

# Step 4 — Creating a Virtual Host for your Website using Apache
- sudo mkdir /var/www/projectlamp
- sudo chown -R $USER:$USER /var/www/projectlamp
- ![image](https://user-images.githubusercontent.com/83317716/116784669-24e83e00-aab3-11eb-9dfc-6cfb4d56ac69.png)
- sudo vi /etc/apache2/sites-available/projectlamp.conf
- sudo ls /etc/apache2/sites-available
- sudo a2ensite projectlamp
- sudo a2dissite 000-default
- sudo apache2ctl configtest
- sudo systemctl reload apache2
- ![image](https://user-images.githubusercontent.com/83317716/116784801-ca9bad00-aab3-11eb-9aa9-72625cbffd7f.png)
- sudo echo 'Hello LAMP from hostname' $(curl -s http://169.254.169.254/latest/meta-data/public-hostname) 'with public IP' $(curl -s http://169.254.169.254/latest/meta-data/public-ipv4) > /var/www/projectlamp/index.html
- showing the page in webbrowser

# Step 5 — Enable PHP on the website
- sudo vim /etc/apache2/mods-enabled/dir.conf
- cat /etc/apache2/mods-enabled/dir.conf
- ![image](https://user-images.githubusercontent.com/83317716/116785017-fbc8ad00-aab4-11eb-8fdd-8e71e80aade3.png)
- PHP site reload
- ![image](https://user-images.githubusercontent.com/83317716/116785149-9aeda480-aab5-11eb-9fcf-babdc5b30381.png)
- 




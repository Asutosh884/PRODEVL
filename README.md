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

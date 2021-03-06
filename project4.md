# MEAN STACK DEPLOYMENT TO UBUNTU IN AWS
In this assignment we are going to implement a simple Book Register web form using MEAN stack.

#Step 1: Install NodeJs

#sudo apt update

#sudo apt upgrade

Now we will Install NodeJS with below command

#sudo apt install -y nodejs

![step1-nodejs-installnodejs](https://user-images.githubusercontent.com/83317716/128594139-57f45a68-fa71-42df-a47d-4a7d79b5cc45.JPG)

#Step 2: Install MongoDB

#Install MongoDB : Below command install MongoDB

#sudo apt install -y mongodb

#![step2-mongodb-install](https://user-images.githubusercontent.com/83317716/128594424-e1ed3bf4-e103-48ee-8d2b-f8d03b3bcff8.JPG)

#Start The server

#sudo service mongodb start

#![step2-mongodb-start-status](https://user-images.githubusercontent.com/83317716/128594433-67bed117-f515-4dde-bbb7-85522298c8ca.JPG)


#Verify that the service is up and running

#sudo systemctl status mongodb

![step2-mongodb-start-status](https://user-images.githubusercontent.com/83317716/128595366-890441fa-89ec-46fa-8ee2-4d0341805f8e.JPG)

#sudo apt install -y npm

![step2-npm-install](https://user-images.githubusercontent.com/83317716/128595511-00e3e246-3b77-4c62-9aac-739c7114ba14.JPG)


#sudo npm install body-parser

![step2-bodyparser-install](https://user-images.githubusercontent.com/83317716/128595411-947be0c1-83ea-4195-b654-d9eeb547d965.JPG)

#mkdir Books && cd Books

#npm init

![step2-npm-init](https://user-images.githubusercontent.com/83317716/128595552-645fecb0-dba3-4ae9-9ec2-a6294949e859.JPG)

#Add a file with 

#vi server.js

#![step2-serverjs](https://user-images.githubusercontent.com/83317716/128595447-c3ae7f98-6119-49be-9067-82d54eebaa6b.JPG)


#Step 3: Install Express and set up routes to the server

#sudo npm install express mongoose

![step3-instalmoongose](https://user-images.githubusercontent.com/83317716/128595603-32e7d042-7b48-420d-aaa6-ad971be539eb.JPG)

#mkdir apps && cd apps

#vi routes.js

#mkdir models && cd models

#vi book.js

![step3-routesjs-models-books](https://user-images.githubusercontent.com/83317716/128595645-7fce36d5-334b-4ad5-85bc-3f97323aee55.JPG)

#Step 4 ??? Access the routes with AngularJS

#Change the directory back to ???Books???

#cd ../..

#mkdir public && cd public

#vi script.js

#vi index.html

![step4-indexhtml](https://user-images.githubusercontent.com/83317716/128595736-4acb22fd-e511-480a-99b2-4e2a008e886d.JPG)

#change directory to Books and Start the server with below command

#node server.js

![step4-node-serverjsstarted](https://user-images.githubusercontent.com/83317716/128595765-6ee2d1b6-7f7e-47fa-93a1-ba8ab0ba9b2b.JPG)

#we need to open TCP port 3300 in AWS Web Console for EC2 Instance.

#Now you can access our Book Register web application from the Internet with a browser using Public IP address or Public DNS name.

This is how your Web Book Register Application will look like in browser:

![step4-browserview](https://user-images.githubusercontent.com/83317716/128595840-29989c41-a7c4-417c-a181-0e3551c4373c.JPG)

     
     


     

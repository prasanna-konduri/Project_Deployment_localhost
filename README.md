# Project Deployment localhost
## Introduction:
This Project explains step by step process ofon deploying a project in local machine.
## Prerequisites:
1. OS - macOS - sonoma 14.5
2. Server - nginx version: nginx/1.27.0

## Deployment steps:
1. Install nginx through homebrew if not installed.

   ```
   homebrew install nginx
   ```
   
3. Then open nginx config file

   ```
   sudo nano /usr/local/etc/nginx/nginx.conf
   ```
   
5. To set up the local DNS you need to modify the '/etc/hosts' file. Attach your website name to the ip.

   ```
   sudo nano /etc/hosts
   127.0.0.1 awsomeweb
   ```
   
6. Add the following lines to the config file. check for the server section and add the following lines

   ```
   listen 8080;
   server_name  awesomeweb;
   #charset koi8-r;
   #access_log  logs/host.access.log  main;
   root /absolute/path/to/project;
   index index.html;
   ```
   
7. Check for any configuration errors and start the server
   ```
   sudo nginx -t
   sudo brew services restart nginx
   ```
9. Go to your web browser and type your website name. you can see your website with the given name.

    
   <img width="1440" alt="Screenshot 2024-08-07 at 12 13 56 AM" src="https://github.com/user-attachments/assets/c32eb887-61f0-4645-977a-ab39a2268767">
  

    

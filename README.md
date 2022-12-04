# ugarit devops task 

1. I have installed elastic search and kibana (both version 8.2.0) on my pc on ubuntu 18

2. configured Nginx to run as reverse http proxy, to access Kibana on port 8888. please check [kibana.conf](https://github.com/Dina-Adel-1302/ugarit/blob/bcc2c511da375c5369da3624a208a5e2149af4dc/kibana.conf)

  2.2. added user: elastic in nginx for accessing kibana. using the following command: 
     ```
     sudo htpasswd -c /etc/nginx/htpasswd.users elastic
     ```

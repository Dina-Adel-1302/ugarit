# ugarit devops task 

1. I have installed elastic search and kibana (both version 8.2.0) on my pc on ubuntu 18

2. configured Nginx to run as reverse http proxy, to access Kibana on port 8888. please check [kibana.conf]()
2.2 added user: elastic in nginx for accessing kibana. using the command 
```
sudo htpasswd -c /etc/nginx/htpasswd.users user_account
```

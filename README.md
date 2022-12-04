# ugarit devops task 

* I have installed elastic search and kibana (both version 8.2.0) on my pc on ubuntu 18. 

* added user test with the role safee.  

* configured Nginx to run as reverse http proxy, to access Kibana on port 8888. please check [kibana.conf](https://github.com/Dina-Adel-1302/ugarit/blob/bcc2c511da375c5369da3624a208a5e2149af4dc/kibana.conf)
       
* added the defautl user "elastic" in nginx for accessing kibana, using the following command:  
 ```
sudo htpasswd -c /etc/nginx/htpasswd.users elastic
```

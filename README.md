# ugarit devops task 

* I have installed elastic search and kibana (both version 8.2.0) on my pc on ubuntu 18. 

* added user test with the role safee.  

* configured Nginx to run as reverse http proxy, to be able to access Kibana on port 8888. please check [kibana.conf](https://github.com/Dina-Adel-1302/ugarit/blob/bcc2c511da375c5369da3624a208a5e2149af4dc/kibana.conf) it's in /etc/nginx/conf.d
       
* added the defautl user "elastic" in nginx for accessing kibana, using the following command:  
 ```
sudo htpasswd -c /etc/nginx/htpasswd.users elastic
```
![](https://github.com/Dina-Adel-1302/ugarit/blob/a6ee7045796dc6e6f1ed87acea3fe32042579f9a/screen_shots/Screenshot%20from%202022-12-04%2020-32-43.png)
![](https://github.com/Dina-Adel-1302/ugarit/blob/a6ee7045796dc6e6f1ed87acea3fe32042579f9a/screen_shots/Screenshot%20from%202022-12-04%2020-34-08.png)

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


## metricbeat.yml / created keystores for the password and the http certificate
![](https://github.com/Dina-Adel-1302/ugarit/blob/007ead8b3387f42a8ac3c2c9a52bb353db55dc60/screen_shots/Screenshot%20from%202022-12-05%2012-21-40.png)

## issue #1: nginx status is not configured by default, so i had to configure it manually.
## nginx_status.conf in /etc/nginx/conf.d
![](https://github.com/Dina-Adel-1302/ugarit/blob/98d72fd5ba36edf3e2495886bcdcb04986e89689/screen_shots/Screenshot%20from%202022-12-07%2010-08-21.png)

## testing via curl http://127.0.0.1:81/nginx_status
![](https://github.com/Dina-Adel-1302/ugarit/blob/a60e509c1e6bd8385d1d4f475c51f6c98c68e81c/screen_shots/Screenshot%20from%202022-12-07%2010-18-42.png)

## nevertheless metric beat is not able to fetch nginx status.
## metricbeat dashboard / nginx module 
![](https://github.com/Dina-Adel-1302/ugarit/blob/98d72fd5ba36edf3e2495886bcdcb04986e89689/screen_shots/Screenshot%20from%202022-12-07%2010-05-29.png)

## metricbeat module nginx.yml
![](https://github.com/Dina-Adel-1302/ugarit/blob/98d72fd5ba36edf3e2495886bcdcb04986e89689/screen_shots/Screenshot%20from%202022-12-07%2010-04-19.png)

## metricbeat dashboard / system module
![](https://github.com/Dina-Adel-1302/ugarit/blob/98d72fd5ba36edf3e2495886bcdcb04986e89689/screen_shots/Screenshot%20from%202022-12-07%2010-06-28.png)
![](https://github.com/Dina-Adel-1302/ugarit/blob/98d72fd5ba36edf3e2495886bcdcb04986e89689/screen_shots/Screenshot%20from%202022-12-07%2010-06-33.png)


## filebeat.yml / created keystores for the password and the http certificate
![](https://github.com/Dina-Adel-1302/ugarit/blob/b6cc2fbdd0b6a189cbce4f7d62859d53a6997b5d/screen_shots/Screenshot%20from%202022-12-05%2012-54-56.png)


## filebeat dashboard / system module
![](https://github.com/Dina-Adel-1302/ugarit/blob/803325522d5170f8669cf5f183b1ba18507814b7/screen_shots/Screenshot%20from%202022-12-07%2008-27-45.png)

## filebeat dashboard / auditd module
![](https://github.com/Dina-Adel-1302/ugarit/blob/803325522d5170f8669cf5f183b1ba18507814b7/screen_shots/Screenshot%20from%202022-12-07%2008-28-57.png)

## heartbeat.yml
![](https://github.com/Dina-Adel-1302/ugarit/blob/42b177a12a0812bb503b2296873407f37727464b/screen_shots/Screenshot%20from%202022-12-05%2021-53-42.png)

## issue #2: heartbeat is showing that elasticsearch is down
## heartbeat uptime interface 
![](https://github.com/Dina-Adel-1302/ugarit/blob/843c88938fb3514e1243416e040dd77b81f9663f/screen_shots/Screenshot%20from%202022-12-05%2023-12-48.png)

## dashboard 1
![](https://github.com/Dina-Adel-1302/ugarit/blob/9edbcd8f8879e2559f1a787ba27fa20405375c66/screen_shots/dashboard1/Screenshot%20from%202022-12-06%2001-43-48.png)
![](https://github.com/Dina-Adel-1302/ugarit/blob/9edbcd8f8879e2559f1a787ba27fa20405375c66/screen_shots/dashboard1/Screenshot%20from%202022-12-06%2011-42-35.png)

## dashboard 2 / I don't have SSH history so i used sudo commands history instead
![](https://github.com/Dina-Adel-1302/ugarit/blob/9edbcd8f8879e2559f1a787ba27fa20405375c66/screen_shots/dashboard2/Screenshot%20from%202022-12-06%2011-47-27.png)
![](https://github.com/Dina-Adel-1302/ugarit/blob/9edbcd8f8879e2559f1a787ba27fa20405375c66/screen_shots/dashboard2/Screenshot%20from%202022-12-06%2011-52-42.png)

## Safee priviliges 
![](https://github.com/Dina-Adel-1302/ugarit/blob/37517222f900eabc642aabd9318514c27ba7e22c/screen_shots/Screenshot%20from%202022-12-07%2006-42-51.png)
![](https://github.com/Dina-Adel-1302/ugarit/blob/3feb803a8a002d0f9a374830479a1e508983661a/screen_shots/Screenshot%20from%202022-12-07%2006-43-11.png)

## Elast Alert for cpu usage more than 1% via email
![](https://github.com/Dina-Adel-1302/ugarit/blob/75c694c5d3ac1beace7705234bddb5f6718ad2f5/screen_shots/elastalert/Screenshot%20from%202022-12-11%2014-36-31.png)

## Elast Alert for detecting that kibana monitor is down via email
![](https://github.com/Dina-Adel-1302/ugarit/blob/75c694c5d3ac1beace7705234bddb5f6718ad2f5/screen_shots/elastalert/Screenshot%20from%202022-12-12%2007-30-13.png)

## Elast Alert for detecting sudo command via telegram
![](https://github.com/Dina-Adel-1302/ugarit/blob/1812d4fb51f443ecb4d1fc7d95e220d016fa734c/screen_shots/elastalert/Screenshot%20from%202022-12-12%2012-43-24.png)

## Elast Alert [configuration files](https://github.com/Dina-Adel-1302/ugarit/tree/main/elastalert2)

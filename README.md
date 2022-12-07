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


## metricbeat dashboard with modules system and nginx enabled
![](https://github.com/Dina-Adel-1302/ugarit/blob/007ead8b3387f42a8ac3c2c9a52bb353db55dc60/screen_shots/Screenshot%20from%202022-12-05%2010-49-15.png)


## filebeat.yml / created keystores for the password and the http certificate
![](https://github.com/Dina-Adel-1302/ugarit/blob/b6cc2fbdd0b6a189cbce4f7d62859d53a6997b5d/screen_shots/Screenshot%20from%202022-12-05%2012-54-56.png)


## filebeat dashboard with modules system and auditd enabled
![](https://github.com/Dina-Adel-1302/ugarit/blob/8893a8c142624e3016b3e0c6678e30408b2461a7/screen_shots/Screenshot%20from%202022-12-05%2020-29-56.png)

## heartbeat.yml
![](https://github.com/Dina-Adel-1302/ugarit/blob/42b177a12a0812bb503b2296873407f37727464b/screen_shots/Screenshot%20from%202022-12-05%2021-53-42.png)

## heartbeat uptime interface 
![](https://github.com/Dina-Adel-1302/ugarit/blob/843c88938fb3514e1243416e040dd77b81f9663f/screen_shots/Screenshot%20from%202022-12-05%2023-12-48.png)

## dashboard 1
![](https://github.com/Dina-Adel-1302/ugarit/blob/9edbcd8f8879e2559f1a787ba27fa20405375c66/screen_shots/dashboard1/Screenshot%20from%202022-12-06%2001-43-48.png)
![](https://github.com/Dina-Adel-1302/ugarit/blob/9edbcd8f8879e2559f1a787ba27fa20405375c66/screen_shots/dashboard1/Screenshot%20from%202022-12-06%2011-42-35.png)

## dashboard 2 / I don't have SSH history so instead I showed sudo commands history
![](https://github.com/Dina-Adel-1302/ugarit/blob/9edbcd8f8879e2559f1a787ba27fa20405375c66/screen_shots/dashboard2/Screenshot%20from%202022-12-06%2011-47-27.png)
![](https://github.com/Dina-Adel-1302/ugarit/blob/9edbcd8f8879e2559f1a787ba27fa20405375c66/screen_shots/dashboard2/Screenshot%20from%202022-12-06%2011-52-42.png)

## Safee priviliges 
![](https://github.com/Dina-Adel-1302/ugarit/blob/37517222f900eabc642aabd9318514c27ba7e22c/screen_shots/Screenshot%20from%202022-12-07%2006-42-51.png)
![](https://github.com/Dina-Adel-1302/ugarit/blob/3feb803a8a002d0f9a374830479a1e508983661a/screen_shots/Screenshot%20from%202022-12-07%2006-43-11.png)


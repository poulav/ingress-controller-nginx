# ingress-controller-nginx

In this project, 
I have created two simple Web Servers using Nginx and hosted simple webpages on them.
 - the folder web-service-nginx contains the first website
 and the second folder web-service-nginx-2 contains the second website.
 - next, the proxy-server website has the configuration files and certificates as well as it is itself a server that is responsible for the reverse proxy. 


Few Notes While I was performing the reverse proxy,

 - To know about the host IP Address
ifconfig | grep "inet " | grep -Fv 127.0.0.1 | awk '{print $2}'

- This host ip address has to be configured under /etc/hosts
sudo vim /etc/hosts

- To display the list of networks inside docker,
docker network ls

- SSL Config ssl.config has to have ssl_ciphers in a single line


###References:

https://phoenixnap.com/kb/docker-nginx-reverse-proxy
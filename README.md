## Reverse Proxy Demo Setup using Docker and Nginx

This project demonstrates the setup of two simple web servers using Nginx, hosting straightforward webpages on them.

- The directory `web-service-nginx` contains the files for the first website.
- The directory `web-service-nginx-2` contains the files for the second website.
- The `proxy-server` directory holds the configuration files, certificates, and serves as the reverse proxy server.

### Notes on Reverse Proxy Configuration:

- To identify the host IP address:
  ```
  ifconfig | grep "inet " | grep -Fv 127.0.0.1 | awk '{print $2}'
  ```

- Configure this host IP address in `/etc/hosts`:
  ```
  sudo vim /etc/hosts
  ```

- View the list of networks within Docker:
  ```
  docker network ls
  ```

- The `ssl.config` should have `ssl_ciphers` in a single line.

### References:

[Guide on Docker Nginx Reverse Proxy](https://phoenixnap.com/kb/docker-nginx-reverse-proxy)
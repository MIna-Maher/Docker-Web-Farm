Building Dockerized Web Farm using basic web server Docker image and the hosting OS as Load Balancer.<br/>
Using the host OS as proxy server and load balancer ( installing Nginx on The Host OS ). <br/>
                    **Building The Docker Containers using the base image**.<br/>
`docker pull minamaherdocker/docker-web-farm:v1`  <br/>
                    **my Docker Bridge network subnet 10.1.0.0/16**<br/>
`docker run -itd --name baseweb1 --network minabridge --ip 10.1.0.10 -p 8081:80 minamaherdocker/docker-web-farm:v1`<br/>
`docker run -itd --name baseweb2 --network minabridge --ip 10.1.0.11 -p 8082:80 minamaherdocker/docker-web-farm:v2`<br/>
                    **Configuring host OS as proxy server (Nginx)**<br/>
#`mv deafult.conf /etc/nginx/sites-availabe/`<br/>
#`systemctl restart nginx`<br/>

Building Dockerized Web Farm using basic web server Docker image and the hosting OS as Load Balancer.
Using the host OS as proxy server and load balancer ( installing Nginx on The Host OS ). 
                    **Building The Docker Containers using the base image**.
`docker pull minamaherdocker/docker-web-farm:v1`  
                    **my Docker Bridge network subnet 10.1.0.0/16**
`docker run -itd --name baseweb1 --network minabridge --ip 10.1.0.10 -p 8081:80 minamaherdocker/docker-web-farm:v1`
`docker run -itd --name baseweb2 --network minabridge --ip 10.1.0.11 -p 8082:80 minamaherdocker/docker-web-farm:v2`
                    **Configuring host OS as proxy server (Nginx)**
#`mv deafult.conf /etc/nginx/sites-availabe/`
#`systemctl restart nginx`

# fib-cal-aws
Output during study of dockerizing multiple services developed in React, Express and NodeJS

There are multiple modules under this workout project;  
* Client (written in React)  
* Server (the API, written in ExpressJS)  
* Redis  
* Postgre
* Worker (listens Redis for updates, written in NodeJS)  
* Nginx (as reverse proxy)  
* Nginx for serving client  

All sub-modules are dockerized and multiple containers are composed by with docker compose  
Modules are deployed to AWS EBS through Travis CI  
Travis CI executes tests, builds images and pushes to Docker Hub  
Upon pushing images to docker HUB, invokes AWS deployment  


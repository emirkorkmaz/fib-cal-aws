# fib-cal-aws
Output during study of dockerizing multiple services developed in React, Express and NodeJS

There are multiple modules under this workout project;  
* Client (written in React)  
* Server (the API, written in ExpressJS)  
* Redis  (Elastic Cache is used in AWS, default VPC is used but new security group created then assigned)
* Postgre (RDS is used in AWS, default VPC is used but new security group created then assigned)
* Worker (listens Redis for updates, written in NodeJS)  
* Nginx (as reverse proxy)  
* Nginx for serving client  

All sub-modules are dockerized.
Modules are deployed to AWS EB (default VPC is used but new security group created then assigned) through Travis CI  (for testing purpose of custom cloud server, there is docker compose too)  
Travis CI executes tests, builds images and pushes to Docker Hub  
Upon pushing images to docker HUB, invokes AWS deployment  

https://travis-ci.org/emirkorkmaz/fib-cal-aws
https://hub.docker.com/u/jaqenhghar2402/
http://fibcalaws-env.u9iq5ad268.eu-central-1.elasticbeanstalk.com/
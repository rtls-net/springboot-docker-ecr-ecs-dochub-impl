### install  AWS in window machine
        
	 download AWSCLIV2 in your machine and proceed with normal software install
 
### configure aws account in aws cli

        cmd>aws configure

        provide genarated IAM acces key and secreat key

###  push image to ECR registry

       cmd> aws ecr get-login-password | docker login --username AWS --password-stdin <ecr main url without registry name>

### Build Docker image

-   if you building through maven build and spring  boot then 

	     mvn clean install

	     mvn spring-boot:build image

   -  then you need to tag docker image like 

            docker tag <image-name>:<tag-name> <ecr full registry with repo name>

###  Docker push

        docker push <ecr full registry with repo name>


 ![image](https://github.com/rtls-net/springboot-docker-ecr-ecs-dochub-impl/assets/147226341/9623d287-2145-42ad-8df5-f666fd4a20f4)







### Build Docker Image

      docker build -t <image-name> .

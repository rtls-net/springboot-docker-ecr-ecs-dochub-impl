# springboot-docker-ecs
Run your Docker image on AWS ECS (Elastic Container Service)

### Required commands

- Build Docker Image.

		mvn spring-boot:build-image
   
- Run Docker Image.

		docker run --tty --publish 8080:8080 <image-name>
    
- Tag Docker Image

		docker tag <image-name> {username}/tag-name
    
- Push Docker Image to Docker Hub

		docker push  {username}/tag-name
		
- Application Flow  

<img width="576" alt="11" src="https://user-images.githubusercontent.com/25712816/91267149-570d0780-e790-11ea-8497-806b30cbcfc2.PNG">


### should be used in ECR after push docker image to docker hub like

      docker.io/rtlsecs/springboot-docker-aws-ecs:latest---website/image/tag


### Build Docker image using Docker Command

        docker build -t <image-name> .


### Configure ECS

      - Create ECS cluster  
          -- provide cluster name and select infrastructure where you want to deploy i.e -> Fargate 

      - Assign task def by going to cluster and then Task

	     --provide TaskDefRole---->AmazonECSTaskExecutionRolePolicy

              --provide  ECR Image uri in Image section 

       - provide Security group like below

	     AllTCp
             AllTeriffic

      





